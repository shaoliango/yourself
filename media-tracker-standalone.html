<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的影视库 - 个人追剧统计</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
/* 全局变量 */
:root {
    --bg-primary: #0f0f0f;
    --bg-secondary: #1a1a1a;
    --bg-card: #222222;
    --bg-hover: #2a2a2a;
    --text-primary: #ffffff;
    --text-secondary: #a0a0a0;
    --text-muted: #666666;
    --accent: #e50914;
    --accent-hover: #ff1a1a;
    --accent-gold: #ffd700;
    --accent-blue: #3b82f6;
    --accent-green: #22c55e;
    --accent-purple: #a855f7;
    --border: #333333;
    --shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
    --shadow-hover: 0 8px 30px rgba(0, 0, 0, 0.6);
    --radius: 12px;
    --radius-sm: 8px;
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
    font-family: 'Noto Sans SC', -apple-system, BlinkMacSystemFont, sans-serif;
    background: var(--bg-primary);
    color: var(--text-primary);
    min-height: 100vh;
    line-height: 1.6;
}

::-webkit-scrollbar { width: 8px; height: 8px; }
::-webkit-scrollbar-track { background: var(--bg-secondary); }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 4px; }
::-webkit-scrollbar-thumb:hover { background: var(--text-muted); }

.app-container { display: flex; flex-direction: column; min-height: 100vh; }

.navbar {
    position: fixed; top: 0; left: 0; right: 0; height: 64px;
    background: rgba(15, 15, 15, 0.95);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center;
    padding: 0 24px; z-index: 1000; gap: 32px;
}

.logo { display: flex; align-items: center; gap: 12px; font-size: 20px; font-weight: 700; }
.logo i { color: var(--accent); font-size: 24px; }

.nav-tabs { display: flex; gap: 8px; flex: 1; overflow-x: auto; }

.nav-tab {
    background: transparent; border: none;
    color: var(--text-secondary);
    padding: 10px 16px;
    border-radius: var(--radius-sm);
    cursor: pointer; font-size: 14px; font-weight: 500;
    display: flex; align-items: center; gap: 8px;
    transition: var(--transition); white-space: nowrap;
}
.nav-tab:hover { background: var(--bg-hover); color: var(--text-primary); }
.nav-tab.active { background: var(--accent); color: white; }

.nav-actions { display: flex; gap: 12px; }

.btn-search {
    width: 40px; height: 40px; border-radius: 50%;
    background: var(--bg-card); border: 1px solid var(--border);
    color: var(--text-primary); cursor: pointer;
    transition: var(--transition);
}
.btn-search:hover { background: var(--bg-hover); border-color: var(--text-muted); }

.btn-add {
    background: var(--accent); color: white; border: none;
    padding: 10px 20px; border-radius: var(--radius-sm);
    font-size: 14px; font-weight: 600; cursor: pointer;
    display: flex; align-items: center; gap: 8px;
    transition: var(--transition);
}
.btn-add:hover { background: var(--accent-hover); transform: translateY(-2px); }

.main-content { display: flex; margin-top: 64px; min-height: calc(100vh - 64px); }

.stats-panel {
    width: 280px; background: var(--bg-secondary);
    border-right: 1px solid var(--border);
    padding: 24px 16px;
    display: flex; flex-direction: column; gap: 20px;
    position: fixed; top: 64px; left: 0; bottom: 0;
    overflow-y: auto;
}

.stats-card {
    background: var(--bg-card); border-radius: var(--radius);
    padding: 20px; border: 1px solid var(--border);
}
.stats-card h3 {
    font-size: 14px; font-weight: 600;
    color: var(--text-secondary); margin-bottom: 16px;
    display: flex; align-items: center; gap: 8px;
}
.stats-card h3 i { color: var(--accent); }

.stat-item { text-align: center; padding: 12px; }
.stat-item.total {
    background: linear-gradient(135deg, var(--accent) 0%, #ff6b6b 100%);
    border-radius: var(--radius-sm); margin-bottom: 12px;
}
.stat-item.total .stat-value, .stat-item.total .stat-label { color: white; }
.stat-value { font-size: 32px; font-weight: 700; color: var(--text-primary); display: block; }
.stat-label { font-size: 12px; color: var(--text-secondary); margin-top: 4px; }
.stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
.stat-grid .stat-item { background: var(--bg-hover); border-radius: var(--radius-sm); padding: 16px 8px; }
.stat-grid .stat-value { font-size: 24px; }

.duration-display { display: flex; align-items: baseline; justify-content: center; gap: 8px; padding: 20px; }
.duration-value {
    font-size: 48px; font-weight: 700;
    background: linear-gradient(135deg, var(--accent-blue) 0%, var(--accent-purple) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.duration-unit { font-size: 16px; color: var(--text-secondary); }

.top-rated-list { display: flex; flex-direction: column; gap: 12px; max-height: 200px; overflow-y: auto; }
.top-rated-item { display: flex; align-items: center; gap: 12px; padding: 8px; border-radius: var(--radius-sm); cursor: pointer; transition: var(--transition); }
.top-rated-item:hover { background: var(--bg-hover); }
.top-rated-poster { width: 40px; height: 56px; border-radius: 4px; object-fit: cover; background: var(--bg-hover); }
.top-rated-info { flex: 1; min-width: 0; }
.top-rated-name { font-size: 13px; font-weight: 500; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.top-rated-rating { font-size: 12px; color: var(--accent-gold); display: flex; align-items: center; gap: 4px; }

.stats-card canvas { max-height: 150px; }

.content-area { flex: 1; margin-left: 280px; padding: 24px; }

.filter-bar {
    display: flex; justify-content: space-between; align-items: center;
    margin-bottom: 24px; padding: 16px 20px;
    background: var(--bg-card); border-radius: var(--radius);
    border: 1px solid var(--border); flex-wrap: wrap; gap: 12px;
}
.filter-group { display: flex; gap: 12px; flex-wrap: wrap; }

.filter-select {
    background: var(--bg-secondary); border: 1px solid var(--border);
    color: var(--text-primary); padding: 10px 16px;
    border-radius: var(--radius-sm); font-size: 14px;
    cursor: pointer; transition: var(--transition);
}
.filter-select:hover { border-color: var(--text-muted); }
.filter-select:focus { outline: none; border-color: var(--accent); }

.view-toggle { display: flex; gap: 4px; background: var(--bg-secondary); padding: 4px; border-radius: var(--radius-sm); }
.view-btn {
    width: 36px; height: 36px; border: none; background: transparent;
    color: var(--text-secondary); border-radius: 6px;
    cursor: pointer; transition: var(--transition);
}
.view-btn:hover { color: var(--text-primary); }
.view-btn.active { background: var(--accent); color: white; }

.media-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 24px; }

.media-card {
    background: var(--bg-card); border-radius: var(--radius);
    overflow: hidden; border: 1px solid var(--border);
    transition: var(--transition); cursor: pointer; position: relative;
    animation: fadeIn 0.4s ease forwards;
}
.media-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-hover); border-color: var(--text-muted); }
.media-card:hover .poster-overlay { opacity: 1; }

.media-poster { position: relative; aspect-ratio: 2/3; overflow: hidden; }
.media-poster img { width: 100%; height: 100%; object-fit: cover; transition: var(--transition); }
.media-card:hover .media-poster img { transform: scale(1.05); }

.poster-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, transparent 50%);
    opacity: 0; transition: var(--transition);
    display: flex; align-items: flex-end; padding: 16px;
}
.poster-actions { display: flex; gap: 8px; width: 100%; }
.poster-btn {
    flex: 1; padding: 10px; border: none;
    border-radius: var(--radius-sm); font-size: 12px;
    font-weight: 600; cursor: pointer; transition: var(--transition);
}
.poster-btn.edit { background: var(--accent-blue); color: white; }
.poster-btn.delete { background: var(--bg-hover); color: var(--text-primary); }
.poster-btn:hover { transform: scale(1.05); }

.status-badge {
    position: absolute; top: 12px; right: 12px;
    padding: 4px 10px; border-radius: 20px;
    font-size: 11px; font-weight: 600;
    backdrop-filter: blur(10px);
}
.status-badge.finished { background: rgba(34, 197, 94, 0.9); color: white; }
.status-badge.watching { background: rgba(59, 130, 246, 0.9); color: white; }
.status-badge.dropped { background: rgba(239, 68, 68, 0.9); color: white; }
.status-badge.pending { background: rgba(156, 163, 175, 0.9); color: white; }

.rating-badge {
    position: absolute; top: 12px; left: 12px;
    background: rgba(0, 0, 0, 0.75); backdrop-filter: blur(10px);
    padding: 4px 8px; border-radius: 6px;
    display: flex; align-items: center; gap: 4px;
    font-size: 12px; font-weight: 600;
}
.rating-badge i { color: var(--accent-gold); font-size: 10px; }

.progress-bar { position: absolute; bottom: 0; left: 0; right: 0; height: 3px; background: rgba(0, 0, 0, 0.5); }
.progress-fill { height: 100%; background: var(--accent); transition: width 0.3s ease; }

.media-info { padding: 16px; }
.media-title { font-size: 14px; font-weight: 600; color: var(--text-primary); margin-bottom: 8px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
.media-meta { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 8px; }
.media-meta span { font-size: 12px; color: var(--text-secondary); display: flex; align-items: center; gap: 4px; }
.media-tags { display: flex; flex-wrap: wrap; gap: 4px; }
.media-tag { background: var(--bg-hover); padding: 2px 8px; border-radius: 4px; font-size: 11px; color: var(--text-secondary); }

.empty-state { text-align: center; padding: 80px 20px; }
.empty-state i { font-size: 64px; color: var(--text-muted); margin-bottom: 24px; }
.empty-state p { font-size: 16px; color: var(--text-secondary); margin-bottom: 24px; }

.btn-primary {
    background: var(--accent); color: white; border: none;
    padding: 12px 24px; border-radius: var(--radius-sm);
    font-size: 14px; font-weight: 600; cursor: pointer;
    transition: var(--transition);
}
.btn-primary:hover { background: var(--accent-hover); }

.btn-secondary {
    background: var(--bg-hover); color: var(--text-primary);
    border: 1px solid var(--border);
    padding: 12px 24px; border-radius: var(--radius-sm);
    font-size: 14px; font-weight: 600; cursor: pointer;
    transition: var(--transition);
}
.btn-secondary:hover { background: var(--border); }

.modal-overlay {
    position: fixed; inset: 0;
    background: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(4px); z-index: 2000;
    display: none; align-items: center; justify-content: center; padding: 20px;
}
.modal-overlay.active { display: flex; }

.modal {
    background: var(--bg-card); border-radius: var(--radius);
    border: 1px solid var(--border);
    max-width: 600px; width: 100%; max-height: 90vh;
    overflow-y: auto; position: relative;
}

.modal-header {
    display: flex; align-items: center; justify-content: space-between;
    padding: 20px 24px; border-bottom: 1px solid var(--border);
    position: sticky; top: 0; background: var(--bg-card); z-index: 10;
}
.modal-header h2 { font-size: 18px; font-weight: 600; }
.modal-close {
    width: 36px; height: 36px; border-radius: 50%;
    background: var(--bg-hover); border: none;
    color: var(--text-primary); cursor: pointer;
    transition: var(--transition);
}
.modal-close:hover { background: var(--border); }

.modal-form { padding: 24px; }
.form-row { display: flex; gap: 16px; margin-bottom: 16px; flex-wrap: wrap; }
.form-group { flex: 1; min-width: 150px; }
.form-group.flex-2 { flex: 2; }
.form-group label { display: block; font-size: 13px; font-weight: 500; color: var(--text-secondary); margin-bottom: 8px; }
.form-group label .required { color: var(--accent); }
.form-group input, .form-group select, .form-group textarea {
    width: 100%; background: var(--bg-secondary);
    border: 1px solid var(--border); color: var(--text-primary);
    padding: 12px 14px; border-radius: var(--radius-sm);
    font-size: 14px; transition: var(--transition);
}
.form-group input:focus, .form-group select:focus, .form-group textarea:focus { outline: none; border-color: var(--accent); }
.form-group input::placeholder, .form-group textarea::placeholder { color: var(--text-muted); }
.form-group textarea { resize: vertical; min-height: 80px; }

.poster-preview { margin-top: 12px; border-radius: var(--radius-sm); overflow: hidden; display: none; }
.poster-preview.active { display: block; }
.poster-preview img { width: 100%; max-height: 200px; object-fit: cover; }

.tag-input-container {
    display: flex; flex-wrap: wrap; align-items: center;
    background: var(--bg-secondary); border: 1px solid var(--border);
    border-radius: var(--radius-sm); padding: 8px; gap: 8px; min-height: 44px;
}
.tags-wrapper { display: flex; flex-wrap: wrap; gap: 6px; }
.tag-chip {
    background: var(--accent); color: white;
    padding: 4px 10px; border-radius: 12px;
    font-size: 12px; display: flex; align-items: center; gap: 6px;
}
.tag-chip button { background: none; border: none; color: white; cursor: pointer; padding: 0; font-size: 14px; line-height: 1; }
.tag-input-container input { border: none; background: transparent; padding: 4px; flex: 1; min-width: 100px; }
.tag-input-container input:focus { outline: none; border: none; }

.rating-input { display: flex; align-items: center; gap: 8px; }
.rating-input input { width: 80px; }
.rating-max { color: var(--text-muted); font-size: 14px; }

.progress-input { display: flex; align-items: center; gap: 8px; }
.progress-input input { width: 60px; text-align: center; }
.progress-input span { color: var(--text-secondary); }

.form-actions { display: flex; gap: 12px; justify-content: flex-end; margin-top: 24px; padding-top: 24px; border-top: 1px solid var(--border); }

.detail-modal { max-width: 800px; }
.detail-content { display: flex; flex-direction: column; }
.detail-poster-section { display: flex; gap: 24px; padding: 24px; flex-wrap: wrap; }
.detail-poster { width: 200px; flex-shrink: 0; }
.detail-poster img { width: 100%; border-radius: var(--radius); box-shadow: var(--shadow); }
.detail-info { flex: 1; min-width: 250px; }
.detail-title { font-size: 24px; font-weight: 700; margin-bottom: 8px; }
.detail-meta-row { display: flex; flex-wrap: wrap; gap: 16px; margin-bottom: 16px; color: var(--text-secondary); font-size: 14px; }
.detail-rating { display: flex; align-items: center; gap: 6px; color: var(--accent-gold); font-weight: 600; }
.detail-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 16px; }
.detail-tag { background: var(--bg-hover); padding: 4px 12px; border-radius: 12px; font-size: 12px; color: var(--text-secondary); }
.detail-cast { font-size: 14px; color: var(--text-secondary); margin-bottom: 16px; }
.detail-synopsis { margin-top: 16px; }
.detail-synopsis h4 { font-size: 14px; color: var(--text-secondary); margin-bottom: 8px; }
.detail-synopsis p { font-size: 14px; line-height: 1.8; color: var(--text-primary); }

