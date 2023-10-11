# Language-conversion
# Using python, we can convert a written text to any languages we prefer

from googletrans import Translator

text = input("Enter the text to translate: ")
language_choice = input("Enter the target language ")

### Define a dictionary to map language names to language codes
languages = {
    "spanish": 'es',
    "chinese": 'zh-CN',
    "bengali": 'bn',
    "german": 'de',
    "hindi": 'hi',
    "english": 'en',
    "italian": 'it'
}

if language_choice in languages:
    target_language = languages[language_choice]
 
    translator = Translator()

    result = translator.translate(text, dest=target_language)

    print(f'Translated to {language_choice}: {result.text}')
else:
    print("Invalid language choice.")

