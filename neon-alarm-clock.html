<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Neon Alarm Clock</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap');

  :root {
    --neon-royal-blue: #0047ab;
    --neon-purple: #bb00ff;
    --background-dark: #0a0a23;
    --text-color: #e1dbf7;
  }

  body {
    margin: 0;
    height: 100vh;
    background: radial-gradient(circle at center, var(--neon-royal-blue) 0%, #090927 80%);
    color: var(--text-color);
    font-family: 'Orbitron', monospace, monospace;
    display: flex;
    justify-content: center;
    align-items: center;
    user-select: none;
  }

  .container {
    background: #0e0e3d;
    border-radius: 24px;
    padding: 40px 50px;
    max-width: 360px;
    width: 90vw;
    box-shadow:
      0 0 15px var(--neon-purple),
      0 0 30px var(--neon-royal-blue),
      inset 0 0 20px #1a1a54;
    text-align: center;
  }

  h1 {
    margin-bottom: 30px;
    font-size: 2.8rem;
    color: var(--neon-purple);
    text-shadow:
      0 0 15px var(--neon-purple),
      0 0 30px var(--neon-purple);
  }

  .current-time {
    font-size: 1.8rem;
    letter-spacing: 2px;
    margin-bottom: 25px;
    font-weight: 700;
    color: var(--neon-royal-blue);
    text-shadow:
      0 0 10px var(--neon-royal-blue),
      0 0 20px var(--neon-royal-blue);
  }

  label {
    font-size: 1.1rem;
    font-weight: 600;
    display: block;
    margin-bottom: 8px;
    text-align: left;
    color: var(--text-color);
    letter-spacing: 0.6px;
  }

  input[type="time"],
  select {
    width: 100%;
    padding: 14px 18px;
    border-radius: 14px;
    border: none;
    font-size: 1.1rem;
    outline: none;
    margin-bottom: 22px;
    background: #201f44;
    color: var(--text-color);
    font-family: 'Orbitron', monospace;
    box-shadow:
      0 0 8px #150f7b inset;
    transition: background-color 0.3s ease;
  }
  input[type="time"]:focus,
  select:focus {
    background: #321ce3;
    box-shadow:
      0 0 15px var(--neon-purple),
      0 0 25px var(--neon-purple),
      0 0 40px var(--neon-purple);
    color: #fff;
  }

  button {
    width: 100%;
    padding: 16px 0;
    font-size: 1.25rem;
    font-weight: 700;
    background-color: var(--neon-purple);
    color: #fff;
    border: none;
    border-radius: 16px;
    cursor: pointer;
    box-shadow:
      0 0 20px var(--neon-purple),
      0 0 40px var(--neon-purple);
    transition: background-color 0.25s ease, box-shadow 0.25s ease;
    user-select: none;
  }
  button:hover:not(:disabled) {
    background-color: #a100e6;
    box-shadow:
      0 0 30px #bb00ff,
      0 0 50px #bb00ff;
  }
  button:disabled {
    background-color: #45265f99;
    box-shadow: none;
    cursor: not-allowed;
  }
  #stopAlarmBtn {
    margin-top: 20px;
    background-color: var(--neon-royal-blue);
    box-shadow:
      0 0 15px var(--neon-royal-blue),
      0 0 35px var(--neon-royal-blue);
  }
  #stopAlarmBtn:hover:not(:disabled) {
    background-color: #0034a8;
    box-shadow:
      0 0 25px #0047ab,
      0 0 45px #0047ab;
  }

  .status {
    margin-top: 20px;
    font-weight: 700;
    font-size: 1.15rem;
    letter-spacing: 0.7px;
    min-height: 26px;
    color: var(--neon-purple);
    text-shadow:
      0 0 6px var(--neon-purple);
  }

  .alarm-ringing {
    margin-top: 32px;
    font-size: 1.6rem;
    font-weight: 900;
    color: #7efff5;
    text-shadow:
      0 0 12px #7efff5,
      0 0 30px #7efff5,
      0 0 50px #7efff5;
  }
