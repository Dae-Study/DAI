# DAI

## 폴더 설명
1. Labeling : 비속어 라벨링 코드
2. Sentence_separation : 두 단어 비교 및 문장 분석 코드
3. Webpage : 웹페이지 코드 

## 비속어 라벨링
비속어 : 0 , 속어 : 1, 외국어 : 000으로 라벨링 

1차 라벨링 단계 

     1. 1차 형태소 분리 df ['processed_text']

     2. 1차 필터링 후 형태소 분리 df['final_processed_text']

     3. 1차 필터링 후 형태소의 병합하여 텍스트 저장 df ['1st_filtering_text']

     4. 1st_filtering_text에서 60% 이상 한글인 text에서 비속어/속어 분류함


## 두 단어 비교 & 문장 분석 

hangul_components는 초성, 중성, 종성, 자음, 모음 리스트를 모아둠

combine_word는 잘못된 문장 (예: 안ㄴㅕㅇ하ㅏ세요)를 필터링시 비속어 등의 인식이 쉬워지도록 고치는 기능

GET_DB는 몽고디비와 관련된 기능들을 모아둠

두단어_비교는 문장내 의미가 반대되는 반의어끼리 비교하여 부정 또는 긍정을 나눔
