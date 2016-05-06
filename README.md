# RYandexTranslate

[![Downloads](http://cranlogs.r-pkg.org/badges/grand-total/RYandexTranslate)](http://cran.r-project.org/package=RYandexTranslate)
[![cran version](http://www.r-pkg.org/badges/version/RYandexTranslate)](http://cran.rstudio.com/web/packages/RYandexTranslate)

R package to translate text using Yandex Translate API.

##Installation

To install from CRAN repository:

```R
install.packages("RYandexTranslate")
```

To install from github:

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
```R
#>"detect_language"   "get_translation_direction"   "translate"   
```

To get a list of translation directions supported by the service

```R
api_key="YOUR API KEY"
directions=get_translation_direction(api_key)
head(directions)
```
```
#>"az-ru" "be-bg" "be-cs" "be-de" "be-en" "be-es"
```
To detect the language of the specified text

```R
data=detect_language(api_key,text="how are you?")
data
```
```R
#>"en"
```

To translate text to the specified language

```R
data=translate(api_key,text="how are you?",lang="en-hi"  )
```
```R
#>$lang
#>[1] "en-hi"
#>
#>$text
#>[1] "आप कैसे हैं?"
```
##Resources
* [Rpubs Blog link](http://www.rpubs.com/mukul13/RYandexTranslate)
* [Yandex Translate API doc](https://tech.yandex.com/translate/doc/dg/concepts/api-overview-docpage/)
