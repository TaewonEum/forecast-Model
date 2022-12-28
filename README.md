# 주가 forecast-Model

주가 예측 모델(LSTM)

사용 프레임워크:Jupyter lab

#사용 패키지

![image](https://user-images.githubusercontent.com/104436260/209777192-fea91ce3-5ec3-4818-a932-668fff671a6a.png)

FinanceDataReader=주가 데이터를 가져오는 라이브러리

tensorflow=데이터의 Tensor변환 등 전처리에 사용하기 위해 import

# FinanceDataReader 기능

Samsung전자 주가

![image](https://user-images.githubusercontent.com/104436260/209778000-92a0b0a6-b92d-4930-873b-350966ef557b.png)

LG전자 주가

![image](https://user-images.githubusercontent.com/104436260/209778083-3d51e2fe-b7ea-4d7e-9059-8b755af46cb6.png)

Kia 주가

![image](https://user-images.githubusercontent.com/104436260/209778117-84ccefc7-1068-4537-ba68-c2cb5003c930.png)

종목 코드를 입력하면 해당 회사의 상장일부터 금일 주가까지 Loading가능

# 주요 종목들 Trend 파악해보기

-1. SAMSUNG

![image](https://user-images.githubusercontent.com/104436260/209778563-d04a9434-ca74-4b23-97ba-740901f6778c.png)

전체적으로 주가가 성장하는 추세를 보임.

그래프 상으로 2018년도에 고점을 찍고 하락, 2020년말~2021년초 쯤 전체 상한가를 찍고 하락세를 보임.

