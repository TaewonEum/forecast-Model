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

# SAMSUNG 전자 Trend 파악해보기

-1. SAMSUNG

![image](https://user-images.githubusercontent.com/104436260/209778563-d04a9434-ca74-4b23-97ba-740901f6778c.png)

전체적으로 주가가 성장하는 추세를 보임.

그래프 상으로 2018년도에 고점을 찍고 하락, 2020년말~2021년초 쯤 전체 상한가를 찍고 하락세를 보임.

SAMSUNG의 전체 주가를 4Part로 나누어서 시각화

(1998-2002), (2002-2008), (2008-2015), (2015-2022) 4 Part로 나누어 시각화

![image](https://user-images.githubusercontent.com/104436260/209779297-b1375355-ccd4-4cae-b2b9-a0f1f9c8ea7d.png)

2015년에 비해 거의 2021년도 초에는 400%가량 주가가 증가함.

# 주가 데이터 PreProcessing

- 데이터 표준화(최소-최대 정규화)

![image](https://user-images.githubusercontent.com/104436260/209780124-348d8a5b-212c-4153-a425-92ff39a0d3e1.png)

Open~Volume까지의 변수 표준화 시켜줌

min-max scaler 생성

표준화 적용

![image](https://user-images.githubusercontent.com/104436260/209889092-038f6911-4e77-4f35-9b6c-9a45c00c43a6.png)

# Data Split

-Train:Test=8:2 비율로 Data Split

![image](https://user-images.githubusercontent.com/104436260/209889323-efb3d7b2-4dfa-4a4a-86ac-b3557d435b15.png)

# Window data set 생성하기

![image](https://user-images.githubusercontent.com/104436260/209889455-78bf1228-d658-40fa-9602-742c07df9b75.png)

![image](https://user-images.githubusercontent.com/104436260/209890017-e104c484-5fe4-48a6-9967-0fe9d2ef32c2.png)

iteration을 통해 train_data, test_data의 형태를 보면 함수가 잘 적용된 것을 알 수 있다.

32배치사이즈에 20일 동안의 x값으로 이루어진 x 데이터

32개의 y값으로 이루어진 y데이터

