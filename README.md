# Health-related Document level Embeddings


## Training Embeddings 
Embeddings presented in the research are pre-trained:
- using [fastText](https://fasttext.cc/) 
- at document level
- for both [CBOW](http://dblp.org/rec/bib/journals/corr/abs-1301-3781) (T300 and T600) and [Skip-gram](http://dblp.org/rec/bib/journals/corr/abs-1301-3781) (T300SG, T600SG) models
- Parameter choices for training: character n-grams of length 5, a window of size 5, ten negative samples per positive sample, and learning rate of 0.05 is used.
- Dimensions: 300 and 600 

## Data  

The TREC precision medicine/clinical decision support track 2017 [TREC2017](https://trec.nist.gov/pubs/trec26/papers/Overview-PM.pdf) data (24G of health-related data) is used for pre-training embeddings. This includes 26.8 million published abstracts of medical literature listed on PubMed Central, 241,006 clinical trials documents, and 70,025 abstracts from recent proceedings focused on cancer therapy from AACR (American Association for Cancer Research) and ASCO (American Society of Clinical Oncology).

The clinical notes from [MIMIC-III Clinical Database](https://physionet.org/works/MIMICIIIClinicalDatabase/access.shtml) used for experiments. See publications for details of the results. 


| Model | Dimensions | Training Time* | Model Size  |
| :------ | --------: | --------: | -----: |
| T300 | 300  |7 hours | 13G |
| T300SG | 300 | 28 hours | 13G |
| T600 | 600 | 13 hours | 23G |
| T600SG | 600 | 51 hours | 23G |

* Processing was run on a 4 core Intel i7-6700K CPU @ 4.00GHz with 64GB of RAM.



[T300SG embeddings](https://www.dropbox.com/s/ctk8uxjfqo09fkl/T300SG.zip?dl=0)
