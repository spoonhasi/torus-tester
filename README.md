# Torus_Tester
---
Torus_Tester는 TORUS를 테스트할 용도로 만들어졌습니다.

## Libraries and Licenses
This project uses the following open-source libraries:

1. **ScottPlot**
   - License: [MIT License](LICENSE/LICENSE_ScottPlot.txt)
   - Copyright: (c) 2018 Scott Harden / Harden Technologies, LLC

2. **Newtonsoft.Json**
   - License: [MIT License](LICENSE/LICENSE_Newtonsoft.Json.txt)
   - Copyright: (c) 2007 James Newton-King

For detailed license information, please refer to the [LICENSE folder](LICENSE/).

## 사용법
---
- TORUS는 [torus.co.kr](https://torus.co.kr/ko/main/download)에서 받을 수 있습니다.
- 사용하려는 TORUS의 "TORUS/Example/Api"(이전 버전은 "TORUS/Example_VS19/Api")에서 아래 DLL 14개만 본 App의 TorusApi 폴더에 복사해야 합니다. 본 App은 TORUS v2.3.0 이상에서 제대로 동작합니다.
  - IntelligentApiCS.dll, ItemCS.dll, intelligentApi.dll, libAddress.dll, libAppInfo.dll, libCommandMaker.dll, libEdgeData.dll,
    libGuid.dll, libList.dll, libRpcClient.dll, libRpcServer.dll, libSharedMap.dll, libTrace.dll, zlib.dll
- 본 App을 TORUS가 인식하기 위해서 "TorusTester.info" 파일을 사용하려는 TORUS의 "TORUS/Binary/application"에 복사해야 합니다. 
- "CommonDataModels/MachineDataModelSample.txt"에 사용 가능한 MachineDataModel이 저장되어 있습니다. 마지막으로 불러온 파일이 없으면 앱 시작 시 이 파일을 불러옵니다.

## Updates
---
v2.3.20
- 공통 필터, MachineDataModel 필터가 '&'로 시작하거나 끝날 때 발생하던 크래시 수정
- 시계열 데이터 큐의 스레드 안전성 개선, 수집 시작 실패 시 수집 루프가 남던 문제 수정
- 기본 MachineDataModel 파일을 찾지 못하던 문제 수정
- Api 폴더를 TorusApi로 변경하고 필요한 DLL 14개만 유지
- 빌드 경고 제거, 문서 정리 (TORUS 다운로드 안내 추가)

v2.3.19
- 빌드 이식성 개선 (Api DLL 복사 경로를 프로젝트 상대경로로 변경)

v2.3.18
- TORUS API 업데이트
- 시계열 수집 시작 실패 시 오류코드 표시

v2.3.17
- 사용하지 않는 함수 정리

v2.3.16
- 시계열 데이터 스트림별 별개 그래프 표시

v2.3.15
- 시계열 데이터 스트림별 그래프 표시

v2.3.14
- 싱글, 멀티의 실행결과 개별 표시

v2.3.13
- 싱글, 멀티를 동시에 개별 실행할 수 있도록 수정

v2.3.12
- 오류코드 수정
- 폴더 연결시의 용량추가3종세트를 싱글방식으로 변환

v2.3.11
- 타임아웃 오류코드 수정

v2.3.10
- 시계열 데이터 수집시 현재 Status정보 파악시의 슬립 구간 조정

v2.3.9
- 시계열 데이터 수집 설정 기능 개선

v2.3.8
- 시계열 데이터 수집 설정 기능 메뉴 추가

v2.3.7
- 미구현 기능 버튼 삭제

v2.3.6
- 사용한 라이브러리의 라이센스 파일 추가

v2.3.5
- 모니터링 탭에서 Reset이 표시 안되는 버그 수정

v2.3.4
- 모니터링 탭에 알람 상태 표현 추가

v2.3.3
- MainFile 파일명 표기 관련 임시조치

v2.3.2
- 모니터링 탭의 화면 표시 개선

v2.3.1
- CurrentFile 파일명 표기 관련 임시조치

v2.3.0
- 모니터링 테스트 탭 추가
- Torus 설정 탭 추가
- getData, updateData 항목 검색 기능 추가
- 시계열 데이터 수집 기능 테스트 기능 추가

v2.2.2
- 오류코드 추가 (NC_ERR_NO_TOOL_GROUP, NC_ERR_NO_SELECETD_FILE, NC_ERR_WRONG_NAME_OF_NC_FILE)