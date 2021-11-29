# COVID_KG

## data
- ```raw_data.tsv``` : press(보도사), title(기사제목), url, content(기사 본문)으로 구성된 tsv 파일
- ```sentence_split.txt``` : 기사 + 정부 보도자료를 하나로 합치고, 한 줄에 한 문장이 위치하도록 split한 파일
- ```ne_tag_dict.csv``` : NER 자동 태깅을 위한 dict 자료
- ```pre_tagged_sents.txt``` : ```ne_tag_dict.csv``` 딕셔너리를 이용하여 자동 태깅한 결과를 문장별로 나열한 txt 파일
- ```pre_tagged_sents.csv``` : 위 txt 파일과 동일하지만 형식만 csv

## preprocessing
- ```create_corpus.ipynb``` : ```raw_data.tsv```에서 기사 본문만 추출 + 정부 보도자료를 하나로 합쳐서 문장 단위로 split하는 코드 (결과: ```sentence_split.txt```)

## NER
- ```ner_pre_tagging.ipynb``` : ```ne_tag_dict.csv``` 딕셔너리를 이용하여 자동 태깅해주는 코드 (결과: ```pre_tagged_sents.txt```, ```pre_tagged_sents.csv```)
- ```convert_to_ner_train_input.ipynb``` : NER 학습시에 사용하는 ```train.tsv``` 형식으로 바꾸어줄 때 사용하는 코드
