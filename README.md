# harply

### currently under development (check out my google colab notebooks!)

**harply** is a deep learning solution for anonymizing data (using tensorflow 2.x). **harply** gets its name from Harpocrates, who was the god of silence, secrecy and confidentiality. 

Many companies, non-profits, and other organizations need to be able to analyze datasets. However, often in order to utilize the proper tools, those same organizations often need to be able to utilize cloud resources *or* send that dataset to a particular vendor. In some cases, the organization may wish to use **Kaggle** or another similar resource.

Anonymizing the data in theses scenarios is crucial. However, as researchers have identified ways to reassemble or deanonymize data (https://techcrunch.com/2019/07/24/researchers-spotlight-the-lie-of-anonymous-data/), new methods need to be crafted.

The goal of **harply** is to:
  * show first how generative neural networks can be utilized to produce data statistically similar to an original dataset,
  * but also demonstrate that no record can be identified from the original dataset.

The model works by two-three deep learning models built in tensorflow.

  1) A generative model that creates a duplicate of the original dataset. This model is designed to minimize the differences in the *statistical* relationships between the two datasets. I'm currently exploring what loss functions best allow this.
  2) An adversarial model designed to see if it can match records back to the original dataset.
  3) There will be potentially a third model designed to see if it can tell the difference between the two datasets (from a statistical perspective) as well.
