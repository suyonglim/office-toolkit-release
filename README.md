# Office Toolkit 배포 파일

PowerPoint·PDF·Excel 문서 작업을 돕는 Windows용 도구 모음 **Office Toolkit**의 설치 파일과 업데이트 정보(`latest.json`)를 두는 저장소입니다. 소스 코드는 여기에 없습니다.

## 설치

1. 오른쪽 **Releases**에서 맨 위(Latest) 버전의 `Office_Toolkit_setup_<버전>_<날짜>.exe`를 받습니다.
2. 받은 파일을 실행하고 이용 조건에 동의한 뒤 설치합니다. 관리자 권한은 필요하지 않습니다.
3. 설치 후에는 프로그램이 새 버전을 스스로 확인하고 알려 줍니다. 알림 창에서 업데이트를 고르면 받고, 설치하고, 다시 실행합니다.

필요 환경: Windows 10/11 (64비트), Microsoft Edge WebView2 런타임(Windows 11에는 기본으로 들어 있음). 일부 기능은 Microsoft PowerPoint·Excel이 설치되어 있어야 합니다.

### "Windows의 PC 보호" 창이 뜰 때

설치 파일에 코드 서명이 없어서, 처음 받는 PC에서는 SmartScreen 경고가 뜰 수 있습니다. **추가 정보 → 실행**을 누르면 설치가 진행됩니다. 받은 파일이 원본과 같은지는 아래처럼 확인할 수 있습니다.

```powershell
Get-FileHash .\Office_Toolkit_setup_1.1.3_20261127.exe -Algorithm SHA256
```

출력된 값이 해당 릴리스의 `latest.json`에 적힌 `sha256`과 같으면 원본입니다.

## 인터넷 연결과 개인정보

- 프로그램은 새 버전을 확인하려고 실행 중에 이 저장소의 `latest.json`을 읽고, 업데이트를 고르면 여기서 설치 파일을 받습니다.
- 이때 IP 주소 등 접속 정보가 GitHub에 남으며, [GitHub 개인정보 처리방침](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement)을 따릅니다.
- 개발자는 이용자의 개인정보나 문서 내용을 수집하지 않습니다. 작업 기록은 이용자 PC에만 저장됩니다.
- 업데이트 정보는 전자 서명(Ed25519)으로 확인하므로, 서명이 맞지 않는 업데이트는 설치되지 않습니다.

## 이용 조건과 오픈 소스 고지

- 이용 조건: 설치 화면과 설치 폴더의 `TERMS_OF_USE.txt`.
  - 개인 용도로 무료로 사용할 수 있습니다. 회사·기관·단체의 업무에 쓰려면 별도 허락이 필요합니다(아래 문의처로 연락).
  - 설치 파일을 고치지 않은 그대로 다른 사람에게 직접 전달할 수 있습니다.
  - 판매, 고쳐서 배포, 역분석, 다른 웹사이트·자료실 등에 올리는 것은 할 수 없습니다. 이 페이지 주소를 알려 주는 것은 괜찮습니다.
  - 프로그램은 "있는 그대로" 제공됩니다.
- 오픈 소스 고지: 설치 폴더의 `THIRD_PARTY_NOTICES.txt`(시작 메뉴 → Office Toolkit → 오픈 소스 고지). 들어 있는 오픈 소스 구성 요소와 각 라이선스 문구를 모아 두었습니다.

## 문의

이메일: yong8635@naver.com (사용 문의, 업무 사용 허락 요청, 오류 신고)

---

Microsoft, Windows, Office, PowerPoint, Excel은 Microsoft Corporation의 상표입니다. 이 프로그램은 Microsoft와 관계가 없으며, Microsoft가 만들거나 보증한 제품이 아닙니다.