.detail-stats-section {
    background: var(--bg-secondary); padding: 20px 24px;
    display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 16px;
}
.detail-stat { text-align: center; }
.detail-stat-label { font-size: 12px; color: var(--text-muted); margin-bottom: 4px; }
.detail-stat-value { font-size: 18px; font-weight: 600; color: var(--text-primary); }

.detail-notes-section { padding: 24px; border-top: 1px solid var(--border); }
.detail-notes-section h4 { font-size: 14px; color: var(--text-secondary); margin-bottom: 12px; }
.detail-notes-section p { font-size: 14px; line-height: 1.8; color: var(--text-primary); white-space: pre-wrap; }

.search-overlay {
    position: fixed; inset: 0; background: rgba(0, 0, 0, 0.9);
    z-index: 3000; display: none; flex-direction: column; padding: 20px;
}
.search-overlay.active { display: flex; }
.search-box {
    display: flex; align-items: center; gap: 16px;
    background: var(--bg-card); border: 2px solid var(--border);
    border-radius: var(--radius); padding: 16px 24px;
    max-width: 600px; margin: 0 auto; width: 100%;
}
.search-box i { font-size: 20px; color: var(--text-muted); }
.search-box input { flex: 1; background: transparent; border: none; font-size: 18px; color: var(--text-primary); }
.search-box input:focus { outline: none; }
.search-close { background: none; border: none; color: var(--text-secondary); font-size: 20px; cursor: pointer; }
.search-results { max-width: 600px; margin: 20px auto 0; width: 100%; display: flex; flex-direction: column; gap: 12px; overflow-y: auto; }

.search-result-item {
    display: flex; gap: 16px; padding: 16px;
    background: var(--bg-card); border-radius: var(--radius);
    border: 1px solid var(--border); cursor: pointer;
    transition: var(--transition);
}
.search-result-item:hover { background: var(--bg-hover); }
.search-result-poster { width: 60px; height: 90px; border-radius: 6px; object-fit: cover; background: var(--bg-hover); }
.search-result-info { flex: 1; }
.search-result-title { font-weight: 600; margin-bottom: 4px; }
.search-result-meta { font-size: 13px; color: var(--text-secondary); }

/* 搜索结果优化 */
.search-hint { text-align: center; color: var(--text-muted); font-size: 13px; padding: 16px 12px; }
.search-result-item.active { background: var(--bg-hover); border-left: 3px solid var(--accent); }
.search-result-title mark { background: rgba(255, 209, 102, 0.4); color: inherit; border-radius: 3px; padding: 0 2px; }
.search-badge { display: inline-block; font-size: 11px; line-height: 1; color: var(--accent); background: var(--bg-hover); border: 1px solid var(--border); border-radius: 4px; padding: 2px 6px; margin-left: 8px; vertical-align: middle; }

.calendar-view {
    position: fixed; inset: 0; background: var(--bg-primary);
    z-index: 1500; display: none; flex-direction: column;
    padding: 24px; margin-left: 280px; margin-top: 64px;
}
.calendar-view.active { display: flex; }
.calendar-header { display: flex; align-items: center; justify-content: center; gap: 24px; margin-bottom: 24px; }
.calendar-header h3 { font-size: 20px; font-weight: 600; }
.cal-nav {
    width: 40px; height: 40px; border-radius: 50%;
    background: var(--bg-card); border: 1px solid var(--border);
    color: var(--text-primary); cursor: pointer;
    transition: var(--transition);
}
.cal-nav:hover { background: var(--bg-hover); }
.calendar-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 16px; flex: 1; }
.calendar-day {
    background: var(--bg-card); border-radius: var(--radius);
    border: 1px solid var(--border); padding: 16px;
    display: flex; flex-direction: column;
}
.calendar-day.today { border-color: var(--accent); }
.day-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 12px; }
.day-name { font-size: 12px; color: var(--text-muted); text-transform: uppercase; }
.day-date { font-size: 18px; font-weight: 600; }
.day-items { flex: 1; display: flex; flex-direction: column; gap: 8px; }
.day-item {
    background: var(--bg-hover); padding: 8px;
    border-radius: 6px; font-size: 12px;
    cursor: pointer; transition: var(--transition);
}
.day-item:hover { background: var(--border); }
.day-item.movie { border-left: 3px solid var(--accent); }
.day-item.tv { border-left: 3px solid var(--accent-blue); }
.day-item.anime { border-left: 3px solid var(--accent-purple); }

.media-grid.list-view { display: flex; flex-direction: column; gap: 12px; }
.media-card.list-style { display: flex; flex-direction: row; }
.media-card.list-style .media-poster { width: 120px; flex-shrink: 0; aspect-ratio: auto; height: 180px; }
.media-card.list-style .media-info { flex: 1; display: flex; flex-direction: column; justify-content: center; }

@keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
.media-card:nth-child(1) { animation-delay: 0s; }
.media-card:nth-child(2) { animation-delay: 0.05s; }
.media-card:nth-child(3) { animation-delay: 0.1s; }
.media-card:nth-child(4) { animation-delay: 0.15s; }
.media-card:nth-child(5) { animation-delay: 0.2s; }
.media-card:nth-child(6) { animation-delay: 0.25s; }

@media (max-width: 1200px) {
    .stats-panel { width: 240px; }
    .content-area, .calendar-view { margin-left: 240px; }
}

@media (max-width: 1024px) {
    .stats-panel { display: none; }
    .content-area, .calendar-view { margin-left: 0; }
}

@media (max-width: 768px) {
    .navbar { padding: 0 12px; gap: 12px; }
    .logo span, .nav-tab span, .btn-add span { display: none; }
    .media-grid { grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); gap: 12px; }
    .detail-poster { width: 150px; }
    .calendar-grid { grid-template-columns: 1fr; }
}
    </style>
