# Real-ESRGAN 기여 안내

:art: Real-ESRGAN에 기여해 주셔서 감사합니다. 새로운 기능/모델/오타 수정/제안/유지보수 등 모든 종류의 기여를 환영합니다. 모든 기여자는 [README.md](../README.md#hugs-acknowledgement)에 목록으로 표시됩니다.

오픈 소스를 지향하며 일반 이미지 복원을 위한 실용적인 알고리즘을 함께 개발하고자 합니다. 개인의 힘에는 한계가 있으므로 다음과 같은 다양한 기여를 환영합니다:

- 새로운 기능 제안 및 구현
- 새로운 모델 (사용자 미세조정 모델)
- 버그 수정
- 오타 수정
- 개선 제안
- 유지보수
- 문서 보강
- 기타

## 워크플로우

1. Real-ESRGAN 저장소를 포크(fork)하고 최신 상태로 동기화합니다.
2. 새 브랜치를 체크아웃합니다 (PR에는 `master` 브랜치 사용을 피하세요).
3. 변경사항을 커밋합니다.
4. 풀 리퀘스트(PR)를 생성합니다.

**참고**:

1. 코드 스타일 및 린트(lint) 규칙을 확인하세요.
   1. 스타일 설정은 `setup.cfg`에 명시되어 있습니다.
   2. VSCode를 사용하면 `.vscode/settings.json`에 일부 설정이 포함되어 있습니다.
2. `pre-commit` 훅 사용을 강력히 권장합니다. 커밋 전에 코드 스타일과 린트 검사를 자동으로 수행합니다.
   1. 프로젝트 루트에서 `pre-commit install`을 실행하세요.
   2. `pre-commit` 설정은 `.pre-commit-config.yaml`에 있습니다.
3. 큰 변경을 하기 전에 [Discussions](https://github.com/xinntao/Real-ESRGAN/discussions)에 먼저 이슈나 토론을 여는 것이 좋습니다.
   1. 환영합니다 :sunglasses: 가능하면 저도 토론에 참여하겠습니다.

## TODO 리스트

:zero: 모델 성능을 개선하는 가장 직접적인 방법은 특정 데이터셋에 대해 미세조정(fine-tune)하는 것입니다.

다음은 현재 고려 중인 TODO 항목들입니다:

- [ ] 사람 얼굴(인물)에 최적화
- [ ] 텍스트(문자)에 최적화
- [ ] 복원 강도 조절(컨트롤 가능한 복원)

:one: 또한 개선이 필요한 여러 [이슈](https://github.com/xinntao/Real-ESRGAN/issues)가 있습니다. 도움 가능하시면 알려주세요 :smile:
