# upgraded 디렉터리 구조 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일 및 폴더 구조를 복사한 디렉터리입니다. 이곳에서 Python 2.5 기반의 레거시 코드를 Python 3 등 최신 환경에 맞게 업그레이드 및 리팩터링 작업을 진행하게 됩니다.

## 주요 하위 구조

- `MANIFEST.in`, `README.rst`, `setup.py`, `distribute_setup.py`, `distribute-0.6.10.tar.gz`: 프로젝트 메타/설치 파일 및 레거시 배포 관련 파일
- `docs/`: 프로젝트 문서 및 Sphinx 기반 빌드 산출물
  - `build/`: 빌드된 문서(HTML, doctree 등)
  - `source/`: Sphinx 문서 원본(rst, conf.py 등)
- `guachi/`: 실제 Python 패키지 소스 코드
  - `__init__.py`, `config.py`, `database.py`: 주요 모듈
  - `tests/`: 단위 테스트 코드
- `guachi.egg-info/`: 패키지 메타데이터(빌드/설치 시 생성)

## 활용 목적

- 이 디렉터리에서 레거시 코드를 최신 Python 문법 및 패키징 방식으로 점진적으로 업그레이드합니다.
- 테스트, 문서, 설치 스크립트 등 모든 부분을 최신화하며, 변경 전후의 동작을 비교할 수 있습니다.
- 업그레이드 작업의 각 단계를 독립적으로 실험하고 검증할 수 있습니다.