</style>
</head>
<body>
  <main class="container" role="main" aria-label="Neon themed alarm clock app">
    <h1>Neon Alarm Clock</h1>
    <div class="current-time" id="currentTime" aria-live="polite">--:--:--</div>

    <label for="alarmTime">Set Alarm Time:</label>
    <input id="alarmTime" type="time" aria-required="true" aria-label="Set alarm time" autocomplete="off" />

    <label for="soundSelect">Select Alarm Sound:</label>
    <select id="soundSelect" aria-label="Select alarm sound">
      <option value="beep" selected>Default Beep</option>
      <option value="glass">Glass Chime</option>
      <option value="digital">Digital Alarm</option>
      <option value="doorbell">Doorbell</option>
    </select>

    <button id="setAlarmBtn" aria-live="polite">Set Alarm</button>
    <button id="stopAlarmBtn" style="display:none;" aria-live="polite">Stop Alarm</button>

    <div class="status" id="status" aria-live="polite">No alarm set</div>
    <div class="alarm-ringing" id="alarmRinging" role="alert" aria-live="assertive" style="display:none;">⏰ Alarm ringing! Wake up!</div>
  </main>

<script>
  'use strict';

  const currentTimeElem = document.getElementById('currentTime');
  const alarmTimeInput = document.getElementById('alarmTime');
  const soundSelect = document.getElementById('soundSelect');
  const setAlarmBtn = document.getElementById('setAlarmBtn');
  const stopAlarmBtn = document.getElementById('stopAlarmBtn');
  const statusElem = document.getElementById('status');
  const alarmRingingElem = document.getElementById('alarmRinging');

  let alarmTime = null;
  let alarmTimeout = null;
  let alarmAudio = null;

  const soundFiles = {
    glass: 'https://actions.google.com/sounds/v1/alarms/glass_xylophone.ogg',
    digital: 'https://actions.google.com/sounds/v1/alarms/digital_watch_alarm_long.ogg',
    doorbell: 'https://actions.google.com/sounds/v1/alarms/doorbell.ogg'
  };

  // Update current time every second
  function updateCurrentTime() {
    const now = new Date();
    currentTimeElem.textContent = now.toLocaleTimeString();

    if(alarmTime){
      const nowTime = now.toTimeString().slice(0,5);
      if(nowTime === alarmTime){
        triggerAlarm();
      }
    }
  }

  // Beep using Web Audio API
  function playBeep(times=5, interval=700){
    const AudioContext = window.AudioContext || window.webkitAudioContext;
    if(!AudioContext) return;
    const ctx = new AudioContext();
    let count=0;
    function beep(){
      const osc = ctx.createOscillator();
      osc.type='sine';
      osc.frequency.setValueAtTime(1000, ctx.currentTime);
      osc.connect(ctx.destination);
      osc.start();
      setTimeout(()=>{
        osc.stop();
        count++;
        if(count<times) setTimeout(beep, interval);
      },300);
    }
    beep();
  }

  function triggerAlarm(){
    alarmRingingElem.style.display = 'block';
    setAlarmBtn.disabled = true;
    alarmTimeInput.disabled = true;
    soundSelect.disabled = true;
    stopAlarmBtn.style.display = 'block';
    const selectedSound = soundSelect.value;

    if(selectedSound === 'beep'){
      playBeep();
    } else {
      if(alarmAudio){
        alarmAudio.pause();
        alarmAudio = null;
      }
      const soundUrl = soundFiles[selectedSound];
      if(soundUrl){
        alarmAudio = new Audio(soundUrl);
        alarmAudio.loop = true;
        alarmAudio.play().catch(() => {
          playBeep();
        });
      } else {
        playBeep();
      }
    }
    statusElem.textContent = 'Alarm ringing!';
  }

  function stopAlarm(){
    alarmRingingElem.style.display = 'none';
    setAlarmBtn.disabled = false;
    alarmTimeInput.disabled = false;
    soundSelect.disabled = false;
    stopAlarmBtn.style.display = 'none';
    statusElem.textContent = 'Alarm stopped.';
    alarmTime = null;
    if(alarmAudio){
      alarmAudio.pause();
      alarmAudio.currentTime = 0;
      alarmAudio = null;
    }
  }

  setAlarmBtn.addEventListener('click', ()=>{
    if(!alarmTimeInput.value){
      alert('Please select a valid alarm time');
      return;
    }
    alarmTime = alarmTimeInput.value;
    statusElem.textContent = 'Alarm set for ' + alarmTime;
    setAlarmBtn.disabled = true;
    alarmTimeInput.disabled = true;
    soundSelect.disabled = true;
  });

  stopAlarmBtn.addEventListener('click', stopAlarm);

  setInterval(updateCurrentTime, 1000);
  updateCurrentTime();

</script>
</body>
</html>
