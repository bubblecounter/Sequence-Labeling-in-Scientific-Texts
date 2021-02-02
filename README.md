# Sequence-Labeling-in-Scientific-Texts
Applied different models for the task of sequence labeling in scientific texts.
## Task Description
Scientific texts are also a part of human language and they also need to be processed to get
useful relations. In this project (SamEval 2021 Task 8), we will be dealing with specifically the
counts and measurements in the scientific texts. The main problem is the ambiguity and
inconsistency caused by the way that scientist write their text. These make scientific texts
hard to understand. For example, we can easily find measurements like “10 cm” in a text,
but it is not informative unless you also find the measured entity in the text which can be in
anywhere before or after the measurement. The aim of the project is to extract these entity
relations and make scientific texts easier to understand.

## Trials
Implemented NLP pipelines, to extract quantities, measurements along with their measured entities from scientific texts. (SemEval 2021 Task 8) More detailed info about the task can be found [here](https://github.com/harperco/MeasEval). 

So the given baseline model by the organizer were using Spacy NER model, and they were creating realtionships among them using a knockout logic. Their F1 overlap score was 0.21.

We first tried using CNN-biLSTM-CRF model implemented in [here](https://github.com/guillaumegenthial/tf_ner/tree/master/models/lstm_crf).

Using BERT we incresed it to 0.27
By changing the logic in the relation creation we increase it to 0.31.
Then using a BERT model trained on Scientific Texts( [SCIBERT](https://github.com/allenai/scibert)) we increased the f1 overlap score to 0.34. 
