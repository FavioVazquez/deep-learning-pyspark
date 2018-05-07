# Deep Learning with Pyspark

Hi everyone and welcome back to learning :). In this article I’ll continue the
discussion on Deep Learning with Apache Spark. You can see the preparation part for this repo and code 
[here](https://towardsdatascience.com/deep-learning-with-apache-spark-part-1-6d397c16abd).

Here I will focus entirely on the DL pipelines library and how to use it
from scratch. 

### Apache Spark Timeline

The continuous improvements on Apache Spark lead us to this discussion on how to
do Deep Learning with it. I created a detailed timeline of the development of
Apache Spark until now to see how we got here.

![](https://cdn-images-1.medium.com/max/2000/1*dtLoj7pHnbT_rVmv5Y6yFA.png)

### Deep Learning Pipelines

<br> 

![](https://cdn-images-1.medium.com/max/1600/1*6gBbuSw5qH34uI7GF4p97A.png)
<span class="figcaption_hack">Databricks</span>

Deep Learning Pipelines is an open source library created by Databricks that
provides high-level APIs for scalable deep learning in Python with Apache Spark.

It is an awesome effort and it won’t be long until is merged into the official
API, so is worth taking a look of it.

Some of the advantages of this library compared to the ones that joins Spark
with DL are:

* In the spirit of Spark and [Spark MLlib](https://spark.apache.org/mllib/), it
provides easy-to-use APIs that enable deep learning in very few lines of code.
* It focuses on ease of use and integration, without sacrificing performace.
* It’s build by the creators of Apache Spark (which are also the main
contributors) so it’s more likely for it to be merged as an official API than
others.
* It is written in Python, so it will integrate with all of its famous libraries,
and right now it uses the power of TensorFlow and Keras, the two main libraries
of the moment to do DL.

Deep Learning Pipelines builds on Apache Spark’s [ML
Pipelines](https://spark.apache.org/docs/latest/ml-pipeline.html) for training,
and with Spark DataFrames and SQL for deploying models. It includes high-level
APIs for common aspects of deep learning so they can be done efficiently in a
few lines of code:

* Image loading
* Applying pre-trained models as transformers in a Spark ML pipeline
* Transfer learning
* Applying Deep Learning models at scale
* Distributed hyperparameter tuning **(next part)**
* Deploying models in DataFrames and SQL

I will describe each of these features in detail with examples. These examples
comes from the official
[notebook](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/5669198905533692/3647723071348946/3983381308530741/latest.html)
by Databricks.

### Apache Spark on Deep Cognition

To run and test the codes in this article you will need to create an account in
[Deep Cognition](http://deepcognition.ai/register/). 

Is very easy and then you can access all of their features. When you log in this
is what you should be seeing:

![](https://cdn-images-1.medium.com/max/2000/1*8ijqj85Tjscv9xpXjHfEFA.png)

Now just click on the left part, the Notebook button:

![](https://cdn-images-1.medium.com/max/1600/1*mnMlcYuO2U-KzRvYSuj-Cw.png)

And you will be on the Jupyter Notebook with all the installed packages :). Oh!
A note here: The Spark Notebook (DLS SPARK) is an upcoming feature which will be
released to public sometime next month and tell that it is still in private beta
(just for this post).

![](https://cdn-images-1.medium.com/max/1600/1*cbQSGKgPDBNoBfGdDJqESg.png)

You can see the full code in the Notebook here:

https://github.com/FavioVazquez/deep-learning-pyspark/blob/master/SparkDL.ipynb

Soon I’ll discuss Distributed Hyperparameter Tuning with Spark, and
will try new models and examples :). So stay tuned!
