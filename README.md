<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:1f6feb&height=120&section=header"/>

<!-- OT/ICS(솔루션)와 취약점 제보를 분리된 줄로 표현 -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=680&lines=OT%2FICS+Security+Solution+Builder;Vulnerability+Disclosure+%7C+KVE-2026-0123;Backend+Dev+%7C+DevSecOps+%7C+OnPremise+Ops;BoB+14th+%7C+Wireshark+OSS+Contributor" alt="Typing SVG"/>

<br/>

<img src="https://img.shields.io/badge/OT%2FICS_Security-Solution_Builder-FF4500?style=flat-square"/>
<img src="https://img.shields.io/badge/Vuln_Disclosure-KVE--2026--0123-2563EB?style=flat-square"/>
<img src="https://img.shields.io/badge/BoB_14기-보안제품개발트랙-CC0000?style=flat-square"/>
<img src="https://img.shields.io/badge/Wireshark_Contributor-MR_%2322852_Approved-1679A7?style=flat-square&logo=wireshark&logoColor=white"/>

</div>

<br/>

## 🧑‍💻 About Me

| | |
|:--|:--|
| **OT/ICS 보안** | 솔루션 구축 · 산업 제어 시스템 대상 비침투적 보안 모니터링 설계·검증 |
| **취약점 제보** | 대법원 KVE-2026-0123 · CLASSUM SSO — 책임 제보 및 패치 기여 |
| **BoB 14기** | 보안제품개발트랙 · KISA 한국인터넷진흥원 |
| **OSS 기여** | Wireshark XGT_FEnet dissector MR #22852 Approved |
| **백엔드 / 운영** | Spring Boot · 온프레미스 · DevSecOps |
| **현재** | IaC 기반 하이브리드 클라우드 인프라 부트캠프 (메가스터디IT아카데미, 2026.02~08) |

> OT/ICS 보안은 **취약점 발굴이 아닌 솔루션 구축** 영역에서 수행했습니다.  
> Modbus TCP · S7Comm · XGT_FEnet 프로토콜 분석, 비침투적 탐지 파이프라인 설계,  
> Wireshark dissector 기여까지 직접 진행했습니다.

<br/>

---

## 🎖️ BoB 14th — 보안제품개발트랙

> **KISA 한국인터넷진흥원 · 2025.07 — 2026.02**  
> 보안 심화교육 + 트랙 전문교육 + 최종 프로젝트(SLiMe)

### Network Track (트랙 교육)

저수준 네트워크 구현부터 커널 레벨 패킷 처리까지 직접 구현했습니다.

