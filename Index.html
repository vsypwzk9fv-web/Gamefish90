<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Fishery Quiz & Catch - เกมตกปลาและทายสายพันธุ์ปลา</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    html, body {
      width: 100%;
      height: 100%;
      overflow: hidden;
      font-family: 'Kanit', sans-serif;
      background-color: #0f172a;
      color: #f8fafc;
      user-select: none;
      -webkit-user-select: none;
      touch-action: manipulation;
    }
    .custom-scrollbar::-webkit-scrollbar {
      width: 5px;
    }
    .custom-scrollbar::-webkit-scrollbar-track {
      background: #1e293b;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: #475569;
      border-radius: 3px;
    }
  </style>
</head>
<body class="w-full h-full flex flex-col p-2 sm:p-4 justify-between">

  <!-- Header -->
  <header class="w-full max-w-2xl mx-auto flex items-center justify-between bg-slate-800/90 border border-slate-700 px-3 py-2 rounded-xl shadow-md flex-shrink-0">
    <div class="flex items-center gap-2">
      <div class="p-1.5 bg-teal-500/20 text-teal-400 rounded-lg border border-teal-500/30">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path>
        </svg>
      </div>
      <div>
        <h1 class="text-xs sm:text-sm font-bold text-teal-300 leading-tight">Fishery Quiz & Catch</h1>
        <p class="text-[9px] text-slate-400">ตกปลา & เรียนรู้สายพันธุ์สัตว์น้ำ</p>
      </div>
    </div>
    <div class="flex items-center gap-2">
      <div class="text-right">
        <div class="text-[9px] text-slate-400">คะแนน</div>
        <div id="scoreText" class="text-xs sm:text-sm font-bold text-amber-400">0 XP</div>
      </div>
      <button onclick="togglePedia()" class="px-2 py-1 bg-slate-700 hover:bg-slate-600 border border-slate-600 rounded-lg text-xs font-medium flex items-center gap-1 transition">
        <span>📖</span>
        <span class="hidden sm:inline">สมุดสะสม</span>
      </button>
    </div>
  </header>

  <!-- Main Game Container -->
  <main class="w-full max-w-2xl mx-auto flex-1 flex flex-col my-2 overflow-hidden bg-slate-900 rounded-xl border border-slate-700 shadow-xl relative">
    
    <!-- Status Badges -->
    <div class="absolute top-2 left-2 z-10 bg-slate-900/80 backdrop-blur px-2 py-0.5 rounded-full border border-slate-700 text-[10px] text-teal-400 font-medium">
      จุดตกปลา: แหล่งน้ำธรรมชาติ
    </div>
    <div id="statusBadge" class="absolute top-2 right-2 z-10 bg-amber-500/20 text-amber-300 backdrop-blur px-2 py-0.5 rounded-full border border-amber-500/30 text-[10px] font-medium">
      พร้อมออกตกปลา
    </div>

    <!-- Fixed Canvas Container -->
    <div id="canvasContainer" class="w-full flex-1 relative overflow-hidden bg-slate-950">
      <canvas id="fishCanvas" class="block w-full h-full"></canvas>
    </div>

    <!-- Control Area -->
    <div class="p-2.5 bg-slate-800/95 border-t border-slate-700 flex flex-col gap-1.5 flex-shrink-0">
      <div class="flex justify-between text-[10px] sm:text-xs font-medium text-slate-300">
        <span>จังหวะวัดเบ็ด</span>
        <span id="timingStatus" class="text-amber-400">กดปุ่มเพื่อเริ่มตกปลา</span>
      </div>
      
      <!-- Timing Bar -->
      <div class="relative w-full h-4 bg-slate-950 rounded-full border border-slate-700 overflow-hidden">
        <div id="greenZone" class="absolute top-0 bottom-0 bg-emerald-500/50 border-x-2 border-emerald-400" style="left: 40%; width: 25%;"></div>
        <div id="meterPointer" class="absolute top-0 bottom-0 w-2 bg-yellow-300 shadow-[0_0_6px_#fde047]" style="left: 0%;"></div>
      </div>

      <button id="actionBtn" onclick="handleActionButton()" class="w-full py-2 bg-teal-500 hover:bg-teal-400 text-slate-950 font-bold text-xs sm:text-sm rounded-lg transition shadow active:scale-[0.99]">
        🎣 หย่อนสายเบ็ด
      </button>
    </div>

  </main>

  <!-- Quiz Modal Window -->
  <div id="quizModal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-md z-50 flex items-center justify-center p-3 hidden">
    <div class="bg-slate-800 border border-slate-700 rounded-2xl max-w-sm w-full p-4 shadow-2xl flex flex-col gap-3 max-h-[90vh] overflow-y-auto custom-scrollbar">
      
      <div class="flex items-center justify-between border-b border-slate-700 pb-2">
        <div>
          <span class="text-[10px] font-semibold uppercase tracking-wider text-teal-400">ปลาติดเบ็ดแล้ว!</span>
          <h2 class="text-sm sm:text-base font-bold text-white">ทายสายพันธุ์สัตว์น้ำ</h2>
        </div>
        <span class="text-lg">🐟</span>
      </div>

      <!-- Fish Preview -->
      <div class="w-full h-24 bg-slate-900 rounded-xl border border-slate-700 flex items-center justify-center p-2 relative overflow-hidden">
        <div id="quizFishImage" class="w-full h-full flex items-center justify-center"></div>
      </div>

      <!-- Quiz Hint -->
      <div class="bg-slate-900/60 p-2 rounded-xl border border-slate-700 text-xs text-slate-300">
        <span class="text-teal-400 font-bold">💡 คำใบ้: </span>
        <span id="quizHintText">กำลังโหลด...</span>
      </div>

      <!-- Options -->
      <div id="quizOptions" class="grid grid-cols-1 gap-1.5"></div>

      <!-- Result Banner -->
      <div id="quizResultBanner" class="hidden p-2 rounded-xl border text-xs flex flex-col gap-1"></div>

      <!-- Close Button -->
      <button id="modalCloseBtn" onclick="closeQuizModal()" class="w-full py-2 bg-slate-700 hover:bg-slate-600 text-white rounded-xl font-semibold text-xs transition hidden">
        ตกปลาตัวต่อไป 🎣
      </button>

    </div>
  </div>

  <!-- Fishpedia Modal -->
  <div id="pediaModal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-md z-50 flex items-center justify-center p-3 hidden">
    <div class="bg-slate-800 border border-slate-700 rounded-2xl max-w-md w-full p-4 shadow-2xl flex flex-col gap-3 max-h-[85vh]">
      <div class="flex items-center justify-between border-b border-slate-700 pb-2">
        <h2 class="text-xs sm:text-sm font-bold text-white flex items-center gap-2">📖 สารานุกรมสัตว์น้ำ (Fishpedia)</h2>
        <button onclick="togglePedia()" class="text-slate-400 hover:text-white text-base">✕</button>
      </div>
      
      <div id="pediaList" class="grid grid-cols-1 sm:grid-cols-2 gap-2 overflow-y-auto custom-scrollbar pr-1 flex-1"></div>
    </div>
  </div>

  <!-- Script Game Logic -->
  <script>
    const FISH_DATABASE = [
      {
        id: "tilapia",
        name: "ปลานิล",
        sciName: "Oreochromis niloticus",
        type: "ปลาน้ำจืด",
        habitat: "บ่อเลี้ยง, แม่น้ำ",
        hint: "ลำตัวข้างแบน มีแถบสีดำคั่นตามยาวลำตัวและครีบ นำเข้าโดยในหลวงรัชกาลที่ 9",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><ellipse cx="50" cy="30" rx="35" ry="20" fill="#64748b"/><path d="M15 30 L5 15 L5 45 Z" fill="#475569"/><polygon points="35,10 65,10 55,20" fill="#475569"/><circle cx="70" cy="25" r="3" fill="#000"/></svg>`
      },
      {
        id: "catfish",
        name: "ปลาดุกอุย",
        sciName: "Clarias batrachus",
        type: "ปลาน้ำจืด",
        habitat: "หนอง บึง นาข้าว",
        hint: "ลำตัวยาว ไม่มีเกล็ด มีหนวด 4 คู่รอบปาก สามารถหายใจด้วยอวัยวะพิเศษ",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><path d="M20 30 Q50 15 80 28 Q85 30 80 32 Q50 45 20 30 Z" fill="#334155"/><path d="M20 30 L5 20 L5 40 Z" fill="#1e293b"/><circle cx="75" cy="25" r="2.5" fill="#facc15"/></svg>`
      },
      {
        id: "seabass",
        name: "ปลากะพงขาว",
        sciName: "Lates calcarifer",
        type: "ปลาสองน้ำ",
        habitat: "ชายฝั่ง, ป่าชายเลน",
        hint: "ลำตัวหนา หัวแหลม ตาโตสีเหลืองทอง ครีบหลังแบ่งเป็นสองส่วน",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><ellipse cx="50" cy="30" rx="38" ry="18" fill="#94a3b8"/><path d="M12 30 L2 18 L2 42 Z" fill="#64748b"/><circle cx="75" cy="24" r="3.5" fill="#facc15"/></svg>`
      },
      {
        id: "giant_catfish",
        name: "ปลาบึก",
        sciName: "Pangasianodon gigas",
        type: "ปลาน้ำจืดใหญ่",
        habitat: "แม่น้ำโขง",
        hint: "ปลาน้ำจืดไม่มีเกล็ดขนาดใหญ่ที่สุดในโลก ไม่มีฟัน กินพืชและตะไคร่น้ำ",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><ellipse cx="50" cy="30" rx="42" ry="22" fill="#475569"/><path d="M8 30 L-2 15 L-2 45 Z" fill="#334155"/><circle cx="80" cy="32" r="3" fill="#000"/></svg>`
      },
      {
        id: "blackchin",
        name: "ปลาหมอคางดำ",
        sciName: "Sarotherodon melanotheron",
        type: "เอเลี่ยนสปีชีส์",
        habitat: "น้ำกร่อย ชายฝั่ง",
        hint: "มีจุดสีดำใต้คาง ขยายพันธุ์เร็ว ฟักไข่ในปาก ส่งผลกระทบต่อระบบนิเวศ",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><ellipse cx="50" cy="30" rx="32" ry="19" fill="#84cc16"/><path d="M18 30 L5 18 L5 42 Z" fill="#65a30d"/><circle cx="72" cy="24" r="3" fill="#000"/></svg>`
      },
      {
        id: "snakeskin_gourami",
        name: "ปลาสลิด",
        sciName: "Trichopodus pectoralis",
        type: "ปลาน้ำจืด",
        habitat: "หนอง บึง คลอง",
        hint: "ลำตัวแบนข้าง มีลายดำพาดขวาง นิยมนำมาทำปลาสลิดแดดเดียวของขึ้นชื่อบางบ่อ",
        svg: `<svg viewBox="0 0 100 60" class="w-24 h-14"><ellipse cx="50" cy="30" rx="30" ry="22" fill="#52525b"/><path d="M20 30 L8 18 L8 42 Z" fill="#3f3f46"/><circle cx="70" cy="24" r="2.5" fill="#facc15"/></svg>`
      }
    ];

    let score = 0;
    let caughtSet = new Set();
    let gameState = "IDLE";
    let targetPointerPos = 0;
    let pointerDirection = 1;
    let greenZoneStart = 35;
    let greenZoneWidth = 25;
    let currentFish = null;
    let waveOffset = 0;

    const canvas = document.getElementById("fishCanvas");
    const container = document.getElementById("canvasContainer");
    const ctx = canvas.getContext("2d");

    function resizeCanvas() {
      const rect = container.getBoundingClientRect();
      if (canvas.width !== rect.width || canvas.height !== rect.height) {
        canvas.width = rect.width;
        canvas.height = rect.height;
      }
    }

    function drawScene() {
      resizeCanvas();
      const w = canvas.width;
      const h = canvas.height;
      const waterY = h * 0.4;

      ctx.clearRect(0, 0, w, h);

      // Sky Background
      ctx.fillStyle = "#1e293b";
      ctx.fillRect(0, 0, w, waterY);

      // Water Background
      ctx.fillStyle = "#0891b2";
      ctx.fillRect(0, waterY, w, h - waterY);

      // Wave Effect
      waveOffset += 0.04;
      ctx.fillStyle = "rgba(255, 255, 255, 0.15)";
      ctx.beginPath();
      ctx.moveTo(0, waterY);
      for (let x = 0; x <= w; x += 15) {
        ctx.lineTo(x, waterY + Math.sin(x * 0.04 + waveOffset) * 3);
      }
      ctx.lineTo(w, h);
      ctx.lineTo(0, h);
      ctx.closePath();
      ctx.fill();

      // Fishing Rod & Line
      const rodTipX = w * 0.65;
      const rodTipY = h * 0.15;

      ctx.strokeStyle = "#b45309";
      ctx.lineWidth = 4;
      ctx.lineCap = "round";
      ctx.beginPath();
      ctx.moveTo(w * 0.1, h * 0.35);
      ctx.quadraticCurveTo(w * 0.35, h * 0.15, rodTipX, rodTipY);
      ctx.stroke();

      if (gameState !== "IDLE") {
        let lineTargetY = waterY + 15 + Math.sin(waveOffset * 2) * 2;
        ctx.strokeStyle = "rgba(255, 255, 255, 0.7)";
        ctx.lineWidth = 1;
        ctx.beginPath();
        ctx.moveTo(rodTipX, rodTipY);
        ctx.lineTo(rodTipX, lineTargetY);
        ctx.stroke();

        // Bobber
        ctx.fillStyle = "#ef4444";
        ctx.beginPath();
        ctx.arc(rodTipX, lineTargetY - 2, 4, 0, Math.PI * 2);
        ctx.fill();
        ctx.fillStyle = "#ffffff";
        ctx.beginPath();
        ctx.arc(rodTipX, lineTargetY + 2, 4, 0, Math.PI * 2);
        ctx.fill();
      }

      // Timing Pointer Movement
      if (gameState === "HOOKING") {
        targetPointerPos += 2 * pointerDirection;
        if (targetPointerPos >= 100 || targetPointerPos <= 0) {
          pointerDirection *= -1;
        }
        document.getElementById("meterPointer").style.left = targetPointerPos + "%";
      }

      requestAnimationFrame(drawScene);
    }

    function handleActionButton() {
      const btn = document.getElementById("actionBtn");
      const badge = document.getElementById("statusBadge");
      const statusText = document.getElementById("timingStatus");

      if (gameState === "IDLE") {
        gameState = "WAITING";
        btn.innerText = "⏳ รอปลากินเหยื่อ...";
        btn.disabled = true;
        btn.className = "w-full py-2 bg-slate-700 text-slate-400 font-bold text-xs sm:text-sm rounded-lg cursor-not-allowed";
        badge.innerText = "หย่อนเหยื่อลงน้ำแล้ว...";
        badge.className = "absolute top-2 right-2 z-10 bg-blue-500/20 text-blue-300 backdrop-blur px-2 py-0.5 rounded-full border border-blue-500/30 text-[10px] font-medium";

        setTimeout(() => {
          if (gameState === "WAITING") {
            gameState = "HOOKING";
            greenZoneStart = 20 + Math.floor(Math.random() * 50);
            document.getElementById("greenZone").style.left = greenZoneStart + "%";
            document.getElementById("greenZone").style.width = greenZoneWidth + "%";

            btn.disabled = false;
            btn.innerText = "🎣 ฮุก! (กดเพื่อวัดเบ็ด)";
            btn.className = "w-full py-2 bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold text-xs sm:text-sm rounded-lg transition shadow animate-pulse";
            badge.innerText = "🐟 FISH ON!";
            badge.className = "absolute top-2 right-2 z-10 bg-red-500/30 text-red-300 backdrop-blur px-2 py-0.5 rounded-full border border-red-500/50 text-[10px] font-bold animate-bounce";
            statusText.innerText = "กดให้ตรงแถบสีเขียว!";
          }
        }, 2000 + Math.random() * 2000);

      } else if (gameState === "HOOKING") {
        const isHit = targetPointerPos >= greenZoneStart && targetPointerPos <= (greenZoneStart + greenZoneWidth);
        if (isHit) {
          triggerQuiz();
        } else {
          statusText.innerText = "❌ วัดเบ็ดพลาด! ปลาหลุดไปแล้ว";
          resetGame();
        }
      }
    }

    function resetGame() {
      gameState = "IDLE";
      const btn = document.getElementById("actionBtn");
      const badge = document.getElementById("statusBadge");

      btn.disabled = false;
      btn.innerText = "🎣 หย่อนสายเบ็ด";
      btn.className = "w-full py-2 bg-teal-500 hover:bg-teal-400 text-slate-950 font-bold text-xs sm:text-sm rounded-lg transition shadow active:scale-[0.99]";
      badge.innerText = "พร้อมออกตกปลา";
      badge.className = "absolute top-2 right-2 z-10 bg-amber-500/20 text-amber-300 backdrop-blur px-2 py-0.5 rounded-full border border-amber-500/30 text-[10px] font-medium";
    }

    function triggerQuiz() {
      gameState = "QUIZ";
      currentFish = FISH_DATABASE[Math.floor(Math.random() * FISH_DATABASE.length)];

      document.getElementById("quizHintText").innerText = currentFish.hint;
      document.getElementById("quizFishImage").innerHTML = currentFish.svg;

      const options = [currentFish];
      while (options.length < 4) {
        const rand = FISH_DATABASE[Math.floor(Math.random() * FISH_DATABASE.length)];
        if (!options.find(o => o.id === rand.id)) options.push(rand);
      }
      options.sort(() => Math.random() - 0.5);

      const optionsContainer = document.getElementById("quizOptions");
      optionsContainer.innerHTML = "";
      
      options.forEach(opt => {
        const optBtn = document.createElement("button");
        optBtn.className = "p-2 bg-slate-700/80 hover:bg-slate-600 border border-slate-600 rounded-xl text-xs font-medium text-left transition flex items-center justify-between";
        optBtn.innerHTML = `<span>${opt.name}</span><span class="text-[9px] text-slate-400">${opt.type}</span>`;
        optBtn.onclick = () => submitAnswer(opt.id, optBtn);
        optionsContainer.appendChild(optBtn);
      });

      document.getElementById("quizResultBanner").className = "hidden";
      document.getElementById("modalCloseBtn").classList.add("hidden");
      document.getElementById("quizModal").classList.remove("hidden");
    }

    function submitAnswer(selectedId, btnElement) {
      const buttons = document.querySelectorAll("#quizOptions button");
      buttons.forEach(b => b.disabled = true);

      const banner = document.getElementById("quizResultBanner");
      banner.classList.remove("hidden");

      if (selectedId === currentFish.id) {
        score += 100;
        caughtSet.add(currentFish.id);
        document.getElementById("scoreText").innerText = score + " XP";

        btnElement.className = "p-2 bg-emerald-600 border border-emerald-400 rounded-xl text-xs font-bold text-white text-left flex items-center justify-between";
        banner.className = "p-2 bg-emerald-500/20 border border-emerald-500/40 rounded-xl text-xs text-emerald-300 flex flex-col gap-0.5";
        banner.innerHTML = `<div class="font-bold">🎉 ถูกต้อง! +100 XP</div><div>คือ <span class="font-bold text-white">${currentFish.name}</span> (<em>${currentFish.sciName}</em>)</div>`;
      } else {
        btnElement.className = "p-2 bg-rose-600 border border-rose-400 rounded-xl text-xs font-bold text-white text-left flex items-center justify-between";
        banner.className = "p-2 bg-rose-500/20 border border-rose-500/40 rounded-xl text-xs text-rose-300 flex flex-col gap-0.5";
        banner.innerHTML = `<div class="font-bold">❌ ยังไม่ถูกต้อง!</div><div>เฉลย: <span class="font-bold text-amber-300">${currentFish.name}</span> (${currentFish.sciName})</div>`;
      }

      document.getElementById("modalCloseBtn").classList.remove("hidden");
      renderPedia();
    }

    function closeQuizModal() {
      document.getElementById("quizModal").classList.add("hidden");
      resetGame();
    }

    function renderPedia() {
      const pediaContainer = document.getElementById("pediaList");
      pediaContainer.innerHTML = "";

      FISH_DATABASE.forEach(fish => {
        const isCaught = caughtSet.has(fish.id);
        const card = document.createElement("div");
        card.className = `p-2 rounded-xl border flex gap-2 items-center ${isCaught ? "bg-slate-700/60 border-teal-500/40" : "bg-slate-900/50 border-slate-800 opacity-60"}`;
        card.innerHTML = `
          <div class="w-10 h-9 bg-slate-900 rounded-lg flex items-center justify-center border border-slate-700 flex-shrink-0">${isCaught ? fish.svg : '<span class="text-xs">❓</span>'}</div>
          <div class="flex-1 min-w-0">
            <div class="flex items-center justify-between"><h4 class="font-bold text-xs ${isCaught ? 'text-teal-300' : 'text-slate-400'} truncate">${isCaught ? fish.name : '???'}</h4><span class="text-[8px] px-1 py-0.5 rounded bg-slate-800 text-slate-400">${fish.type}</span></div>
            <p class="text-[9px] text-slate-400 italic truncate">${isCaught ? fish.sciName : 'ยังไม่เคยตกได้'}</p>
          </div>`;
        pediaContainer.appendChild(card);
      });
    }

    function togglePedia() {
      const modal = document.getElementById("pediaModal");
      modal.classList.toggle("hidden");
      if (!modal.classList.contains("hidden")) renderPedia();
    }

    // Initialize Application
    window.addEventListener("resize", resizeCanvas);
    drawScene();
    renderPedia();
  </script>
</body>
</html>
