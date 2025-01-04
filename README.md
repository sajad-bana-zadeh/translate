
Key Features Section:
    Highlight the main features of your project. Use bullet points for clarity and ease of reading. For example:
    Automated Translation using Google Translate API.
    User-Friendly Interface.
    Batch Processing capabilities.
    Language Support focusing on English to Persian.

# English to Persian Subtitle Translator

A tool designed to translate English subtitles into Persian, enhancing accessibility for Persian-speaking audiences. This project utilizes advanced translation APIs and libraries to ensure high-quality translations.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install googletrans
```

## Usage and code

```python
from googletrans import Translator

# read English file
with open("en.srt", 'r') as lines:
    content = lines.readlines()

# Translator
for index, item in enumerate(content):
    if item == '\n':
        async with Translator() as translator:
            result = await translator.translate(text=content[index-1], src='en', dest='fa')
            content[index-1] = result.text + '\n'

# save Persian file
with open('fa.srt', 'w') as file:
    for line in content:
        # Write the string followed by a newline character
        file.write(line)
```
