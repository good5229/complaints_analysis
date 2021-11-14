# 제1회 민원 데이터 분석 공모전

응모 주제 : 제공되는 민원 데이터의 시각화 분석을 통해 정책 개선 아이디어 제시

분석 및 결과제출 : 2021년 11월 19일(금)까지

사용 데이터

- 국민권익위원회 제공 데이터(비공개)
- [OPEN API](https://www.data.go.kr/iim/api/selectAPIAcountView.do)

심사 기준
- 독창성 및 구체성
- 분석기법의 우수성
- 실현 가능성

변경사항 : bigdata.epeople.go.kr

-----------------

## 간단한 EDA

- 민원 분야명 value_counts()

    ```txt
    행정/자치/안전       18253
    국토/교통/농림/해양    13117
    교육/문화/체육/관광    11109
    재정/금융/소비자       5003
    산업/방송/통신/과학     2995
    국방/보훈/외교/통일     2216
    노동/환경           1772
    법제/사법           1414
    식품의약품            783
    기타               587
    
    Name: 분야명, dtype: int64
    ```

- 담당부서명 value_counts()

```
납세자보호담당관    2509
운영지원과       2260
감사담당관       1791
행정법무담당관     1777
민원여권과       1722
            ... 
산림병해충과         1
수질관리과          1
성북세무서          1
경남서부세관         1
항공관제국          1
Name: 담당부서명, Length: 1404, dtype: int64
```

- 주요 민원 처리 부서

```
재정/금융/소비자-납세자보호담당관       2509
산업/방송/통신/과학-행정법무담당관      1777
행정/자치/안전-감사담당관           1753
행정/자치/안전-민원여권과           1722
국토/교통/농림/해양-운영지원과        1349
교육/문화/체육/관광-총무과          1027
행정/자치/안전-청문감사인권관          923
재정/금융/소비자-규제개혁법무담당관       914
국토/교통/농림/해양-선원해사안전과       882
교육/문화/체육/관광-행정지원과         825
국토/교통/농림/해양-항만물류과         818
법제/사법-혁신행정담당관             793
식품의약품-고객지원담당관             782
교육/문화/체육/관광-행정과           739
국토/교통/농림/해양-해양수산환경과       716
국토/교통/농림/해양-고객지원담당관       712
행정/자치/안전-법무감사혁신담당관        676
노동/환경-운영지원과               675
산업/방송/통신/과학-규제개혁법무담당관     625
행정/자치/안전-시민봉사담당관          619
국토/교통/농림/해양-도로안전운영과       614
행정/자치/안전-민원봉사과            597
국토/교통/농림/해양-시설안전관리과       513
국토/교통/농림/해양-항로표지과         434
교육/문화/체육/관광-중등교육지원과       423
행정/자치/안전-경무과              407
행정/자치/안전-혁신소통기획관          390
행정/자치/안전-민원토지과            380
행정/자치/안전-민원지적과            375
교육/문화/체육/관광-학교운영지원과       349
행정/자치/안전-통합민원과            347
교육/문화/체육/관광-대학재정장학과       301
교육/문화/체육/관광-학교지원과         297
교육/문화/체육/관광-유초등교육지원과      294
교육/문화/체육/관광-학술진흥과         278
행정/자치/안전-자치행정과            273
행정/자치/안전-토지민원과            271
국방/보훈/외교/통일-고객지원과         263
행정/자치/안전-민원과              255
행정/자치/안전-교통행정과            249
행정/자치/안전-종합민원과            249
교육/문화/체육/관광-학생건강지원과       249
국토/교통/농림/해양-하천계획과         248
교육/문화/체육/관광-평생교육건강과       248
교육/문화/체육/관광-교원정책과         243
교육/문화/체육/관광-초등교육지원과       234
국토/교통/농림/해양-보상과           227
교육/문화/체육/관광-중등교육과         224
행정/자치/안전-열린민원과            208
교육/문화/체육/관광-재정지원과         208
행정/자치/안전-종합민원실            205
교육/문화/체육/관광-교육협력복지과       204
국토/교통/농림/해양-항만건설과         203
행정/자치/안전-소통민원과            195
국토/교통/농림/해양-도로계획과         190
행정/자치/안전-시정혁신담당관          187
산업/방송/통신/과학-인터넷이용자정책과     186
교육/문화/체육/관광-학교통합지원센터      185
행정/자치/안전-시민봉사과            184
교육/문화/체육/관광-시설과           181
Name: 분야명-담당부서명, dtype: int64
```

## 주제 후보군 리스트

- 분야별로 주로 묻는 민원의 주요 키워드와 해당 분야의 민원이 주로 발생하는 날짜, 시기는 어떻게 될까?
    - 이를 통해 특정 요일에 따라 민원 담당인을 유동적으로 배치해서 민원 담당자의 업무를 분담할 수 있지 않을까?
    - 
- 

