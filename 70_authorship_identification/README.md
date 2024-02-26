# 作者识别(authorship identification)

```py
# 导入string模块
import string


# 清理单词
def clean_word(word):
    """
    word是一个字符串
    返回一个字符串，它把word转成小写，去掉两头的标点符号(punctuation),
    但是保留中间的标点符号。

    >>> clean_word('Hello!')
    'hello'
    >>> clean_word('hello-world')
    'hello-world'
    """
    word = word.lower()
    return word.strip(string.punctuation)


# 计算平均单词长度
def average_word_length(text):
    """
    text是一个文本字符串。返回text中所有单词的平均长度。
    空字符串word不算单词

    >>> average_word_length('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    4.1
    """
    words = text.split()
    # 去掉空字符串
    words = [clean_word(word) for word in words if clean_word(word)]
    if len(words) == 0:
        return 0
    return sum(len(word) for word in words) / len(words)


# 计算不同单词的比例
def different_to_total(text):
    """
    text是一个文本字符串。返回text中不同单词的比例。
    空字符串word不算单词

    >>> different_to_total('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    0.7
    """
    words = text.split()
    # 去掉空字符串
    words = [clean_word(word) for word in words if clean_word(word)]
    if len(words) == 0:
        return 0
    return len(set(words)) / len(words)


# 计算只出现一次的单词的比例
def exactly_once_to_total(text):
    """
    text是一个文本字符串。返回text中只出现一次的单词的比例。
    空字符串word不算单词

    提示：使用字典判断单词是否只出现一次

    >>> exactly_once_to_total('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    0.5
    """
    words = text.split()
    # 去掉空字符串
    words = [clean_word(word) for word in words if clean_word(word)]
    if len(words) == 0:
        return 0
    word_count = {}
    for word in words:
        if word in word_count:
            word_count[word] += 1
        else:
            word_count[word] = 1
    return sum(1 for word in word_count if word_count[word] == 1) / len(words)


# 通过分隔符分割字符串
def split_string(text, separators):
    """
    text是一个文本字符串，separators是表示包含多个分隔符的字符串。
    把text按照separators中的任意一个字符进行分割后，返回结果列表。
    移除分隔后字符串两边的空格。
    空字符串不要放入列表。

    >>> split_string('one*two[three', '*[')
    ['one', 'two', 'three']
    >>> split_string('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.', '.?!')
    ['A pearl', 'Pearl', 'Lustrous pearl', 'Rare', 'What a nice find']
    """
    result = [text]
    for separator in separators:
        text, result = result, []
        for seq in text:
            result += seq.split(separator)
    return [seq.strip() for seq in result if seq]


# 获取句子
def get_sentences(text):
    """
    text是一个文本字符串。返回一个列表，其中包含text中的所有句子。
    句子由.?!结束。

    >>> get_sentences('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    ['A pearl', 'Pearl', 'Lustrous pearl', 'Rare', 'What a nice find']
    """
    return split_string(text, '.?!')


# 计算每个句子的平均单词数
def average_sentence_length(text):
    """
    text是一个文本字符串。返回text中每个句子的平均单词(word)数。
    空字符串不算单词。

    >>> average_sentence_length('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    2.0
    """
    sentences = get_sentences(text)
    if len(sentences) == 0:
        return 0
    return sum(len(sentence.split()) for sentence in sentences) / len(sentences)


# 获取句子中的短语
def get_phrase(sentence):
    """
    sentence是一个句子。返回一个列表，其中包含sentence中的所有短语。
    短语由,;:结束。

    >>> get_phrase('A pearl, Pearl; Lustrous pearl: Rare')
    ['A pearl', 'Pearl', 'Lustrous pearl', 'Rare']
    """
    return split_string(sentence, ',;:')


# 计算每个句子的平均短语数
def average_sentence_complexity(text):
    """
    text是一个文本字符串。返回text中每个句子的平均短语(phrase)数。

    >>> average_sentence_complexity('A pearl! Pearl! Lustrous pearl! Rare. What a nice find.')
    1.0
    >>> average_sentence_complexity('A pearl! Pearl! Lustrous pearl! Rare, What a nice find.')
    1.25
    """
    sentences = get_sentences(text)
    if len(sentences) == 0:
        return 0
    return sum(len(get_phrase(sentence)) for sentence in sentences) / len(sentences)


def make_signature(text):
    """
    text是一个文本字符串。返回一个列表，其中包含text的特征。
    特征包括：
    - 平均单词长度
    - 不同单词的比例
    - 只出现一次的单词的比例
    - 每个句子的平均单词数
    - 每个句子的平均短语数

    >>> make_signature('A pearl! Pearl! Lustrous pearl! Rare, What a nice find.')
    [4.1, 0.7, 0.5, 2.5, 1.25]
    """
    return [
        average_word_length(text),
        different_to_total(text),
        exactly_once_to_total(text),
        average_sentence_length(text),
        average_sentence_complexity(text)
    ]


# 获取已知作者的书的特征
def get_all_signatures(known_dir):
    """
    known_dir是一个目录，其中包含多个文本文件(书)。
    返回一个字典，其中包含每个文件的特征。
    键是文件名，值是文件的特征。
    """
    import os
    signatures = {}
    for filename in os.listdir(known_dir):
        path = os.path.join(known_dir, filename)
        with open(path, encoding='utf-8') as file:
            text = file.read()
            signatures[filename] = make_signature(text)
    return signatures


# 比较两个特征列表获取加权分数
def get_score(signature1, signature2, weights):
    """
    signature1和signature2是两个特征列表，weights是一个数字列表。
    返回signature1和signature2之间的相似度分数。

    >>> get_score([4.6, 0.1, 0.05, 10, 2], [4.3, 0.1, 0.04, 16, 4], [11, 33, 50, 0.4, 4])
    14.2
    """
    score = 0
    for i in range(len(signature1)):
        score += abs(signature1[i] - signature2[i]) * weights[i]
    return score


# 获取签名最接近的文件
def lowest_score(signature_dict, unknown_signature, weights):
    """
    signature_dict是一个字典，其中包含每个文件的特征。
    unknown_signature是一个特征列表。
    weights是一个包含五个权重的数字列表。
    返回一个文件名，它包含与unknown_signature最相似的特征。
    >>> d = {'Dan': [1, 1, 1, 1, 1], 'Leo': [3, 3, 3, 3, 3]}
    >>> unknown = [1, 0.8, 0.9, 1.3, 1.4]
    >>> weights = [11, 33, 50, 0.4, 4]
    >>> lowest_score(d, unknown, weights)
    'Dan'
    """
    best_score = None
    best_file = None
    for filename in signature_dict:
        signature = signature_dict[filename]
        score = get_score(signature, unknown_signature, weights)
        if best_score is None or score < best_score:
            best_score = score
            best_file = filename
    return best_file


# 处理数据找出作者
def process_data(mystery_filename, known_dir):
    """
    mystery_filename是一个文件名，它的作者需要被确定。
    know_dir是一个目录，其中包含已知作者的文本(书)。
    返回mystery_filename的作者。

    weights = [11, 33, 50, 0.4, 4]
    """
    known_signatures = get_all_signatures(known_dir)
    with open(mystery_filename, encoding='utf-8') as file:
        text = file.read()
        signature = make_signature(text)
        return lowest_score(known_signatures, signature, [11, 33, 50, 0.4, 4])


# 猜测作者
def make_guess(known_dir):
    """
    请求用户输入输入一个文件名。
    获取所有已知作者的书的特征。
    输出文件名的作者。
    """
    mystery_filename = input('Enter the filename of the mystery novel: ')
    print('The author of the mystery novel is', process_data(mystery_filename, known_dir))


make_guess('known_authors')
```
