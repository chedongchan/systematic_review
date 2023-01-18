# This is analysis and model training on data from my systematic review of spontaneous activity of sensory neurons after peripheral nerve injury. 

To view the project analysis, please see systematic_review_analysis.ipynb. 
[Link](https://github.com/chedongchan/systematic_review/blob/main/systematic_review_analysis.ipynb).
  
skills/ modules used - Python (scikit-learn, pytorch, lightning, numpy, pandas, matplotlib, seaborn, xgboost)

## Project Description and Problem Statement

Chronic pain is devastating. Many pain-relieving drugs have been developed but none provide long-lasting analgesia. 
One explanation for the lack of results is that we simply do not know enough about chronic pain development. 

One of the hallmarks of chronic pain is spontaneous activity of sensory neurons after injury. 
I gathered all the available data on Pubmed of spontaneous activity of peripheral sensory neurons after nerve injury.
I explore the general distributions of data and then proceed to find any interesting relationships in the data. 

One problem is that many articles do not/ cannot distinguish the A fibres into its subcategories: A-beta and A-delta. 
This is important because A beta is typically considered to encode non-painful information while the A-delta is considered to encode painful information. Therefore, these two functionally distinct entities are grouped together under the same umbrella term A fibres - thus it could be a source of information loss that if recovered could push further human knowledge of spontaneous activities and chronic pain. In order to achieve this, one could develop a predictive model based on features around the fibres.

Thus, I use my knowledge of basic statistics and machine learning to generate a model that can predict the fibre types of experiments based on the common features reported in publications. 

I find that my model is able to predict upto 62% of the fibre types using simple logistic regressor model/XGBoost with feature selection and hyperparameter tuning. A surprising relationship, which makes a lot of sense given the context of research, was that the year of publication was a great influence of fibre types studied. Additionally, I developed a neural network that can predict 99% of the fibre types, which could be used to predict the fibre types of papers in the past that do not distinguish the fibre types. 

In conlcusion, though models can be generated to salvage the data that are lost, the unavoidable issue is that the seminal papers describing spontaneous activity are few in number and on the whole, there is a clear lack of data for such a complex, and important concept. Therefore, I urge the researchers in the pain field to repeat older, seminal studies (whilst being aligned with the modern reporting standards) and add more to the severely under-represented experiment configurations (species, long-term studies, fibre type focus).

## Authors
* [chedongchan](https://github.com/chedongchan)

## Feedback
If you have any feedback or queries about the product, please message me at dongchan.choi@kcl.ac.uk

## License
This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/chedongchan/systematic_review/blob/main/LICENCE) file for details
