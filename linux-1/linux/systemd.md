# Systemd

```bash
# /etc/systemd/system/multi.user.target.wants/biz-client.service 

[Unit] 
Description=Bizppurio Biz-Client SMS and KakaoTalk 

[Service] 
Type=simple 
ExecStart=/home/ubuntu/biz_client_v2011/script/biz_start 
Restart=on-failure 

[Install] 
WantedBy=multi-user.target
```

```bash
# 링크 걸어주기
sudo ln -sf /home/ubuntu/biz_client_v2011/biz-client.service biz-client.service

# systemd 목록 다시 불러오기
sudo systemctl daemon-reload
```



