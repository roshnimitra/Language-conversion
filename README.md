# Language-conversion
###Using python, we can convert a written text to any languages we prefer

'''bash
pip install googletrans
'''
'''python
from googletrans import Translator

text = input("Enter the text to translate: ")
language_choice = input("Enter the target language (e.g., Spanish, Chinese, Italian): ")

# Define a dictionary to map language names to language codes
languages = {
    "spanish": 'es',
    "chinese": 'zh-CN',
    "bengali": 'bn',
    "german": 'de',
    "hindi": 'hi',
    "english": 'en',
    "italian": 'it'
}

# Check if the user's input matches a language in the dictionary
if language_choice in languages:
    target_language = languages[language_choice]
    
    # Create a Translator object
    translator = Translator()

    # Translate the text
    result = translator.translate(text, dest=target_language)

    # Print the translation
    print(f'Translated to {language_choice}: {result.text}')
else:
    print("Invalid language choice. Please choose from Spanish, Chinese, or Italian.")
'''