</head>
<body>
    <div class="app-container">
        <header class="navbar">
            <div class="logo"><i class="fas fa-film"></i><span>我的影视库</span></div>
            <nav class="nav-tabs">
                <button class="nav-tab active" data-category="all"><i class="fas fa-home"></i> 全部</button>
                <button class="nav-tab" data-category="movie"><i class="fas fa-video"></i> 电影</button>
                <button class="nav-tab" data-category="tv"><i class="fas fa-tv"></i> 电视剧</button>
                <button class="nav-tab" data-category="anime"><i class="fas fa-dragon"></i> 动漫</button>
                <button class="nav-tab" data-filter="watched"><i class="fas fa-check-circle"></i> 已看</button>
                <button class="nav-tab" data-filter="watching"><i class="fas fa-play-circle"></i> 待看</button>
                <button class="nav-tab" data-view="calendar"><i class="fas fa-calendar-alt"></i> 追剧日历</button>
            </nav>
            <div class="nav-actions">
                <button class="btn-search" id="searchBtn"><i class="fas fa-search"></i></button>
                <button class="btn-add" id="addMediaBtn"><i class="fas fa-plus"></i> 添加影视</button>
            </div>
        </header>

        <main class="main-content">
            <aside class="stats-panel">
                <div class="stats-card">
                    <h3><i class="fas fa-chart-pie"></i> 观影统计</h3>
                    <div class="stat-item total">
                        <span class="stat-value" id="totalCount">0</span>
                        <span class="stat-label">已收录总数</span>
                    </div>
                    <div class="stat-grid">
                        <div class="stat-item"><span class="stat-value" id="movieCount">0</span><span class="stat-label">电影</span></div>
                        <div class="stat-item"><span class="stat-value" id="tvCount">0</span><span class="stat-label">电视剧</span></div>
                        <div class="stat-item"><span class="stat-value" id="animeCount">0</span><span class="stat-label">动漫</span></div>
                        <div class="stat-item"><span class="stat-value" id="watchedCount">0</span><span class="stat-label">已看完</span></div>
                    </div>
                </div>
                <div class="stats-card">
                    <h3><i class="fas fa-clock"></i> 观看时长</h3>
                    <div class="duration-display">
                        <span class="duration-value" id="totalDuration">0</span>
                        <span class="duration-unit">小时</span>
                    </div>
                </div>
                <div class="stats-card">
                    <h3><i class="fas fa-star"></i> 高分佳作</h3>
                    <div class="top-rated-list" id="topRatedList"></div>
                </div>
                <div class="stats-card">
                    <h3><i class="fas fa-chart-bar"></i> 月度数据</h3>
                    <canvas id="monthlyChart"></canvas>
                </div>
                <div class="stats-card">
                    <h3><i class="fas fa-calendar"></i> 分类统计</h3>
                    <canvas id="yearlyChart"></canvas>
                </div>
            </aside>

            <section class="content-area">
                <div class="filter-bar">
                    <div class="filter-group">
                        <select id="sortSelect" class="filter-select">
                            <option value="date-desc">最新添加</option>
                            <option value="date-asc">最早添加</option>
                            <option value="rating-desc">评分最高</option>
                            <option value="rating-asc">评分最低</option>
                            <option value="year-desc">年份最新</option>
                            <option value="year-asc">年份最早</option>
                            <option value="name-asc">名称 A-Z</option>
                        </select>
                        <select id="regionSelect" class="filter-select">
                            <option value="all">全部地区</option>
                            <option value="cn">国产</option>
                            <option value="foreign">海外</option>
                        </select>
                        <select id="statusSelect" class="filter-select">
                            <option value="all">全部状态</option>
                            <option value="finished">已看完</option>
                            <option value="watching">追更中</option>
                            <option value="dropped">弃剧</option>
                            <option value="pending">待看</option>
                        </select>
                    </div>
                    <div class="view-toggle">
                        <button class="view-btn active" data-view="grid"><i class="fas fa-th"></i></button>
                        <button class="view-btn" data-view="list"><i class="fas fa-list"></i></button>
                    </div>
                </div>
                <div class="media-grid" id="mediaGrid"></div>
                <div class="empty-state" id="emptyState" style="display: none;">
                    <i class="fas fa-film"></i>
                    <p>还没有收录任何影视作品</p>
                    <button class="btn-primary" id="emptyAddBtn">添加第一部</button>
                </div>
            </section>
        </main>
    </div>

    <!-- 添加/编辑弹窗 -->
    <div class="modal-overlay" id="modalOverlay">
        <div class="modal" id="mediaModal">
            <div class="modal-header">
                <h2 id="modalTitle">添加影视</h2>
                <button class="modal-close" id="modalClose"><i class="fas fa-times"></i></button>
            </div>
            <form class="modal-form" id="mediaForm">
                <input type="hidden" id="mediaId">
                <div class="form-row">
                    <div class="form-group flex-2">
                        <label>作品名称 <span class="required">*</span></label>
                        <input type="text" id="mediaName" required placeholder="输入影视名称">
                    </div>
                    <div class="form-group">
                        <label>分类 <span class="required">*</span></label>
                        <select id="mediaCategory" required>
                            <option value="">选择分类</option>
                            <option value="movie">电影</option>
                            <option value="tv">电视剧</option>
                            <option value="anime">动漫</option>
                        </select>
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>上映年份 <span class="required">*</span></label>
                        <input type="number" id="mediaYear" required min="1900" max="2030" placeholder="如：2024">
                    </div>
                    <div class="form-group">
                        <label>月份</label>
                        <select id="mediaMonth">
                            <option value="">选择月份</option>
                            <option value="1">1月</option><option value="2">2月</option><option value="3">3月</option>
                            <option value="4">4月</option><option value="5">5月</option><option value="6">6月</option>
                            <option value="7">7月</option><option value="8">8月</option><option value="9">9月</option>
                            <option value="10">10月</option><option value="11">11月</option><option value="12">12月</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>地区</label>
                        <select id="mediaRegion"><option value="cn">国产</option><option value="foreign">海外</option></select>
                    </div>
                </div>
                <div class="form-group">
                    <label>海报图片URL <span class="required">*</span></label>
                    <input type="url" id="mediaPoster" required placeholder="粘贴高清海报图片链接">
                    <div class="poster-preview" id="posterPreview"></div>
                </div>
                <div class="form-group">
                    <label>主演</label>
                    <input type="text" id="mediaCast" placeholder="用逗号分隔，如：张三, 李四">
                </div>
                <div class="form-group">
                    <label>剧情简介</label>
                    <textarea id="mediaSynopsis" rows="3" placeholder="输入作品简介..."></textarea>
                </div>
                <div class="form-group">
                    <label>类型标签</label>
                    <div class="tag-input-container">
                        <div class="tags-wrapper" id="tagsWrapper"></div>
                        <input type="text" id="tagInput" placeholder="输入标签后按回车">
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>观看状态</label>
                        <select id="mediaStatus">
                            <option value="pending">待看</option>
                            <option value="watching">追更中</option>
                            <option value="finished">已看完</option>
                            <option value="dropped">弃剧</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>评分</label>
                        <div class="rating-input">
                            <input type="number" id="mediaRating" min="0" max="10" step="0.5" placeholder="0-10">
                            <span class="rating-max">/ 10</span>
                        </div>
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>观看日期</label>
                        <input type="date" id="mediaWatchDate">
                    </div>
                    <div class="form-group">
                        <label>观看时长(小时)</label>
                        <input type="number" id="mediaDuration" min="0" step="0.5" placeholder="如：2.5">
                    </div>
                </div>
                <div class="form-row">
                    <div class="form-group">
                        <label>追剧进度</label>
                        <div class="progress-input">
                            <input type="number" id="mediaProgress" min="0" placeholder="已看">
                            <span>/</span>
                            <input type="number" id="mediaTotal" min="0" placeholder="全剧">
                            <span>集</span>
                        </div>
                    </div>
                    <div class="form-group">
                        <label>入坑时间</label>
                        <input type="date" id="mediaStartDate">
                    </div>
                </div>
                <div class="form-group">
                    <label>观后感</label>
                    <textarea id="mediaNotes" rows="4" placeholder="记录你的观影感受..."></textarea>
                </div>
                <div class="form-actions">
                    <button type="button" class="btn-secondary" id="cancelBtn">取消</button>
                    <button type="submit" class="btn-primary">保存</button>
                </div>
            </form>
        </div>
    </div>

    <!-- 详情弹窗 -->
    <div class="modal-overlay" id="detailOverlay">
        <div class="modal detail-modal" id="detailModal">
            <button class="modal-close" id="detailClose" style="position:absolute;top:16px;right:16px;"><i class="fas fa-times"></i></button>
            <div class="detail-content" id="detailContent"></div>
        </div>
    </div>

    <!-- 搜索弹窗 -->
    <div class="search-overlay" id="searchOverlay">
        <div class="search-box">
            <i class="fas fa-search"></i>
            <input type="text" id="searchInput" placeholder="搜索影视名称、演员...">
            <button class="search-close" id="searchClose"><i class="fas fa-times"></i></button>
        </div>
        <div class="search-results" id="searchResults"></div>
    </div>

    <!-- 日历视图 -->
    <div class="calendar-view" id="calendarView">
        <div class="calendar-header">
            <button class="cal-nav" id="prevWeek"><i class="fas fa-chevron-left"></i></button>
            <h3 id="calendarTitle">本周追剧</h3>
            <button class="cal-nav" id="nextWeek"><i class="fas fa-chevron-right"></i></button>
        </div>
        <div class="calendar-grid" id="calendarGrid"></div>
    </div>

    <script>
