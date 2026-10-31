<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#0b1020">
<title>مذاكرتي | إعداد: زهراء أحمد</title>
<style>
:root{--bg:#0b1020;--panel:#11182b;--text:#f5f7ff;--muted:#9ba7c0;--primary:#7c5cff;--primary2:#5b8cff;--green:#21c98b;--yellow:#ffc857;--red:#ff647c;--border:rgba(255,255,255,.09);--shadow:0 18px 50px rgba(0,0,0,.25);}
*{box-sizing:border-box}
body{margin:0;font-family:Tahoma,Arial,sans-serif;background:radial-gradient(circle at 10% 0%,rgba(124,92,255,.18),transparent 28%),radial-gradient(circle at 90% 10%,rgba(91,140,255,.13),transparent 25%),var(--bg);color:var(--text);min-height:100vh;}
button,input,select,textarea{font:inherit}button{cursor:pointer;border:0}
.app{display:flex;min-height:100vh;}
.sidebar{width:260px;background:rgba(10,15,30,.9);border-left:1px solid var(--border);padding:22px 16px;position:fixed;right:0;top:0;bottom:0;z-index:20;}
.brand{display:flex;gap:12px;align-items:center;padding:8px 8px 25px;}
.logo{width:46px;height:46px;border-radius:15px;background:linear-gradient(135deg,var(--primary),var(--primary2));display:grid;place-items:center;font-size:23px;}
.brand h2{margin:0;font-size:18px;} .brand small{color:var(--muted);}
.nav{display:grid;gap:7px;} .nav button{background:transparent;color:var(--muted);padding:13px 14px;border-radius:12px;text-align:right;display:flex;gap:11px;align-items:center;}
.nav button:hover,.nav button.active{background:rgba(124,92,255,.14);color:#fff;}
.main{margin-right:260px;width:calc(100% - 260px);padding:22px;max-width:1500px;margin-left:auto;}
.topbar{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-bottom:20px;} .topbar h1{font-size:25px;margin:0 0 5px;} .topbar p{margin:0;color:var(--muted);}
.actions{display:flex;gap:8px;} .iconbtn,.primary,.ghost,.danger{border-radius:12px;padding:11px 14px;color:#fff;} .iconbtn,.ghost{background:var(--panel);border:1px solid var(--border);} .primary{background:linear-gradient(135deg,var(--primary),var(--primary2));box-shadow:0 10px 25px rgba(124,92,255,.2);} .danger{background:rgba(255,100,124,.12);color:#ff9aaa;border:1px solid rgba(255,100,124,.25);}
.grid{display:grid;gap:16px;} .stats{grid-template-columns:repeat(4,1fr);} .card{background:rgba(17,24,43,.84);border:1px solid var(--border);border-radius:20px;padding:18px;box-shadow:var(--shadow);backdrop-filter:blur(10px);}
.stat{display:flex;align-items:center;gap:14px;} .stat .ico{width:48px;height:48px;border-radius:14px;display:grid;place-items:center;background:rgba(124,92,255,.13);font-size:22px;} .stat b{font-size:25px;} .stat span{display:block;color:var(--muted);font-size:13px;margin-top:3px;}
.content{grid-template-columns:1.25fr .75fr;margin-top:16px;} .card h3{margin:0 0 15px;font-size:17px;}
.progress{height:9px;background:#252e47;border-radius:20px;overflow:hidden;} .progress>div{height:100%;background:linear-gradient(90deg,var(--primary),var(--primary2));border-radius:20px;transition:.3s;}
.task{display:flex;align-items:center;gap:12px;padding:12px 0;border-bottom:1px solid var(--border);} .task:last-child{border-bottom:0;} .check{width:23px;height:23px;border-radius:7px;border:2px solid #65708a;background:transparent;flex:0 0 auto;} .task.done .check{background:var(--green);border-color:var(--green);} .task.done .title{text-decoration:line-through;color:#75809a;} .task .title{font-weight:bold;} .task small{display:block;color:var(--muted);margin-top:4px;} .badge{margin-right:auto;padding:5px 8px;border-radius:8px;font-size:11px;background:rgba(255,200,87,.12);color:var(--yellow);}
.section{display:none;} .section.active{display:block;} .toolbar{display:flex;flex-wrap:wrap;gap:9px;margin-bottom:15px;}
input,select,textarea{background:#0e1528;color:#fff;border:1px solid var(--border);border-radius:11px;padding:11px;outline:none;width:100%;} input:focus,select:focus,textarea:focus{border-color:var(--primary);}
.formgrid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;} .formgrid .full{grid-column:1/-1;}
.modal{position:fixed;inset:0;background:rgba(0,0,0,.65);display:none;align-items:center;justify-content:center;z-index:50;padding:18px;} .modal.show{display:flex;} .modalbox{width:min(600px,100%);background:var(--panel);border:1px solid var(--border);border-radius:20px;padding:20px;max-height:90vh;overflow:auto;} .modalhead{display:flex;justify-content:space-between;align-items:center;margin-bottom:15px;} .modalhead h3{margin:0;}
.week{display:grid;grid-template-columns:repeat(7,1fr);gap:9px;} .day{min-height:210px;background:#0e1528;border:1px solid var(--border);border-radius:15px;padding:10px;} .dayhead{text-align:center;font-weight:bold;padding-bottom:9px;border-bottom:1px solid var(--border);margin-bottom:7px;} .slot{padding:9px;border-radius:10px;background:rgba(124,92,255,.11);margin:7px 0;font-size:12px;} .slot b{display:block;} .slot small{color:var(--muted);}
.timerWrap{text-align:center;padding:12px;} .timer{font-size:75px;font-weight:900;letter-spacing:3px;margin:15px 0;background:linear-gradient(135deg,#fff,#aab7ff);-webkit-background-clip:text;color:transparent;} .mode{display:flex;justify-content:center;gap:7px;margin-bottom:12px;} .mode button{padding:8px 12px;border-radius:9px;background:#202a44;color:var(--muted);} .mode button.active{background:var(--primary);color:#fff;} .timerBtns{display:flex;justify-content:center;gap:8px;} .timerBtns button{min-width:100px;} .quote{font-size:18px;line-height:1.8;text-align:center;padding:20px;color:#dce2f5;} .goal{padding:13px 0;border-bottom:1px solid var(--border);} .goal:last-child{border:0;} .goalTop{display:flex;justify-content:space-between;gap:10px;} .goalTop span{color:var(--muted);font-size:12px;} .notes{min-height:250px;resize:vertical;} .empty{text-align:center;color:var(--muted);padding:25px;} .mobileNav{display:none;} .toast{position:fixed;bottom:20px;left:20px;background:#fff;color:#111;padding:12px 16px;border-radius:12px;box-shadow:var(--shadow);display:none;z-index:100;font-weight:bold;} .toast.show{display:block;}
@media(max-width:950px){.sidebar{display:none;} .main{margin:0;width:100%;padding:14px;padding-bottom:90px;} .stats{grid-template-columns:repeat(2,1fr);} .content{grid-template-columns:1fr;} .week{grid-template-columns:repeat(2,1fr);} .mobileNav{position:fixed;display:flex;bottom:0;left:0;right:0;background:rgba(10,15,30,.96);border-top:1px solid var(--border);z-index:30;padding:7px;gap:5px;justify-content:space-around;} .mobileNav button{background:transparent;color:var(--muted);font-size:11px;padding:7px;} .mobileNav button.active{color:#fff;} .mobileNav span{display:block;font-size:19px;} .timer{font-size:60px;}}
@media(max-width:560px){.topbar{align-items:flex-start;} .topbar h1{font-size:20px;} .actions .ghost{display:none;} .stats{gap:9px;} .card{padding:14px;border-radius:16px;} .week{grid-template-columns:1fr;} .formgrid{grid-template-columns:1fr;} .formgrid .full{grid-column:auto;}}
</style>
</head>
<body>
<div class="app">
<aside class="sidebar">
<div class="brand"><div class="logo">📚</div><div><h2>مذاكرتي</h2><small>إعداد: زهراء أحمد</small></div></div>
<nav class="nav" id="sideNav">
<button class="active" data-page="home">🏠 لوحة التحكم</button>
<button data-page="tasks">✅ المهام</button>
<button data-page="schedule">📅 جدول المذاكرة</button>
<button data-page="timer">⏱️ مؤقت المذاكرة</button>
<button data-page="goals">🎯 الأهداف</button>
<button data-page="subjects">📚 المواد</button>
<button data-page="notes">📝 الملاحظات اليومية</button>
<button data-page="stats">📊 الإحصائيات</button>
</nav>
</aside>
<main class="main">
<div class="topbar">
<div><h1 id="pageTitle">لوحة التحكم</h1><p>الطالبة: <strong style="color:#9d8cff">زهراء أحمد</strong> • <span id="dateLine"></span></p></div>
<div class="actions"><button class="ghost" onclick="toggleTheme()">🌓 المظهر</button><button class="primary" onclick="openTaskModal()">＋ مهمة</button></div>
</div>
<section class="section active" id="home">
<div class="card" style="margin-bottom:16px;text-align:center;padding:25px">
<div style="font-size:14px;color:var(--muted);margin-bottom:6px">مرحبًا بكِ في تطبيق</div>
<div style="font-size:30px;font-weight:900;background:linear-gradient(135deg,#fff,#9d8cff);-webkit-background-clip:text;color:transparent">مذاكرتي</div>
<div style="font-size:18px;margin-top:7px">👩‍🎓 زهراء أحمد</div>
<div style="color:var(--muted);margin-top:7px">خططي • ذاكري • أنجزي • طوري نفسك 🚀</div>
</div>
<div class="grid stats">
<div class="card stat"><div class="ico">🔥</div><div><b id="streak">0</b><span>أيام الاستمرار</span></div></div>
<div class="card stat"><div class="ico">✅</div><div><b id="doneCount">0</b><span>مهام مكتملة</span></div></div>
<div class="card stat"><div class="ico">⏱️</div><div><b id="studyMinutes">0</b><span>دقائق مذاكرة</span></div></div>
<div class="card stat"><div class="ico">⭐</div><div><b id="points">0</b><span>نقاط الإنجاز</span></div></div>
</div>
<div class="grid content">
<div class="card"><h3>📌 مهام اليوم</h3><div id="todayTasks"></div></div>
<div class="card"><h3>🎯 تقدمك اليوم</h3><div style="display:flex;justify-content:space-between;margin-bottom:9px"><span>نسبة الإنجاز</span><b id="todayPercent">0%</b></div><div class="progress"><div id="todayProgress" style="width:0%"></div></div><div class="quote" id="quote"></div></div>
</div>
</section>
<section class="section" id="tasks">
<div class="card">
<div class="toolbar">
<button class="primary" onclick="openTaskModal()">＋ إضافة مهمة</button>
<select id="taskFilter" onchange="renderTasks()" style="max-width:180px"><option value="all">كل المهام</option><option value="todo">غير مكتملة</option><option value="done">مكتملة</option></select>
<select id="priorityFilter" onchange="renderTasks()" style="max-width:180px"><option value="all">كل الأولويات</option><option value="high">عالية</option><option value="medium">متوسطة</option><option value="low">منخفضة</option></select>
</div>
<div id="tasksList"></div>
</div>
</section>
<section class="section" id="schedule">
<div class="card">
<div class="toolbar"><button class="primary" onclick="openScheduleModal()">＋ حصة جديدة</button><button class="ghost" onclick="clearSchedule()">مسح الجدول</button></div>
<div class="week" id="week"></div>
</div>
</section>
<section class="section" id="timer">
<div class="card timerWrap">
<h3>⏱️ مؤقت المذاكرة الذكي</h3>
<div class="mode"><button class="active" data-min="25">25 دقيقة</button><button data-min="50">50 دقيقة</button><button data-min="custom">مخصص</button></div>
<div class="timer" id="timerDisplay">25:00</div>
<p id="timerStatus" style="color:var(--muted)">جاهزة للمذاكرة 💪</p>
<div class="timerBtns">
<button class="primary" id="timerStart" onclick="startTimer()">ابدأي</button>
<button class="ghost" onclick="pauseTimer()">إيقاف</button>
<button class="danger" onclick="resetTimer()">إعادة</button>
</div>
<div style="max-width:400px;margin:25px auto 0"><label>المادة التي تذاكريها</label><select id="timerSubject" style="margin-top:7px"></select></div>
</div>
</section>
<section class="section" id="goals">
<div class="card"><div class="toolbar"><button class="primary" onclick="openGoalModal()">＋ هدف جديد</button></div><div id="goalsList"></div></div>
</section>
<section class="section" id="subjects">
<div class="card"><div class="toolbar"><button class="primary" onclick="openSubjectModal()">＋ إضافة مادة</button></div><div id="subjectsList"></div></div>
</section>
<section class="section" id="notes">
<div class="card">
<h3>📝 ملاحظاتي اليوم</h3>
<textarea class="notes" id="dailyNotes" placeholder="اكتبي أهم ما أنجزتيه، ما تحتاجين لمراجعته، أو أي ملاحظات لليوم..."></textarea>
<div style="display:flex;gap:8px;margin-top:10px">
<button class="primary" onclick="saveNotes()">💾 حفظ الملاحظات</button>
<button class="ghost" onclick="clearNotes()">مسح</button>
</div>
</div>
</section>
<section class="section" id="stats">
<div class="grid stats">
<div class="card stat"><div class="ico">📚</div><div><b id="allTasks">0</b><span>إجمالي المهام</span></div></div>
<div class="card stat"><div class="ico">🎯</div><div><b id="goalDone">0</b><span>أهداف مكتملة</span></div></div>
<div class="card stat"><div class="ico">📖</div><div><b id="subjectCount">0</b><span>المواد</span></div></div>
<div class="card stat"><div class="ico">📈</div><div><b id="completionRate">0%</b><span>نسبة الإنجاز</span></div></div>
</div>
<div class="card" style="margin-top:16px">
<h3>🏆 مستوى الطالبة</h3>
<div style="display:flex;justify-content:space-between;margin-bottom:8px"><b id="levelName">مبتدئة</b><span id="levelPoints">0 / 100 XP</span></div>
<div class="progress"><div id="levelBar" style="width:0%"></div></div>
<p style="color:var(--muted);margin-bottom:0">كل مهمة مكتملة = 10 نقاط، وكل جلسة مذاكرة مكتملة = 5 نقاط.</p>
</div>
<div class="card" style="margin-top:16px">
<h3>⚙️ البيانات</h3>
<div class="toolbar">
<button class="ghost" onclick="exportData()">⬇️ تصدير البيانات</button>
<button class="ghost" onclick="document.getElementById('importFile').click()">⬆️ استيراد</button>
<button class="danger" onclick="resetAll()">🗑️ حذف كل البيانات</button>
<input id="importFile" type="file" accept=".json" style="display:none" onchange="importData(event)">
</div>
</div>
</section>
</main>
</div>
<div class="mobileNav" id="mobileNav">
<button class="active" data-page="home"><span>🏠</span>الرئيسية</button>
<button data-page="tasks"><span>✅</span>المهام</button>
<button data-page="schedule"><span>📅</span>الجدول</button>
<button data-page="timer"><span>⏱️</span>المؤقت</button>
<button data-page="stats"><span>📊</span>إحصائيات</button>
</div>
<div class="modal" id="modal">
<div class="modalbox">
<div class="modalhead"><h3 id="modalTitle"></h3><button class="iconbtn" onclick="closeModal()">✕</button></div>
<div id="modalBody"></div>
</div>
</div>
<div class="toast" id="toast"></div>
<script>
const KEY='mazakarty_zahra_v2';
const defaultSubjects=['اللغة العربية','اللغة الإنجليزية','الرياضيات','الكيمياء','الفيزياء','التاريخ','المواد الشرعية'];
const defaultData={tasks:[],schedule:[],goals:[],subjects:defaultSubjects,notes:{},minutes:0,points:0,studyDays:{},theme:'dark'};
let data=load();
let timer={seconds:1500,running:false,interval:null,base:1500};

function load(){
try{
const saved=JSON.parse(localStorage.getItem(KEY)||'null');
if(!saved){return {...defaultData};}
return {...defaultData,...saved,subjects:Array.isArray(saved.subjects)?saved.subjects.filter(s=>s!=='الأحياء'):[...defaultSubjects]};
}catch(e){return {...defaultData};}
}

function save(){localStorage.setItem(KEY,JSON.stringify(data));}

function esc(s){
return String(s??'').replace(/[&<>"']/g,m=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#039;'}[m]));
}

function today(){return new Date().toISOString().slice(0,10);}
function dateText(){return new Date().toLocaleDateString('ar-EG',{weekday:'long',year:'numeric',month:'long',day:'numeric'});}
document.getElementById('dateLine').textContent=dateText();

const quotes=[
'النجاح لا يأتي من كثرة الوقت، بل من حسن استغلاله.',
'ابدئي الآن، ولو بخطوة صغيرة.',
'كل صفحة تذاكريها تقربك من هدفك.',
'نظمي وقتك، وستجدين أن الوقت يكفيك.',
'لا تنتظري الحماس؛ ابدئي وسيأتي الحماس مع الإنجاز.',
'مستقبلك يستحق ساعة تركيز إضافية.'
];

function showPage(id){
document.querySelectorAll('.section').forEach(x=>x.classList.toggle('active',x.id===id));
document.querySelectorAll('[data-page]').forEach(x=>x.classList.toggle('active',x.dataset.page===id));
const titles={home:'لوحة التحكم',tasks:'المهام',schedule:'جدول المذاكرة',timer:'مؤقت المذاكرة',goals:'الأهداف',subjects:'المواد',notes:'الملاحظات اليومية',stats:'الإحصائيات'};
document.getElementById('pageTitle').textContent=titles[id]||'مذاكرتي';
if(id==='tasks')renderTasks();
if(id==='schedule')renderSchedule();
if(id==='goals')renderGoals();
if(id==='subjects')renderSubjects();
if(id==='stats')renderStats();
if(id==='home')renderHome();
if(id==='notes')renderNotes();
}

document.querySelectorAll('[data-page]').forEach(b=>b.onclick=()=>showPage(b.dataset.page));

function renderHome(){
const tt=data.tasks.filter(t=>t.date===today());
const done=tt.filter(t=>t.done).length;
const pct=tt.length?Math.round(done/tt.length*100):0;
document.getElementById('todayTasks').innerHTML=tt.length?tt.slice(0,7).map(taskHTML).join(''):'<div class="empty">لا توجد مهام اليوم 🎉<br>أضف أول مهمة وابدأ.</div>';
document.getElementById('todayPercent').textContent=pct+'%';
document.getElementById('todayProgress').style.width=pct+'%';
document.getElementById('quote').textContent='“'+quotes[new Date().getDate()%quotes.length]+'”';
document.getElementById('doneCount').textContent=data.tasks.filter(t=>t.done).length;
document.getElementById('studyMinutes').textContent=data.minutes;
document.getElementById('points').textContent=data.points;
document.getElementById('streak').textContent=calcStreak();
}

function taskHTML(t){
const p={high:['عالية','red'],medium:['متوسطة','yellow'],low:['منخفضة','green']}[t.priority]||['متوسطة','yellow'];
return `<div class="task ${t.done?'done':''}" onclick="toggleTask('${t.id}')"><button class="check">${t.done?'✓':''}</button><div><div class="title">${esc(t.title)}</div><small>${esc(t.subject||'عام')} • ${esc(t.date||'')}</small></div><span class="badge">${p[0]}</span></div>`;
}

function renderTasks(){
let arr=[...data.tasks];
let f=document.getElementById('taskFilter').value;
let p=document.getElementById('priorityFilter').value;
if(f==='todo')arr=arr.filter(t=>!t.done);
if(f==='done')arr=arr.filter(t=>t.done);
if(p!=='all')arr=arr.filter(t=>t.priority===p);
arr.sort((a,b)=>(a.date||'').localeCompare(b.date||''));
document.getElementById('tasksList').innerHTML=arr.length?arr.map(t=>taskHTML(t)+`<div style="text-align:left;margin-top:-42px;margin-bottom:12px"><button class="danger" style="padding:6px 9px" onclick="event.stopPropagation();deleteTask('${t.id}')">حذف</button></div>`).join(''):'<div class="empty">لا توجد مهام هنا.</div>';
}

function openTaskModal(){
document.getElementById('modalTitle').textContent='إضافة مهمة جديدة';
document.getElementById('modalBody').innerHTML=`<div class="formgrid"><div class="full"><label>اسم المهمة</label><input id="mTitle" placeholder="مثال: مراجعة الكيمياء"></div><div><label>المادة</label><select id="mSubject">${data.subjects.map(s=>`<option>${esc(s)}</option>`).join('')}<option>عام</option></select></div><div><label>التاريخ</label><input id="mDate" type="date" value="${today()}"></div><div><label>الأولوية</label><select id="mPriority"><option value="high">عالية</option><option value="medium" selected>متوسطة</option><option value="low">منخفضة</option></select></div><div><label>المدة بالدقائق</label><input id="mDuration" type="number" value="30" min="5"></div><div class="full"><button class="primary" style="width:100%" onclick="addTask()">حفظ المهمة</button></div></div>`;
openModal();
}

function addTask(){
const title=document.getElementById('mTitle').value.trim();
if(!title){return toast('اكتب اسم المهمة أولًا');}
data.tasks.push({
id:Date.now().toString(),
title:title,
subject:document.getElementById('mSubject').value,
date:document.getElementById('mDate').value,
priority:document.getElementById('mPriority').value,
duration:+document.getElementById('mDuration').value||30,
done:false
});
save();
closeModal();
renderHome();
renderTasks();
toast('تمت إضافة المهمة ✅');
}

function toggleTask(id){
const t=data.tasks.find(x=>x.id===id);
if(!t)return;
t.done=!t.done;
if(t.done)data.points+=10;
else data.points=Math.max(0,data.points-10);
if(t.done)data.studyDays[t.date]=true;
save();
renderHome();
renderTasks();
renderStats();
}

function deleteTask(id){
data.tasks=data.tasks.filter(t=>t.id!==id);
save();
renderTasks();
renderHome();
toast('تم حذف المهمة');
}

function calcStreak(){
let d=new Date();
let n=0;
while(true){
let k=d.toISOString().slice(0,10);
if(data.studyDays[k]){
n++;
d.setDate(d.getDate()-1);
}else{break;}
}
return n;
}

const days=['السبت','الأحد','الاثنين','الثلاثاء','الأربعاء','الخميس','الجمعة'];

function renderSchedule(){
document.getElementById('week').innerHTML=days.map(day=>`<div class="day"><div class="dayhead">${day}</div>${data.schedule.filter(x=>x.day===day).map(x=>`<div class="slot"><b>${esc(x.subject)}</b><small>${esc(x.time)} • ${esc(x.duration)} دقيقة</small><br><button class="danger" style="margin-top:5px;padding:4px 7px;font-size:10px" onclick="deleteSlot('${x.id}')">حذف</button></div>`).join('')||'<div class="empty" style="padding:18px 3px">فارغ</div>'}</div>`).join('');
}

function openScheduleModal(){
document.getElementById('modalTitle').textContent='إضافة حصة للجدول';
document.getElementById('modalBody').innerHTML=`<div class="formgrid"><div><label>اليوم</label><select id="sDay">${days.map(x=>`<option>${x}</option>`).join('')}</select></div><div><label>المادة</label><select id="sSub">${data.subjects.map(s=>`<option>${esc(s)}</option>`).join('')}</select></div><div><label>الوقت</label><input id="sTime" type="time" value="16:00"></div><div><label>المدة</label><input id="sDur" type="number" value="60" min="5"></div><div class="full"><button class="primary" style="width:100%" onclick="addSlot()">إضافة للجدول</button></div></div>`;
openModal();
}

function addSlot(){
data.schedule.push({
id:Date.now().toString(),
day:document.getElementById('sDay').value,
subject:document.getElementById('sSub').value,
time:document.getElementById('sTime').value,
duration:+document.getElementById('sDur').value||60
});
save();
closeModal();
renderSchedule();
toast('تم تحديث الجدول 📅');
}

function deleteSlot(id){
data.schedule=data.schedule.filter(x=>x.id!==id);
save();
renderSchedule();
}

function clearSchedule(){
if(confirm('مسح جدول المذاكرة بالكامل؟')){
data.schedule=[];
save();
renderSchedule();
}
}

function setTimerMin(m){
if(timer.running){pauseTimer();}
if(m==='custom'){
let v=prompt('⏱️ اكتب مدة المؤقت بالدقائق\nمثال: 35 أو 90','45');
if(v===null)return;
v=String(v).trim().replace(',', '.');
const minutes=Number(v);
if(!Number.isFinite(minutes)||minutes<=0||minutes>1440){
toast('أدخل مدة صحيحة من 1 إلى 1440 دقيقة');
return;
}
m=minutes;
timer.custom=true;
timer.customMinutes=minutes;
}else{
timer.custom=false;
}
timer.base=timer.seconds=Math.round(Number(m)*60);
updateTimer();
document.querySelectorAll('.mode button').forEach(b=>{
if(b.dataset.min==='custom'){
b.classList.toggle('active',timer.custom===true);
}else{
b.classList.toggle('active',Number(b.dataset.min)===Number(m));
}
});
document.getElementById('timerStatus').textContent=timer.custom?`مؤقت مخصص: ${formatMinutes(Number(m))}`:'جاهزة للمذاكرة 💪';
}

function formatMinutes(minutes){
const h=Math.floor(minutes/60);
const m=minutes%60;
if(h>0){
return m>0?`${h} ساعة و ${m} دقيقة`:`${h} ساعة`;
}
return `${m} دقيقة`;
}

document.querySelectorAll('.mode button').forEach(b=>b.onclick=()=>setTimerMin(b.dataset.min));

function updateTimer(){
let m=Math.floor(timer.seconds/60);
let s=timer.seconds%60;
document.getElementById('timerDisplay').textContent=String(m).padStart(2,'0')+':'+String(s).padStart(2,'0');
}

function startTimer(){
if(timer.running)return;
if(timer.seconds<=0){resetTimer();}
timer.running=true;
document.getElementById('timerStatus').textContent='مذاكرة جارية... ركّزي 🎯';
document.getElementById('timerStart').textContent='يعمل الآن';
timer.interval=setInterval(()=>{
if(timer.seconds>0){
timer.seconds--;
updateTimer();
}else{
finishTimer();
}
},1000);
}

function pauseTimer(){
if(!timer.running){
document.getElementById('timerStatus').textContent='المؤقت متوقف مؤقتًا';
return;
}
timer.running=false;
clearInterval(timer.interval);
document.getElementById('timerStatus').textContent='تم إيقاف المؤقت مؤقتًا';
document.getElementById('timerStart').textContent='استمرار';
}

function resetTimer(){
timer.running=false;
clearInterval(timer.interval);
timer.seconds=timer.base;
updateTimer();
document.getElementById('timerStatus').textContent=timer.custom?`مؤقت مخصص: ${formatMinutes(timer.base/60)}`:'جاهزة للمذاكرة 💪';
document.getElementById('timerStart').textContent='ابدأي';
}

function finishTimer(){
timer.running=false;
clearInterval(timer.interval);
let mins=Math.round(timer.base/60);
data.minutes+=mins;
data.points+=5;
data.studyDays[today()]=true;
save();
toast('أحسنتِ! انتهت جلسة المذاكرة 🏆');
document.getElementById('timerStatus').textContent='انتهت الجلسة! خذي استراحة قصيرة ☕';
renderHome();
renderStats();
resetTimer();
}

function fillSubjects(){
document.getElementById('timerSubject').innerHTML=data.subjects.map(s=>`<option>${esc(s)}</option>`).join('');
}

function renderSubjects(){
document.getElementById('subjectsList').innerHTML=data.subjects.map((s,i)=>`<div class="task"><div class="ico">📘</div><div><b>${esc(s)}</b><small>${data.tasks.filter(t=>t.subject===s&&t.done).length} مهام مكتملة</small></div><button class="danger" style="margin-right:auto" onclick="deleteSubject(${i})">حذف</button></div>`).join('');
}

function openSubjectModal(){
document.getElementById('modalTitle').textContent='إضافة مادة';
document.getElementById('modalBody').innerHTML=`<input id="subName" placeholder="اسم المادة"><button class="primary" style="width:100%;margin-top:10px" onclick="addSubject()">إضافة</button>`;
openModal();
}

function addSubject(){
let s=document.getElementById('subName').value.trim();
if(!s)return;
if(!data.subjects.includes(s))data.subjects.push(s);
save();
closeModal();
renderSubjects();
fillSubjects();
toast('تمت إضافة المادة 📚');
}

function deleteSubject(i){
if(confirm('حذف المادة؟')){
data.subjects.splice(i,1);
save();
renderSubjects();
fillSubjects();
}
}

function renderGoals(){
document.getElementById('goalsList').innerHTML=data.goals.length?data.goals.map(g=>`<div class="goal"><div class="goalTop"><b>${esc(g.title)}</b><span>${g.progress}%</span></div><div class="progress" style="margin:9px 0"><div style="width:${g.progress}%"></div></div><div style="display:flex;gap:7px"><button class="ghost" onclick="changeGoal('${g.id}',5)">+5%</button><button class="ghost" onclick="changeGoal('${g.id}',-5)">-5%</button><button class="danger" onclick="deleteGoal('${g.id}')">حذف</button></div></div>`).join(''):'<div class="empty">ضعي هدفك الأول 📈</div>';
}

function openGoalModal(){
document.getElementById('modalTitle').textContent='هدف جديد';
document.getElementById('modalBody').innerHTML=`<div class="formgrid"><div class="full"><label>الهدف</label><input id="gTitle" placeholder="مثال: إنهاء الباب الأول في الكيمياء"></div><div class="full"><button class="primary" style="width:100%" onclick="addGoal()">إضافة الهدف</button></div></div>`;
openModal();
}

function addGoal(){
let t=document.getElementById('gTitle').value.trim();
if(!t)return;
data.goals.push({id:Date.now().toString(),title:t,progress:0});
save();
closeModal();
renderGoals();
renderStats();
toast('تمت إضافة الهدف 🎯');
}

function changeGoal(id,n){
let g=data.goals.find(x=>x.id===id);
if(g){
let old=g.progress;
g.progress=Math.max(0,Math.min(100,g.progress+n));
if(old<100&&g.progress===100)data.points+=20;
save();
renderGoals();
renderStats();
renderHome();
}
}

function deleteGoal(id){
data.goals=data.goals.filter(x=>x.id!==id);
save();
renderGoals();
renderStats();
}

function saveNotes(){
data.notes[today()]=document.getElementById('dailyNotes').value;
save();
toast('تم حفظ ملاحظات اليوم 💾');
}

function clearNotes(){
document.getElementById('dailyNotes').value='';
data.notes[today()]='';
save();
}

function renderNotes(){
document.getElementById('dailyNotes').value=data.notes[today()]||'';
}

function renderStats(){
document.getElementById('allTasks').textContent=data.tasks.length;
document.getElementById('goalDone').textContent=data.goals.filter(g=>g.progress===100).length;
document.getElementById('subjectCount').textContent=data.subjects.length;
const rate=data.tasks.length?Math.round(data.tasks.filter(t=>t.done).length/data.tasks.length*100):0;
document.getElementById('completionRate').textContent=rate+'%';
let level=Math.floor(data.points/100)+1;
let cur=data.points%100;
document.getElementById('levelName').textContent='المستوى '+level;
document.getElementById('levelPoints').textContent=cur+' / 100 XP';
document.getElementById('levelBar').style.width=cur+'%';
}

function exportData(){
let blob=new Blob([JSON.stringify(data,null,2)],{type:'application/json'});
let a=document.createElement('a');
a.href=URL.createObjectURL(blob);
a.download='mazakarty-zahra-backup.json';
a.click();
URL.revokeObjectURL(a.href);
toast('تم تصدير البيانات');
}

function importData(e){
let f=e.target.files[0];
if(!f)return;
let r=new FileReader();
r.onload=()=>{
try{
data={...defaultData,...JSON.parse(r.result)};
data.subjects=(data.subjects||defaultSubjects).filter(s=>s!=='الأحياء');
save();
location.reload();
}catch(x){
toast('ملف غير صالح');
}
};
r.readAsText(f);
}

function resetAll(){
if(confirm('سيتم حذف كل المهام والجدول والأهداف والإحصائيات. هل أنت متأكدة؟')){
localStorage.removeItem(KEY);
location.reload();
}
}

function toggleTheme(){
data.theme=data.theme==='light'?'dark':'light';
save();
applyTheme();
}

function applyTheme(){
if(data.theme==='light'){
document.documentElement.style.setProperty('--bg','#f3f6fc');
document.documentElement.style.setProperty('--panel','#fff');
document.documentElement.style.setProperty('--text','#172033');
document.documentElement.style.setProperty('--muted','#647089');
document.documentElement.style.setProperty('--border','rgba(20,30,60,.1)');
}else{
document.documentElement.style.setProperty('--bg','#0b1020');
document.documentElement.style.setProperty('--panel','#11182b');
document.documentElement.style.setProperty('--text','#f5f7ff');
document.documentElement.style.setProperty('--muted','#9ba7c0');
document.documentElement.style.setProperty('--border','rgba(255,255,255,.09)');
}
}

function openModal(){
document.getElementById('modal').classList.add('show');
}

function closeModal(){
document.getElementById('modal').classList.remove('show');
}

document.getElementById('modal').addEventListener('click',e=>{
if(e.target.id==='modal')closeModal();
});

function toast(msg){
let t=document.getElementById('toast');
t.textContent=msg;
t.classList.add('show');
clearTimeout(window.toastT);
window.toastT=setTimeout(()=>t.classList.remove('show'),2200);
}

document.addEventListener('keydown',e=>{
if(e.key==='Escape')closeModal();
});

function init(){
applyTheme();
fillSubjects();
renderHome();
renderTasks();
renderSchedule();
renderGoals();
renderSubjects();
renderStats();
renderNotes();
updateTimer();
}

init();
</script>
</body>
</html>
