
# 시각장애인 횡단보도 보행 보조 앱, SafeLight

![logo](https://github.com/hanmango-o/image-resource/blob/master/SafeLight-README/logo.png?raw=true)

SafeLight는 시각장애인이 음향신호기 버튼을 직접 누르지 않아도, BLE(Bluetooth Low Energy) 기반으로 앱에서 신호기를 원격 제어할 수 있도록 개발된 횡단보도 보행 보조 앱입니다.

## Background

시각장애인이 횡단보도를 건너기 위해서는 신호등에서 발생하는 음향 신호가 필요합니다.

그러나 현재 설치된 `음향신호기(압버튼)`는 점자블록과 멀리 떨어져 있거나, 주변 장애물에 가려 사용이 어렵습니다.

- [인천 시각장애인 음향신호기, 점자블록과 뚝 떨어져 ‘유명무실’](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
- [점자블록과 멀고 가로수에 막혀 음향신호기 ‘있으나 마나’](https://www.kookje.co.kr/news2011/asp/newsbody.asp?code=0300&key=20210420.33003005763)


이에 따라 실제로는 음향신호기의 기능이 제대로 작동하지 않아 보행 안전에 취약한 상황이 반복되고 있습니다.


## Solution

![service_architecture](https://github.com/hanmango-o/image-resource/blob/master/SafeLight-README/service_architecture.png?raw=true)

SafeLight는 BLE 통신을 이용해 음향 신호기를 App으로 제어해 별다른 조작없이 시각장애인이 횡단보도 음향신호를 유도할 수 있도록 돕습니다.

- **음향 신호기 제어**  
  경찰청 스마트 음향신호기 프로토콜을 기반으로 BLE 통신을 통해 음향 신호기를 제어합니다. `위치 유도`를 통해 시각장애인이 횡단보도 위치를 찾고, `음성 안내` 기능을 통해 안전하게 횡단할 수 있도록 합니다.
- **안전 나침반**  
  횡단보도 위치 정보를 기반으로, 사용자의 이동 각도를 실시간으로 분석하여 15도 이상 벗어난 방향으로 보행할 경우, 햅틱 피드백을 제공해 올바른 방향으로 걷도록 안내합니다.
- **안전 경광등**  
  날씨 Open API를 통해 비, 눈, 안개 등 운전자의 가시거리가 확보되지 않은 상황에서스마트폰의 카메라 플래쉬가 주기적으로 깜빡여 운전자에게 보행자의 위치를 알려줍니다.



## Demo

![service_architecture](https://github.com/hanmango-o/image-resource/blob/master/SafeLight-README/demo.gif?raw=true)



## Key Points

### 필드 테스트를 통한 사용성 검증

    실제 시각장애인을 인터뷰하고 UX 기반의 앱 개발을 진행했습니다. 내부 테스트를 위해 실제 음향신호기를 구매하여 안전성 확보에 집중했습니다.

### Accessibility 호환

    국제 접근성 표준(WCAG)에 부합하도록 개발하고, 한국 웹접근성평가센터의 테스트를 통과하여 사용성을 인증받았습니다.


## Tech Stack

<a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=flutter,firebase" />
    <!-- <img src="http://www.w3.org/2000/svg" /> -->
    <img 
  src='data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="%23007AFF" d="M12 0C6.76 0 3.1484 2.4895 3.1484 12S6.76 24 12 24c5.24 0 8.8516-2.4895 8.8516-12S17.24 0 12 0zm-.7773 1.6816l6.2148 6.2149L13.334 12l4.1035 4.1035-6.2148 6.2149V14.125l-3.418 3.42-1.2422-1.2442L10.8515 12l-4.289-4.3008 1.2422-1.2441 3.418 3.4199V1.6816zm1.748 4.2442v3.9687l1.9844-1.9843-1.9844-1.9844zm0 8.1816v3.9668l1.9844-1.9844-1.9844-1.9824Z"/></svg>' 
  alt="Bluetooth Icon" 
  width="48" 
  height="48" 
/>
  </a>

## Link
- [AppStore](https://apps.apple.com/kr/app/%EC%84%B8%EC%9D%B4%ED%94%84%EB%9D%BC%EC%9D%B4%ED%8A%B8/id6444276334)
- [보도자료](https://news.lghellovision.net/news/articleView.html?idxno=408922)
- [Document](DOCS.md)
