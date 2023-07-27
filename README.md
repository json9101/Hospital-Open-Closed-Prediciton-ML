### 주제
은행에서 대출을 해줄때에 병원의 폐업 가능성 있습니다. 은행의 손해를 줄이기위해 병원의 폐업율을 예측하여 대출을 해줄지 말지를 결정하려고 합니다. 이 프로젝트에서 머신러닝을 사용하여 병원 폐업율을 높은 정확도로 예측해보는것이 목표입니다. 

### 준비
csv파일로 된 데이터로, 데이터는 
- inst_id - 각 파일에서의 병원 고유 번호
- OC – 영업/폐업 분류, 2018년 폐업은 2017년 폐업으로 간주함
- sido – 병원의 광역 지역 정보
- sgg – 병원의 시군구 자료
- openDate – 병원 설립일
- bedCount - 병원이 갖추고 있는 병상의 수
-instkind – 병원, 의원, 요양병원, 한의원, 종합병원 등 병원의 종류

·        종합병원 : 입원환자 100명 이상 수용 가능

·        병원 : 입원 환자 30명 이상 100명 미만 수용 가능

·        의원 : 입원 환자 30명 이하 수용 가능

·        한방 병원(한의원) : 침술과 한약으로 치료하는 의료 기관.  
- revenue1 – 매출액, 2017(회계년도)년 데이터를 의미함
- salescost1 – 매출원가, 2017(회계년도)년 데이터를 의미함
- sga1 - 판매비와 관리비, 2017(회계년도)년 데이터를 의미함
- salary1 – 급여, 2017(회계년도)년 데이터를 의미함
- noi1 – 영업외수익, 2017(회계년도)년 데이터를 의미함
- noe1 – 영업외비용, 2017(회계년도)년 데이터를 의미함
- Interest1 – 이자비용, 2017(회계년도)년 데이터를 의미함
- ctax1 – 법인세비용, 2017(회계년도)년 데이터를 의미함
- Profit1 – 당기순이익, 2017(회계년도)년 데이터를 의미함
- liquidAsset1 – 유동자산, 2017(회계년도)년 데이터를 의미함
- quickAsset1 – 당좌자산, 2017(회계년도)년 데이터를 의미함
- receivableS1 - 미수금(단기), 2017(회계년도)년 데이터를 의미함
- inventoryAsset1 – 재고자산, 2017(회계년도)년 데이터를 의미함
- nonCAsset1 – 비유동자산, 2017(회계년도)년 데이터를 의미함
- tanAsset1 – 유형자산, 2017(회계년도)년 데이터를 의미함
- OnonCAsset1 - 기타 비유동자산, 2017(회계년도)년 데이터를 의미함
- receivableL1 – 장기미수금, 2017(회계년도)년 데이터를 의미함
- debt1 – 부채총계, 2017(회계년도)년 데이터를 의미함
- liquidLiabilities1 – 유동부채, 2017(회계년도)년 데이터를 의미함
- shortLoan1 – 단기차입금, 2017(회계년도)년 데이터를 의미함
- NCLiabilities1 – 비유동부채, 2017(회계년도)년 데이터를 의미함
- longLoan1 – 장기차입금, 2017(회계년도)년 데이터를 의미함
- netAsset1 – 순자산총계, 2017(회계년도)년 데이터를 의미함
- surplus1 – 이익잉여금, 2017(회계년도)년 데이터를 의미함
- revenue2 – 매출액, 2016(회계년도)년 데이터를 의미함
- salescost2 – 매출원가, 2016(회계년도)년 데이터를 의미함
- sga2 - 판매비와 관리비, 2016(회계년도)년 데이터를 의미함
- salary2 – 급여, 2016(회계년도)년 데이터를 의미함
- noi2 – 영업외수익, 2016(회계년도)년 데이터를 의미함
- noe2 – 영업외비용, 2016(회계년도)년 데이터를 의미함
- interest2 – 이자비용, 2016(회계년도)년 데이터를 의미함
- ctax2 – 법인세비용, 2016(회계년도)년 데이터를 의미함
- profit2 – 당기순이익, 2016(회계년도)년 데이터를 의미함
- liquidAsset2 – 유동자산, 2016(회계년도)년 데이터를 의미함
- quickAsset2 – 당좌자산, 2016(회계년도)년 데이터를 의미함
- receivableS2 - 미수금(단기), 2016(회계년도)년 데이터를 의미함
- inventoryAsset2 – 재고자산, 2016(회계년도)년 데이터를 의미함
- nonCAsset2 – 비유동자산, 2016(회계년도)년 데이터를 의미함
- tanAsset2 – 유형자산, 2016(회계년도)년 데이터를 의미함
- OnonCAsset2 - 기타 비유동자산, 2016(회계년도)년 데이터를 의미함
- receivableL2 – 장기미수금, 2016(회계년도)년 데이터를 의미함
- Debt2 – 부채총계, 2016(회계년도)년 데이터를 의미함
- liquidLiabilities2 – 유동부채, 2016(회계년도)년 데이터를 의미함
- shortLoan2 – 단기차입금, 2016(회계년도)년 데이터를 의미함
- NCLiabilities2 – 비유동부채, 2016(회계년도)년 데이터를 의미함
- longLoan2 – 장기차입금, 2016(회계년도)년 데이터를 의미함
- netAsset2 – 순자산총계, 2016(회계년도)년 데이터를 의미함
- surplus2 – 이익잉여금, 2016(회계년도)년 데이터를 의미함
- employee1 – 고용한 총 직원의 수, 2017(회계년도)년 데이터를 의미함
- employee2 – 고용한 총 직원의 수, 2016(회계년도)년 데이터를 의미함
- ownerChange – 대표자의 변동
의 컬럼들을 포함하고 있습니다.

