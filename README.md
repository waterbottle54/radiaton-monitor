# 원전 방사능 실시간 모니터링  

 ## Introduction

 Nationwide monitoring     |  Focused monitoring
:-------------------------:|:-------------------------:
![](https://github.com/waterbottle54/radiaton-monitor/blob/main/images.png) | ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/gori.png)

 Warning Preferences       |  Virtual Warning Test
 :------------------------:|:-------------------------:
 ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/settings.png) | ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/warning.png)

 
 * **원전 방사능 실시간 모니터링**은 **Java / Android** 로 작성된 **Mobile** 공공 안전 어플리케이션입니다.<br>
 
   이 어플리케이션은 **(주)한수원** 으로부터 방사선량 데이터를 제공받습니다. <br>

   Rest API(XML)로부터 방사선량을 제공받고, Sevice Component를 통해 경고 기능을 구현하였습니다.

 ## Funtionality
> ### Monitoring
> * 전국 원자력발전소의 방사선량 및 안전도를 조회할 수 있다.
> * 특정 원자력발전소에 속하는 관측소들의 방사선량을 조회할 수 있다.
> * 새로고침하여 데이터를 최신 정보로 갱신할 수 있다.

> ### Radioactivity warning
> * 기준치 이상의 방사선량이 관측되면 경고 알림을 발신한다.
> * 기준치를 커스터마이징 할 수 있다.
> * 가상의 발전소를 통해 경고 알람 기능의 작동 여부를 점검할 수 있다.

 ## Project Overview
> ### Language
> Java (1.8)

> ### IDE
> Android Studio (Ape) 
 
> ### REST API
> * (주)한수원의 실시간 방사선량 OPEN API를 HTTPS 통신으로 접근한다.
> * XML format으로 된 데이터를 parsing 하여 어플리케이션 모델로 변환한다.

 ## Author
 * 조성원 (Sung Won Jo)
 
     📧 waterbottle54@naver.com
   
     📚 [Portfolio](https://www.devsungwonjo.pe.kr/)
   
     📹 [Youtube Channel](https://www.youtube.com/@vanilla03034)
   
 ## Version History
 * **1.01** (2021.5): First Release
   ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/onestore.png)

 ## Acknowledgments
 * (주)한국수력원자력 (KHNP Co.,Ltd.)

