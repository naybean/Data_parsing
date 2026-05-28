# Data_parsing

## :file_folder:IUCLID6 Genetic Toxicity Parser

IUCLID (International Uniform Chemical Information Database) is a free software application developed by ECHA (European Chemicals Agency) and the OECD.

- IUCLID6 dossier 파일(.i6z)에서 Genetic Toxicity in Vitro endpoint 정보를 추출하기 위한 스크립트입니다. 
- 본 코드는 대량의 IUCLID6 dossier 파일로부터 유전독성 데이터를 구조화된 csv 형태로 변환하기 위해 작성되었습니다.

**1. dossier_파일구조탐색_MaterialAndMethod포함.ipynb**
  - 단일 IUCLID6 dossier 파일의 내부 구조를 탐색하기 위한 스크립트
  - IUCLID dossier의 구조가 복잡하기 때문에 실제 parser 구현 전에 원하는 endpoint가 어디에 저장되어 있는지 확인하기 위해 사용

**2. iuclid dossier 파싱 Materials and Methods 포함.ipynb**
  - 다수의 IUCLID6 dossier 파일에서 Genetic Toxicity in Vitro section을 추출하여 csv 파일로 저장하는 parser
  - 추출 대상 예시:
      - Key result
      - Species / strain
      - Metabolic activation
      - Genotoxiciy
      - Cytotoxicity
      - Vehicle control validity
      - Positive / negative control validity
  - IUCLID6 내부 값들 중 일부는 숫자 또는 코드 형태로 저장되어 있음
  - 실제 텍스트 값으로 변환하기 **'list of field.csv'** 파일 사용
