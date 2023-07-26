### 주제
병원폐업률 머신러닝 예측모델 만들기

### 준비
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

OC 영업 폐업을 타겟 컬럼으로 열려있을지 닫혀있을지 예측하기

### 전처리
필요한 패캐지를 불러오고 csv파일로 되어있는 데이터를 불러옵니다

<img width="469" alt="image" src="https://github.com/json9101/Project/assets/57518426/7b6ccfb1-8b1f-4e97-9ca0-f1bed2dc7119">

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

<img width="392" alt="image" src="https://github.com/json9101/Project/assets/57518426/4da1f645-b6dd-4a93-8641-855aa974454b">

정확도가 약 95%정도까지만 나왔습니다

각 컬럼의 중요도를 시각화 해보았습니다

![image](https://github.com/json9101/Project/assets/57518426/0c53cf7f-c67f-487f-8be8-0e879628aab9)

### 보안할점
위의 각 컬럼의 중요도와 같이 모든 컬럼의 상관이 크다고 보는 0.4를 넘는 컬럼이 없습니다
정확도를 높이기 위해서는 여러가지 컬럼들 잘 선택해서 테스트를 해봐야합니다.















