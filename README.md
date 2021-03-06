# Nearthlab Github Naming Rule

Specification for Nearthlab Git Repository Naming.

## 문제 제기


```
영석 : 성민님, 저희 FC랑 통신하는 코드 좀 보고 싶은데요
성민 : 아, 그 코드 저희 지상국 깃헙에 있어요

(10분 후...)

영석 : (으아아, 도대체 어디있는 거야... 멘붕) 성민님, 깃헙에 올라와 있는거 맞아요?
성민 : 여기 QuisqueProject 리파지터리에 있잖아요!
영석 : ...
```

![혼란해](./img/honranhae.jpg)

프로젝트를 생성할 때 저장소 이름에 대한 일관성이 없어, 저장소를 찾거나 정렬하기 어렵습니다. 따라서, 신규 입사자나, 본인이 관여하지 않은 Repository의 코드를 참고하고자 할 때, 다소 혼란을 겪을 수 있습니다.

## 제안

우선, 저장소 네이밍에는 전부 **소문자** 및 **하이픈(-)** 만을 이용합시다.
```bash
tel-me-tel-me-te-te-te-te-tel-me-jyp
```
그리고 일관성을 위해서 `service-role-platform` 의 형태를 제안합니다.

- `service` : 이 저장소가 기여하고 있는 서비스 명 혹은 프로젝트 명
- `role` : 이 저장소가 서비스/프로젝트에서 하는 역할
- `platform` : 이 저장소가 동작하는 플랫폼 혹은 작성된 언어
```bash
fc-core-c
```

더 이상 쓰지 않는 프로젝트의 경우 위의 이름 앞에 legacy 접두어를 붙입니다.
```bash
legacy-gcs-server-dotnet
```

## Service ?

이 곳에는 해당 프로젝트나 서비스를 핵심적으로 설명하는 짧은 단어를 넣어주세요. 프로젝트나 서비스를 가장 잘 설명해줄 수 있는 단어가 무엇일지 고민해보세요. 사람들은 이 단어로 저장소를 검색할 것입니다. 단, 이름이 과도하게 길어지는 것을 방지하기 위해 회사에서 주요하게 사용하는 서비스/프로젝트의 경우 다음 약어를 사용해주세요. ~~아마 거의 다 해당할겁니다~~

| Word |  Acronym |
| --- | --- |
| Flight Controller | fc |
| Ground Control Station | gcs |
| Payload | pl |
| Telemetry/Telecommand | tmtc |
| Hardware | hw |
| System Integration | si |

## Role ?

이 곳에는 저장소가 프로젝트나 서비스에서 기여하는 역할 대해서 적어주세요. 하나의 프로젝트에서 생성된 저장소가 여러 개 일 때, 이 단어만 보고 어떤 기능이 들어 있을 지 예상할 수 있도록 이름을 선택하세요. 굳이 1단어가 아니어도 됩니다

예시 :

| Role | description   |
| --- | --- |
| lib | 라이브러리 |
| server | 서버 |
| client | 클라이언트 |
| core | 핵심 기능 |
| extention | 확장 기능 |
| sdk | Software Development Kit |
| interface | interface |
| cli | command-line user interface |
| gui | graphical user interface |
| util | 도구들 |
| tools | 도구들 |
| samples | 샘플 코드 |
| documents | 문서 |
| ...|그 외 역할을 잘 설명하는 단어|

## Platform ?

이 곳에는 해당 프로젝트나 서비스가 동작하는 플랫폼 혹은 개발의 사용되는 언어를 넣어주세요. 가장 중요하거나 강조되어야 할 플랫폼을 적어줌으로써 읽는 사람이 헷갈리지 않도록 도와줄 수 있습니다.

nodejs, javascript 중에 고민한다면 nodejs를 선택하세요. nodejs 플랫폼을 적어줌으로써 사용되는 언어가 javascript 인지 자연스럽게 추론 할 수 있습니다. 이와 같이 자연스럽게 언어가 추론되는 플랫폼은 플랫폼 명을 적어주세요. 플랫폼이 OS에 제한되는 경우에도 굳이 OS를 적을 필요는 없습니다. 단, 특정 환경에서 동작하는 것을 강조하고 싶다면 적어주세요. 예를 들어 linux-ARM 환경에서만 동작한다면 강조해서 적어주세요. 

예시 :

| Platform | description   |
| --- | --- |
| nodejs | nodejs 어플리케이션 |
| angular | Angular 어플리케이션 |
| dotnet | dotnet 어플리케이션 |
| javascript | javascript 어플리케이션 |
| cpp | c++ 어플리케이션 |
| java | java 어플리케이션 |
| windows | 윈도우에서 동작 |
| linux-arm | linux ARM 버전에서 동작 |
| jetson-tx-1 | tx-1 보드 위에서 동작 |

## 적용

#### 기존

```bash
ngcs
ladgnss
nodejs-server
hippogriff-gcs-client
photo-viewer
inspection-viewer
zed
DW74
```

#### Role 적용

```bash
fc-core-c
gcs-client-angular
pl-manager-dotnet
pl-controller-linux-arm-cpp
```
