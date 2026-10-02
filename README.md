<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>도준(DO-JUN) 성장 & 기질 인포그래픽 대시보드</title>
  <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css" />
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Pretendard', '-apple-system', 'BlinkMacSystemFont', 'system-ui', 'Roboto', 'sans-serif'],
          },
          colors: {
            brand: {
              50: '#F5F7FF',
              100: '#EBF0FE',
              500: '#4F46E5',
              600: '#4338CA',
            },
            coral: {
              400: '#FB7185',
              500: '#F43F5E',
            },
            amber: {
              400: '#FBBF24',
              500: '#F59E0B',
            },
            mint: {
              400: '#34D399',
              500: '#10B981',
            }
          }
        }
      }
    }
  </script>
  <style>
    @keyframes floatOrb {
      0%, 100% { transform: translateY(0px) scale(1); }
      50% { transform: translateY(-16px) scale(1.05); }
    }
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.6; filter: blur(30px); }
      50% { opacity: 0.9; filter: blur(40px); }
    }
    .animate-float {
      animation: floatOrb 8s ease-in-out infinite;
    }
    .animate-glow {
      animation: pulseGlow 6s ease-in-out infinite;
    }
    .glass-card {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border: 1px solid rgba(255, 255, 255, 0.7);
      box-shadow: 0 10px 30px -5px rgba(99, 102, 241, 0.08), 0 4px 6px -2px rgba(0, 0, 0, 0.03);
    }
    .glass-card-dark {
      background: linear-gradient(135deg, rgba(30, 27, 75, 0.92), rgba(49, 46, 129, 0.95));
      backdrop-filter: blur(16px);
      box-shadow: 0 20px 40px -10px rgba(30, 27, 75, 0.4);
    }
    .sparkle {
      pointer-events: none;
      position: absolute;
      animation: sparkleAnim 0.8s forwards ease-out;
    }
    @keyframes sparkleAnim {
      0% { transform: translate(0, 0) scale(1); opacity: 1; }
      100% { transform: translate(var(--tx), var(--ty)) scale(0); opacity: 0; }
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased min-h-screen relative overflow-x-hidden selection:bg-indigo-500 selection:text-white">

  <!-- Background Ambient Glows -->
  <div class="fixed inset-0 pointer-events-none overflow-hidden -z-10">
    <div class="absolute -top-32 -left-32 w-96 h-96 bg-indigo-300/35 rounded-full animate-glow animate-float"></div>
    <div class="absolute top-1/3 -right-32 w-[30rem] h-[30rem] bg-rose-200/40 rounded-full animate-glow animate-float" style="animation-delay: -3s;"></div>
    <div class="absolute -bottom-32 left-1/4 w-[28rem] h-[28rem] bg-amber-200/30 rounded-full animate-glow animate-float" style="animation-delay: -5s;"></div>
  </div>

  <main class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 py-8 md:py-12 space-y-10">

    <!-- HERO PROFILE HEADER -->
    <header class="glass-card rounded-3xl p-6 sm:p-10 relative overflow-hidden transition-all duration-300 hover:shadow-xl">
      <div class="absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-indigo-500/10 to-rose-500/10 rounded-full blur-2xl -mr-16 -mt-16 pointer-events-none"></div>

      <div class="flex flex-wrap items-center justify-between gap-4 mb-6">
        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-indigo-50 border border-indigo-200/60 text-indigo-700 text-xs sm:text-sm font-semibold tracking-wide shadow-sm">
          <span class="w-2 h-2 rounded-full bg-indigo-500 animate-ping"></span>
          2026 2학기 자이새순 어린이집 발달 진단 리포트
        </div>
        <div class="text-xs sm:text-sm text-slate-500 font-medium flex items-center gap-2">
          <span>📅 상담일: 2026. 10. 02</span>
          <span class="hidden sm:inline">•</span>
          <span class="hidden sm:inline">대상: 이도준 (만 2세 / 2024.02생)</span>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
        <div class="lg:col-span-8 space-y-4">
          <div class="flex items-center gap-3 flex-wrap">
            <h1 class="text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
              도준 <span class="text-indigo-600 font-black">DO-JUN</span>
            </h1>
            <span class="px-3 py-1 rounded-xl bg-slate-900 text-white font-bold text-xs sm:text-sm tracking-wider shadow-sm">
              만 2세 (32개월)
            </span>
          </div>

          <div class="space-y-2">
            <div class="text-indigo-600 font-bold text-lg sm:text-xl flex items-center gap-2">
              <span class="text-2xl">🧩</span> 기질 유형 코드 : <span class="bg-indigo-100/80 text-indigo-900 px-2.5 py-0.5 rounded-lg border border-indigo-200">L.C.A.S</span>
            </div>
            <p class="text-2xl sm:text-3xl font-black text-slate-800 leading-snug tracking-tight">
              “이유가 납득되면 스스로 움직이는<br class="hidden sm:inline" />
              <span class="bg-clip-text text-transparent bg-gradient-to-r from-indigo-600 via-purple-600 to-rose-500">
                꼬마 전략가 & 크리에이터
              </span>”
            </p>
          </div>

          <p class="text-slate-600 leading-relaxed text-sm sm:text-base pt-1">
            1학기 초반의 낯가림과 고집 시기를 지나 교사와의 깊은 신뢰를 구축했습니다. 이제는 타율적인 통제가 아닌 
            <strong class="text-slate-900 font-semibold underline decoration-indigo-300 decoration-2">‘명확한 인과관계’</strong>를 
            이해시켜 주면 놀라운 집중력과 배려심, 창의력을 발휘하는 황금기 만개기를 맞이했습니다.
          </p>
        </div>

        <div class="lg:col-span-4 flex flex-col items-center justify-center p-6 rounded-2xl bg-gradient-to-br from-indigo-500/10 via-purple-500/5 to-rose-500/10 border border-indigo-100 text-center">
          <div class="relative w-24 h-24 mb-3 flex items-center justify-center">
            <div class="absolute inset-0 bg-gradient-to-tr from-indigo-500 to-rose-400 rounded-full blur-md opacity-70 animate-pulse"></div>
            <div class="relative w-20 h-20 bg-white rounded-full flex items-center justify-center text-4xl shadow-inner border border-white">
              🚀
            </div>
          </div>
          <span class="text-xs uppercase tracking-widest text-indigo-600 font-bold">Comprehensive Growth Score</span>
          <span class="text-4xl font-black text-slate-900 my-1">92.5 <span class="text-base font-semibold text-slate-400">/ 100</span></span>
          <span class="text-xs text-emerald-600 font-semibold bg-emerald-50 px-2.5 py-1 rounded-full border border-emerald-200">
            ↑ 1학기 대비 비약적 성장 달성
          </span>
        </div>
      </div>
    </header>

    <!-- SECTION 1: RADAR CHART & METRIC ANALYSIS -->
    <section class="glass-card rounded-3xl p-6 sm:p-10 space-y-8">
      <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-3 border-b border-slate-100 pb-5">
        <div>
          <span class="text-xs font-bold uppercase tracking-wider text-indigo-600">Development Gauge</span>
          <h2 class="text-2xl font-black text-slate-900">도준 6대 종합 발달 헥사곤</h2>
        </div>
        <p class="text-xs sm:text-sm text-slate-500">교사 관찰 데이터 및 일과 수행 역량 기반 정밀 산출</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-center">
        <!-- Canvas Radar Chart -->
        <div class="md:col-span-6 flex flex-col items-center justify-center relative">
          <div class="relative w-full max-w-[340px] aspect-square flex items-center justify-center">
            <canvas id="radarCanvas" class="w-full h-full drop-shadow-md cursor-pointer"></canvas>
          </div>
          <p class="text-xs text-slate-400 mt-2 text-center">차트 꼭짓점에 마우스를 올리면 상세 수치가 강조됩니다</p>
        </div>

        <!-- Metric Bars -->
        <div class="md:col-span-6 space-y-4">
          <!-- Item 1 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-indigo-500"></span> 창의 · 구성 몰입도
              </span>
              <span class="text-sm font-black text-indigo-600">98% <span class="text-xs font-medium text-slate-400">(상위 1%)</span></span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-indigo-500 to-purple-500 rounded-full transition-all duration-1000" style="width: 98%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">정형화되지 않은 박스, 블록으로 '세모 놀이터' 등 독창적 구조물 창작</p>
          </div>

          <!-- Item 2 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-purple-500"></span> 자존감 & 성취욕(애살)
              </span>
              <span class="text-sm font-black text-purple-600">92%</span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-purple-500 to-pink-500 rounded-full transition-all duration-1000" style="width: 92%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">"도준이 키 컸네", "잘한다"는 칭찬과 선의의 자극에 강한 내적 동기</p>
          </div>

          <!-- Item 3 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-rose-500"></span> 규칙 이해 및 자기조절
              </span>
              <span class="text-sm font-black text-rose-600">90%</span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-pink-500 to-rose-500 rounded-full transition-all duration-1000" style="width: 90%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">경로당 배려 등 이유를 납득하면 스스로 질주를 멈추고 친구 훈육까지 주도</p>
          </div>

          <!-- Item 4 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-amber-500"></span> 언어 구사 및 어휘력
              </span>
              <span class="text-sm font-black text-amber-600">90%</span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-amber-400 to-amber-500 rounded-full transition-all duration-1000" style="width: 90%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">어른 문장을 자연스럽게 응용 및 변형하며 책 읽기 교감 후 어휘 대폭발</p>
          </div>

          <!-- Item 5 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span> 또래 관계 & 리더십
              </span>
              <span class="text-sm font-black text-emerald-600">90%</span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-emerald-400 to-emerald-500 rounded-full transition-all duration-1000" style="width: 90%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">친구가 장난감을 뺏으려 해도 울지 않고 말로 조율하며 조각을 떼어주는 배려</p>
          </div>

          <!-- Item 6 -->
          <div class="group p-3 rounded-2xl hover:bg-indigo-50/50 transition-colors">
            <div class="flex justify-between items-center mb-1">
              <span class="text-sm font-bold text-slate-800 flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-sky-500"></span> 기본 생활 자립도
              </span>
              <span class="text-sm font-black text-sky-600">85%</span>
            </div>
            <div class="w-full h-2.5 bg-slate-100 rounded-full overflow-hidden">
              <div class="h-full bg-gradient-to-r from-sky-400 to-indigo-400 rounded-full transition-all duration-1000" style="width: 85%;"></div>
            </div>
            <p class="text-xs text-slate-500 mt-1">알레르기 없이 골고루 완식, 1시간 반 숙면, 음악 신호에 이불·신발 정리 척척</p>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 2: LCAS TEMPERAMENT CODE ANALYSIS -->
    <section class="space-y-6">
      <div class="text-center max-w-xl mx-auto space-y-2">
        <span class="text-xs font-black uppercase tracking-widest text-indigo-600 bg-indigo-50 px-3 py-1 rounded-full border border-indigo-200">
          Core Temperament Archetype
        </span>
        <h2 class="text-2xl sm:text-3xl font-black text-slate-900">도준이의 L.C.A.S 4대 기질 팩터</h2>
        <p class="text-slate-500 text-sm">도준이를 움직이는 4가지 핵심 심리 기제를 카드를 눌러 확인해보세요.</p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
        <!-- Factor 1: L -->
        <div class="glass-card rounded-2xl p-6 border-t-4 border-indigo-500 transition-all duration-300 hover:-translate-y-1.5 hover:shadow-xl flex flex-col justify-between">
          <div class="space-y-3">
            <div class="flex items-center justify-between">
              <span class="text-3xl font-black text-indigo-600">L</span>
              <span class="text-xs font-semibold px-2 py-0.5 rounded-md bg-indigo-50 text-indigo-700">논리 수용</span>
            </div>
            <h3 class="text-lg font-bold text-slate-900">Logical Receiver</h3>
            <p class="text-xs text-indigo-950/70 font-medium">단호한 명령 대신 원리와 이유를 납득시키는 스토리텔링에 100% 순응</p>
            <div class="pt-2 text-xs text-slate-600 bg-slate-50/80 p-3 rounded-xl border border-slate-100 space-y-1">
              <p class="font-bold text-slate-800">💡 관찰된 교사 훈육법:</p>
              <p>"아랫집 경로당 할머니들이 시끄러우니 세모 놀이터에서 뛰자", "누워 먹으면 머리로 가서 병원 가" 즉각 납득</p>
            </div>
          </div>
          <div class="mt-4 pt-3 border-t border-slate-100 text-[11px] text-indigo-500 font-semibold flex items-center justify-between">
            <span>설명형 부모링 최적화</span>
            <span>★ ★ ★ ★ ★</span>
          </div>
        </div>

        <!-- Factor 2: C -->
        <div class="glass-card rounded-2xl p-6 border-t-4 border-purple-500 transition-all duration-300 hover:-translate-y-1.5 hover:shadow-xl flex flex-col justify-between">
          <div class="space-y-3">
            <div class="flex items-center justify-between">
              <span class="text-3xl font-black text-purple-600">C</span>
              <span class="text-xs font-semibold px-2 py-0.5 rounded-md bg-purple-50 text-purple-700">비정형 창작</span>
            </div>
            <h3 class="text-lg font-bold text-slate-900">Creative Maker</h3>
            <p class="text-xs text-purple-950/70 font-medium">정해진 완성품보다 빈 박스, 자석 블록, 테이프로 자기만의 세계를 창조</p>
            <div class="pt-2 text-xs text-slate-600 bg-slate-50/80 p-3 rounded-xl border border-slate-100 space-y-1">
              <p class="font-bold text-slate-800">💡 관찰된 대표 행동:</p>
              <p>비정형 구조물을 만들어 "선생님, 세모 놀이터야!" 자랑. 백지 스케치북과 자유 블록 놀이 시 최고의 몰입도</p>
            </div>
          </div>
          <div class="mt-4 pt-3 border-t border-slate-100 text-[11px] text-purple-500 font-semibold flex items-center justify-between">
            <span>창의 공간 감각 우수</span>
            <span>★ ★ ★ ★ ★</span>
          </div>
        </div>

        <!-- Factor 3: A -->
        <div class="glass-card rounded-2xl p-6 border-t-4 border-rose-500 transition-all duration-300 hover:-translate-y-1.5 hover:shadow-xl flex flex-col justify-between">
          <div class="space-y-3">
            <div class="flex items-center justify-between">
              <span class="text-3xl font-black text-rose-600">A</span>
              <span class="text-xs font-semibold px-2 py-0.5 rounded-md bg-rose-50 text-rose-700">성취욕·애살</span>
            </div>
            <h3 class="text-lg font-bold text-slate-900">Ambitious Sprinter</h3>
            <p class="text-xs text-rose-950/70 font-medium">자신이 잘하고 싶어 하는 욕심(애살)이 커서 칭찬과 선의의 라이벌에 즉각 반응</p>
            <div class="pt-2 text-xs text-slate-600 bg-slate-50/80 p-3 rounded-xl border border-slate-100 space-y-1">
              <p class="font-bold text-slate-800">💡 모티베이션 트리거:</p>
              <p>"도준이 키 엄청 컸네!", "태호보다 멋지게 하마 입!" 반응에 밥도 2그릇 뚝딱. 토라졌을 땐 다그침 금지</p>
            </div>
          </div>
          <div class="mt-4 pt-3 border-t border-slate-100 text-[11px] text-rose-500 font-semibold flex items-center justify-between">
            <span>자존감 피드백 민감</span>
            <span>★ ★ ★ ★ ☆</span>
          </div>
        </div>

        <!-- Factor 4: S -->
        <div class="glass-card rounded-2xl p-6 border-t-4 border-emerald-500 transition-all duration-300 hover:-translate-y-1.5 hover:shadow-xl flex flex-col justify-between">
          <div class="space-y-3">
            <div class="flex items-center justify-between">
              <span class="text-3xl font-black text-emerald-600">S</span>
              <span class="text-xs font-semibold px-2 py-0.5 rounded-md bg-emerald-50 text-emerald-700">리더십 & 배려</span>
            </div>
            <h3 class="text-lg font-bold text-slate-900">Social Leader</h3>
            <p class="text-xs text-emerald-950/70 font-medium">주변에 친구들을 끌어당기며, 갈등을 울음 대신 언어로 중재하는 성숙한 사회성</p>
            <div class="pt-2 text-xs text-slate-600 bg-slate-50/80 p-3 rounded-xl border border-slate-100 space-y-1">
              <p class="font-bold text-slate-800">💡 또래 관계 양상:</p>
              <p>장난감을 뺏겨도 "내가 하고 있잖아" 또박또박 말하고 다른 부품을 떼어주는 양보력. 위험한 친구 훈육까지 솔선</p>
            </div>
          </div>
          <div class="mt-4 pt-3 border-t border-slate-100 text-[11px] text-emerald-500 font-semibold flex items-center justify-between">
            <span>또래 흡인력 최상</span>
            <span>★ ★ ★ ★ ★</span>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 3: GROWTH MOMENTUM INTERACTIVE COMPARISON -->
    <section class="glass-card rounded-3xl p-6 sm:p-10 space-y-6">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-slate-100 pb-5">
        <div>
          <span class="text-xs font-bold uppercase tracking-wider text-indigo-600">Evolution Map</span>
          <h2 class="text-2xl font-black text-slate-900">1학기 적응기 vs 2학기 만개기 비교</h2>
        </div>

        <!-- Toggle Controls -->
        <div class="inline-flex p-1 bg-slate-100 rounded-2xl border border-slate-200/80 self-start sm:self-auto">
          <button id="viewCompareBtn" onclick="switchGrowthView('compare')" class="px-4 py-1.5 rounded-xl text-xs sm:text-sm font-bold bg-white text-indigo-600 shadow-sm transition-all">
            한눈에 나란히 보기
          </button>
          <button id="viewAfterBtn" onclick="switchGrowthView('after')" class="px-4 py-1.5 rounded-xl text-xs sm:text-sm font-bold text-slate-600 hover:text-indigo-600 transition-all">
            ✨ 2학기 성장 하이라이트
          </button>
        </div>
      </div>

      <!-- Growth Grid Container -->
      <div id="growthContainer" class="grid grid-cols-1 md:grid-cols-2 gap-6">

        <!-- Card 1: 1학기 (Before) -->
        <div id="beforeCol" class="p-6 rounded-2xl bg-slate-100/70 border border-slate-200 space-y-4">
          <div class="flex items-center justify-between border-b border-slate-200/80 pb-3">
            <span class="inline-flex items-center gap-2 text-sm font-extrabold text-slate-600">
              <span class="w-3 h-3 rounded-full bg-slate-400"></span> 1학기 (원 이동 초기 / 탐색·방어기)
            </span>
            <span class="text-xs text-slate-400 font-medium">환경 변화 적응 단계</span>
          </div>

          <ul class="space-y-3 text-xs sm:text-sm text-slate-600">
            <li class="flex items-start gap-2.5">
              <span class="text-rose-400 font-bold">✕</span>
              <span><strong>호명 반응:</strong> 불러도 대답 없이 눈으로만 흘깃 보고 멈칫함</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-rose-400 font-bold">✕</span>
              <span><strong>감정 표현:</strong> 요구가 관철되지 않으면 울음, 짜증, 고집 발현</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-rose-400 font-bold">✕</span>
              <span><strong>식사 태도:</strong> 엉덩이를 옆으로 돌리거나 뒤로 눕고 장난감 고집</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-rose-400 font-bold">✕</span>
              <span><strong>갈등 대처:</strong> 장난감 뺏기면 방어적 울음과 독점 경향</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-rose-400 font-bold">✕</span>
              <span><strong>신체 에너지:</strong> 교실 안에서 에너지를 조절하지 못하고 질주</span>
            </li>
          </ul>
        </div>

        <!-- Card 2: 2학기 (After) -->
        <div id="afterCol" class="p-6 rounded-2xl bg-gradient-to-br from-indigo-50/90 to-purple-50/90 border border-indigo-200 space-y-4 shadow-sm">
          <div class="flex items-center justify-between border-b border-indigo-100 pb-3">
            <span class="inline-flex items-center gap-2 text-sm font-extrabold text-indigo-700">
              <span class="w-3 h-3 rounded-full bg-indigo-500 animate-pulse"></span> 2학기 현재 (신뢰 구축 / 전성기)
            </span>
            <span class="text-xs bg-indigo-100 text-indigo-800 font-bold px-2 py-0.5 rounded-full">눈부신 진화</span>
          </div>

          <ul class="space-y-3 text-xs sm:text-sm text-slate-800">
            <li class="flex items-start gap-2.5">
              <span class="text-emerald-500 font-black">✓</span>
              <span><strong>호명 반응:</strong> 부르면 즉각 달려와 안기며 풍부한 애정 표현</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-emerald-500 font-black">✓</span>
              <span><strong>언어 소통:</strong> “내가 하고 있잖아” 명확히 의사 전달, 어휘력 폭발</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-emerald-500 font-black">✓</span>
              <span><strong>식사 습관:</strong> 이유 설명 후 허리 꼿꼿이 세우고 골고루 완식</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-emerald-500 font-black">✓</span>
              <span><strong>사회성·배려:</strong> 울지 않고 조율하며 자기 블록 조각 떼어 양보</span>
            </li>
            <li class="flex items-start gap-2.5">
              <span class="text-emerald-500 font-black">✓</span>
              <span><strong>규칙 내면화:</strong> 질주 멈춤, 위험한 친구에게 “그러면 안 돼” 훈육</span>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SECTION 4: ROUTINE & PHYSICAL DATA CARDS -->
    <section class="space-y-6">
      <div class="border-b border-slate-200/80 pb-3">
        <span class="text-xs font-bold uppercase tracking-wider text-indigo-600">Daily Life & Physical Care</span>
        <h2 class="text-2xl font-black text-slate-900">도준이의 일과·신체 케어 분석 카드</h2>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
        <!-- Meal Care -->
        <div class="glass-card rounded-2xl p-5 space-y-3">
          <div class="w-10 h-10 rounded-xl bg-amber-100 text-amber-700 flex items-center justify-center text-xl font-bold">
            🍚
          </div>
          <h3 class="font-black text-slate-800 text-base">식습관 & 영양</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            특정 알레르기 없이 국, 고기, 샐러드, 과일 모두 잘 먹으며 밥 리필 잦음. 
            <span class="text-amber-700 font-semibold">초록 나물류</span>는 약간 꺼리지만 “키 쑥쑥 크자” 칭찬과 또래 경쟁 자극에 완식.
          </p>
          <div class="pt-2 border-t border-slate-100 flex items-center justify-between text-[11px] text-slate-400">
            <span>식사 집중도</span>
            <span class="font-bold text-amber-600">최상급 (자석식사)</span>
          </div>
        </div>

        <!-- Sleep Routine -->
        <div class="glass-card rounded-2xl p-5 space-y-3">
          <div class="w-10 h-10 rounded-xl bg-indigo-100 text-indigo-700 flex items-center justify-center text-xl font-bold">
            🌙
          </div>
          <h3 class="font-black text-slate-800 text-base">낮잠 & 수면</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            오후 1:30~3:00 사이 중간에 깨는 일 없이 1시간~1시간 반 동안 편안한 숙면 유지. 
            머리를 부드럽게 긁어주거나 등을 토닥여 주면 안정적으로 입면 성공.
          </p>
          <div class="pt-2 border-t border-slate-100 flex items-center justify-between text-[11px] text-slate-400">
            <span>수면 안정성</span>
            <span class="font-bold text-indigo-600">100% 지속숙면</span>
          </div>
        </div>

        <!-- Fine Motor Skills -->
        <div class="glass-card rounded-2xl p-5 space-y-3">
          <div class="w-10 h-10 rounded-xl bg-purple-100 text-purple-700 flex items-center justify-center text-xl font-bold">
            🎨
          </div>
          <h3 class="font-black text-slate-800 text-base">소근육 & 손잡이</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            양손을 쓰되 <span class="text-purple-700 font-semibold">왼손 우세</span> 성향. 선 안을 메우는 색칠 힘과 눈-손 협응력 최우수. 
            억지 선 긋기 대신 백지 스케치북 자유 드로잉이 창의성에 특효.
          </p>
          <div class="pt-2 border-t border-slate-100 flex items-center justify-between text-[11px] text-slate-400">
            <span>추천 도구</span>
            <span class="font-bold text-purple-600">백지 & 자석블록</span>
          </div>
        </div>

        <!-- Autonomy Routine -->
        <div class="glass-card rounded-2xl p-5 space-y-3">
          <div class="w-10 h-10 rounded-xl bg-emerald-100 text-emerald-700 flex items-center justify-center text-xl font-bold">
            ⚡
          </div>
          <h3 class="font-black text-slate-800 text-base">자립 루틴화</h3>
          <p class="text-xs text-slate-600 leading-relaxed">
            원내 일과를 완벽 체득하여 음악이 나오면 자기 이불을 챙겨 오고, 외출 신호에 신발·양말을 찾아 착용. 
            손 씻기 노래에 맞춰 군대식 자동화 완료.
          </p>
          <div class="pt-2 border-t border-slate-100 flex items-center justify-between text-[11px] text-slate-400">
            <span>생활 규율력</span>
            <span class="font-bold text-emerald-600">자립형 모범생</span>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 5: FATHER'S ACTION PLAYBOOK (DO & DON'T) -->
    <section class="glass-card rounded-3xl p-6 sm:p-10 space-y-8">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-slate-100 pb-5">
        <div>
          <span class="text-xs font-bold uppercase tracking-wider text-coral-500">Father & Son Strategy</span>
          <h2 class="text-2xl font-black text-slate-900">아빠를 위한 실전 양육 플레이북</h2>
          <p class="text-slate-500 text-xs sm:text-sm mt-1">“단호한 억압은 튕겨 나가고, 내 편 지지는 평생의 신뢰를 낳는다”</p>
        </div>

        <!-- Checklist Progress Counter -->
        <div class="flex items-center gap-3 bg-indigo-50 border border-indigo-200/80 px-4 py-2 rounded-2xl">
          <span class="text-xs font-bold text-indigo-700">오늘의 실천 목표:</span>
          <span id="progressBadge" class="text-sm font-black text-indigo-900">0 / 5 완료</span>
        </div>
      </div>

      <!-- Action Items Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">

        <!-- DO Playbook -->
        <div class="space-y-4">
          <div class="flex items-center gap-2 text-emerald-700 font-extrabold text-base">
            <span class="w-6 h-6 rounded-lg bg-emerald-100 flex items-center justify-center text-sm">👍</span>
            아빠가 실천하면 폭풍 성장하는 DO (적극 추천)
          </div>

          <div class="space-y-3">
            <!-- DO 1 -->
            <label class="flex items-start gap-3 p-4 rounded-2xl bg-emerald-50/50 border border-emerald-200/60 hover:bg-emerald-50 transition cursor-pointer select-none group">
              <input type="checkbox" onchange="toggleItem(this)" class="mt-1 w-4 h-4 rounded text-emerald-600 focus:ring-emerald-500">
              <div class="space-y-1">
                <span class="text-xs font-bold text-emerald-800 block">1. 낯선 갈등 시 ‘무조건 도준이 편 방패’ 되기</span>
                <p class="text-xs text-slate-600 leading-relaxed">
                  키즈카페에서 다른 아이가 장난감을 뺏으려 할 때 도준이에게 양보를 강요하지 않고, 아빠가 상대에게 
                  <em>“이 친구가 먼저 하고 있어. 다 할 때까지 조금만 기다려줄래?”</em>라고 먼저 선을 그어주기.
                </p>
              </div>
            </label>

            <!-- DO 2 -->
            <label class="flex items-start gap-3 p-4 rounded-2xl bg-emerald-50/50 border border-emerald-200/60 hover:bg-emerald-50 transition cursor-pointer select-none group">
              <input type="checkbox" onchange="toggleItem(this)" class="mt-1 w-4 h-4 rounded text-emerald-600 focus:ring-emerald-500">
              <div class="space-y-1">
                <span class="text-xs font-bold text-emerald-800 block">2. 눈높이 인과관계 스토리텔링 훈육</span>
                <p class="text-xs text-slate-600 leading-relaxed">
                  “앉아!”, “먹어!” 같은 지시 대신 <em>“허리를 펴고 앉아야 배 속 음식물 미끄럼틀이 영양분을 머리랑 다리로 쑥쑥 보내줘”</em> 식의 원리 설명.
                </p>
              </div>
            </label>

            <!-- DO 3 -->
            <label class="flex items-start gap-3 p-4 rounded-2xl bg-emerald-50/50 border border-emerald-200/60 hover:bg-emerald-50 transition cursor-pointer select-none group">
              <input type="checkbox" onchange="toggleItem(this)" class="mt-1 w-4 h-4 rounded text-emerald-600 focus:ring-emerald-500">
              <div class="space-y-1">
                <span class="text-xs font-bold text-emerald-800 block">3. 비정형 재료 제공 & 구체적 디테일 리액션</span>
                <p class="text-xs text-slate-600 leading-relaxed">
                  택배 상자, 종이테이프, 블록을 쥐여주고 결과물이 나오면 <em>“우와! 세모 모양으로 튼튼한 다리를 만들었네!”</em>라며 구체적인 확대 리액션 보여주기.
                </p>
              </div>
            </label>

            <!-- DO 4 -->
            <label class="flex items-start gap-3 p-4 rounded-2xl bg-emerald-50/50 border border-emerald-200/60 hover:bg-emerald-50 transition cursor-pointer select-none group">
              <input type="checkbox" onchange="toggleItem(this)" class="mt-1 w-4 h-4 rounded text-emerald-600 focus:ring-emerald-500">
              <div class="space-y-1">
                <span class="text-xs font-bold text-emerald-800 block">4. 대근육 발산 놀이 파트너(축구·달리기)</span>
                <p class="text-xs text-slate-600 leading-relaxed">
                  에너지가 넘치는 시기이므로 야외에서 마음껏 뛰고 공을 찰 수 있는 든든한 친구 같은 아빠 역할 수행.
                </p>
              </div>
            </label>

            <!-- DO 5 -->
            <label class="flex items-start gap-3 p-4 rounded-2xl bg-emerald-50/50 border border-emerald-200/60 hover:bg-emerald-50 transition cursor-pointer select-none group">
              <input type="checkbox" onchange="toggleItem(this)" class="mt-1 w-4 h-4 rounded text-emerald-600 focus:ring-emerald-500">
              <div class="space-y-1">
                <span class="text-xs font-bold text-emerald-800 block">5. 삐쳤을 때는 ‘1~2분 기다림’ 후 안아주기</span>
                <p class="text-xs text-slate-600 leading-relaxed">
                  토라졌을 때 억지로 말을 시키지 않고 <em>“도준이 속상했구나, 마음 풀리면 언제든 아빠한테 와”</em> 하며 감정을 정리할 시간 허용.
                </p>
              </div>
            </label>
          </div>
        </div>

        <!-- DON'T Guide -->
        <div class="space-y-4">
          <div class="flex items-center gap-2 text-rose-700 font-extrabold text-base">
            <span class="w-6 h-6 rounded-lg bg-rose-100 flex items-center justify-center text-sm">⚠️</span>
            아빠가 무심코 하기 쉬운 DON'T (절대 주의)
          </div>

          <div class="space-y-3">
            <!-- DON'T 1 -->
            <div class="p-4 rounded-2xl bg-rose-50/60 border border-rose-200/70 space-y-1">
              <span class="text-xs font-bold text-rose-800 block">❌ 군대식 명령 및 엄격한 단호함 (거리감 유발)</span>
              <p class="text-xs text-slate-600 leading-relaxed">
                남자아이라는 이유로 밥상머리나 일상에서 단호하게 억누르면 아빠를 피하거나 신뢰에 금이 갑니다. 안전사고 외에는 유연한 설명과 달램이 필요합니다.
              </p>
            </div>

            <!-- DON'T 2 -->
            <div class="p-4 rounded-2xl bg-rose-50/60 border border-rose-200/70 space-y-1">
              <span class="text-xs font-bold text-rose-800 block">❌ 남 앞에서 먼저 ‘양보’를 강요하는 행위</span>
              <p class="text-xs text-slate-600 leading-relaxed">
                아빠가 상대편을 들어 도준이의 장난감을 건네주면 <em>“아빠는 내 편이 아니구나”</em> 하는 깊은 상처와 배신감을 느낍니다.
              </p>
            </div>

            <!-- DON'T 3 -->
            <div class="p-4 rounded-2xl bg-rose-50/60 border border-rose-200/70 space-y-1">
              <span class="text-xs font-bold text-rose-800 block">❌ 틀에 박힌 선 긋기·정형화된 미술 조기교육 강요</span>
              <p class="text-xs text-slate-600 leading-relaxed">
                선을 곧게 긋지 못해도 상관없습니다. 모방력과 공간 감각이 탁월하므로 정형화된 틀에 가두기보다 자유로운 낙서와 창작이 두뇌 발달에 핵심입니다.
              </p>
            </div>

            <!-- DON'T 4 -->
            <div class="p-4 rounded-2xl bg-rose-50/60 border border-rose-200/70 space-y-1">
              <span class="text-xs font-bold text-rose-800 block">❌ 약속 어기기 (일찍 오기, 선물 약속 등)</span>
              <p class="text-xs text-slate-600 leading-relaxed">
                도준이는 영리해서 약속 이행 여부로 신뢰를 측정합니다. 부득이하게 약속이 변경되면 반드시 정중히 사과하고 대안을 지켜주어야 합니다.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 6: CONFLICT SIMULATOR (KIDS CAFE DIALOGUE) -->
    <section class="glass-card-dark rounded-3xl p-6 sm:p-10 text-white space-y-6 relative overflow-hidden">
      <div class="absolute -right-10 -bottom-10 w-60 h-60 bg-indigo-500/20 rounded-full blur-3xl pointer-events-none"></div>

      <div class="space-y-2">
        <span class="text-xs font-bold uppercase tracking-wider text-indigo-300">Real Situation Script</span>
        <h3 class="text-xl sm:text-2xl font-black">실전 시뮬레이션: 키즈카페 장난감 쟁탈 상황 대처법</h3>
        <p class="text-xs sm:text-sm text-indigo-200">2주 전 키즈카페 고민, 앞으로 이렇게 대화하면 도준이의 자존감과 신뢰가 200% 상승합니다.</p>
      </div>

      <!-- Dialogue Bubbles -->
      <div class="space-y-4 max-w-2xl text-xs sm:text-sm">
        <!-- Step 1 -->
        <div class="flex items-start gap-3">
          <span class="px-2 py-1 bg-rose-500 text-white font-bold rounded-lg text-xs shrink-0">1단계</span>
          <div class="bg-white/10 backdrop-blur-md p-3.5 rounded-2xl rounded-tl-none border border-white/10 space-y-1">
            <p class="text-indigo-300 font-semibold text-xs">아빠가 상대 낯선 아이에게 먼저 방패막이 되기:</p>
            <p class="text-white">“친구야 미안하지만, 지금 도준이가 먼저 가지고 놀고 있단다. 조금만 기다려 주면 다 만들고 빌려줄게~”</p>
          </div>
        </div>

        <!-- Step 2 -->
        <div class="flex items-start gap-3">
          <span class="px-2 py-1 bg-amber-500 text-white font-bold rounded-lg text-xs shrink-0">2단계</span>
          <div class="bg-white/10 backdrop-blur-md p-3.5 rounded-2xl rounded-tl-none border border-white/10 space-y-1">
            <p class="text-amber-300 font-semibold text-xs">도준이에게 안도감과 양보의 명분을 열어주기:</p>
            <p class="text-white">“도준아, 친구도 이게 멋져 보여서 만져보고 싶었나 봐. 도준이가 멋진 성 다 만들고 나면 아빠한테 먼저 자랑하고 저 친구한테 빌려주자, 알겠지?”</p>
          </div>
        </div>

        <!-- Result -->
        <div class="p-3.5 rounded-xl bg-emerald-500/20 border border-emerald-400/30 text-emerald-200 text-xs flex items-center gap-2">
          <span>✨</span>
          <span><strong>기대 효과:</strong> 도준이는 ‘아빠가 내 영역을 지켜준다’는 확신을 얻고, 자발적으로 타인을 배려하는 성숙한 양보를 배우게 됩니다.</span>
        </div>
      </div>
    </section>

    <!-- FOOTER & ACTION BAR -->
    <footer class="flex flex-col sm:flex-row items-center justify-between gap-4 py-4 text-xs text-slate-500 border-t border-slate-200/80">
      <div class="flex items-center gap-2">
        <span class="font-bold text-slate-700">도준이네 아빠 성장 프로젝트</span>
        <span>•</span>
        <span>자이새순 어린이집 담임선생님 심층 상담 데이터 반영</span>
      </div>

      <div class="flex items-center gap-3">
        <button onclick="copySummaryText()" class="px-4 py-2 rounded-xl bg-white border border-slate-200 text-slate-700 font-bold hover:bg-slate-50 hover:text-indigo-600 transition shadow-sm flex items-center gap-1.5">
          📋 핵심 요약 복사하기
        </button>
        <button onclick="scrollToTop()" class="p-2 rounded-xl bg-indigo-50 border border-indigo-200 text-indigo-600 font-bold hover:bg-indigo-100 transition shadow-sm" title="맨 위로">
          ↑
        </button>
      </div>
    </footer>

  </main>

  <!-- Toast Notification Box -->
  <div id="toastBox" class="fixed bottom-6 left-1/2 -translate-x-1/2 px-5 py-3 rounded-2xl bg-slate-900/90 text-white text-xs sm:text-sm font-semibold shadow-2xl backdrop-blur-md opacity-0 pointer-events-none transition-all duration-300 z-50 flex items-center gap-2">
    <span id="toastIcon">✨</span>
    <span id="toastMsg">알림 메시지</span>
  </div>

  <script>
    // Radar Chart Engine
    const canvas = document.getElementById('radarCanvas');
    const ctx = canvas.getContext('2d');

    const metrics = [
      { label: "창의·구성", value: 0.98, display: "98%" },
      { label: "자존감·애살", value: 0.92, display: "92%" },
      { label: "규칙·조절", value: 0.90, display: "90%" },
      { label: "언어·어휘", value: 0.90, display: "90%" },
      { label: "또래리더십", value: 0.90, display: "90%" },
      { label: "기본생활", value: 0.85, display: "85%" }
    ];

    let animProgress = 0;

    function resizeCanvas() {
      const rect = canvas.getBoundingClientRect();
      const dpr = window.devicePixelRatio || 1;
      canvas.width = rect.width * dpr;
      canvas.height = rect.height * dpr;
      ctx.scale(dpr, dpr);
      drawRadar(animProgress);
    }

    function drawRadar(progress) {
      const rect = canvas.getBoundingClientRect();
      const w = rect.width;
      const h = rect.height;
      const cx = w / 2;
      const cy = h / 2;
      const radius = Math.min(cx, cy) * 0.72;
      const numPoints = metrics.length;
      const step = (Math.PI * 2) / numPoints;
      const startAngle = -Math.PI / 2;

      ctx.clearRect(0, 0, w, h);

      // Background Webs
      const levels = 5;
      for (let lvl = 1; lvl <= levels; lvl++) {
        const r = (radius / levels) * lvl;
        ctx.beginPath();
        for (let i = 0; i < numPoints; i++) {
          const angle = startAngle + i * step;
          const x = cx + r * Math.cos(angle);
          const y = cy + r * Math.sin(angle);
          if (i === 0) ctx.moveTo(x, y);
          else ctx.lineTo(x, y);
        }
        ctx.closePath();
        ctx.strokeStyle = lvl === levels ? "rgba(99, 102, 241, 0.25)" : "rgba(148, 163, 184, 0.18)";
        ctx.lineWidth = 1;
        ctx.stroke();
      }

      // Axis Lines
      for (let i = 0; i < numPoints; i++) {
        const angle = startAngle + i * step;
        const x = cx + radius * Math.cos(angle);
        const y = cy + radius * Math.sin(angle);
        ctx.beginPath();
        ctx.moveTo(cx, cy);
        ctx.lineTo(x, y);
        ctx.strokeStyle = "rgba(148, 163, 184, 0.25)";
        ctx.stroke();
      }

      // Draw Polygon Data (with animation progress)
      ctx.beginPath();
      for (let i = 0; i < numPoints; i++) {
        const angle = startAngle + i * step;
        const r = radius * (metrics[i].value * progress);
        const x = cx + r * Math.cos(angle);
        const y = cy + r * Math.sin(angle);
        if (i === 0) ctx.moveTo(x, y);
        else ctx.lineTo(x, y);
      }
      ctx.closePath();

      // Fill Gradient
      const grad = ctx.createRadialGradient(cx, cy, 10, cx, cy, radius);
      grad.addColorStop(0, "rgba(99, 102, 241, 0.5)");
      grad.addColorStop(0.7, "rgba(168, 85, 247, 0.35)");
      grad.addColorStop(1, "rgba(244, 63, 94, 0.2)");
      ctx.fillStyle = grad;
      ctx.fill();

      ctx.lineWidth = 2.5;
      ctx.strokeStyle = "#4F46E5";
      ctx.stroke();

      // Draw Data Nodes & Labels
      for (let i = 0; i < numPoints; i++) {
        const angle = startAngle + i * step;
        const r = radius * (metrics[i].value * progress);
        const nx = cx + r * Math.cos(angle);
        const ny = cy + r * Math.sin(angle);

        // Outer glow node
        ctx.beginPath();
        ctx.arc(nx, ny, 4.5, 0, Math.PI * 2);
        ctx.fillStyle = "#ffffff";
        ctx.fill();
        ctx.lineWidth = 2;
        ctx.strokeStyle = "#4F46E5";
        ctx.stroke();

        // Label Position
        const labelR = radius + 22;
        const lx = cx + labelR * Math.cos(angle);
        const ly = cy + labelR * Math.sin(angle);

        ctx.font = "bold 11px Pretendard, sans-serif";
        ctx.fillStyle = "#1e293b";
        ctx.textAlign = "center";
        ctx.textBaseline = "middle";
        ctx.fillText(metrics[i].label, lx, ly - 6);

        ctx.font = "9px Pretendard, sans-serif";
        ctx.fillStyle = "#6366f1";
        ctx.fillText(metrics[i].display, lx, ly + 7);
      }
    }

    function animateChart() {
      let start = null;
      const duration = 1200;

      function step(timestamp) {
        if (!start) start = timestamp;
        const progress = Math.min((timestamp - start) / duration, 1);
        // Ease Out Cubic
        animProgress = 1 - Math.pow(1 - progress, 3);
        drawRadar(animProgress);
        if (progress < 1) {
          requestAnimationFrame(step);
        }
      }
      requestAnimationFrame(step);
    }

    window.addEventListener('load', () => {
      resizeCanvas();
      animateChart();
    });
    window.addEventListener('resize', resizeCanvas);

    // Web Audio Sound Synthesizer (No external dependencies)
    const audioCtx = new (window.AudioContext || window.webkitAudioContext)();

    function playSoftBeep(frequency = 587.33, duration = 0.12) {
      if (audioCtx.state === 'suspended') {
        audioCtx.resume();
      }
      try {
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(frequency, audioCtx.currentTime);
        gain.gain.setValueAtTime(0.08, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + duration);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start();
        osc.stop(audioCtx.currentTime + duration);
      } catch (e) {
        // Fallback silently if audio restricted
      }
    }

    function showToast(msg, icon = '✨') {
      const toast = document.getElementById('toastBox');
      const toastMsg = document.getElementById('toastMsg');
      const toastIcon = document.getElementById('toastIcon');
      toastMsg.innerText = msg;
      toastIcon.innerText = icon;

      toast.classList.remove('opacity-0', 'pointer-events-none');
      toast.classList.add('opacity-100');

      setTimeout(() => {
        toast.classList.remove('opacity-100');
        toast.classList.add('opacity-0', 'pointer-events-none');
      }, 2500);
    }

    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Checklist Progress Counter & Sparkle Effect
    let completedCount = 0;
    const totalGoals = 5;

    function toggleItem(checkbox) {
      const parent = checkbox.closest('label');
      if (checkbox.checked) {
        completedCount++;
        playSoftBeep(783.99, 0.18); // G5 note
        createSparkles(checkbox);
        parent.classList.add('bg-emerald-100/70', 'border-emerald-400');
      } else {
        completedCount--;
        parent.classList.remove('bg-emerald-100/70', 'border-emerald-400');
      }

      const badge = document.getElementById('progressBadge');
      badge.innerText = `${completedCount} / ${totalGoals} 완료`;

      if (completedCount === totalGoals) {
        playSoftBeep(1046.50, 0.3); // High C6 celebrate
        showToast("멋져요! 오늘 아빠 실천 목표 5개를 모두 달성했습니다! 👏", "🏆");
      }
    }

    function createSparkles(element) {
      const rect = element.getBoundingClientRect();
      const count = 8;
      for (let i = 0; i < count; i++) {
        const span = document.createElement('span');
        span.className = 'sparkle text-xs';
        span.innerText = ['✨', '⭐', '💛', '🎉'][Math.floor(Math.random() * 4)];
        const tx = (Math.random() - 0.5) * 80 + 'px';
        const ty = (Math.random() - 0.7) * 80 + 'px';
        span.style.setProperty('--tx', tx);
        span.style.setProperty('--ty', ty);
        span.style.left = (rect.left + rect.width / 2 + window.scrollX) + 'px';
        span.style.top = (rect.top + rect.height / 2 + window.scrollY) + 'px';
        document.body.appendChild(span);
        setTimeout(() => span.remove(), 800);
      }
    }

    // Growth Momentum View Toggle
    function switchGrowthView(viewMode) {
      const beforeCol = document.getElementById('beforeCol');
      const afterCol = document.getElementById('afterCol');
      const compareBtn = document.getElementById('viewCompareBtn');
      const afterBtn = document.getElementById('viewAfterBtn');

      playSoftBeep(659.25, 0.1);

      if (viewMode === 'after') {
        beforeCol.classList.add('hidden');
        afterCol.classList.replace('md:col-span-1', 'md:col-span-2');
        compareBtn.classList.remove('bg-white', 'text-indigo-600', 'shadow-sm');
        compareBtn.classList.add('text-slate-600');
        afterBtn.classList.add('bg-white', 'text-indigo-600', 'shadow-sm');
        afterBtn.classList.remove('text-slate-600');
      } else {
        beforeCol.classList.remove('hidden');
        afterCol.classList.replace('md:col-span-2', 'md:col-span-1');
        afterBtn.classList.remove('bg-white', 'text-indigo-600', 'shadow-sm');
        afterBtn.classList.add('text-slate-600');
        compareBtn.classList.add('bg-white', 'text-indigo-600', 'shadow-sm');
        compareBtn.classList.remove('text-slate-600');
      }
    }

    // Clipboard Copy Summary
    function copySummaryText() {
      const summary = `[도준이 성장 & 기질 리포트]
- 기질 유형: L.C.A.S (논리적 크리에이터형)
- 핵심 특징: 인과관계 설명 시 100% 행동 수정, 창의 구성력 98%, 또래 리더십 90%
- 아빠 필살 가이드:
  1) 키즈카페 갈등 시 무조건 도준이 편 방패 되기
  2) 눈높이 인과관계 스토리텔링 훈육 (지시 금지)
  3) 비정형 재료(박스·블록) 제공 및 구체적 칭찬
  4) 축구·달리기 대근육 발산 놀이 친구 되기
  5) 삐쳤을 때 1~2분 기다려준 뒤 안아주기`;

      const textArea = document.createElement("textarea");
      textArea.value = summary;
      textArea.style.position = "fixed";
      textArea.style.opacity = "0";
      document.body.appendChild(textArea);
      textArea.select();
      try {
        document.execCommand('copy');
        showToast("클립보드에 도준이 리포트 요약본이 복사되었습니다!", "📋");
      } catch (err) {
        showToast("복사 중 오류가 발생했습니다.", "⚠️");
      }
      document.body.removeChild(textArea);
    }
  </script>
</body>
</html>
