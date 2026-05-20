<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, maximum-scale=1.0, touch-action=manipulation">
  <title>Раннер • Персонажи и костюмы</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: linear-gradient(180deg, #1a1a2e 0%, #16213e 100%);
      min-height: 100vh; display: flex; justify-content: center; align-items: center;
      font-family: 'Courier New', Courier, monospace;
      touch-action: manipulation; user-select: none;
    }
    .game-wrapper {
      position: relative; display: flex; flex-direction: column;
      align-items: center; gap: 15px;
    }
    .game-container {
      position: relative; background-color: #f7f7f7; border-radius: 24px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.6), inset 0 0 10px rgba(255,255,255,0.2);
      overflow: hidden; width: 100%; max-width: 800px;
    }
    canvas { display: block; width: 100%; height: auto; background-color: #ffffff; cursor: pointer; touch-action: manipulation; }
    .record-panel {
      position: absolute; top: 12px; right: 20px; background: rgba(0,0,0,0.7);
      backdrop-filter: blur(6px); color: #fdd835; padding: 8px 18px;
      border-radius: 40px; font-weight: bold; font-size: 1.2rem; letter-spacing: 1px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3); border: 1px solid rgba(255,255,255,0.25);
      display: flex; align-items: center; gap: 6px; z-index: 10; pointer-events: none;
    }
    .music-toggle {
      position: absolute; top: 12px; left: 20px; background: rgba(0,0,0,0.7);
      backdrop-filter: blur(6px); color: white; border: 1px solid rgba(255,255,255,0.25);
      border-radius: 40px; padding: 8px 14px; font-weight: bold; font-size: 1.1rem;
      cursor: pointer; z-index: 20; letter-spacing: 1px; transition: background 0.2s;
      font-family: 'Courier New', monospace; white-space: nowrap; box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    .pause-button {
      position: absolute; top: 12px; left: 50%; transform: translateX(-50%);
      background: rgba(0,0,0,0.7); backdrop-filter: blur(6px); color: white;
      border: 1px solid rgba(255,255,255,0.25); border-radius: 40px; padding: 8px 18px;
      font-weight: bold; font-size: 1.1rem; cursor: pointer; z-index: 20; letter-spacing: 1px;
      transition: background 0.2s; font-family: 'Courier New', monospace; white-space: nowrap;
    }
    .restart-hint {
      position: absolute; bottom: 20px; left: 50%; transform: translateX(-50%);
      background: rgba(0,0,0,0.6); color: #ddd; padding: 6px 18px; border-radius: 20px;
      font-size: 0.9rem; backdrop-filter: blur(4px); white-space: nowrap; z-index: 10; pointer-events: none; display: none;
    }
    .continue-overlay {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0,0,0,0.7); display: flex; justify-content: center; align-items: center; z-index: 25; display: none;
    }
    .continue-panel {
      background: #1e1e2e; border: 2px solid #fdd835; border-radius: 20px;
      padding: 20px 30px; text-align: center; color: white; box-shadow: 0 10px 30px rgba(0,0,0,0.8);
    }
    .continue-panel h3 { color: #fdd835; margin-bottom: 10px; font-size: 1.3rem; }
    .continue-panel p { margin-bottom: 15px; font-size: 1rem; }
    .continue-panel .timer { font-size: 2rem; color: #ff5252; font-weight: bold; margin-bottom: 15px; }
    .continue-buttons { display: flex; gap: 15px; justify-content: center; }
    .continue-btn { background: #4caf50; color: white; border: none; padding: 10px 20px; border-radius: 25px; font-weight: bold; cursor: pointer; font-family: 'Courier New', monospace; font-size: 1rem; }
    .decline-btn { background: #f44336; color: white; border: none; padding: 10px 20px; border-radius: 25px; font-weight: bold; cursor: pointer; font-family: 'Courier New', monospace; font-size: 1rem; }
    .in-game-menu-btn {
      position: absolute; top: 60px; left: 50%; transform: translateX(-50%);
      background: rgba(0,0,0,0.7); backdrop-filter: blur(6px); color: #fdd835;
      border: 1px solid rgba(255,255,255,0.25); border-radius: 40px; padding: 8px 18px;
      font-weight: bold; font-size: 1rem; cursor: pointer; z-index: 20; letter-spacing: 1px;
      transition: background 0.2s; font-family: 'Courier New', monospace; display: none;
    }
    .menu-overlay {
      position: absolute; top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0,0,0,0.85); backdrop-filter: blur(8px); display: flex;
      justify-content: center; align-items: center; z-index: 30; border-radius: 24px;
    }
    .menu-panel {
      background: #1e1e2e; border: 2px solid #555; border-radius: 24px; padding: 20px;
      width: 90%; max-width: 600px; color: white; text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.7); max-height: 80vh; overflow-y: auto;
    }
    .menu-panel h2 { margin-bottom: 15px; font-size: 1.8rem; color: #fdd835; }
    .currencies-menu { display: flex; justify-content: center; gap: 20px; margin-bottom: 15px; font-weight: bold; font-size: 1.1rem; }
    .currencies-menu .crystals { color: #80d8ff; }
    .currencies-menu .cryptostals { color: #ff80ab; }
    .menu-tabs { display: flex; gap: 10px; margin-bottom: 20px; flex-wrap: wrap; justify-content: center; }
    .menu-tab { background: #333; color: white; border: none; padding: 10px 16px; border-radius: 20px; cursor: pointer; font-family: 'Courier New', monospace; font-weight: bold; font-size: 0.8rem; }
    .menu-tab.active { background: #fdd835; color: #222; }
    .menu-content { text-align: left; }
    .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
    .card { background: #333; border-radius: 16px; padding: 10px; cursor: pointer; transition: all 0.2s; border: 2px solid transparent; text-align: center; }
    .card.locked { opacity: 0.5; cursor: not-allowed; filter: grayscale(0.6); }
    .card.selected { border-color: #fdd835; box-shadow: 0 0 15px rgba(253,216,53,0.5); }
    .card:hover:not(.locked) { background: #444; }
    .preview { width: 50px; height: 50px; margin: 0 auto 6px; border-radius: 10px; }
    .card-name { font-weight: bold; font-size: 0.8rem; }
    .card-price { font-size: 0.7rem; }
    .card-price.crystals { color: #80d8ff; }
    .card-price.cryptostals { color: #ff80ab; }
    .achievement-list { display: flex; flex-direction: column; gap: 10px; }
    .achievement-item { background: #2a2a3a; padding: 10px 15px; border-radius: 12px; display: flex; justify-content: space-between; align-items: center; }
    .achievement-item.claimed { opacity: 0.6; }
    .achievement-reward { font-size: 0.8rem; }
    .achievement-reward.crystals { color: #80d8ff; }
    .achievement-reward.cryptostals { color: #ff80ab; }
    .quest-item { background: #2a2a3a; padding: 10px 15px; border-radius: 12px; margin-bottom: 8px; font-size: 0.85rem; }
    .pass-item { background: #2a2a3a; padding: 10px 15px; border-radius: 12px; margin-bottom: 8px; font-size: 0.85rem; display: flex; justify-content: space-between; align-items: center; }
    .pass-timer { font-size: 0.75rem; color: #aaa; margin-bottom: 10px; text-align: center; }
    .pass-progress { background: #444; border-radius: 10px; height: 10px; margin: 5px 0; overflow: hidden; }
    .pass-progress-fill { background: #fdd835; height: 100%; transition: width 0.3s; }
    .btn { background: #fdd835; color: #222; border: none; padding: 8px 16px; border-radius: 20px; font-weight: bold; cursor: pointer; font-family: 'Courier New', monospace; }
    .btn:disabled { background: #666; cursor: not-allowed; }
    .close-btn { margin-top: 20px; }
    .promo-input {
      background: #333; border: 2px solid #555; color: white; padding: 12px;
      border-radius: 12px; font-size: 1.2rem; text-align: center; font-family: 'Courier New', monospace;
      width: 100%; margin: 10px 0; letter-spacing: 2px; transition: border-color 0.3s;
    }
    .promo-input:focus { outline: none; border-color: #fdd835; }
    .promo-message { margin: 10px 0; padding: 10px; border-radius: 12px; font-weight: bold; display: none; }
    .promo-message.success { background: #1b5e20; color: #81c784; display: block; }
    .promo-message.error { background: #b71c1c; color: #ef9a9a; display: block; }
  </style>
</head>
<body>
<div class="game-wrapper">
  <div class="game-container" id="gameContainer">
    <canvas id="gameCanvas" width="800" height="400"></canvas>
    <button class="music-toggle" id="musicToggle">🔊</button>
    <div class="record-panel">🏆 <span id="recordDisplay">0</span></div>
    <button class="pause-button" id="pauseButton">⏸️ Пауза</button>
    <button class="in-game-menu-btn" id="inGameMenuBtn">🏠 В меню</button>
    <div class="restart-hint" id="restartHint">🔄 Коснитесь / Пробел, чтобы начать заново</div>
    <div class="continue-overlay" id="continueOverlay">
      <div class="continue-panel">
        <h3>💀 Вы проиграли!</h3>
        <p>Хотите продолжить за 💎100 кристаллов?</p>
        <div class="timer" id="continueTimer">8</div>
        <div class="continue-buttons">
          <button class="continue-btn" id="continueYes">✅ Да (💎100)</button>
          <button class="decline-btn" id="continueNo">❌ Нет</button>
        </div>
      </div>
    </div>
    <div class="menu-overlay" id="menuOverlay" style="display: none;">
      <div class="menu-panel" id="menuPanel"></div>
    </div>
  </div>
</div>

<script>
(function() {
  const canvas = document.getElementById('gameCanvas');
  const ctx = canvas.getContext('2d');
  
  const recordDisplay = document.getElementById('recordDisplay');
  const restartHint = document.getElementById('restartHint');
  const pauseButton = document.getElementById('pauseButton');
  const inGameMenuBtn = document.getElementById('inGameMenuBtn');
  const menuOverlay = document.getElementById('menuOverlay');
  const menuPanel = document.getElementById('menuPanel');
  const musicToggle = document.getElementById('musicToggle');
  const continueOverlay = document.getElementById('continueOverlay');
  const continueTimer = document.getElementById('continueTimer');
  const continueYes = document.getElementById('continueYes');
  const continueNo = document.getElementById('continueNo');

  const CANVAS_WIDTH = 800;
  const CANVAS_HEIGHT = 400;
  const GROUND_Y = 320;

  let gameOver = false, paused = false, menuOpen = false, continueActive = false;
  let continueSeconds = 8, continueInterval = null;
  let score = 0, highScore = 0, crystals = 0, cryptostals = 0;
  let passXP = 0, passLevel = 1;
  let lastPassReset = '';
  let stats = { jumps: 0, deaths: 0, crystalsCollected: 0, totalScore: 0 };
  let speedBoostActive = false, speedBoostTimer = 0;
  let doubleCrystalsActive = false, doubleCrystalsTimer = 0;
  let lootboxReady = false, lastLootboxDay = '';
  let fireworks = [];
  let baseSpeed = 6.5, currentSpeed = baseSpeed;

  let character = {
    x: 120, y: GROUND_Y - 54,
    width: 44, height: 54,
    vy: 0, gravity: 0.8, jumpPower: -14,
    grounded: true
  };

  let obstacles = [], birds = [], crystalsOnMap = [];
  let spawnTimer = 0, nextSpawnIn = 70, birdSpawnTimer = 0, crystalSpawnTimer = 0;
  
  let stars = [];
  for (let i = 0; i < 60; i++) {
    stars.push({
      x: Math.random() * CANVAS_WIDTH,
      y: Math.random() * GROUND_Y * 0.7,
      size: Math.random() * 2 + 0.5,
      twinkle: Math.random() * Math.PI * 2
    });
  }

  // Персонажи с уникальными особенностями
  const CHARACTERS = {
    LEO: { 
      id: 'leo', name: 'Лео', type: 'animal', 
      color: '#ff9800', secondary: '#e65100', belly: '#ffcc80', earInner: '#ffab91',
      hasMane: true, maneColor: '#ff6d00',
      earShape: 'round', tailType: 'long',
      specialFeature: 'mane'
    },
    DINO: { 
      id: 'dino', name: 'Дино', type: 'animal', 
      color: '#4caf50', secondary: '#2e7d32', belly: '#a5d6a7', earInner: '#81c784',
      hasSpikes: true, spikeColor: '#1b5e20',
      earShape: 'spikes', tailType: 'short_thick',
      specialFeature: 'spikes'
    },
    CAT: { 
      id: 'cat', name: 'Котик', type: 'animal', 
      color: '#9e9e9e', secondary: '#616161', belly: '#e0e0e0', earInner: '#f48fb1',
      hasWhiskers: true, whiskerColor: '#eceff1',
      earShape: 'pointy', tailType: 'curly',
      specialFeature: 'whiskers'
    },
    DOG: { 
      id: 'dog', name: 'Собачка', type: 'animal', 
      color: '#8d6e63', secondary: '#5d4037', belly: '#d7ccc8', earInner: '#bcaaa4',
      hasTongue: true, tongueColor: '#ff5252',
      earShape: 'floppy', tailType: 'waggy',
      specialFeature: 'tongue'
    },
    PANTHER: { 
      id: 'panther', name: 'Пантера', type: 'animal', 
      color: '#1a1a1a', secondary: '#333', belly: '#2a2a2a', earInner: '#444',
      hasTeeth: true, elongated: true,
      earShape: 'small_round', tailType: 'long_sleek',
      specialFeature: 'teeth'
    },
    BEAR: { 
      id: 'bear', name: 'Медвежонок', type: 'animal', 
      color: '#8d6e63', secondary: '#5d4037', belly: '#d7ccc8', earInner: '#bcaaa4',
      chubby: true, hasClaws: true, clawColor: '#3e2723',
      earShape: 'small_round', tailType: 'tiny',
      specialFeature: 'chubby'
    },
    FOX: { 
      id: 'fox', name: 'Лис', type: 'animal', 
      color: '#ff6d00', secondary: '#bf360c', belly: '#ffcc80', earInner: '#ffffff',
      pointyNose: true, hasWhiteTips: true, whiteTipColor: '#ffffff',
      earShape: 'pointy_tall', tailType: 'bushy',
      specialFeature: 'bushy_tail'
    },
    RABBIT: { 
      id: 'rabbit', name: 'Кролик', type: 'animal', 
      color: '#f5f5f5', secondary: '#e0e0e0', belly: '#fff', earInner: '#ff80ab',
      jumpBonus: true, hasFluffyTail: true, fluffyTailColor: '#ffffff',
      earShape: 'long_ears', tailType: 'fluffy_ball',
      specialFeature: 'long_ears'
    },
    SPIDERMAN: { 
      id: 'spiderman', name: 'Человек-паук', type: 'humanoid', price: 5000, 
      color: '#c62828', secondary: '#1565c0', belly: '#2196f3',
      spiderEmblem: true,
      specialFeature: 'spider_emblem'
    },
    SUN: { 
      id: 'sun', name: 'Солнце', type: 'star', price: 7000, 
      color: '#ffd600', secondary: '#ff8f00', belly: '#ffea00',
      hasRays: true,
      specialFeature: 'rays'
    },
    EARTH: { 
      id: 'earth', name: 'Земля', type: 'planet', price: 3000, 
      color: '#2196f3', secondary: '#4caf50', belly: '#fff',
      earthColors: true,
      specialFeature: 'continents'
    },
    MOON: { 
      id: 'moon', name: 'Луна', type: 'planet', price: 2500, 
      color: '#9e9e9e', secondary: '#757575', belly: '#bdbdbd',
      moonCraters: true,
      specialFeature: 'craters'
    }
  };

  let currentCharacter = CHARACTERS.LEO;
  let ownedCharacters = new Set(['leo', 'dino', 'cat', 'dog', 'panther', 'bear', 'fox', 'rabbit']);

  const ALL_SKINS = {
    GOLDEN: { id: 'golden', name: 'Золотой', price: 1500, color: '#ffd700', secondary: '#b8860b', belly: '#fff176', earInner: '#ffec80', currency: 'crystals' },
    RARE: { id: 'rare', name: 'Редкий', price: 2000, color: '#2196f3', secondary: '#0d47a1', belly: '#90caf9', earInner: '#64b5f6', currency: 'crystals' },
    EPIC: { id: 'epic', name: 'Эпический', price: 3000, color: '#9c27b0', secondary: '#6a1b9a', belly: '#ce93d8', earInner: '#e1bee7', currency: 'crystals' },
    MYTHIC: { id: 'mythic', name: 'Мифический', price: 5000, color: '#f44336', secondary: '#b71c1c', belly: '#ef9a9a', earInner: '#ffcdd2', currency: 'crystals' },
    LEGENDARY: { id: 'legendary', name: 'Легендарный', price: 7000, color: '#ffea00', secondary: '#ffab00', belly: '#fff9c4', earInner: '#ffff8d', currency: 'crystals' },
    COSMIC: { id: 'cosmic', name: 'Космический', price: 10000, color: '#7c4dff', secondary: '#651fff', belly: '#b388ff', earInner: '#d1c4e9', currency: 'crystals' },
    CHROMATIC: { id: 'chromatic', name: 'Хроматический', price: 15000, color: '#ff4081', secondary: '#00e5ff', belly: '#ffffff', earInner: '#ffffff', chromatic: true, currency: 'crystals' },
    ULTRA: { id: 'ultra', name: 'Ультралегендарный', price: 50000, color: '#ff4081', secondary: '#00e5ff', belly: '#ff80ab', earInner: '#f8bbd0', ultra: true, currency: 'crystals' },
    FLAME: { id: 'flame', name: 'Пламенный', color: '#ff6d00', secondary: '#d50000', belly: '#ffab40', earInner: '#ff5252', flame: true, currency: 'crystals' },
    ROBO: { id: 'robo', name: 'Робо', price: 30000, color: '#9e9e9e', secondary: '#616161', belly: '#bdbdbd', earInner: '#757575', roboEyes: true, currency: 'crystals' },
    TECH: { id: 'tech', name: 'Технарь', price: 40000, color: '#4fc3f7', secondary: '#0288d1', belly: '#b3e5fc', earInner: '#81d4fa', techGlasses: true, currency: 'crystals' },
    SMART: { id: 'smart', name: 'Умный', price: 7000, color: '#fff', secondary: '#e0e0e0', belly: '#f5f5f5', earInner: '#eee', whiteShirt: true, tie: true, currency: 'cryptostals' }
  };

  let activeSkin = null;
  let ownedSkins = new Set();

  // Система промокодов
  const PROMOCODES = {
    'GOLDEN2026': {
      reward: { type: 'skin', skinId: 'golden' },
      description: 'Золотой скин',
      oneTime: true
    },
    'KOSMOMAY': {
      reward: { type: 'skin', skinId: 'cosmic' },
      description: 'Космический скин',
      oneTime: true
    },
    'KRIPT2026': {
      reward: { type: 'cryptostals', amount: 5000 },
      description: '5000 криптосталлов',
      oneTime: true
    },
    'KRISTMAY': {
      reward: { type: 'crystals', amount: 12000 },
      description: '12000 кристаллов',
      oneTime: true
    },
    'FAILPRISE': {
      reward: { type: 'combo', skinId: 'flame', crystals: 3000 },
      description: 'Пламенный скин + 3000 кристаллов',
      oneTime: true
    }
  };
  let usedPromocodes = new Set();

  const ACHIEVEMENTS = [
    { id: 'beginner', name: 'Начинающий', req: 5000, reward: 400, currency: 'crystals' },
    { id: 'good', name: 'Молодец', req: 15000, reward: 1000, currency: 'crystals' },
    { id: 'advanced', name: 'Продвинутый', req: 25000, reward: 2000, currency: 'crystals' },
    { id: 'gamer', name: 'Игроман', req: 40000, reward: 4000, currency: 'crystals' },
    { id: 'elder', name: 'Старейшина', req: 50000, reward: 8000, currency: 'crystals' },
    { id: 'champion', name: 'Чемпион', req: 100000, reward: 10000, currency: 'crystals' }
  ];
  let claimedAchievements = new Set();

  let dailyQuests = [], weeklyQuests = [];
  let dailyClaimed = [false, false, false, false];
  let weeklyClaimed = [false, false];
  let lastDailyReset = '', lastWeeklyReset = '';

  let passQuests = [];
  let passClaimed = [];
  const PASS_XP_PER_LEVEL = 400;
  const PASS_RESET_HOURS = 4;

  let audioCtx = null, musicGain = null, musicPlaying = false;

  function initAudio() {
    if (!audioCtx) {
      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      musicGain = audioCtx.createGain();
      musicGain.gain.value = 0.15;
      musicGain.connect(audioCtx.destination);
    }
    if (audioCtx.state === 'suspended') audioCtx.resume();
  }

  function playJumpSound() {
    if (!audioCtx) return;
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.connect(gain);
    gain.connect(audioCtx.destination);
    osc.type = 'sine';
    osc.frequency.setValueAtTime(400, audioCtx.currentTime);
    osc.frequency.exponentialRampToValueAtTime(700, audioCtx.currentTime + 0.1);
    gain.gain.setValueAtTime(0.3, audioCtx.currentTime);
    gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.2);
    osc.start(audioCtx.currentTime);
    osc.stop(audioCtx.currentTime + 0.2);
  }

  function playDeathSound() {
    if (!audioCtx) return;
    const osc = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.connect(gain);
    gain.connect(audioCtx.destination);
    osc.type = 'sawtooth';
    osc.frequency.setValueAtTime(300, audioCtx.currentTime);
    osc.frequency.exponentialRampToValueAtTime(80, audioCtx.currentTime + 0.5);
    gain.gain.setValueAtTime(0.3, audioCtx.currentTime);
    gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.6);
    osc.start(audioCtx.currentTime);
    osc.stop(audioCtx.currentTime + 0.6);
  }

  function startMusic() {
    if (!audioCtx) initAudio();
    if (musicPlaying) return;
    musicPlaying = true;
    musicToggle.textContent = '🔊';
  }

  function stopMusic() {
    musicPlaying = false;
    musicToggle.textContent = '🔇';
  }

  function toggleMusic() {
    if (musicPlaying) stopMusic();
    else startMusic();
  }

  function loadData() {
    try {
      highScore = parseInt(localStorage.getItem('runnerHighScore')) || 0;
      crystals = parseInt(localStorage.getItem('runnerCrystals')) || 0;
      cryptostals = parseInt(localStorage.getItem('runnerCryptostals')) || 0;
      passXP = parseInt(localStorage.getItem('runnerPassXP')) || 0;
      passLevel = parseInt(localStorage.getItem('runnerPassLevel')) || 1;
      lastPassReset = localStorage.getItem('runnerLastPassReset') || '';
      ownedSkins = new Set(JSON.parse(localStorage.getItem('runnerOwnedSkins') || '[]'));
      ownedCharacters = new Set(JSON.parse(localStorage.getItem('runnerOwnedCharacters') || '["leo","dino","cat","dog","panther","bear","fox","rabbit"]'));
      claimedAchievements = new Set(JSON.parse(localStorage.getItem('runnerAchievements') || '[]'));
      passClaimed = JSON.parse(localStorage.getItem('runnerPassClaimed') || '[]');
      usedPromocodes = new Set(JSON.parse(localStorage.getItem('runnerUsedPromocodes') || '[]'));
      const charId = localStorage.getItem('runnerCharacter');
      currentCharacter = Object.values(CHARACTERS).find(c => c.id === charId) || CHARACTERS.LEO;
      const skinId = localStorage.getItem('runnerActiveSkin');
      activeSkin = skinId ? (ALL_SKINS[skinId.toUpperCase()] || null) : null;
      dailyClaimed = JSON.parse(localStorage.getItem('runnerDailyClaimed') || '[false,false,false,false]');
      weeklyClaimed = JSON.parse(localStorage.getItem('runnerWeeklyClaimed') || '[false,false]');
      lastDailyReset = localStorage.getItem('runnerDailyReset') || '';
      lastWeeklyReset = localStorage.getItem('runnerWeeklyReset') || '';
      stats = JSON.parse(localStorage.getItem('runnerStats') || '{"jumps":0,"deaths":0,"crystalsCollected":0,"totalScore":0}');
      lastLootboxDay = localStorage.getItem('runnerLootboxDay') || '';
      lootboxReady = lastLootboxDay !== new Date().toDateString();
    } catch (e) {
      console.error('Error loading data:', e);
    }
  }

  function saveData() {
    try {
      localStorage.setItem('runnerHighScore', highScore);
      localStorage.setItem('runnerCrystals', crystals);
      localStorage.setItem('runnerCryptostals', cryptostals);
      localStorage.setItem('runnerPassXP', passXP);
      localStorage.setItem('runnerPassLevel', passLevel);
      localStorage.setItem('runnerLastPassReset', lastPassReset);
      localStorage.setItem('runnerOwnedSkins', JSON.stringify([...ownedSkins]));
      localStorage.setItem('runnerOwnedCharacters', JSON.stringify([...ownedCharacters]));
      localStorage.setItem('runnerAchievements', JSON.stringify([...claimedAchievements]));
      localStorage.setItem('runnerPassClaimed', JSON.stringify(passClaimed));
      localStorage.setItem('runnerUsedPromocodes', JSON.stringify([...usedPromocodes]));
      localStorage.setItem('runnerCharacter', currentCharacter.id);
      localStorage.setItem('runnerActiveSkin', activeSkin ? activeSkin.id : '');
      localStorage.setItem('runnerDailyClaimed', JSON.stringify(dailyClaimed));
      localStorage.setItem('runnerWeeklyClaimed', JSON.stringify(weeklyClaimed));
      localStorage.setItem('runnerDailyReset', lastDailyReset);
      localStorage.setItem('runnerWeeklyReset', lastWeeklyReset);
      localStorage.setItem('runnerStats', JSON.stringify(stats));
      localStorage.setItem('runnerLootboxDay', lastLootboxDay);
    } catch (e) {
      console.error('Error saving data:', e);
    }
  }

  function updateUI() {
    recordDisplay.textContent = highScore;
  }

  function activatePromocode(code) {
    const upperCode = code.toUpperCase().trim();
    
    if (!upperCode) {
      return { success: false, message: 'Введите промокод!' };
    }
    
    const promo = PROMOCODES[upperCode];
    if (!promo) {
      return { success: false, message: 'Промокод не найден!' };
    }
    
    if (promo.oneTime && usedPromocodes.has(upperCode)) {
      return { success: false, message: 'Вы уже использовали этот промокод!' };
    }
    
    if (promo.reward.type === 'skin') {
      const skinId = promo.reward.skinId;
      if (ownedSkins.has(skinId)) {
        return { success: false, message: 'У вас уже есть этот скин!' };
      }
      ownedSkins.add(skinId);
      usedPromocodes.add(upperCode);
      saveData();
      addFireworks();
      return { success: true, message: `Промокод активирован! Получен скин: ${ALL_SKINS[skinId.toUpperCase()].name}` };
    }
    
    if (promo.reward.type === 'crystals') {
      crystals += promo.reward.amount;
      usedPromocodes.add(upperCode);
      saveData();
      addFireworks();
      return { success: true, message: `Промокод активирован! Получено ${promo.reward.amount} кристаллов` };
    }
    
    if (promo.reward.type === 'cryptostals') {
      cryptostals += promo.reward.amount;
      usedPromocodes.add(upperCode);
      saveData();
      addFireworks();
      return { success: true, message: `Промокод активирован! Получено ${promo.reward.amount} криптосталлов` };
    }
    
    if (promo.reward.type === 'combo') {
      const skinId = promo.reward.skinId;
      if (ownedSkins.has(skinId)) {
        return { success: false, message: 'У вас уже есть этот скин!' };
      }
      ownedSkins.add(skinId);
      crystals += promo.reward.crystals;
      usedPromocodes.add(upperCode);
      saveData();
      addFireworks();
      return { success: true, message: `Промокод активирован! Получен скин ${ALL_SKINS[skinId.toUpperCase()].name} и ${promo.reward.crystals} кристаллов` };
    }
    
    return { success: false, message: 'Ошибка активации промокода!' };
  }

  function addFireworks() {
    for (let i = 0; i < 30; i++) {
      fireworks.push({
        x: Math.random() * CANVAS_WIDTH,
        y: Math.random() * CANVAS_HEIGHT * 0.5,
        vx: (Math.random() - 0.5) * 4,
        vy: -Math.random() * 6 - 2,
        life: 40 + Math.random() * 30,
        color: ['#ff0', '#f00', '#0f0', '#00f', '#f0f'][Math.floor(Math.random() * 5)]
      });
    }
  }

  function generateDailyQuests() {
    const templates = [
      { desc: 'Дойди до 3000', target: 3000 },
      { desc: 'Дойди до 5000', target: 5000 },
      { desc: 'Дойди до 8000', target: 8000 },
      { desc: 'Дойди до 10000', target: 10000 },
      { desc: 'Дойди до 12000', target: 12000 },
      { desc: 'Дойди до 15000', target: 15000 }
    ];
    dailyQuests = [];
    const used = new Set();
    while (dailyQuests.length < 4) {
      const q = templates[Math.floor(Math.random() * templates.length)];
      if (!used.has(q.desc)) {
        used.add(q.desc);
        dailyQuests.push({ ...q });
      }
    }
    dailyClaimed = [false, false, false, false];
  }

  function generateWeeklyQuests() {
    const templates = [
      { desc: 'Дойди до 25000', target: 25000 },
      { desc: 'Дойди до 35000', target: 35000 },
      { desc: 'Дойди до 50000', target: 50000 },
      { desc: 'Побей рекорд', target: 'record' },
      { desc: 'Дойди до 75000', target: 75000 }
    ];
    weeklyQuests = [];
    const used = new Set();
    while (weeklyQuests.length < 2) {
      const q = templates[Math.floor(Math.random() * templates.length)];
      if (!used.has(q.desc)) {
        used.add(q.desc);
        weeklyQuests.push({ ...q });
      }
    }
    weeklyClaimed = [false, false];
  }

  function generatePassQuests() {
    const quests = [
      { desc: 'Дойди до счёта 10000', type: 'score', target: 10000, xp: 150 },
      { desc: 'Дойди до счёта 25000', type: 'score', target: 25000, xp: 200 },
      { desc: 'Дойди до счёта 50000', type: 'score', target: 50000, xp: 300 },
      { desc: 'Побей свой рекорд', type: 'record', xp: 200 }
    ];
    passQuests = [];
    const used = new Set();
    while (passQuests.length < 4) {
      const q = quests[Math.floor(Math.random() * quests.length)];
      if (!used.has(q.desc)) {
        used.add(q.desc);
        passQuests.push({ ...q });
      }
    }
    passClaimed = new Array(passQuests.length).fill(false);
    lastPassReset = new Date().toISOString();
    saveData();
  }

  function resetPassIfNeeded() {
    const now = new Date();
    if (lastPassReset) {
      const lastReset = new Date(lastPassReset);
      const hoursPassed = (now - lastReset) / (1000 * 60 * 60);
      if (hoursPassed >= PASS_RESET_HOURS) generatePassQuests();
    } else {
      generatePassQuests();
    }
  }

  function getPassTimeRemaining() {
    if (!lastPassReset) return '00:00:00';
    const now = new Date();
    const lastReset = new Date(lastPassReset);
    const nextReset = new Date(lastReset.getTime() + PASS_RESET_HOURS * 60 * 60 * 1000);
    const remaining = nextReset - now;
    if (remaining <= 0) return 'Обновление...';
    const hours = Math.floor(remaining / (1000 * 60 * 60));
    const minutes = Math.floor((remaining % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((remaining % (1000 * 60)) / 1000);
    return `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
  }

  function checkPassQuests() {
    passQuests.forEach((q, i) => {
      if (!passClaimed[i]) {
        let completed = false;
        if (q.type === 'score' && score >= q.target) completed = true;
        else if (q.type === 'record' && highScore > 0) completed = true;
        if (completed) {
          passClaimed[i] = true;
          passXP += q.xp;
          while (passXP >= PASS_XP_PER_LEVEL) {
            passXP -= PASS_XP_PER_LEVEL;
            passLevel++;
            crystals += 500;
          }
          saveData();
        }
      }
    });
  }

  function checkAchievements() {
    ACHIEVEMENTS.forEach(a => {
      if (highScore >= a.req && !claimedAchievements.has(a.id)) {
        claimedAchievements.add(a.id);
        if (a.currency === 'crystals') crystals += a.reward;
        else cryptostals += a.reward;
        addFireworks();
        saveData();
      }
    });
  }

  function checkQuestCompletion() {
    dailyQuests.forEach((q, i) => {
      if (!dailyClaimed[i] && typeof q.target === 'number' && score >= q.target) {
        dailyClaimed[i] = true;
        crystals += 500;
        saveData();
      }
    });
    weeklyQuests.forEach((q, i) => {
      if (!weeklyClaimed[i]) {
        if (q.target === 'record' && highScore > 0) {
          weeklyClaimed[i] = true;
          crystals += 2000;
          saveData();
        } else if (typeof q.target === 'number' && score >= q.target) {
          weeklyClaimed[i] = true;
          crystals += 2000;
          saveData();
        }
      }
    });
  }

  function resetGame() {
    character.y = GROUND_Y - character.height;
    character.vy = 0;
    character.grounded = true;
    obstacles = [];
    birds = [];
    crystalsOnMap = [];
    spawnTimer = 0;
    birdSpawnTimer = 0;
    crystalSpawnTimer = 0;
    nextSpawnIn = 70 + Math.floor(Math.random() * 60);
    score = 0;
    currentSpeed = baseSpeed;
    gameOver = false;
    paused = false;
    continueActive = false;
    restartHint.style.display = 'none';
    continueOverlay.style.display = 'none';
    if (continueInterval) clearInterval(continueInterval);
    inGameMenuBtn.style.display = 'none';
    pauseButton.textContent = '⏸️ Пауза';
    pauseButton.style.display = 'block';
    speedBoostActive = false;
    speedBoostTimer = 0;
    doubleCrystalsActive = false;
    doubleCrystalsTimer = 0;
    fireworks = [];
  }

  function triggerGameOver() {
    gameOver = true;
    stats.deaths++;
    playDeathSound();
    saveData();
    if (crystals >= 100 && !continueActive) {
      continueActive = true;
      continueOverlay.style.display = 'flex';
      continueSeconds = 8;
      continueTimer.textContent = '8';
      restartHint.style.display = 'none';
      pauseButton.style.display = 'none';
      inGameMenuBtn.style.display = 'none';
      continueInterval = setInterval(() => {
        continueSeconds--;
        continueTimer.textContent = continueSeconds;
        if (continueSeconds <= 0) {
          clearInterval(continueInterval);
          continueActive = false;
          continueOverlay.style.display = 'none';
          restartHint.style.display = 'block';
          pauseButton.style.display = 'block';
        }
      }, 1000);
    } else {
      restartHint.style.display = 'block';
    }
  }

  function continueGame() {
    if (!continueActive || crystals < 100) return;
    crystals -= 100;
    continueActive = false;
    continueOverlay.style.display = 'none';
    if (continueInterval) clearInterval(continueInterval);
    gameOver = false;
    character.y = GROUND_Y - character.height;
    character.vy = 0;
    character.grounded = true;
    obstacles = obstacles.filter(o => o.x > character.x + character.width + 50);
    birds = birds.filter(b => b.x > character.x + character.width + 50);
    saveData();
    updateUI();
    pauseButton.style.display = 'block';
    pauseButton.textContent = '⏸️ Пауза';
  }

  function declineContinue() {
    continueActive = false;
    continueOverlay.style.display = 'none';
    if (continueInterval) clearInterval(continueInterval);
    restartHint.style.display = 'block';
    pauseButton.style.display = 'block';
  }

  function attemptJump() {
    if (continueActive) return;
    if (gameOver && !continueActive) {
      resetGame();
      return;
    }
    if (menuOpen) return;
    if (paused) {
      paused = false;
      pauseButton.textContent = '⏸️ Пауза';
      inGameMenuBtn.style.display = 'none';
      return;
    }
    if (character.grounded) {
      character.vy = currentCharacter.jumpBonus ? -16 : -14;
      character.grounded = false;
      stats.jumps++;
      playJumpSound();
    }
  }

  function togglePause() {
    if (continueActive) return;
    if (gameOver && !continueActive) {
      resetGame();
      return;
    }
    if (menuOpen) return;
    paused = !paused;
    if (paused) {
      pauseButton.textContent = '▶️ Продолжить';
      inGameMenuBtn.style.display = 'block';
    } else {
      pauseButton.textContent = '⏸️ Пауза';
      inGameMenuBtn.style.display = 'none';
    }
  }

  function openMenu() {
    if (continueActive) return;
    menuOpen = true;
    paused = true;
    menuOverlay.style.display = 'flex';
    pauseButton.style.display = 'none';
    inGameMenuBtn.style.display = 'none';
    continueOverlay.style.display = 'none';
    renderMenu('characters');
  }

  function closeMenu() {
    menuOpen = false;
    paused = false;
    menuOverlay.style.display = 'none';
    pauseButton.style.display = 'block';
    pauseButton.textContent = '⏸️ Пауза';
  }

  function renderMenu(tab) {
    resetPassIfNeeded();
    const today = new Date().toDateString();
    if (lastLootboxDay !== today) {
      lootboxReady = true;
      lastLootboxDay = today;
      saveData();
    }

    menuPanel.innerHTML = `
      <h2>🏠 Главное меню</h2>
      <div class="currencies-menu">
        <span class="crystals">💎 ${crystals}</span>
        <span class="cryptostals">🔮 ${cryptostals}</span>
      </div>
      <div class="menu-tabs">
        <button class="menu-tab ${tab === 'characters' ? 'active' : ''}" data-tab="characters">🐾</button>
        <button class="menu-tab ${tab === 'shop' ? 'active' : ''}" data-tab="shop">🛒</button>
        <button class="menu-tab ${tab === 'skins' ? 'active' : ''}" data-tab="skins">🎨</button>
        <button class="menu-tab ${tab === 'achievements' ? 'active' : ''}" data-tab="achievements">🏅</button>
        <button class="menu-tab ${tab === 'quests' ? 'active' : ''}" data-tab="quests">📋</button>
        <button class="menu-tab ${tab === 'pass' ? 'active' : ''}" data-tab="pass">🌵</button>
        <button class="menu-tab ${tab === 'stats' ? 'active' : ''}" data-tab="stats">📊</button>
        <button class="menu-tab ${tab === 'promo' ? 'active' : ''}" data-tab="promo" style="background:#ff9800;color:#fff;">🎫</button>
        ${lootboxReady ? '<button class="menu-tab" data-tab="lootbox" style="background:#ff5722;color:#fff;">🎁</button>' : ''}
      </div>
      <div class="menu-content" id="menuContent"></div>
      <button class="btn close-btn" id="closeMenuBtn">Играть</button>
    `;

    document.getElementById('closeMenuBtn').addEventListener('click', closeMenu);
    
    menuPanel.querySelectorAll('.menu-tab').forEach(btn => {
      btn.addEventListener('click', () => {
        const tabName = btn.dataset.tab;
        if (tabName === 'lootbox') {
          openLootbox();
          renderMenu('characters');
        } else {
          renderMenu(tabName);
        }
      });
    });

    const content = document.getElementById('menuContent');
    switch (tab) {
      case 'characters': renderCharacters(content); break;
      case 'shop': renderShop(content); break;
      case 'skins': renderSkins(content); break;
      case 'achievements': renderAchievements(content); break;
      case 'quests': renderQuests(content); break;
      case 'pass': renderPass(content); break;
      case 'stats': renderStats(content); break;
      case 'promo': renderPromo(content); break;
    }
  }

  function renderPromo(container) {
    container.innerHTML = `
      <div style="text-align:center;">
        <h3 style="color:#ff9800;margin-bottom:15px;">🎫 Активация промокода</h3>
        <p style="font-size:0.85rem;color:#aaa;margin-bottom:10px;">Введите промокод для получения награды</p>
        <input type="text" class="promo-input" id="promoInput" placeholder="Введите промокод" maxlength="20" autocomplete="off">
        <button class="btn" id="activatePromoBtn" style="background:#ff9800;margin:10px 0;">Активировать</button>
        <div class="promo-message" id="promoMessage"></div>
        <div style="margin-top:15px;font-size:0.7rem;color:#666;">
          <p>Доступные промокоды:</p>
          <p style="color:#ffd700;">GOLDEN2026 - Золотой скин</p>
          <p style="color:#7c4dff;">KOSMOMAY - Космический скин</p>
          <p style="color:#ff80ab;">KRIPT2026 - 5000 криптосталлов</p>
          <p style="color:#80d8ff;">KRISTMAY - 12000 кристаллов</p>
          <p style="color:#ff6d00;">FAILPRISE - Пламенный скин + 3000 кристаллов</p>
        </div>
      </div>
    `;

    setTimeout(() => {
      const promoInput = document.getElementById('promoInput');
      const activateBtn = document.getElementById('activatePromoBtn');
      const promoMessage = document.getElementById('promoMessage');

      function handleActivation() {
        const code = promoInput.value;
        const result = activatePromocode(code);
        
        promoMessage.className = 'promo-message';
        promoMessage.textContent = '';
        
        if (result.success) {
          promoMessage.className = 'promo-message success';
          promoMessage.textContent = result.message;
          promoInput.value = '';
        } else {
          promoMessage.className = 'promo-message error';
          promoMessage.textContent = result.message;
        }
      }

      activateBtn.addEventListener('click', handleActivation);
      promoInput.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') handleActivation();
      });
      promoInput.focus();
    }, 100);
  }

  function openLootbox() {
    lootboxReady = false;
    lastLootboxDay = new Date().toDateString();
    const rewards = [
      { type: 'crystals', amount: 200, text: '💎 200 кристаллов' },
      { type: 'crystals', amount: 500, text: '💎 500 кристаллов' },
      { type: 'crystals', amount: 1000, text: '💎 1000 кристаллов' },
      { type: 'cryptostals', amount: 100, text: '🔮 100 криптосталлов' },
      { type: 'cryptostals', amount: 300, text: '🔮 300 криптосталлов' }
    ];
    const reward = rewards[Math.floor(Math.random() * rewards.length)];
    if (reward.type === 'crystals') crystals += reward.amount;
    else cryptostals += reward.amount;
    saveData();
    addFireworks();
    alert('🎁 Вы получили: ' + reward.text);
  }

  function renderCharacters(container) {
    container.innerHTML = '<div class="grid"></div>';
    const grid = container.querySelector('.grid');
    Object.values(CHARACTERS).forEach(ch => {
      if (!ownedCharacters.has(ch.id)) return;
      const card = document.createElement('div');
      card.className = 'card' + (currentCharacter.id === ch.id ? ' selected' : '');
      card.innerHTML = `
        <div class="preview" style="background:${ch.color};"></div>
        <div class="card-name">${ch.name}</div>
        <div style="font-size:0.65rem;color:#aaa;">${ch.specialFeature || ch.type}</div>
      `;
      card.addEventListener('click', () => {
        currentCharacter = ch;
        saveData();
        renderMenu('characters');
      });
      grid.appendChild(card);
    });
  }

  function renderShop(container) {
    container.innerHTML = '<div class="grid"></div>';
    const grid = container.querySelector('.grid');
    
    Object.values(CHARACTERS).forEach(ch => {
      if (!ch.price || ownedCharacters.has(ch.id)) return;
      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `
        <div class="preview" style="background:${ch.color};"></div>
        <div class="card-name">${ch.name} (${ch.specialFeature || ch.type})</div>
        <div class="card-price crystals">💎 ${ch.price * 2}</div>
        <div class="card-price cryptostals">🔮 ${ch.price}</div>
      `;
      card.addEventListener('click', () => {
        if (cryptostals >= ch.price) {
          cryptostals -= ch.price;
          ownedCharacters.add(ch.id);
          saveData();
          renderMenu('shop');
        } else if (crystals >= ch.price * 2) {
          crystals -= ch.price * 2;
          ownedCharacters.add(ch.id);
          saveData();
          renderMenu('shop');
        }
      });
      grid.appendChild(card);
    });

    Object.values(ALL_SKINS).forEach(s => {
      if (ownedSkins.has(s.id) || !s.price) return;
      const card = document.createElement('div');
      card.className = 'card';
      const sym = s.currency === 'cryptostals' ? '🔮' : '💎';
      const cls = s.currency === 'cryptostals' ? 'cryptostals' : 'crystals';
      card.innerHTML = `
        <div class="preview" style="background:${getSkinPreviewColor(s)};"></div>
        <div class="card-name">${s.name}</div>
        <div class="card-price ${cls}">${sym} ${s.price}</div>
      `;
      card.addEventListener('click', () => {
        const afford = s.currency === 'cryptostals' ? cryptostals >= s.price : crystals >= s.price;
        if (afford) {
          if (s.currency === 'cryptostals') cryptostals -= s.price;
          else crystals -= s.price;
          ownedSkins.add(s.id);
          saveData();
          renderMenu('shop');
        }
      });
      grid.appendChild(card);
    });
  }

  function getSkinPreviewColor(skin) {
    if (skin.chromatic) return 'linear-gradient(135deg, red, orange, yellow, green, blue, indigo, violet)';
    if (skin.ultra) return 'linear-gradient(135deg, #ff4081, #00e5ff, #ffea00, #ff4081)';
    if (skin.flame) return 'linear-gradient(0deg, #ffd600, #ff6d00, #d50000)';
    return skin.color;
  }

  function renderSkins(container) {
    const avail = Object.values(ALL_SKINS).filter(s => ownedSkins.has(s.id));
    container.innerHTML = '<div class="grid"></div>';
    const grid = container.querySelector('.grid');
    
    const noneCard = document.createElement('div');
    noneCard.className = 'card' + (!activeSkin ? ' selected' : '');
    noneCard.innerHTML = `
      <div class="preview" style="background:${currentCharacter.color};"></div>
      <div class="card-name">Стандартный</div>
    `;
    noneCard.addEventListener('click', () => {
      activeSkin = null;
      saveData();
      renderMenu('skins');
    });
    grid.appendChild(noneCard);

    avail.forEach(s => {
      const card = document.createElement('div');
      card.className = 'card' + (activeSkin?.id === s.id ? ' selected' : '');
      card.innerHTML = `
        <div class="preview" style="background:${getSkinPreviewColor(s)};"></div>
        <div class="card-name">${s.name}</div>
      `;
      card.addEventListener('click', () => {
        activeSkin = s;
        saveData();
        renderMenu('skins');
      });
      grid.appendChild(card);
    });
  }

  function renderAchievements(container) {
    container.innerHTML = '<div class="achievement-list"></div>';
    const list = container.querySelector('.achievement-list');
    ACHIEVEMENTS.forEach(a => {
      const unlocked = highScore >= a.req;
      const claimed = claimedAchievements.has(a.id);
      const div = document.createElement('div');
      div.className = 'achievement-item' + (claimed ? ' claimed' : '');
      const sym = a.currency === 'cryptostals' ? '🔮' : '💎';
      const cls = a.currency === 'cryptostals' ? 'cryptostals' : 'crystals';
      div.innerHTML = `
        <span>${a.name} (${a.req}) <span class="achievement-reward ${cls}">${sym}${a.reward}</span></span>
      `;
      const btn = document.createElement('button');
      btn.className = 'btn';
      btn.textContent = claimed ? '✅' : (unlocked ? 'Забрать' : '🔒');
      btn.disabled = claimed || !unlocked;
      btn.addEventListener('click', () => {
        if (!claimed && unlocked) {
          if (a.currency === 'cryptostals') cryptostals += a.reward;
          else crystals += a.reward;
          claimedAchievements.add(a.id);
          saveData();
          renderMenu('achievements');
        }
      });
      div.appendChild(btn);
      list.appendChild(div);
    });
  }

  function renderQuests(container) {
    container.innerHTML = '<strong>📅 Ежедневные:</strong><br>';
    dailyQuests.forEach((q, i) => {
      container.innerHTML += `<div class="quest-item">${q.desc} ${dailyClaimed[i] ? '✅' : '(💎500)'}</div>`;
    });
    container.innerHTML += '<strong>📆 Еженедельные:</strong><br>';
    weeklyQuests.forEach((q, i) => {
      container.innerHTML += `<div class="quest-item">${q.desc} ${weeklyClaimed[i] ? '✅' : '(💎2000)'}</div>`;
    });
  }

  function renderPass(container) {
    resetPassIfNeeded();
    const timeRemaining = getPassTimeRemaining();
    container.innerHTML = `
      <div><strong>🌵 Kaktus Pass — Уровень ${passLevel}</strong></div>
      <div class="pass-timer">⏱️ Обновление через: ${timeRemaining}</div>
      <div class="pass-progress">
        <div class="pass-progress-fill" style="width:${(passXP / PASS_XP_PER_LEVEL) * 100}%"></div>
      </div>
      <div style="font-size:0.8rem;margin-bottom:10px;">${passXP}/${PASS_XP_PER_LEVEL} XP</div>
      <strong>Задания:</strong><br>
    `;
    passQuests.forEach((q, i) => {
      container.innerHTML += `<div class="pass-item"><span>${q.desc} (${q.xp} XP)</span><span>${passClaimed[i] ? '✅' : ''}</span></div>`;
    });
  }

  function renderStats(container) {
    container.innerHTML = `
      <div style="text-align:left;font-size:14px;">
        <p>🦘 Прыжков: <strong>${stats.jumps}</strong></p>
        <p>💀 Смертей: <strong>${stats.deaths}</strong></p>
        <p>💎 Кристаллов собрано: <strong>${stats.crystalsCollected}</strong></p>
        <p>🏆 Общий счёт: <strong>${stats.totalScore}</strong></p>
        <p>🌵 Уровень Pass: <strong>${passLevel}</strong></p>
        <p>🎨 Скинов: <strong>${ownedSkins.size}</strong></p>
        <p>🐾 Персонажей: <strong>${ownedCharacters.size}</strong></p>
        <p>🎫 Промокодов использовано: <strong>${usedPromocodes.size}</strong></p>
      </div>
    `;
  }

  function randomSpawnDelay() {
    return Math.floor(Math.random() * 60 + 70);
  }

  function getObstacleGaps() {
    if (obstacles.length < 2) return [];
    const sorted = [...obstacles].sort((a, b) => a.x - b.x);
    const gaps = [];
    for (let i = 0; i < sorted.length - 1; i++) {
      const gapStart = sorted[i].x + sorted[i].width;
      const gapEnd = sorted[i + 1].x;
      if (gapEnd - gapStart > 130) {
        gaps.push({ start: gapStart, end: gapEnd });
      }
    }
    return gaps;
  }

  function spawnBird() {
    const gaps = getObstacleGaps();
    if (gaps.length > 0) {
      const gap = gaps[Math.floor(Math.random() * gaps.length)];
      const bx = gap.start + (gap.end - gap.start) / 2;
      const by = Math.random() < 0.5 ? GROUND_Y - 60 : GROUND_Y - 130;
      birds.push({ x: bx, y: Math.max(35, by), width: 44, height: 34 });
    }
  }

  function update() {
    if (gameOver || paused || menuOpen || continueActive) return;

    if (!character.grounded) {
      character.vy += character.gravity;
      character.y += character.vy;
      if (character.y >= GROUND_Y - character.height) {
        character.y = GROUND_Y - character.height;
        character.vy = 0;
        character.grounded = true;
      }
    }

    // ИЗМЕНЕНО: ускорение каждые 5000 вместо 10000
    const speedMultiplier = 1 + Math.floor(score / 5000) * 0.3;
    if (speedBoostActive) {
      currentSpeed = baseSpeed * speedMultiplier * 1.5;
      speedBoostTimer--;
      if (speedBoostTimer <= 0) speedBoostActive = false;
    } else {
      currentSpeed = baseSpeed * speedMultiplier;
    }

    spawnTimer++;
    if (spawnTimer >= nextSpawnIn) {
      spawnTimer = 0;
      nextSpawnIn = randomSpawnDelay();
      const h = 40 + Math.random() * 25;
      obstacles.push({ x: CANVAS_WIDTH, y: GROUND_Y - h, width: 30, height: h });
    }

    if (score >= 40000) {
      birdSpawnTimer++;
      if (birdSpawnTimer >= 140) {
        birdSpawnTimer = 0;
        spawnBird();
      }
    }

    crystalSpawnTimer++;
    if (crystalSpawnTimer > 80) {
      crystalSpawnTimer = 0;
      crystalsOnMap.push({
        x: CANVAS_WIDTH,
        y: GROUND_Y - 30 - Math.random() * 100,
        w: 15,
        h: 15,
        collected: false
      });
    }

    for (let i = obstacles.length - 1; i >= 0; i--) {
      obstacles[i].x -= currentSpeed;
      if (obstacles[i].x < -50) obstacles.splice(i, 1);
    }
    for (let i = birds.length - 1; i >= 0; i--) {
      birds[i].x -= currentSpeed;
      if (birds[i].x < -50) birds.splice(i, 1);
    }
    for (let i = crystalsOnMap.length - 1; i >= 0; i--) {
      crystalsOnMap[i].x -= currentSpeed;
      if (crystalsOnMap[i].x < -50) crystalsOnMap.splice(i, 1);
    }

    for (let i = crystalsOnMap.length - 1; i >= 0; i--) {
      const cr = crystalsOnMap[i];
      if (
        character.x < cr.x + cr.w &&
        character.x + character.width > cr.x &&
        character.y < cr.y + cr.h &&
        character.y + character.height > cr.y
      ) {
        let amount = 5;
        if (doubleCrystalsActive) amount *= 2;
        crystals += amount;
        stats.crystalsCollected += amount;
        crystalsOnMap.splice(i, 1);
      }
    }

    if (doubleCrystalsActive) {
      doubleCrystalsTimer--;
      if (doubleCrystalsTimer <= 0) doubleCrystalsActive = false;
    }

    score += Math.floor(currentSpeed * 0.7);
    stats.totalScore += Math.floor(currentSpeed * 0.7);
    if (score > highScore) {
      highScore = score;
      saveData();
      updateUI();
      checkAchievements();
    }

    checkQuestCompletion();
    checkPassQuests();

    for (const obs of obstacles) {
      if (
        character.x < obs.x + obs.width &&
        character.x + character.width > obs.x &&
        character.y < obs.y + obs.height &&
        character.y + character.height > obs.y
      ) {
        triggerGameOver();
        return;
      }
    }
    for (const bird of birds) {
      if (
        character.x < bird.x + bird.width &&
        character.x + character.width > bird.x &&
        character.y < bird.y + bird.height &&
        character.y + character.height > bird.y
      ) {
        triggerGameOver();
        return;
      }
    }

    for (let i = fireworks.length - 1; i >= 0; i--) {
      fireworks[i].x += fireworks[i].vx;
      fireworks[i].y += fireworks[i].vy;
      fireworks[i].vy += 0.1;
      fireworks[i].life--;
      if (fireworks[i].life <= 0) fireworks.splice(i, 1);
    }
  }

  function getTheme() {
    if (score >= 40000) return 'space';
    if (score >= 25000) return 'inverted';
    return 'normal';
  }

  function drawSky() {
    const theme = getTheme();
    if (theme === 'normal') {
      ctx.fillStyle = '#ffffff';
      ctx.fillRect(0, 0, CANVAS_WIDTH, GROUND_Y);
    } else if (theme === 'inverted') {
      ctx.fillStyle = '#1a1a1a';
      ctx.fillRect(0, 0, CANVAS_WIDTH, GROUND_Y);
    } else {
      const grd = ctx.createLinearGradient(0, 0, 0, GROUND_Y);
      grd.addColorStop(0, '#0d0d2b');
      grd.addColorStop(0.5, '#1a1a4e');
      grd.addColorStop(1, '#2d1b69');
      ctx.fillStyle = grd;
      ctx.fillRect(0, 0, CANVAS_WIDTH, GROUND_Y);
      stars.forEach(s => {
        const twinkle = Math.sin(Date.now() * 0.003 + s.twinkle) * 0.5 + 0.5;
        ctx.fillStyle = `rgba(255,255,255,${0.4 + twinkle * 0.6})`;
        ctx.beginPath();
        ctx.arc(s.x, s.y, s.size, 0, Math.PI * 2);
        ctx.fill();
      });
    }
  }

  function drawGround() {
    const theme = getTheme();
    if (theme === 'normal') {
      ctx.fillStyle = '#1a1a1a';
      ctx.fillRect(0, GROUND_Y, CANVAS_WIDTH, CANVAS_HEIGHT - GROUND_Y);
      ctx.strokeStyle = '#333';
      ctx.lineWidth = 2;
      ctx.beginPath();
      ctx.moveTo(0, GROUND_Y);
      ctx.lineTo(CANVAS_WIDTH, GROUND_Y);
      ctx.stroke();
    } else if (theme === 'inverted') {
      ctx.fillStyle = '#f0f0f0';
      ctx.fillRect(0, GROUND_Y, CANVAS_WIDTH, CANVAS_HEIGHT - GROUND_Y);
      ctx.strokeStyle = '#ccc';
      ctx.lineWidth = 2;
      ctx.beginPath();
      ctx.moveTo(0, GROUND_Y);
      ctx.lineTo(CANVAS_WIDTH, GROUND_Y);
      ctx.stroke();
    } else {
      ctx.fillStyle = '#4a148c';
      ctx.fillRect(0, GROUND_Y, CANVAS_WIDTH, CANVAS_HEIGHT - GROUND_Y);
      ctx.strokeStyle = '#6a1b9a';
      ctx.lineWidth = 3;
      ctx.beginPath();
      ctx.moveTo(0, GROUND_Y);
      ctx.lineTo(CANVAS_WIDTH, GROUND_Y);
      ctx.stroke();
    }
  }

  function getEffectiveColors() {
    const skin = activeSkin;
    const ch = currentCharacter;
    if (!skin) return {
      primary: ch.color,
      secondary: ch.secondary,
      belly: ch.belly,
      earInner: ch.earInner
    };
    
    // Специальные скины с градиентами
    if (skin.flame) {
      return {
        primary: '#ff6d00',
        secondary: '#d50000',
        belly: '#ffab40',
        earInner: '#ff5252',
        gradient: 'flame'
      };
    }
    if (skin.chromatic) {
      return {
        primary: skin.color,
        secondary: skin.secondary,
        belly: skin.belly,
        earInner: skin.earInner,
        gradient: 'chromatic'
      };
    }
    if (skin.ultra) {
      return {
        primary: skin.color,
        secondary: skin.secondary,
        belly: skin.belly,
        earInner: skin.earInner,
        gradient: 'ultra'
      };
    }
    
    return {
      primary: skin.color,
      secondary: skin.secondary,
      belly: skin.belly || '#ffffff',
      earInner: skin.earInner || '#ffab91'
    };
  }

  function drawCharacter() {
    const { x, y, width, height } = character;
    ctx.save();
    const ch = currentCharacter;
    const colors = getEffectiveColors();

    if (ch.type === 'star') {
      drawStarCharacter(x, y, width, height, ch, colors);
    } else if (ch.type === 'planet') {
      drawPlanetCharacter(x, y, width, height, ch, colors);
    } else if (ch.type === 'humanoid') {
      drawHumanoidCharacter(x, y, width, height, ch, colors);
    } else {
      drawAnimalCharacter(x, y, width, height, ch, colors);
    }

    ctx.restore();
  }

  function getBodyFillStyle(x, y, w, h, colors) {
    if (colors.gradient === 'flame') {
      const grad = ctx.createLinearGradient(x, y + h * 0.3, x, y + h * 0.8);
      grad.addColorStop(0, '#d50000');
      grad.addColorStop(0.5, '#ff6d00');
      grad.addColorStop(1, '#ffd600');
      return grad;
    }
    if (colors.gradient === 'chromatic') {
      const t = Date.now() * 0.002;
      return `rgb(${128 + Math.sin(t) * 127}, ${128 + Math.sin(t + 2) * 127}, ${128 + Math.sin(t + 4) * 127})`;
    }
    if (colors.gradient === 'ultra') {
      const grad = ctx.createLinearGradient(x, y, x + w, y + h);
      grad.addColorStop(0, '#ff4081');
      grad.addColorStop(0.5, '#00e5ff');
      grad.addColorStop(1, '#ffea00');
      return grad;
    }
    return colors.primary;
  }

  function drawStarCharacter(x, y, w, h, ch, colors) {
    const cx = x + w / 2;
    const cy = y + h / 2;
    
    ctx.shadowColor = colors.secondary;
    ctx.shadowBlur = 25;
    
    const time = Date.now() * 0.001;
    const spikes = 8;
    const outerRadius = w * 0.4 + Math.sin(time * 2) * 3;
    const innerRadius = w * 0.2 + Math.sin(time * 2 + Math.PI) * 2;
    
    const starGrad = ctx.createRadialGradient(cx, cy, innerRadius * 0.5, cx, cy, outerRadius);
    starGrad.addColorStop(0, '#ffffff');
    starGrad.addColorStop(0.3, colors.primary);
    starGrad.addColorStop(1, colors.secondary);
    
    ctx.fillStyle = starGrad;
    ctx.beginPath();
    for (let i = 0; i < spikes * 2; i++) {
      const radius = i % 2 === 0 ? outerRadius : innerRadius;
      const angle = (i * Math.PI) / spikes - Math.PI / 2;
      const sx = cx + Math.cos(angle) * radius;
      const sy = cy + Math.sin(angle) * radius;
      if (i === 0) ctx.moveTo(sx, sy);
      else ctx.lineTo(sx, sy);
    }
    ctx.closePath();
    ctx.fill();
    ctx.shadowBlur = 0;
    
    ctx.fillStyle = '#ffffff';
    ctx.beginPath();
    ctx.arc(cx - 5, cy - 5, 5, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(cx + 8, cy - 5, 5, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#1b1b1b';
    ctx.beginPath();
    ctx.arc(cx - 4, cy - 5, 3, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(cx + 9, cy - 5, 3, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.strokeStyle = '#1b1b1b';
    ctx.lineWidth = 2;
    ctx.beginPath();
    ctx.arc(cx + 2, cy + 5, 6, 0, Math.PI);
    ctx.stroke();
  }

  function drawPlanetCharacter(x, y, w, h, ch, colors) {
    const cx = x + w / 2;
    const cy = y + h / 2;
    const radius = w * 0.38;
    
    ctx.shadowColor = colors.secondary;
    ctx.shadowBlur = 20;
    
    const planetGrad = ctx.createRadialGradient(cx - radius * 0.3, cy - radius * 0.3, radius * 0.1, cx, cy, radius);
    planetGrad.addColorStop(0, '#ffffff');
    planetGrad.addColorStop(0.3, colors.primary);
    planetGrad.addColorStop(1, colors.secondary);
    
    ctx.fillStyle = planetGrad;
    ctx.beginPath();
    ctx.arc(cx, cy, radius, 0, Math.PI * 2);
    ctx.fill();
    ctx.shadowBlur = 0;
    
    if (ch.id === 'earth' || ch.earthColors) {
      ctx.fillStyle = '#4caf50';
      ctx.beginPath();
      ctx.ellipse(cx - radius * 0.2, cy - radius * 0.1, radius * 0.3, radius * 0.2, 0.3, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.ellipse(cx + radius * 0.3, cy + radius * 0.15, radius * 0.25, radius * 0.18, -0.2, 0, Math.PI * 2);
      ctx.fill();
    }
    
    if (ch.id === 'moon' || ch.moonCraters) {
      ctx.fillStyle = 'rgba(255,255,255,0.3)';
      ctx.beginPath();
      ctx.arc(cx - radius * 0.3, cy - radius * 0.2, radius * 0.15, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.arc(cx + radius * 0.4, cy + radius * 0.1, radius * 0.12, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.arc(cx - radius * 0.1, cy + radius * 0.4, radius * 0.18, 0, Math.PI * 2);
      ctx.fill();
    }
    
    ctx.fillStyle = '#ffffff';
    ctx.beginPath();
    ctx.arc(cx - 7, cy - 3, 5, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(cx + 7, cy - 3, 5, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#1b1b1b';
    ctx.beginPath();
    ctx.arc(cx - 6, cy - 3, 3, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(cx + 8, cy - 3, 3, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.strokeStyle = '#1b1b1b';
    ctx.lineWidth = 2;
    ctx.beginPath();
    ctx.arc(cx, cy + 3, 5, 0.1, Math.PI - 0.1);
    ctx.stroke();
  }

  function drawHumanoidCharacter(x, y, w, h, ch, colors) {
    ctx.fillStyle = 'rgba(0,0,0,0.3)';
    ctx.beginPath();
    ctx.ellipse(x + w / 2, y + h * 0.92, w * 0.35, h * 0.05, 0, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = getBodyFillStyle(x, y, w, h, colors);
    ctx.beginPath();
    ctx.roundRect(x + w * 0.2, y + h * 0.35, w * 0.6, h * 0.45, 8);
    ctx.fill();
    
    if (ch.spiderEmblem) {
      ctx.strokeStyle = '#ffffff';
      ctx.lineWidth = 2;
      const spiderX = x + w / 2;
      const spiderY = y + h * 0.55;
      
      ctx.fillStyle = '#ffffff';
      ctx.beginPath();
      ctx.arc(spiderX, spiderY, 5, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.arc(spiderX, spiderY - 8, 3, 0, Math.PI * 2);
      ctx.fill();
      
      for (let i = 0; i < 4; i++) {
        const angle = (i / 4) * Math.PI - Math.PI / 4;
        ctx.beginPath();
        ctx.moveTo(spiderX, spiderY);
        ctx.lineTo(spiderX + Math.cos(angle) * 12, spiderY + Math.sin(angle) * 12);
        ctx.stroke();
        ctx.beginPath();
        ctx.moveTo(spiderX, spiderY);
        ctx.lineTo(spiderX - Math.cos(angle) * 12, spiderY + Math.sin(angle) * 12);
        ctx.stroke();
      }
    }
    
    const headX = x + w / 2;
    const headY = y + h * 0.25;
    const headSize = w * 0.18;
    
    ctx.fillStyle = colors.primary;
    ctx.beginPath();
    ctx.arc(headX, headY, headSize, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#ffffff';
    ctx.beginPath();
    ctx.ellipse(headX - headSize * 0.35, headY - headSize * 0.1, 6, 8, -0.2, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.ellipse(headX + headSize * 0.35, headY - headSize * 0.1, 6, 8, 0.2, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.strokeStyle = '#000000';
    ctx.lineWidth = 2;
    ctx.beginPath();
    ctx.ellipse(headX - headSize * 0.35, headY - headSize * 0.1, 6, 8, -0.2, 0, Math.PI * 2);
    ctx.stroke();
    ctx.beginPath();
    ctx.ellipse(headX + headSize * 0.35, headY - headSize * 0.1, 6, 8, 0.2, 0, Math.PI * 2);
    ctx.stroke();
    
    ctx.fillStyle = colors.secondary;
    if (character.grounded && !paused && !gameOver) {
      const runCycle = Date.now() * 0.01;
      ctx.beginPath();
      ctx.roundRect(x + w * 0.25, y + h * 0.75 + Math.sin(runCycle) * 3, w * 0.1, h * 0.12, 3);
      ctx.fill();
      ctx.beginPath();
      ctx.roundRect(x + w * 0.55, y + h * 0.75 + Math.sin(runCycle + Math.PI) * 3, w * 0.1, h * 0.12, 3);
      ctx.fill();
    } else {
      ctx.beginPath();
      ctx.roundRect(x + w * 0.25, y + h * 0.75, w * 0.1, h * 0.12, 3);
      ctx.fill();
      ctx.beginPath();
      ctx.roundRect(x + w * 0.55, y + h * 0.75, w * 0.1, h * 0.12, 3);
      ctx.fill();
    }
  }

  function drawAnimalCharacter(x, y, w, h, ch, colors) {
    // Тень
    ctx.fillStyle = 'rgba(0,0,0,0.3)';
    ctx.beginPath();
    ctx.ellipse(x + w / 2, y + h * 0.92, w * 0.35, h * 0.05, 0, 0, Math.PI * 2);
    ctx.fill();

    // Тело с учётом особенностей
    const bodyGrad = ctx.createLinearGradient(x, y + h * 0.3, x, y + h * 0.8);
    bodyGrad.addColorStop(0, colors.primary);
    bodyGrad.addColorStop(0.5, colors.belly);
    bodyGrad.addColorStop(1, colors.secondary);
    ctx.fillStyle = colors.gradient ? getBodyFillStyle(x, y, w, h, colors) : bodyGrad;
    
    if (ch.chubby) {
      ctx.beginPath();
      ctx.ellipse(x + w * 0.5, y + h * 0.55, w * 0.4, h * 0.4, 0, 0, Math.PI * 2);
      ctx.fill();
    } else if (ch.elongated) {
      ctx.beginPath();
      ctx.ellipse(x + w * 0.5, y + h * 0.55, w * 0.28, h * 0.38, 0, 0, Math.PI * 2);
      ctx.fill();
    } else {
      ctx.beginPath();
      ctx.ellipse(x + w * 0.5, y + h * 0.55, w * 0.34, h * 0.35, 0, 0, Math.PI * 2);
      ctx.fill();
    }

    // Голова
    const headX = x + w * 0.7;
    const headY = y + h * 0.28;
    const headSize = ch.chubby ? w * 0.3 : (ch.elongated ? w * 0.22 : w * 0.25);
    
    ctx.fillStyle = colors.primary;
    ctx.beginPath();
    ctx.arc(headX, headY, headSize, 0, Math.PI * 2);
    ctx.fill();
    ctx.strokeStyle = colors.secondary;
    ctx.lineWidth = 1.5;
    ctx.stroke();

    // Грива льва
    if (ch.hasMane) {
      ctx.fillStyle = ch.maneColor;
      for (let i = 0; i < 12; i++) {
        const angle = (i / 12) * Math.PI * 2;
        const mx = headX + Math.cos(angle) * headSize * 1.2;
        const my = headY + Math.sin(angle) * headSize * 1.2;
        ctx.beginPath();
        ctx.arc(mx, my, headSize * 0.3, 0, Math.PI * 2);
        ctx.fill();
      }
    }

    // Шипы дино
    if (ch.hasSpikes) {
      ctx.fillStyle = ch.spikeColor;
      for (let i = 0; i < 5; i++) {
        const sx = x + w * 0.3 + i * w * 0.1;
        const sy = y + h * 0.3 - i * 2;
        ctx.beginPath();
        ctx.moveTo(sx, sy);
        ctx.lineTo(sx + 4, sy - 12);
        ctx.lineTo(sx + 8, sy);
        ctx.fill();
      }
    }

    // Глаза
    ctx.fillStyle = '#ffffff';
    ctx.beginPath();
    ctx.arc(headX - headSize * 0.25, headY - headSize * 0.1, headSize * 0.22, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(headX + headSize * 0.25, headY - headSize * 0.1, headSize * 0.22, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#4e342e';
    ctx.beginPath();
    ctx.arc(headX - headSize * 0.25, headY - headSize * 0.1, headSize * 0.15, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(headX + headSize * 0.25, headY - headSize * 0.1, headSize * 0.15, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#000000';
    ctx.beginPath();
    ctx.arc(headX - headSize * 0.25, headY - headSize * 0.1, headSize * 0.08, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(headX + headSize * 0.25, headY - headSize * 0.1, headSize * 0.08, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = '#ffffff';
    ctx.beginPath();
    ctx.arc(headX - headSize * 0.28, headY - headSize * 0.15, headSize * 0.04, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(headX + headSize * 0.22, headY - headSize * 0.15, headSize * 0.04, 0, Math.PI * 2);
    ctx.fill();

    // Нос (острый для лиса)
    if (ch.pointyNose) {
      ctx.fillStyle = ch.secondary;
      ctx.beginPath();
      ctx.moveTo(headX + headSize * 0.8, headY);
      ctx.lineTo(headX + headSize * 1.1, headY - 2);
      ctx.lineTo(headX + headSize * 1.1, headY + 2);
      ctx.lineTo(headX + headSize * 0.8, headY + 1);
      ctx.fill();
      
      if (ch.hasWhiteTips) {
        ctx.fillStyle = ch.whiteTipColor;
        ctx.beginPath();
        ctx.arc(headX + headSize * 1.05, headY, 1.5, 0, Math.PI * 2);
        ctx.fill();
      }
    } else {
      ctx.fillStyle = '#3e2723';
      ctx.beginPath();
      ctx.arc(headX + headSize * 0.5, headY + headSize * 0.1, headSize * 0.18, 0, Math.PI * 2);
      ctx.fill();
      ctx.fillStyle = 'rgba(255,255,255,0.5)';
      ctx.beginPath();
      ctx.arc(headX + headSize * 0.55, headY + headSize * 0.05, headSize * 0.06, 0, Math.PI * 2);
      ctx.fill();
    }

    // Усы
    if (ch.hasWhiskers) {
      ctx.strokeStyle = ch.whiskerColor;
      ctx.lineWidth = 0.8;
      for (let i = -2; i <= 2; i++) {
        if (i === 0) continue;
        const side = i > 0 ? 1 : -1;
        ctx.beginPath();
        ctx.moveTo(headX + headSize * 0.3, headY + headSize * 0.25);
        ctx.lineTo(headX + headSize * (0.3 + side * 0.6), headY + headSize * (0.25 - i * 0.1));
        ctx.stroke();
      }
    }

    // Рот и зубы
    ctx.strokeStyle = '#333';
    ctx.lineWidth = 1.2;
    ctx.beginPath();
    ctx.arc(headX + headSize * 0.3, headY + headSize * 0.35, headSize * 0.15, 0.1, Math.PI - 0.1);
    ctx.stroke();

    // Зубы пантеры
    if (ch.hasTeeth) {
      ctx.fillStyle = '#ffffff';
      ctx.beginPath();
      ctx.moveTo(headX + headSize * 0.2, headY + headSize * 0.4);
      ctx.lineTo(headX + headSize * 0.25, headY + headSize * 0.6);
      ctx.lineTo(headX + headSize * 0.3, headY + headSize * 0.4);
      ctx.fill();
      ctx.beginPath();
      ctx.moveTo(headX + headSize * 0.5, headY + headSize * 0.4);
      ctx.lineTo(headX + headSize * 0.55, headY + headSize * 0.6);
      ctx.lineTo(headX + headSize * 0.6, headY + headSize * 0.4);
      ctx.fill();
    }

    // Язык собачки
    if (ch.hasTongue && !paused && !gameOver) {
      ctx.fillStyle = ch.tongueColor;
      ctx.beginPath();
      ctx.ellipse(headX + headSize * 0.4, headY + headSize * 0.5, 4, 7, 0.1, 0, Math.PI * 2);
      ctx.fill();
    }

    // Уши с разными формами
    drawCharacterEars(x, y, w, h, headX, headY, headSize, ch, colors);

    // Лапы
    ctx.fillStyle = colors.secondary;
    if (character.grounded && !paused && !gameOver) {
      const runCycle = Date.now() * 0.01;
      ctx.beginPath();
      ctx.ellipse(x + w * 0.3, y + h * 0.85 + Math.sin(runCycle) * 3, w * 0.08, h * 0.1, 0, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.ellipse(x + w * 0.6, y + h * 0.85 + Math.sin(runCycle + Math.PI) * 3, w * 0.08, h * 0.1, 0, 0, Math.PI * 2);
      ctx.fill();
      
      // Когти медведя
      if (ch.hasClaws) {
        ctx.fillStyle = ch.clawColor;
        for (let i = 0; i < 2; i++) {
          const px = x + w * (0.3 + i * 0.3);
          const py = y + h * 0.85 + Math.sin(runCycle + i * Math.PI) * 3;
          for (let j = -1; j <= 1; j++) {
            ctx.beginPath();
            ctx.arc(px + j * 3, py - 5, 2, 0, Math.PI * 2);
            ctx.fill();
          }
        }
      }
    } else {
      ctx.beginPath();
      ctx.ellipse(x + w * 0.3, y + h * 0.85, w * 0.08, h * 0.1, 0, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.ellipse(x + w * 0.6, y + h * 0.85, w * 0.08, h * 0.1, 0, 0, Math.PI * 2);
      ctx.fill();
    }

    // Хвосты разных типов
    drawCharacterTail(x, y, w, h, ch, colors);
  }

  function drawCharacterEars(x, y, w, h, hx, hy, hs, ch, colors) {
    if (ch.earShape === 'long_ears') {
      // Кроличьи уши
      ctx.fillStyle = colors.primary;
      ctx.beginPath();
      ctx.ellipse(x + w * 0.25, y - h * 0.05, 6, 18, 0.1, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.ellipse(x + w * 0.55, y - h * 0.05, 6, 18, -0.1, 0, Math.PI * 2);
      ctx.fill();
      ctx.fillStyle = colors.earInner;
      ctx.beginPath();
      ctx.ellipse(x + w * 0.25, y - h * 0.05, 3, 12, 0.1, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.ellipse(x + w * 0.55, y - h * 0.05, 3, 12, -0.1, 0, Math.PI * 2);
      ctx.fill();
    } else if (ch.earShape === 'pointy_tall') {
      // Лисьи уши
      drawPointyEar(hx - hs * 0.5, hy - hs * 0.8, 8, 20, -0.2, colors);
      drawPointyEar(hx + hs * 0.5, hy - hs * 0.8, 8, 20, 0.2, colors);
    } else if (ch.earShape === 'pointy') {
      // Кошачьи уши
      drawPointyEar(hx - hs * 0.6, hy - hs * 0.7, 7, 16, -0.1, colors);
      drawPointyEar(hx + hs * 0.6, hy - hs * 0.7, 7, 16, 0.1, colors);
    } else if (ch.earShape === 'floppy') {
      // Висячие уши
      drawFloppyEar(hx - hs * 0.6, hy - hs * 0.3, 7, 18, -0.5, colors);
      drawFloppyEar(hx + hs * 0.6, hy - hs * 0.3, 7, 18, 0.5, colors);
    } else if (ch.earShape === 'spikes') {
      // Шипы вместо ушей
      ctx.fillStyle = colors.primary;
      ctx.beginPath();
      ctx.moveTo(hx - hs * 0.6, hy - hs * 0.3);
      ctx.lineTo(hx - hs * 0.5, hy - hs * 0.8);
      ctx.lineTo(hx - hs * 0.3, hy - hs * 0.2);
      ctx.fill();
      ctx.beginPath();
      ctx.moveTo(hx + hs * 0.6, hy - hs * 0.3);
      ctx.lineTo(hx + hs * 0.5, hy - hs * 0.8);
      ctx.lineTo(hx + hs * 0.3, hy - hs * 0.2);
      ctx.fill();
    } else {
      // Круглые уши
      ctx.fillStyle = colors.primary;
      ctx.strokeStyle = colors.secondary;
      ctx.lineWidth = 1.5;
      ctx.beginPath();
      ctx.arc(hx - hs * 0.6, hy - hs * 0.5, hs * 0.2, 0, Math.PI * 2);
      ctx.fill();
      ctx.stroke();
      ctx.beginPath();
      ctx.arc(hx + hs * 0.6, hy - hs * 0.5, hs * 0.2, 0, Math.PI * 2);
      ctx.fill();
      ctx.stroke();
      ctx.fillStyle = colors.earInner;
      ctx.beginPath();
      ctx.arc(hx - hs * 0.6, hy - hs * 0.5, hs * 0.12, 0, Math.PI * 2);
      ctx.fill();
      ctx.beginPath();
      ctx.arc(hx + hs * 0.6, hy - hs * 0.5, hs * 0.12, 0, Math.PI * 2);
      ctx.fill();
    }
  }

  function drawPointyEar(ex, ey, ew, eh, angle, colors) {
    ctx.save();
    ctx.translate(ex, ey);
    ctx.rotate(angle);
    ctx.fillStyle = colors.primary;
    ctx.beginPath();
    ctx.moveTo(0, -eh / 2);
    ctx.lineTo(-ew / 2, eh / 2);
    ctx.lineTo(ew / 2, eh / 2);
    ctx.closePath();
    ctx.fill();
    ctx.strokeStyle = colors.secondary;
    ctx.lineWidth = 1;
    ctx.stroke();
    ctx.fillStyle = colors.earInner;
    ctx.beginPath();
    ctx.moveTo(0, -eh / 3);
    ctx.lineTo(-ew / 3, eh / 3);
    ctx.lineTo(ew / 3, eh / 3);
    ctx.closePath();
    ctx.fill();
    ctx.restore();
  }

  function drawFloppyEar(ex, ey, ew, eh, angle, colors) {
    ctx.save();
    ctx.translate(ex, ey);
    ctx.rotate(angle);
    ctx.fillStyle = colors.primary;
    ctx.beginPath();
    ctx.ellipse(0, -eh / 4, ew, eh / 2, 0.1, 0, Math.PI * 2);
    ctx.fill();
    ctx.strokeStyle = colors.secondary;
    ctx.lineWidth = 1;
    ctx.stroke();
    ctx.fillStyle = colors.earInner;
    ctx.beginPath();
    ctx.ellipse(0, -eh / 4, ew * 0.6, eh / 3, 0.1, 0, Math.PI * 2);
    ctx.fill();
    ctx.restore();
  }

  function drawCharacterTail(x, y, w, h, ch, colors) {
    ctx.strokeStyle = colors.primary;
    
    if (ch.tailType === 'bushy') {
      // Пушистый лисий хвост
      const tailWave = Math.sin(Date.now() * 0.003) * 5;
      ctx.fillStyle = colors.primary;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.1, y + h * 0.7);
      ctx.quadraticCurveTo(x - w * 0.3, y + h * 0.5, x - w * 0.3 + tailWave, y + h * 0.3);
      ctx.quadraticCurveTo(x - w * 0.2, y + h * 0.15, x - w * 0.1, y + h * 0.2);
      ctx.quadraticCurveTo(x + w * 0.05, y + h * 0.4, x + w * 0.1, y + h * 0.7);
      ctx.fill();
      
      if (ch.hasWhiteTips) {
        ctx.fillStyle = ch.whiteTipColor;
        ctx.beginPath();
        ctx.arc(x - w * 0.25 + tailWave, y + h * 0.25, 5, 0, Math.PI * 2);
        ctx.fill();
      }
    } else if (ch.tailType === 'fluffy_ball') {
      // Пушистый шарик
      const bounce = Math.sin(Date.now() * 0.01) * 2;
      ctx.fillStyle = ch.fluffyTailColor;
      ctx.beginPath();
      ctx.arc(x + w * 0.1, y + h * 0.75 + bounce, 6, 0, Math.PI * 2);
      ctx.fill();
    } else if (ch.tailType === 'long_sleek') {
      // Длинный гладкий
      ctx.lineWidth = w * 0.06;
      const tailWave = Math.sin(Date.now() * 0.002) * 4;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.1, y + h * 0.75);
      ctx.quadraticCurveTo(x - w * 0.4, y + h * 0.6, x - w * 0.35 + tailWave, y + h * 0.2);
      ctx.stroke();
    } else if (ch.tailType === 'waggy') {
      // Виляющий
      ctx.lineWidth = w * 0.06;
      const wag = Math.sin(Date.now() * 0.02) * 8;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.1, y + h * 0.75);
      ctx.quadraticCurveTo(x - w * 0.3, y + h * 0.6, x - w * 0.25 + wag, y + h * 0.3);
      ctx.stroke();
    } else if (ch.tailType === 'curly') {
      // Закрученный
      ctx.lineWidth = w * 0.06;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.1, y + h * 0.75);
      ctx.quadraticCurveTo(x - w * 0.2, y + h * 0.5, x - w * 0.15, y + h * 0.4);
      ctx.quadraticCurveTo(x - w * 0.1, y + h * 0.3, x - w * 0.05, y + h * 0.35);
      ctx.stroke();
    } else if (ch.tailType === 'short_thick') {
      // Короткий толстый
      ctx.lineWidth = w * 0.1;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.05, y + h * 0.78);
      ctx.quadraticCurveTo(x - w * 0.1, y + h * 0.75, x - w * 0.08, y + h * 0.65);
      ctx.stroke();
    } else {
      // Обычный
      ctx.lineWidth = w * 0.06;
      const tailWave = Math.sin(Date.now() * 0.003) * 5;
      ctx.beginPath();
      ctx.moveTo(x + w * 0.1, y + h * 0.75);
      ctx.quadraticCurveTo(x - w * 0.2, y + h * 0.6, x - w * 0.15 + tailWave, y + h * 0.4);
      ctx.stroke();
    }
  }

  function drawObstacles() {
    obstacles.forEach(o => {
      ctx.save();
      ctx.fillStyle = '#2e7d32';
      ctx.beginPath();
      ctx.roundRect(o.x, o.y, o.width, o.height, 6);
      ctx.fill();
      ctx.fillStyle = '#4caf50';
      ctx.beginPath();
      ctx.roundRect(o.x + 4, o.y + 2, o.width - 8, o.height - 4, 4);
      ctx.fill();
      ctx.fillStyle = '#81c784';
      ctx.beginPath();
      ctx.arc(o.x + o.width / 2, o.y + 4, 5, 0, Math.PI * 2);
      ctx.fill();
      ctx.restore();
    });
  }

  function drawBirds() {
    birds.forEach(b => {
      ctx.save();
      const bg = ctx.createLinearGradient(b.x, b.y, b.x + b.width, b.y + b.height);
      bg.addColorStop(0, '#1a237e');
      bg.addColorStop(0.5, '#7c4dff');
      bg.addColorStop(1, '#00bcd4');
      ctx.fillStyle = bg;
      ctx.beginPath();
      ctx.ellipse(b.x + b.width / 2, b.y + b.height / 2, b.width / 3, b.height / 3.5, 0, 0, Math.PI * 2);
      ctx.fill();
      ctx.restore();
    });
  }

  function draw() {
    ctx.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
    drawSky();
    drawGround();

    crystalsOnMap.forEach(cr => {
      ctx.fillStyle = '#00BCD4';
      ctx.fillRect(cr.x, cr.y, cr.w, cr.h);
      ctx.fillStyle = '#fff';
      ctx.fillRect(cr.x + 3, cr.y + 2, 4, 4);
    });

    drawObstacles();
    drawBirds();
    drawCharacter();

    fireworks.forEach(f => {
      ctx.globalAlpha = f.life / 70;
      ctx.fillStyle = f.color;
      ctx.beginPath();
      ctx.arc(f.x, f.y, 3, 0, Math.PI * 2);
      ctx.fill();
    });
    ctx.globalAlpha = 1;

    ctx.fillStyle = score >= 25000 ? '#ffffff' : '#212121';
    ctx.font = 'bold 20px "Courier New"';
    ctx.fillText(currentCharacter.name + ': ' + score, 20, 45);

    if (speedBoostActive) {
      ctx.fillStyle = '#ff9800';
      ctx.fillText('⚡ БУСТ', CANVAS_WIDTH - 100, 45);
    }
    if (doubleCrystalsActive) {
      ctx.fillStyle = '#80d8ff';
      ctx.fillText('💎 x2', CANVAS_WIDTH - 100, 65);
    }

    if (gameOver && !continueActive) {
      ctx.globalAlpha = 0.8;
      ctx.fillStyle = '#212121';
      ctx.font = 'bold 36px "Courier New"';
      ctx.textAlign = 'center';
      ctx.fillText('💀 КОНЕЦ ИГРЫ', CANVAS_WIDTH / 2, CANVAS_HEIGHT / 2);
      ctx.textAlign = 'left';
      ctx.globalAlpha = 1;
    }
  }

  if (!ctx.roundRect) {
    ctx.roundRect = function(x, y, w, h, r) {
      ctx.beginPath();
      ctx.moveTo(x + r, y);
      ctx.lineTo(x + w - r, y);
      ctx.quadraticCurveTo(x + w, y, x + w, y + r);
      ctx.lineTo(x + w, y + h - r);
      ctx.quadraticCurveTo(x + w, y + h, x + w - r, y + h);
      ctx.lineTo(x + r, y + h);
      ctx.quadraticCurveTo(x, y + h, x, y + h - r);
      ctx.lineTo(x, y + r);
      ctx.quadraticCurveTo(x, y, x + r, y);
      ctx.closePath();
    };
  }

  function gameLoop() {
    update();
    draw();
    requestAnimationFrame(gameLoop);
  }

  function handleKeyDown(e) {
    if (e.key === 'p' || e.key === 'P' || e.key === 'Escape') {
      e.preventDefault();
      if (menuOpen) closeMenu();
      else togglePause();
    }
    if (e.key === ' ' || e.key === 'Space' || e.key === 'ArrowUp') {
      e.preventDefault();
      attemptJump();
    }
  }

  canvas.addEventListener('click', e => {
    e.preventDefault();
    initAudio();
    attemptJump();
  });
  
  canvas.addEventListener('touchstart', e => {
    e.preventDefault();
    initAudio();
    attemptJump();
  });
  
  pauseButton.addEventListener('click', e => {
    e.stopPropagation();
    togglePause();
  });
  
  inGameMenuBtn.addEventListener('click', e => {
    e.stopPropagation();
    openMenu();
  });
  
  musicToggle.addEventListener('click', e => {
    e.stopPropagation();
    toggleMusic();
  });
  
  continueYes.addEventListener('click', e => {
    e.stopPropagation();
    continueGame();
  });
  
  continueNo.addEventListener('click', e => {
    e.stopPropagation();
    declineContinue();
  });
  
  window.addEventListener('keydown', handleKeyDown);

  function resetDailyIfNeeded() {
    const today = new Date().toDateString();
    if (lastDailyReset !== today) {
      dailyClaimed = [false, false, false, false];
      lastDailyReset = today;
      generateDailyQuests();
      saveData();
    }
  }

  function resetWeeklyIfNeeded() {
    const now = new Date();
    if (now.getDay() === 0) {
      const today = now.toDateString();
      if (lastWeeklyReset !== today) {
        weeklyClaimed = [false, false];
        lastWeeklyReset = today;
        generateWeeklyQuests();
        saveData();
      }
    }
  }

  function init() {
    loadData();
    resetDailyIfNeeded();
    resetWeeklyIfNeeded();
    resetPassIfNeeded();
    if (!dailyQuests.length) generateDailyQuests();
    if (!weeklyQuests.length) generateWeeklyQuests();
    if (!passQuests.length) generatePassQuests();
    updateUI();
    resetGame();
    gameLoop();
  }

  init();
  setInterval(saveData, 3000);
})();
</script>
</body>
</html>
