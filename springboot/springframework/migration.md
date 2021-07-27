# Migration

1. 아마존 인스턴스 : small, 우분투 ami 20.04
2. 필요한 패키지 파악 필요
   1. tomcat
      1. 경로 : /var/lib/tomcat8
      2. 버전 : tomcat8
      3. 설정 : /etc/tomcat8 -&gt; server.xml 등 자원 경로 여기서 설정
   2. jdk
      1. 버전 : java-11-openjdk-amd64
   3. MariaDB
      1. 버전 : mysql  Ver 15.1 Distrib 10.5.6-MariaDB, for debian-linux-gnu \(x86\_64\) using readline 5.2
      2. 경로 설정 : src/main/resources/config/profile/prod/context-datasource.xml
   4. biz\_client\_v2011
      1. 경로 : /home/dalock/biz\_client\_v2011
   5. Innopay
   6. SlackBot
3. 이전하면서 RDS 분리 필요
4. ELB\[로드밸런스\], Route53
5. cron, script 확인
6. IP 화이트리스트

