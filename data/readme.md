# Data

The corpus data is presented in two formats: JSON and RNC-XML. In both format, every text is presented in a separate file.

| Russian Title          | Original Author     | Year | №. Tokens Russian | Romani Title              | Transl. Author | Transl. Year | №. Tokens Romani | JSON-file | RNC-XML-file |
|------------------------|---------------------|------|-------------------|---------------------------|----------------|--------------|------------------|-----------|--------------|
| Dubrovskij             | A. S. Pushkin      | 1833 | 19249             | Dubrovsko                 | A. Svetlovo    | 1936         | 19957            | `dubrovsky.json`          |      `dubrovsky.xml`        |
| Posle bala             | L. N. Tolstoy       | 1903 | 3103              | Koli progyya balo         | N. Pankovo     | 1936         | 2764             |`posle_bala.json`           |    `posle_bala.xml`           |
| Tri medvedya           |    L. N. Tolstoy                 | 1875 | 493               | Trin rychya               |  N. Pankovo               | 1937         | 497              | `tri_med.json`          |  `tri_med.xml`             |
| Spat' hochetsya        | A. P. Checkhov      | 1888 | 1584              | Te soves kamelpe          | A. Svetlovo    | 1934         | 1552             |     `spath_khoch.json`      |    `spath_khoch.xml`           |
| Van'ka                 |    A. P. Checkhov                  | 1886 | 1157              | Van'ka                    |  A. Svetlovo              | 1934         | 1241             |   `vanka.json`        |    `vanka.xml`          |
| Malen'kie rasskazy     | A. S. Neverov       | 1922 | 1855              | Rakiribena vash tykne chyavorenge | G. Lebedevo | 1930      | 1952             | `neverov.json`          |      `neverov.xml`        |
| V brigade proryv       | M. A. Sholokhov     | 1930 | 5126              | Dre brigada proriskiribe  | O. Pankovo     | 1934         | 5299             |    `brigada.json`       |        `brigada.xml`       |
| Esli vrag ne sdayotsya, – ego unichtozhayut | A. M. Gor'kij      | 1930 | 815               | Koli vrago na zdelape les has'kirna | M. Bezlyudskij | 1930   | 583              |   `vrago.json`        |   `vrago.xml`           |
| Strasti-mordasti       | A. M. Gor'kij                    | 1913 | 4069              | Strasti-mordasti          | A. Svetlovo    | 1934         | 4299             |      `strasti.json`     |      `strasti.xml`        |
| Druzhki                |    A. M. Gor'kij                 | 1898 | 3819              | Druzhke                   |       A. Svetlovo         | 1934         | 3200             |  `druzhki.json`         |    `druzhki.xml`          |
| Zlodei                 | A. M. Gor'kij                    | 1901 | 6390              | Zlodei                    |    A. Svetlovo            | 1934         | 6038             | `zlodei.json`          |     `zlodei.xml`         |
| Mal'va                 | A. M. Gor'kij                    | 1897 | 12146             | Mal'va                    |   A. Svetlovo             | 1934         | 12979            |     `malva.json`      |      `malva.xml`         |
| Rozhdenie cheloveka    | A. M. Gor'kij                    | 1898 | 2758              | Manusheskiro biyanype     |  A. Svetlovo              | 1935         | 2358             |  `birth.json`         |    `birth.xml`          |
| Na plotah              |  A. M. Gor'kij                   | 1895 | 3409              | Pro ploty                 |  A. Svetlovo              | 1936         | 3379             |  `ploty.json`         |       `ploty.xml`       |
| Tovarishchi            |  A. M. Gor'kij                   | 1895 | 3845              | Tovarishshi               |   A. Svetlovo             | 1937         | 3519             |  `tovar.json`         |     `tovar.xml`         |
| Makar Chudra           |  A. M. Gor'kij                   | 1892 | 6062              | Makar Chudra              |   A. Svetlovo             | 1932         | 3900             |   `cudra.json`        |      `cudra.xml`        |
| Emel'yan Pilyaj        | A. M. Gor'kij                    | 1893 | 3550              | Emel'yano Pilyaj          |   A. Svetlovo             | 1932         | 2829             |       `emelyan.json`    |     `emelyan.xml`          |
| K rabochim i krest'yanam | A. M. Gor'kij                  | 1930 | 1159             | Ko butyar'ya              | M. Bezlyudskij | 1930      | 1102             |  `ko_but.json`         |    `ko_but.xml`          |
| Son Makara             | V. G. Korolenko     | 1885 | 7613              | Makaroskiro soibe         | A. Svetlovo    | 1935         | 7187             |    `sleep.json`       |      `sleep.xml`         |
| **Total**              |                     |      | **88742**         |                           |                |              | **84635**        |           |              |

## JSON

JSON files have the following structure:

```
{
    "corpus": [
        {
            "sentence_rus": "...",
            "sentence_roma": "...",
            "sentence_id": "...",
            "words_roma": [
                [
                    {
                        "wf": "...",
                        "lemma": "...",
                        "gramm": [
                            "...",
                            "...",
                             ...
                        ],
                        "wfGlossed": "...",
                        "gloss": "...",
                        "trans_en": "...",
                        "trans": "..."
                    }
                ],
                [
                    ...
                ],
                ...
                ]

        },
        ...
  ]
}
```

Annotation fields explanation:

| **Field**        | **Description**                                     |
|------------------|-----------------------------------------------------|
| **sentence_rus**    | sentence in Russian                                |
| **sentence_roma**    | sentence in Ruska Romani                           |
| **sentence_id**      | id of a sentence                                    |
| **words_roma**       | annotations of each Ruska Romani token in a sentence|
| **wf**            | word form                                                    |
| **lemma**         | normalised form of a word                                    |
| **gramm**         | grammatical features of a word, such as part of speech, gender, case, etc |
| **wfGlossed**     | word form divided into morphological elements by hyphens     |
| **trans_en**      | English translation of a word                                |
| **trans**         | Russian translation of a word                                |

## RNC-XML

XML files have the following structure:

```
<body>
  <para id="..." id_str="...">
    <se lang="rom"><w><ana lex="..." wordf="..." gr="...,...,..." transl_ru="..."/>...</w>,<w><ana ...>...</w><w><ana ...>...</w></se>
    <se lang="ru">...</se>
  </para>
  <para>
  ...
  </para>
</body>
```
**NB:** while tokens in Ruska Romani sentences are written with containers like <w> and <ana>, sentences in Russian are written in one string without any annotations.

