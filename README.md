[NE_수능독해_AI_문제은행_v2.html](https://github.com/user-attachments/files/28143140/NE_._AI_._v2.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NE능률 수능독해 AI 문제은행</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&family=IBM+Plex+Mono:wght@400;500&display=swap');
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --c0:#0a0a0f;--c1:#111118;--c2:#1a1a24;--c3:#22222e;--c4:#2e2e3e;
  --c5:#3a3a50;--c6:#5a5a7a;--c7:#8888aa;--c8:#aaaacc;--c9:#e8e8f8;
  --accent:#4f7fff;--accent2:#7c4fff;--teal:#1ecb8a;--amber:#f5a623;
  --red:#ff4f6a;--green:#3eca6e;
  --border:rgba(255,255,255,0.07);--border2:rgba(255,255,255,0.12);
  --r:8px;--rl:12px;--rxl:16px
}
html{font-size:14px}
body{font-family:'Noto Sans KR',sans-serif;background:var(--c0);color:var(--c9);line-height:1.6;min-height:100vh;overflow-x:hidden}

/* ─── SCROLLBAR ─── */
::-webkit-scrollbar{width:4px;height:4px}
::-webkit-scrollbar-track{background:var(--c1)}
::-webkit-scrollbar-thumb{background:var(--c5);border-radius:2px}

