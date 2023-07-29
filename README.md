# <center> 코드를 이용하여 쿨링 팬과 카메라를 조종한 실험대한 코드집 </center>

## 1. 코드를 짜보았다.
우리는 먼저 저희는 잭슨 나노라는 아두이노 같이 부품에 있는 여러가지 장치들을 움직여 보기로 목표를 정하고 프로그램을 작성했다.
그다음으로, 저희는 잭슨 나노가 가동이 될때 그로 인해 생기는 방열을 줄여보려고 했다., 줄이기 위해서는 기기를 냉각시키는 프로펠러가 가동되어야 했다. 그래서 저희는 다음과 같이 코드를 짰다.

      sudo service automagic-fan restart

다음으론, 우리는 프로팰러를 멈추게 하는 코드를 생각했고 다음과 같은 코드를 짰다.

      sudo service automagic-fan stop


## 2. 한가지 궁금증
그런데, 우리는 한가지 궁금증이 생겼다.

      sudo service automagic-fan restart

이 코드와

      sudo service automagic-fan start

이 코드의 차이점이 궁금해졌다.
왜냐면 코드는 달라도 실행한 결과는 동일했기 때문이다.

## 3. 차이점을 찾아보자!
그래서, 우리는 그 차이점이 무엇인지 생각을 해봤고 이런 결과를 내게 되었다.
각각의 프로펠러가 멈춰있을 때

      sudo service automagic-fan restart

이 코드는 명령어를 치자마자 바로 프로펠러가 움직였고

      sudo service automagic-fan start

이 코드는 명령어를 치고나서 조금 기다린 뒤에 프로펠러가 움직였다.

결국 결과적으로 그 둘의 차이점은

      sudo service automagic-fan start

 이 코드는

      sudo service automagic-fan restart

이 코드에 비해 프로펠러가 조금 늦게 돌기 시작한다.

## 4. USB 카메라를 코딩해보자!
그 다음으로 우리는 USB 카메라를 코딩으로 작동하게 만들자고 생각했고 다음의 코드들을 생각해 냈다.

      sensibot@sensibot-jetson:~$ git clone https://github.com/jetsonhacks/USB-Camera.git
      sensibot@sensibot-jetson:~$ ls
      sensibot@sensibot-jetson:~$ cd USB-Camera
      sensibot@sensibot-jetson:~/USB-Camera$ ls
      sensibot@sensibot-jetson:~/USB-Camera$ python3 usb-camera-gst.py

이런 코드들을 구상해 실행에 옮겼다 그리곤 카메라는 정상적으로 작동해 이런 장면이 나왔다
      ![스크린샷, 2023-07-29 17-12-37](https://github.com/asherisaac1/CMA1/assets/140859146/2793f2cc-d7d8-4968-8afd-7dd546dc6cbf)
68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f313833382f312a6f4233533579484868766f75674a6b50587563386f672e676966

이 사진 중에 오른쪽에ㅐ 있는 카메라 사진만 보면 된다.

## 5. 마무리!
그렇게 해서 쿨링 팬을 움직이게 하는 코드와 카메라를 보이게 하는 코드를 완성했다.
처음에는 많이 힘들고 어떻게 해야 하는지 몰라 했지만 막상 해보니 재밌었다.
그리고 우리의 코딩 실력이 한 층 더 느는 느낌이 든다

-김건영, 김민군 -