// 数据存储
let mediaData = JSON.parse(localStorage.getItem('mediaData')) || [];
let currentCategory = 'all';
let currentFilter = null;
let currentTags = [];
let calendarOffset = 0;
let searchResultsArr = [];
let searchCursor = 0;

// DOM 元素
const elements = {
    mediaGrid: document.getElementById('mediaGrid'),
    emptyState: document.getElementById('emptyState'),
    modalOverlay: document.getElementById('modalOverlay'),
    mediaForm: document.getElementById('mediaForm'),
    detailOverlay: document.getElementById('detailOverlay'),
    detailContent: document.getElementById('detailContent'),
    searchOverlay: document.getElementById('searchOverlay'),
    searchInput: document.getElementById('searchInput'),
    searchResults: document.getElementById('searchResults'),
    calendarView: document.getElementById('calendarView'),
    calendarGrid: document.getElementById('calendarGrid'),
    posterPreview: document.getElementById('posterPreview'),
    tagsWrapper: document.getElementById('tagsWrapper'),
    tagInput: document.getElementById('tagInput')
};

// 初始化
document.addEventListener('DOMContentLoaded', () => {
    initEventListeners();
    renderMedia();
    updateStats();
    initCharts();
});

// 事件监听
function initEventListeners() {
    document.querySelectorAll('.nav-tab').forEach(tab => tab.addEventListener('click', () => handleNavTab(tab)));
    document.getElementById('addMediaBtn').addEventListener('click', openAddModal);
    document.getElementById('emptyAddBtn')?.addEventListener('click', openAddModal);
    document.getElementById('modalClose').addEventListener('click', closeModal);
    document.getElementById('cancelBtn').addEventListener('click', closeModal);
    document.getElementById('detailClose').addEventListener('click', closeDetail);
    elements.mediaForm.addEventListener('submit', handleFormSubmit);
    document.getElementById('mediaPoster').addEventListener('input', handlePosterInput);
    elements.tagInput.addEventListener('keydown', handleTagInput);
    document.getElementById('sortSelect').addEventListener('change', renderMedia);
    document.getElementById('regionSelect').addEventListener('change', renderMedia);
    document.getElementById('statusSelect').addEventListener('change', renderMedia);
    document.querySelectorAll('.view-btn').forEach(btn => btn.addEventListener('click', () => handleViewToggle(btn)));
    document.getElementById('searchBtn').addEventListener('click', openSearch);
    document.getElementById('searchClose').addEventListener('click', closeSearch);
    elements.searchInput.addEventListener('input', handleSearch);
    elements.searchInput.addEventListener('keydown', handleSearchKeydown);
    document.getElementById('prevWeek').addEventListener('click', () => { calendarOffset--; renderCalendar(); });
    document.getElementById('nextWeek').addEventListener('click', () => { calendarOffset++; renderCalendar(); });
    elements.modalOverlay.addEventListener('click', (e) => { if (e.target === elements.modalOverlay) closeModal(); });
    elements.detailOverlay.addEventListener('click', (e) => { if (e.target === elements.detailOverlay) closeDetail(); });
    elements.searchOverlay.addEventListener('click', (e) => { if (e.target === elements.searchOverlay) closeSearch(); });
    document.addEventListener('keydown', (e) => { if (e.key === 'Escape') { closeModal(); closeDetail(); closeSearch(); } });
}

function handleNavTab(tab) {
    document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
    tab.classList.add('active');
    const category = tab.dataset.category;
    const filter = tab.dataset.filter;
    const view = tab.dataset.view;
    if (view === 'calendar') { elements.calendarView.classList.add('active'); renderCalendar(); }
    else { elements.calendarView.classList.remove('active'); currentCategory = category || 'all'; currentFilter = filter || null; renderMedia(); }
}

function openAddModal() {
    document.getElementById('modalTitle').textContent = '添加影视';
    elements.mediaForm.reset();
    document.getElementById('mediaId').value = '';
    currentTags = [];
    renderTags();
    elements.posterPreview.classList.remove('active');
    elements.posterPreview.innerHTML = '';
    elements.modalOverlay.classList.add('active');
}

