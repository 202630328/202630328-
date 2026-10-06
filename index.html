<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>마타임 - 나의 시간은 내가 챙긴다</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .step-content { transition: all 0.25s ease-in-out; }
        @keyframes pulse-subtle {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.03); }
        }
        .clock-anim { animation: pulse-subtle 4s infinite ease-in-out; }
        
        /* 윈도우 환경을 위한 깔끔한 커스텀 스크롤바 */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: transparent; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }
    </style>
</head>
<body class="bg-slate-200 min-h-screen text-slate-800 flex justify-center items-center p-3 sm:p-6">

    <!-- 메인 앱 컨테이너 (화면 높이의 95%를 넘지 않도록 제한하고 스크롤 허용) -->
    <main class="w-full max-w-3xl bg-white rounded-2xl shadow-2xl flex flex-col h-[750px] max-h-[95vh] border border-slate-300 overflow-hidden">
        
        <!-- 상단 헤더 (고정) -->
        <header class="bg-slate-100 border-b border-slate-200 px-6 py-3.5 flex items-center justify-between select-none shrink-0">
            <div class="flex items-center gap-2 cursor-pointer" onclick="handleLogoClick()">
                <span class="text-xl">⏰</span>
                <span class="font-extrabold text-slate-800 tracking-tight text-base">MyTime</span>
            </div>

            <!-- 우측 프로필 / 관리자 / 로그인 상태 -->
            <div class="flex items-center gap-3">
                <button onclick="openAdminMode()" class="text-xs bg-slate-200 hover:bg-slate-300 text-slate-700 px-2.5 py-1.5 rounded-lg font-bold transition flex items-center gap-1">
                    <span>⚙️
                </button>
                <div id="userBadge" class="hidden flex items-center gap-2">
                    <div class="w-7 h-7 rounded-full bg-indigo-600 text-white font-bold text-xs flex items-center justify-center" id="avatarInitial">U</div>
                    <span id="badgeUserName" class="text-xs font-bold text-slate-700"></span>
                    <button onclick="logout()" class="text-xs text-slate-400 hover:text-red-500 underline ml-1">로그아웃</button>
                </div>
            </div>
        </header>

        <!-- 메인 컨텐츠 영역 (이 부분만 스크롤됨, flex-1 및 overflow-y-auto 적용) -->
        <div class="p-4 sm:p-6 flex-1 overflow-y-auto flex flex-col">
            
            <!-- STEP 1: 로그인 / 회원가입 (my-auto를 주어 세로 중앙 정렬 유지) -->
            <section id="step1" class="step-content max-w-md mx-auto w-full space-y-5 my-auto">
                <div class="text-center space-y-1">
                    <h2 class="text-2xl font-black text-slate-900">마타임 시작하기</h2>
                    <p class="text-xs text-slate-500">시간표를 설정하려면 먼저 로그인해 주세요</p>
                </div>

                <div class="flex border-b text-sm font-bold text-center">
                    <button id="tabLoginBtn" onclick="switchAuthTab('login')" class="w-1/2 py-2 border-b-2 border-blue-600 text-blue-600">로그인</button>
                    <button id="tabRegisterBtn" onclick="switchAuthTab('register')" class="w-1/2 py-2 border-b-2 border-transparent text-slate-400 hover:text-slate-600">회원가입</button>
                </div>

                <!-- 로그인 폼 -->
                <form id="loginForm" onsubmit="handleLogin(event)" class="space-y-3">
                    <div>
                        <label class="block text-xs font-semibold text-slate-500 mb-1">아이디</label>
                        <input type="text" id="loginId" placeholder="아이디" required class="w-full p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none text-sm">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-slate-500 mb-1">비밀번호</label>
                        <input type="password" id="loginPw" placeholder="비밀번호" onkeydown="checkCapsLock(event)" onkeyup="checkCapsLock(event)" required class="w-full p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none text-sm">
                        <!-- Caps Lock 경고 문구 -->
                        <p id="loginPwCapsLock" class="hidden text-xs text-amber-600 font-bold mt-1.5 flex items-center gap-1">
                            <span>⚠️</span> Caps Lock이 켜져 있습니다. 비밀번호 입력 시 꺼주세요.
                        </p>
                    </div>
                    <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3.5 rounded-xl transition shadow-lg shadow-blue-100 text-sm">로그인하기</button>
                </form>

                <!-- 회원가입 폼 -->
                <form id="registerForm" onsubmit="handleRegister(event)" class="space-y-3 hidden">
                    <div>
                        <label class="block text-xs font-semibold text-slate-500 mb-1">이름 / 닉네임</label>
                        <input type="text" id="regName" placeholder="예: 언주짱" required class="w-full p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none text-sm">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-slate-500 mb-1">아이디</label>
                        <input type="text" id="regId" placeholder="아이디 생성" required class="w-full p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none text-sm">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-slate-500 mb-1">비밀번호</label>
                        <input type="password" id="regPw" placeholder="비밀번호 입력 (영문/숫자)" oninput="validateRegPassword()" required class="w-full p-3 border border-slate-200 rounded-xl focus:ring-2 focus:ring-blue-500 outline-none text-sm transition">
                        <p id="regPwError" class="hidden text-xs text-red-500 font-bold mt-1.5 flex items-center gap-1"></p>
                    </div>
                    <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3.5 rounded-xl transition shadow-lg shadow-blue-100 text-sm">가입 완료하기</button>
                </form>
            </section>


            <!-- STEP MAIN: 메인 화면 -->
            <section id="stepMain" class="step-content hidden space-y-4 my-auto">
                
                <!-- 상단 인사말 배너 -->
                <div class="bg-gradient-to-r from-blue-50 to-indigo-50 border border-blue-100 p-4 rounded-2xl flex items-center justify-between shrink-0">
                    <div>
                        <h2 class="text-base font-extrabold text-slate-800">
                            <span id="welcomeUserName" class="text-blue-600"></span>님, <span id="randomGreetingText">반갑습니다!</span>
                        </h2>
                        <p class="text-xs text-slate-500 mt-0.5">오늘도 계획적인 시간 관리를 응원합니다!</p>
                    </div>
                    <span class="text-2xl">✨</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-12 gap-5 items-stretch pb-4">
                    <!-- 좌측: 핵심 기능 버튼 2개 -->
                    <div class="md:col-span-7 grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <button onclick="openTodaySchedule()" class="flex flex-col items-center justify-center p-6 bg-white hover:bg-slate-50 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition group text-center min-h-[180px]">
                            <div class="w-16 h-16 bg-orange-500 rounded-2xl flex items-center justify-center text-white text-3xl shadow-lg shadow-orange-200 group-hover:scale-105 transition">
                                ⏱️
                            </div>
                            <span class="mt-4 font-bold text-slate-800 text-base">오늘 시간 계산</span>
                            <span class="text-xs text-slate-400 mt-1">오늘의 짬시간 정밀 분석</span>
                        </button>

                        <button onclick="goToStep('stepWeekly')" class="flex flex-col items-center justify-center p-6 bg-white hover:bg-slate-50 rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition group text-center min-h-[180px]">
                            <div class="w-16 h-16 bg-blue-600 rounded-2xl flex items-center justify-center text-white text-3xl shadow-lg shadow-blue-200 group-hover:scale-105 transition">
                                📅
                            </div>
                            <span class="mt-4 font-bold text-slate-800 text-base">주간 시간표</span>
                            <span class="text-xs text-slate-400 mt-1">월~금 고정 스케줄 설정</span>
                        </button>
                    </div>

                    <!-- 우측: 실시간 시계 카드 -->
                    <div class="md:col-span-5 flex flex-col justify-between min-h-[250px]">
                        <div class="bg-gradient-to-b from-slate-900 to-indigo-950 text-white rounded-2xl border border-slate-800 shadow-lg p-5 flex flex-col items-center text-center relative overflow-hidden h-full justify-center">
                            
                            <!-- 실시간 회전 시계 SVG -->
                            <div class="clock-anim mb-3 relative flex items-center justify-center">
                                <svg width="90" height="90" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <circle cx="50" cy="50" r="45" fill="#1E293B" stroke="#38BDF8" stroke-width="4"/>
                                    <circle cx="50" cy="50" r="40" fill="#0F172A"/>
                                    <circle cx="50" cy="15" r="2" fill="#38BDF8"/>
                                    <circle cx="85" cy="50" r="2" fill="#38BDF8"/>
                                    <circle cx="50" cy="85" r="2" fill="#38BDF8"/>
                                    <circle cx="15" cy="50" r="2" fill="#38BDF8"/>
                                    <line id="clockHourHand" x1="50" y1="50" x2="50" y2="28" stroke="#F43F5E" stroke-width="3.5" stroke-linecap="round"/>
                                    <line id="clockMinuteHand" x1="50" y1="50" x2="50" y2="18" stroke="#38BDF8" stroke-width="2.5" stroke-linecap="round"/>
                                    <circle cx="50" cy="50" r="4" fill="#FFFFFF"/>
                                </svg>
                            </div>

                            <div id="zoomClock" class="text-3xl font-black tracking-tight text-cyan-300">12:00 PM</div>
                            <div id="zoomDate" class="text-xs text-slate-300 mt-1 font-medium">--년 --월 --일 --요일</div>

                            <div id="homeScheduleSummary" class="mt-4 pt-3 border-t border-slate-800 text-xs font-semibold text-slate-300 w-full">
                                '오늘 시간 계산'을 눌러 짬시간을 정밀 분석해보세요!
                            </div>
                        </div>
                    </div>
                </div>
            </section>


            <!-- STEP WEEKLY: 주간 시간표 설정 -->
            <section id="stepWeekly" class="step-content hidden max-w-xl mx-auto w-full space-y-5 pb-6">
                
                <div class="border-b pb-3 flex justify-between items-center shrink-0">
                    <div>
                        <div class="flex items-center gap-2">
                            <span class="text-xs font-bold text-blue-600 bg-blue-50 px-2.5 py-1 rounded-full">주간 설정</span>
                            <span id="autoSaveStatus" class="text-[11px] text-emerald-600 font-medium opacity-0 transition-opacity duration-300">✓ 실시간 자동 저장됨</span>
                        </div>
                        <h2 class="text-xl font-bold mt-1 text-slate-900">월~금 주간 시간표</h2>
                    </div>
                    
                    <button onclick="goToStep('stepMain')" class="bg-slate-800 hover:bg-slate-900 text-white font-bold px-4 py-2 rounded-xl text-xs shadow-md transition flex items-center gap-1.5 shrink-0">
                        <span>🏠</span> 메인으로
                    </button>
                </div>

                <div class="flex bg-slate-100 p-1 rounded-xl text-xs font-bold text-slate-500 shrink-0">
                    <button id="dayTab-mon" onclick="switchDayTab('mon')" class="flex-1 py-2 rounded-lg bg-white text-blue-600 shadow-sm">월</button>
                    <button id="dayTab-tue" onclick="switchDayTab('tue')" class="flex-1 py-2 rounded-lg">화</button>
                    <button id="dayTab-wed" onclick="switchDayTab('wed')" class="flex-1 py-2 rounded-lg">수</button>
                    <button id="dayTab-thu" onclick="switchDayTab('thu')" class="flex-1 py-2 rounded-lg">목</button>
                    <button id="dayTab-fri" onclick="switchDayTab('fri')" class="flex-1 py-2 rounded-lg">금</button>
                </div>

                <div class="space-y-3 bg-slate-50 p-4 rounded-2xl border border-slate-200">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                        <div>
                            <label class="block text-xs font-semibold text-slate-600 mb-1">☀️ 기상 시간</label>
                            <div class="flex gap-2">
                                <select id="weekWake_h" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                                <select id="weekWake_m" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            </div>
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-600 mb-1">🌙 취침 시간</label>
                            <div class="flex gap-2">
                                <select id="weekBed_h" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                                <select id="weekBed_m" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            </div>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">🏫 학교 끝나는 시간</label>
                        <div class="flex gap-2">
                            <select id="weekSchoolEnd_h" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            <select id="weekSchoolEnd_m" onchange="autoSaveCurrentDaySchedule()" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">📚 다니는 학원 총 시간</label>
                        <select id="weekAcademyHours" onchange="autoSaveCurrentDaySchedule()" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                            <option value="0">학원 없음 (0시간)</option>
                            <option value="2">2시간</option>
                            <option value="3">3시간</option>
                            <option value="4">4시간</option>
                            <option value="5">5시간 이상</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">📌 추가 일정 (운동, 과외 등)</label>
                        <select id="weekExtraHours" onchange="autoSaveCurrentDaySchedule()" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                            <option value="0">없음 (0시간)</option>
                            <option value="1">1시간</option>
                            <option value="2">2시간</option>
                            <option value="3">3시간 이상</option>
                        </select>
                    </div>
                </div>

                <div class="pt-2 shrink-0">
                    <button onclick="resetAllWeeklySchedule()" class="w-full bg-red-50 hover:bg-red-100 text-red-600 font-bold py-3 rounded-xl transition border border-red-200 text-xs flex items-center justify-center gap-1">
                        <span>⚠️</span> 주간 시간표 전체 초기화
                    </button>
                </div>
            </section>


            <!-- STEP TODAY: 오늘 시간 계산하기 -->
            <section id="stepToday" class="step-content hidden max-w-xl mx-auto w-full space-y-5 pb-6">
                
                <div class="border-b pb-3 flex justify-between items-center shrink-0">
                    <div>
                        <span class="text-xs font-bold text-blue-600 bg-blue-50 px-2.5 py-1 rounded-full">TODAY</span>
                        <h2 class="text-xl font-bold mt-1 text-slate-900"><span id="todayDayName" class="text-blue-600"></span> 시간표 구체적 수정</h2>
                    </div>
                    
                    <button onclick="goToStep('stepMain')" class="bg-slate-800 hover:bg-slate-900 text-white font-bold px-4 py-2 rounded-xl text-xs shadow-md transition flex items-center gap-1.5 shrink-0">
                        <span>🏠</span> 메인으로
                    </button>
                </div>

                <p class="text-xs text-slate-500 shrink-0">주간 시간표에서 불러온 오늘의 기본 틀입니다. 오늘 특이사항을 수정해 주세요.</p>

                <div class="space-y-3 bg-slate-50 p-4 rounded-2xl border border-slate-200">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                        <div>
                            <label class="block text-xs font-semibold text-slate-600 mb-1">☀️ 오늘 기상 시간</label>
                            <div class="flex gap-2">
                                <select id="todayWake_h" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                                <select id="todayWake_m" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            </div>
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-600 mb-1">🌙 오늘 목표 취침 시간</label>
                            <div class="flex gap-2">
                                <select id="todayBed_h" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                                <select id="todayBed_m" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            </div>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">🏫 오늘 학교 끝나는 시간</label>
                        <div class="flex gap-2">
                            <select id="todaySchoolEnd_h" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                            <select id="todaySchoolEnd_m" class="w-1/2 p-2.5 border rounded-xl text-sm bg-white cursor-pointer"></select>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">오늘 학원 시간</label>
                        <select id="todayAcademyHours" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                            <option value="0">오늘 학원 없음 / 휴강 (0시간)</option>
                            <option value="2">2시간</option>
                            <option value="3">3시간</option>
                            <option value="4">4시간</option>
                            <option value="5">5시간 이상</option>
                        </select>
                    </div>

                    <div class="grid grid-cols-2 gap-3 bg-blue-50/50 p-3 rounded-xl border border-blue-100">
                        <div>
                            <label class="block text-xs font-semibold text-blue-900 mb-1">🚶 이동 시간 (학원 등)</label>
                            <select id="todayCommuteHours" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                                <option value="0">이동 거의 없음 (0분)</option>
                                <option value="0.33">약 20분</option>
                                <option value="0.5" selected>약 30분</option>
                                <option value="0.75">약 45분</option>
                                <option value="1">약 1시간</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-blue-900 mb-1">🚿 씻기/준비 시간</label>
                            <select id="todayRoutineHours" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                                <option value="0.33">간단히 (약 20분)</option>
                                <option value="0.5" selected>보통 (약 30분)</option>
                                <option value="0.75">여유있게 (약 45분)</option>
                                <option value="1">1시간 이상</option>
                            </select>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">📌 오늘 추가 일정</label>
                        <select id="todayExtraHours" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                            <option value="0">없음 (0시간)</option>
                            <option value="1">1시간</option>
                            <option value="2">2시간</option>
                            <option value="3">3시간 이상</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-xs font-semibold text-slate-600 mb-1">🔥 오늘 제출할 숙제량</label>
                        <select id="todayHomeworkHours" class="w-full p-2.5 border rounded-xl text-sm bg-white cursor-pointer">
                            <option value="0.5">🟢 적음 (약 30분 소요)</option>
                            <option value="1.5" selected>🟡 보통 (약 1.5시간 소요)</option>
                            <option value="3">🔴 폭탄! (약 3시간 이상 소요)</option>
                        </select>
                    </div>
                </div>

                <div class="flex gap-2 pt-2 shrink-0">
                    <button onclick="goToStep('stepMain')" class="w-1/3 bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold py-3 rounded-xl transition text-sm">취소</button>
                    <button onclick="calculateTodayFreeTime()" class="w-2/3 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded-xl transition shadow-lg shadow-blue-100 text-sm">🤖 오늘 짬시간 계산하기</button>
                </div>
            </section>


            <!-- STEP RESULT: AI 결과 리포트 -->
            <section id="stepResult" class="step-content hidden max-w-xl mx-auto w-full space-y-5 text-center my-auto">
                
                <div class="border-b pb-3 text-left flex justify-between items-center">
                    <div>
                        <span class="text-xs font-bold text-blue-600 bg-blue-50 px-2.5 py-1 rounded-full">REPORT</span>
                        <h2 class="text-xl font-bold mt-1 text-slate-900">오늘의 짬시간 분석</h2>
                    </div>
                    <button onclick="goToStep('stepMain')" class="bg-slate-800 hover:bg-slate-900 text-white font-bold px-4 py-2 rounded-xl text-xs shadow-md transition flex items-center gap-1.5">
                        <span>🏠</span> 메인으로
                    </button>
                </div>

                <div class="bg-gradient-to-br from-blue-600 to-indigo-700 text-white p-6 rounded-2xl shadow-xl">
                    <p class="text-xs font-medium text-blue-100"><span id="resUserName" class="underline font-bold"></span> 학생의 오늘 순수 짬시간</p>
                    <p id="resFreeTime" class="text-4xl font-black my-3 tracking-tight">0시간 0분</p>
                    <p id="resSleepTimeNotice" class="text-xs text-blue-100 opacity-90"></p>
                </div>

                <div class="text-left bg-slate-50 p-4 rounded-2xl border border-slate-200 space-y-2">
                    <div class="flex items-center gap-1.5">
                        <span class="text-base">🤖</span>
                        <h3 class="font-bold text-xs text-slate-800 uppercase tracking-wide">AI 코치 솔루션</h3>
                    </div>
                    <p id="resAiAdvice" class="text-xs text-slate-600 leading-relaxed font-medium"></p>
                </div>

                <div class="space-y-2 pt-2">
                    <button onclick="goToStep('stepToday')" class="w-full bg-blue-50 hover:bg-blue-100 text-blue-700 font-bold py-3 rounded-xl transition text-sm">스케줄 다시 수정하기</button>
                </div>
            </section>


            <!-- STEP ADMIN: 관리자 모드 -->
            <section id="stepAdmin" class="step-content hidden max-w-2xl mx-auto w-full space-y-5 my-auto">
                <div class="border-b pb-3 flex justify-between items-center">
                    <div>
                        <span class="text-xs font-bold text-red-600 bg-red-50 px-2.5 py-1 rounded-full">ADMIN</span>
                        <h2 class="text-xl font-bold mt-1 text-slate-900">회원 명단 및 시스템 관리</h2>
                    </div>
                    
                    <button onclick="handleLogoClick()" class="bg-slate-800 hover:bg-slate-900 text-white font-bold px-4 py-2 rounded-xl text-xs shadow-md transition flex items-center gap-1.5">
                        <span>🏠</span> 돌아가기
                    </button>
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div class="bg-indigo-50 border border-indigo-100 p-4 rounded-2xl">
                        <span class="text-xs font-bold text-indigo-500">전체 가입 회원</span>
                        <p class="text-2xl font-black text-indigo-900 mt-1" id="adminTotalUserCount">0명</p>
                    </div>
                    <div class="bg-slate-50 border border-slate-200 p-4 rounded-2xl flex flex-col justify-center">
                        <button onclick="changeAdminPassword()" class="text-xs font-bold text-slate-600 hover:text-slate-900 underline text-left">
                            🔐 관리자 비밀번호 변경
                        </button>
                    </div>
                </div>

                <div class="bg-white border border-slate-200 rounded-2xl overflow-hidden shadow-sm">
                    <div class="bg-slate-50 px-4 py-3 border-b border-slate-200 font-bold text-xs text-slate-600 grid grid-cols-12 gap-2">
                        <span class="col-span-3">아이디</span>
                        <span class="col-span-3">이름/닉네임</span>
                        <span class="col-span-4">시간표 설정 상태</span>
                        <span class="col-span-2 text-center">관리</span>
                    </div>

                    <div id="adminUserListContainer" class="divide-y divide-slate-100 max-h-80 overflow-y-auto text-xs">
                    </div>
                </div>
            </section>

        </div>
    </main>

    <!-- 스크립트 -->
    <script>
        let currentUser = null;
        let activeDayTab = 'mon';

        const timeSelectIds = ['weekWake', 'weekBed', 'weekSchoolEnd', 'todayWake', 'todayBed', 'todaySchoolEnd'];

        const greetingList = [
            "좋은 하루입니다! ✨",
            "반갑습니다! 오늘 하루도 화이팅! 💪",
            "알찬 하루를 함께 만들어봐요! ☀️",
            "오늘의 짬시간을 알뜰하게 챙겨보세요! ⏱️",
            "반가워요! 당신의 최고의 하루를 응원합니다 🚀",
            "오늘도 계획적인 시간 관리 되세요! 🎯"
        ];

        const emptyDayData = { wake: "", bed: "", schoolEnd: "", academy: 0, extra: 0 };
        const emptyWeekly = {
            mon: { ...emptyDayData },
            tue: { ...emptyDayData },
            wed: { ...emptyDayData },
            thu: { ...emptyDayData },
            fri: { ...emptyDayData }
        };

        function initTimeSelects() {
            timeSelectIds.forEach(id => {
                const hEl = document.getElementById(id + '_h');
                const mEl = document.getElementById(id + '_m');
                if (!hEl || !mEl) return;

                let hHtml = '<option value="">--시</option>';
                for (let i = 0; i < 24; i++) {
                    const val = String(i).padStart(2, '0');
                    let label = `${val}시`;
                    if (i === 0) label = `00시 (자정)`;
                    else if (i === 12) label = `12시 (정오)`;
                    else if (i > 12) label = `${val}시 (오후 ${i - 12}시)`;
                    else label = `${val}시 (오전 ${i}시)`;
                    hHtml += `<option value="${val}">${label}</option>`;
                }
                hEl.innerHTML = hHtml;

                let mHtml = '<option value="">--분</option>';
                for (let i = 0; i < 60; i += 10) {
                    const val = String(i).padStart(2, '0');
                    mHtml += `<option value="${val}">${val}분</option>`;
                }
                mEl.innerHTML = mHtml;
            });
        }

        function getTimeValue(id) {
            const h = document.getElementById(id + '_h')?.value;
            const m = document.getElementById(id + '_m')?.value;
            if (!h || !m) return "";
            return `${h}:${m}`;
        }

        function setTimeValue(id, val) {
            const hEl = document.getElementById(id + '_h');
            const mEl = document.getElementById(id + '_m');
            if (!hEl || !mEl) return;

            if (!val || !val.includes(':')) {
                hEl.value = "";
                mEl.value = "";
                return;
            }

            const [h, m] = val.split(':');
            hEl.value = String(h).padStart(2, '0');
            mEl.value = String(m).padStart(2, '0');
        }

        window.onload = function() {
            initTimeSelects();
            startClock();
            const savedUser = localStorage.getItem('mytime_current_user');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                updateUserBadge();
                goToStep('stepMain');
            } else {
                goToStep('step1');
            }
        };

        function startClock() {
            function update() {
                const now = new Date();
                let hours = now.getHours();
                const minutes = now.getMinutes();
                const seconds = now.getSeconds();
                
                const minutesStr = String(minutes).padStart(2, '0');
                const ampm = hours >= 12 ? 'PM' : 'AM';
                const displayHours = hours % 12 ? hours % 12 : 12;

                const timeStr = `${displayHours}:${minutesStr} ${ampm}`;
                const year = now.getFullYear();
                const month = now.getMonth() + 1;
                const date = now.getDate();
                const dayNames = ['일요일', '월요일', '화요일', '수요일', '목요일', '금요일', '토요일'];
                const dayName = dayNames[now.getDay()];

                if(document.getElementById('zoomClock')) document.getElementById('zoomClock').innerText = timeStr;
                if(document.getElementById('zoomDate')) document.getElementById('zoomDate').innerText = `${year}년 ${month}월 ${date}일 ${dayName}`;

                const hourAngle = ((hours % 12) + minutes / 60) * 30;
                const minuteAngle = (minutes + seconds / 60) * 6;

                const hourHand = document.getElementById('clockHourHand');
                const minuteHand = document.getElementById('clockMinuteHand');

                if (hourHand) hourHand.setAttribute('transform', `rotate(${hourAngle}, 50, 50)`);
                if (minuteHand) minuteHand.setAttribute('transform', `rotate(${minuteAngle}, 50, 50)`);
            }
            update();
            setInterval(update, 1000);
        }

        function checkCapsLock(e) {
            const capsEl = document.getElementById('loginPwCapsLock');
            if (e.getModifierState && e.getModifierState('CapsLock')) {
                capsEl.classList.remove('hidden');
            } else {
                capsEl.classList.add('hidden');
            }
        }

        function validateRegPassword() {
            const input = document.getElementById('regPw');
            const errEl = document.getElementById('regPwError');
            const val = input.value;

            if (!val) {
                errEl.classList.add('hidden');
                input.classList.remove('border-red-500', 'ring-2', 'ring-red-500');
                return true;
            }

            const hasKorean = /[ㄱ-ㅎ|ㅏ-ㅣ|가-힣]/.test(val);

            if (hasKorean) {
                errEl.innerHTML = "<span>⚠️</span> 한글이 입력되었습니다. 영문/숫자로 입력해주세요.";
                errEl.classList.remove('hidden');
                input.classList.add('border-red-500', 'ring-2', 'ring-red-500');
                return false;
            } else {
                errEl.classList.add('hidden');
                input.classList.remove('border-red-500', 'ring-2', 'ring-red-500');
                return true;
            }
        }

        function goToStep(stepId) {
            if (!currentUser && stepId !== 'step1' && stepId !== 'stepAdmin') {
                alert('로그인이 필요한 기능입니다. 먼저 로그인해 주세요.');
                stepId = 'step1';
            }

            const steps = ['step1', 'stepMain', 'stepWeekly', 'stepToday', 'stepResult', 'stepAdmin'];
            steps.forEach(s => document.getElementById(s).classList.add('hidden'));
            document.getElementById(stepId).classList.remove('hidden');

            if (stepId === 'stepMain') {
                setRandomGreeting();
                updateHomeScheduleSummaryUI();
            } else if (stepId === 'stepWeekly') {
                switchDayTab(activeDayTab);
            }
        }

        function updateHomeScheduleSummaryUI() {
            const summaryEl = document.getElementById('homeScheduleSummary');
            if (currentUser && currentUser.todaySummary) {
                summaryEl.innerHTML = currentUser.todaySummary;
            } else {
                summaryEl.innerHTML = `'오늘 시간 계산'을 눌러 짬시간을 정밀 분석해보세요!`;
            }
        }

        function setRandomGreeting() {
            if (!currentUser) return;
            const randomIndex = Math.floor(Math.random() * greetingList.length);
            document.getElementById('welcomeUserName').innerText = currentUser.name;
            document.getElementById('randomGreetingText').innerText = greetingList[randomIndex];
        }

        function handleLogoClick() {
            if (currentUser) {
                goToStep('stepMain');
            } else {
                goToStep('step1');
            }
        }

        function switchAuthTab(tab) {
            if (tab === 'login') {
                document.getElementById('loginForm').classList.remove('hidden');
                document.getElementById('registerForm').classList.add('hidden');
                document.getElementById('tabLoginBtn').className = "w-1/2 py-2 border-b-2 border-blue-600 text-blue-600 font-bold";
                document.getElementById('tabRegisterBtn').className = "w-1/2 py-2 border-b-2 border-transparent text-slate-400 font-bold";
            } else {
                document.getElementById('loginForm').classList.add('hidden');
                document.getElementById('registerForm').classList.remove('hidden');
                document.getElementById('tabRegisterBtn').className = "w-1/2 py-2 border-b-2 border-blue-600 text-blue-600 font-bold";
                document.getElementById('tabLoginBtn').className = "w-1/2 py-2 border-b-2 border-transparent text-slate-400 font-bold";
            }
        }

        function handleRegister(e) {
            e.preventDefault();
            const name = document.getElementById('regName').value.trim();
            const id = document.getElementById('regId').value.trim();
            const pw = document.getElementById('regPw').value.trim();

            if (!validateRegPassword()) {
                alert('비밀번호를 규칙에 맞게 입력해 주세요 (한글 입력 불가).');
                return;
            }

            let users = JSON.parse(localStorage.getItem('mytime_users') || '[]');
            if (users.find(u => u.id === id)) return alert('이미 존재하는 아이디입니다.');

            const newUser = { id, pw, name, weekly: JSON.parse(JSON.stringify(emptyWeekly)), todaySummary: null };
            users.push(newUser);
            localStorage.setItem('mytime_users', JSON.stringify(users));
            alert('회원가입이 완료되었습니다! 로그인해 주세요.');
            switchAuthTab('login');
        }

        function handleLogin(e) {
            e.preventDefault();
            const id = document.getElementById('loginId').value.trim();
            const pw = document.getElementById('loginPw').value.trim();

            let users = JSON.parse(localStorage.getItem('mytime_users') || '[]');
            const user = users.find(u => u.id === id && u.pw === pw);

            if (user) {
                if (!user.weekly) user.weekly = JSON.parse(JSON.stringify(emptyWeekly));
                currentUser = user;
                localStorage.setItem('mytime_current_user', JSON.stringify(user));
                updateUserBadge();
                goToStep('stepMain');
            } else {
                alert('아이디 또는 비밀번호가 일치하지 않습니다.');
            }
        }

        function logout() {
            localStorage.removeItem('mytime_current_user');
            currentUser = null;
            document.getElementById('userBadge').classList.add('hidden');
            goToStep('step1');
        }

        function updateUserBadge() {
            if (currentUser) {
                document.getElementById('badgeUserName').innerText = currentUser.name;
                document.getElementById('avatarInitial').innerText = currentUser.name.charAt(0);
                document.getElementById('userBadge').classList.remove('hidden');
            }
        }

        function openAdminMode() {
            const adminPw = localStorage.getItem('mytime_admin_pw') || 'djswnwnd';
            const inputPw = prompt('🔒 관리자 비밀번호를 입력해주세요:');

            if (inputPw === null) return;

            if (inputPw === adminPw) {
                renderAdminView();
                goToStep('stepAdmin');
            } else {
                alert('❌ 비밀번호가 올바르지 않습니다.');
            }
        }

        function renderAdminView() {
            const users = JSON.parse(localStorage.getItem('mytime_users') || '[]');
            document.getElementById('adminTotalUserCount').innerText = `${users.length}명`;

            const container = document.getElementById('adminUserListContainer');
            container.innerHTML = '';

            if (users.length === 0) {
                container.innerHTML = '<div class="p-6 text-center text-slate-400 font-medium">가입된 회원이 없습니다.</div>';
                return;
            }

            users.forEach((u) => {
                let isSet = false;
                if (u.weekly) {
                    isSet = Object.values(u.weekly).some(day => day.wake && day.bed && day.schoolEnd);
                }

                const row = document.createElement('div');
                row.className = "px-4 py-3 grid grid-cols-12 gap-2 items-center hover:bg-slate-50 transition";
                row.innerHTML = `
                    <span class="col-span-3 font-semibold text-slate-800 overflow-hidden text-ellipsis">${u.id}</span>
                    <span class="col-span-3 text-slate-700">${u.name}</span>
                    <span class="col-span-4">
                        ${isSet ? '<span class="text-emerald-600 font-bold bg-emerald-50 px-2 py-0.5 rounded">설정 완료</span>' : '<span class="text-slate-400">미설정</span>'}
                    </span>
                    <div class="col-span-2 text-center">
                        <button onclick="deleteUserByAdmin('${u.id}')" class="text-xs text-red-500 hover:text-red-700 font-bold underline">삭제</button>
                    </div>
                `;
                container.appendChild(row);
            });
        }

        function deleteUserByAdmin(userId) {
            if (confirm(`정말 회원 [${userId}] 님을 강제 삭제하시겠습니까?`)) {
                let users = JSON.parse(localStorage.getItem('mytime_users') || '[]');
                users = users.filter(u => u.id !== userId);
                localStorage.setItem('mytime_users', JSON.stringify(users));

                if (currentUser && currentUser.id === userId) {
                    logout();
                } else {
                    renderAdminView();
                }
                alert('회원이 삭제되었습니다.');
            }
        }

        function changeAdminPassword() {
            const newPw = prompt('새로 변경할 관리자 비밀번호를 입력해 주세요:');
            if (newPw && newPw.trim() !== '') {
                localStorage.setItem('mytime_admin_pw', newPw.trim());
                alert('관리자 비밀번호가 성공적으로 변경되었습니다!');
            }
        }

        function switchDayTab(day) {
            activeDayTab = day;
            const days = ['mon', 'tue', 'wed', 'thu', 'fri'];
            days.forEach(d => {
                const btn = document.getElementById(`dayTab-${d}`);
                if (d === day) {
                    btn.className = "flex-1 py-2 rounded-lg bg-white text-blue-600 shadow-sm font-bold";
                } else {
                    btn.className = "flex-1 py-2 rounded-lg text-slate-500 font-bold";
                }
            });

            const dayData = (currentUser && currentUser.weekly && currentUser.weekly[day]) ? currentUser.weekly[day] : emptyDayData;
            setTimeValue('weekWake', dayData.wake);
            setTimeValue('weekBed', dayData.bed);
            setTimeValue('weekSchoolEnd', dayData.schoolEnd);
            document.getElementById('weekAcademyHours').value = dayData.academy || 0;
            document.getElementById('weekExtraHours').value = dayData.extra || 0;
        }

        function autoSaveCurrentDaySchedule() {
            if (!currentUser) return;
            if (!currentUser.weekly) currentUser.weekly = JSON.parse(JSON.stringify(emptyWeekly));

            currentUser.weekly[activeDayTab] = {
                wake: getTimeValue('weekWake'),
                bed: getTimeValue('weekBed'),
                schoolEnd: getTimeValue('weekSchoolEnd'),
                academy: parseFloat(document.getElementById('weekAcademyHours').value),
                extra: parseFloat(document.getElementById('weekExtraHours').value)
            };

            saveUserData();

            const statusEl = document.getElementById('autoSaveStatus');
            statusEl.classList.remove('opacity-0');
            setTimeout(() => { statusEl.classList.add('opacity-0'); }, 1200);
        }

        function saveUserData() {
            localStorage.setItem('mytime_current_user', JSON.stringify(currentUser));
            let users = JSON.parse(localStorage.getItem('mytime_users') || '[]');
            const idx = users.findIndex(u => u.id === currentUser.id);
            if (idx !== -1) {
                users[idx] = currentUser;
                localStorage.setItem('mytime_users', JSON.stringify(users));
            }
        }

        function resetAllWeeklySchedule() {
            if (!currentUser) return;

            const confirmReset = confirm("⚠️ 주의: 정말 모든 요일의 주간 시간표를 초기화하시겠습니까?\n이 작업은 되돌릴 수 없습니다.");
            
            if (confirmReset) {
                currentUser.weekly = JSON.parse(JSON.stringify(emptyWeekly));
                currentUser.todaySummary = null;
                saveUserData();
                switchDayTab(activeDayTab);
                alert("주간 시간표가 성공적으로 초기화되었습니다.");
            }
        }

        function openTodaySchedule() {
            if (!currentUser) {
                alert('로그인이 필요합니다.');
                goToStep('step1');
                return;
            }

            const dayMap = ['sun', 'mon', 'tue', 'wed', 'thu', 'fri', 'sat'];
            const dayNamesKo = ['일요일', '월요일', '화요일', '수요일', '목요일', '금요일', '토요일'];
            
            const now = new Date();
            let dayIndex = now.getDay();
            
            let dayKey = dayMap[dayIndex];
            let dayName = dayNamesKo[dayIndex];
            if (dayIndex === 0 || dayIndex === 6) {
                dayKey = 'mon';
                dayName = '월요일(주말 대체)';
            }

            const dayData = (currentUser.weekly && currentUser.weekly[dayKey]) ? currentUser.weekly[dayKey] : null;

            const isConfigured = dayData && dayData.wake && dayData.bed && dayData.schoolEnd;

            if (!isConfigured) {
                alert('⚠️ 주간 시간표가 설정되어 있지 않습니다!\n[오늘 시간 계산]을 하려면 먼저 주간 시간표(월~금)를 입력해 주셔야 합니다.');
                goToStep('stepWeekly');
                return;
            }

            document.getElementById('todayDayName').innerText = dayName;

            setTimeValue('todayWake', dayData.wake);
            setTimeValue('todayBed', dayData.bed);
            setTimeValue('todaySchoolEnd', dayData.schoolEnd);
            document.getElementById('todayAcademyHours').value = dayData.academy || 0;
            document.getElementById('todayExtraHours').value = dayData.extra || 0;

            goToStep('stepToday');
        }

        function timeToMinutes(timeStr) {
            if (!timeStr) return null;
            const [h, m] = timeStr.split(':').map(Number);
            return h * 60 + m;
        }

        function calculateTodayFreeTime() {
            const schoolEndVal = getTimeValue('todaySchoolEnd');
            const bedVal = getTimeValue('todayBed');

            if (!schoolEndVal || !bedVal) {
                alert('학교 끝나는 시간과 취침 시간을 먼저 모두 선택해 주세요!');
                return;
            }

            const schoolEndMin = timeToMinutes(schoolEndVal);
            let bedMin = timeToMinutes(bedVal);
            
            const academyHours = parseFloat(document.getElementById('todayAcademyHours').value);
            const extraHours = parseFloat(document.getElementById('todayExtraHours').value);
            const homeworkHours = parseFloat(document.getElementById('todayHomeworkHours').value);
            
            const commuteHours = parseFloat(document.getElementById('todayCommuteHours').value);
            const routineHours = parseFloat(document.getElementById('todayRoutineHours').value);

            if (bedMin < schoolEndMin) {
                bedMin += 24 * 60;
            }

            const totalAvailableMin = bedMin - schoolEndMin;
            const totalUsedMin = Math.round((academyHours + extraHours + homeworkHours + commuteHours + routineHours) * 60);

            let freeMin = totalAvailableMin - totalUsedMin;
            if (freeMin < 0) freeMin = 0;

            const freeH = Math.floor(freeMin / 60);
            const freeM = freeMin % 60;

            document.getElementById('resUserName').innerText = currentUser.name;
            document.getElementById('resFreeTime').innerText = `${freeH}시간 ${freeM}분`;
            document.getElementById('resSleepTimeNotice').innerText = `(이동, 샤워 등 씻는 시간을 공제한 순수 자유시간 / 목표 취침시간 ${bedVal} 기준)`;

            const summaryHtml = `오늘 분석된 순수 짬시간<br><span class="text-cyan-300 text-base font-black">${freeH}시간 ${freeM}분</span>`;
            currentUser.todaySummary = summaryHtml;
            saveUserData();

            let advice = "";
            if (freeMin >= 180) {
                advice = `🎉 이동시간 및 씻는 시간까지 제외하고도 ${freeH}시간 이상의 알짜배기 자유시간이 남습니다! 여유롭게 취미나 휴식을 즐겨보세요!`;
            } else if (freeMin >= 90) {
                advice = `👍 샤워 및 이동시간을 알차게 계산한 짬시간입니다! 25분 집중에 5분 휴식을 취하는 방식으로 숙제를 처리해보세요.`;
            } else if (freeMin > 0) {
                advice = `⚠️ 타이트한 하루입니다. 이동 및 준비시간이 꽤 소요되므로 딴짓하지 않고 핵심 숙제부터 빠르게 끝내는 것이 좋습니다.`;
            } else {
                advice = `🚨 스케줄 과부하 상태입니다! 학원, 이동시간, 샤워만 해도 시간이 부족할 수 있습니다. 숙제 분량을 조절하거나 취침 시간을 조금 뒤로 조율해 보세요.`;
            }

            document.getElementById('resAiAdvice').innerText = advice;
            goToStep('stepResult');
        }
    </script>
</body>
</html>
