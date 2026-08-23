:root {
  --bg:        #0a0d12;
  --surface:   #121822;
  --surface-2: #182131;
  --border:    #232d3d;
  --text:      #c8d2e0;
  --heading:   #eef3fa;
  --muted:     #7b8798;
  --accent:    #e8a33d;
  --accent-dim:#8a6323;
  --mono: ui-monospace, "SF Mono", SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace;
  --sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}

* { box-sizing: border-box; }

html { -webkit-text-size-adjust: 100%; }

body {
  margin: 0;
  background: var(--bg);
  background-image:
    radial-gradient(ellipse 80% 50% at 50% -10%, rgba(232,163,61,.07), transparent 70%);
  background-repeat: no-repeat;
  color: var(--text);
  font-family: var(--sans);
  font-size: 16px;
  line-height: 1.65;
}

.wrap { width: 100%; max-width: 860px; margin: 0 auto; padding: 0 20px; }

/* --- шапка --- */
.site-header {
  border-bottom: 1px solid var(--border);
  background: rgba(10,13,18,.85);
  backdrop-filter: blur(8px);
  position: sticky; top: 0; z-index: 10;
}
.site-header .wrap {
  display: flex; align-items: center; justify-content: space-between;
  gap: 16px; flex-wrap: wrap; padding-top: 14px; padding-bottom: 14px;
}
.brand {
  font-family: var(--mono);
  font-size: 14px; letter-spacing: .08em; text-transform: uppercase;
  color: var(--heading); text-decoration: none; font-weight: 600;
}
.brand:hover { color: var(--accent); }
.site-nav { display: flex; gap: 20px; }
.site-nav a {
  font-family: var(--mono); font-size: 13px; color: var(--muted);
  text-decoration: none; letter-spacing: .04em;
}
.site-nav a:hover { color: var(--accent); }

/* --- страница --- */
.page { padding-top: 44px; padding-bottom: 72px; }

.page-title {
  font-family: var(--mono);
  font-size: 30px; line-height: 1.2; font-weight: 600;
  color: var(--heading); margin: 0 0 8px;
  letter-spacing: -.01em;
}
.page-desc { color: var(--muted); margin: 0 0 32px; font-size: 17px; }

h2, h3, h4 { color: var(--heading); font-family: var(--mono); font-weight: 600; line-height: 1.3; }
h2 {
  font-size: 22px; margin: 44px 0 14px;
  padding-bottom: 8px; border-bottom: 1px solid var(--border);
}
h3 { font-size: 17px; margin: 32px 0 10px; color: var(--accent); }
h4 { font-size: 15px; margin: 24px 0 8px; }

p { margin: 0 0 16px; }

a { color: var(--accent); text-decoration: none; border-bottom: 1px solid var(--accent-dim); }
a:hover { border-bottom-color: var(--accent); }

strong { color: var(--heading); }
em { color: var(--muted); }

hr { border: 0; border-top: 1px solid var(--border); margin: 40px 0; }

ul, ol { padding-left: 22px; }
li { margin-bottom: 8px; }
li::marker { color: var(--accent-dim); }

blockquote {
  margin: 20px 0; padding: 12px 18px;
  border-left: 3px solid var(--accent-dim);
  background: var(--surface); color: var(--muted);
}
blockquote p:last-child { margin-bottom: 0; }

code {
  font-family: var(--mono); font-size: .88em;
  background: var(--surface-2); color: var(--accent);
  padding: 2px 6px; border-radius: 4px;
}
pre {
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 8px; padding: 16px; overflow-x: auto;
}
pre code { background: none; color: var(--text); padding: 0; }

/* --- таблицы характеристик --- */
table {
  width: 100%; border-collapse: collapse;
  margin: 20px 0; font-size: 15px;
  background: var(--surface);
  border: 1px solid var(--border); border-radius: 8px;
  overflow: hidden;
}
th, td { padding: 9px 14px; text-align: left; border-bottom: 1px solid var(--border); }
tr:last-child td { border-bottom: 0; }
th { color: var(--muted); font-family: var(--mono); font-size: 13px; font-weight: 600; }
td:first-child { width: 38%; color: var(--muted); }
tbody tr:hover { background: var(--surface-2); }

/* --- карточки разделов --- */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
  gap: 16px;
  margin: 32px 0 8px;
}
.card {
  display: block; position: relative;
  padding: 22px 20px 20px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px;
  text-decoration: none; border-bottom: 1px solid var(--border);
  transition: border-color .15s, background .15s, transform .15s;
}
.card:hover {
  border-color: var(--accent-dim);
  background: var(--surface-2);
  transform: translateY(-2px);
}
.card-count {
  display: block;
  font-family: var(--mono); font-size: 28px; font-weight: 600;
  color: var(--accent); line-height: 1;
}
.card-name {
  display: block; margin: 10px 0 6px;
  font-family: var(--mono); font-size: 17px; font-weight: 600;
  color: var(--heading);
}
.card-desc { display: block; color: var(--muted); font-size: 14px; line-height: 1.5; }
.card-meta {
  display: block; margin-top: 14px;
  font-family: var(--mono); font-size: 12px; letter-spacing: .05em;
  text-transform: uppercase; color: var(--accent-dim);
}
.card:hover .card-meta { color: var(--accent); }

/* --- подвал --- */
.site-footer {
  border-top: 1px solid var(--border);
  padding: 24px 0;
  color: var(--muted);
  font-family: var(--mono); font-size: 12px; letter-spacing: .04em;
}

@media (max-width: 600px) {
  .page-title { font-size: 24px; }
  table { font-size: 14px; }
  th, td { padding: 8px 10px; }
  td:first-child { width: 45%; }
}
