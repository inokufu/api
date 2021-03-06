<p align="center">
  <a href="https://inokufu.github.io/api/#introduction">
  <img src="https://github.com/inokufu/api/blob/master/source/images/logo_inokufu_API_cloud_square.svg" alt="Inokufu API Cloud Documentation " width="300"></a>
  <br>
</p>


<p align="center">Building the biggest database of Learning Objects.</p>


The API documentation page can be accessed [here](https://inokufu.github.io/api/#introduction)

Features
------------

* **Only the best** — Our indexing & data wrangling technology GNO6 uses the latest advances in NLP and Machine Learning to sort and highlight the best educational content on any topic. 

* **Multi supports** — Our objective is to index and anaylyse any learning objects available out there. Currently, our API give you access to video, moocs, podcasts and apps. Additional types of support are in preparation: books, ebooks, trainings, degrees, distance learning, articles, courses, etc  

* **Fast** — Our API were developed with speed in mind. Our cloud infrastructure was set up to handle calls at high speed (inferior to a few hundred ms) even when a call involves sorting through millions of Learning Objects. 

* **Scalable** — Wether your are working on a side project, a startup product or integrating our endpoints in a LMS used by major Universities, we have the infrastructure to handle your workload. We are an AWS Technlogy partner and our API is built according to the best practices and tools in the field.

Getting started with Inokufu API Cloud is super easy! Simply call any of our endpoint with the demo key provided in the doc or send us an email to request your own free developer API key  <a href="mailto:contact@inokufu.com?subject=Inokufu API Key request&body=Hi,%0D%0A %0D%0A I found your awesome Inokufu API Cloud and I would be very intersted to get a Key!%0D%0A %0D%0A My name is .... and I'd like to get a free API key for testing purpose / paid API key for integrating it in my app/project. %0D%0A %0D%0A Regards, %0D%0A ...">here</a>.

Getting Started with our API
------------------------------

### Check the documentation

We recommend you to take a deep look at our API documentation page, which can can be accessed [here](https://inokufu.github.io/api/#introduction)

### Utility

We have a few utility endpoints to help you set up your call parameters on other endpoints:
- Type: This endpoint retrieves a list of the types of LO currently supported.
- Bloom: This endpoint retrieves a list of the levels of learning objectives associated to a LO and currently supported. These levels are adapted from those of [Bloom's taxonomy](https://en.wikipedia.org/wiki/Bloom%27s_taxonomy):
  - `Discover` is used as a synonym of knowledge, 
  - `Understand` for comprehension,
  - `Do` for application
  - `Curriculum` was added as a compound level for LO that include the three other levels (`Discover`, `Understand`, `Do`) in a coherent way (e.g. University degree).  
- Lang: This endpoint retrieves a list of the languages currently supported (i.e. english and french) 

### Learning Objects

These endpoints enable you to search Learning Objects in our index in different ways:
- by keywords
- by ROME code
- by Formacode

### Note on Timeout

You may experience timeout during the first calls to our endpoints after a long period of inactivity when using demo or free keys. Don't worry, wait a few minutes and make your call again, everything should work as usual. There is no cold start issue when using a paid key.


Questions? Need Help? Found a bug?
--------------------

If you've got questions about our API, found a bug or just want to chat with the developers, please feel free to send us an email to [support@inokufu.com](mailto:support@inokufu.com)!


Credits
--------------------
This API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to check their awesome [repo](https://github.com/slatedocs/slate) on Github! 

ROME code is a job thesaurus developped by [Pôle Emploi](https://www.pole-emploi.fr/accueil). Check out their [website](https://www.pole-emploi.fr/employeur/vos-recrutements/le-rome-et-les-fiches-metiers.html) for more information about this thesaurus.

Formacode® is a domain of formation thesaurus developed by [Centre Inffo](https://formacode.centre-inffo.fr). Formacode® is a registered trade mark owned by Centre Inffo. Check out their [website](https://formacode.centre-inffo.fr) for more information about this thesaurus.
