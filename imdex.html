<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Geo_Log Verification OJT System</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root { --wvsu-blue: #0369a1; --sky-bg: #f0f9ff; }
        body { background-color: var(--sky-bg); color: var(--wvsu-blue); overflow: hidden; font-family: sans-serif; -webkit-tap-highlight-color: transparent; }
        .glass { background: rgba(255, 255, 255, 0.98); border: 1px solid rgba(14, 165, 233, 0.2); border-radius: 1.5rem; }
        #sidebar.hidden-sidebar { transform: translateX(-100%); }
        #sidebar { position: fixed; inset: 0; width: 16rem; z-index: 300; transition: transform 0.1s linear; }
        .page-content { display: none; height: 100%; overflow-y: auto; }
        .page-active { display: block; }
        .role-btn-active { background-color: #0284c7 !important; color: white !important; }
        .btn-time-in { background: #10b981; color: white; }
        .btn-time-out { background: #ef4444; color: white; }
        #login-screen { position: fixed; inset: 0; z-index: 500; display: flex; align-items: center; justify-content: center; background: var(--sky-bg); }
        .hidden-login { display: none !important; }
        
        .calendar-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem; }
        .calendar-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 4px; text-align: center; }
        .weekday { font-size: 9px; font-weight: 900; color: #94a3b8; padding-bottom: 5px; text-transform: uppercase; }
        .day-box { aspect-ratio: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; font-size: 11px; font-weight: 700; border-radius: 10px; background: #fff; border: 1px solid #f1f5f9; position: relative; }
        .day-active { background: #0ea5e9; color: white; border-color: #0284c7; }
        .today { border: 2px solid #0369a1; color: #0369a1; }
        .dot { width: 4px; height: 4px; background: #10b981; border-radius: 50%; position: absolute; bottom: 4px; }
    </style>
</head>
<body class="min-h-screen">

    <div id="login-screen">
        <div class="w-full max-w-xs p-8 glass shadow-2xl text-center space-y-6">
            <div>
                <h1 class="font-black text-sky-900 uppercase text-[10px]">West Visayas State University</h1>
                <p class="text-[12px] font-black text-sky-600 uppercase">Pototan Campus</p>
                <div class="h-[2px] w-12 bg-sky-200 mx-auto my-2"></div>
                <p class="text-[9px] font-bold text-sky-400 uppercase tracking-widest">Geo_Log OJT Verification</p>
            </div>
            
            <div class="flex gap-1 bg-sky-100 p-1 rounded-xl">
                <button onclick="setRole('student')" id="btn-student" class="flex-1 py-2 rounded-lg text-[10px] font-black role-btn-active">STUDENT</button>
                <button onclick="setRole('prof')" id="btn-prof" class="flex-1 py-2 rounded-lg text-[10px] font-black text-sky-400">PROFESSOR</button>
            </div>

            <div class="space-y-2 text-left">
                <input type="text" id="login-user" placeholder="ID Number" class="w-full p-4 rounded-xl border-2 font-bold outline-none border-sky-50 focus:border-sky-400">
                <input type="password" id="login-pass" placeholder="Year of Birth" class="w-full p-4 rounded-xl border-2 font-bold outline-none border-sky-50 focus:border-sky-400">
            </div>

            <button onclick="attemptLogin()" class="w-full py-4 bg-sky-600 text-white rounded-xl font-black uppercase text-xs shadow-lg">Enter System</button>
        </div>
    </div>

    <div id="main-app" class="hidden h-screen flex flex-col">
        <header class="bg-white border-b p-4 text-center shrink-0">
            <h1 class="font-black text-sky-900 uppercase text-[11px] tracking-tight">Geo_Log Verification OJT System</h1>
            <p class="font-bold text-sky-500 text-[9px] uppercase tracking-tighter">West Visayas State University • Pototan Campus</p>
        </header>

        <main class="flex-1 relative p-4 overflow-hidden">
            
            <div id="dash-page" class="page-content space-y-4">
                <div class="flex justify-between items-center">
                    <button onclick="toggleMenu(true)" class="w-10 h-10 glass flex items-center justify-center text-xl">☰</button>
                    <p id="clock" class="font-black text-sky-600 tabular-nums">00:00:00</p>
                </div>
                
                <div class="glass p-6 text-center border-t-4 border-sky-600 shadow-md">
                    <h2 id="user-name-title" class="text-lg font-black uppercase text-sky-800">...</h2>
                    <p id="user-course-title" class="text-[9px] font-bold text-sky-400 uppercase tracking-widest mb-6">...</p>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <button onclick="instantLog('IN')" class="btn-time-in p-6 rounded-2xl font-black uppercase text-xs shadow-md">Time In</button>
                        <button onclick="instantLog('OUT')" class="btn-time-out p-6 rounded-2xl font-black uppercase text-xs shadow-md">Time Out</button>
                    </div>
                </div>

                <div class="px-2">
                    <h4 class="text-[9px] font-black text-sky-300 uppercase mb-2">Recent Logs</h4>
                    <div id="log-preview" class="space-y-2"></div>
                </div>
            </div>

            <div id="calendar-page" class="page-content space-y-4">
                <div class="flex justify-between items-center px-2">
                    <button onclick="toggleMenu(true)" class="w-10 h-10 glass flex items-center justify-center text-xl">☰</button>
                    <h3 class="font-black text-xs uppercase text-sky-800">Attendance Verification</h3>
                </div>
                
                <div class="glass p-5 shadow-sm">
                    <div class="calendar-header">
                        <h4 id="month-name" class="font-black text-sm uppercase text-sky-700"></h4>
                    </div>
                    <div class="calendar-grid">
                        <div class="weekday">S</div><div class="weekday">M</div><div class="weekday">T</div>
                        <div class="weekday">W</div><div class="weekday">T</div><div class="weekday">F</div>
                        <div class="weekday">S</div>
                    </div>
                    <div id="calendar-days" class="calendar-grid"></div>
                </div>

                <div class="glass p-4 space-y-2 max-h-[35vh] overflow-y-auto">
                    <h4 class="text-[10px] font-black uppercase text-sky-400">Verification History</h4>
                    <div id="full-log-list" class="space-y-2"></div>
                </div>
            </div>

            <div id="directory-page" class="page-content space-y-3">
                <div class="flex justify-between items-center px-2">
                    <button onclick="toggleMenu(true)" class="w-10 h-10 glass flex items-center justify-center text-xl">☰</button>
                    <h3 class="font-black text-xs uppercase">Master Student Registry</h3>
                </div>
                <input type="text" id="dir-search" oninput="renderDir()" placeholder="Search Name or ID..." class="w-full p-4 rounded-xl border-2 font-bold text-xs outline-none focus:border-sky-400">
                <div id="student-list" class="space-y-2"></div>
            </div>

            <div id="student-detail-page" class="page-content space-y-4">
                <button onclick="showPage('directory-page')" class="text-sky-600 font-black text-xs px-2">← Back to Registry</button>
                <div class="glass p-6">
                    <div id="detail-header" class="text-center space-y-1 mb-4"></div>
                    <hr class="mb-4">
                    <h4 class="font-black text-[10px] uppercase mb-2">Authenticated Log History</h4>
                    <div id="detail-log-list" class="space-y-2"></div>
                </div>
            </div>

            <div id="profile-page" class="page-content space-y-4">
                <div class="glass p-6">
                    <h3 class="font-black text-center mb-4 text-xs uppercase">Personal Information</h3>
                    <div class="space-y-3">
                        <input type="text" id="p-id" readonly class="w-full p-4 rounded-xl border-2 font-black text-xs">
                        <input type="text" id="p-name" placeholder="Full Name" class="w-full p-4 rounded-xl border-2 font-bold text-xs">
                        <input type="text" id="p-course" placeholder="Course" class="w-full p-4 rounded-xl border-2 font-bold text-xs">
                        <button onclick="saveProfile()" class="w-full py-4 bg-sky-600 text-white rounded-xl font-black text-xs uppercase">Save Profile</button>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <aside id="sidebar" class="hidden-sidebar m-2 flex flex-col glass shadow-2xl">
        <div class="p-6 bg-sky-800 text-white rounded-t-[1.3rem]">
            <h1 class="font-black italic tracking-tighter">Geo_Log System</h1>
            <p id="menu-user-id" class="text-[8px] opacity-70 uppercase font-bold tracking-widest"></p>
        </div>
        <nav id="nav-links" class="p-4 space-y-2 flex-1 text-xs font-black"></nav>
        <div class="p-4"><button onclick="logout()" class="w-full p-3 rounded-lg bg-red-50 text-red-600 font-black text-[10px] uppercase">Sign Out</button></div>
    </aside>

    <script>
        let role = 'student';

        const setRole = (r) => {
            role = r;
            document.getElementById('btn-student').className = `flex-1 py-2 rounded-lg text-[10px] font-black ${r === 'student' ? 'role-btn-active' : 'text-sky-400'}`;
            document.getElementById('btn-prof').className = `flex-1 py-2 rounded-lg text-[10px] font-black ${r === 'prof' ? 'role-btn-active' : 'text-sky-400'}`;
        };

        const attemptLogin = () => {
            const user = document.getElementById('login-user').value.trim();
            const pass = document.getElementById('login-pass').value.trim();
            if(!user || !pass) return;

            if(role === 'prof') {
                if(user === "PROF_Va-ay" && pass === "12345") { localStorage.setItem('geo_sess', 'PROFESSOR'); init(); }
                else alert("Admin access denied.");
            } else {
                let p = JSON.parse(localStorage.getItem('u_' + user));
                if(p) {
                    if(p.dob === pass) { localStorage.setItem('geo_sess', user); init(); }
                    else alert("Incorrect Password");
                } else {
                    const data = { name: "New Trainee", course: "WVSU OJT", dob: pass, id: user };
                    localStorage.setItem('u_' + user, JSON.stringify(data));
                    let reg = JSON.parse(localStorage.getItem('reg')) || [];
                    if(!reg.includes(user)) reg.push(user);
                    localStorage.setItem('reg', JSON.stringify(reg));
                    localStorage.setItem('geo_sess', user);
                    init();
                }
            }
        };

        const init = () => {
            const sess = localStorage.getItem('geo_sess');
            if(!sess) return;
            document.getElementById('login-screen').classList.add('hidden-login');
            document.getElementById('main-app').classList.remove('hidden');
            document.getElementById('menu-user-id').innerText = sess;
            
            const nav = document.getElementById('nav-links');
            if(sess === 'PROFESSOR') {
                nav.innerHTML = `<button onclick="showPage('directory-page')" class="w-full text-left p-3 rounded-lg bg-sky-50">👥 Master Registry</button>`;
                renderDir(); showPage('directory-page');
            } else {
                nav.innerHTML = `<button onclick="showPage('dash-page')" class="w-full text-left p-3 rounded-lg bg-sky-50">📊 Dashboard</button>
                                 <button onclick="showPage('calendar-page')" class="w-full text-left p-3 rounded-lg">📅 Calendar Verification</button>
                                 <button onclick="showPage('profile-page')" class="w-full text-left p-3 rounded-lg">⚙️ Profile Information</button>`;
                renderCalendar(); renderFullLogs(); showPage('dash-page');
            }
            loadProfile(sess);
        };

        const instantLog = (type) => {
            const id = localStorage.getItem('geo_sess');
            const logs = JSON.parse(localStorage.getItem('logs')) || [];
            const now = new Date();
            logs.unshift({ id, type, t: now.toLocaleTimeString(), d: now.toLocaleDateString(), raw: now.toISOString() });
            localStorage.setItem('logs', JSON.stringify(logs));
            renderDashboardLogs(); renderCalendar(); renderFullLogs();
        };

        const renderDashboardLogs = () => {
            const sess = localStorage.getItem('geo_sess');
            const logs = (JSON.parse(localStorage.getItem('logs')) || []).filter(l => l.id === sess).slice(0, 3);
            document.getElementById('log-preview').innerHTML = logs.map(l => `
                <div class="glass p-3 border-l-4 ${l.type==='IN'?'border-green-500':'border-red-500'} flex justify-between">
                    <p class="font-black text-[10px]">${l.d} — ${l.t}</p>
                    <span class="font-black text-[10px] ${l.type==='IN'?'text-green-600':'text-red-600'}">${l.type}</span>
                </div>`).join('');
        };

        const renderCalendar = () => {
            const sess = localStorage.getItem('geo_sess');
            const logs = (JSON.parse(localStorage.getItem('logs')) || []).filter(l => l.id === sess);
            const now = new Date();
            const year = now.getFullYear();
            const month = now.getMonth();
            document.getElementById('month-name').innerText = now.toLocaleString('default', { month: 'long', year: 'numeric' });
            const firstDay = new Date(year, month, 1).getDay();
            const daysInMonth = new Date(year, month + 1, 0).getDate();
            const calendarGrid = document.getElementById('calendar-days');
            calendarGrid.innerHTML = '';
            for (let i = 0; i < firstDay; i++) { calendarGrid.innerHTML += `<div></div>`; }
            for (let i = 1; i <= daysInMonth; i++) {
                const isToday = i === now.getDate();
                const hasLog = logs.some(l => {
                    const ld = new Date(l.raw);
                    return ld.getDate() === i && ld.getMonth() === month && ld.getFullYear() === year;
                });
                calendarGrid.innerHTML += `<div class="day-box ${hasLog ? 'day-active' : ''} ${isToday ? 'today' : ''}">${i}${hasLog ? '<div class="dot"></div>' : ''}</div>`;
            }
        };

        const renderFullLogs = () => {
            const sess = localStorage.getItem('geo_sess');
            const logs = (JSON.parse(localStorage.getItem('logs')) || []).filter(l => l.id === sess);
            document.getElementById('full-log-list').innerHTML = logs.map(l => `
                <div class="p-2 border-b flex justify-between text-[10px] font-bold">
                    <span>${l.d} — ${l.t}</span>
                    <span class="${l.type==='IN'?'text-green-600':'text-red-600'}">${l.type}</span>
                </div>`).join('') || '<p class="text-center text-[9px] py-4 opacity-40">No entries yet</p>';
        };

        const renderDir = () => {
            const reg = JSON.parse(localStorage.getItem('reg')) || [];
            const query = (document.getElementById('dir-search')?.value || '').toLowerCase();
            const list = document.getElementById('student-list');
            list.innerHTML = '';
            reg.filter(id => {
                const p = JSON.parse(localStorage.getItem('u_' + id)) || {};
                return id.toLowerCase().includes(query) || (p.name || '').toLowerCase().includes(query);
            }).forEach(id => {
                const p = JSON.parse(localStorage.getItem('u_' + id)) || {};
                list.innerHTML += `<div onclick="viewStudentDetail('${id}')" class="glass p-3 shadow-sm active:bg-sky-50 transition-colors cursor-pointer">
                        <p class="font-black text-xs text-sky-900">${p.name}</p>
                        <p class="text-[9px] text-sky-400 uppercase font-bold tracking-tight">ID: ${id} • ${p.course}</p></div>`;
            });
        };

        const viewStudentDetail = (id) => {
            const p = JSON.parse(localStorage.getItem('u_' + id)) || {};
            const logs = (JSON.parse(localStorage.getItem('logs')) || []).filter(l => l.id === id);
            document.getElementById('detail-header').innerHTML = `<h2 class="text-sm font-black text-sky-800 uppercase">${p.name}</h2><p class="text-[9px] font-bold text-sky-500 uppercase">ID: ${id} • ${p.course}</p>`;
            document.getElementById('detail-log-list').innerHTML = logs.map(l => `<div class="glass p-3 border-l-4 ${l.type==='IN'?'border-green-500':'border-red-500'} flex justify-between items-center"><span class="text-[9px] font-bold">${l.d} | ${l.t}</span><span class="font-black text-[9px] ${l.type==='IN'?'text-green-600':'text-red-600'}">${l.type}</span></div>`).join('') || '<p class="text-center text-[9px] opacity-50 py-4 font-bold uppercase">No records found</p>';
            showPage('student-detail-page');
        };

        const saveProfile = () => {
            const sess = localStorage.getItem('geo_sess');
            const p = JSON.parse(localStorage.getItem('u_' + sess));
            const data = { ...p, name: document.getElementById('p-name').value, course: document.getElementById('p-course').value };
            localStorage.setItem('u_' + sess, JSON.stringify(data));
            alert("Record updated successfully.");
            init();
        };

        const loadProfile = (id) => {
            if(id === 'PROFESSOR') return;
            const p = JSON.parse(localStorage.getItem('u_' + id)) || {};
            document.getElementById('p-id').value = id;
            document.getElementById('p-name').value = p.name || "";
            document.getElementById('p-course').value = p.course || "";
            document.getElementById('user-name-title').innerText = p.name || "Student";
            document.getElementById('user-course-title').innerText = p.course || "WVSU OJT";
            renderDashboardLogs();
        };

        const showPage = (id) => { 
            document.querySelectorAll('.page-content').forEach(p => p.classList.remove('page-active'));
            document.getElementById(id).classList.add('page-active'); toggleMenu(false);
        };

        const toggleMenu = (s) => document.getElementById('sidebar').classList.toggle('hidden-sidebar', !s);
        const logout = () => { localStorage.removeItem('geo_sess'); location.reload(); };
        setInterval(() => { document.getElementById('clock').innerText = new Date().toLocaleTimeString(); }, 1000);
        window.onload = init;
    </script>
</body>
</html>
