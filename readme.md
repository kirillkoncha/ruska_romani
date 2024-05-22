# Russian and Ruska Romani Parallel Corpus

The parallel corpus for the Ruska Romani dialect and Russian language.

Ruska Romani is the dialect of Romani language attributed to Ruska Roma, the largest subgroup of Romani people in Russia.

The corpus contains the translations of Russian literature into Ruska Romani dialect.

The corpus includes 88,742 Russian tokens and 84,635 Ruska Romani tokens, 74,291 of which were grammatically annotated.

The corpus could be used for linguistic research, including comparative and diachronic studies, bilingual dictionary creation, stylometry research, and NLP/MT tool development for Ruska Romani.

## Data

The corpus consists of Russian texts and their translations to Ruska Romani. The texts were translated in the USSR in the 1920s and 1930. The translated texts include both fiction and non-fiction domains. Both original texts and their translations are written in Cyrillic script. All the text sources and their metadata are presented in the `data` folder.

## Creation

The corpus creation involved manual alignment of a small part of translations with original works, fine-tuning a language model on the aligned pairs, and using the fine-tuned model to align the remaining data. Ruska Romani sentences were annotated using a morphological analyzer, with rules crafted for proper nouns and borrowings.

## Folders

+ `data` — aligned and annotated sentences presented in JSON and RNC-XML formats; see the folder to also find explanations of annotation tags and format structures;
+ `alignment` — code and data to finetune and use LaBSE for Ruska Romani and Russian sentence alignment;
+ `annotation` — code for grammatical annotation of Ruska Romani Sentences

