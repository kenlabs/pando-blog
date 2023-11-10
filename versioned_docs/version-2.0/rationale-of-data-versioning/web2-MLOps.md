# (Web2)MLOps


Machine Learning (ML) has grown significantly in various industries in recent years. ML practitioners from businesses Artificial Intelligent (AI) teams to individual data scientists face multiple data storage related challenges: finding proven and good dataset, storing and maintaining them with ground truth labels, and keeping track of variances of different ML modeling files that are generated during the experiment and production lifecycle. These data files typically are stored internally, or through AWS / Azure / GCP cloud by many individuals or teams but not organized properly, difficult to version, hard to reference or share. 

In particular, Deep Learning, a type of machine learning, requires data scientists to use much larger datasets to train models that imitates the way humans gain certain types of knowledge. These large datasets (for example, in NLP) can have billions of words or sentences in hundreds of GBs or TBs in size which post challenges in storage and management. Furthermore, these large datasets are stored dozens or thousands of copies around the world - a big waste yet none of them are reliable.

JiaoziFS aims to use Filecoin storage network as data foundation to simplify the AI/ML tasks so that scientists can focus on collect, edit, publish and share Natural Language Processing (NLP) domain open datasets, open algorithms and ML models for AI researchers and various industry applications. 

Machine learning application is a data-driven approach to solving problems. The MLOps is a methodology to have a feedback loop from data, model training, evaluation, model publish, deploy, monitoring. There are three core components in an ML application.

+ Code
+ Datasets
+ Models

The code can be training code, application code. Mostly, it is versioned by git and we have been familiar with the way to version it. And we also use git as the single source of truth to drive the whole DevOps lifecycle.

However, for datasets and models, there is still no de facto solution to version them. Usually, these data are stored in cloud object storage, on-premise object storage like MinIO, or NFS. There is still a gap between data storage and version metadata storage. Here is why we would like to build the JiaoziFS.

In addition, we are thinking about how to drive the automation when an artifact store event is triggered. In git, we can trigger a job whenever a git event. In the artifact store, we lack the fundamentals to trigger this event. JiaoFS references the git design and provides the commits and references primitives to make it possible to define a commit or a version that is created. It makes it possible to listen to the object storage or the file system event to trigger an automation job accordingly.

New RFP Ideas for Wave 3 by DecentralTech · Pull Request #138 · filecoin-project/devgrants https://github.com/filecoin-project/devgrants/pull/138/files