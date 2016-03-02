# RYandexTranslate

[![rstudio mirror downloads](http://cranlogs.r-pkg.org/badges/RYandexTranslate)](https://github.com/metacran/cranlogs.app)
[![cran version](http://www.r-pkg.org/badges/version/RYandexTranslate)](http://cran.rstudio.com/web/packages/RYandexTranslate)

R package to translate text using Yandex Translate API.

##Installation

To install RYandexTranslate package:

```R
library(devtools)
install_github("mukul13/RYandexTranslate")
```

To get free API key, sign up [here](https://tech.yandex.com/translate/doc/dg/concepts/api-overview-docpage/)

##Examples

To list all functions supported by RYandexTranslate package

```R
library(RYandexTranslate)
ls("package:RYandexTranslate")
```

To get a list of translation directions supported by the service

```R
api_key="YOUR API KEY"
directions=get_translation_direction(api_key)
```
To detect the language of the specified text

```R
data=detect_language(api_key,text="आप कैसे है?")
```

To translate text to the specified language

```R
data=translate(api_key,text="how are you?",lang="en-hi"  )
```

##Resources

* [Yandex Translate API doc](https://tech.yandex.com/translate/doc/dg/concepts/api-overview-docpage/)
