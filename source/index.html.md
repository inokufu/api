---
title: API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - php
  - javascript


toc_footers:
  - <a href="mailto:contact@inokufu.com?subject=Inokufu API Key request&body=Hi,%0D%0A %0D%0A I found your awesome Inokufu API Cloud and I would be very intersted to get a Key!%0D%0A %0D%0A My name is .... and I'd like to get a free API key for testing purpose / paid API key for integrating it in my app/project. %0D%0A %0D%0A Regards, %0D%0A ...">Ask a Developer Key 🔑 here</a>
  - <a href="http://www.inokufu.com/">Made with ❤️ by Inokufu</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Inokufu API Cloud 🎉

This API documentation shows you how to access our API endpoints, which can get information about Learning Objects in our index. This index has currently more than 700k learning objects from various sources such as YouTube, Coursera, edX, Apple podcasts, Google Play store, etc.

You can view shell, python, php and JavaScript code examples in the dark area to the right. You can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "x-api-key: SAY-FRIEND-AND-ENTER"
```

```python
import requests
url = 'api_endpoint_here'
headers = {'x-api-key': 'SAY-FRIEND-AND-ENTER'}
r = requests.get(url, headers=headers)
r.json()
```

```php
$key = 'SAY-FRIEND-AND-ENTER';
$curl = curl_init('api_endpoint_here');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
curl_setopt($curl, CURLOPT_HTTPHEADER, array('x-api-key:'.$key));
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const search = async () => {fetch('api_endpoint_here', {headers: {"x-api-key": apiKeySecured}} ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```

> Make sure to replace `SAY-FRIEND-AND-ENTER` with your own Developer API key.

Inokufu API Cloud uses API keys to allow access to our API. You can register for a Developer API key by sending us an email at [contact@inokufu.com](mailto:contact@inokufu.com?subject=Inokufu API Key request&body=Hi,%0D%0A %0D%0A I found your awesome Inokufu API Cloud and I would be very intersted to get a Key!%0D%0A %0D%0A My name is .... and I'd like to get a free API key for testing purpose / paid API key for integrating it in my app/project. %0D%0A %0D%0A Regards, %0D%0A ...).

Inokufu API Cloud expects for the API key to be included in API requests to the server in a header that looks like the following:

`x-api-key: SAY-FRIEND-AND-ENTER`

<aside class="notice">For Demo purpose, you can use this API key : <code>demo29331806e87fe8d34d03ddaad2b1b454b58a5b9d4f1385d4f86bb321</code> but beware both request speed and number of daily calls are limited with this key. </aside> 

## Usage plans

Free Developer API keys are available on request at [contact@inokufu.com](mailto:contact@inokufu.com?subject=Inokufu API Key request&body=Hi,%0D%0A %0D%0A I found your awesome Inokufu API Cloud and I would be very intersted to get a Key!%0D%0A %0D%0A My name is .... and I'd like to get a free API key for testing purpose. %0D%0A %0D%0A Regards, %0D%0A ...) and enable you to make up to 500 calls per month. Perfect for experimenting or building a new edtech app!

For higher monthly request quota and request speed, we offer paid usage plan starting at $99/month. Feel free to get in touch at [contact@inokufu.com](mailto:contact@inokufu.com?subject=Inokufu API Key request&body=Hi,%0D%0A %0D%0A I found your awesome Inokufu API Cloud and I would be very intersted to get a Key!%0D%0A %0D%0A My name is .... and I'd like to get a paid API key for integrating it in my app/project. %0D%0A %0D%0A Regards, %0D%0A ...). We are fully dedicated to the success of our customers and partners. Together we can make education better. 😊

Several usage plans are available depending on your needs.

Usage plan | Free | Lite | Pro | Custom
--- | :-:  | :-: | :-: | :-:
Request speed |  10 call/s | 100 call/s | 500 call/s | >> 500 call/s
Monthly limit | 500 calls | 10k calls | 100k calls | >> 100k calls
Search by keywords | ✔️ | ✔️ |  ✔️ | ✔️
Search by ROME | - | ✔️ |  ✔️ | ✔️
Search by Formacode® | - | ✔️ |  ✔️ | ✔️
Support | - | email |  email (48h) | email + phone (24h/7)
Monthly pricing | 0 | $99 | $499 | On quote 

<aside class="warning">
Replace <code>SAY-FRIEND-AND-ENTER</code> with your own Developer API key to make more requests.
</aside>


# Utility
## Type


```shell
curl "https://api.inokufu.com/v1/type"
```

```python
import requests
r = requests.get('https://api.inokufu.com/v1/type')
r.json()
```

```php
$curl = curl_init('https://api.inokufu.com/v1/type');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const type = async () => {fetch('https://api.inokufu.com/v1/type' ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```

> The above command returns JSON structured like this:

```json
[
  {
    "type": "video",
    "description": "Educational videos from providers such as YouTube, Dailymotion, Vimeo, etc."
  },
  {
    "type": "mooc",
    "description": "Massive Open Online Course (MOOC) from providers such as edX, Coursera, OpenClassrooms, Linkedin Learning, etc."
  },
  {
    "type": "podcast",
    "description": "Educational audio file from providers such as ApplePodcasts, SoundCloud."
  },
  {
    "type": "app",
    "description": "Educational app or app that are useful for learning a new skill of job, from providers such as App Store, Google Play Store."
  }
]
```

This endpoint retrieves a list of the types of LO currently supported.   

Type | Example of providers 
--------- | ------- 
`video` | YouTube, Dailymotion, Vimeo 
`mooc` | edX, Coursera, OpenClassrooms, Linkedin Learning 
`podcast` | ApplePodcasts, SoundCloud 
`app` | App Store, Google Play Store 

### HTTP Request

`GET https://api.inokufu.com/v1/type`

### Query Parameters

This endpoint does not require any query parameter. 

<aside class="success">More types such as books, trainings, distance learnings and articles will be added in the upcoming weeks. </aside>

## Bloom

```shell
curl "https://api.inokufu.com/v1/bloom"
```

```python
import requests
r = requests.get('https://api.inokufu.com/v1/bloom')
r.json()
```

```php
$curl = curl_init('https://api.inokufu.com/v1/bloom');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const bloom = async () => {fetch('https://api.inokufu.com/v1/bloom' ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```
> The above command returns JSON structured like this:

```json
[
  {
    "bloom": "discover",
    "description": "These LO are the first step to discover a job or a skill. You'll be able to talk about it, to know the basics. You'll have all the knowledge to decide wether it's for you or not."
  },
  {
    "bloom": "understand",
    "description": "These LO help you better understand this job or skill, in details. You'll dive deeper in the theory. You'll be able to explain, estimate, At the end, you'll be a master of the theoretical aspects."
  },
  {
    "bloom": "do",
    "description": "These LO help you put into practice what you have learned. You'll make, manipulate, simulate. You are applying what you learn."
  },
  {
    "bloom": "curriculum",
    "description": "These LO train you to a specific job or skill at a professional level. From Discovery, Understanding to Doing, at the end you are a Pro."
  }
]
```

This endpoint retrieves a list of the levels of learning objectives associated to a LO and currently supported. These levels are adapted from those of [Bloom's taxonomy](https://en.wikipedia.org/wiki/Bloom%27s_taxonomy). `discover` is used as a synonym of knowledge, `understand` for comprehension and `do` for application. `curriculum` was added as a compound level for LO that include the three other levels (`discover`, `understand`, `do`) in a coherent way (e.g. University degree).  

Bloom | Learning objective 
--------- | ------- 
`discover` | First step to discover a job or a skill. Memorize knowledge.
`understand` | Understanding a job or skill, in details. Being able to explain, estimate.
`do` | Put into practice what has been learned. Make, manipulate, simulate.
`curriculum` | Complete training to a specific job or skill at a professional level.

### HTTP Request

`GET https://api.inokufu.com/v1/bloom`

### Query Parameters

This endpoint does not require any query parameter.

<aside class="success">Higher levels of learning objectives are not yet implemented (analysis, synthesis, evaluation) but are definitely on our roadmap.</aside>
## Language

```shell
curl "https://api.inokufu.com/v1/lang"
```

```python
import requests
r = requests.get('https://api.inokufu.com/v1/lang')
r.json()
```

```php
$curl = curl_init('https://api.inokufu.com/v1/lang');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const lang = async () => {fetch('https://api.inokufu.com/v1/lang' ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```
> The above command returns JSON structured like this:

```json
[
  {
    "lang": "en",
    "description": "Use this code for LO in english language."
  },
  {
    "lang": "fr",
    "description": "Use this code for LO in french language (français)."
  }
]
```

This endpoint retrieves a list of the languages currently supported. Inokufu API cloud uses ISO 2 Letter Language Codes for every endpoints with `lang` as a query parameter.  

Lang code | Language 
--- | :-:  
`en` | english
`fr` | french 

### HTTP Request

`GET https://api.inokufu.com/v1/lang`

### Query Parameters

This endpoint does not require any query parameter.


<aside class="success">
More languages will be added in the upcoming months!
</aside>


# Learning Objects (LO)


## Search by keywords

```shell
curl "https://api.inokufu.com/v1/search?keywords=python&bloom=understand&type=mooc&lang=en&max=2"
  -H "x-api-key: SAY-FRIEND-AND-ENTER"
```

```python
import requests
url = 'https://api.inokufu.com/v1/search?keywords=python&bloom=understand&type=mooc&lang=en&max=2'
headers = {'x-api-key': 'x-api-key: SAY-FRIEND-AND-ENTER'}
r = requests.get(url, headers=headers)
r.json()
```
```php
$key = 'SAY-FRIEND-AND-ENTER';
$curl = curl_init('https://api.inokufu.com/v1/search?keywords=python&bloom=understand&type=mooc&lang=en&max=2');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
curl_setopt($curl, CURLOPT_HTTPHEADER, array('x-api-key:'.$key));
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const search = async () => {fetch('https://api.inokufu.com/v1/search?keywords=python&bloom=understand&type=mooc&lang=en&max=2', {headers: {"x-api-key": apiKeySecured}} ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```


> The above command returns JSON structured like this:

```json
{
    "statusCode": 200,
    "request": {
        "keywords": "python",
        "lang": "en",
        "type": "mooc",
        "sort": "best",
        "max": 2,
        "bloom": "understand",
        "model": "strict"
    },
    "response": [
        {
            "item": 0,
            "title": "Using Python for Research",
            "url": "https://www.edx.org/course/using-python-for-research-2",
            "pictureFullwidth": "https://prod-discovery.edx-cdn.org/media/course/image/c9d14131-a515-462b-82e2-6eaec5bc1c17-f7c5de2ca2ae.small.jpg",
            "pictureSquare": "nan",
            "provider": "Harvard University , edX",
            "learningTimeUnit": "h",
            "learningTimeValue": 480.0
        },
        {
            "item": 1,
            "title": "Python Basics for Data Science",
            "url": "https://www.edx.org/course/python-basics-for-data-science-2",
            "pictureFullwidth": "https://prod-discovery.edx-cdn.org/media/course/image/381a0046-5d78-4790-8776-74620d59f48e-48611c7ca556.small.png",
            "pictureSquare": "nan",
            "provider": "IBM , edX",
            "learningTimeUnit": "h",
            "learningTimeValue": 40.0
        }
    ]
}
```

This endpoint retrieves a list of LO based on the query parameters. 

LO can be searched and filtered by keywords, type, bloom level and language.

### HTTP Request

`GET https://api.inokufu.com/v1/search`

### Query Parameters

Query parameters must be included in URL.

Parameter | Default | Required | Description
--------- | :-: | :-: | -----------
`keywords` | | Yes | Keywords to be searched in LO title. Must be URL encoded (e.g. replacing spaces by `%20`).
`lang` |  | Yes | Currently supported languages are `en` or `fr`.
`type` | | No | Currently supported types are `video`, `mooc`,`podcast` or `app`. If empty, response will include LO of any type.
`bloom` | | No | Currently supported Bloom levels are `discover`, `understand`,`do` or `curriculum`. If empty, response will include LO of any Bloom level.
`sort` | `best` | No | Currently supported sorting order are `random` or `best`. If empty, response will be sorted by relevancy (i.e. `best`).
`max` |  | Yes | The maximum number of LO in response. Limited to 10.
`model` | `strict` | No | Two models are available: `strict` or `extended`. `strict` tends to return less results but closer to the query keywords. `extended` tends to return more results by taking the broader meaning of the query keywords. If empty, `strict` model is used by default. 

API key must be included in a header that looks like the following:

`x-api-key: SAY-FRIEND-AND-ENTER`

<aside class="notice">For Demo purpose, you can use this API key : <code>demo29331806e87fe8d34d03ddaad2b1b454b58a5b9d4f1385d4f86bb321</code> but beware both request speed and number of daily calls are limited with this key. </aside> 

<aside class="success">
For higher request quota and speed, replace <code>SAY-FRIEND-AND-ENTER</code> with your own Developer API key.</aside>

### Response Parameters

Parameter |  Description
--------- | -----------
`title` | Title of the LO.
`url` | Link to the LO webpage.
`pictureFullwidth` | Link to the picture of the LO in landscape format. Return `nan` when not applicable (N/A) or missing value.
`pictureSquare` | Link to the picture of the LO in square or portrait format. Return `nan` when not applicable (N/A) or missing value.
`provider` | Entity providing or hosting the LO.
`learningTimeUnit` | Unit of time associated to the learning time of the LO.
`learningTimeValue` | Learning time of the LO. Return `-1` when not applicable (N/A) or missing value.

<aside class="success">
More API endpoints are under development. Feel free to reach us at contact@inokufu.com if you have specific need or idea. </aside>

## Search by ROME

```shell
curl "https://api.inokufu.com/v1/searchrome?rome=H2605&lang=fr&max=3"
  -H "x-api-key: SAY-FRIEND-AND-ENTER"
```

```python
import requests
url = 'https://api.inokufu.com/v1/searchrome?rome=H2605&lang=fr&max=3'
headers = {'x-api-key': 'x-api-key: SAY-FRIEND-AND-ENTER'}
r = requests.get(url, headers=headers)
r.json()
```

```php
$key = 'SAY-FRIEND-AND-ENTER';
$curl = curl_init('https://api.inokufu.com/v1/searchrome?rome=H2605&lang=fr&max=3');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
curl_setopt($curl, CURLOPT_HTTPHEADER, array('x-api-key:'.$key));
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const searchrome = async () => {fetch('https://api.inokufu.com/v1/searchrome?rome=H2605&lang=fr&max=3', {headers: {"x-api-key": apiKeySecured}} ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```

> The above command returns JSON structured like this:

```json
{
    "statusCode": 200,
    "request": {
        "rome": "H2605",
        "lang": "fr",
        "type": "",
        "sort": "",
        "max": 3,
        "bloom": "",
        "model": "strict"
    },
    "response": [
        {
            "item": 0,
            "title": "Les composants électroniques  L'électronique de zéro ...",
            "url": "https://openclassrooms.com/fr/courses/724810-lelectronique-de-zero/721680-les-composants-electroniques",
            "pictureFullwidth": "https://static.oc-static.com/prod/courses/course_teaser_picture_default.jpg",
            "pictureSquare": "https://static.oc-static.com/prod/courses/course_teaser_picture_default.jpg",
            "provider": "OpenClassrooms",
            "learningTimeUnit": "h",
            "learningTimeValue": 0.3469499999999999
        },
        {
            "item": 1,
            "title": "La diode  L'électronique de zéro",
            "url": "https://openclassrooms.com/fr/courses/724810-lelectronique-de-zero/724552-la-diode",
            "pictureFullwidth": "https://static.oc-static.com/prod/courses/course_teaser_picture_default.jpg",
            "pictureSquare": "https://static.oc-static.com/prod/courses/course_teaser_picture_default.jpg",
            "provider": "OpenClassrooms",
            "learningTimeUnit": "h",
            "learningTimeValue": 0.3469499999999999
        },
        {
            "item": 2,
            "title": "Enseignes et afficheurs à LED",
            "url": "https://www.coursera.org/learn/enseignes-et-afficheurs-led",
            "pictureFullwidth": "https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://coursera-course-photos.s3.amazonaws.com/f3/5cdb40168111e6a053c1fc50b1e8d2/LED-2560x1440px-150dpi.jpg?auto=format,compress",
            "pictureSquare": "nan",
            "provider": "Coursera",
            "learningTimeUnit": "h",
            "learningTimeValue": 27.895
        }
    ]
}
```

This endpoint retrieves a list of LO associated to a specific ROME code. For more information about ROME code, please check [here](https://www.data.gouv.fr/en/datasets/repertoire-operationnel-des-metiers-et-des-emplois-rome/).

LO can be searched and filtered by ROME code, type, bloom level and language.

### HTTP Request

`GET https://api.inokufu.com/v1/searchrome`

### Query Parameters

Query parameters must be included in URL.

Parameter | Default | Required | Description
--------- | :-: | :-: | -----------
`rome` | | Yes | ROME code to be searched. Must be the exact ROME code starting by a uppercase letter and followed by 4 digits without any space (e.g. H2605). For the complete list of ROME code, please check [here](https://www.data.gouv.fr/en/datasets/repertoire-operationnel-des-metiers-et-des-emplois-rome/).
`lang` |  | Yes | Currently supported languages are `en` or `fr`.
`type` | | No | Currently supported types are `video`, `mooc`,`podcast` or `app`. If empty, response will include LO of any type.
`bloom` | | No | Currently supported Bloom levels are `discover`, `understand`,`do` or `curriculum`. If empty, response will include LO of any Bloom level.
`sort` | `best` | No | Currently supported sorting order are `random` or `best`. If empty, response will be sorted by relevancy (i.e. `best`).
`max` |  | Yes | The maximum number of LO in response. Limited to 10.
`model` | `strict` | No | Two models are available: `strict` or `extended2`. `strict` tends to return less results but closer to the query ROME code. `extended2` tends to return more results by taking the broader meaning of the query ROME code. If empty, `strict` model is used by default. 


API key must be included in a header that looks like the following:

`x-api-key: SAY-FRIEND-AND-ENTER`

<aside class="notice">For Demo purpose, you can use this API key : <code>demo29331806e87fe8d34d03ddaad2b1b454b58a5b9d4f1385d4f86bb321</code> but beware both request speed and number of daily calls are limited with this key. </aside> 

<aside class="success">
For higher request quota and speed, replace <code>SAY-FRIEND-AND-ENTER</code> with your own Developer API key.</aside>

### Response Parameters

Parameter |  Description
--------- | -----------
`title` | Title of the LO.
`url` | Link to the LO webpage.
`pictureFullwidth` | Link to the picture of the LO in landscape format. Return `nan` when not applicable (N/A) or missing value.
`pictureSquare` | Link to the picture of the LO in square or portrait format. Return `nan` when not applicable (N/A) or missing value.
`provider` | Entity providing or hosting the LO.
`learningTimeUnit` | Unit of time associated to the learning time of the LO.
`learningTimeValue` | Learning time of the LO. Return `-1` when not applicable (N/A) or missing value.

## Search by Formacode®

```shell
curl "https://api.inokufu.com/v1/searchformacode?formacode=15012&lang=en&max=3"
  -H "x-api-key: SAY-FRIEND-AND-ENTER"
```

```python
import requests
url = 'https://api.inokufu.com/v1/searchformacode?formacode=15012&lang=en&max=3'
headers = {'x-api-key': 'x-api-key: SAY-FRIEND-AND-ENTER'}
r = requests.get(url, headers=headers)
r.json()
```

```php
$key = 'SAY-FRIEND-AND-ENTER';
$curl = curl_init('https://api.inokufu.com/v1/searchformacode?formacode=15012&lang=en&max=3');
//Download the certificate from 'https://api.inokufu.com/v1' to avoid SSL errors and replace 'certInokufu.cer' with the name of your downloaded file
curl_setopt($curl,CURLOPT_CAINFO,__DIR__ . DIRECTORY_SEPARATOR . 'certInokufu.cer');
curl_setopt($curl, CURLOPT_HTTPHEADER, array('x-api-key:'.$key));
$data = curl_exec($curl);
if($data===false){
    var_dump(curl_error($curl));
};
```
```javascript
apiKeySecured = 'SAY-FRIEND-AND-ENTER';
const searchformacode = async () => {fetch('https://api.inokufu.com/v1/searchformacode?formacode=15012&lang=en&max=3', {headers: {"x-api-key": apiKeySecured}} ).then(function(response) {
  if(response.ok) {
      response.json().then(function(json) { 
        const resJson = JSON.stringify(json)
        //console.log(resJson);
        return resJson;
})}})};
```

> The above command returns JSON structured like this:

```json
{
    "statusCode": 200,
    "request": {
        "formacode": "15012",
        "lang": "en",
        "type": "",
        "sort": "",
        "max": 3,
        "bloom": "",
        "model": "strict"
    },
    "response": [
        {
            "item": 0,
            "title": "Presentation skills: Speechwriting and Storytelling",
            "url": "https://www.coursera.org/learn/speechwriting",
            "pictureFullwidth": "https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://coursera-course-photos.s3.amazonaws.com/95/96d7702e3311e795cc116ac5c4d4d4/story.png?auto=format,compress",
            "pictureSquare": "nan",
            "provider": "Coursera",
            "learningTimeUnit": "h",
            "learningTimeValue": 32.0
        },
        {
            "item": 1,
            "title": "Time to Shine Podcast : Public speaking | Communication skills | Storytelling",
            "url": "https://podcasts.apple.com/fr/podcast/time-to-shine-podcast-public-speaking-communication/id930870411?mt=2&app=podcast&at=1010lMK9",
            "pictureFullwidth": "nan",
            "pictureSquare": "https://is5-ssl.mzstatic.com/image/thumb/Podcasts123/v4/4f/9c/3c/4f9c3cf9-671e-c6ba-c2a9-c4610144cc57/mza_4495520741840665111.png/400x400.png",
            "provider": "Apple Podcasts",
            "learningTimeUnit": "min",
            "learningTimeValue": 21786.0
        },
        {
            "item": 2,
            "title": "Oral Communication for Engineering Leaders",
            "url": "https://www.coursera.org/learn/oral-communication",
            "pictureFullwidth": "https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://coursera-course-photos.s3.amazonaws.com/40/f608209f7311e69f58250f615c1d2a/comp-600px-2.jpg?auto=format,compress",
            "pictureSquare": "nan",
            "provider": "Coursera",
            "learningTimeUnit": "h",
            "learningTimeValue": 21.0
        }
    ]
}
```

This endpoint retrieves a list of LO associated to a specific Formacode® number. For more information about Formacode®, please check [here](https://formacode.centre-inffo.fr/spip.php?page=thesaurus).

LO can be searched and filtered by Formacode® number, type, bloom level and language.

### HTTP Request

`GET https://api.inokufu.com/v1/searchformacode`

### Query Parameters

Query parameters must be included in URL.

Parameter | Default | Required | Description
--------- | :-: | :-: | -----------
`formacode` | | Yes | Formacode® to be searched. Must be the exact 5-digits Formacode® number without any space (e.g. 15012). For the complete list of Formacode®, please check [here](https://formacode.centre-inffo.fr/spip.php?page=thesaurus).
`lang` |  | Yes | Currently supported languages are `en` or `fr`.
`type` | | No | Currently supported types are `video`, `mooc`,`podcast` or `app`. If empty, response will include LO of any type.
`bloom` | | No | Currently supported Bloom levels are `discover`, `understand`,`do` or `curriculum`. If empty, response will include LO of any Bloom level.
`sort` | `best` | No | Currently supported sorting order are `random` or `best`. If empty, response will be sorted by relevancy (i.e. `best`).
`max` |  | Yes | The maximum number of LO in response. Limited to 10.
`model` | `strict` | No | Two models are available: `strict` or `extended2`. `strict` tends to return less results but closer to the queried Formacode®. `extended2` tends to return more results by taking the broader meaning of the queried Formacode®. If empty, `strict` model is used by default. 

API key must be included in a header that looks like the following:

`x-api-key: SAY-FRIEND-AND-ENTER`

<aside class="notice">For Demo purpose, you can use this API key : <code>demo29331806e87fe8d34d03ddaad2b1b454b58a5b9d4f1385d4f86bb321</code> but beware both request speed and number of daily calls are limited with this key. </aside> 

<aside class="success">
For higher request quota and speed, replace <code>SAY-FRIEND-AND-ENTER</code> with your own Developer API key.</aside>

### Response Parameters

Parameter |  Description
--------- | -----------
`title` | Title of the LO.
`url` | Link to the LO webpage.
`pictureFullwidth` | Link to the picture of the LO in landscape format. Return `nan` when not applicable (N/A) or missing value.
`pictureSquare` | Link to the picture of the LO in square or portrait format. Return `nan` when not applicable (N/A) or missing value.
`provider` | Entity providing or hosting the LO.
`learningTimeUnit` | Unit of time associated to the learning time of the LO.
`learningTimeValue` | Learning time of the LO. Return `-1` when not applicable (N/A) or missing value.

<aside class="success">
More API endpoints are under development. Feel free to reach us at contact@inokufu.com if you have specific need or idea. </aside>

# Credits

This API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to check their awesome [repo](https://github.com/slatedocs/slate) on Github! 

ROME code is a job thesaurus developped by [Pôle Emploi](https://www.pole-emploi.fr/accueil). Check out their [website](https://www.pole-emploi.fr/employeur/vos-recrutements/le-rome-et-les-fiches-metiers.html) for more information about this thesaurus.

Formacode® is a domain of formation thesaurus developed by [Centre Inffo](https://formacode.centre-inffo.fr). Formacode® is a registered trade mark owned by Centre Inffo. Check out their [website](https://formacode.centre-inffo.fr) for more information about this thesaurus.