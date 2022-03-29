# Listado de Regex Utiles

El siguiente listado de Regex solo tiene como fin un uso propio

## General Useful Regex

.*(options).*

## Amazon Regex
mediamarkt|cambiar| no |walmart|milanuncios|uso|tienda casa|corte ingles|du|zara|walmart|antena 3|formula 1|tv|busco|ok|motogp|carrefour|aldi|forocoches|oferta|ofertas|configurar|instrucciones|bricomart|montar|qual|ç|leroy|codigo|minecraft|instalacion|app|descargar|gif|arduino|abrir|jpg|esquema|png|aiho|lidl|segunda mano|wikipedia|probar|ver|medida| y |que|como|usa|comprar|leroy merlin|ikea|bricodepot|mejor| o |media markt|opini|vs|precio|amazon|balay|crisol|alcampo|wallapop|tutorial|video|quitar|klarstein|hacer|teka|hipercor|aki|el corte ingles|el corte inglés| q |youtube|mercado libre|la tienda en casa| + | - | e |para|aliexpress|barat(a|o)s?|mano a mano|walmart|corte ingles|por [0-9][0-9] euros|mil anuncios|merkamueble|manoamano|conforama|ventas?| tipo |primark|vendo|outlet
(mediamarkt|cambiar| no |walmart| en | por |baratas|baratos|online|tipos|quito|venta|milanuncios|uso|tienda casa|corte ingles|du|zara|walmart|antena 3|formula 1|tv|busco|ok|motogp|carrefour|aldi|forocoches|oferta|ofertas|configurar|instrucciones|bricomart|montar|qual|ç|leroy|codigo|minecraft|instalacion|app|descargar|gif|arduino|abrir|jpg|esquema|png|aiho|lidl|segunda mano|wikipedia|probar|ver|medida| y |que|como|usa|comprar|leroy merlin|ikea|bricodepot|mejor| o |media markt|opini|vs|precio|amazon|balay|crisol|alcampo|wallapop|tutorial|video|quitar|klarstein|hacer|teka|hipercor|aki|el corte ingles|el corte inglés| q |youtube|mercado libre|la tienda en casa| + | - | e |para|aliexpress)

## Provincias Regex
A Coruña|Álava|Albacete|Alicante|Almería|Asturias|Ávila|Badajoz|Baleares|Barcelona|Burgos|Cáceres|Cádiz|Cantabria|Castellón|Ciudad Real|Córdoba|Cuenca|Girona|Granada|Guadalajara|Gipuzkoa|Huelva|Huesca|Jaén|La Rioja|Las Palmas|León|Lérida|Lugo|Madrid|Málaga|Murcia|Navarra|Ourense|Palencia|Pontevedra|Salamanca|Segovia|Sevilla|Soria|Tarragona|Santa Cruz de Tenerife|Tenerife|Teruel|Toledo|Valencia|Valladolid|Vizcaya|Zamora|Zaragoza|a coruña|álava|albacete|alicante|almería|asturias|ávila|badajoz|baleares|barcelona|burgos|cáceres|cádiz|cantabria|castellón|ciudad real|córdoba|cuenca|girona|granada|guadalajara|gipuzkoa|huelva|huesca|jaén|la rioja|las palmas|león|lérida|lugo|madrid|málaga|murcia|navarra|ourense|palencia|pontevedra|salamanca|segovia|sevilla|soria|tarragona|santa cruz de tenerife|teruel|toledo|valencia|valladolid|vizcaya|zamora|zaragoza|tenerife

## HTML Regex

### Strip HTML Comments

<!--(.*?)-->

### Table

<td\s*.*>\s*.*<\/td>

<table\s*.*>\s*.*<\/table>

### SEO

## Match all queries that contain a word

.*seo.*

## Match short query patterns of less than 10 characters

^[\w\W\s\S]{1,10}$

## Match any query longer than 50 characters

^[\w\W\s\S]{50,}$

## Find search, clicks, impressions for specific non HTML assets

\.docx|\.pdf|\.rtf|\.xls

## Match Word or Phrase in a List

(?i)(\W|^)(foo|bar|foo\sbar)(\W|$)

## Matches all queries that contain certain strings

^.*(google|google search).*$

## Filter page URLs longer than 100 characters

^[\w\W\s\S]{100,}$

## Show URLs that do or do not contain the trailing slash

.*\/$

## All urls between a certain slug and ending

(http|https):\/\/www.example.com\/slug\/[^\/]+\/page

## All urls within /word

(http|https):\/\/www.example.com\/word\/.*

## Check if WordPress admin URLs are indexed

.*wp-.*Matches URL slug:^[foo]+(?:-[bar]+)*$

## Transactional Intent

.*(buy|cheap|price|purchase|order).*

## Commercial Intent

