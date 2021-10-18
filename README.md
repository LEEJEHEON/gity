# GITY
Gather Image Through Youtube
---
유튜브에서 원하는 객체를 검출하여 이미지로 저장해주는 코드입니다.  

<img src="./information/image1.png">



## 목차

- [환경](#environment)
- [설치](#installation)
- [실행](#run)
- [작성자](#author)
## Environment
+ OS  
  __ubuntu 20.04__ 에서 테스트를 진행했습니다.
  __Windows 10__ 에서 테스트를 진행했습니다.
+  GPU  
  __RTX3090__ 에서 테스트를 진행했습니다.
+ Tensorflow  
  __tensorflow 2.5__ 에서 작동합니다.



## Installation
0. clone repogitory
```
git clone https://github.com/kyeul611/gity.git
cd ./gity
```
1. 모듈 설치
```
pip install -r requirements.txt
```

2. chromedrive
+ Ubuntu
```
apt-get update
apt install chromium-chromedriver
```
+ Windows
[이곳](https://chromedriver.chromium.org/downloads) 에서 자신의 크롬 버전에 맞는 파일을 다운 받아 gity 파일 안에 넣어 줍니다.

3. youtube-dl
+ Ubuntu
```
wget https://yt-dl.org/downloads/latest/youtube-dl -O youtube-dl
chmod a+rx youtube-dl
```
+ Windows
[이곳](https://github.com/yt-dlp/yt-dlp) 에서 yt-dlp.exe를 받아서 gity 파일 안에 넣어 줍니다.

#### Detector
1. detection-weight

   [이곳](https://drive.google.com/drive/folders/1zB0tJ1U7zNmxUGGbpSF9RhG2szbK1m1r)에서 __yolov3.tf.data-00000-of-00001__ 파일을 다운받아 __gity/yolov3_tf2__ 폴더 안으로 옮겨주세요.



## run

터미널에서 아래 명령어를 실행
```
python main.py --keyword [키워드] --class_name [클래스 종류] 
```

  ___Detection Class___
   Object-detector는 COCO Dataset의 에 대해서 작동합니다.  
   탐지 가능한 클래스 종류는 [이곳](./information/class_list.txt)에서 확인 가능합니다.

example:

```
python main.py --keyword tusker\ elephant --class_name elephant --num_video 5 
```

추가 인자는 아래 명령어를 통해 확인하세요.
```
python main.py --help
```



## references

다음 Open source를 참고하였습니다.

+ [video-preprocessing](https://github.com/AliaksandrSiarohin/video-preprocessing)

+ [object detector](https://github.com/zzh8829/yolov3-tf2)

## 대회 제출 파일

[발표자료.PDF](./information/GITY_발표자료.pdf)


## author

```python
{
	"박 결" : "gyul611@gmail.com",
	"정민혁" : "tlsfk48@gmail.com",
	"이제헌" : "dlwpgjs0723@gmail.com",
}
```
