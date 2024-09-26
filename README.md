# English Vocabulary Mapper

A comprehensive JSON mapping tool for converting British English vocabulary to American English and vice versa. This repository is intended for use in projects that need consistent vocabulary localization, particularly when dealing with AI-generated text outputs.

## Source

This vocabulary list is originally sourced from the [UKGrammar UK to US Dictionary](https://ukgrammar.com/the-definitive-uk-vs-us-Vocabulary-list/), and organized into JSON format for easy integration with applications, particularly for processing outputs from AI APIs.

## Features

- Two JSON mapping files:
  - British to American Vocabulary
  - American to British Vocabulary
- 121 of the most popular mapped words and phrases between British and American English for comprehensive coverage.
- Ready-to-use for applications that require consistent English vocabulary, especially useful when working with AI API outputs that need localization.

## Use Case

This tool is particularly helpful for developers who work with AI-generated text, ensuring the output matches the required English dialect (British or American). The JSON files can be integrated into projects to automatically map vocabulary variations.

### Clone the Repository:

```bash
git clone https://github.com/mdeacey/english-vocabulary-mapper.git
```

## Files

* `british_to_american.json` - Converts British vocabularys to American vocabularys.
* `american_to_british.json` - Converts American vocabularys to British vocabularys.

## Usage

After cloning the repository, you can load the appropriate JSON file into your application to map vocabulary based on your target dialect.

Example usage with AI API outputs:

1. Obtain the text response from an AI API.
2. Map the words using the provided JSON file to convert between British and American vocabularys.
3. Return the modified text for your application.

Example in Python:

```python
import json

# Load the mapping file
with open('british_to_american.json') as f:
    british_to_american = json.load(f)

def map_Vocabulary(text, mapping):
    words = text.split()
    converted_words = [mapping.get(word, word) for word in words]
    return ' '.join(converted_words)

# Example usage
ai_output = "I'll meet you at the car park near the chemist."
converted_output = map_vocabulary(ai_output, uk_to_us)
print(converted_output)
# Output: "I'll meet you at the parking lot near the drugstore."
```

## Contributions

Contributions are welcome! If you find any missing words, phrases, or inconsistencies, feel free to open a pull request or report an issue.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
