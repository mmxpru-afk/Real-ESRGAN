# :european_castle: 모델 동물원

- [일반 이미지용](#일반-이미지용)
- [애니메이션 이미지용](#애니메이션-이미지용)
- [애니메이션 비디오용](#애니메이션-비디오용)

---

## 일반 이미지용

| 모델                                                                                                                          | 배율 | 설명                                  |
| ------------------------------------------------------------------------------------------------------------------------------- | :---- | :------------------------------------------- |
| [RealESRGAN_x4plus](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth)                      | X4    | 일반 이미지용 X4 모델                  |
| [RealESRGAN_x2plus](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.1/RealESRGAN_x2plus.pth)                      | X2    | 일반 이미지용 X2 모델                  |
| [RealESRNet_x4plus](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.1/RealESRNet_x4plus.pth)                      | X4    | MSE 손실을 사용한 X4 모델 (과도한 평활화 효과) |
| [Official ESRGAN_x4](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.1/ESRGAN_SRx4_DF2KOST_official-ff704c30.pth) | X4    | 정식 ESRGAN 모델                        |
| [realesr-general-x4v3](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesr-general-x4v3.pth) | X4 (X1, X2, X3으로도 사용 가능) | 소형 모델 (훨씬 적은 GPU 메모리와 시간 소비); 약한 디블러링 및 노이즈 제거 용량 |

다음 모델들은 **판별자**이며, 일반적으로 미세 조정에 사용됩니다.

| 모델                                                                                                                 | 해당 모델 |
| ---------------------------------------------------------------------------------------------------------------------- | :------------------ |
| [RealESRGAN_x4plus_netD](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.3/RealESRGAN_x4plus_netD.pth) | RealESRGAN_x4plus   |
| [RealESRGAN_x2plus_netD](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.3/RealESRGAN_x2plus_netD.pth) | RealESRGAN_x2plus   |

## 애니메이션 이미지/삽화용

| 모델                                                                                                                         | 배율 | 설명                                                 |
| ------------------------------------------------------------------------------------------------------------------------------ | :---- | :---------------------------------------------------------- |
| [RealESRGAN_x4plus_anime_6B](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth) | X4    | 애니메이션 이미지에 최적화; 6개 RRDB 블록 (소형 네트워크) |

다음 모델들은 **판별자**이며, 일반적으로 미세 조정에 사용됩니다.

| 모델                                                                                                                                   | 해당 모델        |
| ---------------------------------------------------------------------------------------------------------------------------------------- | :------------------------- |
| [RealESRGAN_x4plus_anime_6B_netD](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B_netD.pth) | RealESRGAN_x4plus_anime_6B |

## 애니메이션 비디오용

| 모델                                                                                                                             | 배율 | 설명                    |
| ---------------------------------------------------------------------------------------------------------------------------------- | :---- | :----------------------------- |
| [realesr-animevideov3](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.5.0/realesr-animevideov3.pth) | X4<sup>1</sup>    | XS 크기의 애니메이션 비디오 모델 |

참고: <br>
<sup>1</sup> 이 모델은 X1, X2, X3으로도 사용할 수 있습니다.

다음 모델들은 **판별자**이며, 일반적으로 미세 조정에 사용됩니다.

### TODO
