<h1 align="center">How to convert JSON to Data-frame in python</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-Primeira versÃ£o-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/JTVeiga/Convert-JSON-to-DataFrame/blob/master/README.md" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="Livre" target="_blank">
    <img alt="License: Livre" src="https://img.shields.io/badge/License-Livre-yellow.svg" />
  </a>
  <a href="https://www.linkedin.com/in/jackson-tavares-veiga-37b3a36a/" target="_blank">
  </a>
</p>

> This project (Still in Development) was created with the aim of contributing to laboratory research for the standardization of raw data obtained from the database (DB). The intent of the code is to create a repository that provides the result obtained by loading a JSON file and processing the code for reading in Table format (Rows x Columns) representing the saved elements. This experiment resulted in pre-processing in phyton, using library (json) and (pandas).


### [Reference] (https://www.kindsonthegenius.com/data-science/working-with-data-json-pandas-dataframe-with-python-useful-tipcs/)

### ðŸ  [Homepage](https://github.com/JTVeiga/Convert-JSON-to-DataFrame)

### âœ¨ [Demo](https://github.com/JTVeiga/Convert-JSON-to-DataFrame/blob/master/JSONtoDataFrame.ipynb)

## Install



At the terminal, first you must clone the project (here we use the HTTP protocol, but if you prefer you can copy the project's SSH protocol link): 

```sh
git clone https://github.com/JTVeiga/Convert-JSON-to-DataFrame.git
```

2. Note that the first step will be to load the file 'D:\Python Scripts/JSON_Example.json' which is available in the project tree. Note that this must be saved in an easily accessible location on the machine and change the address 'D:\PythonScripts'.:

```sh
cd 'D:\Python Scripts/JSON_Example.json'
```

3. 
In this example, the Jupyter-Notebook application was used. In my case, I use the condas package manager, but you can use an online machine for testing, as long as it has the packages "json" and "pandas".
```sh
pip install JSON
pip install pandas
```

4. 
In pandas, the DataFrame function is used to build the two-dimensional table, having columns following this example of indexes:
```sh
df = pd.DataFrame(columns=["UserID", "ID", "Title", "Competed"])
```

5. 
The next step of the code was to create extract data from (date) that represents the elements in Json's rows and, for each attribute, organize them in the corresponding columns of the DataFrame:

```sh

for i in range (0, len(date)):
    currentItem = (date[i])
    df.loc[i] = [data[i]["userId"], data[i]["id"], data[i]["title"], data[i]["completed"]]
```

6. 
This was a simple example of extracting data from a JSON to a table, having the indexes organized according to the information extracted from each "row" element. However, it is noticed that in a complete JSON the information is chained, in this sense the search function can be improved.
I pose a challenge for those who enable creating a table of the following JSON:

```sh
{
    "glossary": {
        "title": "example glossary",
		"GlossDiv": {
            "title": "S",
			"GlossList": {
                "GlossEntry": {
                    "ID": "SGML",
					"SortAs": "SGML",
					"GlossTerm": "Standard Generalized Markup Language",
					"Acronym": "SGML",
					"Abbrev": "ISO 8879:1986",
					"GlossDef": {
                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
						"GlossSeeAlso": ["GML", "XML"]
                    },
					"GlossSee": "markup"
                }
            }
        }
    }
}

```

I hope you enjoyed!


## Author

 **Jackson T. Veiga**

Jackson T. Veiga

* CVLattes: http://lattes.cnpq.br/8939850014070884
* ORCID: https://orcid.org/0000-0003-3228-7352
* Github: [@JTVeiga](https://github.com/JTVeiga/)
* LinkedIn: [@Jackson Tavares Veiga](https://www.linkedin.com/in/jackson-tavares-veiga-37b3a36a/)

## Show your support

Give a â­ï¸ if this project helped you!

## ðŸ“ License

Copyright Â© 2021 [Jackson T. Veiga](https://github.com/JTVeiga).<br />
This project is [Livre](Livre) licensed.

***
