---
layout: post
title: [Covid-19] Data Description
date: 2020-06-06
description: Data Description
thumbnail: breakfast-orange-lemon-oranges-large.jpg
categories: DataMining

# Information for the author block
author : Loui
---


   [df.csv]
    결과코드	resultCode	2	필수	00	결과코드  
    결과메시지	resultMsg	50	필수	OK	결과메시지  
    한 페이지 결과 수	numOfRows	4	필수	10	한 페이지 결과 수  
    페이지 번호	pageNo	4	필수	1	페이지번호  
    전체 결과 수	totalCount	4	필수	3	전체 결과 수  
    게시글번호(감염현황 고유값)	SEQ	30	필수	74	게시글번호(감염현황 고유값)  
    기준일	STATE_DT	30	필수	20200315	기준일  
    기준시간	STATE_TIME	30	필수	00:00	기준시간  
    확진자 수	DECIDE_CNT	15	필수	8162	확진자 수  
    격리해제 수	CLEAR_CNT	15	필수	834	격리해제 수  
    검사진행 수	EXAM_CNT	15	필수	16272	검사진행 수  
    사망자 수	DEATH_CNT	15	필수	75	사망자 수  
    치료중 환자 수	CARE_CNT	15	필수	7253	치료중 환자 수  
    결과 음성 수	RESUTL_NEG_CNT	15	필수	243778	결과 음성 수  
    누적 검사 수	ACC_EXAM_CNT	15	필수	268212	누적 검사 수  
    누적 검사 완료 수	ACC_EXAM_COMP_CNT	15	필수	251940	누적 검사 완료 수  
    누적 확진률	ACC_DEF_RATE	30	필수	3.2396602365	누적 환진률  
    등록일시분초	CREATE_DT	30	필수	2020-03-15 10:01:22.000	등록일시분초  
    수정일시분초	UPDATE_DT	30	필수	null	수정일시분초  

    [df_sex.csv]
    resultCode	결과코드	2	1	00	결과코드  
    resultMsg	결과메세지	50	1	NORMAL SERVICE	결과메시지  
    numOfRows	한 페이지 결과 수	4	1	10	한 페이지당 표출 데이터 수  
    pageNo	페이지 수	4	1	1	페이지 수  
    totalCount	전체 결과 수	4	1	2	전체 결과 수  
    SEQ	게시글번호(확진자 성별,연령별 고유값)	30	1	134	게시글번호(확진자 성별,연령별 고유값)  
    GUBUN	구분(성별, 연령별)	30	1	0-9	구분(성별, 연령별)  
    CONF_CASE	확진자	30	1	132	확진자  
    CONF_CASE_RATE	확진률	30	1	1.25	확진률  
    DEATH	사망자	30	1	0	사망자  
    DEATH_RATE	사망률	30	1	0.00	사망률  
    CRITICAL_RATE	치명률	30	1	0	치명률  
    CREATE_DT	등록일시분초	30	1	2020-04-13 10:22:29.663	등록일시분초  
    UPDATE_DT	수정일시분초 	30	1	null	수정일시분초   
    ※ 항목구분 : 필수(1), 옵션(0)