.*(best|top|vs|review*).*

## Navigational Intent

.*brand.*

## Informational Intent

who|what|where|when|why|how|was|did|do|is|are|aren’t|won’t|does|if|can|could|should|would|won’t|were|weren’t|shouldn’t|couldn’t|cannot|can’t|didn’t|did not|does|doesn’t|wouldn’t

### Remove empty HTML Tags

<.[^>]*>(\s+|()|(&nbsp;)*|\s+(&nbsp;)*|(&nbsp;)*\s+|\s+(&nbsp;)*\s+)<\/.[^>]*>

### Find external links

<(a+) (?!(?:href=(["|']+)([http:\/\/])*link\.com([\/])?(.*?)["|'])) *[^>]*>(.*?)[^>]>

## Match Google and YouTube Querys

^https?:\/\/(www\.google\..+|\w+\.youtube\.com).*$

## Capture a query string

((?<=[\?\&])foo\=[^\&\#]*)|((?<=[\?\&])foo(?=[\&\#]))|((?<=[\?\&])foo(?!.))

## Match Phone Number

(\+91[\s-]\d{5}[\s-]\d{5})|(011[\s-]\d{8})|(\+91\d{2}[\s-]\d{8})|(^0\d{10})|(^[6-9]\d{9})|(91[\s-]\d{3,5}[\s-]\d{2,5}[\s-]\d{4})|(91[\s-]\d{5}[\s-]\d{5})|(91[\s-]\d{10})|(\d{4}[\s-]\d{4}[\s-]\d{3})

## Password Validator

^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$

## Split a URL

(?<url>(?:(?<scheme>[a-zA-Z]+:\/\/)?(?<hostname>(?:[-a-zA-Z0-9À-ÖØ-öø-ÿ@%_\+~#=]{1,256}\.){1,256}(?:[-a-zA-Z0-9À-ÖØ-öø-ÿ@%_\+~#=]{1,256})))(?::(?<port>[[:digit:]]+))?(?<path>(?:\/[-a-zA-Z0-9!$&'()*+,\\\/:;=@\[\]._~%]*)*)(?<query>(?:(?:\#|\?)[-a-zA-Z0-9!$&'()*+,\\\/:;=@\[\]._~]*)*))

## Extract Domain from URL

^(?:https?:\/\/)?(?:[^@\/\n]+@)?(?:www\.)?([^:\/?\n]+)
  
## Match a URL with http or https
  
https?:\/\/(?:[[:alnum:]]+\.)?[[:alnum:]]+\.[A-Za-z]{3})(\/\S*
  
### For Js
  
https?:\/\/(www\.)?[A-Za-z0-9]{1,50}\.[A-Za-z]+(\/)?\S.*
  
## Email Verificator

^(?=[a-z][a-z0-9@._-]{5,40}$)[a-z0-9._-]{1,20}@(?:(?=[a-z0-9-]{1,15}\.)[a-z0-9]+(?:-[a-z0-9]+)*\.){1,2}[a-z]{2,6}$
  
## Take anchors
  
href="(?:https:\/\/res\.cloudinary).*?"

## Take IP Port
  
([^\:\n,]+:\d+,?)+
  
## Cut HTTP protocol from a domain
  
https?:\/\/(?:[-\w]+\.)?([-\w]+)\.\w+(?:\.\w+)?\/?.*/i
  
## Leading & Trailing Whitespace
  
^[ \s]+|[ \s]+$
  
## Line does not contains specific string
  
^(?!.*\bstring.*\b).*
  
## Line contains specific string
  
^(.*\bstring.*\b).*
  
### Sort KW by Length

### 1-word keyword
  
^[^\s]*$
  
### 2-word keyword
  
^[^\s]*\s[^\s]*$
 
### 3-word keyword
  
^([^\s]*\s){2}[^\s]*$
  
### 5-words-and-more keywords 
  
^([^\s]*\s){4}[^\s]*$ 

## Useful Regex Articles

1. [Google Regex - Lino](https://www.mecagoenlos.com/Posicionamiento/expresiones-regulares-en-google.php)
2. [Regex - Esteve Castells](https://gist.github.com/estevecastells/436c2a89277f757bcb38ae900fdac71e)
3. [SEO Regex](https://www.jcchouinard.com/regex-for-seo/)
4. [HTML Tags](https://networking.ringofsaturn.com/Web/removetags.php)
5. [GA Regex](https://www.optimizesmart.com/regular-expression-guide-for-seos/)
5. [GA Regex](https://online-metrics.com/regular-expressions/)
6. [GTM Regex](https://measureschool.com/regular-expressions-google-tag-manager/)
7. [MJ Chacon - Useful Regex for Screaming Frog](https://twitter.com/mjcachon/status/1440290214765678603)