| 주제 | 내용 | repository |
|------|------|------|
| **Network Byte Order** | Big/Little Endian 변환, NBO 기반 데이터 송수신 구조 이해 | [01_sum_nbo](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/01_sum_nbo) |
| **OSI / TCP 헤더 파싱** | Ethernet · IP · TCP 헤더를 C로 직접 파싱, 각 필드 추출 및 검증 | [osi-and-tcp](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/osi-and-tcp) |
| **pcap 패킷 캡처** | libpcap 기반 실시간 패킷 캡처 및 필터링 구현 | [pcap-test](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/pcap-test) |
| **ARP 패킷 전송** | 직접 ARP Request/Reply 패킷을 구성해 raw socket으로 전송 | [send-arp](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/send-arp) |
| **ARP Spoofing** | ARP Cache Poisoning 구현 — 타깃과 게이트웨이 사이 트래픽 가로채기 | [arp-spoof](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/arp-spoof) |
| **Socket 프로그래밍** | C++ 기반 TCP Echo Server/Client 구현, 연결 흐름 및 버퍼 처리 | [echo-server-client](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/echo-server-client) |
| **netfilter / iptables** | 커널 netfilter hook 기반 패킷 조작 및 차단 룰 구현 | [netfilter](https://github.com/BoB14-dev-Ryu-Gi-Hyeon/netfilter) |

### OT/ICS Security — Final Project: SLiMe

> 산업 제어 시스템(SCADA·PLC) 환경을 대상으로 한 **비침투적 보안 모니터링 솔루션 구축**  
> OT 장비와 직접 통신하지 않고, 트래픽 미러링(SPAN/TAP) 기반으로만 동작합니다.

| 역할 | 세부 내용 |
|:--|:--|
| **C++ 파서 고도화** | 처리속도 2.7배↑ (2.40s→0.89s) · 메모리 72%↓ · 처리량 3,370 pps |
| **Wireshark 기여** | XGT_FEnet dissector → 공식 저장소 MR #22852 Approved |
| **OT 테스트베드** | Docker 기반 SCADA 1대 + PLC 4대 (Modbus TCP) |
| **탐지 파이프라인** | Redis / Elasticsearch 기반 저지연 설계 |
| **SLM 데이터** | Python · 슬라이딩 윈도우 · 자산 매핑 · JSONL 생성 |
| **백엔드 / 대시보드** | Spring Boot + SSE 실시간 대시보드 연동 |

**커버 프로토콜:** `Modbus TCP` · `S7Comm` · `XGT_FEnet (LS Electric)`  
**위협 모델:** Purdue Model 기반 IT→OT 침투, PLC 비정상 제어 명령 탈취 시나리오  
**결과:** 팀 탐지 정확도 94% · 창업진흥원장 우수상 (STARTUP WATER 2025)

[![SLiMe Org](https://img.shields.io/badge/GitHub-BoB14th--SLiMe-181717?style=flat-square&logo=github)](https://github.com/BoB14th-SLiMe)
[![Wireshark MR](https://img.shields.io/badge/Wireshark-MR_%2322852_Approved-1679A7?style=flat-square&logo=wireshark&logoColor=white)](https://gitlab.com/wireshark/wireshark/-/merge_requests/22852)

<br/>

---

## 🛡️ Vulnerability Disclosure

| 날짜 | 대상 | 취약점 | 결과 |
|------|------|--------|------|
| 2026.01 | 대법원 전자가족관계등록시스템 | 인증 토큰 URL 노출 · 세션 바인딩 미흡 → 제3자 무인증 열람 | KVE-2026-0123 · 13일 패치 |
| 2025.12 | CLASSUM SSO | URL 인증 토큰 노출 · Replay Attack → ATO (CWE-598 · CWE-294) | Critical · 29일 패치 |

<br/>

---

## 🚀 Featured Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>SLiMe — OT/ICS 보안 모니터링 솔루션</h3>
      <p>SCADA·PLC 환경 대상 비침투적 산업 프로토콜 트래픽 분석 시스템. C++ 파서 고도화, Wireshark OSS 기여, Redis/Elasticsearch 탐지 파이프라인, SLM 학습 데이터 구축, 실시간 대시보드까지 구현.</p>
      <p>
        <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
        <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
        <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
        <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white"/>
        <img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white"/>
      </p>
      <p>창업진흥원장 우수상 · 탐지 정확도 94% · BoB 14기 최종 프로젝트</p>
      <a href="https://github.com/BoB14th-SLiMe">Organization →</a>
    </td>
    <td width="50%" valign="top">
      <h3>알림IT — 울산대 공지 알림 서비스</h3>
      <p>14개 학과 공지 자동 수집 → Android/iOS 실시간 알림. 온프레미스 서버를 직접 운영하며 Fail2ban 침입 탐지, 국가 IP 필터링, 악성 스캐너 117개 차단까지 DevSecOps 전반 담당.</p>
      <p>
        <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
        <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
        <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/>
        <img src="https://img.shields.io/badge/Fail2ban-333?style=flat-square"/>
        <img src="https://img.shields.io/badge/Firebase_FCM-FFCA28?style=flat-square&logo=firebase&logoColor=black"/>
      </p>
      <p>실사용자 51명 · 누적 알림 91건 · 운영 중</p>
      <a href="https://github.com/AlarmU-Ulsan">Organization →</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>한바퀴 — 위치 기반 화물 매칭 플랫폼</h3>
      <p>공차율 최소화를 목표로 빈 차량과 화물을 매칭하는 플랫폼. Spring Boot 백엔드, Android 앱, T-Map/Kakao SDK, Raspberry Pi 3 홈서버 온프레미스 배포까지 풀사이클 개발.</p>
      <p>
        <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
        <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
        <img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white"/>
        <img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white"/>
      </p>
      <a href="https://github.com/roundCargo">Organization →</a>
    </td>
    <td width="50%" valign="top">
      <h3>Yesol — 전공 학습 커뮤니티 플랫폼</h3>
      <p>전공 문제·해설 카드 기반 학습 플랫폼. 백엔드 팀장으로 JWT+Redis 인증, Kakao 소셜 로그인, AWS S3, GitHub Actions CI/CD, AWS Elastic Beanstalk 배포까지 핵심 구조 설계.</p>
      <p>
        <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
        <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
        <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white"/>
        <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
      </p>
    </td>
  </tr>
</table>

<br/>

---

## 🛠️ Tech Stack

**Security**  
![OT/ICS](https://img.shields.io/badge/OT%2FICS_Monitoring-FF4500?style=flat-square)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square)
![OWASP](https://img.shields.io/badge/OWASP_Top_10-000000?style=flat-square)
![Fail2ban](https://img.shields.io/badge/Fail2ban%2Fiptables-333?style=flat-square)

**Backend**  
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA%2FHibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Firebase FCM](https://img.shields.io/badge/Firebase_FCM-FFCA28?style=flat-square&logo=firebase&logoColor=black)

**Script & System**  
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Infra / Cloud**  
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale_VPN-0067B3?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Network**  
![CISCO](https://img.shields.io/badge/CISCO-1BA0D7?style=flat-square&logo=cisco&logoColor=white)
![TCP/IP](https://img.shields.io/badge/TCP%2FIP%2FOSI-555?style=flat-square)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)

**Database**  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%2FPostGIS-4169E1?style=flat-square&logo=postgresql&logoColor=white)

<br/>

---

## 🏅 Notable Achievements

| 날짜 | 내용 |
|------|------|
| 2026.03 | **Wireshark 오픈소스 기여** — XGT_FEnet 산업 프로토콜 dissector MR #22852 Approved |
| 2026.01 | **대법원 취약점 제보** — KVE-2026-0123, 제보 후 13일 패치 완료 |
| 2025.12 | **CLASSUM 취약점 제보** — SSO Replay Attack (ATO), 29일 패치 완료 |
| 2025.11 | **AquaSLiMe 우수상** — STARTUP WATER 2025 · 창업진흥원장 |
| 2025.11 | **제2회 울산 모의해킹 대회** — 침해사고 부문 본선 진출 |
| 2025.07 | **BoB(Best of the Best) 14기** — KISA 보안제품개발트랙 수료 |

<br/>

## 📊 GitHub Stats

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=RyuGiHyeon&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=RyuGiHyeon&layout=compact&theme=github_dark&hide_border=true&langs_count=8"/>
</div>
<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=RyuGiHyeon&theme=github-dark-blue&hide_border=true"/>
</div>

<br/>

## 📜 Certifications

- **SQLD** — 한국데이터산업진흥원 `2024.03`
- **네트워크관리사 2급** — 한국정보통신자격협회 `2026.03`

<br/>

## 📬 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-RyuGiHyeon-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RyuGiHyeon)
[![Portfolio](https://img.shields.io/badge/Portfolio-ryugihyeon.github.io-1f6feb?style=for-the-badge&logo=githubpages&logoColor=white)](https://ryugihyeon.github.io/portfolio/)

</div>

<br/>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:1f6feb,50:161b22,100:0d1117&height=100&section=footer"/>
</div>