function openEditModal(id) {
    const media = mediaData.find(m => m.id === id);
    if (!media) return;
    document.getElementById('modalTitle').textContent = '编辑影视';
    document.getElementById('mediaId').value = media.id;
    document.getElementById('mediaName').value = media.name;
    document.getElementById('mediaCategory').value = media.category;
    document.getElementById('mediaYear').value = media.year;
    document.getElementById('mediaMonth').value = media.month || '';
    document.getElementById('mediaRegion').value = media.region || 'cn';
    document.getElementById('mediaPoster').value = media.poster;
    document.getElementById('mediaCast').value = media.cast || '';
    document.getElementById('mediaSynopsis').value = media.synopsis || '';
    document.getElementById('mediaStatus').value = media.status;
    document.getElementById('mediaRating').value = media.rating || '';
    document.getElementById('mediaWatchDate').value = media.watchDate || '';
    document.getElementById('mediaDuration').value = media.duration || '';
    document.getElementById('mediaProgress').value = media.progress || '';
    document.getElementById('mediaTotal').value = media.total || '';
    document.getElementById('mediaStartDate').value = media.startDate || '';
    document.getElementById('mediaNotes').value = media.notes || '';
    currentTags = media.tags || [];
    renderTags();
    if (media.poster) { elements.posterPreview.innerHTML = `<img src="${media.poster}" alt="预览">`; elements.posterPreview.classList.add('active'); }
    elements.modalOverlay.classList.add('active');
}

function closeModal() { elements.modalOverlay.classList.remove('active'); }

function openDetail(id) {
    const media = mediaData.find(m => m.id === id);
    if (!media) return;
    const categoryNames = { movie: '电影', tv: '电视剧', anime: '动漫' };
    const statusNames = { finished: '已看完', watching: '追更中', dropped: '弃剧', pending: '待看' };
    const regionNames = { cn: '国产', foreign: '海外' };
    const progressText = media.progress && media.total ? `${media.progress}/${media.total}集` : '-';
    elements.detailContent.innerHTML = `
        <div class="detail-poster-section">
            <div class="detail-poster"><img src="${media.poster}" alt="${media.name}"></div>
            <div class="detail-info">
                <h2 class="detail-title">${media.name}</h2>
                <div class="detail-meta-row">
                    <span>${categoryNames[media.category]}</span>
                    <span>${media.year}年${media.month ? media.month + '月' : ''}</span>
                    <span>${regionNames[media.region || 'cn']}</span>
                    ${media.rating ? `<span class="detail-rating"><i class="fas fa-star"></i> ${media.rating}</span>` : ''}
                </div>
                <div class="detail-tags">
                    <span class="detail-tag">${statusNames[media.status]}</span>
                    ${media.tags?.map(tag => `<span class="detail-tag">${tag}</span>`).join('') || ''}
                </div>
                ${media.cast ? `<div class="detail-cast"><strong>主演：</strong>${media.cast}</div>` : ''}
                ${media.synopsis ? `<div class="detail-synopsis"><h4>剧情简介</h4><p>${media.synopsis}</p></div>` : ''}
            </div>
        </div>
        <div class="detail-stats-section">
            <div class="detail-stat"><div class="detail-stat-label">观看日期</div><div class="detail-stat-value">${media.watchDate || '-'}</div></div>
            <div class="detail-stat"><div class="detail-stat-label">观看时长</div><div class="detail-stat-value">${media.duration ? media.duration + '小时' : '-'}</div></div>
            <div class="detail-stat"><div class="detail-stat-label">追剧进度</div><div class="detail-stat-value">${progressText}</div></div>
            <div class="detail-stat"><div class="detail-stat-label">入坑时间</div><div class="detail-stat-value">${media.startDate || '-'}</div></div>
        </div>
        ${media.notes ? `<div class="detail-notes-section"><h4><i class="fas fa-comment"></i> 观后感</h4><p>${media.notes}</p></div>` : ''}
    `;
    elements.detailOverlay.classList.add('active');
}

function closeDetail() { elements.detailOverlay.classList.remove('active'); }

function handleFormSubmit(e) {
    e.preventDefault();
    const id = document.getElementById('mediaId').value || generateId();
    const isEdit = !!document.getElementById('mediaId').value;
    const media = {
        id, name: document.getElementById('mediaName').value, category: document.getElementById('mediaCategory').value,
        year: parseInt(document.getElementById('mediaYear').value), month: document.getElementById('mediaMonth').value ? parseInt(document.getElementById('mediaMonth').value) : null,
        region: document.getElementById('mediaRegion').value, poster: document.getElementById('mediaPoster').value,
        cast: document.getElementById('mediaCast').value, synopsis: document.getElementById('mediaSynopsis').value,
        tags: currentTags, status: document.getElementById('mediaStatus').value,
        rating: document.getElementById('mediaRating').value ? parseFloat(document.getElementById('mediaRating').value) : null,
        watchDate: document.getElementById('mediaWatchDate').value,
        duration: document.getElementById('mediaDuration').value ? parseFloat(document.getElementById('mediaDuration').value) : null,
        progress: document.getElementById('mediaProgress').value ? parseInt(document.getElementById('mediaProgress').value) : null,
        total: document.getElementById('mediaTotal').value ? parseInt(document.getElementById('mediaTotal').value) : null,
        startDate: document.getElementById('mediaStartDate').value, notes: document.getElementById('mediaNotes').value,
        createdAt: isEdit ? mediaData.find(m => m.id === id)?.createdAt : new Date().toISOString(),
        updatedAt: new Date().toISOString()
    };
    if (isEdit) { const index = mediaData.findIndex(m => m.id === id); mediaData[index] = media; }
    else { mediaData.push(media); }
    saveData(); closeModal(); renderMedia(); updateStats(); updateCharts();
}

function deleteMedia(id) {
    if (!confirm('确定要删除这部影视吗？')) return;
    mediaData = mediaData.filter(m => m.id !== id);
    saveData(); renderMedia(); updateStats(); updateCharts();
}

function renderMedia() {
    let filtered = [...mediaData];
    if (currentCategory !== 'all') filtered = filtered.filter(m => m.category === currentCategory);
    if (currentFilter) {
        if (currentFilter === 'watched') filtered = filtered.filter(m => m.status === 'finished');
        else if (currentFilter === 'watching') filtered = filtered.filter(m => m.status === 'watching' || m.status === 'pending');
    }
    const region = document.getElementById('regionSelect').value;
    if (region !== 'all') filtered = filtered.filter(m => m.region === region);
    const status = document.getElementById('statusSelect').value;
    if (status !== 'all') filtered = filtered.filter(m => m.status === status);
    const sort = document.getElementById('sortSelect').value;
    filtered.sort((a, b) => {
        switch (sort) {
            case 'date-desc': return new Date(b.createdAt) - new Date(a.createdAt);
            case 'date-asc': return new Date(a.createdAt) - new Date(b.createdAt);
            case 'rating-desc': return (b.rating || 0) - (a.rating || 0);
            case 'rating-asc': return (a.rating || 0) - (b.rating || 0);
            case 'year-desc': return b.year - a.year;
            case 'year-asc': return a.year - b.year;
            case 'name-asc': return a.name.localeCompare(b.name, 'zh-CN');
            default: return 0;
        }
    });
    if (filtered.length === 0) { elements.mediaGrid.innerHTML = ''; elements.emptyState.style.display = 'block'; return; }
    elements.emptyState.style.display = 'none';
    elements.mediaGrid.innerHTML = filtered.map(media => createMediaCard(media)).join('');
    elements.mediaGrid.querySelectorAll('.media-card').forEach(card => {
        const id = card.dataset.id;
        card.addEventListener('click', (e) => { if (!e.target.closest('.poster-actions')) openDetail(id); });
        card.querySelector('.poster-btn.edit')?.addEventListener('click', (e) => { e.stopPropagation(); openEditModal(id); });
        card.querySelector('.poster-btn.delete')?.addEventListener('click', (e) => { e.stopPropagation(); deleteMedia(id); });
    });
}

