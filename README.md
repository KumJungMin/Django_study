# 0. 장고 기본환경 설정하기
<br/>

> 장고를 쓰기 위해선 가상환경을 설정해야한다?

장고는 파이썬으로 웹을 구현하기 필요한 웹 프레임워크(뼈대)이다.
<br/>장고를 쓰기 위해선, visual studio code, git, python을 먼저 설치해야한다.
<br/>
<br/>

## 1) 가상환경을 무엇인가
<br/>
가상환경이 무엇이며, 왜 생겨났을까? 그 이유는 파이썬의 아래특징 때문이다.
<br/>

>"파이썬에서는 한 라이브러리에 한 버전만 설치할 수 있다."

이 말은 A라이브러리에 파이썬2, 3버전을 모두 쓰고 싶어도 할 수 없다는 말이다. 이렇게 되면 여러 프로젝트를 진행할 때, 작업을 바꿀 때마다 다른 버전의 라이브러리를 매번 설치해야 한다. 이런 번거로움을 없애기 위한 장치가 바로 '가상환경'이다.
<a href="https://dojang.io/mod/page/view.php?id=2470"><img src="https://postfiles.pstatic.net/MjAyMDA1MjdfMjQ2/MDAxNTkwNTYwNjg1OTEy.PyKYVohEd7DDnagVOxi5isqz5vPpJYAs58EDGNGP2Qwg.TC3SC8ey2u0VObXMkwtGTC8Y18vD4GvFD0RFfaERh98g.PNG.rmawjdals/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2020-05-27_%EC%98%A4%ED%9B%84_3.24.21.png?type=w580" width="50%"/></a>

*이미지 클릭시 해당 출처로 이동합니다.*

* 결국, 가상환경은 서로 영향을 미치지 않은 독립된 공간을 형성한다.<br/>
* 가상환경을 쓰면, 파이썬 패키지 설치를 하면 전체 영역에 영향을 끼치지 않는다.<br/>
* 각자 독립된 공간에서 여러 프로젝트의 관리가 쉬워진다.<br/>
<br/><br/>
## 2) 장고의 시작
<br/>
가상환경이 뭔지는 알겠는데 그럼 visual studio code에서 장고를 쓰려면 어떻게 해야하나?<br/>

*비주얼 스튜디오 코드, git bash , 파이썬를 설치했다는 가정하에 진행됩니다.*
<br/>

▶비주얼 스튜디오는 구글에 치면 다운로드 가능

▶파이썬도 수동으로 설치가능

▶git bash 설치 https://zetawiki.com/wiki/%EB%A7%A5OS_Git_%EC%84%A4%EC%B9%98

<br/>

#### (1) 바탕화면에 likelion이라는 임의의 폴터를 설치힌다.

#### (2) 비쥬얼스튜디오에서 new project를 눌러 해당 파일을 클릭합니다.

#### (3) new terminal를 눌러 터미널을 킨다.(터미널 위에 선택창은 bash여야 함)
<br/>

> "저는 터미널에 bash가 아닌데, 어떻게 하죠?"
<br/>

``` 
bash설정법
control + 쉬프트 + p를 눌러 
select default shell을 치면
git bash를 클릭하면 끝! 
```
<br/>

#### (4) 가상환경을 생성한다.(가상환경 생성 명령어는 파이썬 버전별로 다름)

```
터미널에 python --version 을 쳐서, 파이썬 버전을 확인해보자.
```

(PLUS) 가상환경의 대표적인 모듈은 3가지가 있습니다.

- venv : Python 3.3 버전 이후 부터 기본모듈에 포함됨

- virtualenv : Python 2 버전부터 사용해오던 가상환경 라이브러리, Python 3에서도 사용가능

- conda : Anaconda Python을 설치했을 시 사용할 수있는 모듈
<br/>

- 파이썬 3 버전이상일  경우, 가상환경 생성법(venv)

``` 
$ python -m venv <가상환경이름>
ex) python -m venv myvenv 
```

<br/>

- 맥

``` 
$ python3 -m venv <가상환경이름> --파이썬 3버전을 쓰고 싶을 때
$ python -m venv <가상환경이름>  --기본적으로 깔린 파이썬 2버전
```

<br/>

- 파이썬 2 버전이하일  경우, 가상환경 생성법(virtualenv)

```
• virtualenv모듈을 사용하려면 pip 명령어로 모듈을 설치해야합니다.
$ pip install virtualenv
----------------
• virtualenv로 가상환경을 생성합니다.
$ virtualenv 가상환경명
```

<br/><br/>

#### (5) 만들어진 가상환경을 구동한다.(사용자의 운영체제별로 명령어 다름)
<br/>

- Mac 또는 리눅스에서 가상환경 구동 방법

```
$ source 가상환경명/bin/activate
```

<br/>

- Windows 가상환경 구동방법

```
$ 가상환경명/Scripts/activate
```

<br/>

- 가상환경을 빠져나오는 명령어

```
$ deactivate
```
<br/>

#### (6) 구동된 가상환경에 장고를 설치한다.

(무조건 가상환경을 키고 장고를 설치합니다)

```
$ pip install django
```

<br/>

- 맥(파이썬 3버전으로 쓰려고 할 때)

```
$ pip3 install django
```

<br/>

이렇게 하면 가상환경 설정과 해당 가상환경에 장고설치가 완료됩니다.
이제 장고를 쓸 수 있음.
<br/>
<br/>
<br/>


___
- 목차

[1] <a href="https://github.com/KumJungMin/Django_study/blob/master/1-%EC%9E%A5%EA%B3%A0%EC%9D%98%20%EC%8B%9C%EC%9E%91:%20hello%20world%20%ED%99%94%EB%A9%B4%EC%97%90%20%EB%9D%84%EC%9A%B0%EA%B8%B0.md">hello world띄우기</a>


___
