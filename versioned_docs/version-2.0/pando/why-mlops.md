# Why MLOps?

In machine learning, data is everywhere. For instance, the dataset used for training needs to be tracked. Then you’ve got the data that is produced from that training such as experiment parameters, metrics, logs etc. Even the models are classed as data. Then, when the ‘golden model’ is finally selected and released, model versioning comes into play, producing more data. Add to that your training code and application code, it’s clear — everything is data. That’s why for a machine learning application version control is an extremely difficult problem to solve.

<img data-mode="light" src="static/images/BohSEwEF5w9wqpav_Si1s098i07aT4tlwtFcfco_4cMOlzh_84saxQver2dbqb2MWO_GHOvELLdRPlRgc9ZQZFkaeNheUcLhk_CfBst5jR1HI_4d0kEvJ5vhohgHuchZVG_OeJtDYJ7AxK7DnTCZ0oM.png" alt="img" style={{ marginBottom: 20 }} />


Solving the data versioning problem for machine learning requires the following important considerations:

+ Huge datasets — Git isn’t suitable, you might want to store your data on S3, NFS, or your own MinIO server.
+ Multi-repo in nature — The data produced from datasets, models, experiments, and code, is all valuable, as is version-tracking this data. A single repository can’t track all of this, and tagging is not a viable solution.
+ Lineage tracing — The dependencies at each stage also need to be tracked. When your product’s environment produces an undesirable output, it could be any number of inputs that caused the issue. How do you go about debugging it? Which model version is your deployment, or batch prediction, using? Which dataset, training code, base model, or random seeds were used to create the model? Where did the dataset come from?
+ Automated testing and error debugging — Without versioning, it’s next to impossible to perform automated testing on datasets and models. When your tests produce differing results, you need to be able to find the root cause of the change.