function createMediaCard(media) {
    const statusNames = { finished: '已看完', watching: '追更中', dropped: '弃剧', pending: '待看' };
    const categoryIcons = { movie: 'fa-video', tv: 'fa-tv', anime: 'fa-dragon' };
    const progressPercent = media.progress && media.total ? (media.progress / media.total * 100) : 0;
    return `
        <div class="media-card" data-id="${media.id}">
            <div class="media-poster">
                <img src="${media.poster}" alt="${media.name}" loading="lazy">
                <span class="status-badge ${media.status}">${statusNames[media.status]}</span>
                ${media.rating ? `<span class="rating-badge"><i class="fas fa-star"></i>${media.rating}</span>` : ''}
                ${progressPercent > 0 ? `<div class="progress-bar"><div class="progress-fill" style="width: ${progressPercent}%"></div></div>` : ''}
                <div class="poster-overlay"><div class="poster-actions">
                    <button class="poster-btn edit"><i class="fas fa-edit"></i> 编辑</button>
                    <button class="poster-btn delete"><i class="fas fa-trash"></i></button>
                </div></div>
            </div>
            <div class="media-info">
                <h3 class="media-title">${media.name}</h3>
                <div class="media-meta">
                    <span><i class="fas ${categoryIcons[media.category]}"></i></span>
                    <span>${media.year}</span>
                    ${media.duration ? `<span>${media.duration}h</span>` : ''}
                </div>
                ${media.tags?.length > 0 ? `<div class="media-tags">${media.tags.slice(0, 2).map(tag => `<span class="media-tag">${tag}</span>`).join('')}</div>` : ''}
            </div>
        </div>`;
}

function updateStats() {
    document.getElementById('totalCount').textContent = mediaData.length;
    document.getElementById('movieCount').textContent = mediaData.filter(m => m.category === 'movie').length;
    document.getElementById('tvCount').textContent = mediaData.filter(m => m.category === 'tv').length;
    document.getElementById('animeCount').textContent = mediaData.filter(m => m.category === 'anime').length;
    document.getElementById('watchedCount').textContent = mediaData.filter(m => m.status === 'finished').length;
    document.getElementById('totalDuration').textContent = mediaData.reduce((sum, m) => sum + (m.duration || 0), 0).toFixed(1);
    const topRated = mediaData.filter(m => m.rating >= 8).sort((a, b) => b.rating - a.rating).slice(0, 5);
    document.getElementById('topRatedList').innerHTML = topRated.length > 0 
        ? topRated.map(m => `<div class="top-rated-item" data-id="${m.id}"><img class="top-rated-poster" src="${m.poster}" alt="${m.name}"><div class="top-rated-info"><div class="top-rated-name">${m.name}</div><div class="top-rated-rating"><i class="fas fa-star"></i> ${m.rating}</div></div></div>`).join('')
        : '<p style="text-align:center;color:var(--text-muted);font-size:12px;">暂无高分作品</p>';
    document.querySelectorAll('.top-rated-item').forEach(item => item.addEventListener('click', () => openDetail(item.dataset.id)));
}

let monthlyChart, yearlyChart;
function initCharts() {
    const chartOptions = { responsive: true, maintainAspectRatio: true, plugins: { legend: { display: false } }, scales: { x: { grid: { color: 'rgba(255,255,255,0.1)' }, ticks: { color: '#a0a0a0', font: { size: 10 } } }, y: { grid: { color: 'rgba(255,255,255,0.1)' }, ticks: { color: '#a0a0a0', font: { size: 10 } } } } };
    monthlyChart = new Chart(document.getElementById('monthlyChart'), { type: 'bar', data: { labels: [], datasets: [{ data: [], backgroundColor: 'rgba(229, 9, 20, 0.8)', borderRadius: 4 }] }, options: chartOptions });
    yearlyChart = new Chart(document.getElementById('yearlyChart'), { type: 'doughnut', data: { labels: ['电影', '电视剧', '动漫'], datasets: [{ data: [0, 0, 0], backgroundColor: ['rgba(229, 9, 20, 0.8)', 'rgba(59, 130, 246, 0.8)', 'rgba(168, 85, 247, 0.8)'] }] }, options: { responsive: true, maintainAspectRatio: true, plugins: { legend: { position: 'bottom', labels: { color: '#a0a0a0', font: { size: 10 }, padding: 8 } } } } });
    updateCharts();
}

function updateCharts() {
    const monthlyData = {};
    mediaData.forEach(m => { if (m.watchDate) { const month = m.watchDate.substring(0, 7); monthlyData[month] = (monthlyData[month] || 0) + 1; } });
    const sortedMonths = Object.keys(monthlyData).sort().slice(-6);
    monthlyChart.data.labels = sortedMonths.map(m => m.replace('-', '年') + '月');
    monthlyChart.data.datasets[0].data = sortedMonths.map(m => monthlyData[m]);
    monthlyChart.update();
    yearlyChart.data.datasets[0].data = [mediaData.filter(m => m.category === 'movie').length, mediaData.filter(m => m.category === 'tv').length, mediaData.filter(m => m.category === 'anime').length];
    yearlyChart.update();
}

function handlePosterInput(e) {
    const url = e.target.value;
    if (url) { elements.posterPreview.innerHTML = `<img src="${url}" alt="预览" onerror="this.parentElement.innerHTML='图片加载失败'">`; elements.posterPreview.classList.add('active'); }
    else { elements.posterPreview.classList.remove('active'); elements.posterPreview.innerHTML = ''; }
}

function handleTagInput(e) {
    if (e.key === 'Enter') { e.preventDefault(); const tag = e.target.value.trim(); if (tag && !currentTags.includes(tag)) { currentTags.push(tag); renderTags(); } e.target.value = ''; }
}

function renderTags() { elements.tagsWrapper.innerHTML = currentTags.map((tag, i) => `<span class="tag-chip">${tag}<button type="button" onclick="removeTag(${i})">×</button></span>`).join(''); }
function removeTag(index) { currentTags.splice(index, 1); renderTags(); }

