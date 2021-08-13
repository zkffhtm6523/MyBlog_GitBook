# 유저 추가하기

## useradd vs adduser

```bash
# david 유저만 추가한다
sudo useradd david

# david 유저 + directory 추가한다
sudo adduser david
```

## 현재 유저 정보 확인

```bash
# 현재 유저정보 확인
sudo vi /etc/passwd
```

![](../../.gitbook/assets/image%20%283%29.png)

* x : 비밀번호 유무 표시
* 첫 번째 1000 : 사용자가 부여받은 고유 ID
* 두 번째 1000 : 소속된 그룹 ID
* 두 번째 centos : 전체 사용자 이름 -&gt; 설정 없을 시 기본 사용자 이름
* :/home/centos : 사용자의 기본 디렉토리
* :/bin/bash : 사용자가 기본으로 사용할  쉘

## 현재 그룹 정보 확인

```bash
# 현재 그룹 정보 확인 
sudo vi /etc/group
```

![](../../.gitbook/assets/image%20%284%29.png)

* **현재 그룹 이름 : 비밀번호 유무 : 현재 그룹 ID : 현재 그룹에 속한 사용자 이름**

