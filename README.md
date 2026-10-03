# Slowry-park
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SLOWRY PARK</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css" />
  <style>
    body {
      font-family: "Pretendard Variable", Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, sans-serif;
    }
  </style>
</head>
<body class="bg-gradient-to-b from-[#e8f5e9] via-[#c8e6c9] to-[#a5d6a7] min-h-screen text-[#1b4332] flex justify-center p-4 sm:p-6">

  <div class="w-full max-w-md flex flex-col items-center">
    
    <!-- 프로필 카드 -->
    <header class="bg-white/90 backdrop-blur-sm border-2 border-[#1b4332] rounded-3xl p-6 w-full text-center shadow-[0_6px_0_#1b4332] mb-6 transition-all">
      <div class="relative w-20 h-20 mx-auto mb-3">
        <div class="w-full h-full rounded-full bg-[#d8f3dc] border-2 border-[#1b4332] flex items-center justify-center text-4xl shadow-inner">
          🦎
        </div>
      </div>
      <h1 class="text-2xl font-extrabold text-[#1b4332] tracking-tight mb-1">SLOWRY PARK</h1>
      <p class="text-xs font-semibold text-[#2d6a4f] tracking-wide">
        WELCOME TO SLOWRY PARK<em class="not-italic italic font-bold text-[#1b4332]">!</em>
      </p>
    </header>

    <!-- 링크 목록 (3개) -->
    <main class="w-full flex flex-col gap-4">
      
      <!-- 1. 블로그 -->
      <div class="bg-white border-2 border-[#1b4332] rounded-2xl p-4 flex items-center justify-between shadow-[0_5px_0_#1b4332] hover:-translate-y-0.5 hover:shadow-[0_7px_0_#1b4332] transition-all">
        <div class="flex items-center gap-3">
          <div class="w-11 h-11 bg-[#e8f5e9] border border-[#2d6a4f] rounded-xl flex items-center justify-center text-2xl">
            🦎
          </div>
          <span class="text-base font-bold text-[#1b4332]">블로그</span>
        </div>
        <div class="flex items-center gap-2">
          <button onclick="openModal('blog')" class="w-9 h-9 bg-[#d8f3dc] hover:bg-[#b7e4c7] border border-[#1b4332] rounded-lg flex items-center justify-center text-lg transition-colors" title="미리보기">
            👁️
          </button>
          <a href="https://m.blog.naver.com/ra-pi" target="_blank" class="w-9 h-9 bg-[#2d6a4f] hover:bg-[#1b4332] text-white border border-[#1b4332] rounded-lg flex items-center justify-center text-sm font-bold transition-colors">
            ➔
          </a>
        </div>
      </div>

      <!-- 2. 오픈채팅방 -->
      <div class="bg-white border-2 border-[#1b4332] rounded-2xl p-4 flex items-center justify-between shadow-[0_5px_0_#1b4332] hover:-translate-y-0.5 hover:shadow-[0_7px_0_#1b4332] transition-all">
        <div class="flex items-center gap-3">
          <div class="w-11 h-11 bg-[#e8f5e9] border border-[#2d6a4f] rounded-xl flex items-center justify-center text-2xl">
            💬
          </div>
          <span class="text-base font-bold text-[#1b4332]">오픈채팅방</span>
        </div>
        <div class="flex items-center gap-2">
          <button onclick="openModal('chat')" class="w-9 h-9 bg-[#d8f3dc] hover:bg-[#b7e4c7] border border-[#1b4332] rounded-lg flex items-center justify-center text-lg transition-colors" title="미리보기">
            👁️
          </button>
          <a href="https://open.kakao.com/me/ra_pi" target="_blank" class="w-9 h-9 bg-[#2d6a4f] hover:bg-[#1b4332] text-white border border-[#1b4332] rounded-lg flex items-center justify-center text-sm font-bold transition-colors">
            ➔
          </a>
        </div>
      </div>

      <!-- 3. 큐리어스 -->
      <div class="bg-white border-2 border-[#1b4332] rounded-2xl p-4 flex items-center justify-between shadow-[0_5px_0_#1b4332] hover:-translate-y-0.5 hover:shadow-[0_7px_0_#1b4332] transition-all">
        <div class="flex items-center gap-3">
          <div class="w-11 h-11 bg-[#e8f5e9] border border-[#2d6a4f] rounded-xl flex items-center justify-center text-2xl">
            🔍
          </div>
          <span class="text-base font-bold text-[#1b4332]">큐리어스</span>
        </div>
        <div class="flex items-center gap-2">
          <button onclick="openModal('curious')" class="w-9 h-9 bg-[#d8f3dc] hover:bg-[#b7e4c7] border border-[#1b4332] rounded-lg flex items-center justify-center text-lg transition-colors" title="미리보기">
            👁️
          </button>
          <a href="https://curious.quizby.me/ra_pi" target="_blank" class="w-9 h-9 bg-[#2d6a4f] hover:bg-[#1b4332] text-white border border-[#1b4332] rounded-lg flex items-center justify-center text-sm font-bold transition-colors">
            ➔
          </a>
        </div>
      </div>

    </main>

    <!-- 푸터 -->
    <footer class="mt-8 text-xs font-semibold text-[#2d6a4f] text-center">
      © SLOWRY PARK. All rights reserved.
    </footer>
  </div>

  <!-- 미리보기 모달 팝업 -->
  <div id="modal-backdrop" class="fixed inset-0 bg-black/50 backdrop-blur-xs hidden items-center justify-center p-4 z-50">
    <div class="bg-[#f2f9f4] border-2 border-[#1b4332] rounded-3xl w-full max-w-sm p-5 shadow-[0_8px_0_#1b4332] relative transform transition-all">
      
      <!-- 닫기 버튼 -->
      <button onclick="closeModal()" class="absolute top-4 right-4 w-8 h-8 rounded-full border border-[#1b4332] flex items-center justify-center text-sm font-bold text-[#1b4332] hover:bg-[#d8f3dc]">
        ✕
      </button>

      <!-- 모달 타이틀 영역 -->
      <div class="flex items-center gap-3 mb-4">
        <span id="modal-icon" class="text-3xl">🦎</span>
        <div>
          <h3 id="modal-title" class="text-lg font-extrabold text-[#1b4332]">라피 개인 블로그</h3>
        </div>
      </div>

      <!-- 모달 안쪽 연녹색 바탕 박스 -->
      <div class="bg-[#e8f5e9] border border-[#b7e4c7] rounded-2xl p-4 mb-5">
        <div id="modal-body" class="text-sm font-medium text-[#1b4332] leading-relaxed space-y-2">
          <!-- 스크립트로 내용이 동적 삽입됩니다 -->
        </div>
      </div>

      <!-- 모달 하단 버튼 -->
      <div class="flex gap-2">
        <button onclick="closeModal()" class="flex-1 py-2.5 bg-white border border-[#1b4332] rounded-xl text-sm font-bold text-[#1b4332] hover:bg-gray-50">
          닫기
        </button>
        <a id="modal-link" href="#" target="_blank" class="flex-1 py-2.5 bg-[#2d6a4f] hover:bg-[#1b4332] text-white border border-[#1b4332] rounded-xl text-sm font-bold flex items-center justify-center gap-1">
          직접 방문하기 ➔
        </a>
      </div>

    </div>
  </div>

  <script>
    const modalData = {
      blog: {
        icon: "🦎",
        title: "라피 개인 블로그",
        link: "https://m.blog.naver.com/ra-pi",
        content: `
          <p>🐾 규겸 및 권전 위주 올라운더</p>
          <p>🐾 모든 작품은 자유 연재</p>
        `
      },
      chat: {
        icon: "💬",
        title: "라피 오픈채팅",
        link: "https://open.kakao.com/me/ra_pi",
        content: `
          <p>💬 라피와 친해지고 싶거나, 하고 싶은 말이 있다면 찾아와주세요 :]</p>
          <p class="font-bold text-[#a71d2a] mt-2">⚠️ 기본 예의는 반드시 지켜주세요!</p>
        `
      },
      curious: {
        icon: "🔍",
        title: "Curious",
        link: "https://curious.quizby.me/ra_pi",
        content: `
          <p class="text-center py-2 font-semibold">SLOWRY PARK 도마뱀 라피에게 궁금한 걸 물어보세요! 👀✨</p>
        `
      }
    };

    function openModal(type) {
      const data = modalData[type];
      if (!data) return;

      document.getElementById('modal-icon').innerText = data.icon;
      document.getElementById('modal-title').innerText = data.title;
      document.getElementById('modal-body').innerHTML = data.content;
      document.getElementById('modal-link').href = data.link;

      const backdrop = document.getElementById('modal-backdrop');
      backdrop.classList.remove('hidden');
      backdrop.classList.add('flex');
    }

    function closeModal() {
      const backdrop = document.getElementById('modal-backdrop');
      backdrop.classList.remove('flex');
      backdrop.classList.add('hidden');
    }

    // 배경 클릭 시 모달 닫기
    document.getElementById('modal-backdrop').addEventListener('click', (e) => {
      if (e.target.id === 'modal-backdrop') {
        closeModal();
      }
    });
  </script>
</body>
</html>
