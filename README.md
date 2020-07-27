# Affiliate-API

 NS홈쇼핑 입점을 위해 제공하는 Open API 입니다.
 관련하여 추가 문의 내용은 itcs@nsmall.com 으로 문의하시면 보다 자세한 안내 드리겠습니다.

** 공지사항 (가이드)
  1. 최신버전의 API 가이드 : NSMall_EDI_API_Specs_v1.36_20190503
  2. API 개발 에러메시지 가이드 : 제휴_인바운드_API_에러리턴메세지_v1.0.xlsx
  3. 변경 및 공지 가이드 : README.md
  
  [Ver 1.38] (변경날짜 2020-07-27)
  - 택배사 코드 20 값 업데이트
    **20(현대) --> 20(롯데)
  - 상품 등록 및 출고지 수정 API 사용시 배송방법코드(DLVR_WAY_CD2) 업데이트
    **40(중량화물) --> 40(제휴)
    
  
  [제휴_인바운드_API_에러리턴메세지_ver 1.2] (변경날짜 2020-04-08)
   - 상품 등록 및 수정 API 사용시 상품명에 '사은품', '증정', '공짜찬스' 문자열은 등록이 불가합니다. 
     리턴 메시지 : 상품명에 등록될 수 없는 문자열[사은품, 증정, 공짜찬스]이 포함되어 있습니다.

  
  [Ver 1.37] (변경날짜 2019-09-23)
   - 변경사항 NSMall_EDI_API_Specs_v1.37_20190923.xls 파일에서 전문의 변경된 부분은 노란색으로 표시하였습니다.
     변경 프로세스의 경우, 해당 PPT 파일을 참조하시면 됩니다. (참조 : NSMall_EDI_API_Specs_v1.37_API변경내용_v0.2.pptx)

   ** 전송하는 URL 주소가 변경되니, 필히 정책사항 및 변경사항 확인해주세요.
   
  [Ver 1.36] (변경날짜 2019-05-03)
   - DV101(배송정보 연동)<br>
     LSC_CD(택배사코드) 업데이트(NS홈쇼핑에서 사용중인 택배사 코드로 재정의)<br><br>
     **신규택배사 7개 (98:천일, 105:경동택배, 109:애니트랙, 111:대신, 112:합동,113:GTX로지스, 117:롯데국제특송)<br>
     **미사용 택배사 16개 (50:HTH, 60:동원, 71:이노지스, 78: 하나로, 84:트라넷, 85:주코, 86:일개미, 87:중앙, 88:한국, 90:기타, 92:한솔, 93:KGB특급택배, 94:다운, 95:삼성전자, 96:사가와익스프레스코리아, 97:세덱스)

  [Ver 1.35] (변경날짜 2019-04-24)
   - GD101(상품등록) / 필수값 추가<br>
     상품등록 API에 INQRY_KEY(조회 KEY) 컬럼 입력 필수
  
  [Ver 1.34] (변경날짜 2018-07-18)
   - GD101(상품등록) / 필수값 추가
  
  [Ver 1.33] (변경날짜 2018-06-04)
   - GD101(상품등록) / GD112(상품별 출고지 수정)

   [Ver 1.32] (변경날짜 2018-05-14)<br>
   - CS 리스트/답변등록 정보요청 API 추가<br>
   - GD111(출고지정보 등록/수정)의 도로명 주소 입력시, 필수값[BLD_MNG_NUM(건물관리번호)] 추가<br>
   <br>
   [Ver 1.31] (변경날짜 2018-04-23)<br>
   - 상품정보(GD101) 비고 항목에 설명 추가<br>
  <br>
   [Ver 1.30] (변경날짜 2018-02-21)
   - 발주정보조회(OR101)에 컬럼 1개 추가
   
   [Ver 1.29] (변경날짜 2017-11-29)
   -  네이버 가격비교에 제공하는 상품 필수정보 추가
   -  @ 변경 사항 (GD101:상품등록, GD103:상품수정)
      - 상품 상태 코드(GOODS_STAT_CD) 추가) 
      - 주문 제작 여부(ORDER_PRDT_YN) 추가) 
      - 국내 해외 방식 코드(DMST_OVS_MEANS_CD) 추가)
      - 판매 방식 코드(SALE_MEANS_CD) 추가)
      - 별도 설치비 여부(EXTRA_INSTF_YN) 추가) 
      - 차등 배송비 여부(DSCR_DLVRF_YN) 추가) 
      
   [Ver 1.28] (변경날짜 2017-11-08)
   -  상품 단품(옵션)의 대표상품.가격으로 선택 기능 추가
   -  @ 변경 사항
      - GD101:상품등록 (대표 단품 순번(RPRSN_UNIT_SEQ) 추가)
      - GD103:상품수정 (대표 단품 코드(RPRSN_UNIT_CD) 추가)
      - CM103:상품별단품조회 (대표 가격 여부(RPRSN_YN) 추가)
       
   [Ver 1.27] (변경날짜 2017-05-30)
   -  출고지정보API(GD112)에 필수항목 5개
      자동승인 업체에 대한 필수 제외 기능
  
  [Ver 1.26] (변경날짜 2017-05-26)
  -  출고지정보API(GD112)에 필수항목 5개 추가
   -  @ 변경 사항
      - 배송수단, 출고지 택배사, 반송택배사, AS출고지택배사, AS반송택배사

  [Ver 1.25] (변경날짜 2017-01-18)
  - 업체 지연 사유 내용/미배송 출고 예정 일자 추가
 
 [Ver 1.24] (변경날짜 2016-11-28) 
 - 안전 인증 코드/안전 인증 번호 추가
 
 [Ver 1.23] (변경날짜 2016-02-17)
  - 상품명 기술서 max 수정

