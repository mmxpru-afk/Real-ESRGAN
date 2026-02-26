# 자주 묻는 질문 (FAQ)

1. **Q: 어떤 모델을 선택해야 하나요?**<br>
A: [docs/model_zoo_KO.md](docs/model_zoo_KO.md)를 참조하세요

1. **Q: `face_enhance`를 애니메이션 이미지/애니메이션 비디오에 사용할 수 있나요?**<br>
A: 아니요, 실제 얼굴에만 사용할 수 있습니다. 애니메이션 이미지/애니메이션 비디오에 이 옵션을 사용하지 않는 것이 좋습니다(GPU 메모리 절약).

1. **Q: "slow_conv2d_cpu" is not implemented for 'Half' 오류가 발생합니다**<br>
A: GPU 메모리 소비를 절약하고 추론 속도를 높이기 위해 Real-ESRGAN은 기본적으로 추론 중에 반정밀도(fp16)를 사용합니다. 그러나 반정밀도 추론을 위한 일부 연산자가 CPU 모드에서 구현되지 않았습니다. 명령에 **`--fp32` 옵션**을 추가해야 합니다. 예를 들어, `python inference_realesrgan.py -n RealESRGAN_x4plus.pth -i inputs --fp32`.
