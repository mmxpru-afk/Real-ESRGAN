<p align="center">
  <img src="assets/realesrgan_logo.png" height=120>
</p>

## <div align="center"><b><a href="README.md">English</a> | <a href="README_CN.md">简体中文</a> | <a href="README_KO.md">한글</a></b></div>

<div align="center">

👀[**데모**](#-데모-영상) **|** 🚩[**업데이트**](#-업데이트) **|** ⚡[**사용법**](#-빠른-추론) **|** 🏰[**모델 동물원**](docs/model_zoo.md) **|** 🔧[설치](#-의존성-및-설치)  **|** 💻[학습](docs/Training.md) **|** ❓[FAQ](docs/FAQ.md) **|** 🎨[기여](docs/CONTRIBUTING.md)

[![download](https://img.shields.io/github/downloads/xinntao/Real-ESRGAN/total.svg)](https://github.com/xinntao/Real-ESRGAN/releases)
[![PyPI](https://img.shields.io/pypi/v/realesrgan)](https://pypi.org/project/realesrgan/)
[![Open issue](https://img.shields.io/github/issues/xinntao/Real-ESRGAN)](https://github.com/xinntao/Real-ESRGAN/issues)
[![Closed issue](https://img.shields.io/github/issues-closed/xinntao/Real-ESRGAN)](https://github.com/xinntao/Real-ESRGAN/issues)
[![LICENSE](https://img.shields.io/github/license/xinntao/Real-ESRGAN.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE)
[![python lint](https://github.com/xinntao/Real-ESRGAN/actions/workflows/pylint.yml/badge.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/.github/workflows/pylint.yml)
[![Publish-pip](https://github.com/xinntao/Real-ESRGAN/actions/workflows/publish-pip.yml/badge.svg)](https://github.com/xinntao/Real-ESRGAN/blob/master/.github/workflows/publish-pip.yml)

</div>

🔥 **AnimeVideo-v3 모델 (애니메이션 비디오 소형 모델)**. [[*애니메이션 비디오 모델*](docs/anime_video_model.md)] 및 [[*비교*](docs/anime_comparisons.md)]를 참조하세요<br>
🔥 **RealESRGAN_x4plus_anime_6B** (애니메이션 이미지용 최적화). [[*애니메이션_모델*](docs/anime_model.md)]을 참조하세요

<!-- 1. 우리 웹사이트에서 시도할 수 있습니다: [ARC Demo](https://arc.tencent.com/en/ai-demos/imgRestore) (현재 RealESRGAN_x4plus_anime_6B만 지원) -->
1. :boom: **업데이트** 온라인 Replicate 데모: [![Replicate](https://img.shields.io/static/v1?label=Demo&message=Replicate&color=blue)](https://replicate.com/xinntao/realesrgan)
1. Real-ESRGAN을 위한 온라인 Colab 데모: [![Colab](https://img.shields.io/static/v1?label=Demo&message=Colab&color=orange)](https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing) **|** Real-ESRGAN (**애니메이션 비디오**)을 위한 온라인 Colab 데모: [![Colab](https://img.shields.io/static/v1?label=Demo&message=Colab&color=orange)](https://colab.research.google.com/drive/1yNl9ORUxxlL4N0keJa2SEPB61imPQd1B?usp=sharing)
1. 휴대용 [Windows](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-windows.zip) / [Linux](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-ubuntu.zip) / [MacOS](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-macos.zip) **실행 파일(Intel/AMD/Nvidia GPU용)**. 자세한 정보는 [여기](#휴대용-실행-파일-ncnn)를 참조하세요. ncnn 구현은 [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan)에 있습니다
<!-- 1. [텐센트 비디오](https://v.qq.com/s/topic/v_child/render/fC4iyCAM.html)에서 개선된 애니메이션을 볼 수 있습니다. -->

Real-ESRGAN은 **실용적인 이미지/비디오 복원 알고리즘**을 개발하는 것을 목표로 합니다.<br>
우리는 강력한 ESRGAN을 실용적인 복원 애플리케이션(즉, Real-ESRGAN)으로 확장했으며, 이는 순수 합성 데이터로 학습되었습니다.

🌌 귀중한 피드백/제안에 감사드립니다. 모든 피드백은 [feedback.md](docs/feedback.md)에 업데이트됩니다.

---

Real-ESRGAN이 도움이 되었다면 이 저장소에 ⭐를 눌러주시거나 친구에게 추천해 주세요 😊 <br>
다른 추천 프로젝트:<br>
▶️ [GFPGAN](https://github.com/TencentARC/GFPGAN): 실제 얼굴 복원을 위한 실용적인 알고리즘 <br>
▶️ [BasicSR](https://github.com/xinntao/BasicSR): 오픈 소스 이미지 및 비디오 복원 도구 모음<br>
▶️ [facexlib](https://github.com/xinntao/facexlib): 유용한 얼굴 관련 함수를 제공하는 컬렉션<br>
▶️ [HandyView](https://github.com/xinntao/HandyView): 보기 및 비교를 위한 PyQt5 기반 이미지 뷰어 <br>
▶️ [HandyFigure](https://github.com/xinntao/HandyFigure): 논문 도자의 오픈 소스 <br>

---

### 📖 Real-ESRGAN: 순수 합성 데이터로 실제 블라인드 초해상도 학습

> [[논문](https://arxiv.org/abs/2107.10833)] &emsp; [[유튜브 영상](https://www.youtube.com/watch?v=fxHWoDSSvSc)] &emsp; [[B站讲解](https://www.bilibili.com/video/BV1H34y1m7sS/)] &emsp; [[포스터](https://xinntao.github.io/projects/RealESRGAN_src/RealESRGAN_poster.pdf)] &emsp; [[PPT 슬라이드](https://docs.google.com/presentation/d/1QtW6Iy8rm8rGLsJ0Ldti6kP-7Qyzy6XL/edit?usp=sharing&ouid=109799856763657548160&rtpof=true&sd=true)]<br>
> [Xintao Wang](https://xinntao.github.io/), Liangbin Xie, [Chao Dong](https://scholar.google.com.hk/citations?user=OSDCB0UAAAAJ), [Ying Shan](https://scholar.google.com/citations?user=4oXBp9UAAAAJ&hl=en) <br>
> [Tencent ARC Lab](https://arc.tencent.com/en/ai-demos/imgRestore); 선전 고등기술 연구원, 중국 과학원

<p align="center">
  <img src="assets/teaser.jpg">
</p>

---

<!---------------------------------- 업데이트 --------------------------->
## 🚩 업데이트

- ✅ **realesr-general-x4v3** 모델 추가 - 일반 장면을 위한 소형 모델입니다. **-dn** 옵션을 지원하여 노이즈를 조절할 수 있습니다(과도한 평활화 결과 방지). **-dn**은 노이즈 제거 강도의 약자입니다.
- ✅ **RealESRGAN AnimeVideo-v3** 모델 업데이트. 자세한 내용은 [애니메이션 비디오 모델](docs/anime_video_model.md) 및 [비교](docs/anime_comparisons.md)를 참조하세요.
- ✅ 애니메이션 비디오용 소형 모델 추가. 자세한 내용은 [애니메이션 비디오 모델](docs/anime_video_model.md)을 참조하세요.
- ✅ ncnn 구현 [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan) 추가.
- ✅ [*RealESRGAN_x4plus_anime_6B.pth*](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth) 추가, **애니메이션** 이미지에 최적화되어 있으며 훨씬 작은 모델 크기입니다. 더 많은 세부 사항과 [waifu2x](https://github.com/nihui/waifu2x-ncnn-vulkan)와의 비교는 [**anime_model.md**](docs/anime_model.md)를 참조하세요
- ✅ 자신의 데이터 또는 쌍을 이루는 데이터에 대한 미세 조정 지원(즉, ESRGAN 미세 조정). [여기](docs/Training.md#Finetune-Real-ESRGAN-on-your-own-dataset)를 참조하세요
- ✅ [GFPGAN](https://github.com/TencentARC/GFPGAN) 통합하여 **얼굴 개선** 지원.
- ✅ [Gradio](https://github.com/gradio-app/gradio)를 사용하여 [Huggingface Spaces](https://huggingface.co/spaces)에 통합됨. [Gradio 웹 데모](https://huggingface.co/spaces/akhaliq/Real-ESRGAN)를 참조하세요. [@AK391](https://github.com/AK391)에 감사드립니다
- ✅ `--outscale`을 사용한 임의의 스케일 지원(실제로 `LANCZOS4`를 사용하여 출력을 추가로 크기 조정). *RealESRGAN_x2plus.pth* 모델 추가.
- ✅ [추론 코드](inference_realesrgan.py)는 다음을 지원합니다: 1) **타일** 옵션; 2) **알파 채널**이 있는 이미지; 3) **회색** 이미지; 4) **16비트** 이미지.
- ✅ 학습 코드가 공개되었습니다. 자세한 가이드는 [Training.md](docs/Training.md)에서 찾을 수 있습니다.

---

<!---------------------------------- 데모 영상 --------------------------->
## 👀 데모 영상

#### Bilibili

- [대요천궁 장면](https://www.bilibili.com/video/BV1ja41117zb)
- [애니메이션 댄스 컷](https://www.bilibili.com/video/BV1wY4y1L7hT/)
- [원피스 장면](https://www.bilibili.com/video/BV1i3411L7Gy/)

#### YouTube

## 🔧 의존성 및 설치

- Python >= 3.7 ([Anaconda](https://www.anaconda.com/download/#linux) 또는 [Miniconda](https://docs.conda.io/en/latest/miniconda.html) 사용 권장)
- [PyTorch >= 1.7](https://pytorch.org/)

### 설치

1. 저장소 복제

    ```bash
    git clone https://github.com/xinntao/Real-ESRGAN.git
    cd Real-ESRGAN
    ```

1. 의존 패키지 설치

    ```bash
    # basic SR 설치 - https://github.com/xinntao/BasicSR
    # 학습 및 추론 모두에 BasicSR을 사용합니다
    pip install basicsr
    # facexlib 및 gfpgan은 얼굴 개선을 위한 것입니다
    pip install facexlib
    pip install gfpgan
    pip install -r requirements.txt
    python setup.py develop
    ```

---

## ⚡ 빠른 추론

Real-ESRGAN을 추론하는 방법은 일반적으로 세 가지가 있습니다.

1. [온라인 추론](#온라인-추론)
1. [휴대용 실행 파일 (NCNN)](#휴대용-실행-파일-ncnn)
1. [Python 스크립트](#python-스크립트)

### 온라인 추론

1. 우리 웹사이트에서 시도할 수 있습니다: [ARC Demo](https://arc.tencent.com/en/ai-demos/imgRestore) (현재 RealESRGAN_x4plus_anime_6B만 지원)
2. Real-ESRGAN용 [Colab 데모](https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing) **|** Real-ESRGAN (**애니메이션 비디오**)용 [Colab 데모](https://colab.research.google.com/drive/1yNl9ORUxxlL4N0keJa2SEPB61imPQd1B?usp=sharing).

### 휴대용 실행 파일 (NCNN)

[Windows](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-windows.zip) / [Linux](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-ubuntu.zip) / [MacOS](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesrgan-ncnn-vulkan-20220424-macos.zip) **실행 파일(Intel/AMD/Nvidia GPU용)**을 다운로드할 수 있습니다.

이 실행 파일은 **휴대용**이며 필요한 모든 바이너리 및 모델을 포함합니다. CUDA 또는 PyTorch 환경이 필요하지 않습니다.<br>

다음 명령을 실행하면 됩니다(Windows 예제, 각 실행 파일의 README.md에서 자세한 정보 참조):

```bash
./realesrgan-ncnn-vulkan.exe -i input.jpg -o output.png -n model_name
```

다섯 가지 모델을 제공했습니다:

1. realesrgan-x4plus  (기본)
2. realesrnet-x4plus
3. realesrgan-x4plus-anime (애니메이션 이미지에 최적화, 소형 모델 크기)
4. realesr-animevideov3 (애니메이션 비디오)

`-n` 인수를 사용하여 다른 모델을 사용할 수 있습니다. 예를 들어, `./realesrgan-ncnn-vulkan.exe -i input.jpg -o output.png -n realesrnet-x4plus`

#### 휴대용 실행 파일 사용법

1. 자세한 내용은 [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan#computer-usages)을 참조하세요.
2. `outscale`과 같은 일부 기능(파이썬 스크립트 `inference_realesrgan.py`에서 지원)을 지원하지 않는다는 점에 유의하세요.

```console
사용법: realesrgan-ncnn-vulkan.exe -i infile -o outfile [옵션]...

  -h                   이 도움말 표시
  -i input-path        입력 이미지 경로 (jpg/png/webp) 또는 디렉토리
  -o output-path       출력 이미지 경로 (jpg/png/webp) 또는 디렉토리
  -s scale             업스케일 비율 (2, 3, 4 가능, 기본값=4)
  -t tile-size         타일 크기 (>=32/0=자동, 기본값=0) 0,0,0은 다중 GPU
  -m model-path        사전 학습 모델 폴더 경로. 기본값=models
  -n model-name        모델 이름 (기본값=realesr-animevideov3, 가능한 값: realesr-animevideov3 | realesrgan-x4plus | realesrgan-x4plus-anime | realesrnet-x4plus)
  -g gpu-id            사용할 GPU 장치 (기본값=자동) 0,1,2는 다중 GPU
  -j load:proc:save    로드/처리/저장을 위한 스레드 수 (기본값=1:2:2) 1:2,2,2:2는 다중 GPU
  -x                   tta 모드 활성화
  -f format            출력 이미지 형식 (jpg/png/webp, 기본값=ext/png)
  -v                   상세 출력
```

이 실행 파일은 입력 이미지를 여러 타일로 먼저 자르고 각각 따로 처리한 다음 마지막으로 함께 연결하기 때문에 블록 불일치를 유발할 수 있습니다(또한 PyTorch 구현과 약간 다른 결과를 생성기도 합니다).

### Python 스크립트

#### Python 스크립트 사용법

1. `outscale` 인수로 **임의의 출력 크기**에 대해 X4 모델을 사용할 수 있습니다. 프로그램은 Real-ESRGAN 출력 후에 저비용 크기 조정 작업을 추가로 수행합니다.

```console
사용법: python inference_realesrgan.py -n RealESRGAN_x4plus -i infile -o outfile [옵션]...

일반적인 명령: python inference_realesrgan.py -n RealESRGAN_x4plus -i infile --outscale 3.5 --face_enhance

  -h                   이 도움말 표시
  -i --input           입력 이미지 또는 폴더. 기본값: inputs
  -o --output          출력 폴더. 기본값: results
  -n --model_name      모델 이름. 기본값: RealESRGAN_x4plus
  -s, --outscale       이미지의 최종 업샘플링 배율. 기본값: 4
  --suffix             복원된 이미지의 접미사. 기본값: out
  -t, --tile           타일 크기, 테스트 중 타일 없음은 0. 기본값: 0
  --face_enhance       GFPGAN을 사용하여 얼굴을 개선할지 여부. 기본값: False
  --fp32               추론 중 fp32 정밀도 사용. 기본값: fp16 (반정밀도).
  --ext                이미지 확장명. 옵션: auto | jpg | png, auto는 입력과 동일한 확장명을 사용합니다. 기본값: auto
```

#### 일반 이미지 추론

사전 학습 모델 다운로드: [RealESRGAN_x4plus.pth](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth)

```bash
wget https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth -P weights
```

추론!

```bash
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs --face_enhance
```

결과는 `results` 폴더에 있습니다

#### 애니메이션 이미지 추론

<p align="center">
  <img src="https://raw.githubusercontent.com/xinntao/public-figures/master/Real-ESRGAN/cmp_realesrgan_anime_1.png">
</p>

사전 학습 모델: [RealESRGAN_x4plus_anime_6B](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth)<br>
 더 많은 세부 사항과 [waifu2x](https://github.com/nihui/waifu2x-ncnn-vulkan)와의 비교는 [**anime_model.md**](docs/anime_model.md)에서 찾을 수 있습니다

```bash
# 모델 다운로드
wget https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth -P weights
# 추론
python inference_realesrgan.py -n RealESRGAN_x4plus_anime_6B -i inputs
```

결과는 `results` 폴더에 있습니다

---

## BibTeX

    @InProceedings{wang2021realesrgan,
        author    = {Xintao Wang and Liangbin Xie and Chao Dong and Ying Shan},
        title     = {Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data},
        booktitle = {International Conference on Computer Vision Workshops (ICCVW)},
        date      = {2021}
    }

## 📧 연락처

질문이 있으시면 `xintao.wang@outlook.com` 또는 `xintaowang@tencent.com`으로 이메일을 보내주세요.

<!---------------------------------- Real-ESRGAN을 사용하는 프로젝트 --------------------------->
## 🧩 Real-ESRGAN을 사용하는 프로젝트

Real-ESRGAN을 개발/사용하는 프로젝트가 있으면 알려주세요.

- NCNN-Android: [RealSR-NCNN-Android](https://github.com/tumuyan/RealSR-NCNN-Android) by [tumuyan](https://github.com/tumuyan)
- VapourSynth: [vs-realesrgan](https://github.com/HolyWu/vs-realesrgan) by [HolyWu](https://github.com/HolyWu)
- NCNN: [Real-ESRGAN-ncnn-vulkan](https://github.com/xinntao/Real-ESRGAN-ncnn-vulkan)

&nbsp;&nbsp;&nbsp;&nbsp;**GUI**

- [Waifu2x-Extension-GUI](https://github.com/AaronFeng753/Waifu2x-Extension-GUI) by [AaronFeng753](https://github.com/AaronFeng753)
- [Squirrel-RIFE](https://github.com/Justin62628/Squirrel-RIFE) by [Justin62628](https://github.com/Justin62628)
- [Real-GUI](https://github.com/scifx/Real-GUI) by [scifx](https://github.com/scifx)
- [Real-ESRGAN_GUI](https://github.com/net2cn/Real-ESRGAN_GUI) by [net2cn](https://github.com/net2cn)
- [Real-ESRGAN-EGUI](https://github.com/WGzeyu/Real-ESRGAN-EGUI) by [WGzeyu](https://github.com/WGzeyu)
- [anime_upscaler](https://github.com/shangar21/anime_upscaler) by [shangar21](https://github.com/shangar21)
- [Upscayl](https://github.com/upscayl/upscayl) by [Nayam Amarshe](https://github.com/NayamAmarshe) and [TGS963](https://github.com/TGS963)

## 🤗 감사의 말

모든 기여자에게 감사드립니다.

- [AK391](https://github.com/AK391): [Gradio](https://github.com/gradio-app/gradio)를 사용하여 RealESRGAN을 [Huggingface Spaces](https://huggingface.co/spaces)에 통합. [Gradio 웹 데모](https://huggingface.co/spaces/akhaliq/Real-ESRGAN)를 참조하세요.
- [Asiimoviet](https://github.com/Asiimoviet): README.md를 중국어(中文)로 번역.
- [2ji3150](https://github.com/2ji3150): [자세하고 귀중한 피드백/제안](https://github.com/xinntao/Real-ESRGAN/issues/131)에 감사드립니다.
- [Jared-02](https://github.com/Jared-02): Training.md를 중국어(中文)로 번역.
