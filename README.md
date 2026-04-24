[pipeline_b2b_v3 (1).html](https://github.com/user-attachments/files/27068181/pipeline_b2b_v3.1.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pipeline B2B — São Leopoldo Mandic</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=Mulish:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0a0c10;--surf:#111318;--surf2:#181b22;--surf3:#1f232e;--surf4:#272c3a;
  --bdr:rgba(255,255,255,.06);--bdr2:rgba(255,255,255,.11);--bdr3:rgba(255,255,255,.18);
  --txt:#dde1ec;--txt2:#7c8298;--txt3:#444a5e;
  --acc:#5b7fff;--accL:rgba(91,127,255,.14);
  --hof:#b06aff;--oral:#3fa9ff;--equip:#2cd98a;--franch:#ffb020;--insum:#40d4f5;--alin:#e070ff;
  --urg:#ff4d4d;--urgL:rgba(255,77,77,.12);
  --alta:#ff8c2a;--altaL:rgba(255,140,42,.12);
  --media:#2cd98a;--mediaL:rgba(44,217,138,.10);
  --ganho:#10d4a0;--ganhoL:rgba(16,212,160,.12);
  --baixa:#555e76;--baixaL:rgba(85,94,118,.12);
  --s-a:#3fa9ff;--s-aL:rgba(63,169,255,.12);
  --s-c:#ffb020;--s-cL:rgba(255,176,32,.12);
  --s-p:#ff4d4d;--s-pL:rgba(255,77,77,.12);
  --s-g:#10d4a0;--s-gL:rgba(16,212,160,.12);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Mulish',sans-serif;background:var(--bg);color:var(--txt);min-height:100vh;font-size:13px;line-height:1.5;overflow-x:hidden}

/* ── HEADER ── */
.hdr{padding:18px 28px 16px;border-bottom:1px solid var(--bdr);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:10px;background:var(--surf);position:sticky;top:0;z-index:100}
.hdr-l{display:flex;align-items:center;gap:13px}
.logo{width:34px;height:34px;border-radius:8px;background:conic-gradient(from 180deg,#5b7fff,#b06aff,#5b7fff);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:700;font-size:14px;color:#fff;flex-shrink:0}
.hdr-title{font-family:'Syne',sans-serif;font-size:15px;font-weight:600;letter-spacing:-.3px}
.hdr-sub{font-size:11px;color:var(--txt2);margin-top:1px}
.hdr-r{display:flex;gap:7px;align-items:center;flex-wrap:wrap}
.btn{font-family:'Mulish',sans-serif;font-size:12px;font-weight:600;padding:7px 13px;border-radius:7px;cursor:pointer;border:1px solid var(--bdr2);background:var(--surf3);color:var(--txt2);transition:all .15s;white-space:nowrap}
.btn:hover{background:var(--surf4);color:var(--txt);border-color:var(--bdr3)}
.btn-p{background:var(--acc);color:#fff;border-color:transparent}.btn-p:hover{background:#4d71f0}
.btn-d{background:var(--urgL);color:var(--urg);border-color:rgba(255,77,77,.2)}.btn-d:hover{background:rgba(255,77,77,.22)}
.btn-s{background:var(--ganhoL);color:var(--ganho);border-color:rgba(16,212,160,.2)}.btn-s:hover{background:rgba(16,212,160,.22)}
.saved-ind{font-size:11px;color:var(--ganho);opacity:0;transition:opacity .3s;font-family:'IBM Plex Mono',monospace}
.saved-ind.show{opacity:1}

/* ── FILTERS ── */
.filters{padding:12px 28px;background:var(--surf);border-bottom:1px solid var(--bdr);display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.fg{display:flex;align-items:center;gap:6px;flex-wrap:wrap}
.fsep{width:1px;height:20px;background:var(--bdr2);margin:0 4px}
.fl{font-size:10px;font-weight:600;color:var(--txt3);text-transform:uppercase;letter-spacing:.8px;margin-right:2px}
.chip{font-size:11px;font-weight:600;font-family:'Mulish',sans-serif;padding:4px 11px;border-radius:999px;border:1px solid var(--bdr2);background:transparent;color:var(--txt2);cursor:pointer;transition:all .15s}
.chip:hover{background:var(--surf3);color:var(--txt)}
.chip.on{color:#fff;border-color:transparent}
.hof.on{background:var(--hof)}.oral.on{background:var(--oral)}.equip.on{background:var(--equip)}
.franch.on{background:var(--franch)}.insum.on{background:var(--insum)}.alin.on{background:var(--alin)}
.c-a.on{background:var(--s-a)}.c-c.on{background:var(--s-c)}.c-p.on{background:var(--s-p)}.c-g.on{background:var(--s-g)}
.c-urg.on{background:var(--urg)}.c-alta.on{background:var(--alta)}.c-med.on{background:var(--media)}
.c-gan.on{background:var(--ganho)}.c-bx.on{background:var(--baixa)}

/* ── MAIN ── */
.main{padding:20px 28px}

/* ── KPIs ── */
.krow{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:9px;margin-bottom:18px}
.kcard{background:var(--surf);border:1px solid var(--bdr);border-radius:10px;padding:14px 16px;position:relative;overflow:hidden}
.kcard::after{content:'';position:absolute;top:0;left:0;right:0;height:2px}
.kt::after{background:var(--acc)}.kb::after{background:var(--hof)}.kp::after{background:var(--equip)}
.ku::after{background:var(--urg)}.ka::after{background:var(--alta)}.kg::after{background:var(--ganho)}
.kl{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.6px;color:var(--txt2);margin-bottom:5px}
.kv{font-family:'Syne',sans-serif;font-size:20px;font-weight:700;line-height:1}
.kv.sm{font-size:13px;font-family:'IBM Plex Mono',monospace;font-weight:400}
.ks{font-size:10px;color:var(--txt3);margin-top:3px;font-family:'IBM Plex Mono',monospace}

/* ── CHARTS ── */
.crow{display:grid;grid-template-columns:1fr 1fr;gap:11px;margin-bottom:18px}
@media(max-width:660px){.crow{grid-template-columns:1fr}}
.cc{background:var(--surf);border:1px solid var(--bdr);border-radius:10px;padding:15px 17px}
.cct{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.6px;color:var(--txt2);margin-bottom:11px}
.brow{display:flex;align-items:center;gap:8px;margin-bottom:6px}
.blbl{font-size:11px;color:var(--txt2);width:88px;text-align:right;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;flex-shrink:0}
.btrk{flex:1;height:9px;background:var(--surf3);border-radius:4px;overflow:hidden}
.bfil{height:100%;border-radius:4px;transition:width .45s cubic-bezier(.4,0,.2,1)}
.bval{font-size:10px;color:var(--txt2);min-width:60px;font-family:'IBM Plex Mono',monospace}

/* ── TABLE ── */
.tbar{display:flex;align-items:center;justify-content:space-between;margin-bottom:9px;flex-wrap:wrap;gap:8px}
.tbar-l{display:flex;align-items:center;gap:10px;flex-wrap:wrap}
.ttitle{font-family:'Syne',sans-serif;font-size:14px;font-weight:600}
.sw{position:relative}
.si{background:var(--surf);border:1px solid var(--bdr2);border-radius:7px;padding:7px 10px 7px 30px;color:var(--txt);font-family:'Mulish',sans-serif;font-size:12px;outline:none;width:210px;transition:border-color .15s}
.si:focus{border-color:var(--acc)}
.sic{position:absolute;left:9px;top:50%;transform:translateY(-50%);color:var(--txt3);font-size:13px;pointer-events:none}
.rcnt{font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--txt3);background:var(--surf2);padding:4px 9px;border-radius:6px;border:1px solid var(--bdr)}
.tw{border:1px solid var(--bdr);border-radius:10px;overflow:hidden;overflow-x:auto}
table{width:100%;border-collapse:collapse;font-size:12px;min-width:900px}
thead tr{background:var(--surf2)}
th{padding:9px 10px;text-align:left;font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.5px;color:var(--txt3);border-bottom:1px solid var(--bdr);white-space:nowrap;cursor:pointer;user-select:none;transition:color .15s}
th:hover{color:var(--txt2)}
th.sorted{color:var(--acc)}
.sa{margin-left:3px;font-size:9px;opacity:.5}
th.sorted .sa{opacity:1}
td{padding:8px 10px;border-bottom:1px solid var(--bdr);color:var(--txt2);overflow:hidden;text-overflow:ellipsis;white-space:nowrap;vertical-align:middle}
tbody tr{background:var(--surf)}
tbody tr:nth-child(even){background:#0f1116}
tbody tr:hover td{background:var(--surf3)!important;color:var(--txt)}
tbody tr:last-child td{border-bottom:none}
.cn{font-weight:600;color:var(--txt)}
.seg-dot{display:inline-block;width:7px;height:7px;border-radius:50%;margin-right:5px;vertical-align:middle;flex-shrink:0}

/* inline editable fields */
.isel{background:var(--surf3);border:1px solid var(--bdr2);border-radius:5px;color:var(--txt);font-family:'Mulish',sans-serif;font-size:11px;padding:3px 6px;outline:none;cursor:pointer;width:100%;transition:border-color .15s}
.isel:hover{border-color:var(--bdr3)}
.isel:focus{border-color:var(--acc);background:var(--surf4)}
input.isel{cursor:text;text-align:right}
input[type=number].isel::-webkit-outer-spin-button,input[type=number].isel::-webkit-inner-spin-button{-webkit-appearance:none}
/* prioridade select color coding */
.isel[data-fld="pr"]{font-weight:600;font-size:10px;letter-spacing:.2px}
.isel[data-fld="pr"].pv-URGENTE{background:rgba(255,77,77,.15);color:#ff7070;border-color:rgba(255,77,77,.3)}
.isel[data-fld="pr"].pv-ALTA{background:rgba(255,140,42,.15);color:#ffaa60;border-color:rgba(255,140,42,.3)}
.isel[data-fld="pr"].pv-MEDIA{background:rgba(44,217,138,.12);color:#5ae8a8;border-color:rgba(44,217,138,.25)}
.isel[data-fld="pr"].pv-GANHO{background:rgba(16,212,160,.14);color:#40e0be;border-color:rgba(16,212,160,.3)}
.isel[data-fld="pr"].pv-BAIXA{background:rgba(85,94,118,.14);color:#8899aa;border-color:rgba(85,94,118,.25)}

/* badges */
.sb{display:inline-flex;align-items:center;gap:4px;font-size:10px;font-weight:600;padding:2px 9px;border-radius:999px;white-space:nowrap}
.sb::before{content:'';width:5px;height:5px;border-radius:50%;background:currentColor;opacity:.7;flex-shrink:0}
.sb-a{background:var(--s-aL);color:#6bc8ff;border:1px solid rgba(63,169,255,.25)}
.sb-c{background:var(--s-cL);color:#ffc84a;border:1px solid rgba(255,176,32,.25)}
.sb-p{background:var(--s-pL);color:#ff7070;border:1px solid rgba(255,77,77,.25)}
.sb-g{background:var(--s-gL);color:#40e0be;border:1px solid rgba(16,212,160,.25)}
.pb{display:inline-flex;align-items:center;gap:4px;font-size:10px;font-weight:600;padding:2px 9px;border-radius:999px;white-space:nowrap}
.pb::before{content:'';width:5px;height:5px;border-radius:50%;background:currentColor;opacity:.7;flex-shrink:0}
.pb-u{background:var(--urgL);color:#ff7070;border:1px solid rgba(255,77,77,.2)}
.pb-a{background:var(--altaL);color:#ffaa60;border:1px solid rgba(255,140,42,.2)}
.pb-m{background:var(--mediaL);color:#5ae8a8;border:1px solid rgba(44,217,138,.2)}
.pb-g{background:var(--ganhoL);color:#40e0be;border:1px solid rgba(16,212,160,.2)}
.pb-b{background:var(--baixaL);color:#8899aa;border:1px solid rgba(85,94,118,.2)}
.prob-tag{font-family:'IBM Plex Mono',monospace;font-size:10px;padding:2px 6px;border-radius:4px;background:var(--surf3);color:var(--txt2)}

/* timeline button */
.tl-btn{background:transparent;border:1px solid var(--bdr2);border-radius:5px;color:var(--txt3);cursor:pointer;font-size:11px;padding:3px 9px;transition:all .15s;font-family:'Mulish',sans-serif;font-weight:600;white-space:nowrap}
.tl-btn:hover{background:var(--accL);color:var(--acc);border-color:rgba(91,127,255,.3)}
.tl-count{display:inline-block;font-size:9px;background:var(--accL);color:var(--acc);border-radius:3px;padding:0 4px;margin-left:3px;font-family:'IBM Plex Mono',monospace;vertical-align:middle}

.empty{text-align:center;padding:40px;color:var(--txt3);font-size:12px}
.add-bar{border:1px dashed var(--bdr2);border-radius:10px;padding:11px 16px;margin-top:9px;display:flex;align-items:center;gap:9px;cursor:pointer;transition:all .15s;color:var(--txt3);font-size:12px;font-weight:500}
.add-bar:hover{border-color:var(--acc);color:var(--acc);background:var(--accL)}

/* ── MAIN MODAL ── */
.overlay{position:fixed;inset:0;background:rgba(0,0,0,.72);z-index:200;display:flex;align-items:center;justify-content:center;padding:20px;opacity:0;pointer-events:none;transition:opacity .2s;backdrop-filter:blur(4px)}
.overlay.open{opacity:1;pointer-events:all}
.modal{background:var(--surf);border:1px solid var(--bdr2);border-radius:14px;width:100%;max-width:580px;max-height:90vh;overflow-y:auto;transform:translateY(10px) scale(.98);transition:transform .2s}
.overlay.open .modal{transform:none}
.mhdr{padding:16px 20px 13px;border-bottom:1px solid var(--bdr);display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;background:var(--surf);z-index:1}
.mtitle{font-family:'Syne',sans-serif;font-size:15px;font-weight:600}
.mclose{background:transparent;border:none;color:var(--txt2);cursor:pointer;font-size:20px;line-height:1;padding:0 4px}.mclose:hover{color:var(--txt)}
.mbody{padding:18px 20px}
.fsec{margin-bottom:18px}
.fsec-title{font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.8px;color:var(--acc);margin-bottom:12px;padding-bottom:6px;border-bottom:1px solid var(--accL)}
.fgrid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.ffull{grid-column:1/-1}
.field label{display:block;font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.6px;color:var(--txt2);margin-bottom:5px}
.req{color:var(--urg);margin-left:2px}
.field input,.field select,.field textarea{width:100%;background:var(--surf2);border:1px solid var(--bdr2);border-radius:7px;padding:8px 10px;color:var(--txt);font-family:'Mulish',sans-serif;font-size:12px;outline:none;transition:border-color .15s}
.field input:focus,.field select:focus,.field textarea:focus{border-color:var(--acc);background:var(--surf3)}
.field select option{background:var(--surf2)}
.field textarea{resize:vertical;min-height:58px;line-height:1.5}
.cond-wrap{display:none}.cond-wrap.show{display:block}
.mfooter{padding:13px 20px 16px;border-top:1px solid var(--bdr);display:flex;gap:8px;justify-content:flex-end}

/* STATUS LEGEND in modal */
.sl-box{background:var(--surf2);border:1px solid var(--bdr);border-radius:8px;padding:11px 14px;margin-bottom:16px}
.sl-title{font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.6px;color:var(--txt3);margin-bottom:8px}
.sl-row{display:flex;flex-wrap:wrap;gap:7px}
.sl-item{display:flex;align-items:flex-start;gap:6px;font-size:11px;color:var(--txt2);min-width:220px;flex:1}
.sl-dot{width:7px;height:7px;border-radius:50%;flex-shrink:0;margin-top:3px}

/* ── TIMELINE MODAL ── */
.tl-overlay{position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:300;display:flex;align-items:center;justify-content:center;padding:20px;opacity:0;pointer-events:none;transition:opacity .2s;backdrop-filter:blur(6px)}
.tl-overlay.open{opacity:1;pointer-events:all}
.tl-modal{background:var(--surf);border:1px solid var(--bdr2);border-radius:14px;width:100%;max-width:640px;max-height:90vh;overflow-y:auto;transform:translateY(10px) scale(.98);transition:transform .2s}
.tl-overlay.open .tl-modal{transform:none}
.tl-hdr{padding:16px 22px 13px;border-bottom:1px solid var(--bdr);display:flex;align-items:flex-start;justify-content:space-between;position:sticky;top:0;background:var(--surf);z-index:1}
.tl-name{font-family:'Syne',sans-serif;font-size:15px;font-weight:700;color:var(--txt)}
.tl-meta{font-size:11px;color:var(--txt2);margin-top:2px}
.tl-close{background:transparent;border:none;color:var(--txt2);cursor:pointer;font-size:22px;line-height:1;padding:0 4px;flex-shrink:0}.tl-close:hover{color:var(--txt)}
.tl-body{padding:20px 22px 24px}

/* FUNIL PROGRESS BAR */
.tl-funnel-wrap{background:var(--surf2);border:1px solid var(--bdr);border-radius:10px;padding:16px 18px;margin-bottom:22px}
.tl-fw-title{font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.6px;color:var(--txt3);margin-bottom:14px}
.funnel-track{display:flex;align-items:flex-start;gap:0;overflow-x:auto;padding-bottom:2px}
.fstep{flex:1;min-width:56px;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative;cursor:default}
.fstep+.fstep::before{content:'';position:absolute;left:-50%;right:50%;top:13px;height:2px;background:var(--bdr2);z-index:0}
.fstep.done+.fstep::before{background:var(--equip);opacity:.6}
.fstep.current+.fstep::before{background:var(--bdr2)}
.fdot{width:26px;height:26px;border-radius:50%;border:2px solid var(--bdr2);background:var(--surf3);display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:var(--txt3);z-index:1;position:relative;transition:all .3s;flex-shrink:0}
.flbl{font-size:9px;color:var(--txt3);text-align:center;line-height:1.3;max-width:58px;transition:color .3s}
.fdate{font-size:8px;font-family:'IBM Plex Mono',monospace;color:var(--txt3);text-align:center;margin-top:2px;min-height:10px}
.fstep.done .fdot{background:var(--equip);border-color:var(--equip);color:#fff}
.fstep.done .flbl{color:var(--equip)}
.fstep.done .fdate{color:var(--equip);opacity:.7}
.fstep.current .fdot{background:var(--acc);border-color:var(--acc);color:#fff;box-shadow:0 0 0 4px rgba(91,127,255,.2)}
.fstep.current .flbl{color:var(--acc);font-weight:700}
.fstep.current .fdate{color:var(--acc);opacity:.8}
.fstep.frozen .fdot{background:rgba(255,176,32,.1);border-color:var(--franch);color:var(--franch)}
.fstep.frozen .flbl{color:var(--franch)}
.fstep.lost .fdot{background:var(--urgL);border-color:var(--urg);color:var(--urg)}
.fstep.lost .flbl{color:var(--urg)}
.tl-status-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.tl-pill{font-size:11px;padding:4px 12px;border-radius:6px;border:1px solid var(--bdr2);background:var(--surf3);color:var(--txt2)}

/* TIMELINE LIST */
.tl-sec-title{font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.7px;color:var(--txt3);margin-bottom:12px}
.tl-empty{text-align:center;padding:20px;color:var(--txt3);font-size:12px;border:1px dashed var(--bdr2);border-radius:8px}
.tl-list{position:relative;padding-left:24px}
.tl-list::before{content:'';position:absolute;left:8px;top:6px;bottom:6px;width:1px;background:var(--bdr2)}
.tl-item{position:relative;margin-bottom:14px}
.tl-item:last-child{margin-bottom:0}
.tl-dot-i{position:absolute;left:-20px;top:4px;width:12px;height:12px;border-radius:50%;border:2px solid var(--bdr2);background:var(--surf);z-index:1;transition:all .2s}
.ti-etapa .tl-dot-i{background:var(--acc);border-color:var(--acc)}
.ti-status .tl-dot-i{background:var(--hof);border-color:var(--hof)}
.ti-potencial .tl-dot-i{background:var(--equip);border-color:var(--equip)}
.ti-nota .tl-dot-i{background:var(--franch);border-color:var(--franch)}
.ti-criacao .tl-dot-i{background:var(--txt3);border-color:var(--txt3)}
.tl-ts{font-family:'IBM Plex Mono',monospace;font-size:10px;color:var(--txt3);margin-bottom:3px}
.tl-card{background:var(--surf2);border:1px solid var(--bdr);border-radius:7px;padding:9px 12px}
.tl-tag{display:inline-block;font-size:9px;font-weight:700;text-transform:uppercase;letter-spacing:.5px;padding:1px 7px;border-radius:3px;margin-bottom:5px}
.tl-tag-etapa{background:rgba(91,127,255,.12);color:#8baeff}
.tl-tag-status{background:rgba(176,106,255,.12);color:#c89aff}
.tl-tag-potencial{background:rgba(44,217,138,.12);color:#5ae8a8}
.tl-tag-nota{background:rgba(255,176,32,.12);color:#ffc84a}
.tl-tag-criacao{background:rgba(85,94,118,.12);color:#8899aa}
.tl-change{display:flex;align-items:center;gap:7px;flex-wrap:wrap;font-size:12px}
.tl-from{color:var(--txt3);text-decoration:line-through}
.tl-arrow{color:var(--txt3);font-size:11px}
.tl-to{color:var(--txt);font-weight:600}
.tl-note-txt{font-size:12px;color:var(--txt)}
.tl-note-obs{font-size:11px;color:var(--txt2);margin-top:4px;font-style:italic;border-top:1px solid var(--bdr);padding-top:4px}

/* add note */
.tl-note-area{margin-top:14px}
.add-note-btn{font-size:11px;font-weight:600;font-family:'Mulish',sans-serif;background:transparent;border:1px dashed var(--bdr2);border-radius:6px;color:var(--txt3);cursor:pointer;padding:6px 14px;transition:all .15s;width:100%}
.add-note-btn:hover{border-color:var(--acc);color:var(--acc);background:var(--accL)}
.note-form{display:none;margin-top:8px}
.note-form.show{display:block}
.note-textarea{width:100%;background:var(--surf3);border:1px solid var(--bdr2);border-radius:7px;padding:8px 10px;color:var(--txt);font-family:'Mulish',sans-serif;font-size:12px;outline:none;resize:vertical;min-height:64px;line-height:1.5;transition:border-color .15s}
.note-textarea:focus{border-color:var(--acc)}
.note-form-btns{display:flex;gap:8px;margin-top:7px}

/* print */
@media print{
  .hdr,.filters,.tl-overlay{display:none!important}
  body{background:#fff;color:#000}
  .tl-modal{box-shadow:none;border:none;max-height:none;overflow:visible}
  .tl-card{background:#f8f8f8!important;border-color:#ddd!important;print-color-adjust:exact}
  .fdot{print-color-adjust:exact}
}

/* footer */
.footer{padding:13px 28px;border-top:1px solid var(--bdr);display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:8px;background:var(--surf)}
.footer p{font-size:10px;color:var(--txt3);font-family:'IBM Plex Mono',monospace}

@keyframes fadeUp{from{opacity:0;transform:translateY(5px)}to{opacity:1;transform:translateY(0)}}
.kcard{animation:fadeUp .3s ease both}
.kcard:nth-child(1){animation-delay:.04s}.kcard:nth-child(2){animation-delay:.08s}
.kcard:nth-child(3){animation-delay:.12s}.kcard:nth-child(4){animation-delay:.16s}
.kcard:nth-child(5){animation-delay:.2s} .kcard:nth-child(6){animation-delay:.24s}
</style>
</head>
<body>

<header class="hdr">
  <div class="hdr-l">
    <div class="logo">M</div>
    <div>
      <div class="hdr-title">Pipeline B2B</div>
      <div class="hdr-sub">São Leopoldo Mandic · Soluções Corporativas · 2026</div>
    </div>
  </div>
  <div class="hdr-r">
    <span class="saved-ind" id="savedInd">✓ Salvo</span>
    <button class="btn" onclick="exportCSV()">Exportar CSV</button>
    <button class="btn btn-s" onclick="openModal(null)">+ Nova empresa</button>
    <button class="btn" onclick="resetData()">Resetar dados</button>
  </div>
</header>

<div class="filters">
  <div class="fg">
    <span class="fl">Segmento</span>
    <button class="chip hof on"  onclick="tog('seg','HOF',this)">HOF</button>
    <button class="chip oral on" onclick="tog('seg','Oral Care',this)">Oral Care</button>
    <button class="chip equip on"onclick="tog('seg','Equipamentos',this)">Equipamentos</button>
    <button class="chip franch on"onclick="tog('seg','FRANCHISING',this)">Franchising</button>
    <button class="chip insum on"onclick="tog('seg','Insumos',this)">Insumos</button>
    <button class="chip alin on" onclick="tog('seg','Alinhadores',this)">Alinhadores</button>
  </div>
  <div class="fsep"></div>
  <div class="fg">
    <span class="fl">Status</span>
    <button class="chip c-a on" onclick="tog('status','Ativa',this)">Ativa</button>
    <button class="chip c-c on" onclick="tog('status','Congelada',this)">Congelada</button>
    <button class="chip c-p on" onclick="tog('status','Perdida',this)">Perdida</button>
    <button class="chip c-g on" onclick="tog('status','Ganha',this)">Ganha</button>
  </div>
  <div class="fsep"></div>
  <div class="fg">
    <span class="fl">Prioridade</span>
    <button class="chip c-urg on" onclick="tog('prio','URGENTE',this)">Urgente</button>
    <button class="chip c-alta on"onclick="tog('prio','ALTA',this)">Alta</button>
    <button class="chip c-med on" onclick="tog('prio','MEDIA',this)">Media</button>
    <button class="chip c-gan on" onclick="tog('prio','GANHO',this)">Ganho</button>
    <button class="chip c-bx on"  onclick="tog('prio','BAIXA',this)">Baixa</button>
  </div>
</div>

<main class="main">
  <div class="krow" id="kpis"></div>
  <div class="crow">
    <div class="cc"><div class="cct">Pipeline ponderado por segmento</div><div id="cSeg"></div></div>
    <div class="cc"><div class="cct">Distribuição por status</div><div id="cStatus"></div></div>
  </div>
  <div class="tbar">
    <div class="tbar-l">
      <span class="ttitle">Empresas</span>
      <div class="sw"><span class="sic">⌕</span><input class="si" id="srch" type="text" placeholder="Buscar..." oninput="render()"></div>
    </div>
    <span class="rcnt" id="rcnt"></span>
  </div>
  <div class="tw">
    <table>
      <thead><tr>
        <th style="width:15%" onclick="srt('n')">Empresa <span class="sa">↕</span></th>
        <th style="width:11%" onclick="srt('s')">Segmento <span class="sa">↕</span></th>
        <th style="width:15%" onclick="srt('e')">Etapa do funil <span class="sa">↕</span></th>
        <th style="width:6%;text-align:center" onclick="srt('prob')">Prob. <span class="sa">↕</span></th>
        <th style="width:10%" onclick="srt('status')">Status <span class="sa">↕</span></th>
        <th style="width:10%;text-align:right" onclick="srt('p')">Potencial <span class="sa">↕</span></th>
        <th style="width:10%;text-align:right" onclick="srt('pond')">Ponderado <span class="sa">↕</span></th>
        <th style="width:9%;text-align:center" onclick="srt('pr')">Prioridade <span class="sa">↕</span></th>
        <th style="width:11%">Ação</th>
        <th style="width:6%;text-align:center">Timeline</th>
      </tr></thead>
      <tbody id="tb"></tbody>
    </table>
  </div>
  <div class="add-bar" onclick="openModal(null)"><span style="font-size:17px">+</span> Adicionar nova empresa</div>
</main>

<footer class="footer">
  <p>São Leopoldo Mandic · Pipeline B2B 2026 · Status conforme Funil de Vendas B2B v2</p>
  <p id="ftxt"></p>
</footer>

<!-- EDIT MODAL -->
<div class="overlay" id="overlay" onclick="if(event.target===this)closeModal()">
  <div class="modal">
    <div class="mhdr">
      <span class="mtitle" id="mTitle">Editar empresa</span>
      <button class="mclose" onclick="closeModal()">×</button>
    </div>
    <div class="mbody">
      <div class="sl-box">
        <div class="sl-title">Status da oportunidade — dimensão independente da etapa</div>
        <div class="sl-row">
          <div class="sl-item"><span class="sl-dot" style="background:var(--s-a)"></span><span><b style="color:var(--s-a)">Ativa</b> — em andamento, sem bloqueio</span></div>
          <div class="sl-item"><span class="sl-dot" style="background:var(--s-c)"></span><span><b style="color:var(--s-c)">Congelada</b> — sem resposta +21 dias · requer data revisão</span></div>
          <div class="sl-item"><span class="sl-dot" style="background:var(--s-p)"></span><span><b style="color:var(--s-p)">Perdida</b> — cliente declinou · requer motivo</span></div>
          <div class="sl-item"><span class="sl-dot" style="background:var(--s-g)"></span><span><b style="color:var(--s-g)">Ganha</b> — contrato assinado · etapa 9</span></div>
        </div>
      </div>
      <div class="fsec">
        <div class="fsec-title">Identificação</div>
        <div class="fgrid">
          <div class="field ffull"><label>Nome da empresa<span class="req">*</span></label><input id="f-n" type="text" placeholder="Ex: GALDERMA"></div>
          <div class="field"><label>Segmento<span class="req">*</span></label>
            <select id="f-s">
              <option>HOF</option><option>Oral Care</option><option>Equipamentos</option>
              <option>FRANCHISING</option><option>Insumos</option><option>Alinhadores</option>
            </select>
          </div>
          <div class="field"><label>Porte</label>
            <select id="f-porte"><option value="">—</option><option>PEQUENA</option><option>MÉDIA</option><option>GRANDE</option><option>GG</option></select>
          </div>
          <div class="field"><label>Responsável</label><input id="f-resp" type="text" placeholder="Nome"></div>
          <div class="field"><label>Contato</label><input id="f-cont" type="text" placeholder="Nome do contato"></div>
        </div>
      </div>
      <div class="fsec">
        <div class="fsec-title">Posição no funil</div>
        <div class="fgrid">
          <div class="field ffull"><label>Etapa do funil</label>
            <select id="f-e" onchange="onEtapa()">
              <option value="">— sem etapa —</option>
              <option value="Mapeada">1 · Mapeada (2%)</option>
              <option value="Contato Iniciado">2 · Contato Iniciado (5%)</option>
              <option value="Reuniao agendada">3 · Reunião Agendada (15%)</option>
              <option value="Reuniao realizada">4 · Reunião Realizada (25%)</option>
              <option value="Proposta em elaboracao">5 · Proposta em Elaboração (35%)</option>
              <option value="Proposta apresentada">6 · Proposta Apresentada (50%)</option>
              <option value="Aprovacao interna em curso">7 · Aprovação Interna em Curso (65%)</option>
              <option value="Em negociacao">8 · Em Negociação (80%)</option>
              <option value="Contrato assinado">9 · Contrato Assinado (100%)</option>
            </select>
          </div>
          <div class="field"><label>Status<span class="req">*</span></label>
            <select id="f-status" onchange="onStatus()">
              <option>Ativa</option><option>Congelada</option><option>Perdida</option><option>Ganha</option>
            </select>
          </div>
          <div class="field cond-wrap" id="revisaoWrap"><label>Data de revisão<span class="req">*</span></label><input id="f-revisao" type="text" placeholder="DD/MM/AAAA"></div>
          <div class="field cond-wrap ffull" id="motivoWrap"><label>Motivo da perda<span class="req">*</span></label>
            <select id="f-motivo">
              <option value="">— selecionar —</option>
              <option>Preço / ROI percebido</option><option>Sem budget</option><option>Concorrente</option>
              <option>Timing</option><option>Sem interesse</option><option>Outro</option>
            </select>
          </div>
        </div>
      </div>
      <div class="fsec">
        <div class="fsec-title">Valores e datas</div>
        <div class="fgrid">
          <div class="field"><label>Potencial (R$)</label><input id="f-p" type="number" min="0" step="1000" placeholder="0"></div>
          <div class="field"><label>Valor 2026 (R$)</label><input id="f-v26" type="number" min="0" step="100" placeholder="0"></div>
          <div class="field"><label>Prioridade<span class="req">*</span></label>
            <select id="f-pr">
              <option value="URGENTE">Urgente — ≤ 7 dias</option><option value="ALTA">Alta — ≤ 15 dias</option>
              <option value="MEDIA" selected>Media — ≤ 30 dias</option><option value="GANHO">Ganho</option>
              <option value="BAIXA">Baixa — ≤ 60 dias</option>
            </select>
          </div>
          <div class="field"><label>Prazo limite</label><input id="f-pz" type="text" placeholder="DD/MM/AAAA"></div>
        </div>
      </div>
      <div class="fsec">
        <div class="fsec-title">Ação e observações</div>
        <div class="fgrid">
          <div class="field ffull"><label>Ação recomendada</label><input id="f-a" type="text" placeholder="Ex: Pressionar decisão — prazo"></div>
          <div class="field ffull"><label>Observação / histórico</label><textarea id="f-obs" placeholder="Registro de contatos, bloqueios, próximos passos..."></textarea></div>
        </div>
      </div>
    </div>
    <div class="mfooter">
      <button class="btn btn-d" id="deleteBtn" onclick="deleteEntry()" style="margin-right:auto;display:none">Excluir</button>
      <button class="btn" onclick="closeModal()">Cancelar</button>
      <button class="btn btn-p" onclick="saveEntry()">Salvar</button>
    </div>
  </div>
</div>

<!-- TIMELINE MODAL -->
<div class="tl-overlay" id="tlOverlay" onclick="if(event.target===this)closeTl()">
  <div class="tl-modal">
    <div class="tl-hdr">
      <div>
        <div class="tl-name" id="tlName">—</div>
        <div class="tl-meta" id="tlMeta">—</div>
      </div>
      <div style="display:flex;gap:8px;align-items:center">
        <button class="btn" style="font-size:11px;padding:5px 11px" onclick="printTl()">Imprimir</button>
        <button class="tl-close" onclick="closeTl()">×</button>
      </div>
    </div>
    <div class="tl-body">
      <div class="tl-funnel-wrap">
        <div class="tl-fw-title">Jornada no funil</div>
        <div class="funnel-track" id="tlFunnel"></div>
        <div class="tl-status-row" id="tlStatusRow"></div>
      </div>
      <div class="tl-sec-title">Histórico de alterações</div>
      <div id="tlList"></div>
      <div class="tl-note-area">
        <button class="add-note-btn" onclick="toggleNoteForm()">+ Adicionar nota manual</button>
        <div class="note-form" id="noteForm">
          <textarea class="note-textarea" id="noteText" placeholder="Registro de contato, observação, decisão interna, bloqueio..."></textarea>
          <div class="note-form-btns">
            <button class="btn btn-p" style="font-size:11px;padding:5px 12px" onclick="saveNote()">Salvar nota</button>
            <button class="btn" style="font-size:11px;padding:5px 12px" onclick="toggleNoteForm()">Cancelar</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div style="position:fixed;bottom:22px;right:22px;z-index:400;background:var(--surf);border:1px solid var(--bdr2);border-radius:9px;padding:10px 15px;font-size:12px;color:var(--txt);transform:translateY(18px);opacity:0;transition:all .25s;pointer-events:none;min-width:170px;display:flex;align-items:center;gap:7px" id="toast">
  <span style="width:7px;height:7px;border-radius:50%;flex-shrink:0" id="toastDot"></span>
  <span id="toastMsg"></span>
</div>

<script>
var PESOS={'Mapeada':.02,'Contato Iniciado':.05,'Reuniao agendada':.15,'Reuniao realizada':.25,'Proposta em elaboracao':.35,'Proposta apresentada':.50,'Aprovacao interna em curso':.65,'Em negociacao':.80,'Contrato assinado':1};
var SEG_C={HOF:'#b06aff','Oral Care':'#3fa9ff',Equipamentos:'#2cd98a',FRANCHISING:'#ffb020',Insumos:'#40d4f5',Alinhadores:'#e070ff'};
var STATUS_C={Ativa:'#3fa9ff',Congelada:'#ffb020',Perdida:'#ff4d4d',Ganha:'#10d4a0'};
var PRIO_ORD={URGENTE:0,GANHO:1,ALTA:2,MEDIA:3,BAIXA:4};
var PRIO_LBL={URGENTE:'Urgente',ALTA:'Alta',MEDIA:'Media',GANHO:'Ganho',BAIXA:'Baixa'};
var PRIO_C={URGENTE:'#ff4d4d',ALTA:'#ff8c2a',MEDIA:'#2cd98a',GANHO:'#10d4a0',BAIXA:'#555e76'};
var ETAPA_SEQ=[
  {v:'Mapeada',l:'Mapeada',n:1},{v:'Contato Iniciado',l:'Contato',n:2},
  {v:'Reuniao agendada',l:'Reun. Ag.',n:3},{v:'Reuniao realizada',l:'Reun. Rl.',n:4},
  {v:'Proposta em elaboracao',l:'Prop. El.',n:5},{v:'Proposta apresentada',l:'Prop. Ap.',n:6},
  {v:'Aprovacao interna em curso',l:'Aprovação',n:7},{v:'Em negociacao',l:'Negoc.',n:8},
  {v:'Contrato assinado',l:'Contrato',n:9}
];

</script>
<script id="dataScript">
var DEFAULT_DATA=[
  /* HOF */
  {id:1, n:'ABBVIE ALLERGAN',     s:'HOF',  porte:'GG',     e:'Contrato assinado',          status:'Ganha',    motivo:'', revisao:'', p:250000, v26:450000, pr:'URGENTE', pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Juliana', obs:'2-02 em contato com Juliana, aguardando reunião com montadora'},
  {id:2, n:'AESKINS',             s:'HOF',  porte:'MÉDIA',  e:'Proposta apresentada',       status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230,  pr:'ALTA',    pz:'09/05/2026', a:'Follow-up 48h — pressionar decisão', resp:'Patricia Bella Costa', cont:'', obs:'25-02 realizada reuniao com Guilherme, aguardando devolutiva'},
  {id:3, n:'AIRELA',              s:'HOF',  porte:'MÉDIA',  e:'Reuniao agendada',           status:'Ativa',    motivo:'', revisao:'', p:0,      v26:0,      pr:'ALTA',    pz:'09/05/2026', a:'Confirmar reunião e preparar pitch', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:4, n:'ALUR MEDICAL',        s:'HOF',  porte:'MÉDIA',  e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:250000, v26:64350,  pr:'MEDIA',   pz:'24/05/2026', a:'Agendar reunião diagnóstico', resp:'Patricia Bella Costa', cont:'Daniela', obs:'23-02 em contato Daniela, aguardando devolutivas'},
  {id:5, n:'ANNA PEGOVA',         s:'HOF',  porte:'GRANDE', e:'Mapeada',                    status:'Congelada',motivo:'', revisao:'01/06/2026', p:0, v26:76900, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar — novo approach', resp:'Patricia Bella Costa', cont:'Kevin Zehil', obs:'Teve prejuízo no evento 2025, aguardando devolutiva sobre benefícios'},
  {id:6, n:'BIOTEC',              s:'HOF',  porte:'PEQUENA',e:'Reuniao agendada',           status:'Congelada',motivo:'', revisao:'15/05/2026', p:0, v26:18900, pr:'ALTA', pz:'09/05/2026', a:'Confirmar reunião — empresa congelada', resp:'Patricia Bella Costa', cont:'Gisele', obs:'23-02 em contato com Gisele'},
  {id:7, n:'BLAU FARMACEUTICA',   s:'HOF',  porte:'MÉDIA',  e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230,  pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — prazo', resp:'Patricia Bella Costa', cont:'Melina', obs:'12-02 empresa não possui budget para 2026'},
  {id:8, n:'CIMED fios',          s:'HOF',  porte:'GRANDE', e:'Proposta em elaboracao',     status:'Congelada',motivo:'', revisao:'30/04/2026', p:500000, v26:0, pr:'ALTA', pz:'09/05/2026', a:'Finalizar proposta após definição do ZECA', resp:'Patricia Bella Costa', cont:'Cimed', obs:'Definição do ZECA pendente'},
  {id:9, n:'DERMA DREAM',         s:'HOF',  porte:'MÉDIA',  e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:250000, v26:0,      pr:'MEDIA',   pz:'24/05/2026', a:'Agendar reunião diagnóstico', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:10,n:'EVO PHARMA',          s:'HOF',  porte:'MÉDIA',  e:'Proposta apresentada',       status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230,  pr:'ALTA',    pz:'09/05/2026', a:'Follow-up — aguardar aprovação da diretoria', resp:'Patricia Bella Costa', cont:'Raquel', obs:'18-02 Raquel informou interesse na cota prata, pediu live injection'},
  {id:11,n:'GALDERMA',            s:'HOF',  porte:'GG',     e:'Em negociacao',              status:'Ativa',    motivo:'', revisao:'', p:500000, v26:99000,  pr:'URGENTE', pz:'01/05/2026', a:'Acompanhar documentação e assinar contrato', resp:'Patricia Bella Costa', cont:'Guilherme', obs:'17-02 fechado cota ouro'},
  {id:12,n:'GRUPO MEDSYSTEMS',    s:'HOF',  porte:'MÉDIA',  e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:120000, v26:0,      pr:'MEDIA',   pz:'24/05/2026', a:'Agendar reunião diagnóstico', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:13,n:'ILIKIA',              s:'HOF',  porte:'MÉDIA',  e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:250000, v26:0,      pr:'ALTA',    pz:'09/05/2026', a:'Agendar reunião de retorno — aguardando 2026', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:14,n:'MERZ',                s:'HOF',  porte:'GRANDE', e:'Proposta em elaboracao',     status:'Perdida',  motivo:'Timing', revisao:'', p:500000, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar — interesse no Educacional', resp:'Patricia Bella Costa', cont:'Juliana', obs:'Não vai ao OdontoConf mas tem interesse em Educacional'},
  {id:15,n:'PHARMAESTHETICS',     s:'HOF',  porte:'MÉDIA',  e:'Aprovacao interna em curso', status:'Ativa',    motivo:'', revisao:'', p:250000, v26:99000,  pr:'URGENTE', pz:'01/05/2026', a:'Monitorar aprovação interna — aguardar devolutiva', resp:'Patricia Bella Costa', cont:'Pharmaesthetics', obs:'16/02 negociação cota ouro, 70k + 20 em produtos'},
  {id:16,n:'PHD DO BRASIL',       s:'HOF',  porte:'MÉDIA',  e:'Em negociacao',              status:'Ativa',    motivo:'', revisao:'', p:120000, v26:120000, pr:'URGENTE', pz:'01/05/2026', a:'Acompanhar validação jurídica e assinar', resp:'Patricia Bella Costa', cont:'', obs:'27/11 Validação do Jurídico'},
  {id:17,n:'RENNOVA',             s:'HOF',  porte:'GRANDE', e:'Proposta em elaboracao',     status:'Ativa',    motivo:'', revisao:'', p:500000, v26:76900,  pr:'ALTA',    pz:'09/05/2026', a:'Agendar reunião de retorno 2026', resp:'Patricia Bella Costa', cont:'Rennova', obs:''},
  {id:18,n:'SINCLAIR',            s:'HOF',  porte:'MÉDIA',  e:'Reuniao agendada',           status:'Perdida',  motivo:'Sem budget', revisao:'', p:250000, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar em 90 dias', resp:'Patricia Bella Costa', cont:'Sinclair', obs:'Proposta encaminhada para Margareth em 13/10'},
  {id:19,n:'MTO IMPORTADORA',     s:'HOF',  porte:'MÉDIA',  e:'Mapeada',                    status:'Perdida',  motivo:'Sem budget', revisao:'', p:250000, v26:76900, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar — novo approach', resp:'Patricia Bella Costa', cont:'REVANESSE', obs:'19/11 Raquel informou que não têm condições de participar em 2026'},
  /* Oral Care */
  {id:20,n:'CURAPROX',            s:'Oral Care',porte:'GRANDE',e:'Contrato assinado',       status:'Ganha',    motivo:'', revisao:'', p:750000, v26:0,     pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Gabriela Victorelli', cont:'Hugo', obs:'Isenção de custo'},
  {id:21,n:'CIMED',               s:'Oral Care',porte:'MÉDIA', e:'Mapeada',                 status:'Ativa',    motivo:'', revisao:'', p:250000, v26:0,     pr:'MEDIA',   pz:'24/05/2026', a:'Iniciar contato — e-mail + WhatsApp', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:22,n:'COLGATE PALMOLIVE',   s:'Oral Care',porte:'GG',    e:'Contato Iniciado',        status:'Perdida',  motivo:'Sem interesse', revisao:'', p:0, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar — novo approach', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:23,n:'DENTALCLEAN',         s:'Oral Care',porte:'MÉDIA', e:'Reuniao realizada',       status:'Perdida',  motivo:'Sem budget', revisao:'', p:150000, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reconquistar — novo approach', resp:'Patricia Bella Costa', cont:'Dental Clean', obs:'04/11 Gabriela Martins declinou por não ter verba aprovada'},
  {id:24,n:'GUM',                 s:'Oral Care',porte:'PEQUENA',e:'Contrato assinado',      status:'Ganha',    motivo:'', revisao:'', p:0,      v26:14900, pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Gum', obs:'Plataforma 04/11'},
  {id:25,n:'HALEON Sensodyne',    s:'Oral Care',porte:'GRANDE',e:'Proposta apresentada',    status:'Congelada',motivo:'', revisao:'15/05/2026', p:250000, v26:0, pr:'ALTA', pz:'09/05/2026', a:'Follow-up após retorno da empresa', resp:'Patricia Bella Costa', cont:'Alexandre', obs:'25/11 proposta enviada, aguardando devolutivas'},
  {id:26,n:'N&W + EDEL WHITE',    s:'Oral Care',porte:'MÉDIA', e:'Em negociacao',           status:'Ativa',    motivo:'', revisao:'', p:250000, v26:150000,pr:'URGENTE', pz:'01/05/2026', a:'Validar jurídico e coletar assinatura', resp:'Patricia Bella Costa', cont:'Daniel', obs:'19/02 interesse em cota platina 160k + 10k em materiais'},
  {id:27,n:'ORAL B',              s:'Oral Care',porte:'GRANDE',e:'Proposta apresentada',    status:'Congelada',motivo:'', revisao:'01/06/2026', p:250000, v26:0, pr:'ALTA', pz:'09/05/2026', a:'Reconectar — empresa reavaliando investimento em odonto', resp:'Patricia Bella Costa', cont:'Silvia', obs:'27/11 não investirá em odonto em 2026'},
  {id:28,n:'ORALFLIX',            s:'Oral Care',porte:'PEQUENA',e:'Proposta apresentada',   status:'Ativa',    motivo:'', revisao:'', p:0,      v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — aguardar resposta do Henrique', resp:'', cont:'Oralflix', obs:'17-02 Henrique analisando participação'},
  {id:29,n:'ORAL WAVE',           s:'Oral Care',porte:'PEQUENA',e:'Mapeada',                status:'Ativa',    motivo:'', revisao:'', p:0,      v26:64900, pr:'ALTA',    pz:'09/05/2026', a:'Agendar reunião de retorno 2026', resp:'Gabriela Sander', cont:'', obs:'Evento online confirmado'},
  {id:30,n:'LISTERINE',           s:'Oral Care',porte:'MÉDIA', e:'Proposta apresentada',    status:'Congelada',motivo:'', revisao:'15/06/2026', p:0, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reconectar após período de avaliação', resp:'Patricia Bella Costa', cont:'', obs:'19/12 enviado email central'},
  /* Equipamentos */
  {id:31,n:'3SHAPE',              s:'Equipamentos',porte:'MÉDIA', e:'Em negociacao',        status:'Ativa',    motivo:'', revisao:'', p:50000,  v26:14900, pr:'URGENTE', pz:'01/05/2026', a:'Fechar valores e contrapartidas', resp:'Patricia Bella Costa', cont:'3Shape', obs:'17-02 Em contato com Glaucia, aguardando devolutiva'},
  {id:32,n:'CARESTREAM DENTAL',   s:'Equipamentos',porte:'GRANDE',e:'Em negociacao',        status:'Ativa',    motivo:'', revisao:'', p:120000, v26:18900, pr:'URGENTE', pz:'01/05/2026', a:'Acompanhar documentação e assinar', resp:'Patricia Bella Costa', cont:'', obs:'08/01 irá participar, quer lugar melhor de stand'},
  {id:33,n:'CRISTOFOLI',          s:'Equipamentos',porte:'MÉDIA', e:'Proposta apresentada', status:'Ativa',    motivo:'', revisao:'', p:75000,  v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — prazo 06/02', resp:'Patricia Bella Costa', cont:'', obs:'06/02'},
  {id:34,n:'Dentsply Sirona',     s:'Equipamentos',porte:'GG',    e:'Reuniao realizada',    status:'Ativa',    motivo:'', revisao:'', p:1000000,v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Agendar reunião de retorno — CIOSP', resp:'Patricia Bella Costa', cont:'Nathalie Rodrigues', obs:'Quer reunião no CIOSP'},
  {id:35,n:'ENVISTA',             s:'Equipamentos',porte:'GRANDE',e:'Proposta apresentada', status:'Ativa',    motivo:'', revisao:'', p:500000, v26:0,     pr:'ALTA',    pz:'09/05/2026', a:'Follow-up 48h — pressionar decisão', resp:'Patricia Bella Costa', cont:'Envista', obs:'19-02 aguardando devolutiva com Patricia'},
  {id:36,n:'GNATUS',              s:'Equipamentos',porte:'GRANDE',e:'Reuniao realizada',    status:'Ativa',    motivo:'', revisao:'', p:250000, v26:0,     pr:'ALTA',    pz:'09/05/2026', a:'Elaborar e enviar proposta (7 dias)', resp:'Gabriela Victorelli', cont:'', obs:''},
  {id:37,n:'IMPLANTEC',           s:'Equipamentos',porte:'MÉDIA', e:'Contrato assinado',    status:'Ganha',    motivo:'', revisao:'', p:0,      v26:42900, pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Jarbas', obs:'Plataforma 04/11'},
  {id:38,n:'OLSEN',               s:'Equipamentos',porte:'MÉDIA', e:'Mapeada',              status:'Ativa',    motivo:'', revisao:'', p:250000, v26:0,     pr:'MEDIA',   pz:'24/05/2026', a:'Reforçar contato e agendar reunião', resp:'Patricia Bella Costa', cont:'Olsen', obs:'26/11 enviado email, aguardar devolutivas'},
  {id:39,n:'PLAMNECA',            s:'Equipamentos',porte:'GRANDE',e:'Em negociacao',        status:'Ativa',    motivo:'', revisao:'', p:0,      v26:54230, pr:'URGENTE', pz:'01/05/2026', a:'Validar jurídico — aguardar devolutiva da Matriz', resp:'Patricia Bella Costa', cont:'Maycon', obs:'Espera devolutiva da Matriz para prazos de pagamento'},
  {id:40,n:'WOSON INDUSTRIA',     s:'Equipamentos',porte:'GRANDE',e:'Reuniao realizada',    status:'Ativa',    motivo:'', revisao:'', p:250000, v26:150000,pr:'ALTA',    pz:'09/05/2026', a:'Elaborar proposta — workshop em março', resp:'Patricia Bella Costa', cont:'Carla', obs:'09/02 solicitou agenda em março para workshop'},
  {id:41,n:'W&H',                 s:'Equipamentos',porte:'MÉDIA', e:'Contrato assinado',    status:'Ganha',    motivo:'', revisao:'', p:0,      v26:42900, pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Gabriela Victorelli', cont:'Marcelo Silva', obs:'Plataforma assinada'},
  /* Alinhadores */
  {id:42,n:'ADITEK / ANGEL ALIGNER',s:'Alinhadores',porte:'GRANDE',e:'Mapeada',            status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230, pr:'MEDIA',   pz:'24/05/2026', a:'Iniciar contato persistente — Fernando não responde', resp:'Patricia Bella Costa', cont:'Aditek/AngelAligner', obs:'24/10 Fernando não responde mensagens e não atende ligação'},
  {id:43,n:'ALIGN',               s:'Alinhadores',porte:'GRANDE',e:'Contato Iniciado',      status:'Congelada',motivo:'', revisao:'01/06/2026', p:250000, v26:76900, pr:'BAIXA', pz:'23/06/2026', a:'Reconectar após evento próprio', resp:'Patricia Bella Costa', cont:'Tamara Kulb', obs:'09-02 Paty conversou no CIOSP, fará evento próprio sem previsão'},
  {id:44,n:'CLEAR CORRECT',       s:'Alinhadores',porte:'MÉDIA', e:'Proposta apresentada', status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — proposta apresentada para Fernanda', resp:'Patricia Bella Costa', cont:'Fernanda Santini', obs:'Apresentada proposta Fernanda Santini'},
  /* Franchising */
  {id:45,n:'AMIL DENTAL',         s:'FRANCHISING',porte:'MÉDIA', e:'Contato Iniciado',     status:'Ativa',    motivo:'', revisao:'', p:0,      v26:0,     pr:'MEDIA',   pz:'24/05/2026', a:'Agendar reunião diagnóstico', resp:'Patricia Bella Costa', cont:'', obs:''},
  {id:46,n:'CLINICORP',           s:'FRANCHISING',porte:'MÉDIA', e:'Proposta apresentada', status:'Perdida',  motivo:'Sem interesse', revisao:'', p:250000, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Reativar com nova proposta em 90 dias', resp:'Patricia Bella Costa', cont:'', obs:'26/11 declinaram propostas Odonto Conf e Branded'},
  {id:47,n:'ODONTOCLINIC (franq. peq.)',s:'FRANCHISING',porte:'PEQUENA',e:'Reuniao realizada',status:'Ativa',motivo:'', revisao:'', p:0,      v26:99000, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — proposta apresentada 20-02', resp:'', cont:'', obs:'20-02 reunião realizada, propostas apresentadas'},
  {id:48,n:'ODONTOCLINIC (franq. grande)',s:'FRANCHISING',porte:'GRANDE',e:'Reuniao realizada',status:'Ativa',motivo:'', revisao:'', p:750000, v26:0,    pr:'ALTA',    pz:'09/05/2026', a:'Elaborar e enviar proposta (7 dias)', resp:'Gabriela Victorelli', cont:'', obs:''},
  {id:49,n:'ODONTOPREV',          s:'FRANCHISING',porte:'GRANDE',e:'Proposta apresentada', status:'Ativa',    motivo:'', revisao:'', p:750000, v26:0,     pr:'ALTA',    pz:'09/05/2026', a:'Follow-up 48h — pressionar decisão', resp:'Gabriela Victorelli', cont:'', obs:''},
  {id:50,n:'SORRI FÁCIL',         s:'FRANCHISING',porte:'PEQUENA',e:'Em negociacao',        status:'Ativa',    motivo:'', revisao:'', p:0,      v26:54230, pr:'URGENTE', pz:'01/05/2026', a:'Acompanhar documentação e assinar', resp:'', cont:'', obs:'Gabi — documentação em andamento'},
  {id:51,n:'REDE ORTO',           s:'FRANCHISING',porte:'PEQUENA',e:'Contato Iniciado',     status:'Congelada',motivo:'', revisao:'01/06/2026', p:0, v26:0, pr:'BAIXA', pz:'23/06/2026', a:'Retornar em junho 2026', resp:'', cont:'Fabiano Bino', obs:'03/12 Fabiano pediu para retornar em janeiro 2026'},
  /* Insumos */
  {id:52,n:'3M / Solvetum',       s:'Insumos',porte:'GG',    e:'Proposta apresentada',      status:'Ativa',    motivo:'', revisao:'', p:0,      v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — proposta enviada por Gabi', resp:'Gabriela Victorelli', cont:'Andrea', obs:'Gabi enviou proposta'},
  {id:53,n:'BAUSCH',              s:'Insumos',porte:'MÉDIA', e:'Contrato assinado',          status:'Ganha',    motivo:'', revisao:'', p:40000,  v26:14900, pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'BAUSCH', obs:'Plataforma 29/10'},
  {id:54,n:'COLTENE',             s:'Insumos',porte:'MÉDIA', e:'Em negociacao',              status:'Ativa',    motivo:'', revisao:'', p:25000,  v26:18900, pr:'URGENTE', pz:'01/05/2026', a:'Validar jurídico — aguardar pós CIOSP', resp:'Patricia Bella Costa', cont:'COLTENE', obs:'08/01 irá participar, aguardar pós CIOSP'},
  {id:55,n:'FGM Dental Group',    s:'Insumos',porte:'GRANDE',e:'Contrato assinado',          status:'Ganha',    motivo:'', revisao:'', p:0,      v26:120000,pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Juliana Felício', obs:'23-02 reunião com jurídico'},
  {id:56,n:'IVOCLAR',             s:'Insumos',porte:'MÉDIA', e:'Contato Iniciado',           status:'Ativa',    motivo:'', revisao:'', p:120000, v26:54230, pr:'ALTA',    pz:'09/05/2026', a:'Pressionar decisão — aguardar devolutiva Larissa', resp:'Patricia Bella Costa', cont:'Ivoclar', obs:'19-02 em contato com Larissa'},
  {id:57,n:'KG SORENSEN',         s:'Insumos',porte:'MÉDIA', e:'Proposta apresentada',       status:'Congelada',motivo:'', revisao:'15/05/2026', p:50000, v26:54230, pr:'BAIXA', pz:'23/06/2026', a:'Reativar — Rodrigo quer entrar em parceria com dental', resp:'', cont:'KG Sorensen', obs:'12-02 Rodrigo quer entrar com alguma dental em parceria'},
  {id:58,n:'KOTA IMPORTS',        s:'Insumos',porte:'MÉDIA', e:'Proposta em elaboracao',     status:'Ativa',    motivo:'', revisao:'', p:250000, v26:54230, pr:'BAIXA',   pz:'23/06/2026', a:'Aguardar devolutiva — reunião realizada 23-02', resp:'', cont:'', obs:'23-02 reunião com carol e fabiana, reenviado apresentação'},
  {id:59,n:'KULZER',              s:'Insumos',porte:'MÉDIA', e:'Contrato assinado',           status:'Ganha',    motivo:'', revisao:'', p:120000, v26:64900, pr:'GANHO',   pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Pamella', obs:'Assinado'},
  {id:60,n:'MAQUIRA',             s:'Insumos',porte:'MÉDIA', e:'Contrato assinado',           status:'Ativa',    motivo:'', revisao:'', p:120000, v26:54230, pr:'URGENTE', pz:'01/05/2026', a:'Confirmar kick-off e onboarding', resp:'Patricia Bella Costa', cont:'Maquira', obs:'18-02 em contato com Carlos, aguardando devolutivas'},
  {id:61,n:'ULTRADENT',           s:'Insumos',porte:'MÉDIA', e:'Em negociacao',              status:'Ativa',    motivo:'', revisao:'', p:250000, v26:99000, pr:'URGENTE', pz:'01/05/2026', a:'Fechar valores e contrapartidas', resp:'Gabriela Victorelli', cont:'Eduardo Braga', obs:'26/02 aguardando parecer do Gabriel quanto à participação'},
  {id:62,n:'VOCO DENTAL',         s:'Insumos',porte:'MÉDIA', e:'Aprovacao interna em curso', status:'Ativa',    motivo:'', revisao:'', p:120000, v26:20000, pr:'URGENTE', pz:'01/05/2026', a:'Acompanhar aprovação e assinar', resp:'', cont:'Ana Júlia / Roberto', obs:'24/11 proposta em análise com a diretoria'},
];
</script>
<script>
var nextId=200, D=[], editingId=null, tlId=null;
var activeSeg=new Set(['HOF','Oral Care','Equipamentos','FRANCHISING','Insumos','Alinhadores']);
var activeSt=new Set(['Ativa','Congelada','Perdida','Ganha']);
var activePrio=new Set(['URGENTE','ALTA','MEDIA','GANHO','BAIXA']);
var sortKey='pr', sortDir=1;

function nowISO(){return new Date().toISOString();}
function fmtDT(iso){if(!iso)return '';var d=new Date(iso);return d.toLocaleDateString('pt-BR',{day:'2-digit',month:'2-digit',year:'numeric'})+' '+d.toLocaleTimeString('pt-BR',{hour:'2-digit',minute:'2-digit'});}
function fmtD(iso){if(!iso)return '';var d=new Date(iso);return d.toLocaleDateString('pt-BR',{day:'2-digit',month:'2-digit',year:'2-digit'});}
function brl(v){return v?'R$\u00a0'+Math.round(v).toLocaleString('pt-BR'):'—';}
function esc(s){return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');}

function addHist(d,type,from,to,note){
  if(!d.hist)d.hist=[];
  d.hist.unshift({type:type,from:String(from||'—'),to:String(to||'—'),note:note||'',ts:nowISO()});
}
function ensureCriacao(d){
  if(!d.hist)d.hist=[];
  if(!d.hist.find(function(h){return h.type==='criacao';}))
    d.hist.push({type:'criacao',from:'',to:d.n,note:'Empresa adicionada ao pipeline',ts:d.criadoEm||'2026-04-24T00:00:00.000Z'});
}

function calc(){D.forEach(function(d){d.prob=PESOS[d.e]||0;d.pond=Math.round((d.p||0)*(d.prob||0));});}

function loadData(){
  var s=localStorage.getItem('mandic_v4');
  if(s){try{D=JSON.parse(s);nextId=Math.max.apply(null,D.map(function(d){return d.id||0}))+1;return;}catch(e){}}
  D=JSON.parse(JSON.stringify(DEFAULT_DATA));nextId=200;
}
function saveData(){
  calc();localStorage.setItem('mandic_v4',JSON.stringify(D));
  var el=document.getElementById('savedInd');el.classList.add('show');
  setTimeout(function(){el.classList.remove('show');},2000);
}
function resetData(){
  if(!confirm('Apagar todas as alterações e voltar aos dados originais?'))return;
  localStorage.removeItem('mandic_v4');loadData();render();showToast('Dados restaurados',STATUS_C.Ativa);
}

function tog(type,val,btn){
  var set=type==='seg'?activeSeg:type==='status'?activeSt:activePrio;
  if(set.has(val)){set.delete(val);btn.classList.remove('on');}else{set.add(val);btn.classList.add('on');}
  render();
}
function srt(key){
  if(sortKey===key)sortDir*=-1;else{sortKey=key;sortDir=1;}
  document.querySelectorAll('th').forEach(function(t){t.classList.remove('sorted');});
  var idx=['n','s','e','prob','status','p','pond','pr'].indexOf(key);
  if(idx>=0)document.querySelectorAll('th')[idx].classList.add('sorted');
  render();
}
function filtered(){
  var q=(document.getElementById('srch').value||'').toLowerCase().trim();
  return D.filter(function(d){
    return activeSeg.has(d.s)&&activeSt.has(d.status)&&activePrio.has(d.pr)&&
      (!q||(d.n||'').toLowerCase().includes(q)||(d.s||'').toLowerCase().includes(q)||
       (d.e||'').toLowerCase().includes(q)||(d.status||'').toLowerCase().includes(q));
  });
}

/* ── KPIs ── */
function renderKpis(rows){
  var urg=rows.filter(function(r){return r.pr==='URGENTE';}).length;
  var alta=rows.filter(function(r){return r.pr==='ALTA';}).length;
  var ganho=rows.filter(function(r){return r.status==='Ganha';}).length;
  var cong=rows.filter(function(r){return r.status==='Congelada';}).length;
  var tp=rows.reduce(function(a,r){return a+r.p;},0);
  var tpd=rows.reduce(function(a,r){return a+r.pond;},0);
  var conv=tp>0?Math.round(tpd/tp*100):0;
  var cards=[
    {c:'kt',l:'Empresas',v:''+rows.length,sb:'no pipeline'},
    {c:'kb',l:'Pot. bruto',v:brl(tp),sb:'total'},
    {c:'kp',l:'Ponderado',v:brl(tpd),sb:'taxa '+conv+'%'},
    {c:'ku',l:'Urgentes',v:''+urg,sb:'≤ 7 dias'},
    {c:'ka',l:'Congeladas',v:''+cong,sb:'precisam revisão'},
    {c:'kg',l:'Ganhas',v:''+ganho,sb:'contratos fechados'},
  ];
  document.getElementById('kpis').innerHTML=cards.map(function(c){
    var sm=c.v.length>9;
    return '<div class="kcard '+c.c+'"><div class="kl">'+c.l+'</div><div class="kv'+(sm?' sm':'')+'">'+c.v+'</div><div class="ks">'+c.sb+'</div></div>';
  }).join('');
}

/* ── CHARTS ── */
function mkBar(lbl,w,col,val){
  return '<div class="brow"><div class="blbl" title="'+lbl+'">'+lbl+'</div>'
    +'<div class="btrk"><div class="bfil" style="width:'+w+'%;background:'+col+'"></div></div>'
    +'<div class="bval">'+val+'</div></div>';
}
function renderCharts(rows){
  var sd={};rows.forEach(function(r){if(!sd[r.s])sd[r.s]=0;sd[r.s]+=r.pond;});
  var se=Object.entries(sd).sort(function(a,b){return b[1]-a[1];});
  var mx=se.length?se[0][1]:1;
  document.getElementById('cSeg').innerHTML=se.length
    ?se.map(function(e){return mkBar(e[0],mx>0?Math.round(e[1]/mx*100):0,SEG_C[e[0]]||'#888',brl(e[1]));}).join('')
    :'<div style="color:var(--txt3);font-size:11px;padding:6px">Sem dados</div>';
  var stc={Ativa:0,Congelada:0,Perdida:0,Ganha:0};
  rows.forEach(function(r){if(stc[r.status]!==undefined)stc[r.status]++;});
  var tot=Object.values(stc).reduce(function(a,b){return a+b;},0)||1;
  document.getElementById('cStatus').innerHTML=Object.entries(stc).filter(function(e){return e[1]>0;})
    .map(function(e){return mkBar(e[0],Math.round(e[1]/tot*100),STATUS_C[e[0]]||'#888',e[1]+' ('+Math.round(e[1]/tot*100)+'%)');}).join('')
    ||'<div style="color:var(--txt3);font-size:11px;padding:6px">Sem dados</div>';
}

/* ── TABLE ── */
function renderTable(rows){
  var tb=document.getElementById('tb');
  var STATUS_ORD={Ativa:0,Congelada:1,Ganha:2,Perdida:3};
  var sorted=rows.slice().sort(function(a,b){
    if(sortKey==='status')return((STATUS_ORD[a.status]||0)-(STATUS_ORD[b.status]||0))*sortDir||b.pond-a.pond;
    var av=sortKey==='pr'?(PRIO_ORD[a.pr]||5):(a[sortKey]||0);
    var bv=sortKey==='pr'?(PRIO_ORD[b.pr]||5):(b[sortKey]||0);
    if(typeof av==='string')av=av.toLowerCase();if(typeof bv==='string')bv=bv.toLowerCase();
    if(av<bv)return -1*sortDir;if(av>bv)return 1*sortDir;return b.pond-a.pond;
  });
  document.getElementById('rcnt').textContent=rows.length+' empresa'+(rows.length!==1?'s':'');
  document.getElementById('ftxt').textContent=rows.length+' de '+D.length+' visíveis';
  if(!sorted.length){tb.innerHTML='<tr><td colspan="10"><div class="empty">Nenhuma empresa para os filtros selecionados.</div></td></tr>';return;}

  var SBC={URGENTE:'pb-u',ALTA:'pb-a',MEDIA:'pb-m',GANHO:'pb-g',BAIXA:'pb-b'};
  var SSC={Ativa:'sb-a',Congelada:'sb-c',Perdida:'sb-p',Ganha:'sb-g'};
  var EOPT=[{v:'',l:'— sem etapa —'},{v:'Mapeada',l:'1·Mapeada(2%)'},{v:'Contato Iniciado',l:'2·Contato(5%)'},{v:'Reuniao agendada',l:'3·Reun.Ag.(15%)'},{v:'Reuniao realizada',l:'4·Reun.Rl.(25%)'},{v:'Proposta em elaboracao',l:'5·Prop.El.(35%)'},{v:'Proposta apresentada',l:'6·Prop.Ap.(50%)'},{v:'Aprovacao interna em curso',l:'7·Aprov.(65%)'},{v:'Em negociacao',l:'8·Negoc.(80%)'},{v:'Contrato assinado',l:'9·Contrato(100%)'}];
  var SOPT=['Ativa','Congelada','Perdida','Ganha'];

  function mkSel(fld,val,opts,id){
    var o=opts.map(function(o){var v=typeof o==='object'?o.v:o,l=typeof o==='object'?o.l:o;return '<option value="'+v+'"'+(v===val?' selected':'')+'>'+(l||'—')+'</option>';}).join('');
    var extra=fld==='pr'?' pv-'+val:'';
    return '<select class="isel'+extra+'" data-id="'+id+'" data-fld="'+fld+'" onchange="inlineUpd(this)" onclick="event.stopPropagation()">'+o+'</select>';
  }
  function mkNum(val,id){
    return '<input type="number" class="isel" style="width:100%;text-align:right;-moz-appearance:textfield" min="0" step="1000" value="'+(val||0)+'" data-id="'+id+'" data-fld="p" onchange="inlineUpd(this)" onclick="event.stopPropagation()">';
  }

  var POPT=['URGENTE','ALTA','MEDIA','GANHO','BAIXA'];

  tb.innerHTML=sorted.map(function(r){
    var prob=r.prob>0?Math.round(r.prob*100)+'%':'—';
    var ac=(r.a||r.obs||'—').substring(0,36)+(((r.a||r.obs||'').length>36)?'…':'');
    var hc=(r.hist&&r.hist.length)||0;
    var hbadge=hc>0?'<span class="tl-count">'+hc+'</span>':'';
    return '<tr ondblclick="openModal('+r.id+')" style="cursor:pointer" title="Duplo clique para editar">'
      +'<td><span class="cn">'+esc(r.n)+'</span></td>'
      +'<td><span class="seg-dot" style="background:'+(SEG_C[r.s]||'#888')+'"></span>'+r.s+'</td>'
      +'<td>'+mkSel('e',r.e||'',EOPT,r.id)+'</td>'
      +'<td style="text-align:center"><span class="prob-tag">'+prob+'</span></td>'
      +'<td>'+mkSel('status',r.status||'Ativa',SOPT,r.id)+'</td>'
      +'<td>'+mkNum(r.p,r.id)+'</td>'
      +'<td style="text-align:right;font-family:\'IBM Plex Mono\',monospace;font-size:11px">'+(r.pond>0?brl(r.pond):'—')+'</td>'
      +'<td>'+mkSel('pr',r.pr||'MEDIA',POPT,r.id)+'</td>'
      +'<td style="font-size:11px;color:var(--txt2)" title="'+(r.a||r.obs||'')+'">'+ac+'</td>'
      +'<td style="text-align:center"><button class="tl-btn" onclick="event.stopPropagation();openTl('+r.id+')">&#9201;'+hbadge+'</button></td>'
      +'</tr>';
  }).join('');
}

/* ── INLINE EDIT ── */
function inlineUpd(el){
  var id=parseInt(el.getAttribute('data-id'));
  var fld=el.getAttribute('data-fld');
  var d=D.find(function(x){return x.id===id;});if(!d)return;
  var old=d[fld]; var val=el.value;
  if(fld==='p')val=parseInt(val)||0;
  if(String(val)===String(old))return;

  ensureCriacao(d);
  if(fld==='e')   addHist(d,'etapa',  old||'—',val||'—','');
  if(fld==='status')addHist(d,'status',old||'—',val||'—',fld==='status'&&val==='Perdida'?d.motivo||'':'');
  if(fld==='p')   addHist(d,'potencial',brl(old),brl(val),'');

  d[fld]=val;
  if(fld==='pr'){['URGENTE','ALTA','MEDIA','GANHO','BAIXA'].forEach(function(p){el.classList.remove('pv-'+p);});el.classList.add('pv-'+val);}
  if(fld==='e'){d.prob=PESOS[val]||0;d.pond=Math.round((d.p||0)*d.prob);if(val==='Contrato assinado'){addHist(d,'status',d.status,'Ganha','Auto: etapa 9');d.status='Ganha';}}
  if(fld==='p'){d.prob=PESOS[d.e]||0;d.pond=Math.round(val*(d.prob||0));}
  if(fld==='status'&&val==='Ganha')d.e='Contrato assinado';

  saveData();
  showToast({e:'Etapa',status:'Status',p:'Potencial',pr:'Prioridade'}[fld]+' atualizado',STATUS_C.Ativa);
  if(fld==='e'||fld==='status'||fld==='p')render();
}

/* ── RENDER ── */
function render(){calc();var rows=filtered();renderKpis(rows);renderCharts(rows);renderTable(rows);}

/* ── EDIT MODAL ── */
function onStatus(){
  var v=document.getElementById('f-status').value;
  document.getElementById('motivoWrap').classList.toggle('show',v==='Perdida');
  document.getElementById('revisaoWrap').classList.toggle('show',v==='Congelada');
  if(v==='Ganha')document.getElementById('f-e').value='Contrato assinado';
}
function onEtapa(){
  if(document.getElementById('f-e').value==='Contrato assinado'){document.getElementById('f-status').value='Ganha';onStatus();}
}
function openModal(id){
  editingId=id;
  var d=id?D.find(function(x){return x.id===id;}):null;
  document.getElementById('mTitle').textContent=d?'Editar: '+d.n:'Nova empresa';
  document.getElementById('deleteBtn').style.display=d?'block':'none';
  var def={n:'',s:'HOF',porte:'',e:'',status:'Ativa',motivo:'',revisao:'',p:0,v26:0,pr:'MEDIA',pz:'',a:'',resp:'',cont:'',obs:''};
  if(d)Object.keys(def).forEach(function(k){def[k]=d[k]!==undefined?d[k]:'';});
  ['n','s','porte','e','status','motivo','revisao','p','v26','pr','pz','a','resp','cont','obs'].forEach(function(k){
    var el=document.getElementById('f-'+k);if(el)el.value=def[k]||'';
  });
  onStatus();
  document.getElementById('overlay').classList.add('open');
}
function closeModal(){document.getElementById('overlay').classList.remove('open');editingId=null;}
function saveEntry(){
  var n=(document.getElementById('f-n').value||'').trim();
  if(!n){showToast('Nome obrigatório',PRIO_C.URGENTE);return;}
  var st=document.getElementById('f-status').value;
  var motivo=document.getElementById('f-motivo').value;
  var revisao=(document.getElementById('f-revisao').value||'').trim();
  if(st==='Perdida'&&!motivo){showToast('Motivo da perda obrigatório',PRIO_C.URGENTE);return;}
  if(st==='Congelada'&&!revisao){showToast('Data de revisão obrigatória',PRIO_C.URGENTE);return;}
  var entry={
    id:editingId||nextId++,
    n:n,s:document.getElementById('f-s').value,porte:document.getElementById('f-porte').value,
    e:document.getElementById('f-e').value,status:st,motivo:motivo,revisao:revisao,
    p:parseInt(document.getElementById('f-p').value)||0,v26:parseInt(document.getElementById('f-v26').value)||0,
    pr:document.getElementById('f-pr').value,pz:document.getElementById('f-pz').value,
    a:document.getElementById('f-a').value,resp:document.getElementById('f-resp').value,
    cont:document.getElementById('f-cont').value,obs:document.getElementById('f-obs').value,
  };
  if(editingId){
    var i=D.findIndex(function(x){return x.id===editingId;});
    if(i>=0){
      var old=D[i];entry.hist=old.hist||[];entry.criadoEm=old.criadoEm;
      ensureCriacao(entry);
      if(entry.e!==old.e)addHist(entry,'etapa',old.e||'—',entry.e||'—','');
      if(entry.status!==old.status)addHist(entry,'status',old.status||'—',entry.status,entry.motivo||'');
      if(entry.p!==old.p)addHist(entry,'potencial',brl(old.p),brl(entry.p),'');
      D[i]=entry;
    }
  }else{
    entry.criadoEm=nowISO();
    entry.hist=[{type:'criacao',from:'',to:entry.n,note:'Empresa adicionada ao pipeline',ts:entry.criadoEm}];
    D.push(entry);
  }
  closeModal();saveData();render();
  showToast(editingId?'Empresa atualizada':'Empresa adicionada',STATUS_C.Ganha);
}
function deleteEntry(){
  if(!editingId)return;
  var d=D.find(function(x){return x.id===editingId;});if(!d)return;
  if(!confirm('Excluir "'+d.n+'"?'))return;
  D=D.filter(function(x){return x.id!==editingId;});
  closeModal();saveData();render();showToast('Empresa excluída',PRIO_C.URGENTE);
}

/* ── TIMELINE ── */
function openTl(id){
  tlId=id;
  var d=D.find(function(x){return x.id===id;});if(!d)return;
  ensureCriacao(d);saveData();
  document.getElementById('tlName').textContent=d.n;
  document.getElementById('tlMeta').textContent=(d.s||'—')+' · '+(d.porte||'—')+' · '+(d.resp||'—');
  renderTlFunnel(d);
  renderTlList(d);
  document.getElementById('noteForm').classList.remove('show');
  document.getElementById('tlOverlay').classList.add('open');
}
function closeTl(){document.getElementById('tlOverlay').classList.remove('open');tlId=null;}

function renderTlFunnel(d){
  var curIdx=ETAPA_SEQ.findIndex(function(s){return s.v===d.e;});
  var isPerdida=d.status==='Perdida', isCongelada=d.status==='Congelada';
  var hist=d.hist||[];

  // Build map: etapa value → first date it appeared in hist
  var etapaDate={};
  hist.forEach(function(h){
    if(h.type==='etapa'){
      var key=h.to;
      if(!etapaDate[key]||new Date(h.ts)<new Date(etapaDate[key]))etapaDate[key]=h.ts;
    }
  });
  // Also seed current etapa if no history for it
  if(d.e&&!etapaDate[d.e]&&hist.length){
    var earliest=hist[hist.length-1];etapaDate[d.e]=earliest?earliest.ts:'';
  }

  var html='';
  ETAPA_SEQ.forEach(function(step,i){
    var cls='fstep';
    if(curIdx>=0){
      if(i<curIdx)cls+=' done';
      else if(i===curIdx){cls+=(isPerdida?' lost':isCongelada?' frozen':' current');}
    }
    var dateStr=etapaDate[step.v]?fmtD(etapaDate[step.v]):'';
    html+='<div class="'+cls+'"><div class="fdot">'+step.n+'</div><div class="flbl">'+step.l+'</div><div class="fdate">'+dateStr+'</div></div>';
  });
  document.getElementById('tlFunnel').innerHTML=html;

  var sc=STATUS_C[d.status]||'#888';
  var pills='<div class="tl-pill" style="border-color:'+sc+';color:'+sc+'">'+d.status+(d.motivo?' · '+d.motivo:'')+(d.revisao?' · rev. '+d.revisao:'')+'</div>';
  pills+='<div class="tl-pill">'+Math.round((d.prob||0)*100)+'% probabilidade</div>';
  pills+='<div class="tl-pill">Ponderado: '+brl(d.pond||0)+'</div>';
  if(d.pz)pills+='<div class="tl-pill">Prazo: '+d.pz+'</div>';
  document.getElementById('tlStatusRow').innerHTML=pills;
}

function renderTlList(d){
  var hist=d.hist||[];
  if(!hist.length){document.getElementById('tlList').innerHTML='<div class="tl-empty">Nenhum registro ainda. As próximas alterações de etapa, status e potencial serão registradas automaticamente.</div>';return;}
  var TYPE={etapa:['Etapa','tl-tag-etapa'],status:['Status','tl-tag-status'],potencial:['Potencial','tl-tag-potencial'],nota:['Nota','tl-tag-nota'],criacao:['Criação','tl-tag-criacao']};
  var html='<div class="tl-list">';
  hist.forEach(function(h){
    var ti=TYPE[h.type]||['',''];
    html+='<div class="tl-item ti-'+h.type+'">'
      +'<div class="tl-dot-i"></div>'
      +'<div class="tl-ts">'+fmtDT(h.ts)+'</div>'
      +'<div class="tl-card">'
      +'<span class="tl-tag '+ti[1]+'">'+ti[0]+'</span>';
    if(h.type==='nota'||h.type==='criacao'){
      html+='<div class="tl-note-txt">'+esc(h.note||h.to||'')+'</div>';
    }else{
      html+='<div class="tl-change"><span class="tl-from">'+esc(h.from)+'</span><span class="tl-arrow">→</span><span class="tl-to">'+esc(h.to)+'</span></div>';
      if(h.note)html+='<div class="tl-note-obs">'+esc(h.note)+'</div>';
    }
    html+='</div></div>';
  });
  html+='</div>';
  document.getElementById('tlList').innerHTML=html;
}

function toggleNoteForm(){
  var f=document.getElementById('noteForm');
  f.classList.toggle('show');
  if(f.classList.contains('show')){document.getElementById('noteText').value='';document.getElementById('noteText').focus();}
}
function saveNote(){
  var txt=(document.getElementById('noteText').value||'').trim();if(!txt)return;
  var d=D.find(function(x){return x.id===tlId;});if(!d)return;
  if(!d.hist)d.hist=[];
  d.hist.unshift({type:'nota',from:'',to:'',note:txt,ts:nowISO()});
  saveData();renderTlList(d);renderTlFunnel(d);
  document.getElementById('noteForm').classList.remove('show');
  showToast('Nota adicionada',STATUS_C.Ativa);render();
}

function printTl(){window.print();}

/* ── EXPORT ── */
function exportCSV(){
  var rows=filtered();
  var cols=['Empresa','Segmento','Porte','Etapa','Prob%','Status','Motivo','Data Revisão','Potencial','Ponderado','Prioridade','Prazo','Responsável','Contato','Ação','Obs'];
  var csv=cols.join(';')+'\n';
  rows.forEach(function(r){
    csv+=[r.n,r.s,r.porte||'',r.e||'',Math.round((r.prob||0)*100)+'%',r.status,r.motivo||'',r.revisao||'',r.p||0,r.pond||0,PRIO_LBL[r.pr]||r.pr,r.pz||'',r.resp||'',r.cont||'',(r.a||'').replace(/;/g,' '),(r.obs||'').replace(/[\r\n;]/g,' ')].join(';')+'\n';
  });
  var a=document.createElement('a');
  a.href='data:text/csv;charset=utf-8,\uFEFF'+encodeURIComponent(csv);
  a.download='pipeline_b2b_mandic.csv';a.click();
  showToast('CSV exportado',STATUS_C.Ativa);
}

/* ── TOAST ── */
function showToast(msg,color){
  var t=document.getElementById('toast');
  document.getElementById('toastMsg').textContent=msg;
  document.getElementById('toastDot').style.background=color||STATUS_C.Ganha;
  t.style.transform='translateY(0)';t.style.opacity='1';
  setTimeout(function(){t.style.transform='translateY(18px)';t.style.opacity='0';},2800);
}

document.addEventListener('keydown',function(e){if(e.key==='Escape'){closeTl();closeModal();}});

loadData();
D.forEach(function(d){ensureCriacao(d);});
saveData();
render();
</script>
</body>
</html>
