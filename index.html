<!DOCTYPE html>
<html lang="vi" class="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DevShield 3D Ultimate - IT Study, Lofi Chill & 3D Quiz Arena</title>
  <!-- Tailwind CSS Engine -->
  <script src="https://www.gstatic.com/antigravity/web/dev/tailwindcss.min.js"></script>
  <style>
    :root {
      --bg-main: #0d1117;
      --card-main: #161b22;
      --border-main: #30363d;
      --text-main: #c9d1d9;
      --text-bright: #f0f6fc;
      --text-muted: #8b949e;
      --accent-blue: #58a6ff;
      --accent-green: #3fb950;
      --accent-purple: #bc8cff;
      --accent-amber: #d29922;
      --accent-red: #f85149;
    }
    body {
      background-color: var(--bg-main);
      color: var(--text-main);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      overflow-x: hidden;
    }
    .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace; }
    
    /* 3D Perspective Card Tilt */
    .card-3d-wrap {
      perspective: 1200px;
      transform-style: preserve-3d;
    }
    .card-3d {
      transition: transform 0.15s ease-out, box-shadow 0.15s ease-out;
      transform-style: preserve-3d;
      position: relative;
    }
    .card-glare {
      position: absolute;
      inset: 0;
      border-radius: 1.25rem;
      pointer-events: none;
      background: radial-gradient(circle at 50% 50%, rgba(255,255,255,0.2) 0%, transparent 65%);
      opacity: 0;
      transition: opacity 0.2s ease;
      mix-blend-mode: overlay;
    }

    /* 3D Flipping Quiz Card */
    .quiz-card-container {
      perspective: 1200px;
    }
    .quiz-card-inner {
      position: relative;
      width: 100%;
      min-height: 380px;
      transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
      transform-style: preserve-3d;
    }
    .quiz-card-inner.flipped {
      transform: rotateY(180deg);
    }
    .quiz-card-front, .quiz-card-back {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      border-radius: 1.25rem;
    }
    .quiz-card-back {
      transform: rotateY(180deg);
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar { width: 6px; height: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg-main); }
    ::-webkit-scrollbar-thumb { background: var(--border-main); border-radius: 4px; }
    ::-webkit-scrollbar-thumb:hover { background: #484f58; }

    /* Equalizer Bar Animation */
    @keyframes eqWave {
      0%, 100% { height: 4px; }
      50% { height: 16px; }
    }
    .eq-bar {
      width: 3px;
      background: #58a6ff;
      border-radius: 2px;
      animation: eqWave 0.8s ease-in-out infinite;
    }
    .eq-bar:nth-child(2) { animation-delay: 0.2s; }
    .eq-bar:nth-child(3) { animation-delay: 0.4s; }
    .eq-bar:nth-child(4) { animation-delay: 0.1s; }
    .eq-bar:nth-child(5) { animation-delay: 0.3s; }
  </style>
</head>
<body class="antialiased min-h-screen p-3 md:p-6 pb-28">

  <div class="max-w-6xl mx-auto space-y-5">

    <!-- ==================== HEADER WITH USER AUTH & LOFI QUICK DOCK ==================== -->
    <header class="flex flex-col lg:flex-row items-start lg:items-center justify-between gap-4 p-4 md:p-5 rounded-2xl bg-[#161b22] border border-[#30363d] shadow-xl">
      <div class="flex items-center gap-3">
        <div class="relative w-12 h-12 rounded-xl bg-indigo-500/15 border border-indigo-500/40 text-indigo-400 flex items-center justify-center font-bold text-xl mono shadow-inner overflow-hidden">
          &lt;/&gt;
          <div class="absolute inset-0 bg-gradient-to-tr from-indigo-500/20 to-transparent animate-pulse"></div>
        </div>
        <div>
          <div class="flex items-center gap-2">
            <h1 class="text-xl font-bold tracking-tight text-[#f0f6fc]">DevShield 3D</h1>
            <span class="px-2 py-0.5 text-xs font-semibold rounded-full bg-gradient-to-r from-indigo-500/30 to-purple-500/30 text-indigo-300 border border-indigo-500/40 mono">v2.5 Full Suite</span>
          </div>
          <p class="text-xs text-[#8b949e]">Time-blocking, Kỷ luật Vi mô, Trạm Nhạc Lofi & Đấu Trường 3D Quiz</p>
        </div>
      </div>

      <!-- Center & Right Controls -->
      <div class="flex flex-wrap items-center gap-2 w-full lg:w-auto justify-between lg:justify-end">
        
        <!-- Interactive Lofi Mini-Player -->
        <div class="flex items-center gap-2.5 px-3 py-1.5 rounded-xl border border-[#30363d] bg-[#0d1117]">
          <button id="btn-lofi-toggle" onclick="toggleLofiMusic()" class="p-1 rounded-lg hover:bg-[#161b22] text-sm text-[#f0f6fc] transition-all flex items-center gap-1.5">
            <span id="lofi-icon">▶️</span>
            <span class="text-xs font-semibold mono" id="lofi-label">Lofi Chill</span>
          </button>
          
          <div id="lofi-visualizer" class="hidden flex items-end gap-0.5 h-4 px-1">
            <div class="eq-bar"></div>
            <div class="eq-bar"></div>
            <div class="eq-bar"></div>
            <div class="eq-bar"></div>
            <div class="eq-bar"></div>
          </div>

          <span class="text-[11px] text-[#8b949e] mono hidden sm:inline" id="lofi-track-name">Midnight Code</span>
        </div>

        <!-- Mood Indicator (Burnout Sensor) -->
        <div class="flex items-center bg-[#0d1117] p-1 border border-[#30363d] rounded-xl text-xs">
          <span class="text-[#8b949e] px-2 font-medium">Não:</span>
          <button id="mood-fresh" onclick="setMood('fresh')" class="px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 bg-emerald-500/20 text-emerald-400 font-medium">
            🟢 Sung sức
          </button>
          <button id="mood-stressed" onclick="setMood('stressed')" class="px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 text-[#8b949e] hover:text-[#f0f6fc]">
            🟡 Căng thẳng
          </button>
          <button id="mood-burnout" onclick="setMood('burnout')" class="px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 text-[#8b949e] hover:text-[#f0f6fc]">
            🔴 Quá tải
          </button>
        </div>

        <!-- User Authentication & Profile Badge -->
        <div id="auth-section" class="flex items-center">
          <!-- Injected via JS (Logged in user or Sign in button) -->
        </div>

      </div>
    </header>

    <!-- BURNOUT EMERGENCY BANNER -->
    <div id="burnout-banner" class="hidden p-4 rounded-xl border transition-all duration-300"></div>

    <!-- ==================== MAIN NAVIGATION TABS ==================== -->
    <div class="flex items-center gap-2 border-b border-[#30363d] pb-2 overflow-x-auto">
      <button onclick="switchTab('tab-3d-visual')" id="btn-tab-3d-visual" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg bg-[#161b22] text-[#f0f6fc] border border-[#30363d] flex items-center gap-2 transition-all">
        <span class="text-base">🧊</span>
        <span>Phòng 3D & Thẻ Vinh Danh</span>
      </button>

      <button onclick="switchTab('tab-quiz-3d')" id="btn-tab-quiz-3d" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg text-[#8b949e] hover:text-[#f0f6fc] flex items-center gap-2 transition-all">
        <span class="text-base">🎮</span>
        <span>3D Quiz Ải Cứu Môn</span>
        <span class="px-1.5 py-0.2 text-[10px] rounded bg-purple-500/30 text-purple-300 mono font-bold">HOT</span>
      </button>

      <button onclick="switchTab('tab-lofi-station')" id="btn-tab-lofi-station" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg text-[#8b949e] hover:text-[#f0f6fc] flex items-center gap-2 transition-all">
        <span class="text-base">🎧</span>
        <span>Trạm Nhạc Lofi Chill</span>
      </button>

      <button onclick="switchTab('tab-timeblock')" id="btn-tab-timeblock" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg text-[#8b949e] hover:text-[#f0f6fc] flex items-center gap-2 transition-all">
        <svg class="w-4 h-4 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
        <span>Lịch Time-blocking</span>
      </button>

      <button onclick="switchTab('tab-habits')" id="btn-tab-habits" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg text-[#8b949e] hover:text-[#f0f6fc] flex items-center gap-2 transition-all">
        <svg class="w-4 h-4 text-emerald-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
        <span>Mỗi Ngày 1 Commit</span>
        <span class="px-1.5 py-0.2 text-[11px] rounded bg-emerald-500/20 text-emerald-400 mono font-bold" id="streak-badge">🔥 7 ngày</span>
      </button>

      <button onclick="switchTab('tab-mental')" id="btn-tab-mental" class="tab-btn px-4 py-2 text-xs md:text-sm font-semibold rounded-lg text-[#8b949e] hover:text-[#f0f6fc] flex items-center gap-2 transition-all">
        <svg class="w-4 h-4 text-amber-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/></svg>
        <span>Cứu Cánh & Chia Sẻ</span>
      </button>
    </div>

    <!-- ==================== TAB 0: 3D CYBER CORE & HOLOGRAPHIC CARD STUDIO ==================== -->
    <div id="tab-3d-visual" class="tab-pane space-y-6">
      
      <!-- Top Section: 3D Dev Core Visualizer -->
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-5 items-stretch">
        
        <!-- Left: Interactive 3D Canvas -->
        <div class="lg:col-span-7 bg-[#161b22] border border-[#30363d] rounded-2xl p-5 flex flex-col justify-between shadow-xl relative overflow-hidden">
          <div class="flex items-center justify-between mb-2 z-10">
            <div>
              <div class="flex items-center gap-2">
                <span class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-ping"></span>
                <h3 class="text-sm font-bold text-[#f0f6fc]">Mô Hình 3D: Dev Energy Core</h3>
              </div>
              <p class="text-xs text-[#8b949e]">Phản ánh mức độ chịu tải thần kinh của sinh viên thời gian thực.</p>
            </div>
            <div class="px-2.5 py-1 rounded-lg bg-[#0d1117] border border-[#30363d] mono text-[11px] text-[#8b949e]">
              <span id="canvas-fps">60 FPS</span> | Kéo chuột để xoay 3D
            </div>
          </div>

          <div class="relative w-full h-72 md:h-80 rounded-xl bg-[#0a0d12] border border-[#30363d] flex items-center justify-center overflow-hidden cursor-grab active:cursor-grabbing">
            <canvas id="core3dCanvas" class="w-full h-full"></canvas>
            
            <div class="absolute bottom-3 left-3 bg-[#161b22]/80 backdrop-blur-sm border border-[#30363d] p-2.5 rounded-xl text-[11px] mono space-y-1">
              <div class="flex items-center gap-2">
                <span class="text-[#8b949e]">Trạng thái:</span>
                <span id="core-status-text" class="text-emerald-400 font-bold">🟢 Bình Ổn - Tối Ưu</span>
              </div>
              <div class="flex items-center gap-2">
                <span class="text-[#8b949e]">Tần số xung:</span>
                <span id="core-freq" class="text-indigo-400">1.25 Hz</span>
              </div>
              <div class="flex items-center gap-2">
                <span class="text-[#8b949e]">Vệ tinh Commit:</span>
                <span class="text-amber-400">7 Satellites Active</span>
              </div>
            </div>

            <div class="absolute top-3 right-3 flex flex-col gap-1.5">
              <button onclick="reset3DCamera()" class="p-1.5 rounded-lg bg-[#161b22]/90 hover:bg-[#30363d] border border-[#30363d] text-xs text-[#c9d1d9]" title="Đặt lại góc nhìn 3D">
                🔄 Reset 3D
              </button>
            </div>
          </div>

          <div class="mt-3 flex items-center justify-between text-xs text-[#8b949e]">
            <span>💡 Mẹo: Nhấp và kéo chuột trên quả cầu để tương tác không gian 3 chiều.</span>
            <span class="mono text-indigo-400">WebGL Isometric 3D Projection</span>
          </div>
        </div>

        <!-- Right: Holographic 3D Tilt Badge Card & Customizer -->
        <div class="lg:col-span-5 bg-[#161b22] border border-[#30363d] rounded-2xl p-5 flex flex-col justify-between shadow-xl">
          <div>
            <div class="flex items-center justify-between mb-3">
              <h3 class="text-sm font-bold text-[#f0f6fc] flex items-center gap-2">
                <span>🎴</span> Thẻ Vinh Danh Kỷ Luật Dev (3D Tilt)
              </h3>
              <span class="text-[10px] px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-400 mono">Holographic</span>
            </div>
            <p class="text-xs text-[#8b949e] mb-4">Rê chuột lên thẻ để trải nghiệm hiệu ứng nghiêng 3D & khúc xạ ánh sáng đa chiều.</p>

            <div class="card-3d-wrap w-full flex justify-center py-2" id="cardContainer">
              <div id="hologramCard" class="card-3d w-full max-w-sm rounded-2xl p-5 border border-indigo-500/40 bg-gradient-to-br from-[#1c2333] via-[#161b22] to-[#0f141c] shadow-2xl relative overflow-hidden">
                <div class="card-glare" id="cardGlare"></div>
                
                <div class="flex items-center justify-between border-b border-indigo-500/20 pb-3 mb-4">
                  <div class="flex items-center gap-2">
                    <span class="text-indigo-400 font-bold mono text-sm">&lt;DevShield/Passport&gt;</span>
                  </div>
                  <span class="px-2 py-0.5 rounded text-[10px] mono font-bold bg-indigo-500/20 text-indigo-300 border border-indigo-500/30">RANK #01</span>
                </div>

                <div class="flex items-center gap-3.5 mb-4">
                  <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-indigo-500 via-purple-500 to-pink-500 p-0.5 shadow-lg">
                    <div class="w-full h-full bg-[#161b22] rounded-[10px] flex items-center justify-center text-2xl font-mono" id="card-avatar-display">
                      👨‍💻
                    </div>
                  </div>
                  <div>
                    <h4 class="font-bold text-base text-[#f0f6fc]" id="card-name">Dev Master: Khoa CNTT</h4>
                    <p class="text-xs text-indigo-400 mono" id="card-role">K68 Software Engineer</p>
                    <div class="flex items-center gap-2 mt-1">
                      <span class="text-[10px] px-1.5 py-0.2 rounded bg-emerald-500/20 text-emerald-300 mono" id="card-streak-tag">🔥 7 Days Streak</span>
                      <span class="text-[10px] px-1.5 py-0.2 rounded bg-purple-500/20 text-purple-300 mono">🛡️ Protected</span>
                    </div>
                  </div>
                </div>

                <div class="grid grid-cols-3 gap-2 p-2.5 rounded-xl bg-[#0d1117]/80 border border-[#30363d] mb-4 text-center mono">
                  <div>
                    <div class="text-[10px] text-[#8b949e]">Deep Work</div>
                    <div class="text-xs font-bold text-emerald-400">12.5 hrs</div>
                  </div>
                  <div class="border-x border-[#30363d]">
                    <div class="text-[10px] text-[#8b949e]">Drop Risk</div>
                    <div class="text-xs font-bold text-blue-400">0.0% (Safe)</div>
                  </div>
                  <div>
                    <div class="text-[10px] text-[#8b949e]">Commits</div>
                    <div class="text-xs font-bold text-amber-400">14 Clean</div>
                  </div>
                </div>

                <div class="flex items-center justify-between pt-2 border-t border-[#30363d]/60 text-[10px] mono text-[#8b949e]">
                  <span>VERIFIED CS STUDENT</span>
                  <span>ANTI-BURNOUT PROT-V2</span>
                </div>
              </div>
            </div>
          </div>

          <div class="pt-4 border-t border-[#30363d] space-y-2.5">
            <button onclick="exportCardAsImage()" class="w-full py-2.5 rounded-xl bg-gradient-to-r from-indigo-600 via-indigo-500 to-purple-600 hover:opacity-90 text-white font-bold text-xs flex items-center justify-center gap-2 shadow-lg transition-all">
              <span>📸</span>
              <span>Xuất Thẻ Hình Ảnh HD (.PNG Tải Về Ngay)</span>
            </button>
          </div>
        </div>

      </div>
    </div>

    <!-- ==================== TAB: 3D IT QUIZ ARENA (VƯỢT ẢI CỨU MÔN) ==================== -->
    <div id="tab-quiz-3d" class="tab-pane hidden space-y-6">
      
      <!-- Quiz HUD Stats -->
      <div class="p-4 bg-[#161b22] border border-[#30363d] rounded-2xl flex flex-wrap items-center justify-between gap-4">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-xl bg-purple-500/20 border border-purple-500/30 flex items-center justify-center text-xl">
            ⚔️
          </div>
          <div>
            <h2 class="text-sm font-bold text-[#f0f6fc]">Đấu Trường 3D: Ôn Tập Tránh Rớt Môn</h2>
            <p class="text-xs text-[#8b949e]">Vượt qua các câu hỏi bẫy thường gặp trong đề thi C++, DSA và OOP.</p>
          </div>
        </div>

        <!-- Scores & Lives -->
        <div class="flex items-center gap-4">
          <div class="flex items-center gap-1.5 px-3 py-1.5 rounded-xl bg-[#0d1117] border border-[#30363d] text-xs">
            <span class="text-[#8b949e]">Mạng sống:</span>
            <span id="quiz-lives" class="text-red-400 font-bold">❤️❤️❤️</span>
          </div>
          <div class="flex items-center gap-1.5 px-3 py-1.5 rounded-xl bg-[#0d1117] border border-[#30363d] text-xs mono">
            <span class="text-[#8b949e]">Điểm tích lũy:</span>
            <span id="quiz-score" class="text-emerald-400 font-bold">0 XP</span>
          </div>
          <button onclick="restartQuiz()" class="px-2.5 py-1.5 rounded-xl bg-[#0d1117] hover:bg-[#30363d] border border-[#30363d] text-xs text-[#c9d1d9]">
            🔄 Làm lại
          </button>
        </div>
      </div>

      <!-- 3D Flip Card Quiz Arena -->
      <div class="max-w-2xl mx-auto quiz-card-container">
        <div id="quizCardInner" class="quiz-card-inner">
          
          <!-- FRONT: QUESTION & OPTIONS -->
          <div class="quiz-card-front bg-[#161b22] border border-[#30363d] p-6 shadow-2xl flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between pb-3 border-b border-[#30363d]">
                <div class="flex items-center gap-2">
                  <span id="quiz-cat-badge" class="px-2.5 py-1 rounded-lg text-xs mono font-bold bg-blue-500/20 text-blue-400 border border-blue-500/30">C++ Pointers</span>
                  <span id="quiz-progress-text" class="text-xs text-[#8b949e] mono">Câu 1/4</span>
                </div>
                <span class="text-xs text-amber-400 mono font-bold">+25 XP nếu đúng</span>
              </div>

              <!-- Question Statement -->
              <div class="my-5">
                <h3 class="text-base font-bold text-[#f0f6fc] leading-relaxed" id="quiz-question-text">
                  Cho đoạn mã C++ sau: <code>int* p = new int(10); delete p; cout &lt;&lt; *p;</code>. Kết quả sẽ là gì?
                </h3>
              </div>

              <!-- 4 Options -->
              <div class="space-y-2.5" id="quiz-options-container">
                <!-- Injected via JS -->
              </div>
            </div>

            <div class="pt-4 border-t border-[#30363d] flex items-center justify-between text-xs text-[#8b949e]">
              <span>💡 Thẻ sẽ tự động lật 3D để giải thích bản chất khi bạn chọn.</span>
              <span class="mono text-indigo-400">3D Card Flip Motion</span>
            </div>
          </div>

          <!-- BACK: EXPLANATION & NEXT STEP -->
          <div class="quiz-card-back bg-gradient-to-br from-[#1c2333] via-[#161b22] to-[#0f141c] border border-indigo-500/40 p-6 shadow-2xl flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between pb-3 border-b border-[#30363d]">
                <span id="quiz-result-badge" class="px-3 py-1 rounded-lg text-xs font-bold mono bg-emerald-500/20 text-emerald-400">✓ CHÍNH XÁC (+25 XP)</span>
                <span class="text-xs text-[#8b949e]">Góc Giải Nghĩa Senior</span>
              </div>

              <div class="my-5 space-y-3">
                <h4 class="text-sm font-bold text-[#f0f6fc]" id="quiz-result-title">Bản chất vấn đề:</h4>
                <div class="p-4 rounded-xl bg-[#0d1117] border border-[#30363d] text-xs text-[#c9d1d9] leading-relaxed" id="quiz-explanation-text">
                  Đây là lỗi <strong>Dangling Pointer (Con trỏ lạc)</strong>. Sau khi gọi <code>delete p</code>, vùng nhớ đã được trả về cho hệ điều hành nhưng con trỏ <code>p</code> vẫn trỏ vào địa chỉ cũ. Việc truy xuất <code>*p</code> sẽ gây ra <em>Undefined Behavior</em> (có thể in giá trị rác hoặc sập chương trình Segmentation Fault).
                </div>
                <div class="p-3 rounded-lg bg-indigo-500/10 border border-indigo-500/20 text-[11px] text-indigo-300">
                  <strong>Mẹo chống thi lại:</strong> Luôn gán <code>p = nullptr;</code> ngay sau khi <code>delete p;</code> để tránh bug hiểm độc này!
                </div>
              </div>
            </div>

            <div class="pt-4 border-t border-[#30363d] flex items-center justify-between">
              <button onclick="flipQuizCardBack()" class="px-4 py-2 rounded-xl bg-[#0d1117] hover:bg-[#30363d] border border-[#30363d] text-xs text-[#c9d1d9]">
                ↩ Xem lại câu hỏi
              </button>
              <button onclick="nextQuizQuestion()" class="px-5 py-2 rounded-xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-xs flex items-center gap-1.5 shadow-lg">
                <span>Câu Tiếp Theo</span>
                <span>→</span>
              </button>
            </div>
          </div>

        </div>
      </div>

    </div>

    <!-- ==================== TAB: LOFI CHILL MUSIC STATION ==================== -->
    <div id="tab-lofi-station" class="tab-pane hidden space-y-6">
      
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-5">
        
        <!-- Left 7 Cols: Interactive Soundboard & Visualizer -->
        <div class="lg:col-span-7 p-6 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-5 shadow-xl">
          <div class="flex items-center justify-between">
            <div>
              <span class="px-2.5 py-0.5 rounded-full bg-blue-500/20 text-blue-400 text-[10px] mono font-bold">SYNTH ENGINE V1.2</span>
              <h2 class="text-base font-bold text-[#f0f6fc] mt-1">Trạm Âm Thanh Lofi Giảm Căng Thẳng (100% Offline)</h2>
              <p class="text-xs text-[#8b949e]">Được tổng hợp trực tiếp bằng Web Audio API, giúp sóng não thư thái khi debug code thâu đêm.</p>
            </div>
            <div class="text-3xl">☕</div>
          </div>

          <!-- Animated Audio Visualizer Display -->
          <div class="p-6 rounded-xl bg-[#0a0d12] border border-[#30363d] text-center space-y-3">
            <div class="flex items-center justify-center gap-1.5 h-16" id="lofi-big-eq">
              <span class="w-2 bg-indigo-500 rounded-full h-4 transition-all"></span>
              <span class="w-2 bg-purple-500 rounded-full h-8 transition-all"></span>
              <span class="w-2 bg-blue-500 rounded-full h-12 transition-all"></span>
              <span class="w-2 bg-emerald-500 rounded-full h-6 transition-all"></span>
              <span class="w-2 bg-amber-500 rounded-full h-10 transition-all"></span>
              <span class="w-2 bg-pink-500 rounded-full h-7 transition-all"></span>
            </div>
            <div class="text-sm font-bold text-[#f0f6fc]" id="now-playing-title">Midnight Code Session (Lo-Fi Chords & Vinyl)</div>
            <p class="text-xs text-[#8b949e]">Nhịp điệu 75 BPM • Chuỗi hợp âm Dm9 - G13 - Cmaj7 - Am9</p>
          </div>

          <!-- Main Player Controls -->
          <div class="flex items-center justify-center gap-4 py-2">
            <button onclick="prevLofiTrack()" class="p-2.5 rounded-xl bg-[#0d1117] hover:bg-[#30363d] border border-[#30363d] text-[#c9d1d9]">
              ⏮️
            </button>
            <button onclick="toggleLofiMusic()" id="btn-lofi-main-play" class="px-6 py-3 rounded-2xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-sm shadow-xl flex items-center gap-2">
              <span id="lofi-main-icon">▶ Bắt Đầu Nghe</span>
            </button>
            <button onclick="nextLofiTrack()" class="p-2.5 rounded-xl bg-[#0d1117] hover:bg-[#30363d] border border-[#30363d] text-[#c9d1d9]">
              ⏭️
            </button>
          </div>

          <!-- Ambient Sliders -->
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-3 border-t border-[#30363d] text-xs">
            <div class="space-y-1.5 p-3 rounded-xl bg-[#0d1117] border border-[#30363d]">
              <div class="flex items-center justify-between">
                <span class="text-[#8b949e]">🎹 Âm lượng Hợp Âm Lofi:</span>
                <span id="vol-synth-val" class="mono text-indigo-400">70%</span>
              </div>
              <input type="range" min="0" max="100" value="70" oninput="setSynthVolume(this.value)" class="w-full accent-indigo-500">
            </div>

            <div class="space-y-1.5 p-3 rounded-xl bg-[#0d1117] border border-[#30363d]">
              <div class="flex items-center justify-between">
                <span class="text-[#8b949e]">🌧️ Âm lượng Tiếng Mưa Rào:</span>
                <span id="vol-rain-val" class="mono text-blue-400">50%</span>
              </div>
              <input type="range" min="0" max="100" value="50" oninput="setRainVolume(this.value)" class="w-full accent-blue-500">
            </div>
          </div>
        </div>

        <!-- Right 5 Cols: Tracklist & Study Atmosphere Tips -->
        <div class="lg:col-span-5 p-6 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-4 shadow-xl">
          <h3 class="text-sm font-bold text-[#f0f6fc] flex items-center gap-2">
            <span>📻</span> Danh Sách Không Gian Âm Thanh
          </h3>

          <div class="space-y-2 text-xs">
            <div onclick="selectLofiTrack(0)" class="p-3 rounded-xl border border-indigo-500/40 bg-indigo-500/10 cursor-pointer hover:border-indigo-400 flex items-center justify-between">
              <div>
                <div class="font-bold text-[#f0f6fc]">01. Midnight Code Session</div>
                <div class="text-[11px] text-[#8b949e]">Hợp âm Rhodes ấm áp + đĩa than Vinyl</div>
              </div>
              <span class="mono text-indigo-400 font-bold">75 BPM</span>
            </div>

            <div onclick="selectLofiTrack(1)" class="p-3 rounded-xl border border-[#30363d] bg-[#0d1117] cursor-pointer hover:border-[#8b949e] flex items-center justify-between">
              <div>
                <div class="font-bold text-[#f0f6fc]">02. Rainy Dormitory 3AM</div>
                <div class="text-[11px] text-[#8b949e]">Mưa rơi ngoài cửa sổ ký túc xá + White Noise</div>
              </div>
              <span class="mono text-blue-400 font-bold">Ambient</span>
            </div>

            <div onclick="selectLofiTrack(2)" class="p-3 rounded-xl border border-[#30363d] bg-[#0d1117] cursor-pointer hover:border-[#8b949e] flex items-center justify-between">
              <div>
                <div class="font-bold text-[#f0f6fc]">03. Deep Flow DSA Marathon</div>
                <div class="text-[11px] text-[#8b949e]">Nhịp bass trầm đều đặn kích thích tập trung</div>
              </div>
              <span class="mono text-purple-400 font-bold">82 BPM</span>
            </div>
          </div>

          <div class="p-4 rounded-xl bg-[#0d1117] border border-[#30363d] space-y-1.5 text-xs text-[#8b949e]">
            <span class="text-amber-400 font-bold">💡 Cơ sở khoa học:</span>
            <p class="leading-relaxed">Âm nhạc Lo-fi với tần số lặp lại và tiếng mưa nền giúp não bộ phát ra sóng <strong>Alpha (8-12 Hz)</strong>, giảm 40% hormone cortisol gây căng thẳng khi đối mặt với deadline khó.</p>
          </div>
        </div>

      </div>

    </div>

    <!-- ==================== TAB 1: TIME-BLOCKING ==================== -->
    <div id="tab-timeblock" class="tab-pane hidden space-y-4">
      <div class="flex flex-col lg:flex-row items-start lg:items-center justify-between gap-3 p-4 bg-[#161b22] rounded-xl border border-[#30363d]">
        <div class="flex items-center gap-1.5 overflow-x-auto w-full lg:w-auto pb-1 lg:pb-0" id="days-bar"></div>
        <div class="flex flex-wrap items-center gap-3 text-xs">
          <span class="flex items-center gap-1.5"><span class="w-3 h-3 rounded bg-blue-500/30 border border-blue-400"></span> 🔵 Lên lớp</span>
          <span class="flex items-center gap-1.5"><span class="w-3 h-3 rounded bg-emerald-500/30 border border-emerald-400"></span> 🟢 Deep Code (90p)</span>
          <span class="flex items-center gap-1.5"><span class="w-3 h-3 rounded bg-amber-500/30 border border-amber-400"></span> 🟡 Bài tập lớn</span>
          <span class="flex items-center gap-1.5"><span class="w-3 h-3 rounded bg-purple-500/30 border border-purple-400"></span> 🟣 Nghỉ ngơi</span>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-5">
        <div class="lg:col-span-2 space-y-3" id="timeline-list"></div>

        <div class="space-y-4">
          <div class="p-4 md:p-5 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-3">
            <h3 class="text-sm font-bold text-[#f0f6fc] flex items-center justify-between">
              <span>+ Thêm Khối Thời Gian</span>
              <span class="text-xs text-[#8b949e] font-normal" id="selected-day-label">Thứ 2</span>
            </h3>

            <div class="space-y-2 text-xs">
              <div>
                <label class="block text-[#8b949e] mb-1">Tên môn / Tác vụ:</label>
                <input id="input-title" type="text" placeholder="Vd: Code Linked List C++ / Giải 1 bài DSA" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc] focus:outline-none focus:border-indigo-500">
              </div>

              <div class="grid grid-cols-2 gap-2">
                <div>
                  <label class="block text-[#8b949e] mb-1">Bắt đầu:</label>
                  <input id="input-start" type="time" value="14:00" class="w-full px-3 py-1.5 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
                </div>
                <div>
                  <label class="block text-[#8b949e] mb-1">Kết thúc:</label>
                  <input id="input-end" type="time" value="15:30" class="w-full px-3 py-1.5 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
                </div>
              </div>

              <div>
                <label class="block text-[#8b949e] mb-1">Phân loại khối:</label>
                <select id="input-cat" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
                  <option value="deep_code">🟢 Deep Code (Tự học / Luyện thuật toán 90p)</option>
                  <option value="lecture">🔵 Lên lớp giảng đường / Thực hành Lab</option>
                  <option value="project">🟡 Bài tập lớn / Đồ án môn học</option>
                  <option value="rest">🟣 Hồi phục / Giải lao / Thể thao</option>
                </select>
              </div>

              <div>
                <label class="block text-[#8b949e] mb-1">Ghi chú nhỏ:</label>
                <input id="input-desc" type="text" placeholder="Tự tay code không copy ChatGPT trước 30p" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
              </div>

              <button onclick="handleAddBlock()" class="w-full mt-2 py-2.5 rounded-lg bg-indigo-600 hover:bg-indigo-700 text-white font-semibold transition-all shadow-md">
                Chèn vào lịch
              </button>
            </div>
          </div>

          <div class="p-4 rounded-xl bg-[#161b22] border border-[#30363d] space-y-3">
            <div class="flex items-center justify-between text-xs">
              <span class="text-[#8b949e]">Tổng giờ Deep Code hôm nay:</span>
              <span class="mono font-bold text-emerald-400" id="deepwork-gauge">1.5h / 3h max</span>
            </div>
            <div class="w-full bg-[#0d1117] h-2.5 rounded-full overflow-hidden border border-[#30363d]">
              <div id="deepwork-bar" class="bg-emerald-500 h-full rounded-full transition-all duration-500" style="width: 50%;"></div>
            </div>
            <div class="p-3 rounded-lg bg-[#0d1117] border border-[#30363d] text-[11px] text-[#8b949e] leading-relaxed">
              <span class="text-amber-400 font-semibold">⚠️ Giới hạn an toàn:</span> Không xếp lịch ngồi code một mình quá 3.5 giờ/ngày. Khi não bão hòa, tỷ lệ sinh ra bug tăng 300%!
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ==================== TAB 2: HABITS & HEATMAP ==================== -->
    <div id="tab-habits" class="tab-pane hidden space-y-5">
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-5">
        <div class="lg:col-span-2 p-5 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-4">
          <div class="flex items-center justify-between">
            <div>
              <h2 class="text-base font-bold text-[#f0f6fc]">Kỷ Luật Vi Mô (Micro-Habit Checklist)</h2>
              <p class="text-xs text-[#8b949e]">Chỉ cần hoàn thành tối thiểu 1 nhiệm vụ nhỏ mỗi ngày để duy trì thói quen.</p>
            </div>
            <span class="px-2.5 py-1 text-xs rounded-full bg-indigo-500/10 text-indigo-400 border border-indigo-500/30 mono" id="habits-counter">
              1/3 hoàn thành
            </span>
          </div>

          <div class="space-y-3" id="habits-list"></div>

          <div class="p-4 rounded-xl bg-[#0d1117] border border-[#30363d] flex flex-col sm:flex-row items-start sm:items-center justify-between gap-3">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-xl bg-purple-500/10 border border-purple-500/30 flex items-center justify-center text-xl">🛡️</div>
              <div>
                <h4 class="text-xs font-bold text-[#f0f6fc]">Bình Cứu Sinh (Streak Freeze)</h4>
                <p class="text-[11px] text-[#8b949e]">Bảo lưu chuỗi khi bạn ốm, thi học kỳ hoặc kiệt sức (Còn <span id="shield-count" class="text-emerald-400 font-bold">2</span> lần tháng này).</p>
              </div>
            </div>
            <button onclick="useShield()" class="px-3 py-1.5 text-xs font-medium rounded-lg bg-[#161b22] hover:bg-[#30363d] border border-[#30363d] text-[#f0f6fc] transition-all whitespace-nowrap">
              Kích hoạt hôm nay
            </button>
          </div>
        </div>

        <div class="p-5 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-4">
          <div class="flex items-center justify-between">
            <h3 class="text-sm font-bold text-[#f0f6fc]">Heatmap Coding 35 Ngày</h3>
            <span class="mono text-xs font-bold text-emerald-400" id="heatmap-streak-tag">🔥 7 Ngày liên tiếp</span>
          </div>
          <p class="text-xs text-[#8b949e]">Visual Dopamine tương tự GitHub. Mỗi ô xanh đại diện cho 1 ngày bạn không buông xuôi.</p>
          <div class="grid grid-cols-7 gap-1.5 p-3 rounded-xl bg-[#0d1117] border border-[#30363d]" id="heatmap-container"></div>
          <div class="flex items-center justify-between text-[11px] text-[#8b949e] pt-1">
            <span>Ít hoạt động</span>
            <div class="flex gap-1 items-center">
              <span class="w-3 h-3 rounded-sm bg-[#161b22] border border-[#30363d]"></span>
              <span class="w-3 h-3 rounded-sm bg-emerald-900/60"></span>
              <span class="w-3 h-3 rounded-sm bg-emerald-600"></span>
              <span class="w-3 h-3 rounded-sm bg-emerald-400"></span>
            </div>
            <span>Tập trung cao</span>
          </div>
        </div>
      </div>
    </div>

    <!-- ==================== TAB 3: MENTAL SAFE SPACE & COMMUNITY SHARING ==================== -->
    <div id="tab-mental" class="tab-pane hidden space-y-5">
      
      <!-- Top Action Bar with "Chia Sẻ Kinh Nghiệm" Button -->
      <div class="p-5 rounded-2xl bg-[#161b22] border border-[#30363d] flex flex-col md:flex-row items-start md:items-center justify-between gap-4">
        <div>
          <h2 class="text-base font-bold text-[#f0f6fc] flex items-center gap-2">
            <span>🧠</span> Cẩm Nang Sống Sót & Diễn Đàn Chia Sẻ Sinh Viên IT
          </h2>
          <p class="text-xs text-[#8b949e] mt-1">Nơi sinh viên chia sẻ trải nghiệm thực tế: nợ môn, gánh đồ án, vượt qua khủng hoảng.</p>
        </div>

        <button onclick="openShareExperienceModal()" class="px-4 py-2 rounded-xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-xs flex items-center gap-2 shadow-lg transition-all whitespace-nowrap">
          <span>✍️</span>
          <span>+ Đăng Kinh Nghiệm Của Bạn</span>
        </button>
      </div>

      <!-- Filter Tags -->
      <div class="flex flex-wrap gap-1.5 text-xs">
        <button onclick="filterAdvice('all')" class="px-2.5 py-1 rounded-lg bg-indigo-600 text-white font-medium adv-filter">Tất cả</button>
        <button onclick="filterAdvice('drop')" class="px-2.5 py-1 rounded-lg bg-[#0d1117] text-[#8b949e] border border-[#30363d] hover:text-[#f0f6fc] adv-filter">Chống Drop Môn</button>
        <button onclick="filterAdvice('study')" class="px-2.5 py-1 rounded-lg bg-[#0d1117] text-[#8b949e] border border-[#30363d] hover:text-[#f0f6fc] adv-filter">Cách Học Code</button>
        <button onclick="filterAdvice('team')" class="px-2.5 py-1 rounded-lg bg-[#0d1117] text-[#8b949e] border border-[#30363d] hover:text-[#f0f6fc] adv-filter">Bài Tập Lớn</button>
        <button onclick="filterAdvice('community')" class="px-2.5 py-1 rounded-lg bg-[#0d1117] text-[#8b949e] border border-[#30363d] hover:text-[#f0f6fc] adv-filter">Bài Đăng Cộng Đồng</button>
      </div>

      <!-- Advice & Experiences Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4" id="advice-grid">
        <!-- Injected via JS -->
      </div>
    </div>

  </div>

  <!-- ==================== USER LOGIN / PROFILE MODAL ==================== -->
  <div id="login-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4" onclick="closeLoginModal(event)">
    <div class="bg-[#161b22] border border-[#30363d] rounded-2xl max-w-md w-full p-6 shadow-2xl space-y-4" onclick="event.stopPropagation()">
      <div class="flex items-center justify-between border-b border-[#30363d] pb-3">
        <h3 class="text-base font-bold text-[#f0f6fc] flex items-center gap-2">
          <span>👨‍💻</span> Thiết Lập Hồ Sơ Lập Trình Viên
        </h3>
        <button onclick="closeLoginModal()" class="text-[#8b949e] hover:text-[#f0f6fc]">✕</button>
      </div>

      <div class="space-y-3 text-xs">
        <div>
          <label class="block text-[#8b949e] mb-1">Họ tên / Nickname Dev:</label>
          <input id="auth-input-name" type="text" placeholder="Vd: Nguyễn Văn A" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
        </div>
        <div>
          <label class="block text-[#8b949e] mb-1">Trường & Chuyên ngành:</label>
          <input id="auth-input-role" type="text" placeholder="Vd: K68 Kỹ Thuật Phần Mềm - ĐHBK" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
        </div>
        <div>
          <label class="block text-[#8b949e] mb-1">Biểu tượng Avatar:</label>
          <div class="flex gap-2">
            <button onclick="selectAvatar('👨‍💻')" class="avatar-opt p-2 rounded-lg bg-[#0d1117] border border-indigo-500 text-lg">👨‍💻</button>
            <button onclick="selectAvatar('👩‍💻')" class="avatar-opt p-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-lg">👩‍💻</button>
            <button onclick="selectAvatar('🥷')" class="avatar-opt p-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-lg">🥷</button>
            <button onclick="selectAvatar('🚀')" class="avatar-opt p-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-lg">🚀</button>
            <button onclick="selectAvatar('🤖')" class="avatar-opt p-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-lg">🤖</button>
          </div>
        </div>

        <div class="pt-2">
          <button onclick="handleLoginSubmit()" class="w-full py-2.5 rounded-xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-xs shadow-lg transition-all">
            Lưu & Đăng Nhập Hệ Thống
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- ==================== SHARE EXPERIENCE MODAL ==================== -->
  <div id="share-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4" onclick="closeShareModal(event)">
    <div class="bg-[#161b22] border border-[#30363d] rounded-2xl max-w-lg w-full p-6 shadow-2xl space-y-4" onclick="event.stopPropagation()">
      <div class="flex items-center justify-between border-b border-[#30363d] pb-3">
        <h3 class="text-base font-bold text-[#f0f6fc] flex items-center gap-2">
          <span>✍️</span> Đăng Bài Chia Sẻ Kinh Nghiệm Cứu Môn
        </h3>
        <button onclick="closeShareModal()" class="text-[#8b949e] hover:text-[#f0f6fc]">✕</button>
      </div>

      <div class="space-y-3 text-xs">
        <div>
          <label class="block text-[#8b949e] mb-1">Tiêu đề chia sẻ:</label>
          <input id="post-title" type="text" placeholder="Vd: Kinh nghiệm qua môn Lập trình mạng khi không hiểu socket..." class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
        </div>
        <div>
          <label class="block text-[#8b949e] mb-1">Chủ đề:</label>
          <select id="post-cat" class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc]">
            <option value="drop">Chống Drop Môn / Gỡ nợ môn</option>
            <option value="study">Chiến thuật tự học code</option>
            <option value="team">Kinh nghiệm làm bài tập lớn</option>
          </select>
        </div>
        <div>
          <label class="block text-[#8b949e] mb-1">Nội dung chi tiết (Đúc kết xương máu):</label>
          <textarea id="post-content" rows="4" placeholder="Kể lại bế tắc bạn gặp phải và cách bạn giải quyết nó..." class="w-full px-3 py-2 rounded-lg bg-[#0d1117] border border-[#30363d] text-[#f0f6fc] leading-relaxed"></textarea>
        </div>

        <button onclick="submitNewExperience()" class="w-full py-2.5 rounded-xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-xs shadow-lg transition-all">
          Đăng Lên Diễn Đàn Sinh Viên
        </button>
      </div>
    </div>
  </div>

  <!-- JAVASCRIPT SYSTEM ENGINE -->
  <script>
    const STORAGE_KEY = 'DEVSHIELD_FULL_V25';
    
    // Default system state
    const defaultData = {
      currentUser: {
        isAuth: false,
        name: 'Tân Sinh Viên IT',
        role: 'K68 Computer Science',
        avatar: '👨‍💻'
      },
      selectedDay: 1,
      streak: 7,
      shieldCount: 2,
      mood: 'fresh',
      quizXP: 0,
      quizLives: 3,
      currentQuizIndex: 0,
      timeBlocks: [
        { id: 'b1', day: 1, title: 'Cấu trúc Dữ liệu & Giải thuật (DSA)', cat: 'lecture', start: '07:30', end: '11:00', done: false, desc: 'Lý thuyết Con trỏ & Linked List.' },
        { id: 'b2', day: 1, title: 'Nghỉ trưa & Hồi phục mắt', cat: 'rest', start: '11:30', end: '13:30', done: true, desc: 'Ăn cơm, đi dạo, không lướt mạng quá 15 phút.' },
        { id: 'b3', day: 1, title: 'Deep Work: Tự code Linked List bằng C++', cat: 'deep_code', start: '14:00', end: '15:30', done: false, desc: 'Implement insertAtHead & deleteNode.' },
        { id: 'b4', day: 1, title: 'Bài Tập Lớn: Thiết Kế Database (Nhóm 4)', cat: 'project', start: '16:00', end: '18:00', done: false, desc: 'Vẽ sơ đồ ERD, chốt schema.' }
      ],
      habits: [
        { id: 1, title: 'Push ít nhất 1 commit sạch lên GitHub', tag: 'Git Habit', done: true, desc: 'Thêm README, fix typo hoặc comment code.' },
        { id: 2, title: 'Giải 1 bài thuật toán nhỏ (LeetCode Easy)', tag: 'DSA', done: false, desc: 'Vẽ tay logic trên giấy trước khi bắt đầu gõ code.' },
        { id: 3, title: 'Refactor 1 hàm trong đồ án nhóm', tag: 'Clean Code', done: false, desc: 'Đặt lại tên biến có nghĩa, xóa các log thừa.' }
      ],
      adviceList: [
        { id: 1, cat: 'drop', title: 'Trượt môn Lập trình C/C++ có phải dấu chấm hết?', author: 'Anh Khoa (Senior SE @ TechCorp)', likes: 42, text: 'Hơn 40% sinh viên từng nợ môn này. Hãy soi từng biến với Debugger thay vì nản lòng nộp đơn bỏ học!' },
        { id: 2, cat: 'study', title: 'Làm sao thoát khỏi Tutorial Hell?', author: 'Chị Mai (Tech Lead)', likes: 38, text: 'Áp dụng quy tắc 1:1: Xem video 20 phút thì phải tắt video đi, tự mở project trống và gõ lại chức năng đó.' },
        { id: 3, cat: 'team', title: 'Đồng đội lặn mất tăm lúc sắp nộp bài tập lớn?', author: 'Anh Duy (Full-stack Dev)', likes: 51, text: 'Phân chia Git branch và Pull Request rõ ràng ngay từ đầu. Ai lặn quá 5 ngày thì báo giảng viên trước 2 tuần.' }
      ]
    };

    let appData = loadData();
    function loadData() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (raw) return JSON.parse(raw);
      } catch (e) {}
      return defaultData;
    }
    function saveData() {
      try { localStorage.setItem(STORAGE_KEY, JSON.stringify(appData)); } catch (e) {}
    }

    // --- TAB SWITCHER ---
    function switchTab(tabId) {
      document.querySelectorAll('.tab-pane').forEach(el => el.classList.add('hidden'));
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.classList.remove('bg-[#161b22]', 'text-[#f0f6fc]', 'border', 'border-[#30363d]');
        btn.classList.add('text-[#8b949e]');
      });
      const target = document.getElementById(tabId);
      if (target) target.classList.remove('hidden');
      const btn = document.getElementById('btn-' + tabId);
      if (btn) {
        btn.classList.add('bg-[#161b22]', 'text-[#f0f6fc]', 'border', 'border-[#30363d]');
        btn.classList.remove('text-[#8b949e]');
      }
    }

    // --- USER AUTHENTICATION & PROFILE LOGIC ---
    let selectedAvatarChar = '👨‍💻';

    function renderAuthBar() {
      const authDiv = document.getElementById('auth-section');
      if (appData.currentUser.isAuth) {
        authDiv.innerHTML = `
          <div class="flex items-center gap-2 p-1 pl-2 pr-3 rounded-xl bg-[#0d1117] border border-indigo-500/40">
            <span class="text-lg">${appData.currentUser.avatar}</span>
            <div class="text-left hidden sm:block">
              <div class="text-xs font-bold text-[#f0f6fc] leading-tight">${appData.currentUser.name}</div>
              <div class="text-[10px] text-indigo-400 mono leading-tight">${appData.currentUser.role}</div>
            </div>
            <button onclick="handleLogout()" class="text-xs text-[#8b949e] hover:text-red-400 ml-1.5" title="Đăng xuất">✕</button>
          </div>
        `;
      } else {
        authDiv.innerHTML = `
          <button onclick="openLoginModal()" class="px-3 py-1.5 rounded-xl bg-indigo-600 hover:bg-indigo-500 text-white font-bold text-xs flex items-center gap-1.5 shadow-md">
            <span>👤</span>
            <span>Đăng Nhập</span>
          </button>
        `;
      }

      // Sync with 3D Hologram Card
      const cardName = document.getElementById('card-name');
      const cardRole = document.getElementById('card-role');
      const cardAvatar = document.getElementById('card-avatar-display');
      if (cardName) cardName.innerText = appData.currentUser.name;
      if (cardRole) cardRole.innerText = appData.currentUser.role;
      if (cardAvatar) cardAvatar.innerText = appData.currentUser.avatar;
    }

    function openLoginModal() {
      document.getElementById('auth-input-name').value = appData.currentUser.name || '';
      document.getElementById('auth-input-role').value = appData.currentUser.role || '';
      document.getElementById('login-modal').classList.remove('hidden');
    }
    function closeLoginModal() {
      document.getElementById('login-modal').classList.add('hidden');
    }

    function selectAvatar(char) {
      selectedAvatarChar = char;
      document.querySelectorAll('.avatar-opt').forEach(b => {
        b.classList.remove('border-indigo-500');
        b.classList.add('border-[#30363d]');
      });
      event.target.classList.remove('border-[#30363d]');
      event.target.classList.add('border-indigo-500');
    }

    function handleLoginSubmit() {
      const name = document.getElementById('auth-input-name').value.trim() || 'Sinh Viên IT';
      const role = document.getElementById('auth-input-role').value.trim() || 'Software Engineer';
      appData.currentUser = {
        isAuth: true,
        name,
        role,
        avatar: selectedAvatarChar
      };
      saveData();
      renderAuthBar();
      closeLoginModal();
    }

    function handleLogout() {
      appData.currentUser.isAuth = false;
      saveData();
      renderAuthBar();
    }

    // --- COMMUNITY ADVICE & SHARING LOGIC ---
    function renderAdvice(category = 'all') {
      const container = document.getElementById('advice-grid');
      if (!container) return;
      container.innerHTML = '';

      const filtered = (category === 'all') 
        ? appData.adviceList 
        : (category === 'community' 
            ? appData.adviceList.filter(a => a.isCommunity)
            : appData.adviceList.filter(a => a.cat === category));

      filtered.forEach(a => {
        const card = document.createElement('div');
        card.className = "p-5 rounded-2xl bg-[#161b22] border border-[#30363d] space-y-2 hover:border-indigo-500/50 transition-all flex flex-col justify-between";
        card.innerHTML = `
          <div class="space-y-2">
            <div class="flex items-center justify-between">
              <span class="px-2 py-0.5 rounded text-[11px] mono bg-indigo-500/10 text-indigo-400 border border-indigo-500/20">${a.author}</span>
              <span class="text-[11px] text-[#8b949e] uppercase mono">${a.cat}</span>
            </div>
            <h3 class="text-sm font-bold text-[#f0f6fc]">${a.title}</h3>
            <p class="text-xs text-[#8b949e] leading-relaxed">${a.text}</p>
          </div>
          <div class="pt-3 border-t border-[#30363d]/60 flex items-center justify-between text-xs">
            <button onclick="likeAdvice(${a.id})" class="px-2.5 py-1 rounded-lg bg-[#0d1117] hover:bg-[#30363d] text-[#c9d1d9] flex items-center gap-1.5 transition-all">
              <span>❤️</span>
              <span id="likes-${a.id}">${a.likes || 12}</span> Cứu Mạng
            </button>
            <span class="text-[11px] text-[#8b949e]">Chia sẻ thực chiến</span>
          </div>
        `;
        container.appendChild(card);
      });
    }

    function filterAdvice(cat) {
      document.querySelectorAll('.adv-filter').forEach(b => {
        b.className = 'px-2.5 py-1 rounded-lg bg-[#0d1117] text-[#8b949e] border border-[#30363d] hover:text-[#f0f6fc] adv-filter';
      });
      event.target.className = 'px-2.5 py-1 rounded-lg bg-indigo-600 text-white font-medium adv-filter';
      renderAdvice(cat);
    }

    function likeAdvice(id) {
      const item = appData.adviceList.find(a => a.id === id);
      if (item) {
        item.likes = (item.likes || 12) + 1;
        saveData();
        const countSpan = document.getElementById(`likes-${id}`);
        if (countSpan) countSpan.innerText = item.likes;
      }
    }

    function openShareExperienceModal() {
      if (!appData.currentUser.isAuth) {
        alert("Vui lòng đăng nhập hồ sơ lập trình viên trước khi chia sẻ kinh nghiệm!");
        openLoginModal();
        return;
      }
      document.getElementById('share-modal').classList.remove('hidden');
    }
    function closeShareModal() {
      document.getElementById('share-modal').classList.add('hidden');
    }

    function submitNewExperience() {
      const title = document.getElementById('post-title').value.trim();
      const cat = document.getElementById('post-cat').value;
      const text = document.getElementById('post-content').value.trim();

      if (!title || !text) {
        alert("Vui lòng nhập đầy đủ tiêu đề và nội dung kinh nghiệm!");
        return;
      }

      appData.adviceList.unshift({
        id: Date.now(),
        cat,
        title,
        author: `${appData.currentUser.avatar} ${appData.currentUser.name}`,
        likes: 1,
        text,
        isCommunity: true
      });

      saveData();
      renderAdvice();
      closeShareModal();
      document.getElementById('post-title').value = '';
      document.getElementById('post-content').value = '';
      alert("🎉 Đã đăng bài chia sẻ thành công lên cộng đồng sinh viên!");
    }

    // --- 3D IT QUIZ ARENA SYSTEM ---
    const quizQuestions = [
      {
        cat: 'C++ Pointers',
        question: 'Cho đoạn mã C++ sau: int* p = new int(10); delete p; cout << *p; Kết quả gì sẽ xảy ra?',
        options: [
          'Chương trình luôn in ra số 10',
          'Undefined Behavior (Con trỏ lạc Dangling Pointer)',
          'Lỗi cú pháp (Compile Error) khi biên dịch',
          'Tự động in ra giá trị 0'
        ],
        correct: 1,
        explanation: 'Đây là lỗi Dangling Pointer! Sau delete p, vùng nhớ đã bị giải phóng nhưng p vẫn trỏ về địa chỉ đó. Truy xuất *p sẽ gây Undefined Behavior hoặc Crash ứng dụng (Segmentation Fault).'
      },
      {
        cat: 'DSA Complexity',
        question: 'Trong cây nhị phân tìm kiếm (BST), trường hợp xấu nhất (Worst-case) độ phức tạp tìm kiếm là bao nhiêu?',
        options: [
          'O(log N)',
          'O(1)',
          'O(N) - khi cây bị suy biến thành danh sách liên kết',
          'O(N log N)'
        ],
        correct: 2,
        explanation: 'Khi các phần tử được chèn theo thứ tự tăng dần hoặc giảm dần, BST sẽ suy biến thành Linked List, khiến độ sâu là N và chi phí tìm kiếm tồi tệ nhất là O(N).'
      },
      {
        cat: 'Git & Teamwork',
        question: 'Lệnh Git nào sau đây hủy bỏ các thay đổi ở thư mục làm việc (Working Tree) chưa staged?',
        options: [
          'git restore .',
          'git commit --amend',
          'git push -f origin main',
          'git branch -D'
        ],
        correct: 0,
        explanation: 'git restore . (hoặc git checkout -- .) sẽ hoàn nguyên các file chưa đưa vào Staging Area về trạng thái commit gần nhất an toàn.'
      },
      {
        cat: 'OOP Principles',
        question: 'Nguyên lý Liskov (L trong SOLID) quy định điều gì quan trọng nhất?',
        options: [
          'Một class chỉ được làm đúng một nhiệm vụ duy nhất',
          'Class con phải thay thế được cho class cha mà không làm hỏng tính đúng đắn',
          'Nên phụ thuộc vào class cụ thể thay vì interface',
          'Không được phép kế thừa quá 2 cấp'
        ],
        correct: 1,
        explanation: 'Liskov Substitution Principle (LSP): Mọi đối tượng của lớp cha đều có thể được thay thế bằng đối tượng của lớp con mà không làm thay đổi tính đúng đắn của chương trình.'
      }
    ];

    let currentQIndex = 0;
    let quizScore = 0;
    let quizLives = 3;

    function renderQuiz() {
      const q = quizQuestions[currentQIndex];
      document.getElementById('quiz-cat-badge').innerText = q.cat;
      document.getElementById('quiz-progress-text').innerText = `Câu ${currentQIndex + 1}/${quizQuestions.length}`;
      document.getElementById('quiz-question-text').innerHTML = q.question;

      const optsContainer = document.getElementById('quiz-options-container');
      optsContainer.innerHTML = '';

      q.options.forEach((opt, idx) => {
        const btn = document.createElement('button');
        btn.className = "w-full text-left p-3.5 rounded-xl border border-[#30363d] bg-[#0d1117] hover:border-indigo-500/80 hover:bg-[#161b22] text-xs text-[#f0f6fc] transition-all flex items-center justify-between";
        btn.innerHTML = `
          <span>${String.fromCharCode(65 + idx)}. ${opt}</span>
          <span class="mono text-[#8b949e]">Chọn</span>
        `;
        btn.onclick = () => selectQuizOption(idx);
        optsContainer.appendChild(btn);
      });

      document.getElementById('quiz-score').innerText = `${quizScore} XP`;
      let hearts = '';
      for (let i = 0; i < quizLives; i++) hearts += '❤️';
      document.getElementById('quiz-lives').innerText = hearts || '💀 Hết mạng';
    }

    function selectQuizOption(choiceIdx) {
      const q = quizQuestions[currentQIndex];
      const isCorrect = (choiceIdx === q.correct);
      const inner = document.getElementById('quizCardInner');
      const badge = document.getElementById('quiz-result-badge');
      const title = document.getElementById('quiz-result-title');
      const expl = document.getElementById('quiz-explanation-text');

      if (isCorrect) {
        quizScore += 25;
        badge.className = "px-3 py-1 rounded-lg text-xs font-bold mono bg-emerald-500/20 text-emerald-400";
        badge.innerText = "✓ CHÍNH XÁC (+25 XP)";
        title.innerText = "Tuyệt vời! Kiến thức rất vững:";
      } else {
        quizLives = Math.max(0, quizLives - 1);
        badge.className = "px-3 py-1 rounded-lg text-xs font-bold mono bg-red-500/20 text-red-400";
        badge.innerText = "✕ CHƯA CHÍNH XÁC (-1 TIM)";
        title.innerText = "Cảnh báo bẫy thi cử:";
      }

      expl.innerHTML = q.explanation;
      inner.classList.add('flipped');
    }

    function flipQuizCardBack() {
      document.getElementById('quizCardInner').classList.remove('flipped');
    }

    function nextQuizQuestion() {
      document.getElementById('quizCardInner').classList.remove('flipped');
      currentQIndex = (currentQIndex + 1) % quizQuestions.length;
      setTimeout(renderQuiz, 250);
    }

    function restartQuiz() {
      currentQIndex = 0;
      quizScore = 0;
      quizLives = 3;
      flipQuizCardBack();
      renderQuiz();
    }

    // --- LOFI MUSIC SYNTHESIZER ENGINE (WEB AUDIO API - 100% OFFLINE) ---
    let audioCtx = null;
    let isLofiPlaying = false;
    let lofiTrackIndex = 0;
    let chordTimer = null;
    let rainSource = null;
    let rainGain = null;
    let synthGain = null;

    const lofiChords = [
      [293.66, 349.23, 440.0, 523.25], // Dm9
      [392.0, 493.88, 587.33, 659.25], // G13
      [261.63, 329.63, 392.0, 493.88], // Cmaj7
      [220.0, 261.63, 329.63, 392.0]   // Am9
    ];
    let chordIdx = 0;

    function initAudioContext() {
      if (!audioCtx) {
        audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        
        synthGain = audioCtx.createGain();
        synthGain.gain.value = 0.15;
        synthGain.connect(audioCtx.destination);

        // Rain noise buffer
        const bufferSize = audioCtx.sampleRate * 2;
        const buffer = audioCtx.createBuffer(1, bufferSize, audioCtx.sampleRate);
        const data = buffer.getChannelData(0);
        let lastOut = 0.0;
        for (let i = 0; i < bufferSize; i++) {
          const white = Math.random() * 2 - 1;
          data[i] = (lastOut + (0.02 * white)) / 1.02;
          lastOut = data[i];
          data[i] *= 3.0;
        }

        rainSource = audioCtx.createBufferSource();
        rainSource.buffer = buffer;
        rainSource.loop = true;

        const rainFilter = audioCtx.createBiquadFilter();
        rainFilter.type = 'lowpass';
        rainFilter.frequency.value = 750;

        rainGain = audioCtx.createGain();
        rainGain.gain.value = 0.04;

        rainSource.connect(rainFilter);
        rainFilter.connect(rainGain);
        rainGain.connect(audioCtx.destination);
        rainSource.start();
      }
    }

    function playChord() {
      if (!isLofiPlaying || !audioCtx) return;
      const notes = lofiChords[chordIdx % lofiChords.length];
      chordIdx++;

      notes.forEach((freq, i) => {
        const osc = audioCtx.createOscillator();
        const noteGain = audioCtx.createGain();
        const filter = audioCtx.createBiquadFilter();

        osc.type = 'triangle';
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime);

        filter.type = 'lowpass';
        filter.frequency.setValueAtTime(600, audioCtx.currentTime);

        const now = audioCtx.currentTime;
        noteGain.gain.setValueAtTime(0.001, now);
        noteGain.gain.linearRampToValueAtTime(0.08 / (i + 1), now + 0.3);
        noteGain.gain.exponentialRampToValueAtTime(0.001, now + 2.8);

        osc.connect(filter);
        filter.connect(noteGain);
        noteGain.connect(synthGain);

        osc.start(now);
        osc.stop(now + 2.9);
      });

      chordTimer = setTimeout(playChord, 2600);
    }

    function toggleLofiMusic() {
      initAudioContext();
      if (audioCtx.state === 'suspended') audioCtx.resume();

      isLofiPlaying = !isLofiPlaying;

      const mainBtn = document.getElementById('lofi-main-icon');
      const headerIcon = document.getElementById('lofi-icon');
      const vis = document.getElementById('lofi-visualizer');

      if (isLofiPlaying) {
        if (mainBtn) mainBtn.innerText = '⏸️ Đang Phát (Tạm Dừng)';
        if (headerIcon) headerIcon.innerText = '⏸️';
        if (vis) vis.classList.remove('hidden');
        playChord();
      } else {
        if (mainBtn) mainBtn.innerText = '▶ Bắt Đầu Nghe';
        if (headerIcon) headerIcon.innerText = '▶️';
        if (vis) vis.classList.add('hidden');
        if (chordTimer) clearTimeout(chordTimer);
      }
    }

    function setSynthVolume(val) {
      document.getElementById('vol-synth-val').innerText = `${val}%`;
      if (synthGain) synthGain.gain.value = (val / 100) * 0.25;
    }
    function setRainVolume(val) {
      document.getElementById('vol-rain-val').innerText = `${val}%`;
      if (rainGain) rainGain.gain.value = (val / 100) * 0.08;
    }

    function selectLofiTrack(idx) {
      lofiTrackIndex = idx;
      const titles = [
        'Midnight Code Session (Lo-Fi Chords & Vinyl)',
        'Rainy Dormitory 3AM (Heavy Rain & White Noise)',
        'Deep Flow DSA Marathon (82 BPM Focus Pulse)'
      ];
      document.getElementById('now-playing-title').innerText = titles[idx];
      document.getElementById('lofi-track-name').innerText = titles[idx].split('(')[0];
      if (!isLofiPlaying) toggleLofiMusic();
    }
    function nextLofiTrack() { selectLofiTrack((lofiTrackIndex + 1) % 3); }
    function prevLofiTrack() { selectLofiTrack((lofiTrackIndex + 2) % 3); }

    // --- 3D CANVAS WEBGL ENGINE ---
    const canvas = document.getElementById('core3dCanvas');
    const ctx = canvas.getContext('2d');
    let rotX = 0.3, rotY = 0.5, targetRotX = 0.3, targetRotY = 0.5;
    let isDragging = false, lastMouseX = 0, lastMouseY = 0;

    function resize3DCanvas() {
      if (!canvas) return;
      canvas.width = canvas.parentElement.clientWidth * window.devicePixelRatio;
      canvas.height = canvas.parentElement.clientHeight * window.devicePixelRatio;
    }
    window.addEventListener('resize', resize3DCanvas);

    if (canvas) {
      canvas.addEventListener('mousedown', (e) => {
        isDragging = true; lastMouseX = e.clientX; lastMouseY = e.clientY;
      });
      window.addEventListener('mousemove', (e) => {
        if (!isDragging) return;
        targetRotY += (e.clientX - lastMouseX) * 0.008;
        targetRotX += (e.clientY - lastMouseY) * 0.008;
        lastMouseX = e.clientX; lastMouseY = e.clientY;
      });
      window.addEventListener('mouseup', () => { isDragging = false; });

      canvas.addEventListener('touchstart', (e) => {
        if (e.touches.length === 1) {
          isDragging = true; lastMouseX = e.touches[0].clientX; lastMouseY = e.touches[0].clientY;
        }
      });
      canvas.addEventListener('touchmove', (e) => {
        if (!isDragging || e.touches.length !== 1) return;
        targetRotY += (e.touches[0].clientX - lastMouseX) * 0.008;
        targetRotX += (e.touches[0].clientY - lastMouseY) * 0.008;
        lastMouseX = e.touches[0].clientX; lastMouseY = e.touches[0].clientY;
      });
      window.addEventListener('touchend', () => { isDragging = false; });
    }

    function reset3DCamera() { targetRotX = 0.3; targetRotY = 0.5; }

    const phi = (1 + Math.sqrt(5)) / 2;
    const verticesBase = [
      [-1, phi, 0], [1, phi, 0], [-1, -phi, 0], [1, -phi, 0],
      [0, -1, phi], [0, 1, phi], [0, -1, -phi], [0, 1, -phi],
      [phi, 0, -1], [phi, 0, 1], [-phi, 0, -1], [-phi, 0, 1]
    ];
    const vertices = verticesBase.map(v => {
      const len = Math.hypot(...v);
      return [v[0] / len, v[1] / len, v[2] / len];
    });

    const edges = [
      [0,11],[0,5],[0,1],[0,7],[0,10],
      [1,5],[1,9],[1,8],[1,7],
      [2,11],[2,10],[2,6],[2,3],[2,4],
      [3,9],[3,4],[3,2],[3,6],[3,8],
      [4,5],[4,9],[4,3],[4,2],[4,11],
      [5,0],[5,1],[5,9],[5,4],[5,11],
      [6,10],[6,7],[6,8],[6,3],[6,2],
      [7,0],[7,1],[7,8],[7,6],[7,10],
      [8,1],[8,9],[8,3],[8,6],[8,7],
      [9,1],[9,5],[9,4],[9,3],[9,8],
      [10,0],[10,11],[10,2],[10,6],[10,7],
      [11,0],[11,10],[11,2],[11,4],[11,5]
    ];

    const satellites = Array.from({ length: 7 }, (_, i) => ({
      orbitRadius: 1.55 + (i * 0.08),
      speed: 0.015 + (i * 0.004),
      angle: (i / 7) * Math.PI * 2,
      inclination: 0.25 * (i % 3 - 1)
    }));

    const particles = Array.from({ length: 45 }, () => ({
      x: (Math.random() - 0.5) * 3.5,
      y: (Math.random() - 0.5) * 3.5,
      z: (Math.random() - 0.5) * 3.5,
      size: Math.random() * 2 + 1
    }));

    let corePulse = 0;

    function render3DScene() {
      if (!canvas) return;
      if (!canvas.width || !canvas.height) resize3DCanvas();
      const w = canvas.width, h = canvas.height;
      const cx = w / 2, cy = h / 2;
      const scale = Math.min(w, h) * 0.28;

      ctx.clearRect(0, 0, w, h);

      rotX += (targetRotX - rotX) * 0.08;
      rotY += (targetRotY - rotY) * 0.08;
      if (!isDragging) {
        targetRotY += (appData.mood === 'burnout' ? 0.003 : 0.008);
      }

      corePulse += 0.04;
      const pulseScale = 1.0 + Math.sin(corePulse) * (appData.mood === 'burnout' ? 0.09 : 0.04);

      let coreColor = '#3fb950';
      if (appData.mood === 'stressed') coreColor = '#d29922';
      else if (appData.mood === 'burnout') coreColor = '#f85149';

      const cosY = Math.cos(rotY), sinY = Math.sin(rotY);
      const cosX = Math.cos(rotX), sinX = Math.sin(rotX);

      function project(x, y, z) {
        const x1 = x * cosY + z * sinY;
        const z1 = -x * sinY + z * cosY;
        const y2 = y * cosX - z1 * sinX;
        const z2 = y * sinX + z1 * cosX;
        const dist = 3.2;
        const fov = dist / (dist + z2);
        return { px: cx + x1 * scale * fov, py: cy + y2 * scale * fov, depth: z2, fov: fov };
      }

      particles.forEach(p => {
        const prj = project(p.x, p.y, p.z);
        if (prj.fov > 0) {
          ctx.fillStyle = `rgba(139, 148, 158, ${0.4 * prj.fov})`;
          ctx.beginPath();
          ctx.arc(prj.px, prj.py, p.size * prj.fov, 0, Math.PI * 2);
          ctx.fill();
        }
      });

      const projectedVertices = vertices.map(v => {
        return project(v[0] * pulseScale, v[1] * pulseScale, v[2] * pulseScale);
      });

      ctx.strokeStyle = coreColor;
      ctx.lineWidth = 1.5;
      edges.forEach(([i1, i2]) => {
        const p1 = projectedVertices[i1];
        const p2 = projectedVertices[i2];
        const avgDepth = (p1.depth + p2.depth) / 2;
        ctx.globalAlpha = Math.max(0.15, Math.min(1.0, 0.6 + avgDepth * 0.4));
        ctx.beginPath();
        ctx.moveTo(p1.px, p1.py);
        ctx.lineTo(p2.px, p2.py);
        ctx.stroke();
      });

      projectedVertices.forEach(p => {
        ctx.globalAlpha = Math.max(0.3, Math.min(1.0, 0.8 + p.depth * 0.3));
        ctx.fillStyle = coreColor;
        ctx.beginPath();
        ctx.arc(p.px, p.py, 3.5 * p.fov, 0, Math.PI * 2);
        ctx.fill();
      });

      satellites.forEach(sat => {
        sat.angle += sat.speed * (appData.mood === 'burnout' ? 0.3 : 1.0);
        const p = project(Math.cos(sat.angle) * sat.orbitRadius, Math.sin(sat.angle * 2) * sat.inclination, Math.sin(sat.angle) * sat.orbitRadius);
        ctx.globalAlpha = 1.0;
        ctx.fillStyle = (sat.angle % Math.PI > 1.5) ? '#58a6ff' : '#bc8cff';
        const sSize = 6 * p.fov;
        ctx.fillRect(p.px - sSize/2, p.py - sSize/2, sSize, sSize);
      });

      ctx.globalAlpha = 1.0;
      requestAnimationFrame(render3DScene);
    }

    // 3D Tilt Card
    const cardWrap = document.getElementById('cardContainer');
    const holoCard = document.getElementById('hologramCard');
    const glare = document.getElementById('cardGlare');

    if (cardWrap && holoCard && glare) {
      cardWrap.addEventListener('mousemove', (e) => {
        const rect = holoCard.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        const cx = rect.width / 2, cy = rect.height / 2;
        const rotYVal = ((x - cx) / cx) * 16;
        const rotXVal = -((y - cy) / cy) * 16;
        holoCard.style.transform = `rotateX(${rotXVal}deg) rotateY(${rotYVal}deg) scale3d(1.02, 1.02, 1.02)`;
        glare.style.opacity = '1';
        glare.style.background = `radial-gradient(circle at ${x}px ${y}px, rgba(255,255,255,0.3) 0%, transparent 65%)`;
      });

      cardWrap.addEventListener('mouseleave', () => {
        holoCard.style.transform = 'rotateX(0deg) rotateY(0deg) scale3d(1, 1, 1)';
        glare.style.opacity = '0';
      });
    }

    function exportCardAsImage() {
      const exportCanvas = document.createElement('canvas');
      exportCanvas.width = 1000;
      exportCanvas.height = 1200;
      const eCtx = exportCanvas.getContext('2d');

      const grad = eCtx.createLinearGradient(0, 0, 1000, 1200);
      grad.addColorStop(0, '#0d1117');
      grad.addColorStop(0.5, '#161b22');
      grad.addColorStop(1, '#090d13');
      eCtx.fillStyle = grad;
      eCtx.fillRect(0, 0, 1000, 1200);

      eCtx.strokeStyle = '#6366f1';
      eCtx.lineWidth = 6;
      eCtx.strokeRect(30, 30, 940, 1140);

      eCtx.fillStyle = '#1c2333';
      eCtx.fillRect(60, 60, 880, 1080);
      eCtx.strokeStyle = '#30363d';
      eCtx.lineWidth = 2;
      eCtx.strokeRect(60, 60, 880, 1080);

      eCtx.fillStyle = '#6366f1';
      eCtx.font = 'bold 36px monospace';
      eCtx.fillText('<DevShield / Passport 3D>', 100, 140);

      eCtx.fillStyle = '#3fb950';
      eCtx.font = 'bold 22px monospace';
      eCtx.fillText('STATUS: VERIFIED CS STUDENT', 100, 190);

      eCtx.fillStyle = '#6366f1';
      eCtx.fillRect(100, 240, 140, 140);
      eCtx.font = '80px sans-serif';
      eCtx.fillText(appData.currentUser.avatar || '👨‍💻', 130, 345);

      eCtx.fillStyle = '#f0f6fc';
      eCtx.font = 'bold 44px sans-serif';
      eCtx.fillText(appData.currentUser.name || 'Dev Master: Khoa CNTT', 270, 290);

      eCtx.fillStyle = '#8b949e';
      eCtx.font = '28px monospace';
      eCtx.fillText(appData.currentUser.role || 'K68 Software Engineer', 270, 340);

      eCtx.fillStyle = '#0d1117';
      eCtx.fillRect(100, 440, 800, 200);
      eCtx.strokeStyle = '#30363d';
      eCtx.strokeRect(100, 440, 800, 200);

      eCtx.fillStyle = '#8b949e';
      eCtx.font = '22px sans-serif';
      eCtx.fillText('STREAK KỶ LUẬT', 140, 500);
      eCtx.fillText('GIỜ DEEP WORK', 410, 500);
      eCtx.fillText('NGUY CƠ DROP MÔN', 660, 500);

      eCtx.font = 'bold 40px monospace';
      eCtx.fillStyle = '#3fb950';
      eCtx.fillText(`🔥 ${appData.streak} NGÀY`, 140, 570);
      eCtx.fillStyle = '#58a6ff';
      eCtx.fillText('12.5h / Tuần', 410, 570);
      eCtx.fillStyle = '#3fb950';
      eCtx.fillText('0.0% An Toàn', 660, 570);

      eCtx.fillStyle = '#f0f6fc';
      eCtx.font = '26px sans-serif';
      eCtx.fillText('Triết lý: "Mỗi ngày 1 commit nhỏ - Không buông xuôi trước bug khó"', 100, 720);

      eCtx.fillStyle = '#30363d';
      for (let i = 0; i < 40; i++) {
        const wLine = (i % 3 === 0) ? 12 : 5;
        eCtx.fillRect(100 + i * 20, 960, wLine, 60);
      }

      eCtx.fillStyle = '#8b949e';
      eCtx.font = '20px monospace';
      eCtx.fillText('DevShield 3D System Verification Seal - 2026', 100, 1070);

      const link = document.createElement('a');
      link.download = `DevShield_Passport_${Date.now()}.png`;
      link.href = exportCanvas.toDataURL('image/png');
      link.click();
    }

    // --- TIMEBLOCKING & HABITS ---
    const dayNames = ['CN', 'Thứ 2', 'Thứ 3', 'Thứ 4', 'Thứ 5', 'Thứ 6', 'Thứ 7'];
    function renderDaysBar() {
      const bar = document.getElementById('days-bar');
      if (!bar) return;
      bar.innerHTML = '';
      [1, 2, 3, 4, 5, 6, 0].forEach(d => {
        const btn = document.createElement('button');
        const isActive = appData.selectedDay === d;
        btn.className = `px-3 py-1.5 text-xs font-semibold rounded-lg mono transition-all ${
          isActive ? 'bg-indigo-600 text-white shadow' : 'bg-[#0d1117] text-[#8b949e] hover:text-[#f0f6fc] border border-[#30363d]'
        }`;
        btn.innerText = (d === 1 ? 'Thứ 2 (Nay)' : dayNames[d]);
        btn.onclick = () => {
          appData.selectedDay = d;
          saveData();
          renderDaysBar();
          renderTimeline();
          document.getElementById('selected-day-label').innerText = dayNames[d];
        };
        bar.appendChild(btn);
      });
    }

    function renderTimeline() {
      const container = document.getElementById('timeline-list');
      if (!container) return;
      container.innerHTML = '';
      const dayBlocks = appData.timeBlocks.filter(b => b.day === appData.selectedDay);

      if (dayBlocks.length === 0) {
        container.innerHTML = `
          <div class="p-8 text-center rounded-2xl bg-[#161b22] border border-[#30363d] space-y-2">
            <span class="text-3xl">☕</span>
            <h4 class="text-sm font-semibold text-[#f0f6fc]">Chưa có lịch cho ngày này!</h4>
            <p class="text-xs text-[#8b949e]">Hãy thêm 1 khối lên lớp hoặc 1 phiên Deep Code 90p ở khung bên phải.</p>
          </div>
        `;
        updateDeepWorkGauge(0);
        return;
      }

      let totalDeepHours = 0;
      dayBlocks.forEach(b => {
        let borderClass = 'border-emerald-500/40 bg-emerald-500/5 text-emerald-400';
        let catLabel = 'Deep Code';
        if (b.cat === 'lecture') {
          borderClass = 'border-blue-500/40 bg-blue-500/5 text-blue-400';
          catLabel = 'Lên lớp';
        } else if (b.cat === 'project') {
          borderClass = 'border-amber-500/40 bg-amber-500/5 text-amber-400';
          catLabel = 'Bài tập lớn';
        } else if (b.cat === 'rest') {
          borderClass = 'border-purple-500/40 bg-purple-500/5 text-purple-400';
          catLabel = 'Nghỉ ngơi';
        }

        if (b.cat === 'deep_code') totalDeepHours += 1.5;

        const card = document.createElement('div');
        card.className = `p-4 rounded-xl border ${borderClass} transition-all flex items-start justify-between gap-4 ${b.done ? 'opacity-60' : ''}`;
        card.innerHTML = `
          <div class="flex items-start gap-3">
            <div class="px-2.5 py-1 rounded bg-[#0d1117] border border-[#30363d] mono text-xs font-bold whitespace-nowrap mt-0.5">
              ${b.start} - ${b.end}
            </div>
            <div>
              <div class="flex items-center gap-2">
                <h3 class="font-semibold text-sm ${b.done ? 'line-through text-[#8b949e]' : 'text-[#f0f6fc]'}">${b.title}</h3>
                <span class="px-1.5 py-0.2 rounded text-[10px] mono bg-[#0d1117] border border-[#30363d]">${catLabel}</span>
              </div>
              <p class="text-xs text-[#8b949e] mt-1">${b.desc || ''}</p>
            </div>
          </div>
          <div class="flex items-center gap-1.5">
            <button onclick="toggleBlockDone('${b.id}')" class="px-2.5 py-1 text-xs rounded-lg ${b.done ? 'bg-emerald-500 text-white' : 'bg-[#0d1117] text-[#8b949e] hover:text-[#f0f6fc] border border-[#30363d]'} transition-all">
              ${b.done ? '✓ Xong' : 'Hoàn tất'}
            </button>
            <button onclick="deleteBlock('${b.id}')" class="p-1 text-xs rounded hover:text-red-400 text-[#8b949e]">✕</button>
          </div>
        `;
        container.appendChild(card);
      });
      updateDeepWorkGauge(totalDeepHours);
    }

    function toggleBlockDone(id) {
      const item = appData.timeBlocks.find(b => b.id === id);
      if (item) item.done = !item.done;
      saveData();
      renderTimeline();
    }
    function deleteBlock(id) {
      appData.timeBlocks = appData.timeBlocks.filter(b => b.id !== id);
      saveData();
      renderTimeline();
    }
    function handleAddBlock() {
      const title = document.getElementById('input-title').value.trim();
      const start = document.getElementById('input-start').value;
      const end = document.getElementById('input-end').value;
      const cat = document.getElementById('input-cat').value;
      const desc = document.getElementById('input-desc').value.trim();
      if (!title) { alert("Vui lòng nhập tên môn hoặc công việc cần làm!"); return; }
      appData.timeBlocks.push({ id: 'b_' + Date.now(), day: appData.selectedDay, title, cat, start, end, done: false, desc });
      saveData();
      renderTimeline();
      document.getElementById('input-title').value = '';
      document.getElementById('input-desc').value = '';
    }
    function updateDeepWorkGauge(hours) {
      const gauge = document.getElementById('deepwork-gauge');
      const bar = document.getElementById('deepwork-bar');
      if (!gauge || !bar) return;
      gauge.innerText = `${hours.toFixed(1)}h / 3.0h max`;
      const pct = Math.min(100, Math.round((hours / 3.0) * 100));
      bar.style.width = pct + '%';
      bar.className = (hours > 3.0) ? 'bg-red-500 h-full rounded-full transition-all' : 'bg-emerald-500 h-full rounded-full transition-all';
    }

    function renderHabits() {
      const container = document.getElementById('habits-list');
      if (!container) return;
      container.innerHTML = '';
      let doneCount = 0;
      appData.habits.forEach(h => {
        if (h.done) doneCount++;
        const label = document.createElement('label');
        label.className = `flex items-start gap-3 p-3.5 rounded-xl border border-[#30363d] hover:bg-[#0d1117] cursor-pointer transition-all ${h.done ? 'bg-emerald-500/5 border-emerald-500/30' : ''}`;
        label.innerHTML = `
          <input type="checkbox" ${h.done ? 'checked' : ''} onchange="toggleHabit(${h.id})" class="mt-1 w-4 h-4 rounded text-indigo-600 focus:ring-0">
          <div class="space-y-0.5">
            <span class="text-sm font-medium ${h.done ? 'text-emerald-300' : 'text-[#f0f6fc]'} flex items-center gap-2">
              <span>${h.title}</span>
              <span class="text-[10px] mono px-1.5 py-0.2 rounded bg-[#0d1117] border border-[#30363d] text-[#8b949e]">${h.tag}</span>
            </span>
            <p class="text-xs text-[#8b949e]">${h.desc}</p>
          </div>
        `;
        container.appendChild(label);
      });
      document.getElementById('habits-counter').innerText = `${doneCount}/${appData.habits.length} hoàn thành`;
      document.getElementById('streak-badge').innerText = `🔥 ${appData.streak} ngày`;
      document.getElementById('heatmap-streak-tag').innerText = `🔥 ${appData.streak} Ngày liên tiếp`;
      document.getElementById('shield-count').innerText = appData.shieldCount;
    }
    function toggleHabit(id) {
      const h = appData.habits.find(item => item.id === id);
      if (h) h.done = !h.done;
      saveData();
      renderHabits();
    }
    function useShield() {
      if (appData.shieldCount <= 0) { alert("Bạn đã hết lượt sử dụng Bình Cứu Sinh trong tháng này!"); return; }
      appData.shieldCount--;
      saveData();
      renderHabits();
      alert("🛡️ Kích hoạt Bình Cứu Sinh thành công! Chuỗi Streak của bạn được bảo toàn an toàn hôm nay.");
    }
    function renderHeatmap() {
      const grid = document.getElementById('heatmap-container');
      if (!grid) return;
      grid.innerHTML = '';
      for (let i = 0; i < 35; i++) {
        const cell = document.createElement('div');
        if (i >= 28) cell.className = 'w-full aspect-square rounded-sm bg-emerald-500 cursor-pointer hover:ring-2 hover:ring-emerald-400 transition-all';
        else if (i >= 21) cell.className = 'w-full aspect-square rounded-sm bg-emerald-600/80 cursor-pointer hover:ring-2 hover:ring-emerald-400 transition-all';
        else if (i === 12 || i === 15 || i === 18) cell.className = 'w-full aspect-square rounded-sm bg-emerald-900/60 cursor-pointer hover:ring-2 hover:ring-emerald-400 transition-all';
        else cell.className = 'w-full aspect-square rounded-sm bg-[#161b22] border border-[#30363d] cursor-pointer hover:ring-1 hover:ring-[#8b949e] transition-all';
        grid.appendChild(cell);
      }
    }

    function setMood(mood) {
      appData.mood = mood;
      saveData();
      const banner = document.getElementById('burnout-banner');
      const bFresh = document.getElementById('mood-fresh');
      const bStressed = document.getElementById('mood-stressed');
      const bBurnout = document.getElementById('mood-burnout');
      const statusText = document.getElementById('core-status-text');

      [bFresh, bStressed, bBurnout].forEach(b => {
        b.className = "px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 text-[#8b949e] hover:text-[#f0f6fc]";
      });

      if (mood === 'fresh') {
        bFresh.className = "px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 bg-emerald-500/20 text-emerald-400 font-medium";
        banner.className = "hidden";
        if (statusText) { statusText.innerText = '🟢 Bình Ổn - Tối Ưu'; statusText.className = 'text-emerald-400 font-bold'; }
      } else if (mood === 'stressed') {
        bStressed.className = "px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 bg-amber-500/20 text-amber-400 font-medium";
        banner.className = "p-4 rounded-xl border border-amber-500/40 bg-amber-500/10 text-amber-300 text-xs flex items-center justify-between";
        banner.innerHTML = `
          <div class="flex items-center gap-3">
            <span class="text-xl">⚠️</span>
            <div><strong>Cảnh báo tải trọng:</strong> Não bạn đang căng thẳng. Hãy ưu tiên bài tập có hạn nộp trong 48h tới, dời việc học thêm framework mới sang cuối tuần!</div>
          </div>
          <button onclick="setMood('fresh')" class="text-[11px] underline ml-4 whitespace-nowrap">Đã hiểu</button>
        `;
        if (statusText) { statusText.innerText = '🟡 Cảnh Báo Tải Cao'; statusText.className = 'text-amber-400 font-bold'; }
      } else if (mood === 'burnout') {
        bBurnout.className = "px-2.5 py-1 rounded-lg transition-all flex items-center gap-1 bg-red-500/20 text-red-400 font-medium";
        banner.className = "p-4 rounded-xl border border-red-500/50 bg-red-500/10 text-red-300 text-xs flex items-center justify-between animate-pulse";
        banner.innerHTML = `
          <div class="flex items-center gap-3">
            <span class="text-xl">🚨</span>
            <div><strong>CHẾ ĐỘ CẤP CỨU BURNOUT:</strong> Đừng ép bản thân code tiếp đêm nay! Hãy dùng 1 lượt Bình Cứu Sinh, hoàn thành 1 task nhẹ nhất rồi đi ngủ trước 23h00. Sức khỏe quan trọng hơn 1 dòng code!</div>
          </div>
          <button onclick="switchTab('tab-habits')" class="px-3 py-1 bg-red-600 text-white rounded text-xs font-bold whitespace-nowrap ml-4">Mở Task Nhẹ</button>
        `;
        if (statusText) { statusText.innerText = '🔴 BÁO ĐỘNG ĐỎ BURNOUT'; statusText.className = 'text-red-400 font-bold animate-pulse'; }
      }
    }

    // --- SYSTEM INITIALIZATION ---
    function init() {
      renderAuthBar();
      renderDaysBar();
      renderTimeline();
      renderHabits();
      renderHeatmap();
      renderAdvice();
      renderQuiz();
      setMood(appData.mood || 'fresh');
      resize3DCanvas();
      render3DScene();
    }
    window.onload = init;
  </script>
</body>
</html>
