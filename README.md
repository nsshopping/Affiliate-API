# Affiliate-API

 NS홈쇼핑 입점을 위해 제공하는 Open API 입니다.
 관련하여 추가 문의 내용은 itcs@nsmall.com 으로 문의하시면 보다 자세한 안내 드리겠습니다.

** 공지사항 (가이드)
  1. 최신버전의 API 가이드 : NSMall_EDI_API_Specs_v2.6_20250401.xls
  2. API 개발 에러메시지 가이드 : IB_API_ReturnMessage_v2.6_20250401.xls
  3. 방화벽요청서 : NS_API 방화벽요청서_V2.0.xls
  4. 변경 및 공지 가이드 : README.md

  [Ver 2.6] (변경날짜 2025-04-01)
  - API : 배송연동 API 전송시, 택배사별 송장 길이 체크(필수)
  - API 메시지 : DV 배송 메시지 항목 추가

  [Ver 2.5] (변경날짜 2025-03-11)
  - InBound API 도메인 변경

  [Ver 2.4.1] (변경날짜 2024-08-28)
  - 상품등록/상품수정 API 전송시, 상품정합성 검증 프로세스 개선<br>
     기존 : 등록/수정 API 전송 -> 정상수집 완료 회신, 상품 등록/수정 등록조회시 실패사유 전달<br>
     개선 : 등록/수정 API 전송 -> 상품정합성 체크 후 수집 완료 회신<br>
     
 ※ 협력사에서 상품등록/수정API 전송 후 상품결과 조회에 대한 빠른 확인 가능하도록 개선.
 
  [Ver 2.4] (변경날짜 2024-07-12)
  - 추가단품등록 API 정책 변경
  - 옵션별 가격상이(UT)상품일 경우, MD승인이 필요하도록 내부정책 변경 
 ※ 균일가(GD)상품일 경우 기존과 동일.
    
  [Ver 2.3] (변경날짜 2023-09-20)
  - 가격수정 API 추가
  - 전시매장수정 API 내 삭제 플래그 추가
  
  [Ver 2.1] (변경날짜 2023-01-18)
  - 도서분류상품 등록시, 도서원가 필수 항목 추가
 
  [Ver 2.0] (변경날짜 2022-12-07)
  - 단계형옵션 상품등록,단품추가등록 API 신규 필드 추가 
  
  [Ver 1.5] (변경날짜 2022-10-28)
  - 택배사코드(LSC_CD) 추가/갱신 
  
  [Ver 1.43] (변경날짜 2022-03-21)
  - 도서분류체계 상품 등록시, 도서필수 정보3개 추가 (도서분류시 필수)
  - 상품등록(GoodsAdd), 상품수정(GoodsMod) API에 필드(BOOK_TYPE,BOOK_GUBUN, BOOK_IS_NUM)
  
  [Ver 1.40] (변경날짜 2020-11-10)
  - 안전확인대상 생활화학제품에 대해 안전확인신고번호 표기 필수
  - 상품등록(GoodsAdd), 상품수정(GoodsMod) API에 SAFE_CERT_VAL 필드 추가
  
  [Ver 1.39] (변경날짜 2020-10-21)
  - 안전인증 대상 상품분류코드에 대해 안전인증코드 필수
  - 상품등록(GoodsAdd), 상품수정(GoodsMod) API에 SAFE_CERT_CD, SAFE_CERT_NUM 필드 추가
    
  [제휴_인바운드_API_에러리턴메세지_ver 1.3] (변경날짜 2020-10-21)
   - 안전인증대상 관련 필드 추가에 따른 에러리턴메시지 추가 
     리턴 메시지 : 
     안전 인증 코드 [SAFE_CERT_CD] 는 최대 숫자 2 자리 까지 입력가능 합니다.
     안전 인증 번호 [SAFE_CERT_NUM] 는 최대 50 Byte 입력 가능 합니다.
     안전 인증 번호 [SAFE_CERT_NUM] 는 최소 12 최대 15 자리입니다.
  
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

