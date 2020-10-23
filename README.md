# How to build large knowledge graphs efficiently (LKGT)
 ISWC 2020 Tutorial

## Schedule:
**November 2<sup>nd</sup>, 2020**  
**Duration:** half day (14:00-18:00 CET) 
All registered participants will receive the details regarding joining the online tutorial.

The tutorial will take about 3 hours. We reserve ~1 hour at the end for discussion and questions. Please join our Slack [workspace](https://join.slack.com/t/lkgt-iswc2020/shared_invite/zt-ipn6b9hc-~noIrcSPSO8ThrNnlblPgw) and [channel](https://app.slack.com/client/T01DQB1P8GY/C01CTPP4R4N) for the discussion session and communication regarding the tutorial. 

More information about the program can be found on [the conference's tutorial program website](https://iswc2020.semanticweb.org/)

## Abstract
Building and hosting a Knowledge Graph requires some effort and a lot of experience in semantic technologies. Turning this Knowledge Graph into a useful resource for problem solving requires even more effort. An important consideration is to provide cost‐sensitive methods to build a Knowledge Graph that is a useful resource for various applications: “There are two main goals of Knowledge Graph refinement: (a) adding missing knowledge to the graph, i.e., completion, and (b) identifying wrong information in the graph, i.e. error detection.” (Paulheim et al. 2017) This tutorial is targeting the process from knowledge creation over knowledge hosting, knowledge curation to knowledge deployment - applied to a Knowledge Graph using schema.org and domain specific extensions of schema.org as an ontology. The tutorial will be based on a book the lecturers co-authored: “Knowledge Graphs - Methodology, Tools and Selected Use Cases” (Fensel et al. 2020) and is an extended and adapted version of a tutorial the lecturers gave at [SEMANTICS2019](https://2019.semantics.cc/satellite-events/how-build-knowledge-graph) and [Knowledge Graph Conference 2020](https://www.knowledgegraph.tech/the-knowledge-graph-conference-kgc/workshops-and-tutorials/#1580503922536-633f3f10-737b).

## Demo Instructions 

### Duke

#### with Docker (Recommended)
We dockerized the Duke tool for you so you do not have to worry about the dependencies on your system. In order to use the dockerized demo:

* Set-up docker on your computer by following the [instructions](https://docs.docker.com/get-docker/) for your operating system. 
* Clone the [repository](https://github.com/STIInnsbruck/lkgt) from GitHub by running `git clone https://github.com/STIInnsbruck/lkgt` command.
* Open the command line (terminal) in the `tutorial` folder.
* Run `docker build -t duke . ` This command will use the the default docker file which directly runs the Duke tool with the example RDF document.
* Run `docker run -it duke` to run the container. 
* Use the interactive linking to detect duplicates.
* The results will be shown on your terminal.

> Alternatively, you can use the `docker build -t duke --f=Dockerfile_alt . ` command to build the image that gives you access to the linux shell, so you can play around with the tool more flexibly. If you use this option, you should run the tool as described in the **Java** instructions below.

#### with Java

For this option you would need Java installed on your computer. We have tested it with Java 8, but newer versions should also fine. If you are having issues with the dependencies, please consider running the Docker demo.

* Clone the [repository](https://github.com/STIInnsbruck/lkgt) from GitHub by running `git clone https://github.com/STIInnsbruck/kgs` command.
* Open the command line (terminal) in the `tutorial` folder.
* Run `java -jar duke-core-1.3-SNAPSHOT.jar --interactive --linkfile=out.txt config.xml`
* Use interactive linking to detect duplicates.
* View the results saved in `out.txt` in the `tutorial` folder with your favorite text editor.

### Domain Specification

A video that demonstrates the tools that work with domain specific patterns created with SHACL can be found [online](hhttps://drive.google.com/file/d/1ZrDy6vu5-jaL_OpkQo3tIBSYX1F16eMg/view?usp=sharing). Additionally, you can register to [semantify.it](https://semantify.it) and try everything yourself.

## Organizers
The presenters are experienced PhD students with several publications in the field. They also actively participate in a industry-funded project, [MindLab](https://mindlab.ai), that aims to build a Knowledge Graph for the tourism domain to be consumed by conversational agents. Moreover, the presenters have teaching experience in the field, especially with courses like Semantic Web and Semantic Web Services.

The organizers are co-authors of the book "Knowledge Graphs - Methodology, Tools and Selected Use Cases" [(Fensel et al., 2020)](https://www.springer.com/de/book/9783030374389).

### Elias Kärle
Semantic Technology Institute Innsbruck  
University Of Innsbruck  
elias[dot]kaerle[at]sti2[dot]at  
[elias.kaerle.com](https://elias.kaerle.com)

Elias Kärle is a senior PhD student at STI Innsbruck. His research is focusing on efficient publication methods for semantic data, supervised by Univ.-Prof. Dr. Dieter Fensel at the Semantic Technology Institute (STI) research group. He has been a part of the research group for five years and worked on numerous industrial and research projects. Before joining the STI he has been working as a full-stack software developer for web applications and mobile applications in the area of eTourism and eCommerce. He has (co-)authored several publications, including conference and journal articles as well as a book, about topics like scalable annotation creation, Knowledge Graph building based on schema.org annotations, and domain specific verification of semantic annotations.

### Umutcan Simsek
Semantic Technology Institute Innsbruck  
University Of Innsbruck  
umutcan[dot]simsek[at]sti2[dot]at  
[umutcan.eu](https://umutcan.eu)

Umutcan Simsek is a senior PhD student at STI Innsbruck. His research is on service-driven goal-oriented dialog systems, supervised by Univ.-Prof. Dr. Dieter Fensel. He has been a part of the research group  for 4 years and worked on several industrial and research projects at both national and EU level. He has (co-) authored several publications, including conference and journal publications as well as a book about topics like web service annotation, Knowledge Graph building based on schema.org annotations and domain-specific verification of semantic annotations. He is also a receiver of the [netidee](https://www.netidee.at/user/1154) grant in 2018 awarded by the Internet Privatstiftung Austria for the most innovative PhD and Master theses in Austria.

## Slides

to be published right after the tutorial

## Methods and Tools

### Knowledge Creation

TBD

### Knowledge Assessment

#### WIQA (Web Information Quality Assessment Framework) 
Allows defining policies to filter triples in a graph

http://wifo5-03.informatik.uni-mannheim.de/bizer/wiqa/ 

*[Bizer and Cyganiak, 2009] Bizer, C., Cyganiak, R.: Quality-driven information filtering using the WIQA policy framework. Journal of Web Semantics 7(1), 1–10 (2009). https://doi.org/10.1016/j.websem.2008.02.005*

#### SWIQA (Semantic Web Information Quality Assessment Framework)

A set of SPARQL-based rules to assess data quality

*[Fürber & Hepp, 2011] Fürber, C., Hepp, M.: Swiqa - a semantic web information quality assessment framework. In: Proceedings of the 19th European Conference on Information Systems (ECIS2011), Helsinki, Finland, June 9-11, 2011. p. 76. Association for Information Systems (AIS e Library) (2011), http://aisel.aisnet.org/ecis2011/76*

#### LINK-QA

Benefits from network features to assess data quality (e.g. counting open chains to find wrongly asserted isSameAs relationships)

*[Guéret et al., 2012] Guéret, C., Groth, P.T., Stadler, C., Lehmann, J.: Assessing linked data mappings using network measures. In: Proceedings of the 9th Extended Semantic Web Conference (ESWC2012), Heraklion, Greece, May 27-31, 2012. Lecture Notes in Computer Science, vol. 7295, pp. 87–102. Springer (2012). https://doi.org/10.1007/978-3-642-30284-8_13*

#### Sieve

Uses data quality indicators, scoring functions and assessment metrics

https://github.com/wbsg/ldif/ 

*[Mendes et al., 2012] Mendes, P.N., Mühleisen, H., Bizer, C.: Sieve: linked data quality assessment and fusion. In: Proceedings of 2nd International Workshop on Linked Web Data Management (LWDM 2012), in conjunction with the 15th International Conference on Extending Database Technology (EDBT2012): Workshops, Berlin, Germany, March 30, 2012. pp. 116–123. ACM (2012). https://doi.org/10.1145/2320765.2320803*

#### Validata

An online tool check the conformance of RDF graphs against ShEx (Shape Expressions)

https://github.com/HW-SWeL/Validata

*[Hansen et al., 2015] Hansen, J.B., Beveridge, A., Farmer, R., Gehrmann, L., Gray, A.J.G., Khutan, S., Robertson, T., Val, J.: Validata: An online tool for testing RDF data conformance. In: Proceedings of the 8th International Conference on Semantic Web Applications and Tools for Life Sciences (SWAT4LS2015), Cambridge, UK, December 7-10, 2015. CEUR Workshop Proceedings, vol. 1546, pp. 157–166. CEUR-WS.org (2015), http://ceur-ws.org/Vol-1546/paper_3.pdf*

#### Luzzu (A Quality Assessment Framework for Linked Open Datasets) 

Allows declarative definitions of quality metrics and produces machine-readable assessment reports based on Dataset Quality Vocabulary

https://eis-bonn.github.io/Luzzu/downloads.html

*[Debattista et al., 2016] Debattista, J., Auer, S., Lange, C.: Luzzu - A methodology and framework for linked data quality assessment. Journal of Data and Information Quality (JDIQ) 8(1), 4:1–4:32 (2016). https://doi.org/10.1145/2992786*

#### RDFUnit 

A framework that assesses linked data quality based on test cases defined in various ways (e.g. RDFS/OWL axioms can be converted into constraints)

https://github.com/AKSW/RDFUnit/
    
*[Kontokostas et al., 2014] Kontokostas, D., Westphal, P., Auer, S., Hellmann, S., Lehmann, J., Cornelissen, R., Zaveri, A.: Test-driven evaluation of linked data quality. In: Proceedings of the 23rd International Conference on World Wide Web (WWW2014), Seoul, Korea, April 07 - 11, 2014. pp. 747–758. ACM (2014). https://doi.org/10.1145/2566486.2568002*



#### SDType  

Uses statistical distributions to predict the types of instances. Incoming and outgoing properties are used as indicators for the types of resources.

https://github.com/HeikoPaulheim/sd-type-validate

*[Paulheim & Bizer, 2013] Paulheim, H., Bizer, C.: Type inference on noisy RDF data. In: Proceedings of the 12th International Semantic Web Conference (ISWC2013), Sydney, Australia, October 21-25, 2013. Lecture Notes in Computer Science, vol. 8218, pp. 510–525. Springer (2013). https://doi.org/10.1007/978-3-642-41335-3_32*


### Knowledge Cleaning

#### HoloClean

An error detection and correction tool based on integrity constraints to identify conflicting and invalid values,  external information to support the constraints, and quantitative statistics to detect outliers.

https://hazyresearch.github.io/snorkel/blog/holoclean.html

*[Rekatsinas et al., 2017] Rekatsinas, T., Chu, X., Ilyas, I.F., R´e, C.: Holoclean: Holistic data repairs with probabilistic inference. Proceedings of the Very Large Data Bases Endowment 10(11), 1190–1201 (2017). https://doi.org/10.14778/3137628.3137631, http://www.vldb.org/pvldb/vol10/p1190-rekatsinas.pdf*

#### KATARA

Learns the relationships between data columns and validate the learn patterns with the help of existing Knowledge Bases and crowd, in order to detect errors in the data. Afterwards it also suggests possible repairs.

*[Chu et al., 2015] Chu, X., Ouzzani, M., Morcos, J., Ilyas, I.F., Papotti, P., Tang, N., Ye, Y.: KATARA: reliable data cleaning with knowledge bases and crowdsourcing. Proceedings of the 41st International Conference on Very Large Data Bases (PVLDB2015), VLDB Endowment, Hawaii, August 31- September 4, 2015 8(12), 1952–1955 (2015). https://doi.org/10.14778/2824032.2824109, http://www.vldb.org/pvldb/vol8/p1952-chu.pdf*

#### SDValidate 

Uses statistical distribution to detect erroneous statements that connect two resources. The statements with less frequent predicate-object pairs are selected as candidates for being wrong.

 https://github.com/HeikoPaulheim/sd-type-validate

*[Paulheim & Bizer,  2014] Paulheim, H., Bizer, C.: Improving the quality of linked data using statistical distributions. International Journal on Semantic Web and Information Systems (IJSWIS) 10(2), 63–86 (2014). https://doi.org/10.4018/ijswis.2014040104*

#### SHACL and ShEx 

Two approaches that aim to verify RDF graphs against a specification (so called shapes). 
For a comparison of two approaches, see Chapter 7 in [Gayo et al., 2017]

https://www.w3.org/TR/shacl/

https://shex.io/shex-semantics/index.html

*[Gayo et al.,  2017] Gayo, J. E. L., Prud'hommeaux, E., Boneva, I.,, Kontokostas, D.  Validating RDF Data. Morgan & Claypool Publishers, (2017)*

#### LOD Laundromat  

Detects and corrects syntactic errors (e.g. bad encoding, broken IRIs), replaces blank nodes with IRIs, removes duplicates in dirty linked open data and re-publishes it in a canonical format.

http://lodlaundromat.org/

*[Beek et al., 2014] Beek, W., Rietveld, L., Bazoobandi, H.R., Wielemaker, J., Schlobach, S.: LOD laundromat: A uniform way of publishing other people’s dirty data. In: Proceedings of the 13th International Semantic Web Conference (ISWC2014), Riva del Garda, Italy, October 19-23, 2014. Lecture Notes in Computer Science, vol. 8796, pp. 213–228. Springer (2014). https://doi.org/10.1007/978-3-319-11964-9_14*



#### TISCO

A framework that tries to identify the time interval where a statement was correct. It uses external knowledge bases and the web content to extract evidence to assess the validity of a statement for a time interval.

*[Rula et al., 2019] Rula, A., Palmonari, M., Rubinacci, S., Ngomo, A.N., Lehmann, J., Maurino, A., Esteves, D.: TISCO: temporal scoping of facts. Journal of Web Semantics 54, 72–86 (2019). https://doi.org/10.1016/j.websem.2018.09.002*

### Knowledge Enrichment

#### Dedupe

A python library that uses machine learning to find duplicates in a dataset and to link two datasets. 

https://github.com/dedupeio/dedupe

#### Duke  

Uses various similarity metrics to detect duplicates in a dataset or link records between two datasets based on a given configuration. 

https://github.com/larsga/Duke

*[Garshol & Borge, 2013] Garshol, L.M., Borge, A.: Hafslund sesam - an archive on semantics. In: Proceedings of the 10th Extending Semantic Web Conference (ESWC2013): Semantics and Big Data, Montpellier, France, May 26-30, 2013. Lecture Notes in Computer Science, vol. 7882, pp. 578–592. Springer (2013). https://doi.org/10.1007/978-3-642-38288-8_39*

#### Legato  

A recording linkage tool that utilizes [Concise Bounded Description](https://www.w3.org/Submission/2004/SUBM-CBD-20040930/#r6) of resources for comparison.

https://github.com/DOREMUS-ANR/legato

*[Achichi et al., 2017] Achichi, M., Bellahsene, Z., Todorov, K.: Legato results for OAEI 2017. In: Proceedings of the 12th International Workshop on Ontology Matching (OM2017) co-located with the 16th International Semantic Web Conference (ISWC2017), Vienna, Austria, October 21, 2017. CEUR Workshop Proceedings, vol. 2032, pp. 146–152. CEUR-WS.org (2017)*

#### LIMES 

A link discovery approach that benefits from the metric spaces (in particular triangle inequality) to reduce the amount of comparisons between source and target dataset.

https://github.com/dice-group/LIMES

*[Ngomo & Auer, 2011] Ngomo, A.N., Auer, S.: LIMES - A time-efficient approach for large-scale link discovery on the web of data. In: Walsh, T. (ed.) Proceedings of the 22nd International Joint Conference on Artificial Intelligence (IJCAI2011), Barcelona, Spain, July 1622, 2011. pp. 2312–2317. AAAI Press (2011). https://doi.org/10.5591/978-1-57735-516-8/IJCAI11-385*


#### SERIMI  

A link discovery tool that utilizes string similarity functions on “label properties” without a prior knowledge of data or schema

https://github.com/samuraraujo/SERIMI-RDF-Interlinking

*[Araújo et al., 2011] Araújo, S., Hidders, J., Schwabe, D., de Vries, A.P.: SERIMI - resource description similarity, RDF instance matching and interlinking. In: Proceedings of the 6th International Workshop on Ontology Matching (OM2011), Bonn, Germany, October 24, 2011. CEUR Workshop Proceedings, vol. 814. CEUR-WS.org (2011), http://ceur-ws.org/Vol-814/om2011_poster6.pdf*

#### SILK  

A link discovery tool with declerative linkage rules applying different similarity metrics (e.g. string, taxonomic, set) that also supports policies for the  notification of datasets when one of them publishes new links to others.

http://silkframework.org/

*[Volz et al., 2009] Volz, J., Bizer, C., Gaedke, M., Kobilarov, G.: Discovering and maintaining links on the web of data. In: Proceedings of the 8th International Semantic Web Conference (ISWC 2009), Chantilly, USA, October 25-29, 2009. Lecture Notes in Computer Science, vol. 5823, pp. 650–665. Springer (2009). https://doi.org/10.1007/978-3-642-04930-9_41*

#### FAGI  

A framework for fusing geospatial data. It suggests fusion strategies based on two datasets with geospatial data and a set of linked entities.

https://github.com/GeoKnow/FAGI-gis

*[Giannopoulos et al., 2014] Giannopoulos, G., Skoutas, D., Maroulis, T., Karagiannakis, N., Athanasiou, S.: FAGI: A framework for fusing geospatial RDF data. In: Proceedings of the Confederated International Conferences ”On the Move to Meaningful Internet Systems” (OTM2014), Amantea, Italy, October 27-31, 2014. Lec- ture Notes in Computer Science, vol. 8841, pp. 553–561. Springer (2014). https://doi.org/10.1007/978-3-662-45563-0_33*


#### KnoFuss   

A framework that allows the application of different methods on different attributes in the same dataset for identification of duplicates and resolves inconsistencies caused by the fusion of linked instances. 

http://technologies.kmi.open.ac.uk/knofuss/

*[Nikolov et al., 2008] Nikolov, A., Uren, V.S., Motta, E., Roeck, A.N.D.: Integration of semantically annotated data by the knofuss architecture. In: Gangemi, A., Euzenat, J. (eds.) Proceedings of the 16th International Conference on Knowledge Engineering and Knowledge Management (EKAW2008): Practice and Patterns, Acitrezza, Italy, September 29 - October 2, 2008. Lecture Notes in Computer Science, vol. 5268, pp. 265–274. Springer (2008). https://doi.org/10.1007/978-3-540-87696-0_24*

#### ODCleanStore 

A framework that contains a fusion module that allows users to configure conflict resolution policies based on different functions (e.g. AVG, MAX, CONCAT) that can be applied on conflicting property values.

*[Knap et al., 2012] Knap, T., Michelfeit, J., Necaský, M.: Linked open data aggregation: Conflict resolution and aggregate quality. In: Proceedings of the 36th Annual IEEE Computer Software and Applications Conference Workshops (COMPSAC2012), Izmir, Turkey, July 16-20, 2012. pp. 106–111. IEEE Computer Society (2012). https://doi.org/10.1109/COMPSACW.2012.29*

#### Sieve 
Sieve has a data fusion module that supports different fusion functions on selected property values. It also utilizes the assessment values from the assessment module in the fusion process. 

*[Mendes et al., 2012] Mendes, P.N., Mühleisen, H., Bizer, C.: Sieve: linked data quality assessment and fusion. In: Proceedings of 2nd International Workshop on Linked Web Data Management (LWDM 2012), in conjunction with the 15th International Conference on Extending Database Technology (EDBT2012): Workshops, Berlin, Germany, March 30, 2012. pp. 116–123. ACM (2012). https://doi.org/10.1145/2320765.2320803*

