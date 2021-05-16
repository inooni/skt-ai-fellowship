# SKT AI Fellowship



#### STK AI Fellowship 링크

> https://www.sktaifellowship.com/



#### 선정 주제

>  (4번) Smart Factory 서비스를 위한 진동/압력/온도 센서의 Anomaly Detection 개발



#### 데이터 소개

> NASA Bearing Dataset
>
> https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/
> 



#### fft_figure.ipynb

>2nd_test의 Bearing 1에 대하여 기존 데이터와 이를 FFT 변환한 결과를 그래프로 그려주는 코드이다. 아래는 각각 1번째, 500번째, 700번째 데이터에 대한 결과이다.


![figure_1](https://user-images.githubusercontent.com/68908491/118388492-cf3d9500-b65f-11eb-8dff-a0b9d8cc8e3a.png)

<p align="center">Figure_1</p>


![figure_500](https://user-images.githubusercontent.com/68908491/118388502-e8dedc80-b65f-11eb-81c9-90d3ae6bcedf.png)

<p align="center">Figure_500</p>

![figure_700](https://user-images.githubusercontent.com/68908491/118388512-f72cf880-b65f-11eb-80bc-0f0675c55fe1.png)

<p align="center">Figure_700</p>

#### fft_result.ipynb

>2nd_test의 Bearing 1의 모든 데이터를 각각 FFT 변환한 후, 진동수 별로 csv파일을 만들어주는 코드이다. 즉, 특정 진동수에 대해 10분 간격으로 측정되는 진폭 값을 의미하며, 984개의 값을 저장하고 있는 10240개의 csv 파일(0 ~ 10239)이 생성된다. 진동수 0의 경우 FFT 변환시 데이터에서 평균값을 빼지 않아 발생한 편향 값으로, 이 또한 학습에 사용될 예정이다.



#### prob_plot.ipynb

>fft_result.ipynb을 통해 생성한, 특정 진동수에 대한 진폭 값의 분포를 살펴보는 코드이다. 아래는 700이라는 임의의 진동수에 대한 결과이다. 0~700, 701~900, 901~984, 3개의 구간으로 나누어서 분포를 살펴보았다.  

![prob_plot](https://user-images.githubusercontent.com/68908491/118388518-feec9d00-b65f-11eb-961b-7d3a7750bd72.png)
