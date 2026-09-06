# CHANGELOG — Tim Focaccia 팀포카치아 (timfocaccia-sample)

## v0.8 (2026-09-06) 히어로 간격·직각 코너 + 투박 비교버전
- **히어로 하단 간격**: 사진과 어닝 띠가 붙어보임 → .hero 하단 패딩 clamp(34px,5vw,60px).
- **라운드 코너 전부 직각**: border-radius 12곳 모두 0(사진·카드·버튼·배지·칩·퀵바 등). 살루메리아 델리 각진 라벨 방향.
- **투박 비교버전 `index-rustic.html` 신설**(다올: 흰 배경이 델리 느낌 약함 → "AI 티 안 나는 투박함"이 배경색이 아니라 실행[그림자·그라데이션·라운드] 문제라 진단). 현 흰색 index.html 유지하고 자산 공유하는 sibling 파일로 나란히 비교:
  - 배경 **페이퍼 크림**(--bg#F4EDDD·bg2#E9DEC6·card#FBF5E6, 채도 낮은 페이퍼톤·밝게 유지해 실사진과 정합).
  - **소프트 그림자 전부 제거 → 하드 보더**(--bd#2E2519, 사진/카드/갤러리 2px·1.6px 실선).
  - **종이 그레인**(body::before feTurbulence 노이즈 opacity .055).
  - **아이브로=테두리 라벨칩**, **배지=러버 스탬프**(흰 테두리+아웃라인+살짝 회전).
  - AA 크림bg 전부≥4.5(red/bg 4.66 최저). ⚠️미결: 다올이 흰색본 vs 투박본 중 택1(택1 후 나머지 정리).

## v0.7 (2026-09-06) 히어로 사진 교체 + 제목 확대
- **히어로 사진 교체**: 다올 제공 tim-hero.jpg(1216×2160, 나무 도마 위 햄·구운 토마토·녹인 치즈 포카치아)→webp(1200폭, q84) 최적화해 tim-hero.webp 덮어씀. alt 갱신. 원본 jpg는 `.assetsignore` 제외.
- **히어로 제목 확대**(다올: 화면이 비어보임): 텍스트 칸 그리드 1.02fr→**1.12fr**(이미지 살짝 축소), h1 max 5rem→**5.4rem**(clamp(3.1rem,7vw,5.4rem)), letter-spacing 0. 한 줄(nowrap) 유지. ⚠️넓은 화면 칸 넘침 방지 위해 상한 관리 — 실기기 렌더 확인 권장.

## v0.6 (2026-09-06) 히어로 한 줄 + 파랑→초록(이탈리아 국기)
- **히어로 제목 한 줄**: "Tim / Focaccia" 2줄 → **"Tim Focaccia" 1줄**(em 레드). h1 clamp(2.4rem,8.4vw,5rem)+`white-space:nowrap`로 한 줄 보장.
- **파랑→초록 전환**(다올: 빨강·파랑·하양은 프랑스 국기 연상 → 이탈리아는 초록·하양·빨강): sky#3C6E94 → **바질 그린 --grn#3E7A4E**(grn-d#2F5E3C). sky 토큰·`.btn-ol-sky`·`.btn-sky`·`.stripe.sky` 전부 grn으로 개명.
- **어닝 스트라이프 이탈리아 국기 순서**: 초록→하양→빨강→하양 repeat.
- **AA**: 흰/grn 5.12·grn텍스트(인스타버튼)/흰bg 5.12·red/흰 5.44·ink/bg 15.93. 전부 ≥4.5.

## v0.5 (2026-09-06) 파란색 채도 상향 + 삼색 스트라이프 + 히어로 재편
- **파란색 채도 ↑**: sky #5A7385(뮤트 스틸블루)→**#3C6E94**(sky-d #2F5878). 흰글씨 대비 5.45·흰bg 위 텍스트 대비 5.45(전부 AA).
- **어닝 스트라이프 3색 교차**: 빨강/크림 2색→**빨강·하양·파랑**(red→#fff→sky→#fff repeat).
- **히어로 최대 글씨=Tim Focaccia**: 기존 "Handmade focaccia & baguette"(대형)→**Tim / Focaccia**(em 레드). 아이브로 "Salumeria · Paninoteca 수제 샌드위치 전문" 삭제 → 그 자리에 **"Handmade focaccia & baguette."**.
- **히어로 인스타 버튼=파란 글자+테두리**(`.btn-ol-sky`, 기존 레드 아웃라인 btn-ol에서 분리).
- **카피 교체**: lead에서 "a little taste of Italy…" 지역 문구 제거 / about 영문·한글 em대시→쉼표, 한글 "샤퀴테리"→"프로마쥬"·"기본에 충실한"→"풍성한" / 위치 "두 곳에서 만나요"→"두 곳에 매장이 있습니다".

## v0.4 (2026-09-06) 얇은 제목 + 순백 배경 + 하늘색 포인트
- **디스플레이 폰트 Anton→Oswald**(다올: 제목 너무 굵음): Anton은 단일 볼드라 얇게 불가 → 콘덴스드 가변폰트 Oswald로 교체, 제목 weight 400→**300**(얇은 포스터체). uppercase·한글 폴백(Pretendard) 동일.
- **배경 순백(#FFFFFF)**: 크림 bg#F6EEDB→순백. bg2#F6F6F4·card#FFFFFF·cream(스트라이프)#F3F3F1 중성화.
- **포인트 올리브→뮤트 하늘색**: --sky#5A7385(채도 낮은 스틸블루, 쨍하지 않게)·sky-d#46596A. olive 토큰·`.stripe.olive`→`.stripe.sky` 전면 개명. 메인 CTA=토마토 레드 유지.
- **명절 휴무 제거**: 익선점 "· 명절(추석 9/25) 휴무" 삭제 → "Last order 18:30"만.
- **AA**: ink/bg 15.93·ink2 6.4·red/bg 5.44(eyebrow·em·링크)·흰/red 5.44·흰/sky 4.97·흰/sky-d 7.25. 전부 ≥4.5.

## v0.3 (2026-09-06) 살루메리아 델리 리스킨 — 이탈리아 감성 최대
- **방향 전환**: v0.2 순백 미니멀 "답 아님"(다올) → 상담 후 **살루메리아 델리** 채택. 이탈리아 동네 정육·샌드위치 가게 감성.
- **폰트**: 디스플레이=**Anton**(초압축 볼드 포스터체, `text-transform:uppercase`·weight무시), 스크립트=**Caveat**(손글씨 액센트), 본문/한글=Pretendard. Bricolage·Inter 제거.
- **팔레트**: 크림 bg#F6EEDB·bg2#EFE3C9·card#FFFDF6 + **토마토 red#C0392B**(red-d#A32E22)·**올리브 olive#5F6B33**(olive-d#4C5628)·모르타델라 **pink#E5A9A9**. v0.2 순백/그레이 폐기.
- **모티프**: 레드/크림 어닝 스트라이프(`.stripe`)+올리브 변형(`.stripe.olive`). 이탈리아어 아이브로(Salumeria · Paninoteca / La nostra storia / Fatto in casa / Il locale / Dove siamo), 스크립트 액센트(hero "fatto a mano ~ every morning"·뱃지 "Fatto a mano"·푸터 "Buon appetito!").
- **버튼/포인트 색 이동**: 구 sky 계열 전부 **올리브**로(loc-name·foot-link hover·보조버튼). 메인 CTA=토마토 레드.
- **구성 유지**(v0.2와 동일, Menu 제외): Header→Hero→red/cream 스트라이프→About(#about tim-ham)→올리브 Band(tim-bread-tim)→Space(#space 갤러리9)→Location(혜화·익선)→다크푸터+퀵바. nav=About/Space/Location.
- **AA**: ink/bg 13.78·ink2 5.54·red/bg 4.71(eyebrow·em)·red-d 6.12(링크)·흰/red 5.44·흰/olive 5.77·olive-d 6.81. 전부 ≥4.5 통과.
- ⚠️미결(승계): 배포 보류(다올: 나중에 한꺼번에 수정 후)·폰트 self-host(납품)·메뉴 가격·영업 시작시간·혜화 별도 IG.

## v0.2 (2026-09-06) 순백 미니멀 + Pretendard + 메뉴 임시제거
- **배경 순백(#FFFFFF)**: 주황베이지 팔레트 제거→화이트+뉴트럴그레이(#F5F5F4), ink 중성(#232020). 레드·스카이 액센트는 유지(어닝 스트라이프·밴드·버튼).
- **폰트 전부 Pretendard**(다올: 일단 Pretendard로, 이후 재검토): Bricolage Grotesque·Inter 링크 제거, --disp/--sans/--kr 모두 Pretendard.
- **메뉴 섹션 임시 제거**(나중에 재검토): #menu 섹션·nav/footer Menu 링크·hero "See the Menu" CTA 삭제. 히어로 CTA=Find us + Instagram. 메뉴 전용 사진(sand-1/2/4/5/6·soup·jambong)은 미사용→`.assetsignore` 제외(메뉴 복귀 시 해제).
- **소개 사진 교체**: tim-jambong → tim-ham(신선한 햄·재료). 미니멀 방향.


## v0.1 (2026-09-06) 최초 빌드 — 이탈리안 샌드위치 · 2지점
- **업종/컨셉**: 서울 혜화·익선 수제 포카치아·바게트 샌드위치 전문점. 톤=**이탈리안 델리·따뜻·영어 위주**. 주황빛 베이지 배경 + 고기빛 레드 + 하늘색 포인트 + 화이트.
- **폰트**: 디스플레이=**Bricolage Grotesque**(다올 지정 protipo[Latinotype 따뜻한 그로테스크]의 무료 대체), UI/본문=Inter, 한글=Pretendard. CDN(납품 self-host).
- **색**: bg 주황베이지 #FAF3E3·bg2 #F2E6CD·cream #FBF6EA·ink #33271C·**red #B8443A(고기빛)**·red-d #9C382F(AA)·**sky #6FA8CC(연한 하늘·awning stripe)**·sky-d #3C7BA2(흰글씨 버튼/뱃지 AA). 어닝 스트라이프 모티프(.stripe).
- **구성**: 헤더(Tim Focaccia 워드마크·o 레드) → 히어로(대형 샌드위치+헤드라인 "Handmade focaccia & baguette"+CTA) → 어닝 스트라이프 → About(수제 빵 스토리) → Menu(샌드위치 쇼케이스 6카드·가격은 매장/IG 안내) → 레드 밴드("Made by hand, every morning"+TIM 각인빵) → Space(12칼럼 갤러리 9컷) → Location(혜화·익선 2지점) → 다크 푸터 + 모바일 퀵바(혜화·익선 지도).
- **실데이터**: 혜화=서울 종로구 대학로11길 18 1층(혜화역 4번출구 189m·소나무길 중간)·L.O.20:30·0507-1491-0837·place **1041424953**. 익선=서울 종로구 돈화문로 81-1 1층(종로3가역 3번출구 374m)·L.O.18:30·02-765-1070·place **2070009857**·추석(9/25) 휴무. IG @timfocacciaiksun(2지점 공용). ⚠️영업 시작시간·메뉴 가격 미확보→L.O.만 표기·가격은 "매장/IG 안내".
- **이미지**: 제공 50중 22 webp(2.7MB, tim-*). 미사용 5컷(cauliflower·ham·logo-draw·sand-3·sketch) `.assetsignore` 제외. favicon/apple(레드+T)·og(히어로+텍스트 밴드).
- **마감/안전**: color-scheme·text-size-adjust·overflow-x·keep-all, 고정바 `<div>`, 리빌 html.js 게이팅+데스크톱전용+2.2s폴백, noscript, 앵커 rAF, reduced-motion 리빌 강제(하우스룰), a11y(aria·focus-visible·alt), JSON-LD Restaurant+department 2지점. 폼 없음.
- **AA**: ink/bg 13.1·ink2 5.7·red 4.84(eyebrow)·red-d 6.29(버튼·링크)·흰/red 5.35·흰/sky-d 4.62(하늘버튼·뱃지). 연한 sky는 무텍스트 스트라이프에만.
- **도메인**: og·canonical·JSON-LD = timfocaccia-sample.lgt3232.workers.dev. 인계 시 치환.
- ⚠️미결: GitHub 업로드(`.assetsignore` 정확명·라이브 404)+CF, 라이브 육안검증(폰트·스트라이프·모바일), 폰트 self-host(납품), 메뉴 가격·영업 시작시간 확보 시 반영, 혜화 별도 IG 유무 확인.
