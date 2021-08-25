---
description: systemd의 서비스 로그를 확인
---

# journalctl

## journalctl이란?

* systemd의 서비스 로그를 확인할 수 있다.
* systemd-journald.service에 의해서 systemd의 정보들을 분석한다.

## 로그 출력 옵션

<table>
  <thead>
    <tr>
      <th style="text-align:center">&#xC635;&#xC158; &#xBA85;&#xB839;</th>
      <th style="text-align:center">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">-a</td>
      <td style="text-align:center">&#xB9E4;&#xC6B0; &#xAE34; &#xACBD;&#xC6B0;&#xC5D0;&#xB3C4; &#xB85C;&#xADF8;
        &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-b</td>
      <td style="text-align:center">&#xB9C8;&#xC9C0;&#xB9C9; &#xBD80;&#xD305; &#xD6C4;&#xC758; log&#xB9CC;
        &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-r</td>
      <td style="text-align:center">&#xB0B4;&#xB9BC;&#xCC28;&#xC21C; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-c</td>
      <td style="text-align:center">&#xCEE4;&#xC11C;&#xAC00; &#xC9C0;&#xC815;&#xD55C; &#xC704;&#xCE58;&#xBD80;&#xD130;
        &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-f</td>
      <td style="text-align:center">&#xCD5C;&#xADFC; &#xB85C;&#xADF8; &#xCD9C;&#xB825; &#xC774;&#xD6C4; &#xACC4;&#xC18D;
        &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-k</td>
      <td style="text-align:center">&#xCEE4;&#xB110; &#xBA54;&#xC138;&#xC9C0;&#xB9CC; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-n</td>
      <td style="text-align:center">&#xCD5C;&#xADFC; 10&#xAC1C;&#xB9CC; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-n 7</td>
      <td style="text-align:center">&#xCD5C;&#xADFC; 7&#xAC1C;&#xB9CC; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">-n _PID</td>
      <td style="text-align:center">&#xD2B9;&#xC815; PID&#xB9CC; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">--since 2020-01-09</td>
      <td style="text-align:center">2020-01-09 &#xC774;&#xD6C4; &#xB85C;&#xADF8;&#xB9CC; &#xCD9C;&#xB825;</td>
    </tr>
    <tr>
      <td style="text-align:center">
        <p>--since 2020-01-09</p>
        <p>--until 2020-01-11</p>
      </td>
      <td style="text-align:center">
        <p>2020-01-09 &#xC774;&#xD6C4;&#xBD80;&#xD130;</p>
        <p>2020-01-11 &#xAE4C;&#xC9C0;&#xC758; &#xB85C;&#xADF8; &#xCD9C;&#xB825;</p>
      </td>
    </tr>
  </tbody>
</table>

## 설정 파일

```bash
# journalctl 설정 파일
vi /etc/systemd/journald.conf

# 설정 파일 내
[Journal]
#Storage=auto
#Compress=yes
#Seal=yes
#SplitMode=uid
#SyncIntervalSec=5m
#RateLimitInterval=30s
#RateLimitBurst=1000
#SystemMaxUse=    -> journal log 파일의 최대 Size를 지정
#SystemKeepFree=
#SystemMaxFileSize=
#RuntimeMaxUse=
#RuntimeKeepFree=
#RuntimeMaxFileSize=
#MaxRetentionSec=
#MaxFileSec=1month  -> journal log 파일의 최대보관일수를 지정
#ForwardToSyslog=yes
#ForwardToKMsg=no
#ForwardToConsole=no
#ForwardToWall=yes
#TTYPath=/dev/console
#MaxLevelStore=debug
#MaxLevelSyslog=debug
#MaxLevelKMsg=notice
#MaxLevelConsole=info
#MaxLevelWall=emerg
```

