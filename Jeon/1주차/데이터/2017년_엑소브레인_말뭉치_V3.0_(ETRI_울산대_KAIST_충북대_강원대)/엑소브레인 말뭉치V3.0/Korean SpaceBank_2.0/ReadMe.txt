* 폴더 설명
a.RawCorpus : 자연어 원본 문서들 
b.KoreanSpaceBank : 공간 정보 태깅 문서들 
c.AnnotationTool(MAE) : 한국어 공간 정보 주석 툴 및 DTD 파일 수록


* 공간 정보 주석 말뭉치 파일 형태
  XML형식으로 구성
  UNIX/UTF-8


* 전체 데이터 명세
Total # of documents = 171
Total # of sentences = 1654
Total # of Place = 4922
Total # of Path = 280
Total # of Spatial Entity = 396
Total # of Motion = 254
Total # of Motion Signal = 249
Total # of Spatial Signal = 1245
Total # of Measure = 282
Total # of QSLink = 1150
Total # of OLink = 565
Total # of MoveLink = 305
Total # of MeasureLink = 345
Average # of words per sentence = 10.422611


* 말뭉치 주석 프로그램
 
말뭉치 주석 프로그램 실행시 미리 설치하여야 할 프로그램
   - Java
 
1. 말뭉치 주석 Open Source 프로그램인 MAE 다운로드
     다운로드 홈페이지 : https://code.google.com/archive/p/mae-annotation/downloads
 
2. 압축을 푼 후 폴더 내 아래 첨부된 DTD 파일 저장
 
3. 폴더내에서 명령 프롬포트 실행
    java -jar mae_v0.9.6.jar
 
4. MAE 창이 뜨면 File 메뉴 -> Load DTD 클릭하여 "SpaceEvalTaskv1.2.1.dtd" 파일 오픈
   -> MAE창 중간에 공간 정보 주석 태그 로딩 확인 가능
   -> 만약 아무런 반응이 없다면 상위 폴더들의 명칭에 한글이 들어있는지 확인. 상위폴더에 한글이 한글자라도 포함이 되면 로딩 불가.
 
5. File 메뉴 -> Load File을 클릭하여 작업할 문서 로딩 및 공간 정보 주석 말뭉치 파일 로딩
   -> 로딩이 되지 않는다면 파일명 또는 상위 폴더들의 명칭에 한글이 들어갔는지 확인.
 
6.  태깅 작업
    ----------개체 태그----------------
    - 1) 원하는 범위를 드래그
    - 2) 마우스 오른쪽 클릭 시 DTD에 정의된 개체 태그 로딩
    - 3) 원하는 태깅 클릭후 확인
 
    -----------관계 태그----------------
    - 1) Ctrl 누른 상태에서 관계가 있는 두 태그 클릭
    - 2) 새 창이 뜨며 DTD에 정의된 관계 태그 로딩
    - 3) 원하는 태깅 클릭 후 확인
 

 
* 에디터를 이용하여 말뭉치 태깅 확인

본 말뭉치는 UNIX/UTF-8 형식이므로 메모장에서는 줄바꿈이 되지 않아 보기 힘들다.
무료 프로그램인 Sublime Text 3, Notepad++ 를 다운받아 파일을 확인한다.
- Sublime Text 3 : https://www.sublimetext.com/3
- Notepad++ : https://notepad-plus-plus.org/
- 단 에디터로 말뭉치를 변경하는 행위는 추천드리지 않는다. 실수로 인해 XML형식이 어그러질수도 있기 때문이다.