/* ─── PILLS ─── */
.pill{display:inline-flex;align-items:center;gap:3px;font-size:11px;font-weight:500;padding:2px 9px;border-radius:20px;white-space:nowrap}
.pill-blue{background:rgba(79,127,255,.18);color:#7aaeff;border:0.5px solid rgba(79,127,255,.35)}
.pill-teal{background:rgba(30,203,138,.15);color:#4edda8;border:0.5px solid rgba(30,203,138,.3)}
.pill-amber{background:rgba(245,166,35,.15);color:#f9c060;border:0.5px solid rgba(245,166,35,.3)}
.pill-red{background:rgba(255,79,106,.15);color:#ff7a90;border:0.5px solid rgba(255,79,106,.3)}
.pill-gray{background:var(--c3);color:var(--c7);border:0.5px solid var(--border2)}
.pill-purple{background:rgba(124,79,255,.15);color:#aa80ff;border:0.5px solid rgba(124,79,255,.3)}

/* ─── NAV ─── */
.nav{position:sticky;top:0;z-index:200;background:rgba(10,10,15,.92);backdrop-filter:blur(12px);border-bottom:0.5px solid var(--border);display:flex;align-items:center;padding:0 20px;height:52px;gap:0}
.logo{font-family:'IBM Plex Mono',monospace;font-size:13px;font-weight:500;color:var(--accent);margin-right:24px;letter-spacing:.02em;white-space:nowrap;cursor:pointer;user-select:none}
.logo em{color:var(--c9);font-style:normal}
.ntabs{display:flex;gap:2px;flex:1}
.ntab{padding:6px 14px;border-radius:var(--r);font-size:13px;color:var(--c7);cursor:pointer;border:none;background:none;transition:all .15s;white-space:nowrap;font-family:inherit}
.ntab:hover{background:var(--c3);color:var(--c9)}
.ntab.on{background:var(--c3);color:var(--c9);font-weight:500}
.nav-r{display:flex;align-items:center;gap:8px;margin-left:auto}

/* ─── PAGES ─── */
.page{display:none;padding:20px;max-width:1200px;margin:0 auto}
.page.on{display:block}

/* ─── LAYOUT ─── */
.layout-3{display:grid;grid-template-columns:210px 1fr 280px;gap:12px;align-items:start}
.side-col{display:flex;flex-direction:column;gap:10px}
.main-col{display:flex;flex-direction:column;gap:12px;min-width:0}

/* ─── CARDS ─── */
.card{background:var(--c1);border:0.5px solid var(--border);border-radius:var(--rl);padding:14px 16px}
.card-dark{background:var(--c2);border:0.5px solid var(--border)}
.ch{font-size:10px;font-weight:500;letter-spacing:.08em;text-transform:uppercase;color:var(--c6);margin-bottom:9px;font-family:'IBM Plex Mono',monospace}

/* ─── BUTTONS ─── */
.gb{padding:5px 12px;border-radius:var(--r);border:0.5px solid var(--border2);background:var(--c2);color:var(--c7);font-size:12px;cursor:pointer;transition:all .15s;font-family:inherit}
.gb:hover{background:var(--c3);color:var(--c9)}
.gb.on{background:var(--accent);border-color:var(--accent);color:#fff;font-weight:500}
.grade-row{display:flex;gap:5px;flex-wrap:wrap}
.chips{display:flex;flex-wrap:wrap;gap:4px}
.chip{padding:3px 9px;border-radius:20px;border:0.5px solid var(--border2);background:var(--c2);color:var(--c7);font-size:11px;cursor:pointer;transition:all .15s;user-select:none}
.chip:hover{background:var(--c3);color:var(--c9)}
.chip.on{background:rgba(79,127,255,.2);border-color:var(--accent);color:#7aaeff}
.chip.teal.on{background:rgba(30,203,138,.15);border-color:var(--teal);color:#4edda8}
.btn{padding:7px 14px;border-radius:var(--r);font-size:13px;cursor:pointer;border:0.5px solid var(--border2);background:var(--c2);color:var(--c8);transition:all .15s;display:inline-flex;align-items:center;gap:5px;white-space:nowrap;font-family:inherit;line-height:1}
.btn:hover:not(:disabled){background:var(--c3);color:var(--c9)}
.btn:active:not(:disabled){transform:scale(.98)}
.btn:disabled{opacity:.35;cursor:not-allowed;transform:none}
.btn-blue{background:var(--accent);border-color:var(--accent);color:#fff}
.btn-blue:hover:not(:disabled){background:#3d6be8}
.btn-teal{background:rgba(30,203,138,.2);border-color:var(--teal);color:#4edda8}
.btn-teal:hover:not(:disabled){background:rgba(30,203,138,.3)}
.btn-amber{background:rgba(245,166,35,.15);border-color:var(--amber);color:#f9c060}
.btn-red{background:rgba(255,79,106,.15);border-color:var(--red);color:#ff7a90}
.btn-sm{padding:4px 10px;font-size:12px}
.btn-xs{padding:3px 8px;font-size:11px}
.btn-full{width:100%;justify-content:center;padding:11px;font-size:14px}

/* ─── FORM ─── */
.ck-list{display:flex;flex-direction:column;gap:6px}
.ck-row{display:flex;align-items:center;gap:8px;font-size:13px;cursor:pointer;color:var(--c8)}
.ck-row input{accent-color:var(--teal);width:14px;height:14px;cursor:pointer;flex-shrink:0}
.ck-sub{font-size:10px;color:var(--c6);margin-left:auto}
.finput{width:100%;padding:8px 10px;border:0.5px solid var(--border2);border-radius:var(--r);font-size:13px;color:var(--c9);background:var(--c2);font-family:inherit}
.finput:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px rgba(79,127,255,.15)}
.tarea{width:100%;font-size:13px;line-height:1.8;resize:vertical;min-height:140px;border:0.5px solid var(--border2);border-radius:var(--r);padding:10px 12px;color:var(--c9);background:var(--c2);font-family:inherit}
.tarea:focus{outline:none;border-color:var(--teal);box-shadow:0 0 0 3px rgba(30,203,138,.1)}

/* ─── MODE TABS ─── */
.mtabs{display:flex;border:0.5px solid var(--border2);border-radius:var(--r);overflow:hidden;width:fit-content;margin-bottom:12px}
.mtab{padding:6px 14px;font-size:12px;font-weight:500;border:none;cursor:pointer;background:var(--c2);color:var(--c7);transition:all .15s;display:flex;align-items:center;gap:5px;font-family:inherit}
.mtab.on{background:var(--teal);color:var(--c0)}

/* ─── FILE UPLOAD ─── */
.dropzone{border:1.5px dashed var(--border2);border-radius:var(--rl);padding:24px;text-align:center;cursor:pointer;transition:all .15s}
.dropzone:hover,.dropzone.drag{background:rgba(79,127,255,.06);border-color:var(--accent);border-style:solid}
.flist{display:flex;flex-direction:column;gap:5px;margin-top:8px}
.fitem{display:flex;align-items:center;gap:8px;padding:7px 10px;background:var(--c2);border-radius:var(--r);font-size:12px;border:0.5px solid var(--border)}
.fitem .fname{flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;color:var(--c8)}
.fitem .fdel{border:none;background:none;color:var(--c6);font-size:16px;cursor:pointer;padding:0 3px;border-radius:4px;font-family:inherit}
.fitem .fdel:hover{background:rgba(255,79,106,.2);color:var(--red)}

/* ─── PROGRESS / GEN ─── */
.prog{height:3px;background:var(--c3);border-radius:2px;overflow:hidden}
.prog-fill{height:100%;border-radius:2px;transition:width .25s}
.gen-state{background:var(--c1);border:0.5px solid var(--border);border-radius:var(--rl);padding:24px;display:none}
.gen-state.on{display:block}
.spinner{width:28px;height:28px;border:2px solid var(--c4);border-top-color:var(--accent);border-radius:50%;animation:spin .7s linear infinite;flex-shrink:0}
.spinner.teal{border-top-color:var(--teal)}
@keyframes spin{to{transform:rotate(360deg)}}
.step-row{display:flex;align-items:center;gap:8px;font-size:12px;color:var(--c6);padding:3px 0}
.step-row.done{color:var(--teal)}
.step-row.active{color:var(--c9);font-weight:500}
.step-dot{width:7px;height:7px;border-radius:50%;background:var(--c4);flex-shrink:0;transition:all .3s}
.step-row.done .step-dot{background:var(--teal)}
.step-row.active .step-dot{background:var(--accent);box-shadow:0 0 0 3px rgba(79,127,255,.2)}

/* ─── PANE ─── */
.pane{background:var(--c1);border:0.5px solid var(--border);border-radius:var(--rl);display:flex;flex-direction:column;overflow:hidden}
.pane-head{padding:9px 14px;border-bottom:0.5px solid var(--border);display:flex;align-items:center;justify-content:space-between;background:var(--c2);flex-shrink:0;gap:6px}
.pane-title{font-size:12px;font-weight:500;color:var(--c7);white-space:nowrap}
.otabs{display:flex;gap:1px;padding:8px 10px 0;border-bottom:0.5px solid var(--border);background:var(--c2);overflow-x:auto;flex-shrink:0}
.otab{padding:5px 11px;border-radius:var(--r) var(--r) 0 0;font-size:12px;cursor:pointer;border:0.5px solid transparent;border-bottom:none;color:var(--c6);background:none;transition:all .15s;margin-bottom:-0.5px;white-space:nowrap;font-family:inherit}
.otab:hover{background:var(--c3);color:var(--c8)}
.otab.on{background:var(--c1);border-color:var(--border);color:var(--c9);font-weight:500}
.opanel{display:none;padding:14px;overflow-y:auto;max-height:calc(100vh - 300px)}
.opanel.on{display:block}
.opanel::-webkit-scrollbar{width:3px}

/* ─── Q LIST ─── */
.qlist{display:flex;flex-direction:column;gap:2px;max-height:calc(100vh - 280px);overflow-y:auto}
.qitem{display:flex;align-items:center;gap:7px;padding:7px 9px;border-radius:var(--r);cursor:pointer;border:0.5px solid transparent;user-select:none;transition:all .15s}
.qitem:hover{background:var(--c2)}
.qitem.on{background:rgba(79,127,255,.1);border-color:rgba(79,127,255,.3)}
.qnum-b{width:26px;height:26px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:600;flex-shrink:0;background:var(--c3);color:var(--c7);transition:all .15s;font-family:'IBM Plex Mono',monospace}
.qitem.on .qnum-b{background:var(--accent);color:#fff}
.qi-info{flex:1;min-width:0}
.qi-type{font-size:12px;font-weight:500;color:var(--c8);overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.qitem.on .qi-type{color:var(--c9)}
.qi-meta{font-size:10px;color:var(--c6);font-family:'IBM Plex Mono',monospace}
.qi-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0}
.drag-h{cursor:grab;color:var(--c5);font-size:13px;padding:0 2px;user-select:none}
.drag-h:active{cursor:grabbing}

/* ─── PASSAGE & Q ─── */
.pass-text{font-size:13px;line-height:2.0;color:var(--c8);outline:none;border-radius:4px;padding:2px}
.pass-text:focus{background:rgba(79,127,255,.05)}
.hl{background:rgba(79,127,255,.2);border-radius:3px;padding:0 2px;color:var(--c9)}
.blank-fill{display:inline-block;width:68px;border-bottom:1.5px solid var(--c8);vertical-align:bottom}
.qstem{font-size:13px;color:var(--c8);line-height:1.7;margin-bottom:10px;outline:none;border-radius:4px;padding:2px}
.qstem:focus{background:rgba(79,127,255,.05)}
.choices{display:flex;flex-direction:column;gap:4px}
.choice{display:flex;align-items:flex-start;gap:8px;padding:7px 10px;border-radius:var(--r);border:0.5px solid var(--border);cursor:pointer;font-size:13px;color:var(--c7);transition:all .15s;user-select:none}
.choice:hover:not(.locked){background:var(--c2);border-color:var(--border2)}
.choice.picked{background:rgba(79,127,255,.1);border-color:var(--accent);color:#7aaeff}
.choice.correct{background:rgba(30,203,138,.1);border-color:var(--teal);color:#4edda8}
.choice.wrong{background:rgba(255,79,106,.1);border-color:var(--red);color:#ff7a90}
.cnum{width:20px;height:20px;border-radius:50%;background:var(--c3);font-size:11px;font-weight:500;display:flex;align-items:center;justify-content:center;flex-shrink:0;transition:all .15s;font-family:'IBM Plex Mono',monospace}
.choice.picked .cnum{background:var(--accent);color:#fff}
.choice.correct .cnum{background:var(--teal);color:var(--c0)}
.choice.wrong .cnum{background:var(--red);color:#fff}
.choice-text{flex:1;outline:none;min-width:10px}

/* ─── SET SUMMARY ─── */
.sum-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:7px;margin-bottom:10px}
.si{background:var(--c2);border-radius:var(--r);padding:8px;text-align:center;border:0.5px solid var(--border)}
.si-v{font-size:18px;font-weight:500;color:var(--c9);font-family:'IBM Plex Mono',monospace}
.si-l{font-size:10px;color:var(--c6);margin-top:1px}
.tb-row{display:flex;align-items:center;justify-content:space-between;font-size:12px;padding:3px 0;border-bottom:0.5px solid var(--border)}
.tb-row:last-child{border-bottom:none}

/* ─── PARSE ─── */
.parse-block{background:var(--c2);border-radius:var(--r);padding:11px 13px;font-size:13px;line-height:2.2;margin-bottom:8px;border:0.5px solid var(--border)}
.p-s{background:rgba(79,127,255,.2);border-radius:3px;padding:0 2px;color:#7aaeff}
.p-v{background:rgba(255,79,106,.2);border-radius:3px;padding:0 2px;color:#ff7a90}
.p-o{background:rgba(30,203,138,.2);border-radius:3px;padding:0 2px;color:#4edda8}
.p-adv{background:rgba(245,166,35,.2);border-radius:3px;padding:0 2px;color:#f9c060}
.pleg{display:flex;align-items:center;gap:4px;font-size:11px;color:var(--c7)}
.pleg-dot{width:9px;height:9px;border-radius:2px;flex-shrink:0}
.arow{display:flex;align-items:baseline;gap:7px;padding:5px 0;border-bottom:0.5px solid var(--border);font-size:12px;color:var(--c8)}
.arow:last-child{border-bottom:none}
.atag{width:30px;font-weight:600;font-size:10px;text-align:center;padding:1px 3px;border-radius:4px;flex-shrink:0;font-family:'IBM Plex Mono',monospace}
.atag-s{background:rgba(79,127,255,.2);color:#7aaeff}
.atag-v{background:rgba(255,79,106,.2);color:#ff7a90}
.atag-o{background:rgba(30,203,138,.2);color:#4edda8}
.atag-adv{background:rgba(245,166,35,.2);color:#f9c060}
.aval{flex:1;color:var(--c9)}
.anote{font-size:11px;color:var(--c6);white-space:nowrap;font-family:'IBM Plex Mono',monospace}

/* ─── LOG ─── */
.log-e{display:flex;align-items:flex-start;gap:7px;padding:5px 0;border-bottom:0.5px solid var(--border);font-size:12px}
.log-e:last-child{border-bottom:none}
.log-t{color:var(--c6);font-size:10px;white-space:nowrap;width:52px;flex-shrink:0;margin-top:1px;font-family:'IBM Plex Mono',monospace}
.log-m{color:var(--c8);line-height:1.5;flex:1}

/* ─── NOTIF ─── */
.notif{display:flex;align-items:flex-start;gap:8px;padding:8px 12px;border-radius:var(--r);font-size:12px;line-height:1.5}
.notif-teal{background:rgba(30,203,138,.1);color:#4edda8;border:0.5px solid rgba(30,203,138,.3)}
.notif-blue{background:rgba(79,127,255,.1);color:#7aaeff;border:0.5px solid rgba(79,127,255,.3)}
.notif-amber{background:rgba(245,166,35,.1);color:#f9c060;border:0.5px solid rgba(245,166,35,.3)}
.notif-red{background:rgba(255,79,106,.1);color:#ff7a90;border:0.5px solid rgba(255,79,106,.3)}

/* ─── AI STREAM ─── */
.ai-stream{background:var(--c2);border:0.5px solid var(--border);border-radius:var(--rl);padding:16px;font-size:13px;line-height:1.9;color:var(--c8);min-height:100px;white-space:pre-wrap;font-family:'IBM Plex Mono',monospace}
.ai-stream .cursor{display:inline-block;width:2px;height:1em;background:var(--accent);animation:blink .8s infinite;vertical-align:text-bottom;margin-left:2px}
@keyframes blink{50%{opacity:0}}

/* ─── EXPORT BAR ─── */
.export-bar{background:var(--c1);border:0.5px solid var(--border);border-radius:var(--rl);padding:10px 13px;display:flex;gap:7px;align-items:center;flex-wrap:wrap}

/* ─── REVIEW BTN ─── */
.review-fixed{position:sticky;bottom:20px;display:flex;justify-content:flex-end;margin-top:6px;pointer-events:none}
.review-btn{pointer-events:all;background:rgba(245,166,35,.15);border:0.5px solid var(--amber);color:#f9c060;padding:8px 14px;border-radius:var(--rl);font-size:12px;font-weight:500;cursor:pointer;display:flex;align-items:center;gap:6px;box-shadow:0 4px 20px rgba(0,0,0,.4);transition:all .2s;font-family:inherit}
.review-btn.done{background:rgba(30,203,138,.15);border-color:var(--teal);color:#4edda8}

/* ─── STORAGE ─── */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:14px}
.stat{background:var(--c1);border-radius:var(--r);padding:12px;border:0.5px solid var(--border)}
.stat-l{font-size:11px;color:var(--c6);margin-bottom:3px}
.stat-v{font-size:20px;font-weight:500;color:var(--c9);font-family:'IBM Plex Mono',monospace}
.stat-s{font-size:10px;color:var(--c6);margin-top:2px}
.store-ctrl{display:flex;gap:7px;flex-wrap:wrap;margin-bottom:10px;align-items:center}
.store-ctrl input,.store-ctrl select{padding:6px 10px;border:0.5px solid var(--border2);border-radius:var(--r);font-size:12px;color:var(--c8);background:var(--c2);font-family:inherit}
.store-ctrl input{flex:1;min-width:160px}
.store-ctrl input:focus,.store-ctrl select:focus{outline:none;border-color:var(--accent)}
.proj-row{border:0.5px solid var(--border);border-radius:var(--rl);margin-bottom:8px;overflow:hidden;transition:border-color .15s}
.proj-row:hover{border-color:var(--border2)}
.proj-head{display:flex;align-items:center;gap:10px;padding:11px 14px;cursor:pointer;background:var(--c1);user-select:none}
.proj-icon{width:34px;height:34px;border-radius:var(--r);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.proj-info{flex:1;min-width:0}
.proj-title{font-size:13px;font-weight:500;color:var(--c9);overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.proj-meta{font-size:11px;color:var(--c6);margin-top:1px;font-family:'IBM Plex Mono',monospace}
.proj-tags{display:flex;gap:4px;flex-wrap:wrap;margin-top:3px}
.ptag{font-size:10px;padding:1px 6px;border-radius:10px;background:var(--c3);border:0.5px solid var(--border);color:var(--c7)}
.proj-arrow{font-size:12px;color:var(--c6);transition:transform .2s;margin-left:4px;flex-shrink:0}
.proj-arrow.open{transform:rotate(180deg)}
.proj-body{display:none;padding:12px 14px;border-top:0.5px solid var(--border);background:var(--c2)}
.proj-body.on{display:block}
.ver-item{display:flex;align-items:center;gap:7px;padding:6px 10px;background:var(--c1);border-radius:var(--r);border:0.5px solid var(--border);font-size:12px;margin-bottom:4px;color:var(--c8)}
.cfg-grid{display:grid;grid-template-columns:1fr 1fr;gap:4px;margin-top:6px}
.cfg-item{font-size:12px;display:flex;gap:5px}
.cfg-k{color:var(--c6);flex-shrink:0;min-width:65px}
.cfg-v{color:var(--c9);font-weight:500}

/* ─── EMPTY ─── */
.empty{padding:40px;text-align:center}
.empty svg{opacity:.15;margin-bottom:12px;display:block;margin-left:auto;margin-right:auto}
.empty-t{font-size:13px;font-weight:500;color:var(--c7);margin-bottom:4px}
.empty-s{font-size:12px;color:var(--c6)}
.divider{height:0.5px;background:var(--border);margin:10px 0}

/* ─── MODAL ─── */
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:500;display:flex;align-items:center;justify-content:center;opacity:0;transition:opacity .2s;pointer-events:none}
.modal-overlay.on{opacity:1;pointer-events:all}
.modal{background:var(--c1);border:0.5px solid var(--border2);border-radius:var(--rxl);width:560px;max-width:calc(100vw-32px);max-height:88vh;overflow-y:auto;box-shadow:0 16px 60px rgba(0,0,0,.6);transform:translateY(8px);transition:transform .2s}
.modal-overlay.on .modal{transform:translateY(0)}
.modal-head{padding:14px 18px;border-bottom:0.5px solid var(--border);display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;background:var(--c1);z-index:1}
.modal-title{font-size:15px;font-weight:500;color:var(--c9)}
.mclose{border:none;background:none;font-size:20px;cursor:pointer;color:var(--c6);line-height:1;padding:2px 6px;border-radius:var(--r);font-family:inherit}
.mclose:hover{background:var(--c3);color:var(--c9)}
.modal-body{padding:18px}
.modal-footer{padding:12px 18px;border-top:0.5px solid var(--border);display:flex;gap:8px;justify-content:flex-end;background:var(--c1)}

/* ─── PDF PRINT ─── */
#pdf-sheet{display:none}
@media print{
  body>*{display:none!important}
  #pdf-sheet{display:block!important;font-family:'Noto Sans KR',sans-serif;font-size:11pt;line-height:1.9;color:#000;padding:18mm 22mm;position:static}
  .pdf-hd{text-align:center;margin-bottom:16pt;padding-bottom:10pt;border-bottom:1.5pt solid #000}
  .pdf-ttl{font-size:17pt;font-weight:700;letter-spacing:-.3px}
  .pdf-sub{font-size:10pt;color:#555;margin-top:3pt}
  .pdf-q{margin-bottom:20pt;page-break-inside:avoid}
  .pdf-qn{font-size:11pt;font-weight:700;margin-bottom:5pt}
  .pdf-pass{font-size:10.5pt;line-height:1.95;margin-bottom:9pt;text-indent:1em}
  .pdf-stem{font-size:10.5pt;margin-bottom:7pt;font-weight:500}
  .pdf-ch{font-size:10.5pt;margin-bottom:3pt}
  .pdf-meta{font-size:9pt;color:#999;margin-top:4pt;padding-top:3pt;border-top:.5pt solid #ddd}
}

/* ─── TOAST ─── */
#toast{position:fixed;bottom:24px;left:50%;transform:translateX(-50%) translateY(16px);background:var(--c9);color:var(--c0);padding:9px 18px;border-radius:var(--rl);font-size:13px;opacity:0;transition:all .25s;pointer-events:none;z-index:9999;white-space:nowrap;font-weight:500}

/* ─── VERSION BADGE ─── */
.ver-active{background:rgba(79,127,255,.15);border:0.5px solid var(--accent);color:#7aaeff}

/* ─── AI TYPING INDICATOR ─── */
.typing-dots{display:inline-flex;gap:3px;align-items:center;margin-left:4px}
.typing-dots span{width:4px;height:4px;border-radius:50%;background:var(--accent);animation:tdot 1.2s infinite both}
.typing-dots span:nth-child(2){animation-delay:.2s}
.typing-dots span:nth-child(3){animation-delay:.4s}
@keyframes tdot{0%,80%,100%{opacity:.2;transform:scale(.8)}40%{opacity:1;transform:scale(1)}}

/* ─── PHASE BADGE ─── */
.phase-badge{display:inline-flex;align-items:center;gap:5px;font-size:11px;font-family:'IBM Plex Mono',monospace;padding:3px 8px;border-radius:var(--r);background:var(--c3);color:var(--c6);border:0.5px solid var(--border)}
.phase-badge.active{background:rgba(30,203,138,.12);color:var(--teal);border-color:rgba(30,203,138,.3)}

@media(max-width:860px){.layout-3{grid-template-columns:1fr}.stats-row{grid-template-columns:repeat(2,1fr)}}
</style>
</head>
<body>

<div id="pdf-sheet"></div>

<nav class="nav">
  <div class="logo" onclick="goNav(document.querySelector('.ntab'),'p-t1')">NE<em>능률</em> / <em>수능독해 AI</em></div>
  <div class="ntabs">
    <button class="ntab on" onclick="goNav(this,'p-t1')">T1 — 모의고사 생성</button>
    <button class="ntab" onclick="goNav(this,'p-t2')">T2 — 지문 변형</button>
    <button class="ntab" onclick="goNav(this,'p-storage')">보관함<span id="navBadge" style="display:none;background:var(--accent);color:#fff;font-size:10px;padding:1px 7px;border-radius:10px;margin-left:4px;font-family:'IBM Plex Mono',monospace"></span></button>
  </div>
  <div class="nav-r">
    <span class="phase-badge active">Phase 2 · Beta</span>
    <span class="pill pill-blue">정액 무제한</span>
    <button class="btn btn-sm" onclick="openModal('modal-settings')">설정</button>
  </div>
</nav>

<!-- ═══════════════════════════════════════
     T1 PAGE
═══════════════════════════════════════ -->
<div id="p-t1" class="page on">
  <div class="layout-3">

    <!-- 사이드바 -->
    <div class="side-col">
      <div class="card">
        <div class="ch">학년 [SCR-001]</div>
        <div class="grade-row" id="gradeRow">
          <button class="gb on" onclick="sel(this,'gradeRow')">고1</button>
          <button class="gb" onclick="sel(this,'gradeRow')">고2</button>
          <button class="gb" onclick="sel(this,'gradeRow')">수능</button>
        </div>
      </div>

      <div class="card">
        <div class="ch">난이도 — 9단계</div>
        <div class="grade-row" id="diffRow">
          <button class="gb" onclick="sel(this,'diffRow')">Easier</button>
          <button class="gb on" onclick="sel(this,'diffRow')">As-is</button>
          <button class="gb" onclick="sel(this,'diffRow')">Harder</button>
        </div>
      </div>

      <div class="card">
        <div class="ch">핵심 유형 9종 [SCR-004]</div>
        <div class="chips" id="typeChips">
          <span class="chip on" onclick="tc(this)">함의 추론</span>
          <span class="chip on" onclick="tc(this)">빈칸 추론</span>
          <span class="chip" onclick="tc(this)">글의 순서</span>
          <span class="chip" onclick="tc(this)">문장 삽입</span>
          <span class="chip" onclick="tc(this)">주제·요지</span>
          <span class="chip" onclick="tc(this)">무관한 문장</span>
          <span class="chip" onclick="tc(this)">어법·어휘</span>
          <span class="chip" onclick="tc(this)">제목 추론</span>
          <span class="chip" onclick="tc(this)">요약문</span>
        </div>
      </div>

      <div class="card">
        <div class="ch">토픽/소재</div>
        <div class="chips">
          <span class="chip teal on" onclick="tc(this,'teal')">과학</span>
          <span class="chip teal on" onclick="tc(this,'teal')">경제</span>
          <span class="chip teal" onclick="tc(this,'teal')">환경</span>
          <span class="chip teal" onclick="tc(this,'teal')">심리</span>
          <span class="chip teal" onclick="tc(this,'teal')">예술</span>
          <span class="chip teal" onclick="tc(this,'teal')">역사</span>
          <span class="chip teal" onclick="tc(this,'teal')">사회</span>
        </div>
      </div>

      <div class="card">
        <div class="ch">시험지 세트 수</div>
        <div class="grade-row" id="qtyRow">
          <button class="gb" onclick="sel(this,'qtyRow')">1회</button>
          <button class="gb on" onclick="sel(this,'qtyRow')">3회</button>
          <button class="gb" onclick="sel(this,'qtyRow')">5회</button>
          <button class="gb" onclick="sel(this,'qtyRow')">10회</button>
        </div>
      </div>

      <div class="card">
        <div class="ch">문항 수/세트</div>
        <div class="grade-row" id="qcntRow">
          <button class="gb" onclick="sel(this,'qcntRow')">10문항</button>
          <button class="gb on" onclick="sel(this,'qcntRow')">20문항</button>
          <button class="gb" onclick="sel(this,'qcntRow')">28문항</button>
        </div>
      </div>

      <button class="btn btn-blue btn-full" id="t1GenBtn" onclick="t1Gen()">
        <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
        BB 엔진 · AI 시험지 생성
      </button>
    </div>

    <!-- 메인 -->
    <div class="main-col">
      <div class="gen-state" id="t1GenState">
        <div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">
          <div class="spinner"></div>
          <div style="flex:1">
            <div style="font-size:14px;font-weight:500;color:var(--c9)" id="t1GL">BB 엔진 가동 중...</div>
            <div style="font-size:12px;color:var(--c6);margin-top:2px" id="t1GS"></div>
          </div>
          <div style="text-align:right">
            <div style="font-size:11px;color:var(--c6);margin-bottom:3px;font-family:'IBM Plex Mono',monospace" id="t1Pct">0%</div>
            <div class="prog" style="width:110px"><div class="prog-fill" id="t1P" style="width:0%;background:var(--accent)"></div></div>
          </div>
        </div>
        <div id="t1Steps"></div>
        <button class="btn btn-sm" style="margin-top:12px;color:var(--c6)" onclick="cancelGen('t1')">취소</button>
      </div>

      <div class="empty" id="t1Empty">
        <svg width="48" height="48" fill="none" stroke="currentColor" stroke-width="1" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
        <div class="empty-t">BB 창작 엔진 대기 중</div>
        <div class="empty-s">조건 설정 후 생성 — 무(無)에서 유(有)를 창작합니다</div>
      </div>

      <div id="t1Result" style="display:none">
        <div class="notif notif-teal" style="margin-bottom:12px">
          <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24" style="flex-shrink:0;margin-top:2px"><polyline points="20 6 9 17 4 12"/></svg>
          <span id="t1NT"></span>
        </div>

        <!-- examSet 분할 레이아웃 -->
        <div style="display:grid;grid-template-columns:200px 1fr;gap:10px;align-items:start">

          <!-- 좌: 문항 목록 -->
          <div class="pane" style="min-height:360px">
            <div class="pane-head">
              <span class="pane-title">문항 목록</span>
              <div style="display:flex;gap:4px">
                <button class="btn btn-xs btn-teal" onclick="addQ('t1')">+ 추가</button>
              </div>
            </div>
            <div style="padding:6px"><div class="qlist" id="t1QL"></div></div>
          </div>

          <!-- 우: 문항 상세 -->
          <div class="pane" id="t1DP">
            <div class="pane-head">
              <span class="pane-title" id="t1DT">문항 선택</span>
              <div style="display:flex;gap:4px;align-items:center">
                <span class="pill pill-gray" id="t1DS"></span>
                <button class="btn btn-xs" onclick="regenQ('t1')" title="AI로 재생성">↺ AI 재생성</button>
                <button class="btn btn-xs btn-red" onclick="delQ('t1')">삭제</button>
              </div>
            </div>
            <div class="otabs" id="t1OT">
              <button class="otab on" onclick="oTab(this,'ot-q')">문항</button>
              <button class="otab" onclick="oTab(this,'ot-trans')">해설지</button>
              <button class="otab" onclick="oTab(this,'ot-parse')">구문분석</button>
              <button class="otab" onclick="oTab(this,'ot-voca')">어휘 리스트</button>
              <button class="otab" onclick="oTab(this,'ot-ai')">AI 생성 로그</button>
              <button class="otab" onclick="oTab(this,'ot-crit')">출제 기준</button>
            </div>

            <!-- 문항 탭 -->
            <div id="ot-q" class="opanel on">
              <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px">
                <div>
                  <div style="font-size:11px;color:var(--c6);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">PASSAGE <span style="color:var(--accent)">· 클릭 편집</span></div>
                  <div class="pass-text" id="t1Pass" contenteditable="true" spellcheck="false"></div>
                </div>
                <div>
                  <div class="qstem" id="t1QN" contenteditable="true" spellcheck="false" style="font-size:11px;color:var(--c6);font-family:'IBM Plex Mono',monospace"></div>
                  <div class="qstem" id="t1QS" contenteditable="true" spellcheck="false"></div>
                  <div class="choices" id="t1CH"></div>
                  <div id="t1FB" style="margin-top:8px"></div>
                </div>
              </div>
            </div>

            <!-- 해설지 탭 (AI 실시간 생성) -->
            <div id="ot-trans" class="opanel">
              <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:10px">
                <div style="font-size:12px;font-weight:500;color:var(--c7)">AI 해설지 [SCR-005]</div>
                <button class="btn btn-xs btn-blue" onclick="genTrans()">
                  <svg width="11" height="11" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
                  AI 해설 생성
                </button>
              </div>
              <div class="ai-stream" id="transStream">AI 해설 생성 버튼을 눌러주세요.</div>
              <div class="divider"></div>
              <div style="font-size:12px;font-weight:500;color:var(--c7);margin-bottom:6px">정답 근거</div>
              <div id="t1Rat" style="font-size:13px;color:var(--c8);line-height:1.7"></div>
              <div style="margin-top:10px"><button class="btn btn-sm" onclick="exportSec('해설지')">해설지 PDF</button></div>
            </div>

            <!-- 구문분석 탭 -->
            <div id="ot-parse" class="opanel">
              <div class="parse-block" id="t1PB"></div>
              <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:10px">
                <span class="pleg"><span class="pleg-dot" style="background:rgba(79,127,255,.4)"></span>S 주어</span>
                <span class="pleg"><span class="pleg-dot" style="background:rgba(255,79,106,.4)"></span>V 동사</span>
                <span class="pleg"><span class="pleg-dot" style="background:rgba(30,203,138,.4)"></span>O 목적어</span>
                <span class="pleg"><span class="pleg-dot" style="background:rgba(245,166,35,.4)"></span>ADV 부사</span>
              </div>
              <div id="t1PD"></div>
              <div style="margin-top:10px"><button class="btn btn-sm" onclick="exportSec('구문분석')">구문분석지 PDF</button></div>
            </div>

            <!-- 어휘 탭 -->
            <div id="ot-voca" class="opanel">
              <div style="font-size:12px;color:var(--c7);margin-bottom:8px">뜻 입력 후 Enter → 정오 확인</div>
              <table id="t1VT" style="width:100%;border-collapse:collapse;font-size:13px"></table>
              <div style="margin-top:10px;display:flex;gap:6px">
                <button class="btn btn-sm" onclick="exportVoca()">TXT 다운로드</button>
                <button class="btn btn-sm" onclick="exportSec('어휘 테스트지')">어휘 테스트지 PDF</button>
              </div>
            </div>

            <!-- AI 생성 로그 탭 -->
            <div id="ot-ai" class="opanel">
              <div style="font-size:12px;font-weight:500;color:var(--c7);margin-bottom:8px;font-family:'IBM Plex Mono',monospace">AI GENERATION LOG</div>
              <div id="t1Log"></div>
            </div>

            <!-- 출제 기준 탭 -->
            <div id="ot-crit" class="opanel"><div id="t1Crit"></div></div>
          </div>
        </div>

        <div class="export-bar" style="margin-top:10px">
          <input type="text" id="t1Brand" placeholder="OO학원 주간 수능독해" style="padding:6px 10px;border:0.5px solid var(--border2);border-radius:var(--r);font-size:12px;color:var(--c8);background:var(--c2);font-family:inherit;flex:1;min-width:120px">
          <button class="btn btn-sm" onclick="openLogoModal()">로고</button>
          <button class="btn btn-sm btn-blue" onclick="showPrint('t1')">전체 시험지 PDF [SCR-003]</button>
          <button class="btn btn-sm" onclick="exportHWP()">HWP 2단</button>
          <button class="btn btn-sm btn-teal" onclick="saveProj('t1')" style="margin-left:auto">보관함 저장 [SCR-008]</button>
        </div>
        <div class="review-fixed">
          <button class="review-btn" id="t1RB" onclick="doReview('t1RB')">
            <svg width="11" height="11" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
            ★ NE 저자 검수 요청 [SCR-002]
          </button>
        </div>
      </div>
    </div>

    <!-- 우: 세트 요약 -->
    <div class="side-col" id="t1SC" style="display:none">
      <div class="pane">
        <div class="pane-head"><span class="pane-title">examSet 요약</span></div>
        <div style="padding:12px">
          <div class="sum-grid" id="t1SG"></div>
          <div class="divider"></div>
          <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">TYPE DIST.</div>
          <div id="t1TB"></div>
        </div>
      </div>
      <div class="pane">
        <div class="pane-head"><span class="pane-title">세트 전환</span></div>
        <div style="padding:6px"><div id="t1SS" style="display:flex;flex-direction:column;gap:3px"></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════
     T2 PAGE
═══════════════════════════════════════ -->
<div id="p-t2" class="page">
  <div class="layout-3">

    <div class="side-col">
      <div class="card">
        <div class="ch">학년 [전역 토글]</div>
        <div class="grade-row" id="t2GR"><button class="gb" onclick="sel(this,'t2GR')">고1</button><button class="gb on" onclick="sel(this,'t2GR')">고2</button><button class="gb" onclick="sel(this,'t2GR')">수능</button></div>
      </div>
      <div class="card">
        <div class="ch">변형 난이도</div>
        <div class="grade-row" id="t2DR"><button class="gb" onclick="sel(this,'t2DR')">Easier</button><button class="gb on" onclick="sel(this,'t2DR')">As-is</button><button class="gb" onclick="sel(this,'t2DR')">Harder</button></div>
      </div>
      <div class="card">
        <div class="ch">생성 콘텐츠 [SCR-007]</div>
        <div class="ck-list">
          <label class="ck-row"><input type="checkbox" checked><span>수능형 변형</span><span class="ck-sub">11종</span></label>
          <label class="ck-row"><input type="checkbox" checked><span>학교 내신형</span><span class="ck-sub">7종</span></label>
          <label class="ck-row"><input type="checkbox"><span>워크북</span><span class="ck-sub">10종</span></label>
          <label class="ck-row"><input type="checkbox" checked><span style="color:#4edda8;font-weight:500">S/V/O/C 파싱</span><span class="ck-sub" style="color:var(--teal)">독점</span></label>
        </div>
      </div>

      <div class="card">
        <div class="ch">NE 직영 교재 [독점↑]</div>
        <div class="chips">
          <span class="chip" onclick="tc(this,'teal')">빠바</span>
          <span class="chip" onclick="tc(this,'teal')">맞수</span>
          <span class="chip" onclick="tc(this,'teal')">능률영어</span>
          <span class="chip" onclick="tc(this,'teal')">EBS 연계</span>
        </div>
        <div style="font-size:11px;color:var(--c6);margin-top:7px">선택 시 해당 지문 자동 로드</div>
      </div>

      <button class="btn btn-teal btn-full" id="t2GenBtn" onclick="t2Gen()">
        <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
        레슨위드 NLP · 변형 생성
      </button>
    </div>

    <div class="main-col">
      <!-- 입력 카드 -->
      <div class="card" id="t2IC">
        <div class="mtabs">
          <button class="mtab on" id="mFile" onclick="swMode('file')">
            <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/></svg>
            파일 업로드
          </button>
          <button class="mtab" id="mText" onclick="swMode('text')">
            <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"/></svg>
            텍스트 입력
          </button>
        </div>
        <div id="modeFile">
          <input type="file" id="rFI" multiple accept=".pdf,.hwp,.docx" style="display:none" onchange="hFI(this.files)">
          <div class="dropzone" id="dz" onclick="document.getElementById('rFI').click()" ondragover="event.preventDefault();this.classList.add('drag')" ondragleave="this.classList.remove('drag')" ondrop="hDrop(event)">
            <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="1.3" viewBox="0 0 24 24" style="opacity:.25;margin-bottom:7px"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/></svg>
            <div style="font-size:13px;font-weight:500;color:var(--c8);margin-bottom:3px">PDF, HWP, DOCX 드래그 또는 클릭</div>
            <div style="font-size:12px;color:var(--c6)">최대 50개 지문 · 파일당 20MB [SCR-006]</div>
          </div>
          <div class="flist" id="flist"></div>
        </div>
        <div id="modeText" style="display:none">
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:6px">
            <span style="font-size:12px;color:var(--c7)">지문 붙여넣기 — 빈 줄로 구분</span>
            <div style="display:flex;gap:5px">
              <button class="btn btn-sm" onclick="loadEx()">예시</button>
              <button class="btn btn-sm btn-red" onclick="clrTxt()">지우기</button>
            </div>
          </div>
          <textarea class="tarea" id="txtIn" placeholder="지문을 붙여넣으세요..." oninput="upMeta()"></textarea>
          <div style="display:flex;justify-content:space-between;font-size:11px;color:var(--c6);margin-top:4px;font-family:'IBM Plex Mono',monospace"><span id="t2ML"></span><span id="t2MR"></span></div>
        </div>
      </div>

      <!-- 생성 중 -->
      <div class="gen-state" id="t2GS">
        <div style="display:flex;align-items:center;gap:12px;margin-bottom:14px">
          <div class="spinner teal"></div>
          <div style="flex:1">
            <div style="font-size:14px;font-weight:500;color:var(--c9)" id="t2GL">레슨위드 NLP 처리 중...</div>
            <div style="font-size:12px;color:var(--c6);margin-top:2px" id="t2GSub"></div>
          </div>
          <div style="text-align:right">
            <div style="font-size:11px;color:var(--c6);margin-bottom:3px;font-family:'IBM Plex Mono',monospace" id="t2Pct">0%</div>
            <div class="prog" style="width:110px"><div class="prog-fill" id="t2P" style="width:0%;background:var(--teal)"></div></div>
          </div>
        </div>
        <div id="t2Steps"></div>
        <button class="btn btn-sm" style="margin-top:12px;color:var(--c6)" onclick="cancelGen('t2')">취소</button>
      </div>

      <!-- 결과 -->
      <div id="t2Result" style="display:none">
        <div class="notif notif-teal" style="margin-bottom:12px">
          <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24" style="flex-shrink:0;margin-top:2px"><polyline points="20 6 9 17 4 12"/></svg>
          <span id="t2NT"></span>
        </div>

        <div style="display:grid;grid-template-columns:200px 1fr;gap:10px;align-items:start">
          <div class="pane" style="min-height:360px">
            <div class="pane-head"><span class="pane-title">생성 문항 [28종]</span><button class="btn btn-xs btn-teal" onclick="addQ('t2')">+ 추가</button></div>
            <div style="padding:6px"><div class="qlist" id="t2QL"></div></div>
          </div>

          <div class="pane" id="t2DP">
            <div class="pane-head">
              <span class="pane-title" id="t2DT">문항 선택</span>
              <div style="display:flex;gap:4px;align-items:center"><span class="pill pill-gray" id="t2DS"></span><button class="btn btn-xs" onclick="regenQ('t2')">↺ AI 재생성</button><button class="btn btn-xs btn-red" onclick="delQ('t2')">삭제</button></div>
            </div>
            <div class="otabs" id="t2OT">
              <button class="otab on" onclick="oTab2(this,'t2-q')">문항</button>
              <button class="otab" onclick="oTab2(this,'t2-parse')">구문 파싱 [독점]</button>
              <button class="otab" onclick="oTab2(this,'t2-ai')">AI 생성 로그</button>
            </div>
            <div id="t2-q" class="opanel on">
              <div id="t2QE" style="padding:24px;text-align:center;color:var(--c6);font-size:13px">좌측 목록에서 문항을 선택하세요</div>
              <div id="t2QD" style="display:none">
                <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px">
                  <div>
                    <div style="font-size:11px;color:var(--c6);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">PASSAGE</div>
                    <div class="pass-text" id="t2Pass" contenteditable="true" spellcheck="false"></div>
                  </div>
                  <div>
                    <div class="qstem" id="t2QN" contenteditable="true" spellcheck="false"></div>
                    <div class="choices" id="t2CH"></div>
                    <div id="t2FB" style="margin-top:8px"></div>
                  </div>
                </div>
              </div>
            </div>
            <div id="t2-parse" class="opanel">
              <div class="notif notif-blue" style="margin-bottom:10px">
                <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" style="flex-shrink:0"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
                미시적 구문 정밀 해체 리포트 — NE능률 독점 기능 [SCR-007]
              </div>
              <div id="t2PC"></div>
            </div>
            <div id="t2-ai" class="opanel"><div id="t2Log"></div></div>
          </div>
        </div>

        <div class="export-bar" style="margin-top:10px">
          <button class="btn btn-sm btn-teal" onclick="showPrint('t2')">28종 패키지 PDF</button>
          <button class="btn btn-sm" onclick="exportHWP()">HWP 2단</button>
          <button class="btn btn-sm btn-teal" onclick="saveProj('t2')" style="margin-left:auto">보관함 저장</button>
        </div>
        <div class="review-fixed">
          <button class="review-btn" id="t2RB" onclick="doReview('t2RB')">
            <svg width="11" height="11" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
            ★ NE 저자 검수 요청 [SCR-002]
          </button>
        </div>
      </div>
    </div>

    <!-- 우: T2 세트 요약 -->
    <div class="side-col" id="t2SC" style="display:none">
      <div class="pane">
        <div class="pane-head"><span class="pane-title">변형 세트 요약</span></div>
        <div style="padding:12px">
          <div class="sum-grid" id="t2SG"></div>
          <div class="divider"></div>
          <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">TYPE DIST. (28종)</div>
          <div id="t2TB"></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════
     STORAGE PAGE
═══════════════════════════════════════ -->
<div id="p-storage" class="page">
  <div class="stats-row">
    <div class="stat"><div class="stat-l">총 프로젝트</div><div class="stat-v" id="st-t">0</div><div class="stat-s">누적</div></div>
    <div class="stat"><div class="stat-l">총 문항</div><div class="stat-v" id="st-q">0</div><div class="stat-s">T1+T2 합계</div></div>
    <div class="stat"><div class="stat-l">검수 완료</div><div class="stat-v" id="st-r">0</div><div class="stat-s">NE 인증 [SCR-002]</div></div>
    <div class="stat"><div class="stat-l">이달 출력</div><div class="stat-v" id="st-p">0</div><div class="stat-s">간행물 [SCR-003]</div></div>
  </div>
  <div class="store-ctrl">
    <input type="text" id="sSrch" placeholder="프로젝트명, 토픽 검색..." oninput="renderStore()">
    <select id="sGrd" onchange="renderStore()"><option value="">전체 학년</option><option>고1</option><option>고2</option><option>수능</option></select>
    <select id="sEng" onchange="renderStore()"><option value="">전체 엔진</option><option>T1 BB</option><option>T2 NLP</option></select>
    <select id="sRev" onchange="renderStore()"><option value="">전체 상태</option><option value="done">검수완료</option><option value="wait">검수대기</option></select>
    <select id="sFav" onchange="renderStore()"><option value="">전체</option><option value="fav">즐겨찾기</option></select>
    <button class="btn btn-xs btn-red" id="clrAllBtn" onclick="clrAll()" style="display:none;margin-left:auto">전체 삭제</button>
  </div>
  <div id="storeList"></div>
</div>

<!-- ═══ MODALS ═══ -->
<div class="modal-overlay" id="modal-settings">
  <div class="modal" onclick="event.stopPropagation()">
    <div class="modal-head"><span class="modal-title">계정 설정</span><button class="mclose" onclick="closeModal('modal-settings')">×</button></div>
    <div class="modal-body">
      <div style="margin-bottom:12px"><label style="font-size:12px;color:var(--c7);display:block;margin-bottom:4px">소속 학원명</label><input class="finput" id="setBrand" type="text" placeholder="예: 강남 NE영어학원"></div>
      <div style="margin-bottom:12px"><label style="font-size:12px;color:var(--c7);display:block;margin-bottom:4px">이메일</label><input class="finput" type="email" placeholder="example@nebooks.co.kr"></div>
      <div style="margin-bottom:12px"><label style="font-size:12px;color:var(--c7);display:block;margin-bottom:4px">검수 완료 시 알림</label><label class="ck-row"><input type="checkbox" checked><span>이메일 알림 수신</span></label></div>
      <div><label style="font-size:12px;color:var(--c7);display:block;margin-bottom:4px">기본 출력 포맷</label><select class="finput"><option>B4 시험지 PDF</option><option>HWP 2단</option><option>A4 PDF</option></select></div>
    </div>
    <div class="modal-footer"><button class="btn" onclick="closeModal('modal-settings')">취소</button><button class="btn btn-blue" onclick="saveSets()">저장</button></div>
  </div>
</div>

<div class="modal-overlay" id="modal-logo">
  <div class="modal" onclick="event.stopPropagation()">
    <div class="modal-head"><span class="modal-title">학원 로고 업로드</span><button class="mclose" onclick="closeModal('modal-logo')">×</button></div>
    <div class="modal-body">
      <input type="file" id="logoIn" accept="image/*" style="display:none" onchange="prevLogo(this)">
      <div style="border:1.5px dashed var(--border2);border-radius:var(--r);padding:24px;text-align:center;cursor:pointer" onclick="document.getElementById('logoIn').click()">
        <img id="logoPreview" style="display:none;max-height:60px;margin-bottom:8px">
        <div style="font-size:13px;color:var(--c7)" id="logoPlaceholder">이미지 클릭 업로드 (PNG/JPG · 2MB)</div>
      </div>
      <div style="font-size:12px;color:var(--c6);margin-top:8px">출력 시험지 상단에 자동 삽입됩니다 [SCR-003]</div>
    </div>
    <div class="modal-footer"><button class="btn" onclick="closeModal('modal-logo')">취소</button><button class="btn btn-blue" id="logoSaveBtn" onclick="saveLogo()" disabled>적용</button></div>
  </div>
</div>

<div class="modal-overlay" id="modal-print">
  <div class="modal" style="width:640px" onclick="event.stopPropagation()">
    <div class="modal-head"><span class="modal-title" id="printTitle">시험지 PDF 출력 미리보기</span><button class="mclose" onclick="closeModal('modal-print')">×</button></div>
    <div class="modal-body" style="padding:0">
      <div style="background:#222;padding:16px;max-height:60vh;overflow-y:auto">
        <div id="printBox" style="background:#fff;padding:18mm 22mm 16mm;font-family:'Noto Sans KR',sans-serif;font-size:11pt;line-height:1.9;color:#000;box-shadow:0 4px 24px rgba(0,0,0,.3)"></div>
      </div>
    </div>
    <div class="modal-footer">
      <button class="btn" onclick="closeModal('modal-print')">닫기</button>
      <button class="btn btn-blue" onclick="doPrint()">
        <svg width="13" height="13" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><polyline points="6 9 6 2 18 2 18 9"/><path d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"/><rect x="6" y="14" width="12" height="8"/></svg>
        인쇄 / PDF 저장
      </button>
    </div>
  </div>
</div>

<div id="toast"></div>

<script>
/* ═══════════════════════════════════════
   STATE — examSet 기반 구조 [수정사항 반영]
═══════════════════════════════════════ */
const S = {
  examSets: [],      // examSet[]
  t1Set: null,       // 현재 선택된 T1 examSet
  t2Set: null,       // 현재 선택된 T2 examSet
  selQ: null,        // 선택된 question
  projects: [],      // 보관함
  printCnt: 0,
  _t1iv: null, _t2iv: null
};

/* ═══════════════════════════════════════
   QUESTION BANK
═══════════════════════════════════════ */
const QB = [
  {
    type:'함의 추론', score:'2점', topic:'경제', qNum:21,
    passage:'The concept of <span class="hl">cognitive load</span> theory, introduced by educational psychologist John Sweller, suggests that the human brain has a limited capacity for processing information simultaneously. When learners are presented with overly complex material, their working memory becomes <span class="hl">overwhelmed</span>, leading to reduced comprehension and retention. Therefore, effective instructional design must break down complex information into manageable chunks, allowing students to build understanding progressively.',
    stem:'다음 글에서 필자가 주장하는 바로 가장 적절한 것은?',
    choices:['학습자의 인지 능력은 개인차가 없다','교육 설계는 정보를 단계적으로 제시해야 한다','복잡한 정보는 한 번에 제시해야 효율적이다','학습 내용을 분할하면 이해와 기억이 향상된다','작업 기억은 훈련으로 무한히 늘릴 수 있다'],
    answer:3,
    trans_prompt:'다음 영어 지문을 한국어로 정밀하게 번역하고, 정답 타겟팅 근거를 설명하세요. 지문: The concept of cognitive load theory suggests the brain has limited capacity...',
    parseHtml:'<span class="p-s">The concept of cognitive load theory</span><span class="p-v"> suggests</span><span class="p-o"> that the human brain has a limited capacity</span><span class="p-adv"> for processing information simultaneously</span>.',
    parseRows:[['S','The concept of cognitive load theory','명사구 주어'],['V','suggests','현재 단순 타동사'],['O','that the human brain has a limited capacity','that-절 목적어'],['ADV','for processing information simultaneously','전치사구 (방법)']],
    voca:[['cognitive','adj.','인지의'],['overwhelmed','adj.','압도된'],['retention','n.','기억력'],['instructional','adj.','교수의'],['progressively','adv.','점진적으로']],
    rationale:'정답 <b>④</b> — "break down complex information into manageable chunks"가 핵심 근거. 복잡한 정보를 분할하여 단계적으로 이해시키는 것이 필자의 주장.'
  },
  {
    type:'빈칸 추론', score:'3점', topic:'과학', qNum:31,
    passage:'Recent studies in neuroscience have revealed that the <span class="hl">neuroplasticity</span> of the adult brain is far greater than previously assumed. Contrary to earlier beliefs, contemporary research demonstrates that neural pathways can be reshaped through sustained practice. This discovery has profound implications, suggesting that <span class="blank-fill"></span>.',
    stem:'다음 빈칸에 들어갈 말로 가장 적절한 것은?',
    choices:['early childhood is the only critical period','the adult brain retains capacity for structural change','neural pathways are fixed after adolescence','rehabilitation has limited effectiveness','cognitive decline is inevitable'],
    answer:1,
    trans_prompt:'다음 영어 지문을 한국어로 번역하고 빈칸 추론의 근거를 설명하세요.',
    parseHtml:'<span class="p-s">Recent studies in neuroscience</span><span class="p-v"> have revealed</span><span class="p-o"> that the neuroplasticity of the adult brain is far greater</span><span class="p-adv"> than previously assumed</span>.',
    parseRows:[['S','Recent studies in neuroscience','명사구 주어'],['V','have revealed','현재완료 타동사'],['O','that the neuroplasticity... is far greater','that-절 목적어'],['ADV','than previously assumed','비교 부사절']],
    voca:[['neuroplasticity','n.','신경가소성'],['sustained','adj.','지속적인'],['deliberate','adj.','의도적인'],['rehabilitation','n.','재활'],['profound','adj.','심오한']],
    rationale:'정답 <b>②</b> — 지문 전체가 성인 뇌의 변화 가능성을 주장. "the adult brain retains capacity for significant structural change"가 자연스럽게 연결.'
  },
  {
    type:'내용 일치', score:'2점', topic:'환경', qNum:22,
    passage:'The Amazon rainforest, often called the "lungs of the Earth," produces approximately <span class="hl">20%</span> of the world\'s oxygen and is home to an estimated <span class="hl">10%</span> of all species on Earth. The forest spans nine countries, with Brazil containing the largest portion at approximately 60%. Annual deforestation rates have been a growing concern, with scientists warning of a tipping point beyond which recovery may be impossible.',
    stem:'다음 글의 내용과 일치하는 것은?',
    choices:['아마존은 지구 산소의 약 30%를 생산한다','아마존에는 지구 전체 종의 약 10%가 서식한다','아마존은 10개 국가에 걸쳐 있다','브라질은 아마존의 약 70%를 차지한다','현재 회복은 이미 불가능하다'],
    answer:1,
    trans_prompt:'아마존 관련 지문을 한국어로 번역하고 내용 일치 정답 근거를 설명하세요.',
    parseHtml:'<span class="p-s">The Amazon rainforest</span><span class="p-v"> produces</span><span class="p-o"> approximately 20% of the world\'s oxygen</span><span class="p-adv"> and supports unprecedented biodiversity</span>.',
    parseRows:[['S','The Amazon rainforest','명사구 주어'],['V','produces','현재 단순 타동사'],['O','approximately 20% of the world\'s oxygen','명사구 목적어'],['ADV','and supports biodiversity','등위 접속사 구']],
    voca:[['approximately','adv.','약, 대략'],['deforestation','n.','삼림 벌채'],['tipping point','n.','임계점'],['span','v.','걸치다'],['portion','n.','부분']],
    rationale:'정답 <b>②</b> — "home to an estimated 10% of all species on Earth"가 직접 근거.'
  },
  {
    type:'글의 순서', score:'2점', topic:'심리', qNum:36,
    passage:'Research in behavioral economics has shown that humans are not purely rational decision-makers. Instead, we are subject to <span class="hl">cognitive biases</span> that systematically influence our choices in predictable ways. These biases often lead us to make decisions that contradict our long-term interests.',
    stem:'주어진 글 다음에 이어질 글의 순서로 가장 적절한 것은?',
    choices:['(A)-(B)-(C)','(A)-(C)-(B)','(B)-(A)-(C)','(B)-(C)-(A)','(C)-(A)-(B)'],
    answer:2,
    trans_prompt:'행동경제학 관련 지문을 번역하고 순서 배열 근거를 설명하세요.',
    parseHtml:'<span class="p-s">Research in behavioral economics</span><span class="p-v"> has shown</span><span class="p-o"> that humans are not purely rational decision-makers</span>.',
    parseRows:[['S','Research in behavioral economics','명사구 주어'],['V','has shown','현재완료 타동사'],['O','that humans are not purely rational','that-절 목적어']],
    voca:[['behavioral','adj.','행동의'],['cognitive','adj.','인지의'],['bias','n.','편향'],['systematically','adv.','체계적으로'],['contradict','v.','모순되다']],
    rationale:'정답 <b>③</b> — (B)에서 구체적 예시 제시 후 (A)에서 결과 설명, (C)에서 결론 도출.'
  },
  {
    type:'문장 삽입', score:'3점', topic:'예술', qNum:38,
    passage:'Throughout history, art has served as a reflection of society\'s values and concerns. In times of social upheaval, artists often respond by creating works that challenge the existing order. <span class="hl">Contemporary art</span> continues this tradition by engaging with pressing issues of our time, from climate change to social justice.',
    stem:'글의 흐름으로 보아 주어진 문장이 들어가기에 가장 적절한 곳은?',
    choices:['①','②','③','④','⑤'],
    answer:2,
    trans_prompt:'예술과 사회 관련 지문을 번역하고 문장 삽입 위치의 근거를 설명하세요.',
    parseHtml:'<span class="p-s">Art</span><span class="p-v"> has served</span><span class="p-o"> as a reflection of society\'s values</span><span class="p-adv"> throughout history</span>.',
    parseRows:[['S','Art','명사 주어'],['V','has served','현재완료 자동사'],['O','as a reflection of society\'s values','전치사구 서술어'],['ADV','throughout history','전치사구 부사']],
    voca:[['upheaval','n.','격변'],['contemporary','adj.','현대의'],['pressing','adj.','긴박한'],['reflection','n.','반영'],['challenge','v.','도전하다']],
    rationale:'정답 <b>③</b> — 주어진 문장이 앞의 역사적 예시와 뒤의 현대적 결론을 자연스럽게 연결.'
  }
];

const T1_STEPS=['원문 소재 분석 중','유형 매핑 중','BB 엔진 지문 창작 중','문항·선지 생성 중','해설 패키지 빌드 중','시험지 세트 구성 중','PDF 렌더링 완료'];
const T2_STEPS=['지문 분석 완료','핵심 문장 추출 완료','NLP 파싱 완료','S/V/O/C 성분 분석 완료','distractor 생성 완료','문항 생성 완료','시험지 세트 반영 완료'];
const STATUS_CLR={'생성 완료':'var(--teal)','검수 필요':'var(--amber)','편집 중':'#aa80ff','검수 완료':'var(--teal)'};

/* ── examSet factory ── */
function mkSet(engine, grade, diff, types, qcnt) {
  const qs = Array.from({length: qcnt}, (_, i) => {
    const b = QB[i % QB.length];
    return {
      id: 'Q_' + Date.now() + '_' + i,
      no: 18 + i, type: b.type, score: b.score, topic: b.topic,
      passage: b.passage, stem: b.stem, choices: [...b.choices],
      answer: b.answer, trans_prompt: b.trans_prompt,
      parseHtml: b.parseHtml, parseRows: b.parseRows,
      voca: b.voca, rationale: b.rationale,
      status: i < 2 ? '검수 필요' : '생성 완료',
      engine,
      createdAt: new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit',second:'2-digit'})
    };
  });
  return {
    id: 'SET_' + Date.now(),
    title: grade + ' ' + diff + ' 실전모의고사',
    engine, grade, diff, types,
    questions: qs,
    createdAt: new Date().toISOString()
  };
}

/* ═══════════════════════════════════════
   NAV & COMMON UI
═══════════════════════════════════════ */
function goNav(btn, id) {
  document.querySelectorAll('.ntab').forEach(b => b.classList.remove('on'));
  document.querySelectorAll('.page').forEach(p => p.classList.remove('on'));
  btn.classList.add('on'); document.getElementById(id).classList.add('on');
  if (id === 'p-storage') renderStore();
}
function sel(el, row) {
  document.getElementById(row).querySelectorAll('.gb').forEach(b => b.classList.remove('on'));
  el.classList.add('on');
}
function tc(el, cls) {
  const chips = el.closest('.chips').querySelectorAll('.chip.on');
  if (el.classList.contains('on') && chips.length <= 1) { toast('최소 1개 선택 필요'); return; }
  el.classList.toggle('on');
}
function oTab(btn, id) {
  const pane = btn.closest('.pane');
  pane.querySelectorAll('.otab').forEach(b => b.classList.remove('on'));
  pane.querySelectorAll('.opanel').forEach(p => p.classList.remove('on'));
  btn.classList.add('on'); document.getElementById(id).classList.add('on');
}
function oTab2(btn, id) { oTab(btn, id); }

/* ═══════════════════════════════════════
   T1 GENERATE
═══════════════════════════════════════ */
function t1Gen() {
  clearInterval(S._t1iv);
  const btn = document.getElementById('t1GenBtn'); btn.disabled = true;
  document.getElementById('t1Empty').style.display = 'none';
  document.getElementById('t1Result').style.display = 'none';
  document.getElementById('t1SC').style.display = 'none';
  const gs = document.getElementById('t1GenState'); gs.classList.add('on');

  const grade = document.getElementById('gradeRow').querySelector('.on').textContent;
  const diff = document.getElementById('diffRow').querySelector('.on').textContent;
  const types = [...document.getElementById('typeChips').querySelectorAll('.chip.on')].map(c => c.textContent);
  const qty = parseInt(document.getElementById('qtyRow').querySelector('.on').textContent) || 3;
  const qcnt = parseInt(document.getElementById('qcntRow').querySelector('.on').textContent) || 20;

  document.getElementById('t1Steps').innerHTML = T1_STEPS.map((s,i) =>
    `<div class="step-row" id="t1s${i}"><div class="step-dot"></div><span>${s}</span></div>`
  ).join('');
  document.getElementById('t1P').style.width = '0%';

  let p = 0, si = 0;
  S._t1iv = setInterval(() => {
    p = Math.min(p + Math.round(8 + Math.random() * 10), 100);
    document.getElementById('t1P').style.width = p + '%';
    document.getElementById('t1Pct').textContent = p + '%';
    const ns = Math.min(Math.floor(p / (100 / T1_STEPS.length)), T1_STEPS.length - 1);
    if (ns !== si) { document.getElementById('t1s'+si)?.classList.add('done'); si = ns; document.getElementById('t1s'+si)?.classList.add('active'); document.getElementById('t1GS').textContent = T1_STEPS[si]; }
    document.getElementById('t1GL').textContent = p + '% 완료';
    if (p >= 100) {
      clearInterval(S._t1iv);
      T1_STEPS.forEach((_,i) => document.getElementById('t1s'+i)?.classList.add('done'));
      setTimeout(() => { gs.classList.remove('on'); doRenderT1(grade, diff, types, qty, qcnt); btn.disabled = false; }, 350);
    }
  }, 140);
}

function doRenderT1(grade, diff, types, qty, qcnt) {
  const sets = Array.from({length: qty}, (_, i) => {
    const s = mkSet('T1 BB 창작 엔진', grade, diff, types, qcnt);
    s.title = grade + ' ' + diff + ' 실전모의고사 ' + (i+1) + '회';
    return s;
  });
  S.examSets = [...S.examSets.filter(x => x.engine !== 'T1 BB 창작 엔진'), ...sets];
  S.t1Set = sets[0];

  document.getElementById('t1NT').textContent = `${qty}개 시험지 세트 생성 완료 — 총 ${qty * qcnt}문항 (4.8초) · BB 창작 엔진 v2.1`;
  document.getElementById('t1Result').style.display = 'block';
  document.getElementById('t1SC').style.display = 'block';

  renderT1SetSel(sets); renderSetSum('t1', sets[0]); renderQL('t1', sets[0].questions);
  selQ('t1', sets[0].questions[0]);
  document.getElementById('t1Result').scrollIntoView({behavior:'smooth', block:'start'});
}

function renderT1SetSel(sets) {
  document.getElementById('t1SS').innerHTML = sets.map((s,i) => `
    <div onclick="swSet(${i})" id="ss-${i}" style="padding:7px 10px;border-radius:var(--r);cursor:pointer;font-size:12px;border:0.5px solid ${i===0?'var(--accent)':'var(--border)'};background:${i===0?'rgba(79,127,255,.1)':'var(--c2)'};color:${i===0?'#7aaeff':'var(--c7)'};transition:all .15s">
      <div style="font-weight:${i===0?500:400}">${s.title}</div>
      <div style="font-size:10px;color:var(--c6);margin-top:1px;font-family:'IBM Plex Mono',monospace">${s.questions.length}문항 · 검수필요 ${s.questions.filter(q=>q.status==='검수 필요').length}개</div>
    </div>`).join('');
}
function swSet(i) {
  const sets = S.examSets.filter(x => x.engine === 'T1 BB 창작 엔진');
  if (!sets[i]) return;
  S.t1Set = sets[i];
  sets.forEach((_,j) => {
    const el = document.getElementById('ss-'+j); if (!el) return;
    const on = j === i;
    el.style.borderColor = on ? 'var(--accent)' : 'var(--border)';
    el.style.background = on ? 'rgba(79,127,255,.1)' : 'var(--c2)';
    el.style.color = on ? '#7aaeff' : 'var(--c7)';
  });
  renderSetSum('t1', sets[i]); renderQL('t1', sets[i].questions); selQ('t1', sets[i].questions[0]);
}

function renderSetSum(which, set) {
  const tc = {};
  set.questions.forEach(q => { tc[q.type] = (tc[q.type]||0)+1; });
  document.getElementById(which+'SG').innerHTML = `
    <div class="si"><div class="si-v">${set.questions.length}</div><div class="si-l">총 문항</div></div>
    <div class="si"><div class="si-v">${set.questions.filter(q=>q.status==='검수 필요').length}</div><div class="si-l">검수 필요</div></div>
    <div class="si"><div class="si-v">${set.questions.length}</div><div class="si-l">편집 가능</div></div>`;
  document.getElementById(which+'TB').innerHTML = Object.entries(tc).map(([t,n]) =>
    `<div class="tb-row"><span style="color:var(--c7)">${t}</span><span style="font-weight:500;color:var(--c9);font-family:'IBM Plex Mono',monospace">${n}</span></div>`).join('');
}

/* ═══════════════════════════════════════
   Q LIST / DETAIL
═══════════════════════════════════════ */
function getQs(which) { return which==='t1' ? S.t1Set?.questions||[] : S.t2Set?.questions||[]; }

function renderQL(which, qs) {
  document.getElementById(which+'QL').innerHTML = qs.map((q,i) => `
    <div class="qitem${i===0?' on':''}" id="qi-${which}-${q.id}" onclick="selQ('${which}',null,'${q.id}')" draggable="true" ondragstart="dS(event,'${which}','${q.id}')" ondragover="event.preventDefault()" ondrop="dD(event,'${which}','${q.id}')">
      <span class="drag-h">⠿</span>
      <div class="qnum-b">${q.no}</div>
      <div class="qi-info">
        <div class="qi-type">${q.type}</div>
        <div class="qi-meta">${q.score} · ${q.topic}</div>
      </div>
      <div class="qi-dot" style="background:${STATUS_CLR[q.status]||'var(--c5)'}"></div>
    </div>`).join('');
}

function selQ(which, qObj, qId) {
  const qs = getQs(which);
  const q = qObj || qs.find(x => x.id === qId);
  if (!q) return;
  S.selQ = q;
  document.querySelectorAll(`#${which}QL .qitem`).forEach(el => el.classList.remove('on'));
  document.getElementById(`qi-${which}-${q.id}`)?.classList.add('on');
  which === 't1' ? renderT1Detail(q) : renderT2Detail(q);
}

function renderT1Detail(q) {
  document.getElementById('t1DT').textContent = `${q.no}번 — ${q.type}`;
  document.getElementById('t1DS').textContent = q.score;
  document.getElementById('t1Pass').innerHTML = q.passage;
  document.getElementById('t1QN').textContent = `${q.no}번. 다음 글을 읽고 물음에 답하시오.`;
  document.getElementById('t1QS').textContent = q.stem;

  const cl = document.getElementById('t1CH');
  cl.innerHTML = ''; document.getElementById('t1FB').innerHTML = '';
  q.choices.forEach((c, i) => {
    const d = document.createElement('div'); d.className = 'choice';
    d.innerHTML = `<div class="cnum">${i+1}</div><span class="choice-text" contenteditable="true" spellcheck="false">${c}</span>`;
    d.onclick = e => { if (e.target === d || e.target.classList.contains('cnum')) pickQ(d, i, q, 't1'); };
    cl.appendChild(d);
  });

  document.getElementById('transStream').textContent = 'AI 해설 생성 버튼을 눌러주세요.';
  document.getElementById('t1Rat').innerHTML = q.rationale;

  // parse
  document.getElementById('t1PB').innerHTML = q.parseHtml;
  const tm = {S:'atag-s',V:'atag-v',O:'atag-o',ADV:'atag-adv'};
  document.getElementById('t1PD').innerHTML = q.parseRows.map(r =>
    `<div class="arow"><span class="atag ${tm[r[0]]||'atag-s'}">${r[0]}</span><span class="aval">${r[1]}</span><span class="anote">${r[2]}</span></div>`).join('');

  // voca
  const vt = document.getElementById('t1VT');
  vt.innerHTML = `<thead style="background:var(--c3)"><tr>${['#','단어','품사','뜻 (입력 후 Enter)'].map(h=>`<th style="padding:5px 8px;text-align:left;font-size:11px;color:var(--c6);border-bottom:0.5px solid var(--border);font-family:'IBM Plex Mono',monospace">${h}</th>`).join('')}</tr></thead>`;
  const tb = document.createElement('tbody');
  q.voca.forEach((v, i) => {
    const tr = document.createElement('tr');
    tr.innerHTML = `<td style="padding:5px 8px;color:var(--c6);border-bottom:0.5px solid var(--border);font-family:'IBM Plex Mono',monospace">${i+1}</td><td style="padding:5px 8px;font-weight:500;border-bottom:0.5px solid var(--border);color:var(--c9)">${v[0]}</td><td style="padding:5px 8px;color:var(--c6);border-bottom:0.5px solid var(--border)">${v[1]}</td><td style="padding:5px 8px;border-bottom:0.5px solid var(--border)"><input type="text" placeholder="뜻을 입력하세요" data-ans="${v[2]}" style="width:100%;border:none;border-bottom:0.5px solid var(--border2);background:transparent;font-size:12px;padding:2px 4px;font-family:inherit;color:var(--c8)" onkeydown="chkV(event,this)"></td>`;
    tb.appendChild(tr);
  });
  vt.appendChild(tb);

  // log
  const now = new Date();
  document.getElementById('t1Log').innerHTML = T1_STEPS.map((step,i) => {
    const t = new Date(now - (T1_STEPS.length-i)*700);
    return `<div class="log-e"><span class="log-t">${t.toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit',second:'2-digit'})}</span><span class="pill ${i===T1_STEPS.length-1?'pill-teal':'pill-blue'}" style="font-size:10px;flex-shrink:0">${i===T1_STEPS.length-1?'완료':'처리'}</span><span class="log-m">${step} — Q${q.no} ${q.type}</span></div>`;
  }).join('');

  // criteria
  document.getElementById('t1Crit').innerHTML = `
    <div class="cfg-grid" style="margin-bottom:10px">
      <div class="cfg-item"><span class="cfg-k">문항</span><span class="cfg-v">${q.no}번</span></div>
      <div class="cfg-item"><span class="cfg-k">유형</span><span class="cfg-v">${q.type}</span></div>
      <div class="cfg-item"><span class="cfg-k">배점</span><span class="cfg-v">${q.score}</span></div>
      <div class="cfg-item"><span class="cfg-k">토픽</span><span class="cfg-v">${q.topic}</span></div>
      <div class="cfg-item"><span class="cfg-k">엔진</span><span class="cfg-v">${q.engine}</span></div>
      <div class="cfg-item"><span class="cfg-k">상태</span><span class="cfg-v">${q.status}</span></div>
    </div>
    <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:6px;font-family:'IBM Plex Mono',monospace">REVIEW CHECKLIST [SCR-002]</div>
    ${['지문 난이도 적절성','선지 매력도 균형','정답 근거 명확성','어법 오류 없음','배점 적절성'].map(item =>
      `<label style="display:flex;align-items:center;gap:8px;font-size:12px;cursor:pointer;padding:3px 0;color:var(--c7)"><input type="checkbox" style="accent-color:var(--teal)"><span>${item}</span></label>`).join('')}`;

  // reset tabs
  const ot = document.getElementById('t1OT');
  ot.querySelectorAll('.otab').forEach(b=>b.classList.remove('on'));
  ot.querySelectorAll('.opanel').forEach(p=>p.classList.remove('on'));
  ot.querySelectorAll('button')[0].classList.add('on');
  document.getElementById('ot-q').classList.add('on');
}

/* ── AI 해설 생성 (Anthropic API streaming) ── */
async function genTrans() {
  const q = S.selQ;
  if (!q) { toast('문항을 먼저 선택해 주세요'); return; }

  const el = document.getElementById('transStream');
  el.innerHTML = 'AI 해설 생성 중<div class="typing-dots"><span></span><span></span><span></span></div>';

  const prompt = `당신은 수능 영어 전문 출제 강사입니다. 다음 영어 지문을 한국어로 정밀하게 번역하고, 정답(${q.answer+1}번 선지)에 대한 타겟팅 근거를 명확하게 설명해 주세요.

[지문]
${q.passage.replace(/<[^>]+>/g,'')}

[문항 유형]: ${q.type}
[정답]: ${q.answer+1}번 — "${q.choices[q.answer]}"

출력 형식:
1. 한글 번역 (정밀하게)
2. 정답 타겟팅 근거 (핵심 어구 중심으로)
3. 오답 소거 논리 (간략히)`;

  try {
    const res = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: {'Content-Type':'application/json'},
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 1000,
        stream: true,
        messages: [{role:'user', content: prompt}]
      })
    });

    el.textContent = '';
    const reader = res.body.getReader();
    const decoder = new TextDecoder();
    let buf = '';

    while(true) {
      const {done, value} = await reader.read();
      if (done) break;
      buf += decoder.decode(value, {stream:true});
      const lines = buf.split('\n');
      buf = lines.pop();
      for (const line of lines) {
        if (!line.startsWith('data: ')) continue;
        const data = line.slice(6).trim();
        if (data === '[DONE]') continue;
        try {
          const j = JSON.parse(data);
          if (j.type === 'content_block_delta' && j.delta?.text) {
            el.textContent += j.delta.text;
            el.scrollTop = el.scrollHeight;
          }
        } catch {}
      }
    }
    toast('AI 해설 생성 완료');
  } catch(e) {
    // fallback mock
    const mockText = `[한글 번역]\n${q.passage.replace(/<[^>]+>/g,'').slice(0,80)}...\n\n교육심리학자 John Sweller가 제안한 인지 부하 이론은, 인간의 뇌가 정보를 동시에 처리하는 능력에 한계가 있다고 제안합니다.\n\n[정답 타겟팅 근거]\n정답 ${q.answer+1}번: "${q.choices[q.answer]}"\n핵심 근거: ${q.rationale.replace(/<[^>]+>/g,'')}`;
    await typeText(el, mockText);
  }
}

async function typeText(el, text) {
  el.textContent = '';
  for (const ch of text) {
    el.textContent += ch;
    el.scrollTop = el.scrollHeight;
    await new Promise(r => setTimeout(r, 12));
  }
}

/* ── Q 인터랙션 ── */
function pickQ(el, idx, q, which) {
  const cl = el.closest('.choices');
  if (cl.querySelector('.correct')) return;
  cl.querySelectorAll('.choice').forEach(c => c.classList.add('locked'));
  const fbId = which + 'FB';
  if (idx === q.answer) {
    el.classList.add('correct');
    document.getElementById(fbId).innerHTML = `<div class="notif notif-teal"><svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24" style="flex-shrink:0"><polyline points="20 6 9 17 4 12"/></svg><span>정답! ${q.rationale}</span></div>`;
  } else {
    el.classList.add('wrong');
    cl.querySelectorAll('.choice')[q.answer].classList.add('correct');
    document.getElementById(fbId).innerHTML = `<div class="notif notif-amber"><svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" style="flex-shrink:0"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg><span>오답. ${q.rationale}</span></div>`;
  }
}

function chkV(e, input) {
  if (e.key !== 'Enter') return;
  const ans = input.dataset.ans; const val = input.value.trim();
  if (!val) return;
  const ok = ans.includes(val.slice(0,2)) || val.includes(ans.slice(0,2));
  input.style.color = ok ? 'var(--teal)' : 'var(--red)';
  input.style.borderColor = ok ? 'var(--teal)' : 'var(--red)';
  toast(ok ? '정답: ' + ans : '오답. 정답: ' + ans);
  if (!ok) setTimeout(() => { input.style.color=''; input.style.borderColor=''; }, 1500);
}

/* ── Q 관리 ── */
function addQ(which) {
  const qs = getQs(which);
  const b = QB[qs.length % QB.length];
  const nq = {...b, id:'Q_'+Date.now(), no:qs.length+18, choices:[...b.choices], status:'생성 완료', engine:which==='t1'?'BB 창작 엔진':'레슨위드 NLP', createdAt:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit',second:'2-digit'})};
  qs.push(nq);
  renderQL(which, qs);
  if (which==='t1' && S.t1Set) renderSetSum('t1', S.t1Set);
  if (which==='t2' && S.t2Set) renderSetSum('t2', S.t2Set);
  selQ(which, nq);
  toast('문항 추가됨 — ' + nq.type);
}

function regenQ(which) {
  const q = S.selQ; if (!q) return;
  const qs = getQs(which); const idx = qs.indexOf(q); if (idx < 0) return;
  const b = QB[(idx+1) % QB.length];
  Object.assign(q, {...b, id:q.id, no:q.no, choices:[...b.choices], engine:q.engine, createdAt:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit',second:'2-digit'})});
  renderQL(which, qs); selQ(which, q);
  toast('문항 재생성됨');
}

function delQ(which) {
  const q = S.selQ; if (!q) return;
  const qs = getQs(which); const idx = qs.indexOf(q);
  if (idx < 0 || qs.length <= 1) { toast('최소 1개 문항 필요'); return; }
  qs.splice(idx, 1); qs.forEach((q,i) => { q.no = 18+i; });
  renderQL(which, qs);
  if (which==='t1' && S.t1Set) renderSetSum('t1', S.t1Set);
  selQ(which, qs[Math.min(idx, qs.length-1)]);
  toast('문항 삭제됨');
}

/* ── DRAG REORDER ── */
let _dId=null, _dW=null;
function dS(e, w, id) { _dId=id; _dW=w; e.currentTarget.classList.add('dragging'); }
function dD(e, w, tid) {
  e.preventDefault(); if (!_dId || _dW !== w) return;
  const qs = getQs(w);
  const fi = qs.findIndex(q=>q.id===_dId), ti = qs.findIndex(q=>q.id===tid);
  if (fi<0||ti<0||fi===ti) return;
  const [m] = qs.splice(fi,1); qs.splice(ti,0,m);
  qs.forEach((q,i)=>{q.no=18+i;});
  renderQL(w,qs); _dId=null; toast('순서 변경됨');
}

/* ═══════════════════════════════════════
   T2 GENERATE
═══════════════════════════════════════ */
function swMode(m) {
  document.getElementById('mFile').classList.toggle('on', m==='file');
  document.getElementById('mText').classList.toggle('on', m==='text');
  document.getElementById('modeFile').style.display = m==='file'?'':'none';
  document.getElementById('modeText').style.display = m==='text'?'':'none';
  document.getElementById('t2Result').style.display = 'none';
}

let uploadedFiles = [];
function hFI(files) { [...files].forEach(f=>addFile(f)); }
function hDrop(e) { e.preventDefault(); document.getElementById('dz').classList.remove('drag'); hFI(e.dataTransfer.files); }

function addFile(file) {
  if (uploadedFiles.length>=50) { toast('최대 50개'); return; }
  const ext = file.name.split('.').pop().toUpperCase();
  if (!['PDF','HWP','DOCX'].includes(ext)) { toast(file.name+' — 미지원 형식'); return; }
  if (file.size>20*1024*1024) { toast('20MB 초과'); return; }
  const item = {id:Date.now()+Math.random(), name:file.name, size:(file.size/1024/1024).toFixed(1)+' MB', ext, progress:0};
  uploadedFiles.push(item); renderFL();
  let p=0; const iv=setInterval(()=>{ p=Math.min(p+Math.round(12+Math.random()*15),100); item.progress=p; renderFL(); if(p>=100)clearInterval(iv); },90);
}

function renderFL() {
  const fl=document.getElementById('flist'); if(!uploadedFiles.length){fl.innerHTML='';return;}
  fl.innerHTML=uploadedFiles.map(f=>`
    <div class="fitem">
      <svg width="12" height="12" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24" style="opacity:.5;flex-shrink:0"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
      <div style="flex:1;min-width:0">
        <div style="display:flex;align-items:center;gap:5px"><span class="fname">${f.name}</span><span style="font-size:10px;padding:1px 5px;border-radius:8px;background:var(--c3);color:var(--c6);font-family:'IBM Plex Mono',monospace">${f.ext}</span><span style="font-size:10px;color:var(--c6)">${f.size}</span></div>
        ${f.progress<100?`<div style="height:2px;background:var(--c3);border-radius:1px;overflow:hidden;margin-top:4px"><div style="height:100%;width:${f.progress}%;background:var(--teal);border-radius:1px;transition:width .3s"></div></div>`:`<div style="font-size:10px;color:var(--teal);margin-top:2px;font-family:'IBM Plex Mono',monospace">✓ 파싱 완료</div>`}
      </div>
      <button class="fdel" onclick="rmFile('${f.id}')">×</button>
    </div>`).join('');
}
function rmFile(id) { uploadedFiles=uploadedFiles.filter(f=>String(f.id)!==String(id)); renderFL(); if(!uploadedFiles.length)document.getElementById('t2Result').style.display='none'; }

function loadEx() {
  document.getElementById('txtIn').value=`The Amazon rainforest produces approximately 20% of the world's oxygen and is home to an estimated 10% of all species on Earth. The forest spans nine countries, with Brazil containing the largest portion at approximately 60%.

Cognitive load theory, introduced by John Sweller, suggests that the human brain has a limited capacity for processing information. Effective instructional design must break down complex information into manageable units.

Recent neuroscience research reveals that the adult brain retains remarkable plasticity. Neural pathways continue to adapt in response to new experiences.`;
  upMeta(); toast('예시 지문 3개 입력됨');
}
function clrTxt() { document.getElementById('txtIn').value=''; upMeta(); document.getElementById('t2Result').style.display='none'; }
function upMeta() {
  const v=document.getElementById('txtIn').value;
  const cnt=v.trim()?v.split(/\n\s*\n/).filter(s=>s.trim().length>20).length:0;
  document.getElementById('t2ML').textContent=v.trim()?`지문 ${Math.max(cnt,1)}개`:'';
  document.getElementById('t2MR').textContent=v.trim()?v.length.toLocaleString()+'자':'';
}

function t2Gen() {
  const isFile = document.getElementById('modeFile').style.display!=='none';
  if(isFile&&!uploadedFiles.some(f=>f.progress>=100)){toast('파일을 먼저 업로드해 주세요');return;}
  if(!isFile&&document.getElementById('txtIn').value.trim().length<20){toast('지문 텍스트를 입력해 주세요');return;}

  clearInterval(S._t2iv);
  const btn=document.getElementById('t2GenBtn'); btn.disabled=true;
  document.getElementById('t2Result').style.display='none';
  document.getElementById('t2SC').style.display='none';
  const gs=document.getElementById('t2GS'); gs.classList.add('on');

  const grade=document.getElementById('t2GR').querySelector('.on').textContent;
  const diff=document.getElementById('t2DR').querySelector('.on').textContent;
  const passCount=isFile?uploadedFiles.filter(f=>f.progress>=100).length:Math.max(document.getElementById('txtIn').value.split(/\n\s*\n/).filter(s=>s.trim().length>20).length,1);
  const qcnt=passCount*4;

  document.getElementById('t2Steps').innerHTML=T2_STEPS.map((s,i)=>`<div class="step-row" id="t2s${i}"><div class="step-dot"></div><span>${s}</span></div>`).join('');
  document.getElementById('t2P').style.width='0%';

  let p=0,si=0;
  S._t2iv=setInterval(()=>{
    p=Math.min(p+Math.round(7+Math.random()*9),100);
    document.getElementById('t2P').style.width=p+'%';
    document.getElementById('t2Pct').textContent=p+'%';
    const ns=Math.min(Math.floor(p/(100/T2_STEPS.length)),T2_STEPS.length-1);
    if(ns!==si){document.getElementById('t2s'+si)?.classList.add('done');si=ns;document.getElementById('t2s'+si)?.classList.add('active');document.getElementById('t2GSub').textContent=T2_STEPS[si];}
    document.getElementById('t2GL').textContent=p+'% 완료';
    if(p>=100){clearInterval(S._t2iv);T2_STEPS.forEach((_,i)=>document.getElementById('t2s'+i)?.classList.add('done'));setTimeout(()=>{gs.classList.remove('on');doRenderT2(grade,diff,passCount,qcnt);btn.disabled=false;},350);}
  },160);
}

function doRenderT2(grade, diff, passCount, qcnt) {
  // examSet 생성 후 state에 등록
  const set = mkSet('T2 레슨위드 NLP', grade, diff, ['내용 일치','빈칸 추론','글의 순서','문장 삽입'], qcnt);
  set.title = grade + ' ' + diff + ' 변형 문제 세트';
  S.t2Set = set;
  S.examSets = [...S.examSets.filter(x=>x.engine!=='T2 레슨위드 NLP'), set];

  document.getElementById('t2NT').textContent=`${passCount}개 지문 처리 완료 — ${qcnt}문항 (수능형 11종 + 내신형 7종 + S/V/O/C 파싱 리포트) [28종 패키지]`;
  document.getElementById('t2Result').style.display='block';
  document.getElementById('t2SC').style.display='block';

  // 문항 목록 렌더
  renderQL('t2', set.questions);
  renderSetSum('t2', set);

  // 구문 파싱 패널 [SCR-007 독점]
  document.getElementById('t2PC').innerHTML=`
    <div style="font-size:12px;color:var(--c7);margin-bottom:8px;font-family:'IBM Plex Mono',monospace">지문 1 / ${passCount}개</div>
    <div class="parse-block"><span class="p-s">The Amazon rainforest</span><span class="p-v"> produces</span><span class="p-o"> approximately 20% of the world's oxygen</span><span class="p-adv"> and supports unprecedented biodiversity</span>.</div>
    <div style="display:flex;gap:8px;flex-wrap:wrap;margin-bottom:10px">
      <span class="pleg"><span class="pleg-dot" style="background:rgba(79,127,255,.4)"></span>S 주어</span>
      <span class="pleg"><span class="pleg-dot" style="background:rgba(255,79,106,.4)"></span>V 동사</span>
      <span class="pleg"><span class="pleg-dot" style="background:rgba(30,203,138,.4)"></span>O 목적어</span>
      <span class="pleg"><span class="pleg-dot" style="background:rgba(245,166,35,.4)"></span>ADV 부사</span>
    </div>
    <div class="arow"><span class="atag atag-s">S</span><span class="aval">The Amazon rainforest</span><span class="anote">명사구 주어</span></div>
    <div class="arow"><span class="atag atag-v">V</span><span class="aval">produces</span><span class="anote">현재 단순 타동사</span></div>
    <div class="arow"><span class="atag atag-o">O</span><span class="aval">approximately 20% of the world's oxygen</span><span class="anote">명사구 목적어</span></div>
    <div class="arow"><span class="atag atag-adv">ADV</span><span class="aval">and supports unprecedented biodiversity</span><span class="anote">등위 접속사 + 동사구</span></div>`;

  // T2 AI 로그
  const now=new Date();
  document.getElementById('t2Log').innerHTML=T2_STEPS.map((step,i)=>{
    const t=new Date(now-(T2_STEPS.length-i)*680);
    return `<div class="log-e"><span class="log-t">${t.toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit',second:'2-digit'})}</span><span class="pill ${i===T2_STEPS.length-1?'pill-teal':'pill-blue'}" style="font-size:10px;flex-shrink:0">${i===T2_STEPS.length-1?'완료':'처리'}</span><span class="log-m">${step}</span></div>`;
  }).join('');

  // 첫 문항 선택
  selQ('t2', set.questions[0]);

  const rb=document.getElementById('t2RB');
  rb.className='review-btn';
  rb.innerHTML='<svg width="11" height="11" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg> ★ NE 저자 검수 요청 [SCR-002]';

  document.getElementById('t2Result').scrollIntoView({behavior:'smooth',block:'start'});
}

function renderT2Detail(q) {
  document.getElementById('t2DT').textContent=`${q.no}번 — ${q.type}`;
  document.getElementById('t2DS').textContent=q.score;
  document.getElementById('t2Pass').innerHTML=q.passage;
  document.getElementById('t2QN').textContent=`${q.no}번. ${q.stem}`;

  const cl=document.getElementById('t2CH'); cl.innerHTML=''; document.getElementById('t2FB').innerHTML='';
  q.choices.forEach((c,i)=>{
    const d=document.createElement('div'); d.className='choice';
    d.innerHTML=`<div class="cnum">${i+1}</div><span class="choice-text" contenteditable="true" spellcheck="false">${c}</span>`;
    d.onclick=e=>{if(e.target===d||e.target.classList.contains('cnum'))pickQ(d,i,q,'t2');};
    cl.appendChild(d);
  });
  document.getElementById('t2QE').style.display='none';
  document.getElementById('t2QD').style.display='block';

  const ot=document.getElementById('t2OT');
  ot.querySelectorAll('.otab').forEach(b=>b.classList.remove('on'));
  ot.querySelectorAll('.opanel').forEach(p=>p.classList.remove('on'));
  ot.querySelectorAll('button')[0].classList.add('on');
  document.getElementById('t2-q').classList.add('on');
}

function cancelGen(w){
  if(w==='t1'){clearInterval(S._t1iv);document.getElementById('t1GenState').classList.remove('on');document.getElementById('t1Empty').style.display='';document.getElementById('t1GenBtn').disabled=false;}
  else{clearInterval(S._t2iv);document.getElementById('t2GS').classList.remove('on');document.getElementById('t2GenBtn').disabled=false;}
}

/* ═══════════════════════════════════════
   PDF — 시험지 전용 렌더러 [수정사항 반영]
═══════════════════════════════════════ */
function buildPDF(set, brand) {
  if (!set) return '<p style="color:#999">생성된 시험지가 없습니다.</p>';
  const title = brand ? brand + ' — ' + set.title : set.title;
  const qs = set.questions;
  return `
    <div class="pdf-hd">
      <div class="pdf-ttl">${title}</div>
      <div class="pdf-sub">${set.grade} · ${set.diff} · ${new Date().toLocaleDateString('ko-KR')} 생성 · ${qs.length}문항</div>
    </div>
    ${qs.map(q=>`
      <div class="pdf-q">
        <div class="pdf-qn">${q.no}. 다음 글을 읽고 물음에 답하시오. [${q.score}]</div>
        <div class="pdf-pass">${q.passage.replace(/<[^>]+>/g,'')}</div>
        <div class="pdf-stem">${q.stem}</div>
        <div>${q.choices.map((c,i)=>`<div class="pdf-ch">${'①②③④⑤'[i]} ${c}</div>`).join('')}</div>
        <div class="pdf-meta">유형: ${q.type} | 난이도: ${set.diff} | 토픽: ${q.topic} | 엔진: ${q.engine}</div>
      </div>`).join('')}
    <div class="pdf-ft">${title}</div>`;
}

function showPrint(which) {
  const set = which==='t1' ? S.t1Set : S.t2Set;
  const brand = document.getElementById('t1Brand')?.value.trim() || '';
  const html = buildPDF(set, brand);
  document.getElementById('printBox').innerHTML = html;
  document.getElementById('pdf-sheet').innerHTML = html;
  document.getElementById('printTitle').textContent = (set?.title||'시험지') + ' 출력 미리보기';
  openModal('modal-print');
}

function doPrint() {
  S.printCnt = (S.printCnt||0)+1;
  updStats(); closeModal('modal-print');
  setTimeout(()=>window.print(), 200);
}
function exportHWP() { toast('HWP 파일 생성 중... (서버 처리)'); }
function exportSec(n) { toast(n + ' PDF 생성 중...'); }
function exportVoca() {
  const q=S.selQ; if(!q)return;
  const txt=q.voca.map((v,i)=>`${i+1}. ${v[0]} (${v[1]}) — ${v[2]}`).join('\n');
  const a=document.createElement('a'); a.href='data:text/plain;charset=utf-8,'+encodeURIComponent(txt); a.download='어휘리스트.txt'; a.click();
  toast('어휘 리스트 다운로드 완료');
}

/* ═══════════════════════════════════════
   REVIEW [SCR-002]
═══════════════════════════════════════ */
function doReview(btnId) {
  const btn=document.getElementById(btnId);
  btn.className='review-btn done';
  btn.innerHTML='<svg width="11" height="11" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg> 검수 요청 완료 · 이메일 알림 발송';
  const which=btnId.startsWith('t1')?'T1 BB':'T2 NLP';
  const p=S.projects.find(x=>x.engine.includes(which));
  if(p){p.reviewed=true; updStats();}
  toast('★ NE 저자 검수 요청 접수 — 완료 시 시스템 알림 및 이메일 발송 [SCR-002]');
}

/* ═══════════════════════════════════════
   SAVE PROJECT [SCR-008]
═══════════════════════════════════════ */
function saveProj(which) {
  const set = which==='t1' ? S.t1Set : S.t2Set;
  if (!set) { toast('먼저 시험지를 생성해 주세요'); return; }
  const brand = document.getElementById('t1Brand')?.value.trim()||'';
  const proj = {
    id: Date.now(), title: set.title, engine: set.engine,
    grade: set.grade, diff: set.diff, brand,
    qCount: set.questions.length, sheets: 1,
    reviewed: false, fav: false,
    date: new Date().toLocaleDateString('ko-KR',{month:'2-digit',day:'2-digit'}),
    passText: set.questions[0]?.passage.replace(/<[^>]+>/g,'')||'',
    config: {grade:set.grade, diff:set.diff, types:set.types, engine:set.engine, lessonwith:which==='t2'},
    versions: [{v:'v1',label:'AI 자동 생성',date:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit'}),active:true}],
    examSetId: set.id
  };
  S.projects.unshift(proj);
  updStats(); updBadge();
  toast('보관함에 저장됨 — v1 생성 [SCR-008, SCR-009]');
}

/* ═══════════════════════════════════════
   STORAGE [SCR-008, SCR-009]
═══════════════════════════════════════ */
function updStats() {
  document.getElementById('st-t').textContent=S.projects.length;
  document.getElementById('st-q').textContent=S.projects.reduce((a,p)=>a+p.qCount,0);
  document.getElementById('st-r').textContent=S.projects.filter(p=>p.reviewed).length;
  document.getElementById('st-p').textContent=S.printCnt||0;
}
function updBadge() {
  const b=document.getElementById('navBadge');
  b.style.display=S.projects.length?'':'none';
  b.textContent=S.projects.length;
}

function renderStore() {
  const q=(document.getElementById('sSrch')?.value||'').toLowerCase();
  const g=document.getElementById('sGrd')?.value||'';
  const eng=document.getElementById('sEng')?.value||'';
  const rev=document.getElementById('sRev')?.value||'';
  const fav=document.getElementById('sFav')?.value||'';
  const list=S.projects.filter(p=>{
    if(q&&!p.title.toLowerCase().includes(q))return false;
    if(g&&p.grade!==g)return false;
    if(eng&&!p.engine.includes(eng.split(' ')[0]))return false;
    if(rev==='done'&&!p.reviewed)return false;
    if(rev==='wait'&&p.reviewed)return false;
    if(fav==='fav'&&!p.fav)return false;
    return true;
  });
  document.getElementById('clrAllBtn').style.display=S.projects.length?'':'none';
  updStats();
  const el=document.getElementById('storeList');
  if(!list.length){
    el.innerHTML=`<div class="card"><div class="empty"><svg width="40" height="40" fill="none" stroke="currentColor" stroke-width="1.1" viewBox="0 0 24 24"><path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z"/></svg><div class="empty-t">${S.projects.length===0?'저장된 프로젝트가 없습니다':'검색 결과 없음'}</div><div class="empty-s">${S.projects.length===0?'T1/T2에서 생성 후 보관함에 저장해 보세요':'조건을 바꿔보세요'}</div></div></div>`;
    return;
  }
  el.innerHTML=list.map(p=>`
    <div class="proj-row" id="pr-${p.id}">
      <div class="proj-head" onclick="togProj(${p.id})">
        <div class="proj-icon" style="background:${p.engine.includes('T1')?'rgba(79,127,255,.15)':'rgba(30,203,138,.12)'}">
          <svg width="14" height="14" fill="none" stroke="${p.engine.includes('T1')?'#7aaeff':'#4edda8'}" stroke-width="2" viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
        </div>
        <div class="proj-info">
          <div class="proj-title">${p.title}</div>
          <div class="proj-meta">${p.date} · ${p.engine} · ${p.qCount}문항${p.brand?' · '+p.brand:''}</div>
          <div class="proj-tags">
            <span class="ptag">${p.grade}</span><span class="ptag">${p.diff}</span>
            <span class="pill ${p.reviewed?'pill-teal':'pill-amber'}" style="font-size:10px;padding:1px 7px">${p.reviewed?'★ NE검수완료':'검수 대기'}</span>
            ${p.fav?'<span class="pill pill-amber" style="font-size:10px">★ 즐겨찾기</span>':''}
          </div>
        </div>
        <div style="display:flex;gap:4px;flex-shrink:0;align-items:center">
          <button class="btn btn-xs" onclick="event.stopPropagation();togFav(${p.id})">${p.fav?'★':'☆'}</button>
          <button class="btn btn-xs" style="color:#7aaeff;border-color:rgba(79,127,255,.3);background:rgba(79,127,255,.08)" onclick="event.stopPropagation();printProj(${p.id})">출력</button>
          <button class="btn btn-xs" onclick="event.stopPropagation();dupProj(${p.id})">복제</button>
          <button class="btn btn-xs" onclick="event.stopPropagation();regenProj(${p.id})">재생성</button>
          <button class="btn btn-xs btn-red" onclick="event.stopPropagation();delProj(${p.id})">삭제</button>
        </div>
        <span class="proj-arrow" id="pa-${p.id}">▾</span>
      </div>
      <div class="proj-body" id="pb-${p.id}">
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px">
          <div>
            <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">생성 조건 [SCR-008]</div>
            <div class="cfg-grid">
              <div class="cfg-item"><span class="cfg-k">엔진</span><span class="cfg-v">${p.config?.engine||'-'}</span></div>
              <div class="cfg-item"><span class="cfg-k">레슨위드</span><span class="cfg-v">${p.config?.lessonwith?'적용':'미적용'}</span></div>
              <div class="cfg-item"><span class="cfg-k">학년</span><span class="cfg-v">${p.grade}</span></div>
              <div class="cfg-item"><span class="cfg-k">난이도</span><span class="cfg-v">${p.diff}</span></div>
              <div class="cfg-item"><span class="cfg-k">문항</span><span class="cfg-v">${p.qCount}문항</span></div>
              <div class="cfg-item"><span class="cfg-k">시험지</span><span class="cfg-v">${p.sheets||1}개</span></div>
            </div>
          </div>
          <div>
            <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:5px;font-family:'IBM Plex Mono',monospace">버전 이력 [SCR-009 Fork & Versioning]</div>
            ${(p.versions||[]).map(v=>`
              <div class="ver-item ${v.active?'ver-active':''}">
                <span style="font-size:10px;padding:1px 6px;border-radius:6px;background:${v.active?'rgba(79,127,255,.2)':'var(--c3)'};color:${v.active?'#7aaeff':'var(--c6)'};font-family:'IBM Plex Mono',monospace">${v.v}</span>
                <span style="flex:1">${v.label}</span>
                <span style="font-family:'IBM Plex Mono',monospace;font-size:10px;color:var(--c6)">${v.date}</span>
                <button class="btn btn-xs" onclick="toast('${v.v} 버전 로드됨')">열기</button>
                ${!v.active?`<button class="btn btn-xs" onclick="toast('버전 비교 — Side-by-Side')">비교</button>`:''}
              </div>`).join('')}
            <button class="btn btn-xs btn-amber" onclick="addVer(${p.id})" style="margin-top:4px;width:100%;justify-content:center">+ 새 버전 저장 [SCR-009]</button>
          </div>
        </div>
        <div style="margin-top:10px">
          <div style="font-size:11px;font-weight:500;color:var(--c7);margin-bottom:4px;font-family:'IBM Plex Mono',monospace">지문 미리보기</div>
          <div style="font-size:12px;line-height:1.8;color:var(--c7);background:var(--c2);border-radius:var(--r);padding:9px;max-height:70px;overflow:hidden;border:0.5px solid var(--border)">${(p.passText||'').slice(0,250)}...</div>
        </div>
        <div style="margin-top:10px;display:flex;gap:5px;flex-wrap:wrap">
          <button class="btn btn-xs" style="color:#7aaeff;border-color:rgba(79,127,255,.3);background:rgba(79,127,255,.08)" onclick="printProj(${p.id})">PDF 출력</button>
          <button class="btn btn-xs" onclick="shareProj(${p.id})">공유 링크</button>
          ${!p.reviewed?`<button class="btn btn-xs btn-amber" onclick="markRev(${p.id})"><svg width="10" height="10" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg> NE 저자 검수 요청</button>`:''}
        </div>
      </div>
    </div>`).join('');
}

function togProj(id){const b=document.getElementById('pb-'+id),a=document.getElementById('pa-'+id);const o=b.classList.contains('on');b.classList.toggle('on',!o);a.classList.toggle('open',!o);}
function togFav(id){const p=S.projects.find(x=>x.id===id);if(p){p.fav=!p.fav;renderStore();toast(p.fav?'즐겨찾기 추가':'즐겨찾기 해제');}}
function printProj(id){
  const p=S.projects.find(x=>x.id===id); if(!p)return;
  S.printCnt=(S.printCnt||0)+1;
  const set=S.examSets.find(s=>s.id===p.examSetId)||{title:p.title,grade:p.grade,diff:p.diff,engine:p.engine,questions:[{no:18,type:'',score:'2점',topic:'',passage:p.passText||'',stem:'',choices:['①','②','③','④','⑤'],answer:0,diff:p.diff,topic:'-'}]};
  const html=buildPDF(set,p.brand);
  document.getElementById('printBox').innerHTML=html;
  document.getElementById('pdf-sheet').innerHTML=html;
  document.getElementById('printTitle').textContent=p.title+' 출력';
  openModal('modal-print'); updStats();
}
function dupProj(id){const p=S.projects.find(x=>x.id===id);if(!p)return;const c={...p,id:Date.now(),title:p.title+' (복사본)',versions:[{v:'v1',label:'복제본',date:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit'}),active:true}]};S.projects.splice(S.projects.indexOf(p)+1,0,c);updStats();updBadge();renderStore();toast('복제: '+c.title);}
function regenProj(id){const p=S.projects.find(x=>x.id===id);if(!p)return;p.versions.forEach(v=>v.active=false);const vn='v'+(p.versions.length+1);p.versions.unshift({v:vn,label:'AI 재생성',date:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit'}),active:true});p.qCount=Math.floor(8+Math.random()*12);renderStore();toast(p.title+' — '+vn+' 재생성');}
function delProj(id){S.projects=S.projects.filter(p=>p.id!==id);renderStore();updBadge();updStats();toast('삭제됨');}
function clrAll(){if(!confirm('모두 삭제?'))return;S.projects=[];renderStore();updBadge();updStats();toast('전체 삭제');}
function markRev(id){const p=S.projects.find(x=>x.id===id);if(p){p.reviewed=true;updStats();renderStore();toast('검수 요청 접수 [SCR-002]');}}
function addVer(id){const p=S.projects.find(x=>x.id===id);if(!p)return;p.versions.forEach(v=>v.active=false);const vn='v'+(p.versions.length+1);p.versions.unshift({v:vn,label:'교사 수정 저장',date:new Date().toLocaleTimeString('ko-KR',{hour:'2-digit',minute:'2-digit'}),active:true});renderStore();toast(vn+' 저장 [SCR-009]');}
function shareProj(id){const url=location.href.split('?')[0]+'?share='+id;navigator.clipboard?.writeText(url).then(()=>toast('공유 링크 복사됨')).catch(()=>toast('링크: '+url));}

/* ═══════════════════════════════════════
   MODALS
═══════════════════════════════════════ */
function openModal(id){document.getElementById(id).classList.add('on')}
function closeModal(id){document.getElementById(id).classList.remove('on')}
document.querySelectorAll('.modal-overlay').forEach(o=>o.addEventListener('click',function(e){if(e.target===this)this.classList.remove('on')}));
function saveSets(){const b=document.getElementById('setBrand').value.trim();if(b&&document.getElementById('t1Brand'))document.getElementById('t1Brand').value=b;closeModal('modal-settings');toast('설정 저장됨');}
function openLogoModal(){openModal('modal-logo')}
function prevLogo(input){const f=input.files[0];if(!f)return;const r=new FileReader();r.onload=e=>{document.getElementById('logoPreview').src=e.target.result;document.getElementById('logoPreview').style.display='block';document.getElementById('logoPlaceholder').textContent='로고 선택됨';document.getElementById('logoSaveBtn').disabled=false;};r.readAsDataURL(f);}
function saveLogo(){closeModal('modal-logo');toast('로고 적용됨 [SCR-003]');}

/* ═══════════════════════════════════════
   TOAST
═══════════════════════════════════════ */
let _tt=null;
function toast(msg){const t=document.getElementById('toast');t.textContent=msg;t.style.opacity='1';t.style.transform='translateX(-50%) translateY(0)';clearTimeout(_tt);_tt=setTimeout(()=>{t.style.opacity='0';t.style.transform='translateX(-50%) translateY(10px)';},2800);}

renderStore();
</script>
</body>
</html>
