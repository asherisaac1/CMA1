먼저 저희는 잭슨 나노라는 아두이노 같이 부품에 있는 여러가지 장치들을 움직여 보기로 목표를 정하고 프로그램을 작성했습니다.
그다음으로, 저희는 잭슨 나노가 가동이 될때 그로 인해 생기는 방열을 줄여보려고 했는데요, 줄이기 위해서는 기기를 냉각시키는 프로펠러가 가동되어야 했습니다. 그래서 저희는 다음과 같이 코드를 짰습니다.sensibot@sensibot-jetson:~$ sudo service automagic-fan restart
이 프로그램을 실행시키면 프로펠러가 돌아가게 됩니다
그리고 이 프로펠러를 고치기 위해서는 어떻게 해야할까 생각하다 다음과 같이 짜게 되었습니다. 
sensibot@sensibot-jetson:~$ sudo service automagic-fan. stop
이 프로그램을 실행시키면 프로펠러가 멈추게 됩니다.
하지만, 저희는 여기서 의문점이 생겼는데요 바로,
sensibot@sensibot-jetson:~$ sudo service automagic-fan start
sensibot@sensibot-jetson:~$ sudo service automagic-fan restart
이 두 코드의 차이점이었습니다. 왜냐하면 두 코드를 실행하면 잭슨나노는 똑같이 프로펠러가 돌아가는 데요.
이 둘의 차이점은 둘다 프로펠러가 멈춰있을 떄
