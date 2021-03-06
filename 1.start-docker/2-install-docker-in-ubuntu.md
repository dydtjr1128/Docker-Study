# 2. Ubuntu에 도커 설치하기

우분투에서 도커를 설치하기는 굉장히 간단합니다.

```bash
sudo apt update 
sudo apt install apt-transport-https ca-certificates curl software-properties-common 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" 
sudo apt update

sudo apt install docker-ce
```

위의 과정을 마치면 도커의 설치는 끝이 납니다.

다음과 같이 간단하게 도커의 실행 여부를 확인 할 수 있습니다.

```bash
sudo systemctl status docker
```

```bash
cys@ubuntu:~/Desktop/Dev$ sudo systemctl status docker
[sudo] password for cys: 
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enable
   Active: active (running) since Tue 2020-03-03 00:34:50 PST; 16h ago
     Docs: https://docs.docker.com
 Main PID: 5320 (dockerd)
    Tasks: 10
   CGroup: /system.slice/docker.service
           └─5320 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.s

Mar 03 01:17:28 ubuntu dockerd[5320]: time="2020-03-03T01:17:28.214461338-08:00" leve
Mar 03 01:17:28 ubuntu dockerd[5320]: time="2020-03-03T01:17:28.215854608-08:00" leve
Mar 03 01:17:28 ubuntu dockerd[5320]: time="2020-03-03T01:17:28.355492431-08:00" leve
Mar 03 01:17:29 ubuntu dockerd[5320]: time="2020-03-03T01:17:29.605098171-08:00" leve
Mar 03 01:17:31 ubuntu dockerd[5320]: time="2020-03-03T01:17:31.383844186-08:00" leve
Mar 03 01:19:24 ubuntu dockerd[5320]: time="2020-03-03T01:19:24.532025865-08:00" leve
Mar 03 01:19:25 ubuntu dockerd[5320]: time="2020-03-03T01:19:25.254893890-08:00" leve
Mar 03 01:19:25 ubuntu dockerd[5320]: time="2020-03-03T01:19:25.698459172-08:00" leve
Mar 03 01:19:27 ubuntu dockerd[5320]: time="2020-03-03T01:19:27.426022506-08:00" leve
Mar 03 01:19:43 ubuntu dockerd[5320]: time="2020-03-03T01:19:43.840276717-08:00" leve
lines 1-19/19 (END)
```

