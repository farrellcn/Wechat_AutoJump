# 自动玩微信小游戏跳一跳

### Requirements

- Python
- Opencv
- tensorflow (if using nn_play.py)

#### for Android
- Adb tools
- Android Phone

#### for IOS (Refer to this [site](https://testerhome.com/topics/7220) for installation)
- iPhone
- Mac
- WebDriverAgent
- facebook-wda
- imobiledevice

### Algorithms for Localization
- multiscale-search
- CV based fast-search
- Convolutional Neural Network based coarse-to-fine model

**Notice: CV based fast-search only support Android for now**

### Run

It is recommended to run the following if have an android phone

	python play.py --phone Android --sensitivity 2.045

If you have an iPhone, download the model following the link belowc, and run the following

	python nn_play.py --phone IOS --sensitivity 2.045

- `--phone` has two options: Android or IOS.
- `--sensitivity` is the constant parameter that controls the pressing time.
- `play.py` using algorithm based on CV, support Android and IOS
- `nn_play.py` using algorithm based on Convolutional Neural Network, support Android and IOS, recommend for IOS

### Performance

Our method can correctly detect the positions of the man (green dot) and the destination (red dot).

It is easy to reach the state of art as long as you like.
But I choose to go die after 859 jumps for about 1.5 hours.

<div align="center">
<img align="center" src="resource/state_859.png" width="250" alt="state_859">
<img align="center" src="resource/state_859_res.png" width="250" alt="state_859">
<img align="center" src="resource/sota.png" width="250" alt="sota">
</div>
<br/>

### Demo Video

Here is a video demo. Excited!

[![微信跳一跳](https://img.youtube.com/vi/OeTI2Kx8Ehc/0.jpg)](https://youtu.be/OeTI2Kx8Ehc "自动玩微信小游戏跳一跳")

### Train Log & Data

CNN train log and train&validation data avaliable at
- [Baidu Drive](https://pan.baidu.com/s/1c2rrlra)
- [Google Drive](https://drive.google.com/drive/folders/1tCUf2krzMpkQh_RJL02x0z__4j7MaUI4?usp=sharing)

**Training:** you need to download and untar data directory and accordingly change data dir path in files under `cnn_coarse_to_fine/data_provider` directory.

**Inference:** you need to download and unzip train log dirs into `resource` directory.

### Algorithm Details

For algorithm details, please go to [https://zhuanlan.zhihu.com/p/32636329](https://zhuanlan.zhihu.com/p/32636329).

