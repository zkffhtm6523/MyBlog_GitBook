# Load Balancing

## Load Balancer?

* 일반적으로 서버의 부하를 분산해주는 장치 또는 기술
* 보통 서버 상단 네트워크에 위치
* 서버 한 대에 집중되지 않게 트래픽을 관리하여 각 서버가 최적의 효율을 발휘할 수 있게 해

![](../.gitbook/assets/image%20%2814%29.png)

## Load Balancer 기본 기능

* **Health Check**
  * 기본적으로 해당 포트를 체크해서 열려있는지 확
* **알고리즘에 따른 분산 처리**
  *  Round Robin\(RB\)
    * 프로세스 사이의 우선순위를 두지 않고 순서대로 시간 단위의 CPU를 할당\(선점형 스케줄링\)
* **NAT\(Network Address Translation\)**
  * A라는 IP를 B로 처리해주는 것
* **DSR\(Direct Server Return\)**
  * 일반 : Server -&gt; Load Balancer -&gt; Client
  * DSR : Server -&gt; Client

## Load Balancing Algorithm

### Least Connection 알고리즘\(잘 사용하지 않음\)

* 현재 매핑되어 잇는 커넥션이 가장 적은 서버로 세션을 연결해주는 방
* 만약 2번째 서버에서 하나의 커넥션이 종료되었다면 그 곳으로 할

![Least Connection](../.gitbook/assets/image%20%2812%29.png)

### Round Robin 알고리즘

* 들어오는 트래픽을 서버 순서대로 배치하는 방식
* 연결된 세션이 비교적 오래 사용되지 않는 경우에 채택하는 것이 좋음
* 만약 4번째 서버의 커넥션이 종료되었더라도 1번째 서버에 7번 트래픽 할

![Round Robin](../.gitbook/assets/image%20%2813%29.png)

### Hash 알고리즘

* 특정 기준을 잡아 특정 서버에 매핑하여 고정적으로 트래픽을 분산
* 일반적으로 사용되는 기준은 출발지\(클라이언트\)의 IP가 

![Hash](../.gitbook/assets/image%20%2815%29.png)



