# 원전 방사능 실시간 모니터링  

 ## Introduction

 Nationwide monitoring         |  Focused monitoring
:-------------------------:|:-------------------------:
![](https://github.com/waterbottle54/radiaton-monitor/blob/main/images.png) | ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/gori.png)
 
 * **원전 방사능 실시간 모니터링**은 **Java / Android** 로 작성된 **Mobile** 공공 안전 어플리케이션입니다.<br>

   이 어플리케이션은 **(주)한수원** 으로부터 방사선량 데이터를 제공받습니다. <br>

   The radioactivity data used in this application is provided from KHNP Co.,Ltd.

 ## Funtionality
> ### Monitoring
> * MRI 및 CT 영상이 담긴 DICOM 파일을 열람할 수 있다.
> * 특정 시리즈의 특정 단면 이미지를 탐색할 수 있다.
> * 단면의 특정 영역을 확대하거나 축소하여 볼 수 있다.

> ### Radioactivity warning
> * 각 단면에서 종양에 해당하는 영역을 마크할 수 있다.
> * 적층된 종양 단면으로부터 종양의 입체 모델을 생성할 수 있다.
> * 종양 모델을 렌더링하고 회전 등 변환을 가할 수 있다.
> * 종양 모델을 파일(*.tmr)로 내보낼 수 있다.

> ### Etc.
> * 프로젝트를 파일(.bts)로 저장하고 불러와서 모델을 수정할 수 있다.
> * Tip, About 메뉴로부터 프로그램 사용 방법, 프로그램 정보를 확인할 수 있다.

 ## Project Overview
> ### Language
> Java (1.8)

> ### IDE
> Android Studio (Ape) 
 
> ### GUI
> * 단일한 윈도우(MainWindow.py)가 존재한다.
> * 윈도우는 2개의 하위 Fragment 모듈들로 구성되며, 대부분의 동작은 각 Fragment가 처리한다.
> * LayersFragment 는 시리즈 및 단면 탐색, 종양 경계 입력을 수행한다.
> * RenderingFragment 는 3D 렌더링, 모델 변환(rotate, scale)을 수행한다.
 
> ### Architecture
> * MVVM Pattern
> * 단일한 뷰모델(ViewModel.py)이 존재한다.
> * Layer 간 결합도를 낮추기 위해 Observer 패턴을 사용하였다.
> * Observer 패턴의 구현을 위해 data와 callback을 갖는 LiveData 모듈을 작성하였다.
 
> ### 3D Graphics
> * 렌더링과 기하 연산에 각각 PyOpenGL(3.1.7), Open3d(0.18.0)를 사용하였다.
> * 사용자가 각 단면마다 입력한 종양 경계점을 적층하여 3D point cloud 를 구성하였다.
> * point cloud 로부터 mesh 를 얻는 계산에는 Poission reconstruction 이 적용되었다.

 ## Author
 * 조성원 (Sung Won Jo)
 
     📧 waterbottle54@naver.com
   
     📚 [Portfolio](https://www.devsungwonjo.pe.kr/)
   
     📹 [YouTube Channel](https://github.com/waterbottle54)
   
 ## Version History
 * **1.01** (2021.5): First Release
   ![](https://github.com/waterbottle54/radiaton-monitor/blob/main/onestore.png)

 ## Acknowledgments
 * (주)한국수력원자력 (KHNP Co.,Ltd.)

