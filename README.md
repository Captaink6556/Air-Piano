# Air Piano

## Introduction
오픈포즈 라이브러리를 이용하여 기본 스켈레톤 기능을 사용하고 알고리즘에 추가적인 기능을 부여하여 손의 위치에 따라 음을 내는 기능을 추가하였다. 이것을 통해 몸의 동작을 이용해 음을 내는 알고리즘을 개발하였다.

1\. 기본기능
- 왼손의 위치에 따른 피아노 건만 위치 조정기능 지원
- 오른손 좌표를 통한 음색 출력기능 지원
- 특정 좌표에 따른 각각의 음색 저장
- 손의 모양에 따른 ON/OFF 기능 지원

2\. UI 및 이펙트
- 피아노 건반 사이에 붉은 라인으로 나눔

3\. 최적화
- Pose Estimation을 이용한 신체관절 추출을 통한 시각적 지원
- Fully connected network를 적용한 손관절 추출을 통한 시작적 지원

4\. 배포
- PC 빌드 및 배포


## Quick Start

### Windows 10
- OpenCV
- [pytorch](https://pytorch.org/)
- [rtmidi](https://pypi.org/project/python-rtmidi/)
- [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)
    1. Visual Studio
    1. Get model
        1. openpose/models/getModels.bat
    1. Add 3rdparty 
        1. openpose/3rdparty/pybind11
    1. CMake
        1. build
        1. BUILD_PYTHON : check
        1. Add Entry : PYTHON_VERSION
        1. Add Entry : PYTHON_EXECUTABLE
        1. openpose/build/OpenPose.sln 실행, Release, build
