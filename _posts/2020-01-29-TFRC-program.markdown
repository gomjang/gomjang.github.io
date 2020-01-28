---
layout: post
title:  "TFRC(TensorFlow Research Cloud) program 사용하기"
date:   2020-01-29 01:49:35 +0900
categories:
---
Google의 [TFRC(TensorFlow Research Cloud)][tfrc-home] 프로그램을 신청하여 제한된 TPU를 무료로 사용 가능하다.  
TFRC 페이지의 [`지금 신청하기`][tfrc-apply]를 통해 Google form에 기본적인 개인 정보와 사용목적을 기입하여 제출하면 된다.


![screencapture-tensorflow-org-tfrc-2020-01-29-02_28_14](/assets/screencapture-tensorflow-org-tfrc-2020-01-29-02_28_14.png)


***1/3 개인정보***
---
![screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-viewform-2020-01-29-02_49_55](/assets/screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-viewform-2020-01-29-02_49_55.png)



신청서의 첫 페이지는 개인 정보 작성이다. 항목은 다음과 같다.


`First Name * : 이름`  
`Last Name * : 성`  
`Email * : 이메일`  
`Organization Name * : 소속`  
`Job title / role : 직책`  
`Country * : 국적`  


***2/3 연구환경과 사용 경험***
---
![screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_07_11](/assets/screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_07_11.png)


다음 두 번째 페이지는 연구환경과 사용 경험에 대한 설문이다.


`Where do you do most of your ML research today? * : 머신러닝 연구 환경`  
`How much experience do you have with Google Cloud Platform? * : GCP 사용 경험`  
`How much experience do you have with Cloud TPUs? * : TPU 사용 경험`  
`Which frameworks and tools are you most interested in using with Cloud TPUs? * : 선호하는 프레임워크`


***3/3 약관 및 개인정보 수집 동의***
---
![screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_28_30](/assets/screencapture-docs-google-forms-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_28_30.png)  


마지막 페이지는 이용 약관과 개인 정보 수집 등에 대한 동의 내용이다.


`Communication Preferences * : TPU 관련 정보메일 발송 여부`  
`AI Principles * : 구글 AI 원칙 동의 여부`  
`Terms and Conditions * : 구글 이용약관 동의 여부`  
`Privacy * : 개인 정보 수집 약관 동의 여부`  


***제출완료***
---
![screencapture-docs-google-forms-u-0-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_40_16](/assets/screencapture-docs-google-forms-u-0-d-e-1FAIpQLSeBXCs4vatyQUcePgRKh-ZiKhEODXkkoeqAKzFa-d-oSVp3iw-formResponse-2020-01-29-03_40_16.png)


신청서 제출 후 TFRC 프로그램 등록까진 경험 상 하루 정도 소요되었다.  
(신청서 제출 후 자동으로 발급되진 않고 TFRC 담당자가 신청서를 확인 후 발급해 주는 방식으로 예상된다.)  
(글 작성 중에 신청 1시간 정도 후에 등록 메일은 받았는데 TFRC 담당지역의 근무시간에 영향을 받는듯하다.(한국 새벽시간))


아래의 TFRC 승인 이메일은 2019년 11월에 신청 후 받은 안내 메일이다.  
기본적으로 TPUs는 GCP 환경에서 제공되므로 project 생성 방법과 TPU API 활성화 방법등을 안내한다.



 ![screencapture-mail-google-mail-u-1-2020-01-29-04_01_59](/assets/screencapture-mail-google-mail-u-1-2020-01-29-04_01_59.png)


TFRC 프로그램을 통해 지원되는 무료 TPUs는 제한된 유형만 사용가능 하므로 주의하여 사용해야 한다.  


**선점형(24시간 동안 선점 이후 중지될 수 있음)**  
v3-8(8G RAM) , us-central1 지역, a zone 100개  
**비선점(동작 보장됨)**  
v2-8(8G RAM) , us-central1 지역, f zone 5개  
v3-8(8G RAM) , us-central1 지역, a zone 5개  


***GCP에서 TPU node 생성 시 TFRC를 통한 할당 여부를 알려주지 않기 때문에 사용자가 할당받은 유형을 생성하여 사용하여야 TPUs 비용이 청구되지 않으니 주의하세요.***

---
![스크린샷 2020-01-29 오전 3.55.14](/assets/스크린샷%202020-01-29%20오전%203.55.14.png)  

---


끝으로 TFRC 프로그램은 기본 30일이 제공되고 종료 1주일과 1일 전에 종료 안내 메일이 발송된다.  
종료 안내 메일의 링크를 통해 feedback을 남길 수 있는데 feedback을 통해 무료 TPUs 사용기간을 추가로 연장 받을 수도 있다.  
2020년 1월 현재 기본 30일 만료 후 feedback을 통해 추가 요청하여 60일을 추가로 할당받아 사용 중이다.  



***TFRC 정책은 변경될 수 있으니 최신 정보를 확인해주세요.***



![screencapture-docs-google-forms-d-e-1FAIpQLSckh1HVK4ivMdOmNJO5CDInEJIFMhV4MBJFOzJr4UbhhNMuQQ-viewform-2020-01-29-04_19_46](/assets/screencapture-docs-google-forms-d-e-1FAIpQLSckh1HVK4ivMdOmNJO5CDInEJIFMhV4MBJFOzJr4UbhhNMuQQ-viewform-2020-01-29-04_19_46.png)



[tfrc-home]: https://www.tensorflow.org/tfrc?hl=ko
[tfrc-apply]: https://docs.google.com/forms/d/e/1FAIpQLSeBXCs4vatyQUcePgRKh_ZiKhEODXkkoeqAKzFa_d-oSVp3iw/viewform?hl=ko
