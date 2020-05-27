# 1. 장고의 시작: hello world 화면에 띄우기
장고는 어떻게 작동될까요?
> 장고는 처리하고자 하는 데이터가 있을 때, 파일끼리 넘겨주고 받는 형식으로 진행됩니다. 그래서, 파일이 여러개 존재합니다.
<br/>

## 1)장고를 시작할 때는 프로젝트 형성부터
우리는 먼저 프로젝트를 만들어야 합니다.

▶터미널에 `"django-admin startproject <프로젝트 이름>"` 을 칩니다.

▶그러면 아래 사진과 같은 파일들이 생성됩니다.

<img src="https://blogfiles.pstatic.net/MjAyMDA1MjdfMjIz/MDAxNTkwNTYyNDQxOTM5.fA6UbE1BT54uEMtciDDg54Uc2YWmakBfwzw6bBbTRRYg.XkSzSu0rh01mD6GMoIp_nqbxV2JhNIRQhkZ7iTXaRfkg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2020-05-27_%EC%98%A4%ED%9B%84_3.51.15.png" width="55%"/>

<br/>

## 2)프로젝트의 구성단위, app만들기
app은 프로젝트의 구성단위, 쉽게 말해 앱들이 모인 게 프로젝트입니다.

▶app을 만들려면 터미널에 `"python manage.py startapp <앱이름>"`

▶앱생성시 여러 파일이 생기는데, 생성된 이 파일들과 프로젝트 파일들끼리 티키타카를 한다. 

<img src="https://blogfiles.pstatic.net/MjAyMDA1MjdfMTAw/MDAxNTkwNTYyNDQxOTMx.ylTAKQd8l76FO9-kgVsnliIGmCasz8zE-MGA5P-jy9Eg.HN-1Du0ChJmXnGoQHjDF_9hyVZkaWcVIgfUsn8dgN0wg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2020-05-27_%EC%98%A4%ED%9B%84_3.51.26.png" width="55%"/>

<br/>

## 3)만들어진 파일들끼리 토스 앤 토스는 어떻게?
####
(1)`app`이름으로 된 폴더에 `templates`라는 폴더에 직접 만든다.
앱을 만들었다고 해서 자동으로 실행되는 게 아니라, 
프로젝트 폴더의 `settings.py`에서 설정해야한다.
<img src="https://blogfiles.pstatic.net/MjAyMDA1MjdfMjYg/MDAxNTkwNTYyNDQxOTQx.NPvtOULO_ONTVMpXvCJ8KTvoWyNDRTB_lE9YxYRwVzAg.tHZgv06rajETQ8AEtps_vqH9QNrKSn8lhPpwfvnsi_Yg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2020-05-27_%EC%98%A4%ED%9B%84_3.51.31.png" width="55%"/>

<img src="https://blogfiles.pstatic.net/MjAyMDA1MjdfMzMg/MDAxNTkwNTYyNDQxOTU4.B3Cb5kYOVkwnxs-2pswJqDEc1Seg5KA6nthneqsSOwsg.Zka9iGyd5whkqLErXzxDqNs9VH0fCa3gBmu1afIT4tAg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2020-05-27_%EC%98%A4%ED%9B%84_3.51.43.png" width="55%"/>
<br/>

#### (2)`view.py`에서는 어떤 링크에 들어갔을 때 이 html파일을 보여주는 경로를 만든다.
<img src="https://postfiles.pstatic.net/MjAxOTAxMTdfMTQ4/MDAxNTQ3NzA4MDQ4Mjkw.Rm4Edxn7dTw-fCgRoOZxa0KiknFM2bcNQraGkSPqmHIg.ccPhDyL_QAFkXNfV0nfMCCpVE4bTwi7nyhqUaMUH2CQg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2019-01-15_%EC%98%A4%ED%9B%84_3.00.07.png?type=w580" width="55%"/>
<img src="https://postfiles.pstatic.net/MjAxOTAxMTdfNzQg/MDAxNTQ3NzA4MDgwMDgy.WBVeCggHXbOgxrpmLWY24dihk0oHmLu4aUSD8Mnsk24g.dwRlRSkFTo3e7frrbJW-j9u-dz1_B0XJD8GW1AAJcjQg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2019-01-17_%EC%98%A4%ED%9B%84_3.54.32.png?type=w580" width="55%"/>

<br/>

#### (3)`url.py`에 내가 만든 html이 어떤 url 입력시 뜨게 할지 결정하는 코드를 쓴다.
이때, `myapp>views.py`에 있는 `home함수`를 쓸거니까, `myapp.views`를 `import`한다.<br/>

<img src="https://postfiles.pstatic.net/MjAxOTAxMTdfNjYg/MDAxNTQ3NzA4MTUxMjUy.0Z0yVNJPzIiBa6LMZnnTAyGzCG460pFVd6YmcV7Asscg.ZPugWbUKdwwxgU2ba-PXCqsVkcObhxV5X7xSOIRiXGYg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2019-01-15_%EC%98%A4%ED%9B%84_3.00.47.png?type=w580" width="55%"/>
<img src="https://postfiles.pstatic.net/MjAxOTAxMTdfMjc0/MDAxNTQ3NzA4MjM4OTYx.5F-0nABqK1eEbyoy18B07vVgEY4VKshN3t4lojfY8GIg.ERG35o438o3Oe0G9nBIE3KBCPt1k3ZUFNVRnLEpxCuQg.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2019-01-17_%EC%98%A4%ED%9B%84_3.57.12.png?type=w580" width="55%"/>
<br/>
<br/>

## 4)마무리
마지막으로 터미널에 `python manage.py runserver`를 쳐서 서버를 킨다.

▶터미널에 뜨는 주소에 들어가면 화면을 볼 수 있다.

<hr/>
- 모든 이미지는 제 블로그에 있는 이미지를 참조했습니다.