OC 영업 폐업을 타겟 컬럼으로 열려있을지 닫혀있을지 머신러닝으로 예측해보겠습니다.

### 결과
랜덤 포레스트 

<img width="365" alt="image" src="https://github.com/json9101/Project/assets/57518426/793583d1-3f01-46c2-822e-81e5369f0bd8">

XGBoost
하이퍼파라미터 튜닝 전 

<img width="320" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/4a4682be-b8b7-4aa1-92d9-9c64e4eaa5c7">

하이퍼파라미터 튜닝 후

<img width="392" alt="image" src="https://github.com/json9101/Project/assets/57518426/4da1f645-b6dd-4a93-8641-855aa974454b">

gridsearch

<img width="273" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/889662af-f0bf-4c6d-b20d-854b54749408">


랜덤 포레스트, XGBoost와 GridSearch 머신러닝 실행결과 세 모델 모두 약 정확도가 약 95%가 나왔습니다.
특히 XGBoost의 경우 하이퍼파라미터 튜닝도 해보았지만 차이점이 없었습니다.

### 보안할점

- 데이터 자체에 Open이 Closed 보다 훨씬 많아서 평균적으로 정확도가 높은것으로 생각됩니다.
- 정확도를 높이기 위해서는 여러가지 컬럼들 잘 선택해서 테스트를 해봐야합니다.
- 하지만 위의 각 컬럼의 중요도와 같이 모든 컬럼의 상관이 크다고 보는 0.4를 넘는 컬럼이 없기 때문에 컬럼 선택에 어려움이 있습니다.

# 결과의 과정이 궁금하시다면 밑에 전처리 과정과 머신러닝 과정을 봐주시면 감사하겠습니다.

### 전처리
필요한 패캐지를 불러오고 csv파일로 되어있는 데이터를 불러옵니다

<img width="557" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/eb80d296-26b5-47e4-a22c-34b5ebb4bcc1">


중복된 데이터를 먼저 지워줍니다

<img width="688" alt="image" src="https://github.com/json9101/Project/assets/57518426/6676b666-1736-4764-a15a-50b9803ae27f">

전체가 결측된 행은 지워줍니다

<img width="614" alt="image" src="https://github.com/json9101/Project/assets/57518426/1e35856b-7c32-4bb0-a572-af1d95d7295e">

OneHotEncoding으로 타입이 String인 컬럼의 결과를 수치화를 해줍니다

<img width="571" alt="image" src="https://github.com/json9101/Project/assets/57518426/c9387db7-d8ff-4e3e-a909-65708dcb238f">

중간중간에 있는 결측치를 채워줍니다

<img width="676" alt="image" src="https://github.com/json9101/Project/assets/57518426/832325d9-62d6-4e1a-b4f3-a294241c574a">

예시로 위의 사진같이 두 employee컬럼에서 둘중 하나의 값만 없을 경우 값이 있는 다른 employee컬럼의 값을 사용합니다

### 머신러닝
필요한 모델 패캐지를 불러오고 데이터를 정규화를 해줍니다

<img width="338" alt="image" src="https://github.com/json9101/Project/assets/57518426/c33b3e3b-51e3-4513-8281-4a1b06828a64">

랜덤 포레스트 

<img width="365" alt="image" src="https://github.com/json9101/Project/assets/57518426/793583d1-3f01-46c2-822e-81e5369f0bd8">

XGBoost

XGBoost 불러오기

<img width="317" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/2604351d-7b3a-4a49-975b-97a8cfab5ef4">

XGBoost 결과

<img width="320" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/4a4682be-b8b7-4aa1-92d9-9c64e4eaa5c7">

하이퍼파라미터 튜닝 설정후 실해 결과

<img width="548" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/984cebbe-5a56-44dd-9c5d-8c31f5d4ee65">


<img width="575" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/250e78ba-a9b1-487f-9c4f-19d3f44bcd94">

GridSearch 하이퍼파라미터 튜닝 설정후 실

<img width="478" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/a0cefe7d-82a0-4bab-8c18-b1ca361326e0">

<img width="402" alt="image" src="https://github.com/json9101/Hospital-Open-Closed-Prediciton-ML-Project/assets/57518426/24ae8a52-5757-4aec-aebf-c13623494df5">



각 컬럼의 중요도를 시각화 해보았습니다

![image](https://github.com/json9101/Project/assets/57518426/0c53cf7f-c67f-487f-8be8-0e879628aab9)





