function handleViewToggle(btn) {
    document.querySelectorAll('.view-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    if (btn.dataset.view === 'list') elements.mediaGrid.classList.add('list-view');
    else elements.mediaGrid.classList.remove('list-view');
}

function openSearch() { elements.searchOverlay.classList.add('active'); elements.searchInput.value = ''; elements.searchResults.innerHTML = '<p class="search-hint">输入名称、演员、类型或剧情关键词开始搜索</p>'; searchResultsArr = []; searchCursor = 0; elements.searchInput.focus(); }
function closeSearch() { elements.searchOverlay.classList.remove('active'); elements.searchInput.value = ''; elements.searchResults.innerHTML = ''; searchResultsArr = []; searchCursor = 0; }

function handleSearch(e) {
    const query = e.target.value.toLowerCase().trim();
    if (!query) { elements.searchResults.innerHTML = '<p class="search-hint">输入名称、演员、类型或剧情关键词开始搜索</p>'; searchResultsArr = []; searchCursor = 0; return; }
    const tokens = query.split(/\s+/).filter(Boolean);
    const catNames = { movie: '电影', tv: '电视剧', anime: '动漫' };
    const regNames = { cn: '国产', foreign: '海外' };

    const compact = s => (s == null ? '' : String(s)).toLowerCase().replace(/\s+/g, '');
    const normTags = t => Array.isArray(t) ? t : (typeof t === 'string' ? (() => { try { const p = JSON.parse(t); return Array.isArray(p) ? p : [t]; } catch { return [t]; } })() : []);
    const FIELD_WEIGHT = { name: 100, cast: 60, tags: 40, synopsis: 25, notes: 15, category: 18, region: 18 };
    const FIELD_LABEL = { name: '', cast: '主演', tags: '类型', synopsis: '剧情', notes: '笔记', category: '分类', region: '地区' };

    const results = [];
    for (const m of mediaData) {
        const fields = {
            name: compact(m.name),
            cast: compact(m.cast),
            tags: compact(normTags(m.tags).join(' ')),
            synopsis: compact(m.synopsis),
            notes: compact(m.notes),
            category: compact(catNames[m.category] || ''),
            region: compact(regNames[m.region] || regNames.cn)
        };
        let score = 0; const matched = new Set(); let ok = true;
        for (const tok of tokens) {
            const tokC = tok.replace(/\s+/g, '');
            let best = 0, bestField = null;
            for (const f in fields) {
                if (fields[f].includes(tokC)) { if (FIELD_WEIGHT[f] > best) { best = FIELD_WEIGHT[f]; bestField = f; } }
            }
            if (!bestField) { ok = false; break; }
            score += best; matched.add(bestField);
        }
        if (!ok) continue;
        let primary = null, primaryW = -1;
        for (const f of matched) { if (FIELD_WEIGHT[f] > primaryW) { primaryW = FIELD_WEIGHT[f]; primary = f; } }
        results.push({ media: m, score, primaryField: primary });
    }

    results.sort((a, b) => b.score - a.score || (b.media.rating || 0) - (a.media.rating || 0) || (a.media.name || '').localeCompare(b.media.name || '', 'zh'));
    searchResultsArr = results;
    searchCursor = 0;

    const esc = s => (s || '').replace(/[&<>"']/g, c => ({ '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;' }[c]));
    const highlight = (text, toks) => {
        let html = esc(text);
        for (const t of toks) { const lit = t.trim(); if (!lit) continue; html = html.replace(new RegExp('(' + lit.replace(/[.*+?^${}()|[\]\\]/g, '\\$&') + ')', 'gi'), '<mark>$1</mark>'); }
        return html;
    };

    if (results.length === 0) { elements.searchResults.innerHTML = '<p class="search-hint">未找到相关影视，换个关键词试试</p>'; return; }
    elements.searchResults.innerHTML = results.map(r => {
        const m = r.media;
        const badge = FIELD_LABEL[r.primaryField] ? `<span class="search-badge">${FIELD_LABEL[r.primaryField]}</span>` : '';
        return `<div class="search-result-item" data-id="${esc(m.id)}"><img class="search-result-poster" src="${esc(m.poster)}" alt="${esc(m.name)}" onerror="this.style.visibility='hidden'"><div class="search-result-info"><div class="search-result-title">${highlight(m.name, tokens)}${badge}</div><div class="search-result-meta">${catNames[m.category]} · ${m.year}年</div></div></div>`;
    }).join('');
    elements.searchResults.querySelectorAll('.search-result-item').forEach(item => item.addEventListener('click', () => { openDetail(item.dataset.id); closeSearch(); }));
}

function handleSearchKeydown(e) {
    const items = elements.searchResults.querySelectorAll('.search-result-item');
    if (items.length === 0) return;
    if (e.key === 'ArrowDown') { e.preventDefault(); searchCursor = Math.min(searchCursor + 1, items.length - 1); highlightSearchCursor(); }
    else if (e.key === 'ArrowUp') { e.preventDefault(); searchCursor = Math.max(searchCursor - 1, 0); highlightSearchCursor(); }
    else if (e.key === 'Enter') { e.preventDefault(); const item = items[searchCursor]; if (item) { openDetail(item.dataset.id); closeSearch(); } }
}

function highlightSearchCursor() {
    const items = elements.searchResults.querySelectorAll('.search-result-item');
    items.forEach((it, i) => it.classList.toggle('active', i === searchCursor));
    items[searchCursor] && items[searchCursor].scrollIntoView({ block: 'nearest' });
}

function renderCalendar() {
    const today = new Date();
    const startOfWeek = new Date(today);
    startOfWeek.setDate(today.getDate() - today.getDay() + calendarOffset * 7);
    const days = ['周日', '周一', '周二', '周三', '周四', '周五', '周六'];
    const monthNames = ['1月', '2月', '3月', '4月', '5月', '6月', '7月', '8月', '9月', '10月', '11月', '12月'];
    const endOfWeek = new Date(startOfWeek); endOfWeek.setDate(startOfWeek.getDate() + 6);
    document.getElementById('calendarTitle').textContent = `${startOfWeek.getFullYear()}年 ${monthNames[startOfWeek.getMonth()]} ${startOfWeek.getDate()}日 - ${monthNames[endOfWeek.getMonth()]} ${endOfWeek.getDate()}日`;
    let html = '';
    for (let i = 0; i < 7; i++) {
        const date = new Date(startOfWeek); date.setDate(startOfWeek.getDate() + i);
        const dateStr = date.toISOString().split('T')[0];
        const isToday = dateStr === today.toISOString().split('T')[0];
        const dayMedia = mediaData.filter(m => m.watchDate === dateStr);
        html += `<div class="calendar-day ${isToday ? 'today' : ''}"><div class="day-header"><span class="day-name">${days[i]}</span><span class="day-date">${date.getDate()}</span></div><div class="day-items">${dayMedia.map(m => `<div class="day-item ${m.category}" data-id="${m.id}">${m.name}</div>`).join('')}</div></div>`;
    }
    elements.calendarGrid.innerHTML = html;
    elements.calendarGrid.querySelectorAll('.day-item').forEach(item => item.addEventListener('click', () => openDetail(item.dataset.id)));
}

function generateId() { return 'media_' + Date.now() + '_' + Math.random().toString(36).substr(2, 9); }
function saveData() { localStorage.setItem('mediaData', JSON.stringify(mediaData)); }
    </script>
</body>
</html>
