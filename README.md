# SocialDynamicsLab

The current repository collect the jupyter notebook with the pre processing, EDA, model selection and results of a group project on the Social Evolution Dataset by MIT (see information at: http://realitycommons.media.mit.edu/socialevolution.html). 

University exam: June, 2020

***
### Project Analysis 
Knowing the determinants of disease transmission is a central issue in public health [1], [4].
In fact, one central aspects is to reduce the spread of a disease. [5] Therefore, the first concern is to understand how illness can affect people’s behaviour [6]. Understanding the behaviour changes in symptomatic individuals is central in order to control transmission.
These are very challenging tasks. Nowadays, thanks to the diffusion of mobile devices that are able to record proximity, detailed data on social interaction can be gathered. These data can then be used to create model able to predict whether an individual will be sick and his or hers change of behaviour [3] [5].
This is the starting point of our analysis.

### Limitations
● Small sample (the final dataset counts more or less 3000 observations, but on a small portion of the population of the college - only 65 students on the campus ).  
● Biases due to coverage (the study only covers students from a single dorm, but these individuals also have contacts with other people around the campus).  
● Biases due to data (Proximity dataset registers bluetooth proximity and the percentage that the specific record concern people that are sharing the same floor in the building. This means that not all the contacts that we are considering are actually true).  
● Approximation of incubation time - to 24, 48 and 72 hours: this might lead to errors in capturing the disease spread.  
● Threshold in the logistic: we decided to keep the canonic 0.5 threshold, that has overall a poor performance. Anyway, some simulation with other threshold are available in the analysis.  

### Results 
Considering all the aforementioned limitations, the main results of this study concerns the time window to be considered while analysing disease spread. In particular, it is clearly unlikely that the observed individuals manifests flu-like symptoms in the 24 hours subsequent to an encounter.  

Although the overall performance of the different models is not very satisfying, the analysis suggests that - overall - the most appropriate time window seems to be between 48h and 72h - often in literature 48 hours is considered, for flu symptoms [6]. With this specific time span, in fact, the general predictive power throughout the different models reaches its best.  

Overall, the study suggests that the social dimension of each individual is one of the most relevant feature when predicting his or her probability to get sick. However, more than giving a precise ranking of the most relevant feature to predict sick records, the most interesting finding regards, as mentioned, the importance of the time window in which individuals develop symptoms.
***

### REFERENCES:

[1] Craft ME. (2015) Infectious disease transmission and contact networks in wildlife and livestock. Phil. Trans. R. Soc B.
http://dx.doi.org/10.1098/rstb.2014.0107  
[2] Madan A., Cebrian M., Lazer D., Pentland A.,Social sensing for epidemiological behavior change MIT Media Lab and Harvard University,Cambridge MA https://link.springer.com/content/pdf/10.1186/s12879-017-2623-2.pdf  
[3] Gonzalez, Robert M and Maffioli, Elisa M., (2020), Is the Phone Mightier than the Virus? Cell Phone Access and Epidemic Containment Efforts.
https://ssrn.com/abstract=3548926  
[4] Melegaro A., Jit M., Gay N., Zagheni E., Edmunds W.J. (2011), What types of contacts are important for the spread of infections? Using contact survey data to explore European mixing patterns, Epidemics 3, 143-151.
https://doi.org/10.1016/j.epidem.2011.04.001  
[5] Milusheva S., (2020) Using Mobile Phone Data to Reduce Spread of Disease, World Bank Policy Research Working Paper No. 9198.
https://ssrn.com/abstract=3564741  
[6] Poletti P., Visintainer R., Lepri B, Merler S., The interplay between individual social behavior and clinical symptoms in small clustered groups. https://dl.acm.org/doi/pdf/10.1145/1864349.1864394  
