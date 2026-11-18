# arch-archive-simulato[index.html](https://github.com/user-attachments/files/35052420/index.html)
вот код <!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Windows 7</title>
<style>
*{box-sizing:border-box;cursor:default}
html,body{margin:0;height:100%;overflow:hidden;background:#000;color:#000;font:12px "Segoe UI",Tahoma,Arial,sans-serif;user-select:none;-webkit-user-select:none}
input,textarea{font:inherit;user-select:text;-webkit-user-select:text}
input[type=text],textarea{cursor:text}
button{font:inherit}
:root{--h:210;--s:60;
 --fa:linear-gradient(180deg,hsla(var(--h),calc(var(--s)*1%),90%,.82),hsla(var(--h),calc(var(--s)*1%),68%,.8) 36px,hsla(var(--h),calc(var(--s)*1%),74%,.8));
 --fi:linear-gradient(180deg,rgba(246,248,251,.86),rgba(214,222,234,.84) 36px,rgba(226,232,241,.84));
 --tb:linear-gradient(180deg,hsla(var(--h),calc(var(--s)*1%),72%,.62),hsla(var(--h),calc(var(--s)*1%),38%,.78) 48%,hsla(var(--h),calc(var(--s)*1%),20%,.88) 52%,hsla(var(--h),calc(var(--s)*1%),28%,.9));
 --sm:linear-gradient(180deg,hsla(var(--h),calc(var(--s)*1%),62%,.8),hsla(var(--h),calc(var(--s)*1%),30%,.88));
 --accent:hsl(var(--h),calc(var(--s)*1%),45%)}
body.noglass{--fa:hsl(var(--h),calc(var(--s)*.6%),78%);--fi:#d6dde8;--tb:hsl(var(--h),calc(var(--s)*.8%),22%);--sm:hsl(var(--h),calc(var(--s)*.8%),30%)}
body.noglass *{backdrop-filter:none!important}
.ic{display:block;flex:none;pointer-events:none}
#wall{position:fixed;inset:0;background-size:cover;background-position:center;background-repeat:no-repeat;background-color:#d9cdbb;transition:background-image .3s}
#desktop{position:absolute;left:0;top:0;right:0;bottom:40px;overflow:hidden}
#icons{position:absolute;inset:0;z-index:1}
#gadget{position:absolute;right:18px;top:14px;z-index:2;width:140px;height:140px;filter:drop-shadow(0 3px 6px rgba(0,0,0,.35))}
#band{position:absolute;border:1px solid #3399ff;background:rgba(51,153,255,.25);display:none;z-index:3}
.di{position:absolute;width:86px;height:92px;padding:4px 2px;display:flex;flex-direction:column;align-items:center;border:1px solid transparent;border-radius:3px;touch-action:none}
.di:hover{background:rgba(255,255,255,.18);border-color:rgba(255,255,255,.35)}
.di.sel{background:rgba(120,170,235,.4);border-color:rgba(130,180,245,.85);box-shadow:inset 0 0 0 1px rgba(255,255,255,.35)}
.di .dp{height:48px;display:flex;align-items:center}
.di .dl{color:#fff;text-align:center;text-shadow:0 0 3px #000,0 1px 2px #000,0 0 5px #000;line-height:1.15;margin-top:2px;overflow:hidden;max-height:3.5em;word-break:break-word}
.di.sel .dl{max-height:none}
.di.moving{opacity:.7;z-index:50}
/* windows */
.win{position:absolute;display:flex;flex-direction:column;padding:0 7px 7px;border-radius:8px 8px 0 0;border:1px solid rgba(0,0,0,.62);background:var(--fa);backdrop-filter:blur(10px) saturate(1.5);box-shadow:inset 0 0 0 1px rgba(255,255,255,.6),0 8px 28px rgba(0,0,0,.5);animation:wopen .16s ease-out;transition:opacity .15s,transform .15s}
.win:not(.active){background:var(--fi);box-shadow:inset 0 0 0 1px rgba(255,255,255,.55),0 4px 14px rgba(0,0,0,.32)}
.win.min{opacity:0;transform:translateY(80px) scale(.6);pointer-events:none;visibility:hidden;transition:opacity .18s,transform .18s,visibility 0s .18s}
.win.closing{opacity:0;transform:scale(.93);pointer-events:none}
.win.max{left:0!important;top:0!important;width:100%!important;height:100%!important;border-radius:0;padding:0 5px 5px}
@keyframes wopen{from{opacity:0;transform:scale(.92)}to{opacity:1;transform:none}}
.tb{height:30px;flex:none;display:flex;align-items:center;gap:6px;padding-left:2px;touch-action:none}
.tb .ti{display:flex}
.tb .tt{flex:1;overflow:hidden;white-space:nowrap;text-overflow:ellipsis;text-shadow:0 0 9px #fff,0 0 7px #fff,0 0 4px #fff,0 0 2px #fff;font-size:12px}
.win:not(.active) .tt{color:#444;text-shadow:0 0 6px #fff,0 0 3px #fff}
.caps{display:flex;align-self:flex-start;margin-top:-1px;margin-right:-6px}
.win.max .caps{margin-right:-4px}
.cap{width:29px;height:19px;display:flex;align-items:center;justify-content:center;border:1px solid rgba(0,0,0,.6);border-top:0;background:linear-gradient(180deg,rgba(255,255,255,.7),rgba(190,210,235,.55) 48%,rgba(120,150,190,.6) 52%,rgba(190,215,240,.7));box-shadow:inset 0 0 0 1px rgba(255,255,255,.5)}
.cap+.cap{margin-left:-1px}
.cap:first-child{border-radius:0 0 0 5px}
.cap:hover{background:linear-gradient(180deg,rgba(255,255,255,.9),rgba(160,215,255,.8) 48%,rgba(60,160,235,.85) 52%,rgba(160,230,255,.9))}
.cap.close{width:47px;border-radius:0 0 5px 0;background:linear-gradient(180deg,#e9b1a6,#d2705c 48%,#b3301a 52%,#d97a5f)}
.cap.close:hover{background:linear-gradient(180deg,#f7c2b8,#ee7d66 48%,#d4351b 52%,#f5906f)}
.cap:only-child{border-radius:0 0 5px 5px}
.win:not(.active) .cap{opacity:.65}
.gmin{width:9px;height:4px;background:#fff;border:1px solid #333;margin-top:6px;box-shadow:0 0 0 1px rgba(255,255,255,.3)}
.gmax{width:11px;height:9px;border:2px solid #fff;border-top-width:3px;box-shadow:0 0 0 1px rgba(0,0,0,.65),inset 0 0 0 1px rgba(0,0,0,.65)}
.grest{width:8px;height:7px;border:2px solid #fff;border-top-width:3px;position:relative;box-shadow:0 0 0 1px rgba(0,0,0,.65),inset 0 0 0 1px rgba(0,0,0,.65);margin:3px 0 0 -3px}
.grest::before{content:"";position:absolute;left:3px;top:-6px;width:6px;height:5px;border:1px solid #fff;border-left:0;border-bottom:0;box-shadow:1px -1px 0 rgba(0,0,0,.6)}
.wbody{flex:1;min-height:0;background:#f0f0f0;border:1px solid rgba(0,0,0,.55);display:flex;flex-direction:column;position:relative;overflow:hidden}
.rz{position:absolute;z-index:6}
.rz-n{top:-3px;left:8px;right:8px;height:6px;cursor:ns-resize}.rz-s{bottom:-3px;left:8px;right:8px;height:6px;cursor:ns-resize}
.rz-e{right:-3px;top:8px;bottom:8px;width:6px;cursor:ew-resize}.rz-w{left:-3px;top:8px;bottom:8px;width:6px;cursor:ew-resize}
.rz-ne{right:-3px;top:-3px;width:10px;height:10px;cursor:nesw-resize}.rz-sw{left:-3px;bottom:-3px;width:10px;height:10px;cursor:nesw-resize}
.rz-nw{left:-3px;top:-3px;width:10px;height:10px;cursor:nwse-resize}.rz-se{right:-3px;bottom:-3px;width:10px;height:10px;cursor:nwse-resize}
.win.max .rz{display:none}
.shield{position:absolute;inset:0;z-index:5}
body.dragging *{pointer-events:none!important}
body.dragging{cursor:default}
#snapprev{position:fixed;display:none;z-index:8000;background:rgba(120,180,255,.25);border:2px solid rgba(255,255,255,.7);border-radius:6px;box-shadow:inset 0 0 25px rgba(255,255,255,.4)}
/* buttons */
.btn{min-width:75px;padding:3px 12px;border:1px solid #707070;border-radius:3px;color:#000;background:linear-gradient(#f2f2f2 45%,#ebebeb 46%,#cfcfcf);box-shadow:inset 0 0 0 1px rgba(255,255,255,.8)}
.btn:hover:not(:disabled){border-color:#3c7fb1;background:linear-gradient(#eaf6fd 45%,#d9f0fc 46%,#bee6fd)}
.btn:active:not(:disabled){background:linear-gradient(#c4e5f6 45%,#98d1ef 46%,#68b3db);border-color:#2c628b}
.btn.def,.btn:focus{border-color:#3c7fb1;box-shadow:inset 0 0 0 1px #6fd3f5;outline:none}
.btn:disabled{color:#888;border-color:#adb2b5;background:#f4f4f4}
.dlg{display:flex;flex-direction:column}
.dlg-t{display:flex;gap:14px;padding:20px 18px 18px;background:#fff;align-items:flex-start;min-height:70px}
.dlg-m{padding-top:6px;line-height:1.4;max-width:300px;user-select:text}
.dlg-b{display:flex;justify-content:flex-end;gap:8px;padding:10px 12px;background:#f0f0f0;border-top:1px solid #dfdfdf}
.dlg input[type=text]{width:100%;margin-top:6px;padding:3px;border:1px solid #7a8aa0}
/* menus */
.menubar{display:flex;flex:none;padding:1px 2px;background:linear-gradient(#fff,#eef1f7);border-bottom:1px solid #d5dbe6}
.mb-item{padding:2px 8px;border:1px solid transparent;border-radius:3px}
.mb-item:hover,.mb-item.on{border-color:#a6c3e4;background:linear-gradient(#fcfdfe,#e0ebf8)}
.ctx{position:fixed;z-index:30000;min-width:170px;padding:2px;background:linear-gradient(90deg,#f1f1f1 27px,#e2e3e3 27px,#e2e3e3 28px,#fff 28px);border:1px solid #979797;box-shadow:2px 3px 5px rgba(0,0,0,.35);animation:fade .1s}
@keyframes fade{from{opacity:0}to{opacity:1}}
.ctx-i{display:flex;align-items:center;padding:3px 4px;border:1px solid transparent;border-radius:3px;white-space:nowrap}
.ctx-i .ck{width:24px;display:flex;justify-content:center;color:#235;flex:none}
.ctx-i .cl{flex:1;padding:0 8px 0 6px}
.ctx-i .cs{color:#666;padding-left:18px;min-width:12px;text-align:right}
.ctx-i:hover:not(.dis){border-color:#a8d8eb;background:linear-gradient(#f2f9fd,#d6ecf9)}
.ctx-i.dis{color:#9a9a9a}.ctx-i.def .cl{font-weight:700}
.ctx-sep{height:1px;margin:3px 2px 3px 30px;background:#e0e0e0;border-bottom:1px solid #fff}
/* taskbar */
#taskbar{position:fixed;left:0;right:0;bottom:0;height:40px;z-index:9000;background:var(--tb);backdrop-filter:blur(12px) saturate(1.5);border-top:1px solid rgba(255,255,255,.55);box-shadow:inset 0 1px 0 rgba(255,255,255,.25),0 -1px 0 rgba(0,0,0,.4);display:flex;align-items:stretch}
#orb{position:absolute;left:4px;top:-9px;width:52px;height:52px;border-radius:50%;z-index:9200;background:radial-gradient(circle at 50% 18%,rgba(255,255,255,.75) 0,rgba(255,255,255,0) 40%),radial-gradient(circle at 50% 115%,#8fe0ff 0,#2b84dc 45%,#0c3f8c 80%);border:1px solid rgba(255,255,255,.7);box-shadow:0 0 0 1px rgba(0,20,60,.8),0 2px 6px rgba(0,0,0,.6),inset 0 -6px 12px rgba(0,180,255,.5);display:flex;align-items:center;justify-content:center}
#orb svg{width:30px;height:30px;filter:drop-shadow(0 1px 2px rgba(0,0,0,.6))}
#orb:hover,#orb.on{filter:brightness(1.25) saturate(1.2);box-shadow:0 0 0 1px rgba(0,20,60,.8),0 0 14px #6cf,inset 0 -6px 12px rgba(0,200,255,.7)}
#tasks{flex:1;margin-left:64px;display:flex;align-items:center;padding:0 4px}
.tbtn{position:relative;width:54px;height:36px;margin:0 1px;display:flex;align-items:center;justify-content:center;border:1px solid transparent;border-radius:4px}
.tbtn:hover{border-color:rgba(255,255,255,.55);background:linear-gradient(rgba(255,255,255,.35),rgba(255,255,255,.08) 50%,rgba(255,255,255,.2) 52%,rgba(255,255,255,.3));box-shadow:inset 0 0 6px rgba(255,255,255,.4)}
.tbtn.run{border-color:rgba(255,255,255,.4);background:linear-gradient(rgba(255,255,255,.28),rgba(255,255,255,.05) 50%,rgba(255,255,255,.12) 52%,rgba(255,255,255,.22))}
.tbtn.multi{box-shadow:3px 0 0 -1px rgba(255,255,255,.55),5px 0 0 -2px rgba(255,255,255,.35)}
.tbtn.act{border-color:rgba(255,255,255,.7);background:linear-gradient(rgba(255,255,255,.55),rgba(150,200,255,.25) 50%,rgba(255,255,255,.25) 52%,rgba(255,255,255,.45));box-shadow:inset 0 0 8px rgba(255,255,255,.6)}
#tray{display:flex;align-items:center;gap:2px;padding-right:4px;color:#fff;text-shadow:0 0 3px #000}
.tr{padding:4px 5px;border:1px solid transparent;border-radius:3px;display:flex;align-items:center}
.tr:hover,#clock:hover{background:rgba(255,255,255,.2);border-color:rgba(255,255,255,.4)}
#lang{font-size:11px}
#clock{text-align:center;line-height:1.25;padding:3px 8px;border:1px solid transparent;border-radius:3px}
#showdesk{width:15px;border-left:1px solid rgba(255,255,255,.5);background:linear-gradient(90deg,rgba(255,255,255,.15),rgba(255,255,255,.05))}
#showdesk:hover{background:rgba(255,255,255,.4)}
#thumbs{position:fixed;bottom:42px;z-index:9050;display:none;gap:6px;padding:6px;border-radius:6px;background:var(--sm);backdrop-filter:blur(10px);border:1px solid rgba(255,255,255,.6);box-shadow:0 4px 14px rgba(0,0,0,.5)}
.th{width:190px;padding:4px;border:1px solid transparent;border-radius:4px;color:#fff;text-shadow:0 0 3px #000}
.th:hover{background:rgba(255,255,255,.3);border-color:rgba(255,255,255,.6)}
.th-h{display:flex;align-items:center;gap:5px;height:20px}
.th-h span{flex:1;overflow:hidden;white-space:nowrap;text-overflow:ellipsis}
.th-x{width:18px;height:16px;text-align:center;border-radius:3px;line-height:16px}
.th-x:hover{background:#d9442a}
.th-p{height:96px;margin-top:3px;background:linear-gradient(135deg,rgba(255,255,255,.85),rgba(190,215,245,.7));border:1px solid rgba(0,0,0,.4);display:flex;align-items:center;justify-content:center}
/* start */
#start{position:fixed;left:2px;bottom:36px;width:410px;height:500px;z-index:9100;border-radius:8px;background:var(--sm);backdrop-filter:blur(14px) saturate(1.6);border:1px solid rgba(255,255,255,.6);box-shadow:inset 0 0 0 1px rgba(0,0,0,.45),0 0 0 1px rgba(0,0,0,.5),4px 4px 16px rgba(0,0,0,.55);display:none}
#start.open{display:block;animation:fade .12s}
.sm-l{position:absolute;left:8px;top:8px;bottom:8px;width:242px;background:#fff;border:1px solid #5e7596;border-radius:5px;display:flex;flex-direction:column;padding:3px}
.sm-list{flex:1;overflow:auto;min-height:0}
.sm-i{display:flex;align-items:center;gap:8px;padding:3px 6px;border:1px solid transparent;border-radius:3px;height:40px}
.sm-i:hover{border-color:#a8d8eb;background:linear-gradient(#f4fafe,#d3ebf9)}
.sm-i .nm{flex:1;overflow:hidden;white-space:nowrap;text-overflow:ellipsis;font-size:12px}
.sm-sep{height:1px;background:#d9dfe8;margin:4px 6px}
.sm-all{padding:6px 10px;margin-top:2px;border-top:1px solid #d9dfe8;font-weight:600}
.sm-all:hover{background:linear-gradient(#f4fafe,#d3ebf9)}
.sm-search{margin-top:4px;position:relative}
.sm-search input{width:100%;height:26px;border:1px solid #8ea4c2;border-radius:3px;padding:0 24px 0 8px;color:#333}
.sm-r{position:absolute;left:256px;right:8px;top:8px;bottom:8px;display:flex;flex-direction:column;color:#fff;text-shadow:0 0 3px rgba(0,0,0,.7)}
.sm-user{height:70px;display:flex;align-items:center;gap:10px;padding:0 4px;font-size:15px}
.sm-av{width:56px;height:56px;border:2px solid rgba(255,255,255,.85);border-radius:6px;background:linear-gradient(#bfe3ff,#4a8fd8);display:flex;align-items:flex-end;justify-content:center;overflow:hidden;box-shadow:0 0 6px rgba(0,0,0,.5)}
.sm-r .ri{padding:5px 8px;border:1px solid transparent;border-radius:3px;display:flex;align-items:center;gap:8px}
.sm-r .ri:hover{border-color:rgba(255,255,255,.55);background:linear-gradient(rgba(255,255,255,.4),rgba(255,255,255,.12))}
.sm-sd{display:flex;margin-top:auto;padding-bottom:2px}
.sd-main{padding:5px 14px;color:#fff;border:1px solid rgba(255,255,255,.5);border-radius:3px 0 0 3px;background:linear-gradient(rgba(255,255,255,.3),rgba(0,0,0,.15) 50%,rgba(0,0,0,.28) 52%,rgba(60,90,140,.4));box-shadow:inset 0 0 0 1px rgba(255,255,255,.15)}
.sd-arr{width:22px;text-align:center;line-height:24px;border:1px solid rgba(255,255,255,.5);border-left:0;border-radius:0 3px 3px 0;background:linear-gradient(rgba(255,255,255,.3),rgba(0,0,0,.15) 50%,rgba(0,0,0,.28) 52%,rgba(60,90,140,.4))}
.sd-main:hover,.sd-arr:hover{background:linear-gradient(rgba(255,255,255,.55),rgba(120,180,255,.35) 50%,rgba(60,120,220,.5) 52%,rgba(120,190,255,.6))}
/* popups */
.pop{position:fixed;bottom:42px;z-index:9060;display:none;padding:10px;border-radius:6px;background:linear-gradient(#fdfeff,#e7eef8);border:1px solid #6d7f99;box-shadow:0 4px 16px rgba(0,0,0,.5)}
.pop.open{display:block}
#clockpop{right:6px;width:380px}
.cal{display:grid;grid-template-columns:repeat(7,1fr);gap:1px;text-align:center}
.cal div{padding:5px 0;border:1px solid transparent}
.cal .dh{color:#335;font-weight:600}.cal .dim{color:#aaa}
.cal .td{background:linear-gradient(#bde0f9,#7fc0ee);border-color:#4a8cc4;color:#000;font-weight:700}
.cal div:not(.dh):hover{border-color:#a8d8eb;background:#e3f2fc}
#volpop{right:70px;width:70px;height:170px;text-align:center}
#volpop input{writing-mode:vertical-lr;direction:rtl;height:110px;width:24px}
#netpop{right:100px;width:260px}
#balloon{position:fixed;right:10px;bottom:46px;width:280px;z-index:9070;padding:10px 12px;background:#ffffe1;border:1px solid #555;border-radius:6px;box-shadow:2px 3px 8px rgba(0,0,0,.4);display:none}
/* overlays */
#boot,#logon,#power{position:fixed;inset:0;z-index:20000;display:none;color:#fff}
#boot,#power{background:#000;align-items:center;justify-content:center;flex-direction:column}
#logon{background:radial-gradient(ellipse at 50% 120%,#7fd0ff 0,#2a79c9 35%,#0b3a80 70%,#04204a);align-items:center;justify-content:center;flex-direction:column;gap:18px;font-size:24px;font-weight:300}
#boot.on,#power.on,#logon.on{display:flex}
.bflag{width:110px;height:110px;animation:glow 1.6s infinite alternate}
@keyframes glow{from{filter:drop-shadow(0 0 4px #fff) brightness(.8)}to{filter:drop-shadow(0 0 18px #6cf) brightness(1.2)}}
.btxt{margin-top:26px;font-size:20px;letter-spacing:1px}
.bbar{margin-top:20px;width:200px;height:8px;border:1px solid #666;border-radius:4px;overflow:hidden;position:relative}
.bbar::after{content:"";position:absolute;top:0;bottom:0;width:60px;background:linear-gradient(90deg,transparent,#4af,transparent);animation:bslide 1.3s infinite linear}
@keyframes bslide{from{left:-60px}to{left:200px}}
.spin{width:36px;height:36px;border-radius:50%;border:4px solid rgba(255,255,255,.3);border-top-color:#fff;animation:rot 1s infinite linear}
@keyframes rot{to{transform:rotate(360deg)}}
.lg-tile{display:flex;flex-direction:column;align-items:center;gap:10px;padding:14px 26px;border:1px solid transparent;border-radius:6px}
.lg-tile:hover{background:rgba(255,255,255,.15);border-color:rgba(255,255,255,.5)}
.lg-av{width:120px;height:120px;border:3px solid rgba(255,255,255,.85);border-radius:10px;background:linear-gradient(#bfe3ff,#4a8fd8);display:flex;align-items:flex-end;justify-content:center;overflow:hidden;box-shadow:0 0 14px rgba(0,0,0,.5)}
.pbtn{width:90px;height:90px;border-radius:50%;border:2px solid #666;background:radial-gradient(circle at 50% 30%,#444,#111);color:#bbb;font-size:42px;display:flex;align-items:center;justify-content:center}
.pbtn:hover{border-color:#6cf;color:#fff;box-shadow:0 0 18px #3af}
/* explorer */
.ex-nav{display:flex;align-items:center;gap:8px;padding:6px 8px;background:linear-gradient(#f7fafe,#e4ebf5);border-bottom:1px solid #c5d0e0;flex:none}
.ex-btns{display:flex;gap:2px}
.ex-b{width:28px;height:28px;border-radius:50%;border:1px solid #6d8bb5;background:radial-gradient(circle at 50% 25%,#fff,#bcd4f0 75%);color:#2b5da8;font-size:11px;padding:0}
.ex-b:disabled{opacity:.4}.ex-b:hover:not(:disabled){background:radial-gradient(circle at 50% 25%,#fff,#8fc4f5 75%)}
.ex-addr{flex:1;min-width:0;height:24px;background:#fff;border:1px solid #9fb0c8;display:flex;align-items:center;padding:0 4px;overflow:hidden;white-space:nowrap}
.seg{padding:2px 4px;border:1px solid transparent;border-radius:2px}.seg:hover{border-color:#a8d8eb;background:#e3f2fc}
.ex-search input{width:160px;height:24px;border:1px solid #9fb0c8;padding:0 6px}
.ex-cmd{display:flex;gap:2px;padding:3px 8px;background:linear-gradient(#fbfcfe,#e8edf6);border-bottom:1px solid #d0d8e6;flex:none}
.cb{padding:3px 10px;border:1px solid transparent;border-radius:3px;background:none;color:#1a2f55}
.cb:hover:not(:disabled){border-color:#a6c3e4;background:linear-gradient(#fff,#dde9f8)}.cb:disabled{color:#999}
.ex-main{flex:1;display:flex;min-height:0;background:#fff}
.ex-side{width:178px;flex:none;overflow:auto;padding:4px;background:linear-gradient(90deg,#f3f6fb,#e8eef7);border-right:1px solid #d0d8e6}
.sd-h{color:#1e3f7a;font-weight:600;margin:10px 4px 3px}
.sd-i{padding:2px 6px;display:flex;gap:6px;align-items:center;border:1px solid transparent;border-radius:3px;white-space:nowrap}
.sd-i:hover{border-color:#bcd5ee;background:#eaf3fc}.sd-i.cur{border-color:#a7c4e6;background:linear-gradient(#e4f0fc,#cfe2f8)}
.ex-list{flex:1;overflow:auto;padding:8px;display:flex;flex-wrap:wrap;align-content:flex-start;gap:4px;outline:none}
.exi{width:98px;padding:5px 3px;display:flex;flex-direction:column;align-items:center;text-align:center;border:1px solid transparent;border-radius:3px;word-break:break-word;line-height:1.2}
.exi:hover{background:linear-gradient(#f7fbfe,#e5f2fc);border-color:#cfe4f5}
.exi.sel{background:linear-gradient(#e8f4fe,#cde6fa);border-color:#7da2ce}
.exi.drive{width:260px;flex-direction:row;text-align:left;gap:8px;padding:6px}
.exi .thumb{width:64px;height:48px;background-size:cover;background-position:center;background-color:#e8eef7;border:1px solid #aab;box-shadow:0 1px 3px rgba(0,0,0,.3)}
.dbar{height:12px;border:1px solid #888;background:#e6e6e6;margin:3px 0;width:150px}.dbar i{display:block;height:100%;background:linear-gradient(#5ebcf0,#1a86d0)}
.det table{width:100%;border-collapse:collapse}.det th{text-align:left;font-weight:400;color:#555;padding:3px 8px;border-right:1px solid #e3e3e3;border-bottom:1px solid #e3e3e3}
.det td{padding:2px 8px;white-space:nowrap}.det tr.sel td{background:#cde6fa}.det tr:hover:not(.sel) td{background:#eaf4fc}
.det .nm{display:flex;gap:6px;align-items:center}
.ex-stat{flex:none;padding:5px 10px;background:linear-gradient(#f5f7fb,#e5eaf3);border-top:1px solid #cfd8e6;color:#333;min-height:24px}
/* notepad */
textarea.np{flex:1;resize:none;border:0;outline:0;padding:2px 4px;font:13px Consolas,"Courier New",monospace;background:#fff;white-space:pre-wrap}
/* calc */
.calc{flex:1;display:flex;flex-direction:column;padding:6px;background:#eef2f9}
.cd{background:#fff;border:1px solid #7c8ca5;padding:4px 8px;text-align:right;margin-bottom:6px;height:62px;position:relative}
.cd .h{font-size:11px;color:#777;height:16px;overflow:hidden}.cd .m{font-size:28px;position:absolute;right:8px;bottom:2px;white-space:nowrap}.cd .mm{position:absolute;left:6px;bottom:4px;font-size:11px;color:#555}
.ck-g{flex:1;display:grid;grid-template-columns:repeat(5,1fr);gap:3px}
.cbt{border:1px solid #8b99ad;border-radius:3px;background:linear-gradient(#fff 45%,#e8edf4 46%,#d3dbe7);padding:0;font-size:14px}
.cbt.n{background:linear-gradient(#fff 45%,#f2f4f8 46%,#e3e8f0);font-weight:700}
.cbt:hover{border-color:#3c7fb1;background:linear-gradient(#eaf6fd 45%,#d9f0fc 46%,#bee6fd)}
.cbt:active{background:linear-gradient(#c4e5f6 45%,#98d1ef 46%,#68b3db)}
.cbt.eq{grid-row:span 2;background:linear-gradient(#bde6a5 45%,#8ed16b 46%,#63b843)}
/* paint */
.pt-top{display:flex;gap:10px;padding:6px 8px;background:linear-gradient(#f8fafd,#dfe7f3);border-bottom:1px solid #b9c6da;flex:none;align-items:center;flex-wrap:wrap}
.pt-tools{display:grid;grid-template-columns:repeat(4,28px);gap:2px}
.pt-t{width:28px;height:26px;padding:0;border:1px solid transparent;border-radius:3px;background:none;font-size:15px}
.pt-t:hover{border-color:#a6c3e4;background:#eaf3fc}.pt-t.on{border-color:#6f9bd2;background:linear-gradient(#cfe4fa,#a9cdf2)}
.pt-pal{display:grid;grid-template-columns:repeat(14,18px);gap:2px}
.pt-c{width:18px;height:18px;border:1px solid #666}
.pt-cur{width:34px;height:34px;position:relative;margin-right:4px}
.pt-cur i{position:absolute;width:22px;height:22px;border:1px solid #333}.pt-cur .p2{right:0;bottom:0}.pt-cur .p1{left:0;top:0;z-index:2}
.pt-area{flex:1;overflow:auto;background:#a8b9d2;padding:6px}
canvas.pc{background:#fff;display:block;box-shadow:2px 2px 4px rgba(0,0,0,.4);touch-action:none;cursor:crosshair}
.pt-st{flex:none;padding:3px 8px;background:#e9edf4;border-top:1px solid #c3cde0;display:flex;gap:30px}
/* minesweeper */
.mine{align-self:flex-start;padding:6px;background:#c0c0c0;border:3px solid;border-color:#fff #7b7b7b #7b7b7b #fff}
.mn-h{display:flex;justify-content:space-between;align-items:center;padding:4px 6px;margin-bottom:6px;border:2px solid;border-color:#7b7b7b #fff #fff #7b7b7b}
.led{background:#000;color:#f00;font:bold 26px/30px "Courier New",monospace;padding:0 3px;border:1px solid;border-color:#7b7b7b #fff #fff #7b7b7b;letter-spacing:1px}
.face{width:34px;height:34px;font-size:20px;padding:0;background:#c0c0c0;border:3px solid;border-color:#fff #7b7b7b #7b7b7b #fff}.face:active{border:1px solid #7b7b7b}
.mn-g{display:grid;border:3px solid;border-color:#7b7b7b #fff #fff #7b7b7b}
.mc{width:24px;height:24px;display:flex;align-items:center;justify-content:center;font:bold 16px Tahoma,Arial;background:#c0c0c0;border:3px solid;border-color:#fff #7b7b7b #7b7b7b #fff;line-height:1}
.mc.o{border:1px solid #8a8a8a;border-width:1px 0 0 1px}.mc.hit{background:#f00}
/* cmd */
.cmd{flex:1;background:#0c0c0c;color:#c0c0c0;font:14px Consolas,"Lucida Console",monospace;padding:4px 6px;overflow:auto}
.cmd .co div{white-space:pre-wrap;word-break:break-all;min-height:1.2em;user-select:text}
.cmd .cl{display:flex}.cmd .cp{white-space:pre}
.cmd input{flex:1;background:transparent;border:0;outline:0;color:inherit;font:inherit;padding:0}
/* misc app */
.tabs{display:flex;padding:6px 6px 0;gap:0;flex:none}
.tab{padding:3px 14px;border:1px solid #8e9aae;border-bottom:0;border-radius:3px 3px 0 0;background:linear-gradient(#f4f6fa,#dde3ee);margin-right:-1px}
.tab.on{background:#fff;position:relative;top:1px;padding-bottom:5px}
.tp{flex:1;background:#fff;border:1px solid #8e9aae;margin:0 6px 6px;overflow:auto;min-height:0;display:flex;flex-direction:column}
.tbl{width:100%;border-collapse:collapse}.tbl th{text-align:left;font-weight:400;padding:3px 8px;border-bottom:1px solid #ddd;border-right:1px solid #e5e5e5;background:linear-gradient(#fff,#f1f3f7)}
.tbl td{padding:3px 8px}.tbl tr.sel td{background:#3399ff;color:#fff}
.wp-grid{display:grid;grid-template-columns:repeat(auto-fill,150px);gap:10px;padding:10px}
.wp{border:2px solid transparent;border-radius:4px;padding:3px;text-align:center}
.wp:hover{background:#e8f3fc;border-color:#bcdcf4}.wp.on{background:#cde6fa;border-color:#4a8cc4}
.wp .t{height:84px;background-size:cover;background-position:center;background-color:#cdd;border:1px solid #889}
.sw{display:flex;gap:8px;padding:0 10px 10px;flex-wrap:wrap}
.sw i{width:34px;height:34px;border:2px solid #fff;border-radius:4px;box-shadow:0 0 0 1px #666}.sw i.on{box-shadow:0 0 0 2px #1a5fb4,0 0 6px #4af}
.cp-grid{display:grid;grid-template-columns:repeat(auto-fill,200px);gap:4px;padding:14px;background:#fff;flex:1;align-content:start;overflow:auto}
.cp-i{display:flex;gap:8px;align-items:center;padding:8px;border:1px solid transparent;border-radius:3px}.cp-i:hover{background:linear-gradient(#f6fbff,#dcedfb);border-color:#bcd6ee}
.sysinfo{padding:18px 22px;background:#fff;flex:1;overflow:auto;line-height:1.7}.sysinfo h3{font-weight:400;color:#1e3f7a;font-size:16px;margin:10px 0 4px;border-bottom:1px solid #d6e0ee}
.sysinfo td:first-child{color:#666;padding-right:20px}
.ie-bar{display:flex;gap:6px;padding:5px 8px;background:linear-gradient(#f4f7fc,#dbe4f2);align-items:center;flex:none}
.ie-bar input{flex:1;height:24px;border:1px solid #8ea4c2;padding:0 6px;background:#fff}
.ie-fav{display:flex;gap:14px;padding:3px 10px;background:#eef2f9;border-bottom:1px solid #c9d4e6;flex:none;color:#1a3b73}
.ie-view{flex:1;overflow:auto;background:#fff;user-select:text}
.wmp{flex:1;background:linear-gradient(#233c63,#0b1a33);color:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:14px}
.wmp-v{display:flex;gap:4px;align-items:flex-end;height:70px}.wmp-v i{width:10px;background:linear-gradient(#7fe3ff,#2a7fd0);height:6px;transition:height .12s}
.wmp-p{width:64px;height:64px;border-radius:50%;border:2px solid #9cf;background:radial-gradient(circle at 50% 30%,#8cd,#27a 70%);font-size:26px;color:#fff;padding:0;box-shadow:0 0 12px #4af}

/* A.R.C.H. Stage 1 additions to original Windows 7 interface */
html,body{font-family:Tahoma,Arial,sans-serif}
#wall{background-image:radial-gradient(ellipse at 67% 37%,#243c52 0%,#101d2e 37%,#03060b 90%)}
#arch-brand{position:fixed;right:4vw;top:7vh;z-index:1;color:#b9c8d6;opacity:.48;font:58px Tahoma,sans-serif;letter-spacing:.16em;pointer-events:none;text-shadow:0 0 20px #94b4d5}
#arch-brand small{display:block;text-align:right;font-size:10px;letter-spacing:.2em}
#arch-pixel{position:fixed;left:58%;top:41%;height:2px;width:2px;background:red;z-index:3;box-shadow:0 0 3px red}
#arch-bsod,#arch-game,#arch-dark{position:fixed;inset:0;z-index:30000;color:#fff}
#arch-bsod{display:none;background:#0000aa;padding:5vh 8vw;white-space:pre-wrap;font:16px/1.45 Consolas,monospace;overflow:auto}
#arch-bsod.on,#arch-dark.on,#arch-game.on{display:block}
#arch-dark{display:none;background:#000}
#arch-game{display:none;background:#000;text-align:center;padding-top:36vh;font:26px Consolas,monospace}
#arch-game button{display:block;margin:40px auto;padding:9px 18px;background:#111;border:1px solid #777;color:#fff}
#arch-notice{display:none;position:fixed;right:15px;bottom:50px;z-index:16000;background:#f4f7fb;color:#243447;padding:14px;border:1px solid #6e92b5;width:340px;box-shadow:0 7px 25px #0009;line-height:1.5}
#arch-notice.on{display:block}#arch-notice button{margin:10px 5px 0 0}
.arch-hist{width:245px;max-width:45%;overflow:auto;border-right:1px solid #bac9d8;background:#edf3fa;flex:none}
.arch-hist h4{margin:12px 8px 5px;color:#476689}.arch-hist button{display:block;width:100%;text-align:left;border:0;border-bottom:1px solid #dbe3ed;background:none;color:#234a71;padding:8px;font:11px Tahoma}.arch-hist button:hover{background:#cde4fa}
.arch-result{padding:25px;line-height:1.65;color:#26333f;overflow:auto;flex:1;background:#fff}.arch-result h2{color:#245888}
/* Mail: Windows Live Mail / Outlook Express inspired */
.mail-shell{height:100%;display:flex;flex-direction:column;font:12px Tahoma,Arial,sans-serif;color:#25374c;background:#f3f6fa;min-height:0}
.mail-head{flex:none;display:flex;justify-content:space-between;align-items:center;padding:11px 16px;background:linear-gradient(#f8fcff,#dbe7f6 48%,#c7d9ed);border-bottom:1px solid #8ca6c2;color:#254976;min-height:58px}.mail-head>div:last-child{text-align:right;line-height:1.4}.mail-logo{font:bold 21px Tahoma;letter-spacing:-.5px;text-shadow:0 1px white}
.mail-toolbar{display:flex;align-items:center;gap:6px;flex:none;padding:5px 10px;border-bottom:1px solid #abbcd0;background:linear-gradient(#fff,#e4ebf4)}.mail-banner{font-size:11px;margin-left:auto;color:#794b54;font-style:italic}
.mail-columns{display:flex;flex:1;min-height:0}.mail-folders{width:155px;flex:none;border-right:1px solid #a9bacb;background:linear-gradient(90deg,#e9f0f8,#dae6f2);padding:9px 4px}.mail-folder{display:block;text-align:left;width:100%;border:1px solid transparent;background:transparent;color:#284766;padding:9px 8px;font:12px Tahoma}.mail-folder:hover,.mail-folder.chosen{background:linear-gradient(#d5e9fa,#b5d3ee);border-color:#8eb3d2}
.mail-list{width:265px;flex:none;background:#fff;border-right:1px solid #a9bacb;overflow:auto}.mail-row{display:block;width:100%;text-align:left;padding:10px 9px;border:0;border-bottom:1px solid #d5dfeb;background:linear-gradient(#fff,#f5f8fb);color:#263a53;font:12px Tahoma;cursor:pointer}.mail-row:hover{background:#ebf4fc}.mail-row.chosen{background:linear-gradient(#d7ebfb,#bdd9f2);box-shadow:inset 3px 0 #598cc3}.mail-subject{display:block;font-weight:bold;overflow:hidden;white-space:nowrap;text-overflow:ellipsis}.mail-from,.mail-date{display:block;color:#52697c;font-size:11px;margin-top:3px}.mail-date{float:right}
.mail-preview{flex:1;min-width:0;background:#fff;overflow:auto;user-select:text}.mail-empty{padding:35px;color:#8290a1}.mail-message-head{padding:14px 18px;border-bottom:1px solid #cdd7e6;background:linear-gradient(#fff,#f2f6fa);line-height:1.7}.mail-message-head h3{font-size:17px;margin:0 0 9px;color:#224b72}.mail-body{padding:22px 20px;white-space:pre-wrap;line-height:1.7;font-size:13px;min-height:150px}.mail-attachments{border-top:1px solid #cdd7e6;padding:12px 18px}.mail-attachments:empty{display:none}.mail-attachments .btn{margin-left:7px}.mail-photo{width:20px;height:20px;display:inline-block;vertical-align:middle;margin:0 5px;background:radial-gradient(circle at 50% 30%,#888 0 4px,transparent 5px),radial-gradient(ellipse at 50% 94%,#8a929e 0 8px,#c4cbd3 9px);filter:blur(2px);border:1px solid #aab5c0;cursor:help}.mail-status{flex:none;border-top:1px solid #aab8c8;padding:5px 9px;background:linear-gradient(#f8fafc,#dce5ee);font-size:11px;color:#536c80}.mail-count{float:right}.mail-spinner{display:inline-block;color:#3278b2;animation:mailspin 1.8s linear infinite}@keyframes mailspin{to{transform:rotate(360deg)}}.mail-freeze{padding:50px 20px;text-align:center;color:#53677b;font-size:16px}.mail-freeze small{display:block;margin:15px}.mail-freeze button{display:block;margin:25px auto}.mail-draft-line{line-height:1.6}.mail-caret{color:#1b2b38;animation:mailblink .8s step-end infinite}@keyframes mailblink{50%{opacity:0}}.mail-draft-input{border:0;outline:0;resize:none;width:90%;height:65px;cursor:not-allowed;background:transparent}.mail-compose{padding:14px;display:flex;flex-direction:column;gap:10px;flex:1;background:#eff3f8}.mail-compose label{display:flex;align-items:center;gap:8px}.mail-compose input{flex:1}.mail-compose input,.mail-compose textarea{border:1px solid #7a8aa0;box-shadow:inset 1px 1px 2px rgba(0,0,0,.15);padding:7px;font:12px Tahoma}.mail-compose textarea{flex:1;resize:none}.mail-compose button{align-self:flex-end}
/* Browser pages, deliberately period-specific 2010s styling */
.arch-result{padding:0!important;font:12px Tahoma,Arial,sans-serif;color:#27374d}.site-page{min-height:100%;display:flex;flex-direction:column;background:#f7f9fc;font:12px/1.5 Tahoma,Arial,sans-serif;color:#263749}.site-page *{box-sizing:border-box}.site-page a{color:#1a3b73;text-decoration:none}.site-page a:hover{text-decoration:underline}.site-header{display:flex;justify-content:space-between;align-items:center;background:linear-gradient(#fbfcff,#dfebf7 48%,#c9dced);border-bottom:1px solid #8da9c2;min-height:64px;padding:10px 22px}.site-header strong{font:bold 25px Tahoma;color:#214774;letter-spacing:-1px}.site-header strong span{color:#e38424}.site-header nav{white-space:nowrap;color:#8794a8}.site-header a{margin:0 5px}.site-crumbs{padding:9px 23px;background:#edf3f9;border-bottom:1px solid #cdd7e6;color:#5b718a}.site-pad{padding:18px 24px;flex:1}.site-pad h1{font-size:20px;color:#1e3d62;margin:0 0 8px;font-weight:normal}.site-meta{font-size:11px;color:#8290a0;margin-bottom:17px}.site-footer{background:linear-gradient(#f7f9fc,#e6edf6);border-top:1px solid #cdd7e6;color:#73869a;padding:12px 24px;margin-top:auto}.site-post{display:flex;margin:10px 0;border:1px solid #cdd7e6;background:white;box-shadow:0 2px 7px rgba(0,0,0,.06);min-height:128px}.site-post aside{width:135px;flex:none;background:linear-gradient(#f2f6fa,#e4edf7);border-right:1px solid #cdd7e6;text-align:center;padding:11px 8px}.site-avatar{width:42px;height:42px;background:linear-gradient(#93badc,#416f9b);border:1px solid #48759c;color:white;box-shadow:inset 0 1px #fff6;display:grid;place-items:center;font:bold 24px Tahoma;margin:0 auto 6px}.site-post:nth-of-type(even) .site-avatar{background:linear-gradient(#e7a671,#9f603b)}.site-post aside b{display:block;color:#214571}.site-post aside small{color:#7a8794}.site-post-text{padding:16px 18px;line-height:1.7;flex:1}.site-post blockquote{margin:0 0 14px;padding:10px;background:#f1f5fa;border-left:4px solid #5b8fc0;color:#596b7d}.site-reply{margin-top:20px;padding:13px;background:linear-gradient(#fbfdff,#e6edf6);border:1px solid #cdd7e6}.site-reply b{display:block;margin-bottom:8px}.site-reply textarea{width:100%;height:85px;display:block;margin-bottom:9px}.site-feedback{color:#5a7385;margin-left:10px}.site-btn,.site-page button,.mail-shell .btn,.mail-compose .btn{font:12px Tahoma;color:#213e62;border:1px solid #7a8aa0;border-radius:3px;background:linear-gradient(#f7f9fc 45%,#e2e8f2 46%,#c9d3e2);padding:6px 13px;box-shadow:inset 0 1px #fff;cursor:pointer}.site-btn:hover,.site-page button:hover{border-color:#4379af;background:linear-gradient(#fff,#d9eafd)}.site-page input,.site-page textarea{font:12px Tahoma;background:#fff;border:1px solid #7a8aa0;box-shadow:inset 1px 1px 2px rgba(0,0,0,.15);padding:7px}.site-search-head{padding:13px 25px;background:linear-gradient(#fff,#e7eef6);border-bottom:1px solid #cdd7e6;display:flex;align-items:center;flex-wrap:wrap;gap:8px}.site-search-head strong{font:bold 29px Tahoma;letter-spacing:-2px;margin-right:15px}.site-search-head strong span:nth-child(1){color:#3072b2}.site-search-head strong span:nth-child(2){color:#d64532}.site-search-head strong span:nth-child(3){color:#f1a900}.site-search-head strong span:nth-child(4){color:#359352}.site-search-head input{min-width:180px;max-width:430px;flex:1;height:31px}.site-search-head nav{width:100%;margin-left:96px;color:#6c7d92;font-size:11px}.site-search .site-pad{background:#fff;padding-left:120px}.site-hit{margin:0 0 18px;max-width:650px;color:#5c6670}.site-hit>a{display:block;font-size:16px;color:#1a3b73}.site-url{color:#27834c;margin:2px 0;font-size:11px}.site-pages{border-top:1px solid #e1e7ee;padding-top:15px;margin:30px 0}.site-pages a{margin:0 5px}.site-article .site-pad{background:#f8fafc}.site-paper{background:#fff;padding:22px;border:1px solid #cdd7e6;box-shadow:0 2px 7px rgba(0,0,0,.06);max-width:760px}.site-paper p{font:13px/1.9 Tahoma;color:#313c49;margin:20px 0}.site-redacted{background:#f3f4f5;color:#666;text-align:center;padding:18px;letter-spacing:1px}.site-comment{background:#fff;border:1px solid #cdd7e6;padding:9px 13px;margin:7px 0;max-width:760px}.site-comment b{color:#1a3b73}.site-comment small{color:#7e8793;margin-left:12px}.site-comment p{margin:6px 0}.site-unavailable{background:white;text-align:center}.site-unavailable-box{margin:auto;padding:55px 20px;max-width:550px}.site-unavailable h1{font-size:23px;color:#345778;font-weight:normal}.site-unavailable p{font-size:13px;color:#596b80}.site-strange{color:#a03538!important}.site-disconnect{width:78px;height:70px;margin:auto;border:3px solid #adbac7;background:linear-gradient(#fff,#e0e7f0);position:relative;box-shadow:2px 3px 8px rgba(0,0,0,.08)}.site-disconnect:before{content:'×';font:bold 39px Tahoma;color:#a53a37;position:absolute;inset:0}.site-unavailable .site-btn{margin-top:14px}.site-action{margin:18px 24px;padding:14px;border:1px solid #cdd7e6;background:#f3f7fc}.site-action input{margin-right:8px}.site-tab{border:1px solid #99b1cb;padding:4px 10px;background:linear-gradient(#fff,#dfebf7)}.arch-result::-webkit-scrollbar,.arch-hist::-webkit-scrollbar,.mail-list::-webkit-scrollbar,.mail-preview::-webkit-scrollbar{width:16px;height:16px}.arch-result::-webkit-scrollbar-thumb,.arch-hist::-webkit-scrollbar-thumb,.mail-list::-webkit-scrollbar-thumb,.mail-preview::-webkit-scrollbar-thumb{background:linear-gradient(90deg,#c7d1dc,#8b9aab,#c4cfda);border:1px solid #8898aa}.arch-result::-webkit-scrollbar-track,.arch-hist::-webkit-scrollbar-track,.mail-list::-webkit-scrollbar-track,.mail-preview::-webkit-scrollbar-track{background:#e6ebf1;border:1px solid #b6c3d1}@media(max-width:760px){.mail-folders{width:120px}.mail-list{width:190px}.site-search .site-pad{padding-left:22px}.site-post aside{width:98px}}
/* Archive recording viewer: original window manager shell + self-contained player. */
.arch-record-window{padding:0!important;border:1px solid #333!important;border-radius:0!important;background:#000!important;box-shadow:0 8px 30px rgba(0,0,0,.8)!important;min-width:420px!important;min-height:300px!important}
.arch-record-window .wbody{border:0;overflow:hidden;background:#000}
.rec-win{position:relative;width:100%;height:100%;background:#000;display:flex;flex-direction:column;font:13px Consolas,'Courier New',monospace;color:#ddd;z-index:100}
.rec-titlebar{height:26px;flex:none;display:flex;align-items:center;padding:0 8px;background:#1a1a1a;color:#aaa;font:12px Tahoma;border-bottom:1px solid #333;cursor:move;user-select:none}
.rec-titlebar .rec-close{margin-left:auto;width:20px;height:18px;text-align:center;line-height:16px;cursor:pointer;border:1px solid #444;border-radius:2px;background:#272727;color:#bbb;padding:0}
.rec-titlebar .rec-close:hover{background:#c9301c;color:#fff}
.rec-canvas{flex:1;width:100%;min-height:0;background:#000;display:block;object-fit:fill}
.rec-text{position:absolute;left:16px;bottom:70px;right:16px;color:#ddd;font:14px Consolas,'Courier New',monospace;line-height:1.5;text-shadow:0 0 4px #000;pointer-events:none;white-space:pre-wrap}
.rec-text .cursor{display:inline-block;width:8px;height:14px;background:#ddd;animation:rec-blink 1s steps(2) infinite;vertical-align:middle;margin-left:2px}@keyframes rec-blink{50%{opacity:0}}
.rec-text .rec-ended{color:#e84747;text-shadow:0 0 8px #700}
.rec-controls{position:absolute;left:0;right:0;bottom:0;height:56px;background:linear-gradient(#1a1a1a,#0a0a0a);border-top:1px solid #333;display:flex;align-items:center;gap:10px;padding:0 16px}
.rec-controls button{background:#2a2a2a;color:#ccc;border:1px solid #444;border-radius:3px;padding:4px 12px;font:12px Tahoma;cursor:pointer}.rec-controls button:hover{background:#3a3a3a;color:#fff}
.rec-progress{flex:1;height:6px;background:#222;border:1px solid #444;position:relative;border-radius:3px;overflow:hidden}.rec-progress .bar{position:absolute;left:0;top:0;bottom:0;width:0%;background:linear-gradient(90deg,#4a8fd8,#8fd0ff);transition:width .1s linear}
.rec-time{color:#888;font:11px Tahoma;min-width:80px;text-align:right}
/* Period-correct local web pages. Existing site-* forum/article styles remain in use. */
.arch-favs{white-space:nowrap;overflow:auto;gap:0!important;font:11px Tahoma;color:#6a7f98;scrollbar-width:auto}.arch-favs a{color:#1a3b73;text-decoration:none;margin:0 4px}.arch-favs a:hover{text-decoration:underline}.arch-ie-status{flex:none;padding:5px 10px;border-top:1px solid #b8c8dc;background:linear-gradient(#fff,#e4eaf2);color:#617488;font:11px Tahoma}
.t-site{background:#f8fafe}.t-header{min-height:68px;background:linear-gradient(#e8eef8,#c9d6ea);border-bottom:1px solid #92a9c4;padding:14px 22px;display:flex;align-items:center;justify-content:space-between;gap:15px}.t-logo{font:bold 24px Tahoma;color:#2f5890;text-shadow:0 1px #fff;letter-spacing:-.5px}.t-header nav{white-space:nowrap;font:11px Tahoma}.t-header a{margin:0 4px}.t-crumb{background:#eef2f9;color:#68778a;border-bottom:1px solid #cdd7e6;padding:8px 22px}.t-content{padding:20px 24px;flex:1;line-height:1.6}.t-content h1{font:normal 21px Tahoma;color:#1f4775;margin:2px 0 14px}.t-content h1 small{font:11px Tahoma;color:#8897a7}.t-content h2{font:normal 17px Tahoma;color:#335b88;margin:18px 0 8px}.t-footer{background:linear-gradient(#f8fafd,#e0e9f4);border-top:1px solid #cdd7e6;color:#798a9c;padding:12px 23px;font:11px Tahoma}.t-intro,.t-hint{background:#f1f5fa;border:1px solid #cdd7e6;padding:10px;margin:10px 0 16px;color:#697e95}.t-danger{color:#ad3030!important;font-weight:bold!important}.t-profiles{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px}.t-profile,.t-thread-row,.t-video,.t-news-item{cursor:pointer;text-align:left;background:linear-gradient(#fff,#f5f8fc);border:1px solid #cdd7e6;box-shadow:0 2px 7px rgba(0,0,0,.06);font:12px Tahoma;color:#273c54}.t-profile:hover,.t-thread-row:hover,.t-video:hover,.t-news-item:hover{background:linear-gradient(#f7fbff,#e4f0fc);border-color:#86a8cf}.t-profile{padding:10px;display:flex;align-items:center;gap:11px}.t-avatar{width:44px;height:44px;flex:none;display:grid;place-items:center;background:linear-gradient(#9fbad9,#4b779f);color:white;border:1px solid #7390ac;font:bold 23px Tahoma;box-shadow:inset 0 1px #fff8}.t-profile small,.t-thread-row small,.t-video small{display:block;color:#7c8999;margin-top:4px}.t-hero{background:linear-gradient(125deg,#edf5ed,#bed9c1);border:1px solid #94b9a1;padding:24px;margin-bottom:20px;color:#2a6340}.t-hero h1{color:#246b40}.t-news{background:#fff;border:1px solid #cdd7e6;box-shadow:0 2px 7px rgba(0,0,0,.06);padding:12px;margin:10px 0}.t-news b{color:#1a3b73}.t-table-head{padding:9px 13px;background:linear-gradient(#f8fafd,#dce8f5);border:1px solid #cdd7e6}.t-table-head span{float:right;color:#6e7e91}.t-thread-row{display:flex;align-items:center;gap:12px;padding:9px 12px;width:100%;border-top:0}.t-thread-row>span:nth-child(2){flex:1}.t-thread-row b{color:#1a3b73}.t-thread-row em{font-style:normal;color:#8894a3}.t-table{border-collapse:collapse;width:100%;background:#fff;border:1px solid #cdd7e6;box-shadow:0 2px 7px rgba(0,0,0,.06)}.t-table th,.t-table td{padding:10px;border-bottom:1px solid #dbe3ec;text-align:left}.t-table th{background:linear-gradient(#f8fbff,#e3ecf7);color:#426285}.t-warning{text-align:center;max-width:600px;margin:40px auto;padding:35px 20px;border:1px solid #cdd7e6;background:#fff;box-shadow:0 2px 7px rgba(0,0,0,.06)}.t-warning h1{color:#a33334}.t-login{max-width:380px;margin:24px auto;padding:22px;background:linear-gradient(#fff,#edf3fb);border:1px solid #a2b8d0;box-shadow:0 2px 7px rgba(0,0,0,.06)}.t-login label{display:block;color:#485d74;margin:10px 0}.t-login input{display:block;width:100%;margin-top:5px}.t-login-result{padding:8px;color:#a13132;min-height:28px}.t-videos{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px}.t-video{padding:8px;display:block;min-width:0}.t-video b{display:block;color:#1a3b73;margin-top:5px}.t-thumb{height:100px;display:grid;place-items:center;position:relative;background:repeating-linear-gradient(130deg,#343c4d,#343c4d 18px,#465569 18px,#465569 36px);color:#eee;font:28px Tahoma}.t-thumb small{position:absolute;bottom:3px;right:4px;color:white;background:#14191be0;padding:2px}.t-player{height:280px;background:repeating-linear-gradient(35deg,#111,#111 14px,#1b1b1b 14px,#1b1b1b 28px);color:#ddd;display:flex;flex-direction:column;align-items:center;justify-content:center;font:42px Tahoma}.t-player small{font:12px Tahoma;margin-top:12px}.t-search{background:#fff;border:1px solid #cdd7e6;padding:20px}.t-search input{min-width:230px;max-width:460px;width:60%;margin-right:8px}.t-search-hit{margin:17px 0}.t-search-hit a{font-size:16px}.t-search-hit small{display:block;color:#2e8a50}.t-wiki{background:#fff;border:1px solid #cdd7e6;padding:20px;line-height:1.8}.t-wiki-box{float:right;margin:0 0 12px 18px;background:#eef4fb;border:1px solid #a9bfd7;padding:12px;min-width:180px}.t-news-item{display:block;width:100%;padding:14px;margin:8px 0}.t-news-item b{color:#1a3b73;font-size:15px}.t-news-item p{margin:5px 0}.t-news-date{float:right;color:#8192a2}.t-site a{color:#1a3b73;text-decoration:none}.t-site a:hover{text-decoration:underline}.t-site button.site-btn,.t-site button[data-arch-login],.t-site button[data-tubby-search]{background:linear-gradient(#f7f9fc 45%,#e2e8f2 46%,#c9d3e2);border:1px solid #7a8aa0;color:#294869}.t-site input{border:1px solid #7a8aa0;box-shadow:inset 1px 1px 2px rgba(0,0,0,.15);font:12px Tahoma}.t-site::-webkit-scrollbar,.arch-favs::-webkit-scrollbar{width:16px;height:16px}.t-site::-webkit-scrollbar-thumb,.arch-favs::-webkit-scrollbar-thumb{background:linear-gradient(90deg,#cbd3dd,#8c9dae);border:1px solid #8a9bac}
@media(max-width:750px){.t-profiles{grid-template-columns:1fr}.t-videos{grid-template-columns:repeat(2,1fr)}.t-header{flex-wrap:wrap}.t-content{padding:12px}}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute"><defs>
<linearGradient id="gFB" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#f6d77a"/><stop offset="1" stop-color="#d9a636"/></linearGradient>
<linearGradient id="gFF" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#fff2b8"/><stop offset="1" stop-color="#f0c24e"/></linearGradient>
<linearGradient id="gBlue" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#8fd0ff"/><stop offset="1" stop-color="#1c6fd0"/></linearGradient>
<linearGradient id="gGreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#b3ee86"/><stop offset="1" stop-color="#2f9a2a"/></linearGradient>
<linearGradient id="gRed" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#ff9f8f"/><stop offset="1" stop-color="#c9301c"/></linearGradient>
<linearGradient id="gGray" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#fdfdfd"/><stop offset="1" stop-color="#b9c2cc"/></linearGradient>
<linearGradient id="gGlass" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#fff" stop-opacity=".95"/><stop offset="1" stop-color="#bdd5ee" stop-opacity=".6"/></linearGradient>
<linearGradient id="gScreen" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#6fc3ff"/><stop offset="1" stop-color="#1561c4"/></linearGradient>
<linearGradient id="gYel" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#fff3a0"/><stop offset="1" stop-color="#f2a61c"/></linearGradient>
<radialGradient id="ckf"><stop offset="0" stop-color="#fff"/><stop offset="1" stop-color="#cfe1f5"/></radialGradient>
</defs></svg>
<div id="wall"></div>
<div id="desktop"><div id="icons"></div><div id="gadget"></div><div id="band"></div></div>
<div id="snapprev"></div>
<div id="start"></div>
<div id="thumbs"></div>
<div id="clockpop" class="pop"></div>
<div id="volpop" class="pop"><div style="font-size:11px;margin-bottom:4px">Динамики</div><input type="range" min="0" max="100" id="volr"><div id="volv" style="margin-top:4px"></div></div>
<div id="netpop" class="pop"><div style="display:flex;gap:10px;align-items:center"><div id="netic"></div><div><b>Сеть 5</b><br>Подключено<br><span style="color:#555">Доступ к Интернету</span></div></div><hr style="border:0;border-top:1px solid #ccd;margin:10px 0"><div style="color:#1a56a8">Центр управления сетями</div></div>
<div id="balloon"></div>
<div id="taskbar">
 <div id="orb" title="Пуск"></div>
 <div id="tasks"></div>
 <div id="tray">
  <span class="tr" title="Показать скрытые значки">▲</span>
  <span class="tr" id="tr-flag" title="Центр поддержки"><svg width="16" height="16" viewBox="0 0 16 16"><path d="M3 1v14" stroke="#fff" stroke-width="1.6"/><path d="M3 2c4-2 6 2 10 0v7c-4 2-6-2-10 0z" fill="#fff"/></svg></span>
  <span class="tr" id="tr-net" data-pop="netpop" title="Сеть 5: Доступ к Интернету"></span>
  <span class="tr" id="tr-vol" data-pop="volpop" title="Динамики"></span>
  <span class="tr" id="lang" title="Русский (Россия)">РУС</span>
  <div id="clock" data-pop="clockpop"><div id="ck-t"></div><div id="ck-d"></div></div>
 </div>
 <div id="showdesk" title="Свернуть все окна"></div>
</div>
<div id="boot"></div>
<div id="logon"></div>
<div id="power"></div>

<div id="arch-brand">A.R.C.H.<small>ARCHIVE OF RECORDED CASES &amp; HISTORY</small></div><div id="arch-pixel"></div>
<div id="arch-notice"><b>Защита A.R.C.H.</b><br>Обнаружен неизвестный файл: record_04. Поместить в карантин?<br><button class="btn">Поместить в карантин</button><button class="btn">Отмена</button></div>
<div id="arch-bsod">A problem has been detected and Windows has been shut down to prevent damage to your computer.

The problem seems to be caused by the following file: r33.sys

UNKNOWN_HARDWARE_EXCEPTION

If this is the first time you've seen this Stop error screen, restart your computer.

*** STOP: 0x00000033 (0x00000000, 0x00000000, 0x00000000, 0x00000000)
*** r33.sys - Address 0x00000033 base at 0x00000000

Beginning dump of physical memory
<div style="border:1px solid #fff;width:220px;height:12px"><div style="width:33%;height:100%;background:#fff"></div></div>33%
Physical memory dump complete.</div><div id="arch-dark"></div><div id="arch-game">ЗАПИСЬ 01<button id="arch-return">Вернуться на рабочий стол</button></div>
<script>
'use strict';
/* ================= helpers ================= */
const $=(s,r=document)=>r.querySelector(s),$$=(s,r=document)=>[...r.querySelectorAll(s)];
const el=(t,c,h)=>{const e=document.createElement(t);if(c)e.className=c;if(h!=null)e.innerHTML=h;return e};
const esc=s=>String(s).replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
const store={get(k,d){try{const v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}},set(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}};
const cfg=Object.assign({wall:'cat',theme:'sky',glass:true,vol:70},store.get('w7cfg',{}));
const saveCfg=()=>store.set('w7cfg',cfg);
const pad=n=>String(n).padStart(2,'0');
const MONTHS=['января','февраля','марта','апреля','мая','июня','июля','августа','сентября','октября','ноября','декабря'];
const MONTHS_N=['Январь','Февраль','Март','Апрель','Май','Июнь','Июль','Август','Сентябрь','Октябрь','Ноябрь','Декабрь'];
const DAYS=['воскресенье','понедельник','вторник','среда','четверг','пятница','суббота'];
const arch={time:'03:33',observer:0,showHidden:false,viewed00:store.get('arch-viewed00',false),booted:false,notice:false,
 observerText(){return 'A.R.C.H. observer.log\nЛог наблюдателя / протокол 33\n03:33:12 — user открыл record_01\n03:33:40 — user посмотрел в сторону\n03:33:59 — observer смотрит\n03:34:00 — user открыл record_02\n'+(this.events||[]).join('\n')+'\nobserver смотрит'}};
/* ================= sound ================= */
let actx;
function audio(){if(!actx){try{actx=new(window.AudioContext||window.webkitAudioContext)()}catch(e){}}if(actx&&actx.state==='suspended')actx.resume();return actx}
function tone(f,t0,dur,type,vol){const a=audio();if(!a)return;const o=a.createOscillator(),g=a.createGain(),v=Math.max(.0002,(vol||.2)*cfg.vol/100),t=a.currentTime+t0;o.type=type||'sine';o.frequency.value=f;g.gain.setValueAtTime(.0001,t);g.gain.linearRampToValueAtTime(v,t+.02);g.gain.exponentialRampToValueAtTime(.0001,t+dur);o.connect(g);g.connect(a.destination);o.start(t);o.stop(t+dur+.05)}
const sfx={ding(){tone(880,0,.25,'triangle');tone(660,.13,.3,'triangle')},start(){[392,523,659,784,1047].forEach((f,i)=>tone(f,i*.13,1.3,'sine',.14))}};
/* ================= icons ================= */
const calcBtns=(()=>{let s='';for(let r=0;r<4;r++)for(let c=0;c<4;c++)s+=`<rect x="${13+c*6}" y="${21+r*6}" width="4.5" height="4.5" fill="${c==3?'#e0902a':'#6b7c8c'}"/>`;return s})();
const ICONS={
folder:'<path d="M4 11h14l4 4h22v27H4z" fill="url(#gFB)" stroke="#b58a24"/><path d="M4 21h41l-3 21H4z" fill="url(#gFF)" stroke="#c9972c"/>',
computer:'<rect x="5" y="6" width="38" height="27" rx="3" fill="url(#gGray)" stroke="#4b5a69"/><rect x="9" y="10" width="30" height="19" fill="url(#gScreen)" stroke="#1d3f73"/><path d="M9 10h30v7c-10 3-20 3-30 0z" fill="#fff" opacity=".28"/><path d="M18 33h12l2 6H16z" fill="#aab4bf" stroke="#4b5a69"/><rect x="11" y="39" width="26" height="4" rx="2" fill="url(#gGray)" stroke="#4b5a69"/>',
trash:'<path d="M11 12h26l-3 31H14z" fill="url(#gGlass)" stroke="#5f7386" stroke-width="1.5"/><path d="M9 12h30" stroke="#5f7386" stroke-width="3" stroke-linecap="round"/><path d="M17 31a8 8 0 0 1 3-11" stroke="#2fa04a" stroke-width="3" fill="none"/><path d="M31 31a8 8 0 0 0-3-11" stroke="#2fa04a" stroke-width="3" fill="none"/><path d="M17 37h14" stroke="#2fa04a" stroke-width="3"/><path d="M17 17l-3 6 7 0z M31 17l3 6-7 0z" fill="#2fa04a"/>',
trashfull:'<path d="M11 14h26l-3 29H14z" fill="url(#gGlass)" stroke="#5f7386" stroke-width="1.5"/><path d="M13 14l4-8 8 3 6-4 5 9z" fill="#fff" stroke="#8a97a5"/><path d="M9 14h30" stroke="#5f7386" stroke-width="3" stroke-linecap="round"/><path d="M17 33a8 8 0 0 1 3-9" stroke="#2fa04a" stroke-width="3" fill="none"/><path d="M31 33a8 8 0 0 0-3-9" stroke="#2fa04a" stroke-width="3" fill="none"/>',
notepad:'<rect x="9" y="5" width="30" height="38" rx="2" fill="#fff" stroke="#5b7ba3"/><rect x="9" y="5" width="30" height="8" fill="url(#gBlue)" stroke="#2b5fa6"/><path d="M14 20h20M14 26h20M14 32h13" stroke="#7a9cc8" stroke-width="2"/><path d="M30 41l12-14 3 3-12 14-5 2z" fill="url(#gYel)" stroke="#8a6a10"/>',
calc:'<rect x="9" y="4" width="30" height="40" rx="4" fill="url(#gGray)" stroke="#4b5a69"/><rect x="13" y="8" width="22" height="9" fill="#c3ecb4" stroke="#4b5a69"/>'+calcBtns,
paint:'<path d="M24 6C12 6 5 15 6 25c1 9 9 17 18 17 4 0 5-3 3-5-2-3 0-6 4-6h6c4 0 7-3 7-7C44 12 36 6 24 6z" fill="#f4dcab" stroke="#8a6d3b"/><circle cx="15" cy="20" r="3.5" fill="#e53935"/><circle cx="24" cy="14" r="3.5" fill="#fdd835"/><circle cx="33" cy="18" r="3.5" fill="#43a047"/><circle cx="14" cy="30" r="3.5" fill="#1e88e5"/>',
mine:'<circle cx="24" cy="25" r="11" fill="#222"/><path d="M24 7v36M6 25h36M11 12l26 26M37 12L11 38" stroke="#222" stroke-width="3"/><circle cx="20" cy="21" r="3.2" fill="#fff"/>',
ie:'<circle cx="24" cy="25" r="15" fill="url(#gBlue)" stroke="#1c4f9c"/><text x="24" y="34" text-anchor="middle" font-family="Georgia,serif" font-weight="bold" font-size="27" fill="#fff">e</text><ellipse cx="24" cy="25" rx="21" ry="8" transform="rotate(-25 24 25)" fill="none" stroke="#f5c518" stroke-width="3"/>',
cmd:'<rect x="4" y="8" width="40" height="32" rx="2" fill="#111" stroke="#666"/><rect x="4" y="8" width="40" height="5" fill="#ddd"/><path d="M10 21l6 4-6 4" stroke="#ddd" stroke-width="2" fill="none"/><path d="M19 31h9" stroke="#ddd" stroke-width="2"/>',
control:'<rect x="5" y="9" width="38" height="30" rx="3" fill="#e9eef5" stroke="#5b7ba3"/><rect x="9" y="14" width="12" height="8" fill="url(#gBlue)"/><rect x="25" y="14" width="14" height="4" fill="url(#gGreen)"/><circle cx="31" cy="29" r="5" fill="url(#gYel)" stroke="#8a6a10"/><rect x="9" y="26" width="12" height="8" fill="url(#gRed)"/>',
doc:'<path d="M10 4h20l10 10v30H10z" fill="#fff" stroke="#6b7c8c"/><path d="M30 4v10h10" fill="#dfe6ee" stroke="#6b7c8c"/><path d="M15 22h20M15 28h20M15 34h14" stroke="#9db0c8" stroke-width="2"/>',
img:'<rect x="5" y="9" width="38" height="30" fill="#fff" stroke="#6b7c8c"/><rect x="8" y="12" width="32" height="24" fill="url(#gScreen)"/><path d="M8 36l10-12 8 8 6-6 8 10z" fill="#3a9a3a"/><circle cx="33" cy="19" r="3" fill="#ffe066"/>',
music:'<circle cx="16" cy="36" r="6" fill="url(#gBlue)" stroke="#1c4f9c"/><circle cx="34" cy="32" r="6" fill="url(#gBlue)" stroke="#1c4f9c"/><path d="M22 36V10l18-4v26" stroke="#1c4f9c" stroke-width="3" fill="none"/>',
drive:'<rect x="4" y="16" width="40" height="18" rx="3" fill="url(#gGray)" stroke="#4b5a69"/><rect x="8" y="26" width="22" height="3" fill="#8fa0b0"/><circle cx="37" cy="28" r="2.5" fill="#4fd14f"/>',
dvd:'<circle cx="24" cy="24" r="18" fill="url(#gGray)" stroke="#4b5a69"/><circle cx="24" cy="24" r="6" fill="#fff" stroke="#4b5a69"/><circle cx="24" cy="24" r="2" fill="#4b5a69"/>',
user:'<circle cx="24" cy="16" r="9" fill="#f6c7a0" stroke="#9a6b43"/><path d="M6 46c0-12 8-17 18-17s18 5 18 17z" fill="url(#gBlue)" stroke="#1c4f9c"/>',
taskmgr:'<rect x="4" y="7" width="40" height="34" rx="2" fill="#fff" stroke="#4b5a69"/><rect x="4" y="7" width="40" height="6" fill="url(#gBlue)"/><path d="M7 33l8-10 6 6 8-14 6 8 6-4" stroke="#2fa04a" stroke-width="2.5" fill="none"/>',
info:'<circle cx="24" cy="24" r="19" fill="url(#gBlue)" stroke="#1c4f9c"/><rect x="21.5" y="21" width="5" height="14" rx="1" fill="#fff"/><circle cx="24" cy="15" r="3" fill="#fff"/>',
question:'<circle cx="24" cy="24" r="19" fill="url(#gBlue)" stroke="#1c4f9c"/><text x="24" y="34" text-anchor="middle" font-family="Arial" font-weight="bold" font-size="28" fill="#fff">?</text>',
warn:'<path d="M24 5L45 41H3z" fill="url(#gYel)" stroke="#9a7410" stroke-linejoin="round" stroke-width="2"/><rect x="22" y="17" width="4" height="13" fill="#333"/><circle cx="24" cy="35" r="2.5" fill="#333"/>',
error:'<circle cx="24" cy="24" r="19" fill="url(#gRed)" stroke="#8c1a0a"/><path d="M16 16l16 16M32 16L16 32" stroke="#fff" stroke-width="5" stroke-linecap="round"/>',
wmp:'<circle cx="24" cy="24" r="19" fill="url(#gYel)" stroke="#a5600a"/><circle cx="24" cy="24" r="13" fill="url(#gBlue)" stroke="#1c4f9c"/><path d="M20 16l13 8-13 8z" fill="#fff"/>',
shield:'<path d="M24 4l17 6v14c0 9-7 16-17 20C14 40 7 33 7 24V10z" fill="url(#gGreen)" stroke="#256b22"/><path d="M16 24l6 6 11-12" stroke="#fff" stroke-width="4" fill="none"/>',
clock:'<circle cx="24" cy="24" r="19" fill="#fff" stroke="#4b6a99" stroke-width="2"/><path d="M24 11v14l9 6" stroke="#223" stroke-width="3" fill="none"/>',
sound:'<path d="M7 18h8l10-8v28l-10-8H7z" fill="url(#gGray)" stroke="#4b5a69"/><path d="M31 16c4 5 4 11 0 16M36 11c7 8 7 18 0 26" stroke="#2b7fd0" stroke-width="3" fill="none"/>',
net:'<circle cx="24" cy="24" r="19" fill="url(#gBlue)" stroke="#1c4f9c"/><path d="M8 20c10 4 22 0 32 4M10 32c10-4 20 0 30-3M24 5c-8 10-8 28 0 38M24 5c8 10 8 28 0 38" stroke="#bff" fill="none" stroke-width="1.5"/>',
shutdown:'<circle cx="24" cy="24" r="19" fill="url(#gRed)" stroke="#8c1a0a"/><path d="M24 11v14M16 17a11 11 0 1 0 16 0" stroke="#fff" stroke-width="4" fill="none" stroke-linecap="round"/>'
};
const ic=(n,s=32)=>`<svg class="ic" width="${s}" height="${s}" viewBox="0 0 48 48">${ICONS[n]||ICONS.doc}</svg>`;
const LOGO='<svg viewBox="0 0 48 48"><path d="M5 10c6-3 11-2 17 0v14c-6-2-11-3-17 0z" fill="#f35325"/><path d="M26 11c6 2 12 2 18-1v14c-6 3-12 3-18 0z" fill="#81bc06"/><path d="M5 27c6-3 11-2 17 0v14c-6-2-11-3-17 0z" fill="#05a6f0"/><path d="M26 28c6 2 12 2 18-1v14c-6 3-12 3-18 0z" fill="#ffba08"/></svg>';
const USERPIC='<svg width="100%" viewBox="0 0 48 48" style="display:block;margin-top:auto"><circle cx="24" cy="18" r="9" fill="#f8d2b0"/><path d="M5 48c0-13 8-18 19-18s19 5 19 18z" fill="#fff"/></svg>';
/* ================= file system ================= */
const mkd=(c,p)=>({type:'dir',children:c||{},prot:!!p}),mkt=t=>({type:'file',kind:'txt',content:t}),mka=a=>({type:'file',kind:'app',app:a,prot:true}),mki=s=>({type:'file',kind:'img',src:s}),mkm=()=>({type:'file',kind:'audio'});
const px=id=>'data:image/svg+xml,'+encodeURIComponent('<svg xmlns="http://www.w3.org/2000/svg" width="800" height="600"><defs><linearGradient id="g" x2="1" y2="1"><stop stop-color="#111b2c"/><stop offset="1" stop-color="#02040a"/></linearGradient></defs><rect width="800" height="600" fill="url(#g)"/></svg>');
const WALLS=[
 {id:'cat',name:'Котёнок в цветах',url:px(16278277)},
 {id:'peony',name:'Белые пионы',url:px(8345863)},
 {id:'peony2',name:'Пионы на солнце',url:px(12082989)},
 {id:'peony3',name:'Нежные пионы',url:px(12155551)},
 {id:'aero',name:'Windows 7 Aero',css:'radial-gradient(ellipse at 30% 110%,#bfefff 0,#4aa7e8 30%,#1b5fb4 60%,#07204d 100%)'},
 {id:'dark',name:'Тёмная тема',css:'radial-gradient(ellipse at 50% 50%,#2c3e55,#0a1020)'}
];
const HOME=['Локальный диск (C:)','Users','white'];
const P_DESK=[...HOME,'Desktop'],P_DOCS=[...HOME,'Documents'],P_PICS=['Локальный диск (C:)','Пользователи','User','Изображения'],P_MUS=['Локальный диск (C:)','Пользователи','User','Музыка'],P_DL=['Локальный диск (C:)','Пользователи','User','Загрузки'];
const P_REC=[...P_DESK,'Записи'],P_TEMP=['Локальный диск (C:)','Windows','Temp'];
function defaultFS(){return mkd({
 'Локальный диск (C:)':{type:'dir',drive:'hdd',prot:true,children:{
  'Windows':mkd({'System32':mkd({'notepad.exe':mka('notepad'),'calc.exe':mka('calc'),'mspaint.exe':mka('paint'),'cmd.exe':mka('cmd'),'taskmgr.exe':mka('taskmgr')},1),'explorer.exe':mka('explorer')},1),
  'Program Files':mkd({'Internet Explorer':mkd({'iexplore.exe':mka('ie')},1),'Windows Media Player':mkd({'wmplayer.exe':mka('wmp')},1)},1),
  'Пользователи':mkd({'User':mkd({
   'Рабочий стол':mkd({},1),
   'Документы':mkd({'Добро пожаловать.txt':mkt('Добро пожаловать в Windows 7!\r\n\r\nЭто браузерный симулятор рабочего стола.\r\nОкна можно перетаскивать, менять размер, сворачивать и разворачивать.\r\nПопробуйте перетащить окно к краю экрана (Aero Snap).\r\n\r\nПуск → Панель управления → Персонализация: смена обоев и цвета окон.'),'Список дел.txt':mkt('1. Выпить чаю\r\n2. Погладить кота\r\n3. Сыграть в Сапёра\r\n4. Нарисовать шедевр в Paint')},1),
   'Изображения':mkd({'Котёнок.jpg':mki(WALLS[0].url),'Пионы.jpg':mki(WALLS[1].url),'Пионы на солнце.jpg':mki(WALLS[2].url)},1),
   'Музыка':mkd({'Калимба.mp3':mkm()},1),
   'Загрузки':mkd({},1)
  },1)},1)}},
 'DVD RW дисковод (D:)':{type:'dir',drive:'dvd',prot:true,children:{}}
})}
let COMP,TRASH;
(function(){const s=store.get('w7fs3',null);if(s&&s.comp&&s.trash){COMP=s.comp;TRASH=s.trash}else{COMP=defaultFS();TRASH=mkd()}})();
const saveFS=()=>store.set('w7fs3',{comp:COMP,trash:TRASH});
const resolve=p=>{if(p[0]==='::trash')return TRASH;let n=COMP;for(const x of p){n=n.children&&n.children[x];if(!n)return null}return n};
function uniq(dir,name){if(!dir.children[name])return name;const m=name.match(/^(.*?)(\.[^.]*)?$/);let i=2;while(dir.children[`${m[1]} (${i})${m[2]||''}`])i++;return `${m[1]} (${i})${m[2]||''}`}
const explorers=new Set();
function fsChanged(){saveFS();explorers.forEach(e=>e.refresh());renderDesktop()}
function fsDelete(path,name){const d=resolve(path);if(!d||!d.children[name])return;const n=d.children[name];if(path[0]==='::trash'){delete d.children[name];return}n.origin=path.slice();TRASH.children[uniq(TRASH,name)]=n;delete d.children[name]}
function fsRestore(name){const n=TRASH.children[name];if(!n)return;const d=resolve(n.origin||P_DESK)||resolve(P_DESK);d.children[uniq(d,name)]=n;delete n.origin;delete TRASH.children[name]}
function fsRename(path,old,nw){nw=nw.trim();const d=resolve(path);if(!nw||/[\\\/:*?"<>|]/.test(nw)){msgBox({title:'Переименование',icon:'error',text:'Имя файла не должно содержать следующих знаков: \\ / : * ? " < > |'});return false}if(nw===old)return true;if(d.children[nw]){msgBox({title:'Переименование',icon:'error',text:'Файл с таким именем уже существует. Укажите другое имя.'});return false}d.children={...Object.fromEntries(Object.entries(d.children).map(([k,v])=>[k===old?nw:k,v]))};return true}
function kindLabel(n){if(n.type==='dir')return n.drive?'Локальный диск':'Папка с файлами';return{txt:'Текстовый документ',img:'Файл JPG',audio:'Файл MP3',app:'Приложение',record:'Архивная запись'}[n.kind]||'Файл'}
function sizeOf(n){if(n.type==='dir')return '';const b=n.kind==='txt'?(n.content||'').length:n.kind==='img'?842000:n.kind==='audio'?3400000:152000;return b<1024?b+' байт':b<1048576?Math.max(1,Math.round(b/1024))+' КБ':(b/1048576).toFixed(1).replace('.',',')+' МБ'}
function nodeIcon(n,s){if(n.type==='dir')return ic(n.drive==='dvd'?'dvd':n.drive?'drive':'folder',s);return ic({txt:'doc',img:'img',audio:'music',record:'wmp'}[n.kind]||(n.kind==='app'&&APPS[n.app]?APPS[n.app].icon:'doc'),s)}
function walk(n,path,cb){if(n.type!=='dir')return;for(const[k,v]of Object.entries(n.children)){cb(k,v,path);if(v.type==='dir')walk(v,[...path,k],cb)}}
function openNode(node,path,name){
 if(path[0]==='::trash'){msgBox({title:'Корзина',icon:'warn',text:'Невозможно открыть элементы в корзине. Чтобы открыть этот элемент, сначала его необходимо восстановить.'});return}
 if(node.type==='dir')return launch('explorer',[...path,name]);
 if(node.kind==='record')return playRecord(node.recId);
 if(node.kind==='txt'){archRecordViewed(name);if(name==='record_00.dat'){arch.viewed00=true;store.set('arch-viewed00',true)}return launch('notepad',{path,name})}
 if(node.kind==='img')return launch('viewer',{src:node.src,name});
 if(node.kind==='audio')return launch('wmp',{name});
 if(node.kind==='app')return launch(node.app)}
function deleteNodes(path,names){
 if(!names.length)return;const d=resolve(path);
 if(names.some(n=>d.children[n]&&d.children[n].prot)){msgBox({title:'Удаление',icon:'error',text:'Отказано в доступе. Для удаления этого элемента требуется разрешение администратора.'});return}
 const perm=path[0]==='::trash';
 msgBox({title:perm?'Удаление файла':'Удаление файла',icon:'question',text:names.length>1?`Вы действительно хотите ${perm?'безвозвратно удалить':'переместить в корзину'} выбранные объекты (${names.length})?`:`Вы действительно хотите ${perm?'безвозвратно удалить':'переместить в корзину'} «${names[0]}»?`,buttons:['Да','Нет'],cb:i=>{if(i===0){names.forEach(n=>fsDelete(path,n));fsChanged()}}})}
function renameFlow(path,name){inputDialog({title:'Переименование',label:'Новое имя:',value:name,cb:v=>{if(fsRename(path,name,v))fsChanged()}})}
function newItem(path,type){const d=resolve(path);if(!d||path[0]==='::trash'||!path.length)return;const n=uniq(d,type==='dir'?'Новая папка':'Новый текстовый документ.txt');d.children[n]=type==='dir'?mkd():mkt('');fsChanged();return n}
function propsBox(path,name){const n=resolve(path).children[name];msgBox({title:'Свойства: '+name,icon:n.type==='dir'?'folder':'doc',html:`<b>${esc(name)}</b><br><br>Тип: ${kindLabel(n)}<br>Расположение: C:\\${esc(path.slice(1).join('\\'))}<br>Размер: ${sizeOf(n)||'—'}<br>Изменён: сегодня`})}
/* ================= wallpaper / theme ================= */
let LOCAL_WALL=false;const FALL='radial-gradient(ellipse at 50% 40%,#f6f0e7,#d9cdbb 70%,#b9a98f)';
function walls(){const a=[...WALLS];if(LOCAL_WALL)a.unshift({id:'local',name:'Мои обои (wallpaper.jpg)',url:'wallpaper.jpg'});const c=store.get('w7custom',null);if(c)a.push({id:'custom',name:'Мой рисунок',url:c});return a}
function applyWall(){const w=walls().find(x=>x.id===cfg.wall)||WALLS[0];$('#wall').style.backgroundImage=w.url?`url("${w.url}"),${FALL}`:w.css}
function setCustomWall(url){store.set('w7custom',url);cfg.wall='custom';saveCfg();applyWall()}
const THEMES=[['sky','Небо',210,60],['twi','Сумерки',255,40],['sea','Море',185,60],['leaf','Лист',115,45],['blush','Румянец',340,55],['pump','Тыква',28,75],['frost','Мороз',210,15],['grph','Графит',220,6]];
function applyTheme(){const t=THEMES.find(x=>x[0]===cfg.theme)||THEMES[0];document.documentElement.style.setProperty('--h',t[2]);document.documentElement.style.setProperty('--s',t[3]);document.body.classList.toggle('noglass',!cfg.glass)}
/* A.R.C.H.: no local wallpaper file or external asset is loaded. */
/* ================= window manager ================= */
const DESK=$('#desktop');const wins=[];let zTop=100,idc=0,activeWin=null;
function applyRect(w){const r=w.rect,s=w.el.style;s.left=r.x+'px';s.top=r.y+'px';s.width=r.w+'px';if(r.h)s.height=r.h+'px'}
function fitWin(w,cw,ch){w.el.style.width=(cw+18)+'px';w.el.style.height=(ch+41)+'px';w.rect.w=cw+18;w.rect.h=ch+41}
function createWindow(o){
 o=Object.assign({w:640,h:420,icon:'doc',title:'',app:'',minW:220,minH:120,resizable:true,maxable:true,minable:true,task:true},o);
 const W=Math.min(o.w,innerWidth-10),H=o.h?Math.min(o.h,innerHeight-50):0,n=wins.length;
 let x=o.x!=null?o.x:Math.max(0,Math.min(innerWidth-W-10,70+(n%9)*30)),y=o.y!=null?o.y:Math.max(0,Math.min(innerHeight-40-(H||200)-5,30+(n%9)*28));
 const e=el('div','win');
 e.innerHTML=`<div class="tb"><span class="ti">${ic(o.icon,16)}</span><span class="tt"></span><div class="caps">${o.minable?'<div class="cap bmin"><i class="gmin"></i></div>':''}${o.maxable?'<div class="cap bmax"><i class="gmax"></i></div>':''}<div class="cap close"><svg width="14" height="12" viewBox="0 0 14 12" style="filter:drop-shadow(0 0 1px #300)"><path d="M3 1.5l8 9M11 1.5l-8 9" stroke="#fff" stroke-width="2.6" stroke-linecap="round"/></svg></div></div></div><div class="wbody"></div>`;
 $('.tt',e).textContent=o.title;
 const win={id:++idc,o,el:e,body:$('.wbody',e),app:o.app,icon:o.icon,title:o.title,min:false,max:false,snap:false,rect:{x,y,w:W,h:H},child:null,parent:o.parent||null,
  setTitle(t){win.title=t;$('.tt',e).textContent=t;renderTasks()},
  recenter(){const w=e.offsetWidth,h=e.offsetHeight;win.rect.x=Math.max(0,(innerWidth-w)/2);win.rect.y=Math.max(0,(innerHeight-40-h)/2-30);win.rect.h=0;e.style.left=win.rect.x+'px';e.style.top=win.rect.y+'px'}};
 applyRect(win);e.style.zIndex=++zTop;DESK.append(e);wins.push(win);arch.observer++;archLogEvent('окно открыто: '+o.title);
 if(o.parent){o.parent.child=win;const sh=el('div','shield');sh.onpointerdown=ev=>{ev.stopPropagation();focusWin(win);win.el.animate([{opacity:.4},{opacity:1}],{duration:200,iterations:2})};o.parent.el.append(sh);win.shield=sh}
 e.addEventListener('pointerdown',()=>focusWin(win),true);
 const caps=$('.caps',e);caps.addEventListener('pointerdown',ev=>ev.stopPropagation());
 const bmin=$('.bmin',e),bmax=$('.bmax',e);
 if(bmin)bmin.onclick=()=>minWin(win);if(bmax)bmax.onclick=()=>toggleMax(win);$('.close',e).onclick=()=>closeWin(win);
 const tb=$('.tb',e);tb.addEventListener('dblclick',ev=>{if(ev.target.closest('.cap'))return;if(ev.target.closest('.ti'))closeWin(win);else toggleMax(win)});
 tb.addEventListener('contextmenu',ev=>{ev.preventDefault();focusWin(win);showMenu(ev.clientX,ev.clientY,[{t:'Восстановить',dis:!win.max&&!win.snap,fn:()=>toggleMax(win)},{t:'Свернуть',dis:!o.minable,fn:()=>minWin(win)},{t:'Развернуть',dis:!o.maxable||win.max,fn:()=>toggleMax(win)},'-',{t:'Закрыть',key:'Alt+F4',def:1,fn:()=>closeWin(win)}])});
 $('.ti',e).addEventListener('click',ev=>{const r=ev.currentTarget.getBoundingClientRect();showMenu(r.left,r.bottom,[{t:'Восстановить',dis:!win.max,fn:()=>toggleMax(win)},{t:'Свернуть',dis:!o.minable,fn:()=>minWin(win)},{t:'Развернуть',dis:!o.maxable||win.max,fn:()=>toggleMax(win)},'-',{t:'Закрыть',def:1,fn:()=>closeWin(win)}])});
 setupDrag(win);
 if(o.resizable)['n','s','e','w','ne','nw','se','sw'].forEach(d=>{const h=el('div','rz rz-'+d);setupResize(win,h,d);e.append(h)});
 if(o.center&&H)win.recenter(),win.rect.h=H;
 focusWin(win);renderTasks();return win}
function setupDrag(win){
 const tb=$('.tb',win.el),prev=$('#snapprev');
 tb.addEventListener('pointerdown',e=>{
  if(e.button!==0||e.target.closest('.cap')||e.target.closest('.ti'))return;
  const sx=e.clientX,sy=e.clientY;let ox,oy,started=false,snapMode=null;
  const dh=innerHeight-40;
  const move=ev=>{
   if(!started){if(Math.hypot(ev.clientX-sx,ev.clientY-sy)<4)return;started=true;document.body.classList.add('dragging');
    const r=win.el.getBoundingClientRect();
    if(win.max||win.snap){ox=win.rect.w*((sx-r.left)/r.width);oy=Math.min(sy-r.top,15);win.max=false;win.snap=false;win.el.classList.remove('max');const g=$('.bmax i',win.el);if(g)g.className='gmax';applyRect(win)}
    else{ox=sx-r.left;oy=sy-r.top}}
   const nx=Math.max(-win.el.offsetWidth+120,Math.min(innerWidth-120,ev.clientX-ox)),ny=Math.max(0,Math.min(dh-30,ev.clientY-oy));
   win.el.style.left=nx+'px';win.el.style.top=ny+'px';
   snapMode=null;if(win.o.resizable&&win.o.maxable){if(ev.clientY<=1)snapMode='max';else if(ev.clientX<=1)snapMode='l';else if(ev.clientX>=innerWidth-2)snapMode='r'}
   if(snapMode){prev.style.display='block';const s=prev.style;s.top='0';s.height=dh+'px';s.left=snapMode==='r'?'50%':'0';s.width=snapMode==='max'?'100%':'50%'}else prev.style.display='none'};
  const up=()=>{removeEventListener('pointermove',move);removeEventListener('pointerup',up);document.body.classList.remove('dragging');prev.style.display='none';if(!started)return;
   if(snapMode==='max'){toggleMax(win)}
   else if(snapMode){const s=win.el.style;s.left=snapMode==='r'?'50%':'0';s.top='0';s.width='50%';s.height=dh+'px';win.snap=true}
   else{win.rect.x=win.el.offsetLeft;win.rect.y=win.el.offsetTop}};
  addEventListener('pointermove',move);addEventListener('pointerup',up)})}
function setupResize(win,h,d){
 h.addEventListener('pointerdown',e=>{
  if(e.button!==0||win.max)return;e.preventDefault();e.stopPropagation();focusWin(win);
  const sx=e.clientX,sy=e.clientY,r0={x:win.el.offsetLeft,y:win.el.offsetTop,w:win.el.offsetWidth,h:win.el.offsetHeight};document.body.classList.add('dragging');
  const move=ev=>{const dx=ev.clientX-sx,dy=ev.clientY-sy;let{x,y,w,h}=r0;
   if(d.includes('e'))w=Math.max(win.o.minW,r0.w+dx);if(d.includes('s'))h=Math.max(win.o.minH,r0.h+dy);
   if(d.includes('w')){w=Math.max(win.o.minW,r0.w-dx);x=r0.x+r0.w-w}if(d.includes('n')){h=Math.max(win.o.minH,r0.h-dy);y=Math.max(0,r0.y+r0.h-h);h=r0.y+r0.h-y}
   const s=win.el.style;s.left=x+'px';s.top=y+'px';s.width=w+'px';s.height=h+'px'};
  const up=()=>{removeEventListener('pointermove',move);removeEventListener('pointerup',up);document.body.classList.remove('dragging');win.snap=false;win.rect={x:win.el.offsetLeft,y:win.el.offsetTop,w:win.el.offsetWidth,h:win.el.offsetHeight};if(win.onResize)win.onResize()};
  addEventListener('pointermove',move);addEventListener('pointerup',up)})}
function focusWin(win){
 if(win.child&&wins.includes(win.child))win=win.child;
 if(win.min){win.min=false;win.el.classList.remove('min')}
 wins.forEach(w=>w.el.classList.toggle('active',w===win));win.el.style.zIndex=++zTop;activeWin=win;renderTasks()}
function minWin(win){win.min=true;win.el.classList.add('min');if(activeWin===win){activeWin=null;nextActive()}renderTasks()}
function nextActive(){const c=wins.filter(w=>!w.min).sort((a,b)=>b.el.style.zIndex-a.el.style.zIndex)[0];if(c)focusWin(c);else{activeWin=null;wins.forEach(w=>w.el.classList.remove('active'));renderTasks()}}
function toggleMax(win){
 if(!win.o.maxable)return;const g=$('.bmax i',win.el);
 if(win.max||win.snap){win.max=false;win.snap=false;win.el.classList.remove('max');applyRect(win);if(g)g.className='gmax'}
 else{win.max=true;win.el.classList.add('max');if(g)g.className='grest'}
 if(win.onResize)setTimeout(win.onResize,0)}
function closeWin(win,force){
 if(!force&&win.o.beforeClose){win.o.beforeClose(()=>closeWin(win,true));return}
 const i=wins.indexOf(win);if(i<0)return;wins.splice(i,1);win.el.classList.add('closing');setTimeout(()=>win.el.remove(),160);
 if(win.o.onClose)win.o.onClose();
 if(win.parent){win.parent.child=null;if(win.shield)win.shield.remove()}
 if(win.child)closeWin(win.child,true);
 if(activeWin===win){activeWin=null;nextActive()}renderTasks()}
/* ================= menus & dialogs ================= */
function killSub(m){if(m._sub){killSub(m._sub);m._sub.remove();m._sub=null}}
function closeMenus(){$$('.ctx').forEach(m=>m.remove());$$('.mb-item.on').forEach(b=>b.classList.remove('on'))}
function showMenu(x,y,items,sub,altX){
 if(!sub)closeMenus();const m=el('div','ctx');
 items.forEach(it=>{
  if(it==='-'){m.append(el('div','ctx-sep'));return}
  const r=el('div','ctx-i'+(it.dis?' dis':'')+(it.def?' def':''));
  r.innerHTML=`<span class="ck">${it.chk?'✓':(it.ico?ic(it.ico,16):'')}</span><span class="cl">${esc(it.t)}</span><span class="cs">${it.key||''}${it.sub?'▸':''}</span>`;
  r.onmouseenter=()=>{killSub(m);if(it.sub&&!it.dis){const b=r.getBoundingClientRect();m._sub=showMenu(b.right-3,b.top-3,it.sub,true,b.left+3)}};
  if(!it.dis)r.onclick=e=>{e.stopPropagation();if(it.sub)return;closeMenus();if(it.fn)it.fn()};
  m.append(r)});
 document.body.append(m);const w=m.offsetWidth,h=m.offsetHeight;
 if(x+w>innerWidth)x=sub&&altX?altX-w:innerWidth-w-2;if(y+h>innerHeight)y=Math.max(0,innerHeight-h-2);
 m.style.left=x+'px';m.style.top=y+'px';return m}
function menubar(menus){
 const bar=el('div','menubar');
 const open=(b,m)=>{closeMenus();b.classList.add('on');const r=b.getBoundingClientRect();showMenu(r.left,r.bottom,typeof m.items==='function'?m.items():m.items);b.classList.add('on')};
 menus.forEach(m=>{const b=el('div','mb-item',m.t);
  b.onpointerdown=e=>{e.stopPropagation();if(b.classList.contains('on'))closeMenus();else open(b,m)};
  b.onmouseenter=()=>{if($('.mb-item.on')&&!b.classList.contains('on'))open(b,m)};bar.append(b)});
 return bar}
function msgBox(o){
 const btns=o.buttons||['OK'];let done=false;const fin=i=>{if(done)return;done=true;if(o.cb)o.cb(i)};
 const w=createWindow({app:'dialog',title:o.title||'Windows',icon:o.icon||'info',w:o.w||390,h:0,minW:100,minH:50,minable:false,maxable:false,resizable:false,task:false,parent:o.parent,onClose:()=>fin(-1)});
 w.body.innerHTML=`<div class="dlg"><div class="dlg-t">${ic(o.icon||'info',32)}<div class="dlg-m">${o.html||esc(o.text||'')}</div></div><div class="dlg-b"></div></div>`;
 const bar=$('.dlg-b',w.body);btns.forEach((t,i)=>{const b=el('button','btn'+(i===0?' def':''),esc(t));b.onclick=()=>{fin(i);closeWin(w,true)};bar.append(b)});
 if(o.icon==='error'||o.icon==='warn')sfx.ding();w.recenter();$('.btn',bar).focus();return w}
function inputDialog(o){
 let done=false;const w=createWindow({app:'dialog',title:o.title,icon:o.icon||'folder',w:380,h:0,minable:false,maxable:false,resizable:false,task:false,parent:o.parent});
 w.body.innerHTML=`<div class="dlg"><div class="dlg-t" style="display:block;min-height:0"><div>${esc(o.label)}</div><input type="text"></div><div class="dlg-b"><button class="btn def">ОК</button><button class="btn">Отмена</button></div></div>`;
 const inp=$('input',w.body),[ok,cn]=$$('.btn',w.body);inp.value=o.value||'';
 const go=()=>{if(done)return;done=true;closeWin(w,true);o.cb(inp.value)};ok.onclick=go;cn.onclick=()=>closeWin(w,true);
 inp.onkeydown=e=>{if(e.key==='Enter')go();e.stopPropagation()};w.recenter();inp.focus();inp.select();return w}
/* ================= apps registry ================= */
const APPS={
 explorer:{name:'Проводник',icon:'folder',fn:a=>appExplorer(a)},
 ie:{name:'Internet Explorer',icon:'ie',fn:()=>appIE()},
 notepad:{name:'Блокнот',icon:'notepad',fn:a=>appNotepad(a)},
 calc:{name:'Калькулятор',icon:'calc',fn:()=>appCalc()},
 paint:{name:'Paint',icon:'paint',fn:()=>appPaint()},
 mine:{name:'Сапёр',icon:'mine',fn:()=>appMine()},
 cmd:{name:'Командная строка',icon:'cmd',fn:()=>appCmd()},
 wmp:{name:'Проигрыватель Windows Media',icon:'wmp',fn:a=>appWmp(a)},
 taskmgr:{name:'Диспетчер задач',icon:'taskmgr',single:1,fn:()=>appTask()},
 control:{name:'Панель управления',icon:'control',single:1,fn:()=>appControl()},
 personalize:{name:'Персонализация',icon:'control',single:1,fn:()=>appPersonalize()},
 sysinfo:{name:'Система',icon:'computer',single:1,fn:()=>appSysinfo()},
 viewer:{name:'Просмотр фотографий Windows',icon:'img',fn:a=>appViewer(a)}
};
function launch(id,arg){const a=APPS[id];if(!a)return;hideStart();closeMenus();if(a.single){const w=wins.find(w=>w.app===id);if(w){focusWin(w);return w}}return a.fn(arg)}
/* ================= taskbar ================= */
const PINNED=['ie','explorer','notepad','calc','paint'];let thumbTimer=null;
function renderTasks(){
 const box=$('#tasks');box.innerHTML='';const order=[...PINNED];wins.filter(w=>w.o.task!==false).forEach(w=>{if(!order.includes(w.app))order.push(w.app)});
 order.forEach(app=>{
  const ws=wins.filter(w=>w.app===app&&w.o.task!==false),a=APPS[app];if(!a)return;
  const b=el('div','tbtn'+(ws.length?' run':'')+(ws.length>1?' multi':'')+(ws.some(w=>w===activeWin&&!w.min)?' act':''),ic(a.icon,32));
  b.onclick=()=>{hideThumbs();closeMenus();hideStart();hidePops();if(!ws.length)launch(app);else if(ws.length===1){const w=ws[0];if(w===activeWin&&!w.min)minWin(w);else focusWin(w)}else showThumbs(b,ws)};
  b.onmouseenter=()=>{if(ws.length)showThumbs(b,ws)};b.onmouseleave=()=>{thumbTimer=setTimeout(hideThumbs,250)};
  b.oncontextmenu=e=>{e.preventDefault();showMenu(e.clientX,e.clientY-90,[{t:a.name,ico:a.icon,def:1,fn:()=>{if(app==='explorer'||!a.single)launch(app);else launch(app)}},'-',{t:PINNED.includes(app)?'Закрепить программу в панели задач':'Закрепить',dis:true},{t:'Закрыть окно',ico:'error',dis:!ws.length,fn:()=>ws.forEach(w=>closeWin(w))}])};
  box.append(b)})}
function showThumbs(b,ws){clearTimeout(thumbTimer);const t=$('#thumbs');t.innerHTML='';t.style.display='flex';
 ws.forEach(w=>{const c=el('div','th',`<div class="th-h">${ic(w.icon,16)}<span>${esc(w.title)}</span><div class="th-x">✕</div></div><div class="th-p">${ic(w.icon,48)}</div>`);
  c.onclick=e=>{if(e.target.closest('.th-x')){closeWin(w);hideThumbs();return}hideThumbs();focusWin(w)};t.append(c)});
 const r=b.getBoundingClientRect(),tw=t.offsetWidth;t.style.left=Math.max(4,Math.min(innerWidth-tw-4,r.left+r.width/2-tw/2))+'px';
 t.onmouseenter=()=>clearTimeout(thumbTimer);t.onmouseleave=()=>{thumbTimer=setTimeout(hideThumbs,250)}}
function hideThumbs(){$('#thumbs').style.display='none'}
let hidden=[];
$('#showdesk').onclick=()=>{const vis=wins.filter(w=>!w.min);if(vis.length){hidden=vis;vis.forEach(w=>minWin(w))}else{hidden.forEach(w=>{if(wins.includes(w))w.min=false,w.el.classList.remove('min')});hidden.forEach(w=>wins.includes(w))&&0;const l=hidden.filter(w=>wins.includes(w));if(l.length)focusWin(l[l.length-1]);hidden=[]}};
/* tray */
$('#tr-net').innerHTML='▂▅<span style="color:#f66;font-weight:bold;font-size:19px">×</span>';$('#tr-net').title='Нет подключения к сети';$('#netpop').innerHTML='<b>Нет подключения к сети</b><br>Внешнее подключение отсутствует.';
/* network indicator is now offline */
const volIcon=()=>`<svg width="18" height="16" viewBox="0 0 18 16"><path d="M1 5h3l4-3v12l-4-3H1z" fill="#fff"/>${cfg.vol>0?'<path d="M11 5c2 2 2 4 0 6M13 3c3 3 3 7 0 10" stroke="#fff" stroke-width="1.4" fill="none"/>':'<path d="M11 5l5 6M16 5l-5 6" stroke="#f66" stroke-width="1.6"/>'}</svg>`;
function updVol(){$('#tr-vol').innerHTML=volIcon();$('#volv').textContent=cfg.vol;$('#volr').value=cfg.vol}
$('#volr').disabled=true;$('#volr').oninput=e=>{};
function hidePops(){$$('.pop').forEach(p=>p.classList.remove('open'))}
function togglePop(id){const p=$('#'+id),was=p.classList.contains('open');hidePops();if(was)return;if(id==='clockpop')buildCal();p.classList.add('open')}
$$('[data-pop]').forEach(t=>t.onclick=()=>{hideStart();closeMenus();togglePop(t.dataset.pop)});
$('#tr-flag').onclick=()=>msgBox({title:'Центр поддержки',icon:'shield',text:'Проблем не обнаружено. Брандмауэр Windows и защита от вирусов включены.'});
$('#lang').onclick=function(){this.textContent=this.textContent==='РУС'?'ENG':'РУС'};
const clocks=[];
function makeClock(sz){
 let t='';for(let i=0;i<60;i++){const a=i*6*Math.PI/180,r1=i%5?52:48,r2=54;t+=`<line x1="${60+Math.sin(a)*r1}" y1="${60-Math.cos(a)*r1}" x2="${60+Math.sin(a)*r2}" y2="${60-Math.cos(a)*r2}" stroke="#345" stroke-width="${i%5?.6:1.8}"/>`}
 const d=el('div','',`<svg width="${sz}" height="${sz}" viewBox="0 0 120 120"><circle cx="60" cy="60" r="58" fill="#2a64ad"/><circle cx="60" cy="60" r="55" fill="url(#ckf)" stroke="#fff" stroke-width="1"/>${t}<line class="hh" x1="60" y1="60" x2="60" y2="36" stroke="#123" stroke-width="4.5" stroke-linecap="round"/><line class="mh" x1="60" y1="60" x2="60" y2="20" stroke="#123" stroke-width="3" stroke-linecap="round"/><line class="sh" x1="60" y1="68" x2="60" y2="14" stroke="#c22" stroke-width="1.4"/><circle cx="60" cy="60" r="3.5" fill="#c22"/></svg>`);
 const c={el:d,update(){const s=0,m=Number(arch.time.slice(3)),h=Number(arch.time.slice(0,2))%12+m/60;$('.hh',d).setAttribute('transform',`rotate(${h*30} 60 60)`);$('.mh',d).setAttribute('transform',`rotate(${m*6} 60 60)`);$('.sh',d).setAttribute('transform',`rotate(${s*6} 60 60)`)}};clocks.push(c);c.update();return c}
function tick(){const n=new Date();$('#ck-t').textContent=arch.time;$('#ck-d').textContent=`${pad(n.getDate())}.${pad(n.getMonth()+1)}.${n.getFullYear()}`;$('#clock').title=`${DAYS[n.getDay()]}, ${n.getDate()} ${MONTHS[n.getMonth()]} ${n.getFullYear()} г.`;clocks.forEach(c=>{if(c.el.isConnected)c.update()})}
let calY,calM;
function buildCal(y,m){const n=new Date();if(y==null){y=n.getFullYear();m=n.getMonth()}calY=y;calM=m;const p=$('#clockpop');
 p.innerHTML=`<div style="display:flex;gap:14px"><div style="flex:1"><div style="color:#1e3f7a;margin-bottom:6px">${DAYS[n.getDay()]}, ${n.getDate()} ${MONTHS[n.getMonth()]} ${n.getFullYear()} г.</div><div style="display:flex;justify-content:space-between;align-items:center;padding:3px 4px;background:linear-gradient(#e9f2fb,#d3e3f5);border:1px solid #b6c9e0;margin-bottom:4px"><span class="cprev" style="padding:0 8px">◀</span><b>${MONTHS_N[m]} ${y}</b><span class="cnext" style="padding:0 8px">▶</span></div><div class="cal"></div></div><div class="ckh" style="padding-top:20px"></div></div><div class="cplink" style="margin-top:8px;border-top:1px solid #ccd;padding-top:6px;color:#1a56a8">Изменение настроек даты и времени...</div>`;
 const g=$('.cal',p);['Пн','Вт','Ср','Чт','Пт','Сб','Вс'].forEach(d=>g.append(el('div','dh',d)));
 const first=(new Date(y,m,1).getDay()+6)%7,dim=new Date(y,m+1,0).getDate(),prevD=new Date(y,m,0).getDate();
 for(let i=0;i<42;i++){const dn=i-first+1;let t,c='';if(dn<1){t=prevD+dn;c='dim'}else if(dn>dim){t=dn-dim;c='dim'}else{t=dn;if(dn===n.getDate()&&m===n.getMonth()&&y===n.getFullYear())c='td'}g.append(el('div',c,t))}
 $('.cprev',p).onclick=()=>buildCal(m?y:y-1,m?m-1:11);$('.cnext',p).onclick=()=>buildCal(m<11?y:y+1,m<11?m+1:0);$('.ckh',p).append(makeClock(110).el);
 $('.cplink',p).onclick=()=>{hidePops();launch('control')}}
function balloon(title,text,ms){const b=$('#balloon');b.innerHTML=`<div style="display:flex;gap:8px;align-items:center;margin-bottom:4px"><b>${esc(title)}</b></div><div>${esc(text)}</div>`;b.style.display='block';b.onclick=()=>b.style.display='none';setTimeout(()=>b.style.display='none',ms||7000)}
/* ================= start menu ================= */
const START_PROGS=['ie','notepad','calc','paint','mine','cmd','wmp','taskmgr'];
let allMode=false;
function buildStart(){
 const s=$('#start');
 s.innerHTML=`<div class="sm-l"><div class="sm-list"></div><div class="sm-all">Все программы ▸</div><div class="sm-search"><input type="text" placeholder="Найти программы и файлы"></div></div>
 <div class="sm-r"><div class="sm-user"><div class="sm-av">${USERPIC}</div>User</div><div class="ri" data-p="docs">${ic('folder',22)}Документы</div><div class="ri" data-p="pics">${ic('img',22)}Изображения</div><div class="ri" data-p="mus">${ic('music',22)}Музыка</div><div class="ri" data-p="dl">${ic('folder',22)}Загрузки</div><div class="ri" data-p="comp">${ic('computer',22)}Компьютер</div><div class="ri" data-p="ctl">${ic('control',22)}Панель управления</div><div class="ri" data-p="dev">${ic('drive',22)}Устройства и принтеры</div><div class="ri" data-p="help">${ic('question',22)}Справка и поддержка</div>
 <div class="sm-sd"><div class="sd-main">Завершение работы</div><div class="sd-arr">▶</div></div></div>`;
 const list=$('.sm-list',s),inp=$('input',s),all=$('.sm-all',s);
 const item=(icon,name,fn)=>{const d=el('div','sm-i',`${ic(icon,32)}<span class="nm">${esc(name)}</span>`);d.onclick=fn;return d};
 function fill(){list.innerHTML='';const q=inp.value.trim().toLowerCase();
  if(q){let c=0;Object.entries(APPS).forEach(([k,a])=>{if(a.name.toLowerCase().includes(q)){list.append(item(a.icon,a.name,()=>launch(k)));c++}});
   walk(COMP,[],(name,n,path)=>{if(c<14&&n.type==='file'&&name.toLowerCase().includes(q)){list.append(item(n.kind==='txt'?'doc':n.kind==='img'?'img':n.kind==='audio'?'music':'doc',name,()=>{hideStart();openNode(n,path,name)}));c++}});
   if(!c)list.append(el('div','',`<div style="padding:14px;color:#555">Совпадений не найдено.</div>`));all.style.display='none';return}
  all.style.display='';all.textContent=allMode?'◀ Назад':'Все программы ▸';
  if(allMode){Object.entries(APPS).forEach(([k,a])=>list.append(item(a.icon,a.name,()=>launch(k))))}
  else{START_PROGS.forEach((k,i)=>{list.append(item(APPS[k].icon,APPS[k].name,()=>launch(k)));if(i===1)list.append(el('div','sm-sep'))})}}
 all.onclick=()=>{allMode=!allMode;fill()};inp.oninput=fill;inp.onkeydown=e=>e.stopPropagation();s._fill=fill;fill();
 const links={docs:()=>launch('explorer',P_DOCS),pics:()=>launch('explorer',P_PICS),mus:()=>launch('explorer',P_MUS),dl:()=>launch('explorer',P_DL),comp:()=>launch('explorer',[]),ctl:()=>launch('control'),dev:()=>msgBox({title:'Устройства и принтеры',icon:'info',text:'Это приложение недоступно в симуляторе.'}),help:()=>msgBox({title:'Справка и поддержка Windows',icon:'question',text:'Двойной щелчок по значку открывает его. Правая кнопка мыши вызывает контекстное меню. Окна можно прижимать к краям экрана.'})};
 $$('.ri',s).forEach(r=>r.onclick=()=>{hideStart();links[r.dataset.p]()});
 $('.sd-main',s).onclick=()=>{hideStart()};
 $('.sd-arr',s).onclick=e=>{e.stopPropagation();const r=e.currentTarget.getBoundingClientRect();showMenu(r.right+2,r.top-170,[{t:'Сменить пользователя',fn:()=>power('lock')},{t:'Выйти из системы',fn:()=>power('logoff')},{t:'Блокировать',fn:()=>power('lock')},{t:'Перезагрузка',fn:()=>power('restart')},{t:'Сон',fn:()=>power('sleep')}])}}
function toggleStart(){const s=$('#start');if(s.classList.contains('open'))hideStart();else{hidePops();closeMenus();allMode=false;const i=$('input',s);i.value='';s._fill();s.classList.add('open');$('#orb').classList.add('on');setTimeout(()=>i.focus(),20)}}
function hideStart(){$('#start').classList.remove('open');$('#orb').classList.remove('on')}
$('#orb').innerHTML=LOGO;$('#orb').onclick=toggleStart;
/* ================= desktop icons ================= */
const SYS=[
 {k:'s:comp',name:'Компьютер',icon:()=>'computer',open:()=>launch('explorer',[]),sys:1},
 {k:'s:trash',name:'Корзина',icon:()=>Object.keys(TRASH.children).length?'trashfull':'trash',open:()=>launch('explorer',['::trash']),sys:1,trash:1},
 {k:'s:ie',name:'Internet Explorer',icon:()=>'ie',open:()=>launch('ie'),sys:1},
 {k:'s:notepad',name:'Блокнот',icon:()=>'notepad',open:()=>launch('notepad'),sys:1},
 {k:'s:calc',name:'Калькулятор',icon:()=>'calc',open:()=>launch('calc'),sys:1},
 {k:'s:paint',name:'Paint',icon:()=>'paint',open:()=>launch('paint'),sys:1},
 {k:'s:mine',name:'Сапёр',icon:()=>'mine',open:()=>launch('mine'),sys:1},
 {k:'s:cmd',name:'Командная строка',icon:()=>'cmd',open:()=>launch('cmd'),sys:1},
 {k:'s:control',name:'Панель управления',icon:()=>'control',open:()=>launch('control'),sys:1}
];
const CW=86,CH=94,PD=6;let iconPos=store.get('w7pos',{}),selKeys=new Set(),dItems=[];
const gridRows=()=>Math.max(1,Math.floor((innerHeight-40-PD)/CH));
function renderDesktop(){
 const box=$('#icons');box.innerHTML='';const dn=resolve(P_DESK);
 dItems=[...SYS.map(s=>({...s})),...Object.entries(dn?dn.children:{}).filter(([name,n])=>!n.hidden||arch.showHidden).map(([name,n])=>({k:'f:'+name,name,node:n,icon:()=>null}))];
 const rows=gridRows(),used=new Set();
 dItems.forEach(it=>{const p=iconPos[it.k];if(p&&p.r<rows){used.add(p.c+','+p.r);it.p=p}});
 let ci=0;dItems.forEach(it=>{if(it.p)return;let c,r;do{c=Math.floor(ci/rows);r=ci%rows;ci++}while(used.has(c+','+r));used.add(c+','+r);it.p={c,r}});
 dItems.forEach(it=>{
  const d=el('div','di'+(selKeys.has(it.k)?' sel':''),`<div class="dp">${it.node?nodeIcon(it.node,48):ic(it.icon(),48)}</div><div class="dl">${esc(it.name)}</div>`);
  d.dataset.k=it.k;d.style.left=(PD+it.p.c*CW)+'px';d.style.top=(PD+it.p.r*CH)+'px';it.el=d;box.append(d)})}
function itemByKey(k){return dItems.find(i=>i.k===k)}
function setSel(keys){selKeys=new Set(keys);dItems.forEach(i=>i.el.classList.toggle('sel',selKeys.has(i.k)))}
function openDI(it){if(it.sys)it.open();else openNode(it.node,P_DESK,it.name)}
function diMenu(it,x,y){
 if(!selKeys.has(it.k))setSel([it.k]);
 const sel=dItems.filter(i=>selKeys.has(i.k)),fs=sel.filter(i=>!i.sys);
 const items=[{t:'Открыть',def:1,fn:()=>openDI(it)},'-'];
 if(it.trash)items.push({t:'Очистить корзину',dis:!Object.keys(TRASH.children).length,fn:()=>emptyTrash()},'-');
 if(fs.length)items.push({t:'Удалить',fn:()=>deleteNodes(P_DESK,fs.map(i=>i.name))},{t:'Переименовать',dis:fs.length!==1,fn:()=>renameFlow(P_DESK,it.name)},'-');
 items.push({t:'Свойства',fn:()=>it.sys?msgBox({title:'Свойства: '+it.name,icon:it.icon(),html:`<b>${esc(it.name)}</b><br><br>Тип: Ярлык<br>Расположение: Рабочий стол`}):propsBox(P_DESK,it.name)});
 showMenu(x,y,items)}
function emptyTrash(){msgBox({title:'Удаление нескольких объектов',icon:'question',text:'Вы действительно хотите безвозвратно удалить все объекты из корзины?',buttons:['Да','Нет'],cb:i=>{if(i===0){TRASH.children={};fsChanged()}}})}
(function setupDesktop(){
 const box=$('#icons'),band=$('#band');
 box.addEventListener('dblclick',e=>{const d=e.target.closest('.di');if(d){const it=itemByKey(d.dataset.k);if(it)openDI(it)}});
 box.addEventListener('contextmenu',e=>{e.preventDefault();const d=e.target.closest('.di');if(d)return diMenu(itemByKey(d.dataset.k),e.clientX,e.clientY);setSel([]);
  showMenu(e.clientX,e.clientY,[{t:'Упорядочить значки',fn:()=>{iconPos={};store.set('w7pos',{});renderDesktop()}},{t:'Обновить',fn:()=>renderDesktop()},'-',{t:'Создать',sub:[{t:'Папку',ico:'folder',fn:()=>{const n=newItem(P_DESK,'dir');if(n)renameFlow(P_DESK,n)}},{t:'Текстовый документ',ico:'doc',fn:()=>{const n=newItem(P_DESK,'txt');if(n)renameFlow(P_DESK,n)}}]},'-',{t:'Разрешение экрана',fn:()=>screenInfo()},{t:'Персонализация',ico:'control',fn:()=>launch('personalize')}])});
 box.addEventListener('pointerdown',e=>{
  if(e.button!==0)return;const d=e.target.closest('.di');
  if(!d){ // rubber band
   const sx=e.clientX,sy=e.clientY,base=e.ctrlKey?new Set(selKeys):new Set();if(!e.ctrlKey)setSel([]);let on=false;
   const mv=ev=>{const x1=Math.min(sx,ev.clientX),y1=Math.min(sy,ev.clientY),x2=Math.max(sx,ev.clientX),y2=Math.max(sy,ev.clientY);if(!on&&(x2-x1<3&&y2-y1<3))return;on=true;
    band.style.display='block';band.style.left=x1+'px';band.style.top=y1+'px';band.style.width=(x2-x1)+'px';band.style.height=(y2-y1)+'px';
    const keys=new Set(base);dItems.forEach(it=>{const r=it.el.getBoundingClientRect();if(r.right>x1&&r.left<x2&&r.bottom>y1&&r.top<y2)keys.add(it.k)});setSel(keys)};
   const up=()=>{removeEventListener('pointermove',mv);removeEventListener('pointerup',up);band.style.display='none'};addEventListener('pointermove',mv);addEventListener('pointerup',up);return}
  const it=itemByKey(d.dataset.k);
  if(e.ctrlKey){const s=new Set(selKeys);s.has(it.k)?s.delete(it.k):s.add(it.k);setSel(s);return}
  if(!selKeys.has(it.k))setSel([it.k]);
  const sx=e.clientX,sy=e.clientY;let moved=false;const mv=ev=>{const dx=ev.clientX-sx,dy=ev.clientY-sy;if(!moved&&Math.hypot(dx,dy)<5)return;moved=true;dItems.filter(i=>selKeys.has(i.k)).forEach(i=>{i.el.classList.add('moving');i.el.style.transform=`translate(${dx}px,${dy}px)`})};
  const up=ev=>{removeEventListener('pointermove',mv);removeEventListener('pointerup',up);
   if(!moved){setSel([it.k]);return}
   const dc=Math.round((ev.clientX-sx)/CW),dr=Math.round((ev.clientY-sy)/CH),rows=gridRows(),cols=Math.floor(innerWidth/CW),mv2=dItems.filter(i=>selKeys.has(i.k));
   const occ=new Set(dItems.filter(i=>!selKeys.has(i.k)).map(i=>i.p.c+','+i.p.r)),tgt=mv2.map(i=>({i,c:i.p.c+dc,r:i.p.r+dr}));
   const ok=tgt.every(t=>t.c>=0&&t.r>=0&&t.r<rows&&t.c<cols&&!occ.has(t.c+','+t.r));
   if(ok){tgt.forEach(t=>iconPos[t.i.k]={c:t.c,r:t.r});dItems.forEach(i=>{if(!iconPos[i.k])iconPos[i.k]={...i.p}});store.set('w7pos',iconPos)}
   renderDesktop()};
  addEventListener('pointermove',mv);addEventListener('pointerup',up)});
 // gadget
 const g=makeClock(140);$('#gadget').append(g.el);
 $('#gadget').addEventListener('contextmenu',e=>{e.preventDefault();e.stopPropagation();showMenu(e.clientX,e.clientY,[{t:'Закрыть гаджет',fn:()=>$('#gadget').style.display='none'}])})
})();
function screenInfo(){msgBox({title:'Разрешение экрана',icon:'computer',html:`<b>Экран: Универсальный монитор</b><br><br>Разрешение: ${innerWidth} × ${innerHeight}<br>Глубина цвета: True Color (32 бита)<br>Частота обновления: 60 Гц`})}
/* ================= EXPLORER ================= */
function appExplorer(startPath){
 const st={path:(startPath||[]).slice(),hist:[],hi:-1,sel:new Set(),view:'icons',filter:''};
 const win=createWindow({app:'explorer',title:'Проводник',icon:'folder',w:860,h:540,onClose:()=>explorers.delete(api)});
 win.body.innerHTML=`<div class="ex-nav"><div class="ex-btns"><button class="ex-b back" disabled>◀</button><button class="ex-b fwd" disabled>▶</button></div><div class="ex-addr"></div><div class="ex-search"><input type="text" placeholder="Поиск"></div></div><div class="ex-cmd"></div><div class="ex-main"><div class="ex-side"></div><div class="ex-list" tabindex="0"></div></div><div class="ex-stat"></div>`;
 const $b=s=>$(s,win.body),list=$b('.ex-list');
 const name=p=>p[0]==='::trash'?'Корзина':p.length?p[p.length-1]:'Компьютер';
 function go(p,push=true){st.path=p.slice();if(push){st.hist=st.hist.slice(0,st.hi+1);st.hist.push(p.slice());st.hi++}st.sel=new Set();st.filter='';$b('.ex-search input').value='';render()}
 const isTrash=()=>st.path[0]==='::trash',isComp=()=>!st.path.length;
 const sideLinks=[['Избранное',[['Рабочий стол',P_DESK,'folder'],['Загрузки',P_DL,'folder']]],['Библиотеки',[['Документы',P_DOCS,'folder'],['Изображения',P_PICS,'img'],['Музыка',P_MUS,'music']]],['Компьютер',[['Компьютер',[],'computer'],['Локальный диск (C:)',['Локальный диск (C:)'],'drive'],['Дисковод (F:)',['Дисковод (F:)'],'dvd']]],['Корзина',[['Корзина',['::trash'],'trash']]]];
 function render(keepList){
  let node=resolve(st.path);if(!node){st.path=[];node=COMP}
  win.setTitle(name(st.path)+' — Проводник');
  $b('.back').disabled=st.hi<=0;$b('.fwd').disabled=st.hi>=st.hist.length-1;
  // address
  const ad=$b('.ex-addr');ad.innerHTML=`${ic(isTrash()?'trash':isComp()?'computer':'folder',16)}&nbsp;`;
  const segs=isTrash()?[['Корзина',['::trash']]]:[['Компьютер',[]],...st.path.map((p,i)=>[p,st.path.slice(0,i+1)])];
  segs.forEach((s,i)=>{if(i)ad.append(el('span','',' ▸ '));const sp=el('span','seg',esc(s[0]));sp.onclick=()=>go(s[1]);ad.append(sp)});
  // cmd
  const cm=$b('.ex-cmd');cm.innerHTML='';
  const cbtn=(t,fn,dis)=>{const b=el('button','cb',t);b.disabled=!!dis;b.onclick=fn;cm.append(b)};
  const sel=[...st.sel].filter(n=>node.children[n]);
  if(isTrash()){cbtn('Очистить корзину',emptyTrash,!Object.keys(TRASH.children).length);cbtn(sel.length?'Восстановить выделенные объекты':'Восстановить все объекты',()=>{(sel.length?sel:Object.keys(TRASH.children)).forEach(fsRestore);fsChanged()},!Object.keys(TRASH.children).length)}
  else if(isComp()){cbtn('Свойства системы',()=>launch('sysinfo'));cbtn('Панель управления',()=>launch('control'))}
  else{cbtn(arch.showHidden?'Скрыть скрытые файлы':'Показать скрытые файлы',()=>{arch.showHidden=!arch.showHidden;fsChanged()});cbtn('Упорядочить ▾',e=>{const r=e.currentTarget.getBoundingClientRect();showMenu(r.left,r.bottom,[{t:'Обновить',fn:render},{t:'Выделить все',fn:()=>{st.sel=new Set(Object.keys(node.children));render()}}])});
   cbtn('Открыть',()=>sel.length&&openItem(sel[0]),!sel.length);cbtn('Новая папка',()=>{const n=newItem(st.path,'dir');if(n)renameFlow(st.path,n)},st.path.length<1);
   cbtn('Вид ▾',e=>{const r=e.currentTarget.getBoundingClientRect();showMenu(r.left,r.bottom,[{t:'Крупные значки',chk:st.view==='icons',fn:()=>{st.view='icons';render()}},{t:'Таблица',chk:st.view==='det',fn:()=>{st.view='det';render()}}])})}
  // side
  const sd=$b('.ex-side');sd.innerHTML='';
  sideLinks.forEach(([h,ls])=>{if(h==='Избранное'||h==='Библиотеки')sd.append(el('div','sd-h',h));
   ls.forEach(([t,p,i])=>{const d=el('div','sd-i'+(JSON.stringify(p)===JSON.stringify(st.path)?' cur':''),`${ic(i,16)}${esc(t)}`);d.onclick=()=>go(p);sd.append(d)})});
  // list
  let ents=Object.entries(node.children).filter(([n,v])=>(!v.hidden||arch.showHidden)&&n.toLowerCase().includes(st.filter.toLowerCase())).sort((a,b)=>(b[1].type==='dir')-(a[1].type==='dir')||a[0].localeCompare(b[0],'ru'));
  list.className='ex-list'+(st.view==='det'&&!isComp()?' det':'');
  if(keepList)$$('[data-n]',list).forEach(x=>x.classList.toggle('sel',st.sel.has(x.dataset.n)));
  else if(!ents.length)list.innerHTML=`<div style="width:100%;text-align:center;color:#777;padding:40px 0">${st.filter?'Совпадений не найдено.':'Эта папка пуста.'}</div>`;
  else if(st.view==='det'&&!isComp()){list.innerHTML=`<table><tr><th style="width:42%">Имя</th><th>Дата изменения</th><th>Тип</th><th>Размер</th></tr>${ents.map(([n,v])=>`<tr class="${st.sel.has(n)?'sel':''}" data-n="${esc(n)}"><td><div class="nm">${nodeIcon(v,16)}${esc(n)}</div></td><td>${new Date().toLocaleDateString('ru')}</td><td>${kindLabel(v)}</td><td>${sizeOf(v)}</td></tr>`).join('')}</table>`}
  else list.innerHTML=ents.map(([n,v])=>{
   if(v.drive){const used=v.drive==='dvd'?0:62;return `<div class="exi drive ${st.sel.has(n)?'sel':''}" data-n="${esc(n)}">${nodeIcon(v,48)}<div><div>${esc(n)}</div>${v.drive==='dvd'?'<div style="color:#777;margin-top:4px">Нет диска</div>':`<div class="dbar"><i style="width:${used}%"></i></div><div style="color:#777">${(238*(100-used)/100).toFixed(1).replace('.',',')} ГБ свободно из 238 ГБ</div>`}</div></div>`}
   const th=v.kind==='img'?`<div class="thumb" style="background-image:url('${esc(v.src)}')"></div>`:nodeIcon(v,48);
   return `<div class="exi ${st.sel.has(n)?'sel':''}" data-n="${esc(n)}">${th}<span>${esc(n)}</span></div>`}).join('');
  $b('.ex-stat').textContent=sel.length?`Выбрано элементов: ${sel.length}`:`Элементов: ${ents.length}`}
 function openItem(n){const node=resolve(st.path),v=node.children[n];if(!v)return;if(v.type==='dir'&&!isTrash())go([...st.path,n]);else openNode(v,st.path,n)}
 list.addEventListener('pointerdown',e=>{list.focus();const it=e.target.closest('[data-n]');if(!it){if(e.button===0){st.sel=new Set();render(true)}return}
  const n=it.dataset.n;if(e.ctrlKey&&e.button===0){st.sel.has(n)?st.sel.delete(n):st.sel.add(n)}else if(!st.sel.has(n)||e.button===0)st.sel=new Set([n]);render(true)});
 list.addEventListener('dblclick',e=>{const it=e.target.closest('[data-n]');if(it)openItem(it.dataset.n)});
 list.addEventListener('contextmenu',e=>{e.preventDefault();const it=e.target.closest('[data-n]');const node=resolve(st.path);
  if(it){const n=it.dataset.n;if(!st.sel.has(n)){st.sel=new Set([n]);render(true)}const sel=[...st.sel];
   const items=isTrash()?[{t:'Восстановить',def:1,fn:()=>{sel.forEach(fsRestore);fsChanged()}},'-',{t:'Удалить',fn:()=>deleteNodes(st.path,sel)}]:[{t:'Открыть',def:1,fn:()=>openItem(n)},'-',{t:'Удалить',fn:()=>deleteNodes(st.path,sel)},{t:'Переименовать',dis:sel.length>1,fn:()=>renameFlow(st.path,n)},'-',{t:'Свойства',fn:()=>propsBox(st.path,n)}];
   showMenu(e.clientX,e.clientY,items)}
  else{st.sel=new Set();render(true);const it2=[{t:'Вид',sub:[{t:'Крупные значки',chk:st.view==='icons',fn:()=>{st.view='icons';render()}},{t:'Таблица',chk:st.view==='det',fn:()=>{st.view='det';render()}}]},{t:'Обновить',fn:render}];
   if(isTrash())it2.push('-',{t:'Очистить корзину',fn:emptyTrash});else if(st.path.length)it2.push('-',{t:'Создать',sub:[{t:'Папку',ico:'folder',fn:()=>{const n=newItem(st.path,'dir');if(n)renameFlow(st.path,n)}},{t:'Текстовый документ',ico:'doc',fn:()=>{const n=newItem(st.path,'txt');if(n)renameFlow(st.path,n)}}]});
   showMenu(e.clientX,e.clientY,it2)}});
 list.addEventListener('keydown',e=>{const sel=[...st.sel];
  if(e.key==='Delete'&&sel.length&&st.path.length)deleteNodes(st.path,sel);else if(e.key==='F2'&&sel.length===1)renameFlow(st.path,sel[0]);else if(e.key==='Enter'&&sel.length)openItem(sel[0]);
  else if(e.key==='Backspace'&&st.path.length&&!isTrash())go(st.path.slice(0,-1));else if(e.key==='F5')render();else if(e.ctrlKey&&e.key==='a'){e.preventDefault();st.sel=new Set(Object.keys(resolve(st.path).children));render()}});
 $b('.back').onclick=()=>{if(st.hi>0){st.hi--;go(st.hist[st.hi],false)}};$b('.fwd').onclick=()=>{if(st.hi<st.hist.length-1){st.hi++;go(st.hist[st.hi],false)}};
 $b('.ex-search input').oninput=e=>{st.filter=e.target.value;render()};$b('.ex-search input').onkeydown=e=>e.stopPropagation();
 const api={refresh:render};explorers.add(api);go(st.path);return win}
/* ================= NOTEPAD ================= */
function pickTextFile(cb){
 const files=[];walk(COMP,[],(n,v,p)=>{if(v.type==='file'&&v.kind==='txt')files.push({n,p})});
 if(!files.length){msgBox({title:'Открыть',icon:'info',text:'Текстовых файлов не найдено.'});return}
 const w=createWindow({app:'dialog',title:'Открыть',icon:'folder',w:400,h:0,minable:false,maxable:false,resizable:false,task:false,parent:activeWin&&activeWin.app==='notepad'?activeWin:null});
 w.body.innerHTML=`<div class="dlg"><div class="dlg-t" style="display:block;min-height:0">Выберите файл:<select style="width:100%;margin-top:6px;padding:3px">${files.map((f,i)=>`<option value="${i}">C:\\${esc(f.p.slice(1).join('\\'))}\\${esc(f.n)}</option>`).join('')}</select></div><div class="dlg-b"><button class="btn def">Открыть</button><button class="btn">Отмена</button></div></div>`;
 const[ok,cn]=$$('.btn',w.body);ok.onclick=()=>{const f=files[$('select',w.body).value];closeWin(w,true);cb(f)};cn.onclick=()=>closeWin(w,true);w.recenter()}
function appNotepad(arg){
 let file=null,modified=false;
 const win=createWindow({app:'notepad',title:'Безымянный — Блокнот',icon:'notepad',w:640,h:430,beforeClose:done=>{
  if(!modified)return done();
  msgBox({title:'Блокнот',icon:'warn',text:`Сохранить изменения в файле ${file?file.name:'Безымянный'}?`,buttons:['Сохранить','Не сохранять','Отмена'],parent:win,cb:i=>{if(i===0)save(false,done);else if(i===1)done()}})}});
 const ta=el('textarea','np');ta.spellcheck=false;
 const upTitle=()=>win.setTitle((modified?'*':'')+(file?file.name:'Безымянный')+' — Блокнот');
 function load(path,name){const d=resolve(path);if(!d||!d.children[name])return;file={dir:d,name};ta.value=d.children[name].content||'';modified=false;upTitle()}
 function save(as,after){
  const text=ta.value;
  if(file&&!as&&file.dir.children[file.name]){file.dir.children[file.name].content=text;modified=false;upTitle();fsChanged();if(after)after();return}
  inputDialog({title:'Сохранить как',label:'Имя файла (папка «Документы»):',value:file?file.name:'Безымянный.txt',icon:'notepad',parent:win,cb:v=>{let n=v.trim();if(!n)return;if(!/\.[a-z0-9]+$/i.test(n))n+='.txt';if(/[\\\/:*?"<>|]/.test(n)){msgBox({icon:'error',title:'Сохранение',text:'Недопустимое имя файла.'});return}
   const docs=resolve(P_DOCS);docs.children[n]=mkt(text);file={dir:docs,name:n};modified=false;upTitle();fsChanged();if(after)after()}})}
 const newDoc=()=>{if(modified){msgBox({title:'Блокнот',icon:'warn',text:'Сохранить изменения?',buttons:['Сохранить','Не сохранять','Отмена'],parent:win,cb:i=>{if(i===0)save(false,reset);else if(i===1)reset()}})}else reset()};
 const reset=()=>{file=null;ta.value='';modified=false;upTitle()};
 let wrap=true;
 const mb=menubar([{t:'Файл',items:[{t:'Создать',key:'Ctrl+N',fn:newDoc},{t:'Открыть...',key:'Ctrl+O',fn:()=>pickTextFile(f=>load(f.p,f.n))},{t:'Сохранить',key:'Ctrl+S',fn:()=>save(false)},{t:'Сохранить как...',fn:()=>save(true)},'-',{t:'Выход',fn:()=>closeWin(win)}]},
  {t:'Правка',items:[{t:'Выделить все',key:'Ctrl+A',fn:()=>{ta.focus();ta.select()}},{t:'Время и дата',key:'F5',fn:()=>ins()}]},
  {t:'Формат',items:()=>[{t:'Перенос по словам',chk:wrap,fn:()=>{wrap=!wrap;ta.style.whiteSpace=wrap?'pre-wrap':'pre';ta.wrap=wrap?'soft':'off'}}]},
  {t:'Справка',items:[{t:'О программе',fn:()=>msgBox({title:'О программе «Блокнот»',icon:'notepad',parent:win,text:'Блокнот — Windows 7 (симулятор). Версия 6.1.'})}]}]);
 function ins(){const n=new Date(),s=`${n.getHours()}:${pad(n.getMinutes())} ${pad(n.getDate())}.${pad(n.getMonth()+1)}.${n.getFullYear()}`;const a=ta.selectionStart;ta.setRangeText(s,a,ta.selectionEnd,'end');modified=true;upTitle()}
 ta.oninput=()=>{if(!modified){modified=true;upTitle()}};
 ta.onkeydown=e=>{e.stopPropagation();if(e.ctrlKey&&e.key==='s'){e.preventDefault();save(false)}else if(e.key==='F5'){e.preventDefault();ins()}else if(e.ctrlKey&&e.key==='n'){e.preventDefault();newDoc()}else if(e.ctrlKey&&e.key==='o'){e.preventDefault();pickTextFile(f=>load(f.p,f.n))}};
 win.body.append(mb,ta);if(arg&&arg.name)load(arg.path,arg.name);setTimeout(()=>ta.focus(),50);return win}
/* ================= CALCULATOR ================= */
function appCalc(){
 const win=createWindow({app:'calc',title:'Калькулятор',icon:'calc',w:288,h:384,resizable:false,maxable:false});
 win.body.innerHTML=`<div class="menubar"></div><div class="calc"><div class="cd"><div class="h"></div><div class="mm"></div><div class="m">0</div></div><div class="ck-g"></div></div>`;
 $('.menubar',win.body).replaceWith(menubar([{t:'Вид',items:[{t:'Обычный',chk:true},{t:'Инженерный',dis:true},{t:'Программист',dis:true}]},{t:'Правка',items:[{t:'Копировать',key:'Ctrl+C',fn:()=>{try{navigator.clipboard.writeText(cur.replace('.',','))}catch(e){}}}]},{t:'Справка',items:[{t:'О программе',fn:()=>msgBox({title:'О программе «Калькулятор»',icon:'calc',parent:win,text:'Калькулятор Windows 7 (симулятор).'})}]}]));
 let cur='0',acc=null,op=null,fresh=true,hist='',mem=0,err=false;
 const disp=$('.m',win.body),hEl=$('.h',win.body),mm=$('.mm',win.body);
 const fmt=n=>{if(!isFinite(n)){return 'Ошибка'}let s=String(parseFloat(n.toPrecision(14)));if(s.includes('e')){s=n.toExponential(8)}return s};
 const show=()=>{disp.textContent=(err?cur:cur.replace('.',','));disp.style.fontSize=disp.textContent.length>14?'18px':disp.textContent.length>10?'22px':'28px';hEl.textContent=hist;mm.textContent=mem?'M':''};
 const calc=(a,b,o)=>o==='+'?a+b:o==='−'?a-b:o==='×'?a*b:b===0?NaN:a/b;
 const seterr=m=>{err=true;cur=m;acc=null;op=null;hist='';fresh=true;show()};
 function press(k){
  if(err&&k!=='C'&&k!=='CE')return;
  if(/^[0-9]$/.test(k)){if(fresh){cur=k;fresh=false}else if(cur.replace(/[-.]/g,'').length<16)cur=cur==='0'?k:cur+k}
  else if(k===','||k==='.'){if(fresh){cur='0.';fresh=false}else if(!cur.includes('.'))cur+='.'}
  else if(['+','−','×','÷'].includes(k)){const v=parseFloat(cur);if(op&&!fresh){const r=calc(acc,v,op);if(isNaN(r))return seterr('Деление на ноль невозможно');acc=r;cur=fmt(r)}else acc=v;op=k;hist=`${fmt(acc)} ${k}`;fresh=true}
  else if(k==='='){if(op){const r=calc(acc,parseFloat(cur),op);if(isNaN(r))return seterr(acc===0&&parseFloat(cur)===0?'Результат не определён':'Деление на ноль невозможно');cur=fmt(r);op=null;acc=null;hist='';fresh=true}}
  else if(k==='C'){cur='0';acc=null;op=null;hist='';fresh=true;err=false}
  else if(k==='CE'){cur='0';fresh=true;err=false}
  else if(k==='←'){if(!fresh){cur=cur.length>1&&!(cur.length===2&&cur[0]==='-')?cur.slice(0,-1):'0'}}
  else if(k==='±'){if(cur!=='0')cur=cur[0]==='-'?cur.slice(1):'-'+cur}
  else if(k==='√'){const v=parseFloat(cur);if(v<0)return seterr('Недопустимый ввод');cur=fmt(Math.sqrt(v));fresh=true}
  else if(k==='1/x'){const v=parseFloat(cur);if(v===0)return seterr('Деление на ноль невозможно');cur=fmt(1/v);fresh=true}
  else if(k==='%'){const v=parseFloat(cur);cur=fmt(acc!=null?acc*v/100:0);fresh=true}
  else if(k==='MC')mem=0;else if(k==='MR'){cur=fmt(mem);fresh=true}else if(k==='MS'){mem=parseFloat(cur);fresh=true}else if(k==='M+'){mem+=parseFloat(cur);fresh=true}else if(k==='M-'){mem-=parseFloat(cur);fresh=true}
  show()}
 const rows=['MC','MR','MS','M+','M-','←','CE','C','±','√','7','8','9','÷','%','4','5','6','×','1/x','1','2','3','−','=','0',',','+'];
 const g=$('.ck-g',win.body);
 rows.forEach(k=>{const b=el('button','cbt'+(/^[0-9,]$/.test(k)?' n':'')+(k==='='?' eq':''),k);if(k==='0')b.style.gridColumn='span 2';b.onclick=()=>press(k);g.append(b)});
 win.onKey=e=>{const m={'*':'×','/':'÷','-':'−','Enter':'=','Escape':'C','Backspace':'←','Delete':'CE','.':','};let k=m[e.key]||e.key;if(/^[0-9+,=%]$/.test(k)||['×','÷','−','←','C','CE'].includes(k)){e.preventDefault();press(k)}};
 show();return win}
/* ================= PAINT ================= */
function appPaint(){
 const win=createWindow({app:'paint',title:'Безымянный — Paint',icon:'paint',w:860,h:580});
 const COLORS=['#000000','#7f7f7f','#880015','#ed1c24','#ff7f27','#fff200','#22b14c','#00a2e8','#3f48cc','#a349a4','#ffffff','#c3c3c3','#b97a57','#ffaec9','#ffc90e','#efe4b0','#b5e61d','#99d9ea','#7092be','#c8bfe7','#4a2c0f','#ff5ea8','#1b6e3a','#0e5a8f','#5c1b8c','#8a8a00','#e0e0e0','#444444'];
 const TOOLS=[['✎','Карандаш','pencil'],['🖌','Кисть','brush'],['⌫','Ластик','eraser'],['🪣','Заливка','fill'],['💉','Выбор цвета','pick'],['╱','Линия','line'],['▭','Прямоугольник','rect'],['◯','Эллипс','ellipse']];
 win.body.innerHTML=`<div class="menubar"></div><div class="pt-top"><div class="pt-tools"></div><div style="display:flex;flex-direction:column;gap:4px"><label>Толщина: <select class="sz"><option>1</option><option>2</option><option selected>4</option><option>8</option><option>14</option><option>24</option></select></label><label>Фигуры: <select class="fl"><option value="0">Контур</option><option value="1">Заливка</option></select></label></div><div class="pt-cur"><i class="p2" style="background:#fff"></i><i class="p1" style="background:#000"></i></div><div class="pt-pal"></div></div><div class="pt-area"><canvas class="pc" width="1000" height="620"></canvas></div><div class="pt-st"><span class="xy">0, 0 пкс</span><span>1000 × 620 пкс</span></div>`;
 const cv=$('canvas',win.body),ctx=cv.getContext('2d',{willReadFrequently:true});ctx.fillStyle='#fff';ctx.fillRect(0,0,cv.width,cv.height);
 let tool='pencil',c1='#000000',c2='#ffffff',undo=[];
 const tl=$('.pt-tools',win.body);TOOLS.forEach(([i,t,k])=>{const b=el('button','pt-t'+(k===tool?' on':''),i);b.title=t;b.onclick=()=>{tool=k;$$('.pt-t',win.body).forEach(x=>x.classList.toggle('on',x===b))};tl.append(b)});
 const pal=$('.pt-pal',win.body);COLORS.forEach(c=>{const d=el('div','pt-c');d.style.background=c;d.onpointerdown=e=>{if(e.button===2)c2=c;else c1=c;$('.p1',win.body).style.background=c1;$('.p2',win.body).style.background=c2};d.oncontextmenu=e=>e.preventDefault();pal.append(d)});
 const snap=()=>{undo.push(ctx.getImageData(0,0,cv.width,cv.height));if(undo.length>20)undo.shift()};
 const doUndo=()=>{if(undo.length)ctx.putImageData(undo.pop(),0,0)};
 function flood(x,y,hex){const W=cv.width,H=cv.height,img=ctx.getImageData(0,0,W,H),d=new Uint32Array(img.data.buffer);const r=parseInt(hex.slice(1,3),16),g=parseInt(hex.slice(3,5),16),b=parseInt(hex.slice(5,7),16);const nc=(255<<24)|(b<<16)|(g<<8)|r;const t=d[y*W+x];if(t===nc)return;const st=[x,y];while(st.length){const yy=st.pop(),xx=st.pop();let i=yy*W+xx;if(d[i]!==t)continue;let l=xx,rr=xx;while(l>0&&d[yy*W+l-1]===t)l--;while(rr<W-1&&d[yy*W+rr+1]===t)rr++;for(let k=l;k<=rr;k++){d[yy*W+k]=nc;if(yy>0&&d[(yy-1)*W+k]===t)st.push(k,yy-1);if(yy<H-1&&d[(yy+1)*W+k]===t)st.push(k,yy+1)}}ctx.putImageData(img,0,0)}
 const pos=e=>{const r=cv.getBoundingClientRect();return[Math.floor((e.clientX-r.left)*cv.width/r.width),Math.floor((e.clientY-r.top)*cv.height/r.height)]};
 cv.oncontextmenu=e=>e.preventDefault();
 cv.onpointerdown=e=>{
  e.preventDefault();cv.setPointerCapture(e.pointerId);const col=e.button===2?c2:c1,sec=e.button===2?c1:c2,[sx,sy]=pos(e),size=+$('.sz',win.body).value,fill=$('.fl',win.body).value==='1';
  if(tool==='pick'){const p=ctx.getImageData(sx,sy,1,1).data,h='#'+[p[0],p[1],p[2]].map(v=>v.toString(16).padStart(2,'0')).join('');if(e.button===2)c2=h;else c1=h;$('.p1',win.body).style.background=c1;$('.p2',win.body).style.background=c2;return}
  snap();if(tool==='fill'){flood(sx,sy,col);return}
  ctx.lineCap='round';ctx.lineJoin='round';ctx.strokeStyle=col;ctx.fillStyle=col;
  const free=tool==='pencil'||tool==='brush'||tool==='eraser';const w=tool==='pencil'?Math.max(1,size/4):tool==='eraser'?size*2.5:size;ctx.lineWidth=w;if(tool==='eraser'){ctx.strokeStyle=sec;ctx.fillStyle=sec}
  let lx=sx,ly=sy;const base=free?null:ctx.getImageData(0,0,cv.width,cv.height);
  if(free){ctx.beginPath();ctx.arc(sx,sy,w/2,0,7);ctx.fill()}
  const mv=ev=>{const[x,y]=pos(ev);$('.xy',win.body).textContent=`${x}, ${y} пкс`;
   if(free){ctx.beginPath();ctx.moveTo(lx,ly);ctx.lineTo(x,y);ctx.stroke();lx=x;ly=y;return}
   ctx.putImageData(base,0,0);ctx.beginPath();
   if(tool==='line'){ctx.moveTo(sx,sy);ctx.lineTo(x,y);ctx.stroke()}
   else if(tool==='rect'){ctx.rect(sx,sy,x-sx,y-sy);fill?(ctx.fillStyle=col,ctx.strokeStyle=sec,ctx.fill(),ctx.stroke()):ctx.stroke()}
   else if(tool==='ellipse'){ctx.ellipse((sx+x)/2,(sy+y)/2,Math.abs(x-sx)/2,Math.abs(y-sy)/2,0,0,7);fill?(ctx.fillStyle=col,ctx.strokeStyle=sec,ctx.fill(),ctx.stroke()):ctx.stroke()}};
  const up=()=>{cv.removeEventListener('pointermove',mv);cv.removeEventListener('pointerup',up)};cv.addEventListener('pointermove',mv);cv.addEventListener('pointerup',up)};
 cv.onpointermove=e=>{if(!(e.buttons)){const[x,y]=pos(e);$('.xy',win.body).textContent=`${x}, ${y} пкс`}};
 const clear=()=>{snap();ctx.fillStyle='#fff';ctx.fillRect(0,0,cv.width,cv.height)};
 $('.menubar',win.body).replaceWith(menubar([{t:'Файл',items:[{t:'Создать',key:'Ctrl+N',fn:clear},{t:'Сохранить как PNG...',key:'Ctrl+S',fn:()=>{const a=document.createElement('a');a.href=cv.toDataURL('image/png');a.download='Рисунок.png';a.click()}},{t:'Сделать фоновым рисунком рабочего стола',fn:()=>{const t=document.createElement('canvas');t.width=1280;t.height=Math.round(1280*cv.height/cv.width);t.getContext('2d').drawImage(cv,0,0,t.width,t.height);setCustomWall(t.toDataURL('image/jpeg',.85));store.set('w7chosen',true)}},'-',{t:'Выход',fn:()=>closeWin(win)}]},{t:'Правка',items:[{t:'Отменить',key:'Ctrl+Z',fn:doUndo},{t:'Очистить рисунок',fn:clear}]},{t:'Справка',items:[{t:'О программе Paint',fn:()=>msgBox({title:'Paint',icon:'paint',parent:win,text:'Paint — Windows 7 (симулятор). ЛКМ — основной цвет, ПКМ — фоновый.'})}]}]));
 win.onKey=e=>{if(e.ctrlKey&&e.key==='z'){e.preventDefault();doUndo()}};return win}
/* ================= MINESWEEPER ================= */
function appMine(){
 const L={b:[9,9,10],i:[16,16,40],e:[30,16,99]};let R=9,C=9,M=10,cells=[],first=true,over=false,won=false,time=0,timer=null;
 const win=createWindow({app:'mine',title:'Сапёр',icon:'mine',w:240,h:340,resizable:false,maxable:false,onClose:()=>clearInterval(timer)});
 win.body.style.background='#c0c0c0';
 win.body.innerHTML=`<div class="menubar"></div><div class="mine"><div class="mn-h"><div class="led l1">010</div><button class="face">🙂</button><div class="led l2">000</div></div><div class="mn-g"></div></div>`;
 const g=$('.mn-g',win.body),face=$('.face',win.body);
 const nb=i=>{const r=Math.floor(i/C),c=i%C,a=[];for(let dr=-1;dr<=1;dr++)for(let dc=-1;dc<=1;dc++){if(!dr&&!dc)continue;const rr=r+dr,cc=c+dc;if(rr>=0&&rr<R&&cc>=0&&cc<C)a.push(rr*C+cc)}return a};
 const flags=()=>cells.filter(c=>c.f).length;
 const led=n=>(n<0?'-'+String(Math.min(99,-n)).padStart(2,'0'):String(Math.min(999,n)).padStart(3,'0'));
 function newGame(lv){if(lv){[C,R,M]=L[lv]}clearInterval(timer);timer=null;time=0;first=true;over=false;won=false;cells=Array.from({length:R*C},()=>({m:true,o:false,f:false,n:0}));render();fit()}
 function fit(){requestAnimationFrame(()=>{const m=$('.mine',win.body);fitWin(win,m.offsetWidth,m.offsetHeight+$('.menubar',win.body).offsetHeight)})}
 const COL=['','#0000ff','#008000','#ff0000','#000080','#800000','#008080','#000','#808080'];
 function render(){
  g.style.gridTemplateColumns=`repeat(${C},24px)`;
  g.innerHTML=cells.map((c,i)=>{let t='',cl='mc';if(c.o){cl+=' o'+(c.m?' hit':'');t=c.m?'💣':c.n?`<span style="color:${COL[c.n]}">${c.n}</span>`:''}else if(c.f){t=(over&&!c.m)?'❌':'🚩'}else if(over&&c.m){t='💣';cl+=' o'}return `<div class="${cl}" data-i="${i}">${t}</div>`}).join('');
  $('.l1',win.body).textContent=led(M-flags());$('.l2',win.body).textContent=led(time);face.textContent=won?'😎':over?'😵':'🙂'}
 function lose(i){over=true;clearInterval(timer);cells.forEach(c=>{if(c.m&&!c.f)c.o=true});cells[i].o=true;render()}
 function reveal(i){
  const c=cells[i];if(c.o||c.f||over)return;
  if(first){first=false;return lose(i);let p=0;const safe=new Set([i]);while(p<M){const k=Math.floor(Math.random()*R*C);if(!cells[k].m&&!safe.has(k)){cells[k].m=true;p++}}cells.forEach((x,k)=>x.n=nb(k).filter(j=>cells[j].m).length);timer=setInterval(()=>{time++;$('.l2',win.body).textContent=led(time)},1000)}
  if(c.m)return lose(i);
  const st=[i];while(st.length){const k=st.pop(),x=cells[k];if(x.o||x.f)continue;x.o=true;if(!x.n)nb(k).forEach(j=>{if(!cells[j].o)st.push(j)})}
  if(cells.filter(x=>x.o).length===R*C-M){won=true;over=true;clearInterval(timer);cells.forEach(x=>{if(x.m)x.f=true});render();return}
  render()}
 g.addEventListener('click',e=>{const d=e.target.closest('.mc');if(d)reveal(+d.dataset.i)});
 g.addEventListener('contextmenu',e=>{e.preventDefault();const d=e.target.closest('.mc');if(!d||over)return;const c=cells[+d.dataset.i];if(!c.o){c.f=!c.f;render()}});
 g.addEventListener('dblclick',e=>{const d=e.target.closest('.mc');if(!d||over)return;const i=+d.dataset.i,c=cells[i];if(c.o&&c.n&&nb(i).filter(j=>cells[j].f).length===c.n)nb(i).forEach(j=>reveal(j))});
 g.addEventListener('pointerdown',e=>{if(!over&&e.button===0)face.textContent='😮'});g.addEventListener('pointerup',()=>{if(!over)face.textContent='🙂'});
 face.onclick=()=>newGame();
 $('.menubar',win.body).replaceWith(menubar([{t:'Игра',items:[{t:'Новая игра',key:'F2',fn:()=>newGame()},'-',{t:'Новичок',fn:()=>newGame('b')},{t:'Любитель',fn:()=>newGame('i')},{t:'Профессионал',fn:()=>newGame('e')},'-',{t:'Выход',fn:()=>closeWin(win)}]},{t:'Справка',items:[{t:'О программе',fn:()=>msgBox({title:'Сапёр',icon:'mine',parent:win,text:'Откройте все клетки, не содержащие мин. ПКМ — флажок. Двойной щелчок по числу — открыть соседей.'})}]}]));
 win.onKey=e=>{if(e.key==='F2')newGame()};newGame('b');return win}
/* ================= COMMAND PROMPT ================= */
function appCmd(){
 const win=createWindow({app:'cmd',title:'Командная строка',icon:'cmd',w:700,h:410});
 win.body.innerHTML=`<div class="cmd"><div class="co"></div><div class="cl"><span class="cp"></span><input type="text" spellcheck="false" autocomplete="off"></div></div>`;
 const box=$('.cmd',win.body),out=$('.co',win.body),inp=$('input',win.body),cp=$('.cp',win.body);
 let cwd=HOME.slice(),hist=[],hi=0;
 const pstr=()=>'C:\\'+cwd.slice(1).join('\\');
 const print=(t='')=>{const d=el('div');d.textContent=t;out.append(d)};
 const prompt=()=>{cp.textContent=pstr()+'>'};
 print('Microsoft Windows [Version 6.1.7601]');print('Copyright (c) 2009 Microsoft Corporation. Все права защищены.');print();prompt();
 box.onclick=()=>{if(!getSelection().toString())inp.focus()};
 const colors='0123456789abcdef',cmap=['#0c0c0c','#0000aa','#00aa00','#00aaaa','#aa0000','#aa00aa','#aa5500','#c0c0c0','#555555','#5555ff','#55ff55','#55ffff','#ff5555','#ff55ff','#ffff55','#ffffff'];
 function dirAt(parts,start){let p=start.slice();for(const x of parts){if(x==='..'){if(p.length>1)p.pop();continue}if(x==='.')continue;const d=resolve(p),k=Object.keys(d.children).find(n=>n.toLowerCase()===x.toLowerCase()&&d.children[n].type==='dir');if(!k)return null;p.push(k)}return p}
 function run(line){
  const[cmd,...rest]=line.trim().split(/\s+/),arg=rest.join(' '),c=(cmd||'').toLowerCase(),dir=resolve(cwd);
  switch(c){
   case '':break;
   case 'help':['CD       Вывод имени либо смена текущей папки.','CLS      Очистка экрана.','COLOR    Установка цвета фона и переднего плана.','DATE     Вывод даты.','DEL      Удаление одного или нескольких файлов.','DIR      Вывод списка файлов и подпапок.','ECHO     Вывод сообщений.','EXIT     Завершение работы программы CMD.EXE.','HOSTNAME Имя компьютера.','IPCONFIG Конфигурация IP.','MKDIR    Создание папки.','PING     Проверка связи.','START    Запуск программы (notepad, calc, mspaint, explorer...).','SYSTEMINFO Сведения о системе.','TASKLIST Список запущенных окон.','TIME     Вывод времени.','TITLE    Смена заголовка окна.','TYPE     Вывод содержимого текстового файла.','VER      Версия Windows.','WHOAMI   Имя пользователя.','SHUTDOWN /s | /r  Выключение или перезагрузка.'].forEach(print);break;
   case 'cls':out.innerHTML='';break;
   case 'echo':print(arg||'ECHO включен.');break;
   case 'ver':print();print('Microsoft Windows [Version 6.1.7601]');break;
   case 'date':print('Текущая дата: '+new Date().toLocaleDateString('ru'));break;
   case 'time':print('Текущее время: '+new Date().toLocaleTimeString('ru')+',00');break;
   case 'hostname':print('SIM-PC');break;
   case 'whoami':print('sim-pc\\user');break;
   case 'title':win.setTitle(arg||'Командная строка');break;
   case 'color':{const a=arg.toLowerCase();if(a.length===2&&colors.includes(a[0])&&colors.includes(a[1])){box.style.background=cmap[colors.indexOf(a[0])];box.style.color=cmap[colors.indexOf(a[1])];inp.style.color=box.style.color}else print('Установка цвета: COLOR bf, где b — фон, f — текст (0-9, a-f).');break}
   case 'dir':{print(' Том в устройстве C не имеет метки.');print(' Содержимое папки '+pstr());print();const d=new Date().toLocaleDateString('ru')+'  '+new Date().toLocaleTimeString('ru').slice(0,5);let f=0,dd=0;
    if(cwd.length>1){print(d+'    <DIR>          .');print(d+'    <DIR>          ..')}
    Object.entries(dir.children).forEach(([n,v])=>{if(v.type==='dir'){dd++;print(`${d}    <DIR>          ${n}`)}else{f++;print(`${d}  ${String(v.kind==='txt'?(v.content||'').length:152000).padStart(14)} ${n}`)}});
    print(`${String(f).padStart(15)} файлов`);print(`${String(dd).padStart(15)} папок  120 534 118 400 байт свободно`);break}
   case 'cd':case 'chdir':{if(!arg){print(pstr());break}let a=arg.replace(/^\/d\s+/i,'').replace(/^"|"$/g,'');let start=cwd;if(/^[cC]:/.test(a)||/^[\\\/]/.test(a)){start=['Локальный диск (C:)'];a=a.replace(/^[cC]:/,'')}const p=dirAt(a.split(/[\\\/]/).filter(Boolean),start);if(p)cwd=p;else print('Системе не удается найти указанный путь.');break}
   case 'mkdir':case 'md':{if(!arg){print('Синтаксис команды неверный.');break}if(dir.children[arg])print('Подпапка или файл '+arg+' уже существует.');else{dir.children[arg]=mkd();fsChanged()}break}
   case 'type':{const k=Object.keys(dir.children).find(n=>n.toLowerCase()===arg.toLowerCase());if(!k)print('Не удается найти указанный файл.');else if(dir.children[k].kind!=='txt')print('Невозможно отобразить двоичный файл.');else print(dir.children[k].content);break}
   case 'del':case 'erase':{const k=Object.keys(dir.children).find(n=>n.toLowerCase()===arg.toLowerCase());if(!k||dir.children[k].type!=='file')print('Не удается найти '+pstr()+'\\'+arg);else if(dir.children[k].prot)print('Отказано в доступе.');else{delete dir.children[k];fsChanged()}break}
   case 'ipconfig':print();print('Настройка протокола IP для Windows');print();print('Ethernet adapter Подключение по локальной сети:');print();print('   DNS-суффикс подключения . . . . . : home');print('   IPv4-адрес. . . . . . . . . . . . : 192.168.0.'+(2+Math.floor(Math.random()*200)));print('   Маска подсети . . . . . . . . . . : 255.255.255.0');print('   Основной шлюз. . . . . . . . . . : 192.168.0.1');break;
   case 'ping':{if(!arg){print('Использование: ping хост');break}print();print(`Обмен пакетами с ${arg} по с 32 байтами данных:`);let n=0;const t=[];const step=()=>{if(!wins.includes(win))return;if(n<4){const ms=8+Math.floor(Math.random()*30);t.push(ms);print(`Ответ от ${arg}: число байт=32 время=${ms}мс TTL=57`);n++;setTimeout(step,500)}else{print();print(`Статистика Ping для ${arg}:`);print('    Пакетов: отправлено = 4, получено = 4, потеряно = 0 (0% потерь)');print(`Приблизительное время приема-передачи в мс:`);print(`    Минимальное = ${Math.min(...t)}мсек, Максимальное = ${Math.max(...t)} мсек, Среднее = ${Math.round(t.reduce((a,b)=>a+b)/4)} мсек`);print();prompt()}};cp.textContent='';step();return 'async'}
   case 'systeminfo':['Имя узла:                        SIM-PC','Название ОС:                     Microsoft Windows 7 Максимальная','Версия ОС:                      6.1.7601 Service Pack 1 Сборка 7601','Изготовитель ОС:                Microsoft Corporation','Процессор(ы):                   '+(navigator.hardwareConcurrency||4)+' процессор(ов)','Полный объем физической памяти: '+((navigator.deviceMemory||4)*1024)+' МБ','Тип системы:                    x64-based PC'].forEach(print);break;
   case 'tasklist':print('Имя образа                     PID Имя сессии');print('========================= ======== ============');print('System Idle Process              0 Services');print('explorer.exe                  1312 Console');wins.filter(w=>w.app!=='dialog').forEach((w,i)=>print(`${(APPS[w.app]?APPS[w.app].name:w.app).padEnd(25)} ${String(2000+i*37).padStart(8)} Console`));break;
   case 'shutdown':{if(/\/s/i.test(arg))power('off');else if(/\/r/i.test(arg))power('restart');else if(/\/l/i.test(arg))power('logoff');else print('Использование: shutdown [/s | /r | /l]');break}
   case 'exit':closeWin(win);return;
   case 'start':{const t=(arg||'').toLowerCase().replace('.exe','');const m={notepad:'notepad',calc:'calc',mspaint:'paint',paint:'paint',explorer:'explorer',taskmgr:'taskmgr',iexplore:'ie',cmd:'cmd',winmine:'mine',mine:'mine',wmplayer:'wmp',control:'control'};if(m[t])launch(m[t]);else print('Системе не удается найти файл '+arg+'.');break}
   case 'notepad':case 'calc':case 'mspaint':case 'explorer':case 'taskmgr':case 'iexplore':case 'winmine':case 'control':run('start '+c);return;
   case 'matrix':print('Просыпайся, Нео...');break;
   default:print(`"${cmd}" не является внутренней или внешней`);print('командой, исполняемой программой или пакетным файлом.')}
  box.scrollTop=box.scrollHeight}
 inp.onkeydown=e=>{e.stopPropagation();
  if(e.key==='Enter'){const l=inp.value;print(pstr()+'>'+l);if(l.trim()){hist.push(l);hi=hist.length}inp.value='';const r=run(l);if(r!=='async'){print();prompt()}box.scrollTop=box.scrollHeight}
  else if(e.key==='ArrowUp'){if(hi>0){hi--;inp.value=hist[hi];e.preventDefault()}}else if(e.key==='ArrowDown'){if(hi<hist.length-1){hi++;inp.value=hist[hi]}else{hi=hist.length;inp.value=''}}};
 setTimeout(()=>inp.focus(),50);return win}
/* ================= TASK MANAGER ================= */
function appTask(){
 let sel=null,tab='apps',cpu=Array(60).fill(10);
 const win=createWindow({app:'taskmgr',title:'Диспетчер задач Windows',icon:'taskmgr',w:480,h:480,minW:380,onClose:()=>clearInterval(iv)});
 win.body.innerHTML=`<div class="menubar"></div><div class="tabs"><div class="tab on" data-t="apps">Приложения</div><div class="tab" data-t="processes">Процессы</div><div class="tab" data-t="perf">Быстродействие</div></div><div class="tp"></div><div class="ex-stat" style="display:flex;gap:30px"><span class="s1"></span><span class="s2"></span></div>`;
 $('.menubar',win.body).replaceWith(menubar([{t:'Файл',items:[{t:'Новая задача (Выполнить...)',fn:()=>inputDialog({title:'Создать новую задачу',label:'Введите имя программы (notepad, calc, mspaint, cmd, explorer):',value:'notepad',icon:'taskmgr',cb:v=>{const m={notepad:'notepad',calc:'calc',mspaint:'paint',cmd:'cmd',explorer:'explorer',iexplore:'ie',winmine:'mine'}[v.trim().toLowerCase().replace('.exe','')];m?launch(m):msgBox({title:v,icon:'error',text:`Windows не удается найти «${esc(v)}». Проверьте правильность написания имени и повторите попытку.`})}})},'-',{t:'Выход из диспетчера задач',fn:()=>closeWin(win)}]}]));
 const tp=$('.tp',win.body);
 $$('.tab',win.body).forEach(t=>t.onclick=()=>{tab=t.dataset.t;$$('.tab',win.body).forEach(x=>x.classList.toggle('on',x===t));draw()});
 function draw(){
  const ws=wins.filter(w=>w.app!=='dialog'&&w!==win.child);
  if(tab==='apps'){
   tp.innerHTML=`<table class="tbl"><tr><th>Задача</th><th style="width:110px">Состояние</th></tr>${ws.map(w=>`<tr class="${sel===w.id?'sel':''}" data-id="${w.id}"><td style="display:flex;gap:6px;align-items:center">${ic(w.icon,16)}${esc(w.title)}</td><td>${w.min?'Свёрнуто':'Работает'}</td></tr>`).join('')}</table><div style="flex:1"></div><div style="display:flex;justify-content:flex-end;gap:6px;padding:8px;border-top:1px solid #ddd"><button class="btn k">Снять задачу</button><button class="btn s">Переключиться</button></div>`;
   $$('tr[data-id]',tp).forEach(r=>r.onclick=()=>{sel=+r.dataset.id;draw()});
   const f=()=>wins.find(w=>w.id===sel);$('.k',tp).onclick=()=>{const w=f();if(w){closeWin(w,true);sel=null}};$('.s',tp).onclick=()=>{const w=f();if(w)focusWin(w)}}
  else if(tab==='processes'){tp.innerHTML='<div style="padding:14px;background:#fff;flex:1">Имя образа　　　 ЦП　　 Память<hr>explorer.exe　　　 0　　　 14 320 КБ<br><b>unknown.exe　　　 33　　　33 333 КБ</b><br><button class="btn kill-unknown" style="margin-top:20px">Завершить процесс unknown.exe</button></div>';$('.kill-unknown',tp).onclick=()=>msgBox({title:'Диспетчер задач',icon:'error',text:'Отказано в доступе. unknown.exe нельзя завершить.'})}
  else{tp.innerHTML=`<div style="padding:12px"><div style="margin-bottom:4px">Загрузка ЦП: <b class="pc"></b></div><canvas width="420" height="150" style="width:100%;height:150px;background:#000;border:2px inset #999"></canvas></div>`;gr()}
  $('.s1',win.body).textContent=`Процессов: ${ws.length+34}`;$('.s2',win.body).textContent=`Загрузка ЦП: ${Math.round(cpu[cpu.length-1])}%`}
 function gr(){const cv=$('canvas',tp);if(!cv)return;const x=cv.getContext('2d');x.fillStyle='#000';x.fillRect(0,0,420,150);x.strokeStyle='#0a4a0a';for(let i=0;i<=420;i+=21){x.beginPath();x.moveTo(i,0);x.lineTo(i,150);x.stroke()}for(let i=0;i<=150;i+=15){x.beginPath();x.moveTo(0,i);x.lineTo(420,i);x.stroke()}x.strokeStyle='#3f3';x.beginPath();cpu.forEach((v,i)=>{const px=i*7,py=150-v*1.5;i?x.lineTo(px,py):x.moveTo(px,py)});x.stroke();$('.pc',tp).textContent=Math.round(cpu[cpu.length-1])+'%'}
 const iv=setInterval(()=>{cpu.push(Math.max(2,Math.min(95,cpu[cpu.length-1]+(Math.random()-.5)*18)));cpu.shift();if(tab==='apps')draw();else{gr();$('.s2',win.body).textContent=`Загрузка ЦП: ${Math.round(cpu[cpu.length-1])}%`}},1000);
 draw();return win}
/* ================= INTERNET EXPLORER ================= */
function appIE(){
 const win=createWindow({app:'ie',title:'Добро пожаловать — Windows Internet Explorer',icon:'ie',w:900,h:580});
 win.body.innerHTML=`<div class="ie-bar"><button class="ex-b bk">◀</button><button class="ex-b fw">▶</button><input type="text" value="about:home"><button class="btn go" style="min-width:40px;padding:3px 8px">➜</button><button class="btn hm" style="min-width:40px;padding:3px 8px">⌂</button></div><div class="ie-fav"><span>★ Избранное</span><span data-u="windows.microsoft.com">Windows</span><span data-u="www.bing.com">Bing</span><span data-u="www.msn.com">MSN</span></div><div class="ie-view"></div>`;
 const view=$('.ie-view',win.body),addr=$('input',win.body);let h=['about:home'],hi=0;
 const home=()=>`<div style="min-height:100%;background:linear-gradient(#d7ecff,#fff 60%);padding:60px 20px;text-align:center"><div style="display:inline-flex;align-items:center;gap:14px">${ic('ie',72)}<div style="text-align:left"><div style="font-size:34px;color:#1e5fa8;font-weight:300">Internet Explorer 8</div><div style="color:#667">Домашняя страница по умолчанию</div></div></div><div style="margin:34px auto 0;max-width:520px;display:flex;gap:6px"><input class="q" type="text" placeholder="Поиск в Интернете" style="flex:1;height:34px;border:1px solid #7fa6d6;padding:0 10px;font-size:15px"><button class="btn sb" style="min-width:80px">Найти</button></div><p style="color:#777;margin-top:40px">Симулятор работает автономно — реальные сайты недоступны.</p></div>`;
 const err=u=>`<div style="padding:30px 40px;font-family:Verdana,Tahoma;color:#000"><div style="display:flex;gap:16px;align-items:center;background:#e8f0fb;padding:16px;border:1px solid #bcd">${ic('warn',48)}<div><div style="font-size:19px;color:#1a4b8e;font-weight:bold">Не удаётся отобразить эту веб-страницу</div></div></div><p><b>Рекомендации:</b></p><ul style="line-height:1.8"><li>Проверьте подключение к сети (приложение работает офлайн).</li><li>Проверьте адрес <b>${esc(u)}</b> на наличие ошибок.</li><li>Вернитесь на <a class="hl" style="color:#06c;text-decoration:underline">домашнюю страницу</a>.</li></ul></div>`;
 function nav(u,push=true){u=u.trim()||'about:home';if(push){h=h.slice(0,hi+1);h.push(u);hi++}addr.value=u;
  if(u==='about:home'){view.innerHTML=home();win.setTitle('Добро пожаловать — Windows Internet Explorer');const q=$('.q',view);const go=()=>nav('http://www.bing.com/search?q='+encodeURIComponent(q.value));$('.sb',view).onclick=go;q.onkeydown=e=>{e.stopPropagation();if(e.key==='Enter')go()}}
  else{view.innerHTML=err(u);win.setTitle('Невозможно отобразить страницу — Windows Internet Explorer');const l=$('.hl',view);if(l)l.onclick=()=>nav('about:home')}
  $('.bk',win.body).disabled=hi<=0;$('.fw',win.body).disabled=hi>=h.length-1}
 $('.bk',win.body).onclick=()=>{if(hi>0){hi--;nav(h[hi],false)}};$('.fw',win.body).onclick=()=>{if(hi<h.length-1){hi++;nav(h[hi],false)}};
 $('.go',win.body).onclick=()=>nav(addr.value);$('.hm',win.body).onclick=()=>nav('about:home');addr.onkeydown=e=>{e.stopPropagation();if(e.key==='Enter')nav(addr.value)};
 $$('.ie-fav span[data-u]',win.body).forEach(s=>s.onclick=()=>nav('http://'+s.dataset.u));nav('about:home');return win}
/* ================= MEDIA PLAYER ================= */
function appWmp(arg){
 const win=createWindow({app:'wmp',title:'Проигрыватель Windows Media',icon:'wmp',w:520,h:360,onClose:()=>stop()});
 win.body.innerHTML=`<div class="wmp"><div style="font-size:18px">${esc((arg&&arg.name)||'Калимба.mp3')}</div><div class="wmp-v">${'<i></i>'.repeat(18)}</div><button class="wmp-p">▶</button><div style="width:70%;height:6px;background:#345;border-radius:3px;overflow:hidden"><div class="pr" style="height:100%;width:0;background:#6cf"></div></div></div>`;
 let iv=null,step=0;const N=[523,659,784,988,784,659,587,698,880,1047,880,698],btn=$('.wmp-p',win.body),bars=$$('.wmp-v i',win.body),pr=$('.pr',win.body);
 function stop(){clearInterval(iv);iv=null;if(btn)btn.textContent='▶';bars.forEach(b=>b.style.height='6px')}
 btn.onclick=()=>{if(iv){stop();return}btn.textContent='❚❚';audio();iv=setInterval(()=>{tone(N[step%N.length],0,.5,'triangle',.16);if(step%4===0)tone(N[step%N.length]/2,0,.9,'sine',.1);step++;pr.style.width=((step%48)/48*100)+'%';bars.forEach(b=>b.style.height=(8+Math.random()*60)+'px')},320)};
 return win}
/* ================= PHOTO VIEWER ================= */
function appViewer(arg){
 const win=createWindow({app:'viewer',title:(arg.name||'Изображение')+' — Просмотр фотографий Windows',icon:'img',w:760,h:540});
 win.body.style.background='#d9e2ef';
 win.body.innerHTML=`<div style="flex:1;display:flex;align-items:center;justify-content:center;background:#e8eef7;min-height:0;position:relative"><img src="${esc(arg.src)}" style="max-width:100%;max-height:100%;object-fit:contain" alt=""><div class="er" style="display:none;color:#666">Не удалось загрузить изображение (нет подключения).</div></div><div style="padding:8px;display:flex;gap:8px;justify-content:center;background:linear-gradient(#f3f6fb,#d7e0ee);border-top:1px solid #b9c6da"><button class="btn bg" style="min-width:160px">Сделать фоном рабочего стола</button></div>`;
 $('img',win.body).onerror=e=>{e.target.style.display='none';$('.er',win.body).style.display='block'};
 $('.bg',win.body).onclick=()=>{const id=(walls().find(w=>w.url===arg.src)||{}).id;if(id){cfg.wall=id;saveCfg();store.set('w7chosen',true);applyWall()}else setCustomWall(arg.src)};return win}
/* ================= CONTROL PANEL / PERSONALIZATION / SYSTEM ================= */
function appControl(){
 const win=createWindow({app:'control',title:'Все элементы панели управления',icon:'control',w:720,h:480});
 const stub=n=>()=>msgBox({title:n,icon:'info',text:'Этот элемент панели управления недоступен в симуляторе.'});
 const items=[['Персонализация','control',()=>launch('personalize')],['Система','computer',()=>launch('sysinfo')],['Экран','computer',screenInfo],['Дата и время','clock',()=>togglePop('clockpop')],['Звук','sound',()=>togglePop('volpop')],['Центр поддержки','shield',()=>msgBox({title:'Центр поддержки',icon:'shield',text:'Проблем не обнаружено.'})],['Сеть','net',()=>togglePop('netpop')],['Учётные записи пользователей','user',stub('Учётные записи пользователей')],['Брандмауэр Windows','shield',stub('Брандмауэр Windows')],['Программы и компоненты','folder',stub('Программы и компоненты')],['Центр обновления Windows','shield',stub('Центр обновления Windows')],['Электропитание','drive',stub('Электропитание')]];
 win.body.innerHTML=`<div style="padding:10px 16px;color:#1e3f7a;font-size:15px;background:linear-gradient(#fff,#eef3fa);border-bottom:1px solid #d0d8e6">Настройка параметров компьютера</div><div class="cp-grid"></div>`;
 const g=$('.cp-grid',win.body);items.forEach(([t,i,fn])=>{const d=el('div','cp-i',`${ic(i,32)}<span style="color:#1a56a8">${esc(t)}</span>`);d.ondblclick=fn;d.onclick=fn;g.append(d)});return win}
function appPersonalize(){
 const win=createWindow({app:'personalize',title:'Персонализация',icon:'control',w:700,h:560,minH:400});
 win.body.style.background='#fff';
 win.body.innerHTML=`<div style="padding:10px 16px;background:linear-gradient(#fff,#eef3fa);border-bottom:1px solid #d0d8e6"><div style="font-size:16px;color:#1e3f7a">Изменение изображения и звуков на компьютере</div><div style="color:#555;margin-top:2px">Выберите фон рабочего стола и цвет окон.</div></div><div style="flex:1;overflow:auto"><div style="padding:10px 12px 0;color:#1e3f7a;font-size:14px">Фон рабочего стола</div><div class="wp-grid"></div><div style="padding:0 12px 8px"><button class="btn br" style="min-width:200px">Обзор… (свой рисунок)</button><input type="file" accept="image/*" style="display:none"></div><div style="padding:6px 12px 6px;color:#1e3f7a;font-size:14px;border-top:1px solid #e3e8f0">Цвет окна</div><div class="sw"></div><div style="padding:0 12px 14px"><label><input type="checkbox" class="gl"> Включить прозрачность</label></div></div>`;
 const grid=$('.wp-grid',win.body),sw=$('.sw',win.body),gl=$('.gl',win.body);
 function draw(){grid.innerHTML='';walls().forEach(w=>{const d=el('div','wp'+(cfg.wall===w.id?' on':''),`<div class="t" style="background-image:${w.url?`url('${esc(w.url)}')`:w.css}"></div><div style="margin-top:3px">${esc(w.name)}</div>`);d.onclick=()=>{cfg.wall=w.id;saveCfg();store.set('w7chosen',true);applyWall();draw()};grid.append(d)});
  sw.innerHTML='';THEMES.forEach(t=>{const i=el('i',cfg.theme===t[0]?'on':'');i.style.background=`linear-gradient(135deg,hsl(${t[2]},${t[3]}%,80%),hsl(${t[2]},${t[3]}%,45%))`;i.title=t[1];i.onclick=()=>{cfg.theme=t[0];saveCfg();applyTheme();draw()};sw.append(i)});gl.checked=cfg.glass}
 gl.onchange=()=>{cfg.glass=gl.checked;saveCfg();applyTheme()};
 const fi=$('input[type=file]',win.body);$('.br',win.body).onclick=()=>fi.click();
 fi.onchange=()=>{const f=fi.files[0];if(!f)return;const r=new FileReader();r.onload=()=>{const im=new Image();im.onload=()=>{const k=Math.min(1,1920/im.width),c=document.createElement('canvas');c.width=im.width*k;c.height=im.height*k;c.getContext('2d').drawImage(im,0,0,c.width,c.height);store.set('w7chosen',true);setCustomWall(c.toDataURL('image/jpeg',.88));draw()};im.src=r.result};r.readAsDataURL(f)};
 draw();return win}
function appSysinfo(){
 const win=createWindow({app:'sysinfo',title:'Система',icon:'computer',w:600,h:470});
 win.body.innerHTML=`<div class="sysinfo"><h3 style="margin-top:0">Издание Windows</h3><div style="display:flex;gap:16px;align-items:center"><div style="width:90px">${LOGO}</div><div><b style="font-size:16px">Windows 7 Максимальная</b><br>© Корпорация Майкрософт (Microsoft Corp.), 2009. Все права защищены.<br>Service Pack 1</div></div><h3>Система</h3><table><tr><td>Оценка:</td><td>7,9 Индекс производительности Windows</td></tr><tr><td>Процессор:</td><td>Виртуальный процессор, ${navigator.hardwareConcurrency||4} логических ядер</td></tr><tr><td>Установленная память (ОЗУ):</td><td>${navigator.deviceMemory||4},00 ГБ</td></tr><tr><td>Тип системы:</td><td>64-разрядная операционная система</td></tr><tr><td>Экран:</td><td>${innerWidth} × ${innerHeight}</td></tr></table><h3>Имя компьютера и параметры рабочей группы</h3><table><tr><td>Компьютер:</td><td>SIM-PC</td></tr><tr><td>Рабочая группа:</td><td>WORKGROUP</td></tr><tr><td>Пользователь:</td><td>User</td></tr></table><h3>Активация Windows</h3><div>Активация Windows выполнена ✔</div></div>`;return win}
/* ================= power / boot ================= */
function clearAll(){wins.slice().forEach(w=>closeWin(w,true));hideStart();hidePops();closeMenus()}
function showLogon(msg,ms,after){const l=$('#logon');l.classList.add('on');l.style.opacity=1;l.innerHTML=`<div class="spin"></div><div>${esc(msg)}</div>`;setTimeout(()=>{if(after)after()},ms)}
function hideOverlays(){['#boot','#logon','#power'].forEach(s=>$(s).classList.remove('on'))}
function tile(){const l=$('#logon');l.classList.add('on');$('#boot').classList.remove('on');$('#power').classList.remove('on');l.innerHTML=`<div class="lg-tile">${`<div class="lg-av">${USERPIC}</div>`}<div>User</div></div><div style="font-size:13px;opacity:.8">Нажмите, чтобы войти</div>`;$('.lg-tile',l).onclick=()=>{audio();welcome()}}
function welcome(){showLogon('Добро пожаловать',1300,()=>{const l=$('#logon');l.style.transition='opacity .5s';l.style.opacity=0;setTimeout(()=>{hideOverlays();l.style.transition='';l.style.opacity=1;sfx.start();balloon('Windows 7','Добро пожаловать! Дважды щёлкните значок на рабочем столе, чтобы открыть программу.')},500)})}
function bootSeq(){hideOverlays();const b=$('#boot');b.classList.add('on');b.innerHTML=`<div class="bflag">${LOGO}</div><div class="btxt">Запуск Windows</div><div class="bbar"></div>`;setTimeout(()=>{b.classList.remove('on');welcome()},2600)}
function offScreen(label){const p=$('#power');p.classList.add('on');p.innerHTML=label?`<div class="pbtn">⏻</div><div style="margin-top:18px;color:#888">Нажмите, чтобы включить компьютер</div>`:'';return p}
function power(kind){
 hideStart();
 if(kind==='lock'){tile();return}
 if(kind==='sleep'){offScreen(false);const wake=()=>{removeEventListener('pointerdown',wake);removeEventListener('keydown',wake);setTimeout(tile,200)};setTimeout(()=>{addEventListener('pointerdown',wake);addEventListener('keydown',wake)},300);return}
 clearAll();
 if(kind==='logoff'){showLogon('Выход из системы',1200,tile);return}
 if(kind==='restart'){showLogon('Перезагрузка',1500,()=>{offScreen(false);setTimeout(bootSeq,800)});return}
 showLogon('Завершение работы',1700,()=>{const p=offScreen(true);$('.pbtn',p).onclick=bootSeq})}
/* ================= global events ================= */
document.addEventListener('pointerdown',e=>{
 if(!e.target.closest('.ctx,.mb-item'))closeMenus();
 if(!e.target.closest('#start,#orb'))hideStart();
 if(!e.target.closest('.pop,[data-pop]'))hidePops();
 if(!e.target.closest('#thumbs,.tbtn'))hideThumbs()},true);
document.addEventListener('contextmenu',e=>{if(!e.target.closest('textarea,input'))e.preventDefault()});
$('#taskbar').addEventListener('contextmenu',e=>{if(e.target.closest('.tbtn'))return;e.preventDefault();showMenu(e.clientX,e.clientY-100,[{t:'Диспетчер задач',ico:'taskmgr',fn:()=>launch('taskmgr')},{t:'Свернуть все окна',fn:()=>$('#showdesk').click()},'-',{t:'Свойства',dis:true}])});
document.addEventListener('keydown',e=>{
 if(e.key==='Meta'){e.preventDefault();toggleStart();return}
 if(e.key==='Escape'){closeMenus();hideStart();hidePops();return}
 if(e.ctrlKey&&e.shiftKey&&e.key==='Escape'){e.preventDefault();launch('taskmgr');return}
 if(e.altKey&&e.key==='F4'&&activeWin){e.preventDefault();closeWin(activeWin);return}
 const t=e.target;if(t&&/INPUT|TEXTAREA|SELECT/.test(t.tagName))return;
 if(activeWin&&activeWin.onKey)activeWin.onKey(e)});
addEventListener('resize',()=>{renderDesktop();wins.forEach(w=>{if(!w.max&&w.rect.y>innerHeight-70){w.rect.y=Math.max(0,innerHeight-110);w.el.style.top=w.rect.y+'px'}})});
/* ================= A.R.C.H. stage 1 extension ================= */
function archSetupFS(){
 const drive=COMP.children['Локальный диск (C:)'];if(!drive)return;
 drive.children.Windows=drive.children.Windows||mkd();drive.children.Windows.children.Temp=drive.children.Windows.children.Temp||mkd();
 drive.children.Windows.children.Temp.children['observer.log']=mkt(arch.observerText());
 drive.children.Users=drive.children.Users||mkd();drive.children.Users.children.white=drive.children.Users.children.white||mkd();
 const user=drive.children.Users.children.white;user.children.Desktop=user.children.Desktop||mkd();user.children.Documents=user.children.Documents||mkd();
 const desk=user.children.Desktop.children,docs=user.children.Documents.children;
 const ensure=(name,node)=>{if(!desk[name])desk[name]=node};
 ensure('Записи',mkd({'record_01.txt':mkt('ЗАПИСЬ 01'),'record_02.txt':mkt('ЗАПИСЬ 02'),'record_03.txt':mkt('ЗАПИСЬ 03')}));
 ensure('Протоколы',mkd({'protocol_13.txt':mkt('Протокол 13\n\nСубъект начал проявлять признаки…\n\nПри обнаружении наблюдателя — не оборачиваться.')}));
 ensure('readme.txt',mkt('Не выключай компьютер'));
 ensure('не_открывать.txt',mkt('я же просил'));
 ensure('Новая папка (2)',mkd());
 ensure('что тут творится.ron',mkd({'запуск.exe':mka('archgame')}));
 ensure('Терминал',mka('cmd'));ensure('Браузер',mka('ie'));ensure('r33.gg',mka('archr33'));
 ensure('Сапёр.exe',mka('mine'));ensure('Косынка.lnk',mka('archcards'));
 ensure('мем_про_телепузика.jpg',mki('data:image/svg+xml,'+encodeURIComponent('<svg xmlns="http://www.w3.org/2000/svg" width="320" height="250"><rect width="320" height="250" fill="#fdc72f"/><rect width="160" height="125" fill="#ef6171"/><rect x="160" y="125" width="160" height="125" fill="#428ce1"/></svg>')));
 ensure('not_for_lane.txt',Object.assign(mkt('Лейн, не смотри записи'),{hidden:true}));desk['not_for_lane.txt'].hidden=true;
 docs['diary.txt']=docs['diary.txt']||mkt('Дневник Уайта\n\n03:33 — сегодня: Уайт пропал без вести.\n\nЕсли я не вернусь, скажите Лейну, что я не хотел. Пусть он не смотрит записи. Пусть просто выключит компьютер.');
 if(!TRASH.children['record_00.dat']&&!resolve(P_REC)?.children['record_00.dat'])TRASH.children['record_00.dat']=Object.assign(mkt('ЗАПИСЬ 00\nФайл помечен как удалённый.'),{origin:P_REC.slice()});
 COMP.children['Архив (D:)']=COMP.children['Архив (D:)']||mkd();COMP.children['Диск (E:)']=COMP.children['Диск (E:)']||mkd();
 COMP.children['Дисковод (F:)']=COMP.children['Дисковод (F:)']||{type:'dir',drive:'dvd',children:{}};
 delete COMP.children['DVD RW дисковод (D:)'];walk(COMP,[],(name,node)=>{if(node.kind==='img'&&/^https?:/i.test(node.src||''))node.src=px(0)});saveFS();
}
archSetupFS();
Object.assign(APPS,{archgame:{name:'запуск.exe',icon:'warn',fn:archExe},archr33:{name:'r33.gg',icon:'ie',fn:archBSOD},archcards:{name:'Косынка.lnk',icon:'doc',fn:archCards}});
SYS.splice(0,SYS.length,
 {k:'s:comp',name:'Этот компьютер',icon:()=>'computer',open:()=>launch('explorer',[]),sys:1},
 {k:'s:trash',name:'Корзина',icon:()=>Object.keys(TRASH.children).length?'trashfull':'trash',open:()=>launch('explorer',['::trash']),sys:1,trash:1});
cfg.wall='dark';cfg.glass=false;
$('#arch-pixel').onmouseenter=e=>{e.target.style.left=(3+Math.random()*90)+'%';e.target.style.top=(4+Math.random()*85)+'%'};
$('#arch-return').onclick=()=>{$('#arch-game').classList.remove('on');renderDesktop()};
$('#tr-flag').onclick=()=>balloon('A.R.C.H.','Обнаружен неизвестный файл: record_04. Поместить в карантин?',8500);
$('#icons').addEventListener('click',e=>{const d=e.target.closest('.di');if(d&&d.dataset.k==='f:r33.gg')archBSOD()});
function archCards(){const w=createWindow({app:'archcards',title:'Косынка.lnk',icon:'doc',w:510,h:320});w.body.innerHTML='<div style="height:100%;display:flex;align-items:center;justify-content:center;gap:9px;background:repeating-linear-gradient(40deg,#225c46,#225c46 20px,#287153 20px,#287153 40px)"><div style="width:90px;height:125px;background:#fff;border-radius:5px;box-shadow:2px 3px 4px #0008;padding:12px;color:#b22;font:70px Georgia">О</div><div style="width:90px;height:125px;background:#fff;border-radius:5px;box-shadow:2px 3px 4px #0008;padding:12px;color:#222;font:70px Georgia">Н</div></div>';return w}
function archExe(){msgBox({title:'Предупреждение системы безопасности',icon:'warn',text:'Не удаётся проверить издателя. Вы действительно хотите запустить этот файл?',buttons:['Да','Нет'],cb:i=>{if(i!==0)return;arch.mailCleared=true;store.set('arch-mail-cleared',true);clearAll();$('#arch-notice').classList.remove('on');const dark=$('#arch-dark');dark.classList.add('on');dark.innerHTML='<div style="text-align:center;padding-top:45vh;font:24px Consolas">ЗАПУСК...</div>';setTimeout(()=>{if(!dark.classList.contains('on'))return;dark.classList.remove('on');$('#arch-game').classList.add('on')},2000)}})}
function archBSOD(){if($('#arch-bsod').classList.contains('on'))return;clearAll();$('#arch-notice').classList.remove('on');$('#arch-bsod').classList.add('on');setTimeout(()=>{$('#arch-bsod').classList.remove('on');$('#arch-dark').classList.add('on');$('#arch-dark').innerHTML='';setTimeout(()=>{$('#arch-dark').classList.remove('on');arch.time='03:33';const desk=resolve(P_DESK);desk.children['предупреждение.txt']=mkt('не заходи на r33.gg\nэто сайт для взрослых\nсерьёзно. не надо.');fsChanged();tick()},500)},3000)}
function archShutdown(){clearAll();$('#arch-notice').classList.remove('on');$('#arch-dark').innerHTML='';$('#arch-dark').classList.add('on');setTimeout(()=>{$('#arch-dark').classList.remove('on');bootSeq()},5000)}
function bootSeq(){hideOverlays();const b=$('#boot');b.classList.add('on');const start=()=>{b.onclick=null;removeEventListener('keydown',key);b.innerHTML=`<div class="bflag">${LOGO}</div><div class="btxt">Запуск Windows 7</div><div class="bbar"></div>`;setTimeout(()=>{b.classList.remove('on');if(!wins.some(w=>w.app==='taskmgr'))minWin(launch('taskmgr'));if(!arch.notice){arch.notice=true;setTimeout(()=>$('#arch-notice').classList.add('on'),1300)}},3000)};const key=e=>{if(!arch.booted)return;start()};if(!arch.booted){arch.booted=true;b.innerHTML='<div style="font:18px Consolas,monospace;letter-spacing:.06em">A.R.C.H. Archive Terminal v2.3<div style="font-size:14px;margin-top:22px;opacity:.7">Press any key</div></div>';b.onclick=start;addEventListener('keydown',key)}else start()}
const ARCH_TERM={help:'help, cls, dir, whoami, logs, observer, history --incognito, shutdown, netcheck, netstat, route, ipconfig, ping observer, tracert archive',dir:'C:\\Users\\white\\Desktop\nЗаписи  Протоколы  readme.txt  что тут творится.ron',whoami:'user... или нет?',logs:'03:33 — [Лейн] — ВХОД','history --incognito':'03:33:01 — как удалить себя из системы\n03:33:14 — observer протокол\n03:33:27 — record_00 восстановление\n03:33:40 — Лейн\n03:33:52 — кто смотрит\n03:33:59 — я',netcheck:'Проверка сетевого адаптера... OK\nПроверка маршрутизатора... OK\nПроверка внешнего подключения... ОШИБКА\nПодключение отсутствует с 03:33:12\nПоследний активный пользователь: white',netstat:'Активные соединения:\nlocalhost:3333 — observer — ESTABLISHED\nlocalhost:8080 — archive — LISTENING\n[нет внешних подключений]',route:'Маршрут по умолчанию: 0.0.0.0\nШлюз: 03:33:03\nМетрика: ∞',ipconfig:'IPv4: 127.0.0.1\nМаска: 255.0.0.0\nШлюз: 0.0.0.0\nDNS: 03:33:03','ping observer':'Ответ от 127.0.0.1: число байт=33 время<1мс TTL=33\nОтвет от 127.0.0.1: число байт=33 время<1мс TTL=33\nОтвет от 127.0.0.1: число байт=33 время<1мс TTL=33'};
function appCmd(incognito=false){const w=createWindow({app:'cmd',title:incognito?'cmd.exe — скрытая история':'cmd.exe',icon:'cmd',w:700,h:410});w.body.innerHTML='<div class="cmd"><div class="co"></div><div class="cl"><span class="cp">ARCH-07\\white&gt;</span><input type="text" spellcheck="false" autocomplete="off"></div></div>';const box=$('.cmd',w.body),out=$('.co',w.body),inp=$('input',w.body);let loop=null;const print=t=>{const d=el('div');d.textContent=t;out.append(d);box.scrollTop=box.scrollHeight};w.o.onClose=()=>clearInterval(loop);print('A.R.C.H. Archive Terminal v2.3');if(incognito)print('доступ к скрытой истории требует проверки сети / введите netcheck для начала диагностики');else print('Введите help для списка команд.');inp.onkeydown=e=>{e.stopPropagation();if(e.key!=='Enter')return;const line=inp.value.trim(),key=line.replace(/\s+/g,' ').toLowerCase();inp.value='';if(!key)return;print('ARCH-07\\white> '+line);if(key==='cls'){out.textContent='';return}if(key==='observer'){setTimeout(()=>{if(wins.includes(w))print('Он смотрит. Не оборачивайся.')},2000);return}if(key==='shutdown'){archShutdown();return}if(key==='tracert archive'){clearInterval(loop);print('Трассировка маршрута к archive:');let hop=0;loop=setInterval(()=>{if(!wins.includes(w)||hop>=12){clearInterval(loop);return}print(`${++hop}  127.0.0.1 localhost`)},350);return}print(ARCH_TERM[key]||'Команда не найдена.')};box.onclick=()=>inp.focus();setTimeout(()=>inp.focus(),30);return w}

const ARCH_HISTORY=[[
 ['как настроить принтер hp в windows 7','Форум поддержки HP: подключите принтер через «Устройства и принтеры» → «Добавить принтер».'],['почему принтер печатает пустые листы','Может, он печатает то, что вы не видите'],['A.R.C.H. внутренний портал вход','portal'],['рецепт кофе в турке пропорции','На одну чашку: 100 мл воды, 1–2 чайные ложки молотого кофе. Нагревать на слабом огне.'],['tubbyhub.com','Сайт недоступен. Но вы всё равно здесь.'],['r33.gg','bsod'],['почему я ищу это в 3 часа ночи','Потому что ты не спишь. А он — да.'],['мемы про архив','meme'],['смихуятина.рф','silence']],
 [['протоколы безопасности A.R.C.H.','Протокол 13: при обнаружении наблюдателя — не оборачиваться'],['что делать если камера включается сама','Заклей. Если не помогает — значит, дело не в камере.'],['телепузики исчезновения 2012','В 2012 году пропали 7 сотрудников. Тела не найдены.'],['список пропавших сотрудников A.R.C.H.','table'],['record_01 что это','record'],['почему записи в архиве меняются','Вы не можете изменить то, что уже произошло.'],['кто такой observer','Результатов: 1. observer — это вы.'],['observer.log где найти','C:\\Windows\\Temp\\observer.log']],
 [['как открыть скрытые файлы windows 7','В Проводнике нажмите «Показать скрытые файлы».'],['C:\\Windows\\Temp observer.log','log'],['как остановить запись экрана','Запись остановить нельзя. Можно только выключить себя.'],['можно ли удалить файл навсегда','Нет. record_00 всё ещё в Корзине.'],['корзина windows восстановление удалённых','Откройте Корзину и нажмите «Восстановить record_00.dat».'],['record_00 существует ли','Да. Он ждёт.'],['кто смотрит через вебкамеру','Никто. Камера смотрит не наружу.'],['как заклеить вебкамеру','Слишком поздно.'],['как проверить зеркало на наличие','Посмотрите в монитор. Он уже там.'],['почему в отражении не я','Потому что это не вы.']],
 [['Лейн кто это','Результатов: 1. Лейн — пользователь, который сейчас смотрит эту страницу.'],['Лейн это я','Нет. Но скоро будет.'],['я не помню как меня зовут','Вы — Уайт. Вы — Лейн. Вы — observer. Выберите.'],['почему я не помню вчера','Потому что вчера не было. Был только архив.'],['помогите','Никто не ответил.'],['как выключить компьютер если он не выключается','Выключить можно. Проснуться — нет.'],['он не выключается','Он и не должен.'],['кто-нибудь','Я здесь.']],
 [['он уже здесь','Да.'],['не оборачивайся','Слишком поздно.'],['я вижу тебя','И я тебя.']]
];
/* A.R.C.H. mail module — attached to the existing desktop/window manager */
ICONS.mail='<rect x="4" y="11" width="40" height="28" rx="2" fill="url(#gGray)" stroke="#47709c" stroke-width="2"/><path d="M5 13l19 15 19-15M5 38l14-13M43 38L29 25" fill="none" stroke="#3971a8" stroke-width="2"/>';
APPS.mail={name:'Почта A.R.C.H.',icon:'mail',single:1,fn:appMail};
SYS.push({k:'s:mail',name:'Почта A.R.C.H.',icon:()=>'mail',open:()=>launch('mail'),sys:1});
START_PROGS.push('mail');
arch.records=new Set(store.get('arch-records',[]));
arch.mailCleared=store.get('arch-mail-cleared',false);
arch.mailViews=0;
arch.balance=3300;
function archRecordViewed(n){if(!/^record_0[123]\.(?:txt|dat)$/.test(n))return;arch.records.add(Number(n.match(/0([123])/)[1]));store.set('arch-records',[...arch.records]);const mail=wins.find(w=>w.app==='mail');if(mail&&mail.archRefresh)mail.archRefresh();}
const MAIL_IN=[
 {id:'p13',from:'admin@arch.local',subject:'Протокол 13',body:'Протокол 13 вступает в силу с сегодняшнего дня. При обнаружении наблюдателя — не оборачиваться. Не смотреть в отражения. Не открывать record_04 без разрешения. Это не рекомендация. — Администрация A.R.C.H.'},
 {id:'ron',from:'ron@arch.local',subject:'папка',body:'я сделал папку. назвал своим именем. не открывай запуск.exe, если не готов. я серьёзно. там не игра. — Рон',attachment:'запуск.exe'},
 {id:'observer',from:'observer@arch.local',subject:'я вижу тебя',body:'',locked:true,attachment:'record_04.dat'},
 {id:'self',from:'white@arch.local',subject:'себе',body:'если ты это читаешь, значит, я не вернулся. пароль от терминала — 0333. не смотри записи. просто выключи компьютер. пожалуйста. — Уайт'},
 {id:'lane',from:'lane@arch.local',subject:'кто ты?',body:'кто ты?',date:'03:33, сегодня'},
 {id:'mom1',from:'mom.white@mail.ru',subject:'Сынок, ты давно не звонил',body:'Уайти, привет. Мы с папой уже неделю не слышим тебя. Ты обещал позвонить в воскресенье. Работа — это хорошо, но ты совсем пропал. Позвони, как сможешь. Мы волнуемся. — Мама'},
 {id:'mom2',from:'mom.white@mail.ru',subject:'Ты поел?',body:'Сынок, я испекла твой любимый пирог. Приезжай, я оставлю тебе кусочек. И пожалуйста, не сиди ночами за этим компьютером. Это не доводит до добра. Я тебе говорила. — Мама'},
 {id:'mom3',from:'mom.white@mail.ru',subject:'Уайт, ответь пожалуйста',body:'Сынок, это уже не смешно. Мы звонили на работу, там говорят, что ты не выходил с ночной смены. Пожалуйста, ответь. Хоть одно слово. Мы очень боимся. — Мама'},
 {id:'dad1',from:'dad.white@mail.ru',subject:'Насчёт машины',body:'Сын, я тут посмотрел, что ты писал про машину. Если нужна помощь — скажи. Не тяни. И не пропадай, мать места себе не находит. — Папа'},
 {id:'dad2',from:'dad.white@mail.ru',subject:'Позвони матери',body:'Уайт, позвони матери. Она не спит. Я знаю, что у тебя работа, но это уже слишком. Позвони. — Папа'},
 {id:'dad3',from:'dad.white@mail.ru',subject:'Мы едем к тебе',body:'Мы с матерью едем к тебе. Не знаю, что у тебя там происходит, но мы приедем и разберёмся. Жди. — Папа',date:'03:33, сегодня'},
 {id:'net1',from:'no-reply@tubbynet.ru',subject:'Ваш баланс',body:'Уважаемый абонент! Ваш текущий баланс: –340 ₽. Рекомендуем пополнить счёт, чтобы избежать отключения. Тариф: «Архивный» (100 Мбит/с). Оплатить: [ссылка]',pay:true},
 {id:'net2',from:'no-reply@tubbynet.ru',subject:'Напоминание об оплате',body:'Уважаемый абонент! Ваш баланс: –1200 ₽. С 03:33 доступ к сети будет ограничен. Пожалуйста, оплатите задолженность. Оплатить: [ссылка]',pay:true},
 {id:'net3',from:'no-reply@tubbynet.ru',subject:'Доступ ограничен',body:'Уважаемый абонент! Ваш доступ к сети ограничен с 03:33. Причина: задолженность. Для восстановления доступа пополните баланс. Оплатить: [ссылка]',pay:true},
 {id:'net4',from:'no-reply@tubbynet.ru',subject:'Вы забыли оплатить',body:'Уважаемый абонент! Мы заметили, что вы пытались выйти в сеть. Напоминаем: доступ ограничен с 03:33. Ваш баланс: –2100 ₽. Вы не можете оплатить счёт, пока не восстановите доступ. Вы не можете восстановить доступ, пока не оплатите счёт. С уважением, TubbyNet.',pay:true},
 {id:'net5',from:'no-reply@tubbynet.ru',subject:'RE: Проблема с оплатой',body:'Уважаемый абонент! Оплата принимается только по карте. Наличные не принимаются. Если карта не проходит, обратитесь в банк. С уважением, TubbyNet.'},
 {id:'net6',from:'no-reply@tubbynet.ru',subject:'RE: Повторно',body:'Уважаемый абонент! Ваше обращение зарегистрировано. Срок рассмотрения — 33 рабочих дня. С уважением, TubbyNet.'}
];
const MAIL_SENT=[
 {id:'s1',from:'white@arch.local',to:'admin@arch.local',subject:'Субъект больше не реагирует',body:'Субъект больше не реагирует на свет. На звук тоже. Что делать? Жду указаний. — Уайт'},
 {id:'s2',from:'white@arch.local',to:'ron@arch.local',subject:'Ты уверен?',body:'Ты уверен, что это безопасно? Я видел, что он делает с записями. Они меняются, Рон. Они меняются, когда я не смотрю. — Уайт'},
 {id:'s3',from:'white@arch.local',to:'lane@arch.local',subject:'Прости',body:'Прости.',date:'03:33'},
 {id:'s4',from:'white@arch.local',to:'no-reply@tubbynet.ru',subject:'Проблема с оплатой',body:'Здравствуйте. Я не могу оплатить счёт. Карта не проходит. Принимаете ли вы наличные? Или можно как-то отсрочить? — Уайт'},
 {id:'s5',from:'white@arch.local',to:'no-reply@tubbynet.ru',subject:'Повторно',body:'Здравствуйте. Я писал вам два дня назад. Ответа нет. У меня отключают интернет, а мне очень нужно. Пожалуйста, ответьте. — Уайт'}
];
function mailItems(folder){if(arch.mailCleared)return folder==='in'?[{id:'last',from:'mom.white@mail.ru',subject:'Сынок, где ты?',body:'Сынок, где ты?'}]:[];
 if(folder==='in'){let a=MAIL_IN.map(m=>({...m}));if(arch.records.has(2)){let l=a.find(m=>m.id==='lane');l.body='я знаю, кто ты.';l.date=new Date().toLocaleString('ru');a.find(m=>m.id==='mom3').body+=' Сынок, мы звонили в полицию. Они говорят, что ещё рано. Рано?!'}
 if(arch.records.has(1)){a.push({id:'watch',from:'observer@arch.local',subject:'ты смотришь',body:'ты смотришь. продолжай.',date:'03:33, сегодня'});a.push({id:'net7',from:'no-reply@tubbynet.ru',subject:`Ваш баланс: –${arch.balance} ₽.`,body:`Ваш баланс: –${arch.balance} ₽. Доступ будет восстановлен после оплаты.`,pay:true})}
 if(arch.records.has(3))a.push({id:'dad4',from:'dad.white@mail.ru',subject:'Мы на месте. Здесь никого нет. Где ты?',body:'',locked:true,date:'03:33, сегодня'});return a}
 if(folder==='sent'){let a=MAIL_SENT.map(m=>({...m}));if(arch.records.has(3))a.find(m=>m.id==='s3').body='Прости. За всё.';if(arch.records.has(2))a.push({id:'s6',from:'white@arch.local',to:'no-reply@tubbynet.ru',subject:'Я оплачу',body:'Я оплачу. Обещаю. Только дайте мне ещё немного времени.',date:'03:33'});return a}
 return [{id:'draft',from:'white@arch.local',to:'lane@arch.local',subject:'Лейн, если ты это читаешь, я…',body:''}]
}
function appMail(){const old=wins.find(w=>w.app==='mail');if(old){focusWin(old);return old}
 const first=!store.get('arch-mail-opened',false);store.set('arch-mail-opened',true);arch.mailViews++;
 const win=createWindow({app:'mail',title:'Почта A.R.C.H. — Уайт',icon:'mail',w:1000,h:620,minW:570,minH:330});
 let folder='in',selected=null,locked=false,draftDone=false,autoTimer=null,balTimer=null,lockTimer=null;
 win.o.onClose=()=>{clearTimeout(autoTimer);clearInterval(balTimer);clearTimeout(lockTimer)};
 win.body.innerHTML='<div class="mail-shell"><div class="mail-head"><div class="mail-logo">✉ Почта A.R.C.H.</div><div><b>Уайт</b><br>white@arch.local</div></div><div class="mail-toolbar"><button class="btn mail-refresh">↻ Обновить</button><button class="btn mail-reply">↶ Ответить</button><span class="mail-banner"></span></div><div class="mail-columns"><nav class="mail-folders"></nav><div class="mail-list"></div><article class="mail-preview"></article></div><div class="mail-status"><span class="mail-spinner">◌</span> Подключение к серверу… <span class="mail-count"></span></div></div>';
 const list=$('.mail-list',win.body),preview=$('.mail-preview',win.body),folders=$('.mail-folders',win.body);
 function renderFolders(){folders.innerHTML='';[['in','✉ Входящие'],['sent','➤ Отправленные'],['draft','▤ Черновики']].forEach(([id,label])=>{const b=el('button','mail-folder'+(folder===id?' chosen':''),esc(label));b.onclick=()=>{folder=id;selected=null;locked=false;render()};folders.append(b)})}
 function render(){renderFolders();let a=mailItems(folder);if(selected&&!a.some(x=>x.id===selected))selected=null;list.innerHTML='';a.forEach(m=>{const b=el('button','mail-row'+(selected===m.id?' chosen':''),`<span class="mail-subject">${esc(m.subject)}${m.attachment?' 📎':''}</span><span class="mail-from">${esc(folder==='sent'?'→ '+m.to:m.from)}</span><span class="mail-date">${esc(m.date||'03:33')}</span>`);b.onclick=()=>{selected=m.id;if(m.locked){locked=true;render();lockTimer=setTimeout(()=>{if(!wins.includes(win)||selected!==m.id)return;locked=false;const t=appCmd();const out=$('.co',t.body),line=el('div');line.textContent='Не время';out.append(line);setTimeout(()=>{if(wins.includes(t))closeWin(t)},3000)},2000)}else{locked=false;render()}};list.append(b)});$('.mail-count',win.body).textContent=`${a.length} писем`;$('.mail-banner',win.body).textContent=arch.mailCleared?'Ящик очищен. Наблюдатель не должен видеть.':'';const m=a.find(x=>x.id===selected);$('.mail-reply',win.body).disabled=!m||folder==='draft';renderPreview(m)}
 function renderPreview(m){if(!m){preview.innerHTML='<div class="mail-empty">Выберите письмо для просмотра.</div>';return}
 if(locked){preview.innerHTML=`<div class="mail-freeze">Открытие письма<span class="mail-dots">...</span><br><small>${esc(m.subject)}</small>${m.attachment?`<button class="btn mail-locked-attachment">📎 record_04.dat — ${33+arch.mailViews*33} КБ</button>`:''}</div>`;const b=$('.mail-locked-attachment',preview);if(b)b.onclick=()=>msgBox({title:'Почта A.R.C.H.',icon:'error',text:'Не удаётся открыть record_04.dat. Отказано в доступе.'});return}
 let sender=m.from||'white@arch.local';const photo=sender==='mom.white@mail.ru'?'<span class="mail-photo" title="Фото недоступно. Адресат не найден."></span>':'';
 preview.innerHTML=`<div class="mail-message-head"><h3>${esc(m.subject)}</h3><div><b>От:</b> ${photo}${esc(sender)}</div><div><b>Кому:</b> ${esc(m.to||'white@arch.local')}</div><div><b>Дата:</b> ${esc(m.date||'03:33, сегодня')}</div></div><div class="mail-body"></div><div class="mail-attachments"></div>`;
 const body=$('.mail-body',preview);if(folder==='draft'){body.innerHTML='<div class="mail-draft-line">Лейн, если ты это читаешь, я<span class="mail-caret">▌</span></div><textarea readonly aria-label="Черновик не допускает редактирования" class="mail-draft-input" placeholder=""></textarea>';$('.mail-draft-input',body).onkeydown=e=>e.preventDefault();if(draftDone)fillDraft();else{clearTimeout(autoTimer);autoTimer=setTimeout(()=>{if(!wins.includes(win)||folder!=='draft'||selected!=='draft')return;draftDone=true;fillDraft()},5000)}}else body.textContent=m.body;
 const at=$('.mail-attachments',preview);if(m.attachment){at.innerHTML='<b>Вложение:</b> ';const button=el('button','btn',esc(m.attachment)+(m.id==='observer'?` — ${33+arch.mailViews*33} КБ`:''));button.onclick=()=>m.id==='ron'?archExe():msgBox({title:'Почта A.R.C.H.',icon:'error',text:'Не удаётся открыть record_04.dat. Отказано в доступе.'});at.append(button)}
 if(m.pay){const btn=el('button','btn','Оплатить');btn.onclick=()=>{const ie=launch('ie');const addr=$('.arch-address',ie.body);addr.value='https://tubbynet.ru/pay';$('.arch-go',ie.body).click()};at.append(btn)}}
 function fillDraft(){const line=$('.mail-draft-line',preview);if(line)line.innerHTML='Лейн, если ты это читаешь, я…я не хотел, чтобы ты это видел.'+(arch.records.has(1)?'<br>Пожалуйста, не открывай следующую запись.':'')+'<span class="mail-caret">▌</span>'}
 function reply(){const m=mailItems(folder).find(x=>x.id===selected);if(!m)return;if(m.locked||m.from==='observer@arch.local')return msgBox({title:'Почта A.R.C.H.',icon:'error',text:'Получатель не найден.'});let to=m.id==='self'?'lane@arch.local':m.id==='mom3'?'white@arch.local':m.from;const c=createWindow({app:'mailcompose',title:'Ответ: '+m.subject,icon:'mail',w:600,h:420});c.body.innerHTML=`<div class="mail-compose"><label>Кому: <input class="mail-to" value="${esc(to)}"></label><label>Тема: <input value="${esc('RE: '+m.subject)}"></label><textarea placeholder="Текст сообщения..."></textarea><button class="btn mail-send">Отправить</button></div>`;$('.mail-send',c.body).onclick=()=>msgBox({title:'Почта A.R.C.H.',icon:'error',text:m.id==='mom3'?'Получатель не найден. Возможно, он уже не здесь.':'Сообщение не отправлено. Нет подключения к серверу.'})}
 $('.mail-reply',win.body).onclick=reply;$('.mail-refresh',win.body).onclick=render;win.archRefresh=render;render();if(first&&!arch.mailCleared)balloon('Почта A.R.C.H.','Новое письмо от dad.white@mail.ru: «Мы едем к тебе»',5500);
 balTimer=setInterval(()=>{if(arch.records.has(1)&&!arch.mailCleared){arch.balance+=33;if(folder==='in')render()}},5000);
 return win}

/* Four reusable early-2010s page templates. Each returns complete in-browser markup. */
function pageForum(query,answer){const printer=/принтер|hp/i.test(query),camera=/камера|вебкамера/i.test(query),title=printer?'Принтер HP печатает пустые листы':camera?'Камера включается сама':'Как показать скрытые файлы в Windows 7';const area=printer?'Принтеры → HP → Настройка':camera?'Оборудование → Веб-камеры':'Windows 7 → Проводник';const question=printer?'Принтер HP печатает пустые листы. Настроил по инструкции, но он выдаёт пустые страницы. Как будто там ничего нет. Кто сталкивался?':camera?'Камера включается сама, даже когда не открыто ни одно приложение. Как её выключить?':'Как в Windows 7 открыть скрытые файлы? Я ищу not_for_lane.txt, но не вижу его.';const reply=printer?'Проверьте картридж. Если не помогает — возможно, он печатает то, что вы не видите.':camera?'Заклейте объектив. Если не помогает — значит, дело не в камере.':'В проводнике включите «Показать скрытые файлы». Только сначала подумайте, хотите ли видеть всё.';
 const post=(nick,role,time,text,quote='')=>`<section class="site-post"><aside><div class="site-avatar">${esc(nick[0].toUpperCase())}</div><b>${esc(nick)}</b><small>${esc(role)}<br>${esc(time)}</small></aside><div class="site-post-text">${quote?`<blockquote>${esc(quote)}</blockquote>`:''}${esc(text)}</div></section>`;
 return `<div class="site-page site-forum"><header class="site-header"><strong><span>Printer</span>Help.ru</strong><nav><a href="#" data-site="home">Форум</a> · <a href="#" data-site="home">Статьи</a> · <a href="#" data-site="login">Вход</a></nav></header><div class="site-crumbs">Форум → ${esc(area)}</div><div class="site-pad"><h1>${esc(title)}</h1><div class="site-meta">Тема открыта сегодня · Просмотров: 33 · Ответов: 1</div>${post('white','Новичок','03:12',question)}${post('admin_hr','Администратор','03:14',reply,printer?'Может, он печатает то, что вы не видите':question)}<div class="site-reply"><b>Быстрый ответ</b><textarea aria-label="Ответ на форуме" placeholder="Ваше сообщение..."></textarea><button type="button" class="site-btn" data-site="reply">Отправить</button><span class="site-feedback"></span></div></div><footer class="site-footer">PrinterHelp.ru © 2012 · Часовой пояс: 03:33</footer></div>`}
function pageSearch(query,answer){const q=esc(query),a=esc(answer||'Результаты найдены в архиве.');const titles=[`${query} — обсуждение на форуме`,`A.R.C.H. — материалы по запросу «${query}»`,'Ответы пользователей · архив обсуждений','Справочник Windows 7 — инструкция','Похожие запросы: кто смотрит','Зеркало страницы · сохранённая копия'];return `<div class="site-page site-search"><header class="site-search-head"><strong><span>Н</span><span>а</span><span>й</span><span>д</span>у</strong><input value="${q}" aria-label="Поисковый запрос"><button class="site-btn" data-site="search">Найти</button><nav>Веб　 Картинки　 Новости　 Карты</nav></header><div class="site-pad"><div class="site-meta">Найдено примерно 33 результата (0,03 сек.)</div>${titles.map((t,i)=>`<div class="site-hit"><a href="#" data-site="result" data-query="${q}">${esc(t)}</a><div class="site-url">archive.local/search/${i+1}</div><div>${i===0?a:esc(['Здесь обсуждают похожие случаи и симптомы.','Сохранённая копия страницы. Информация может быть неполной.','Пользователь white оставил комментарий в 03:33.','Ответ есть, но его не удаётся проверить.','Последняя активность: сегодня, 03:33.'][i-1])}</div></div>`).join('')}<div class="site-pages">Страницы: <a href="#" data-site="page">1</a> <a href="#" data-site="page">2</a> <a href="#" data-site="page">3</a> <a href="#" data-site="page">4</a> <a href="#" data-site="page">5</a></div></div><footer class="site-footer">Найду · Веб-поиск 2012 · сохранённые страницы</footer></div>`}
function pageArticle(query,answer){const protocol=/протокол/i.test(query),title=protocol?'Протокол 13 — инструкция для архивариусов':query,text=protocol?'Протокол 13: при обнаружении наблюдателя — не оборачиваться. Не смотреть в отражения. Не открывать record_04 без разрешения. Остальные страницы пусты.':answer||'Страница недоступна.';return `<div class="site-page site-article"><header class="site-header"><strong>A.R.C.H. <span>Внутренний архив</span></strong><nav><a href="#" data-site="home">Главная</a> · <a href="#" data-site="home">Документы</a> · <a href="#" data-site="home">Форум</a></nav></header><div class="site-crumbs">Архив → Документы → ${esc(title)}</div><div class="site-pad"><div class="site-paper"><h1>${esc(title)}</h1><div class="site-meta">Автор: Уайт · Опубликовано сегодня в 03:33 · Версия 13</div><p>${esc(text)}</p>${protocol?'<p class="site-redacted">[ ОСТАЛЬНЫЕ СТРАНИЦЫ ПУСТЫ ]</p>':''}</div><h3>Комментарии (3)</h3><div class="site-comment"><b>ron</b> <small>03:21</small><p>Кто подписал этот документ?</p></div><div class="site-comment"><b>white</b> <small>03:31</small><p>Я не помню.</p></div><div class="site-comment"><b>observer</b> <small>03:33</small><p>Прочитано.</p></div></div><footer class="site-footer">A.R.C.H. · Только для внутреннего использования</footer></div>`}
function pageUnavailable(query,extra=''){return `<div class="site-page site-unavailable"><div class="site-unavailable-box"><div class="site-disconnect"><i></i></div><h1>Сайт недоступен</h1><p>Соединение с сервером потеряно. Но вы всё равно здесь.</p>${extra?`<p class="site-strange">${esc(extra)}</p>`:''}<div class="site-meta">${esc(query||'Невозможно отобразить страницу')} · Ошибка соединения 03:33</div><a href="#" data-site="home">Вернуться в архив</a>${query==='r33.gg'?'<br><button class="site-btn" data-site="retry-r33">Повторить загрузку</button>':''}</div><footer class="site-footer">Internet Explorer 8 · Работа в автономном режиме</footer></div>`}
/* Full-text A.R.C.H. documents, integrated into the existing virtual filesystem. */
const ARCH_RULE='Документ является собственностью A.R.C.H. Копирование и вынос за пределы архива запрещены. При расхождении бумажной и цифровой копий действительной считается та, которая была открыта последней.';
function archDocument(title,author,date,sections,signature,stamp='A.R.C.H. / ВНУТРЕННИЙ АРХИВ'){
 return `${stamp}\n${'═'.repeat(56)}\n\n${title.toUpperCase()}\nДата составления: ${date}\nАвтор / отдел: ${author}\nРежим доступа: ограниченный\n\n${'─'.repeat(56)}\n\n`+sections.map(([h,t],i)=>`${i+1}. ${h.toUpperCase()}\n\n${t}\n\n`).join(`${'─'.repeat(56)}\n\n`)+`${'─'.repeat(56)}\n${ARCH_RULE}\n\nПодпись: ${signature}\n[ ПЕЧАТЬ: A.R.C.H. / 03:33 ]\n${'═'.repeat(56)}\n`;
}
function installArchDocuments(){const protocols=resolve([...P_DESK,'Протоколы']);const docs=resolve(P_DOCS),user=resolve(HOME);if(!protocols||!docs||!user)return;
 const P=protocols.children,D=docs.children;
 P['protocol_01.txt']=mkt(archDocument('Протокол наблюдения №1','Отдел наблюдения / observer','2012, 03:33',[
 ['Объект','Объект: Уайт. Дата: 2012. Наблюдение ведётся с 03:33.\nИсходное состояние: сотрудник находится в архивном секторе. Доступ к объекту имеет только ответственный исследователь.'],
 ['Результаты наблюдения','Объект не реагирует на свет. Объект не реагирует на звук. Объект смотрит в одну точку.\nВ 03:33 датчики движения зарегистрировали поворот головы. На видеозаписи поворота нет. Повторная проверка оборудования отклонений не выявила.'],
 ['Рекомендации','Рекомендация: продолжить наблюдение. Не приближаться. Не разговаривать.\nПри повторном обнаружении расхождений между журналом и видеозаписью сохранить оба варианта, не сравнивая их в присутствии объекта.'],
 ['Примечание','Наблюдатель не является живым существом. Слово observer обозначает внутренний протокол регистрации. Если субъект считает иначе, не исправлять его вслух.']
 ],'Наблюдатель: observer'));
 P['protocol_07.txt']=mkt(archDocument('Протокол №7: инцидент в лесу','A.R.C.H. Отдел 7','2012',[
 ['Сводка','В 2012 году группа исследователей вошла в лес. Вышли не все. Тела не найдены. Записи уничтожены. Официальная версия: авария. Неофициальная: они всё ещё там.'],
 ['Хронология','03:12 — группа сообщает о стабильном сигнале.\n03:21 — найдено строение, отсутствующее на карте.\n03:33 — прекращена внешняя связь.\n03:34 — радиоканал передаёт голоса сотрудников после подтверждения их исчезновения.'],
 ['Улика 07-Б','На сохранившемся кадре видна открытая дверь. Номер дома меняется при каждом просмотре. Сравнение копий допускается только в присутствии двух сотрудников. Рон отказался подписать протокол сравнения.'],
 ['Заключение','Территория закрыта для посещений. Архив не подтверждает присутствие здания. Запрос на повторную экспедицию отклонён. При получении новых видеозаписей не просматривать их в одиночку.']
 ],'A.R.C.H. Отдел 7'));
 P['protocol_13.txt']=mkt(archDocument('Протокол 13','Администрация A.R.C.H.','сегодня, 03:33',[
 ['Обязательное предписание','При обнаружении наблюдателя — не оборачиваться. Не смотреть в отражения. Не открывать record_04 без разрешения. Это не рекомендация.'],
 ['Признаки активации','Экран остаётся включённым после завершения работы. В истории браузера появляются запросы, которых пользователь не вводил. Последняя строка observer.log читается одинаково при любом количестве открытых окон.'],
 ['Действия персонала','Оставаться на месте. Не вступать в переписку с observer. Не сообщать субъекту, сколько времени прошло с 03:33. Не использовать зеркало для подтверждения личности.'],
 ['Страницы 2–3','[ ОСТАЛЬНЫЕ СТРАНИЦЫ ПУСТЫ ]\n\n\n\n\n\n\n\n\n\n[ СТРАНИЦА 3 ПУСТА ]']
 ],'Администрация A.R.C.H.'));
 P['protocol_33.txt']=mkt(archDocument('Протокол 33: правило архива','Отдел классификации','03:33',[
 ['Формулировка','Если этого нет в архиве — оно всё равно есть в архиве. Если вы читаете это — значит, вы уже в архиве. Если вы в архиве — значит, вы уже не вы.'],
 ['Порядок учёта','Удалённая запись остаётся зарегистрированной. Восстановление файла не считается появлением нового материала. Фамилия автора указывается той, что система показала до открытия документа.'],
 ['Применение','Правило 33 применяется к вещам, лицам и воспоминаниям. Нельзя доказать отсутствие субъекта поиском его имени. Любой отрицательный результат сохраняется как запись.'],
 ['Замечание','Сотрудник Уайт спросил, может ли субъект быть одновременно пользователем и записью. Ответ внесён в закрытое приложение. Рон не подписал приложение.']
 ],'А.R.C.H. / Отдел классификации'));
 P['protocol_last.txt']=mkt(archDocument('Последний протокол','Уайт','03:33, сегодня',[
 ['Личное обращение','Дата: 03:33. Автор: Уайт. Если я не вернусь — скажите Лейну, что я не хотел. Пусть он не смотрит записи. Пусть просто выключит компьютер. Простите.'],
 ['Попытка объяснения','Я думал, что фиксирую происходящее. Позднее понял: каждый просмотр создаёт ещё один вариант. Я не знаю, кто будет читать этот экземпляр. Я не знаю, скольких вариантов меня уже было.'],
 ['Порядок действий','Не запускайте файл, который оставил Рон, если не готовы увидеть начало. Если запустили, не ищите способ перемотать запись. Она не идёт вперёд, пока вы смотрите в сторону.'],
 ['Подтверждение','Это не инструкция для администрации. Это просьба для Лейна. Если имя адресата изменится само, оставить документ на месте.']
 ],'Уайт'));
 const days=[
 ['День 1','Мы приехали проверить сигнал. Лес молчит. Рон говорит, что это нормально. Я не уверен. На старой карте здесь только тропа, а прибор показывает устойчивую передачу откуда-то впереди. Я сохранил первую запись, чтобы потом доказать: мы действительно сюда вошли.'],
 ['День 2','Мы нашли дом. Он не был на карте. Дверь открыта. Кто-то был здесь недавно. В коридоре свет, но счётчик электроэнергии остановился в 03:33. Рон сказал, что слышал шаги. Я сказал, что это ветер. Ни один из нас не вышел проверить.'],
 ['День 3','Рон смотрит записи. Он говорит, что они меняются. Я не верю. Но они меняются. На вчерашнем кадре дверь была слева; теперь она справа. Мы записали время на бумаге. Бумага тоже изменилась. Рон создал папку со своим именем и оставил в ней файл.'],
 ['День 4','Это не Рон. Я не знаю, кто это. Но это не Рон. Его голос прежний, и куртка та же. Он отвечает на вопросы до того, как я их задаю. В камере иногда появляется лицо там, где должен быть пустой коридор.'],
 ['День 5','Мы потеряли связь. Я один. Я не помню, как сюда попал. На кровати лежит куртка, которую я не носил с 2012 года. За окном лес. Я пытался уйти, но вернулся к той же двери, не свернув ни разу.'],
 ['День 6','В отражении не я. Я не помню своего имени. Я не помню, кто я. Я накрыл зеркало тканью, но видел его на выключенном мониторе. Если запись смотрит на меня в ответ, значит, камера не была направлена наружу.'],
 ['День 7','Я нашёл record_00. Я не должен был. Теперь я знаю, что будет. Файл был удалён до того, как я его снял. В Корзине указан мой компьютер. Я не знаю, кто нажал «Восстановить» первым.'],
 ['День 8','Здесь никого нет. Только я. И он. Прости, мама. Прости, папа. Прости, Лейн. Я оставил тебе предупреждения, но каждое из них ведёт к следующей записи. Если это мой почерк, почему я не помню, как писал?']
 ];
 D['diary.txt']=mkt(archDocument('Дневник Уайта','Уайт / личные записи','день 1 — день 8',days,'Уайт','A.R.C.H. / ЛИЧНЫЙ АРХИВ'));
 D['список_пропавших.txt']=mkt(archDocument('Список пропавших сотрудников A.R.C.H.','Отдел кадров / архив','2012 — 03:33, сегодня',[
 ['Основание','Список составлен из кадровых карточек и записей полевых групп. Статус «не найден» означает отсутствие подтверждённых сведений, а не подтверждение смерти.'],
 ['Реестр','Сотрудник             Дата             Статус\n'+'─'.repeat(53)+'\nРон                   2012             пропал в лесу\nТинки-Винки           2012             не найден\nДипси                 2012             не найден\nЛа-Ла                 2012             не найдена\nПо                    2012             не найден\nНу-Ну                 2012             не найден\nУайт                  03:33 сегодня     пропал без вести\nЛейн                  03:33 сегодня     пропал без вести'],
 ['Примечание к карточке Лейна','Графа «должность» не заполнена. Графа «дата приёма» содержит значение 03:33. При печати реестра эта строка оказывается на последней странице независимо от выбранной сортировки.'],
 ['Сверка','По данным отдела кадров, карточка Уайта закрыта. Карточка Лейна активна. Невозможно подтвердить, что это две разные записи.']
 ],'Отдел кадров A.R.C.H.'));
 D['not_for_lane.txt']=mkt(archDocument('НЕ ДЛЯ ЛЕЙНА','Уайт','03:33, сегодня',[
 ['Обращение','Лейн, не смотри записи. Я серьёзно. Если ты это читаешь — значит, ты уже смотришь. Остановись. Выключи компьютер. Пожалуйста.'],
 ['Почему я оставил этот файл','Я не могу объяснить, почему предупреждение лежит рядом с материалами, которые прошу не открывать. Возможно, я надеялся, что ты увидишь его раньше. Возможно, другого способа обратиться к тебе уже нет.'],
 ['Если ты всё-таки продолжишь','Не доверяй дате создания файла. Не доверяй подписи под записью. Если услышишь мой голос, это ещё не доказывает, что говорю я. Не отвечай на письма от observer.'],
 ['Последняя просьба','Просто закрой окно. Не ищи record_00. Если когда-нибудь вспомнишь, как оказался здесь, не проверяй воспоминание по журналу системы.']
 ],'Уайт','ЛИЧНО / НЕ ДЛЯ ЛЕЙНА'));
 D['observer.log']=mkt(arch.observerText());
 user.children['Мои документы']=user.children['Мои документы']||mkd();const M=user.children['Мои документы'].children;
 M['readme.txt']=mkt(archDocument('Прочти меня','Уайт','03:33',[
 ['Перед началом','Не выключай компьютер. Если выключишь — он вернётся. Не смотри записи дважды. Не отвечай на письма от observer. Не заходи на r33.gg. Если ты уже зашёл — не оборачивайся.'],
 ['О файлах','Файл record_00 не исчезает после удаления. Смена имени папки не меняет её содержимое. Файл запуск.exe создан Роном; расширение .ron в названии папки — подпись, а не тип файла.'],
 ['О наблюдении','observer — протокол, а не монстр. Протокол фиксирует открытие окон, даже если окно сразу закрыли. Последняя строка журнала не должна меняться.'],
 ['Если всё начнётся снова','Запиши время, которое видишь на часах. Сравни его с отметкой в письме, которого ещё не отправлял. Если они совпадают, не пытайся доказать, какой из вас первый.']
 ],'Уайт','МОИ ДОКУМЕНТЫ / ПРОЧТИ ПЕРВЫМ'));
 M['инструкция.txt']=mkt(archDocument('Инструкция по безопасности A.R.C.H.','Отдел безопасности','2012 / обновлено 03:33',[
 ['Обязательные правила','1. Не смотреть в отражения.\n2. Не открывать record_04.\n3. Не отвечать observer.\n4. Не выходить в лес после заката.\n5. Если вы видите телепузика без лица — это не телепузик.\n6. Если вы не помните своего имени — не пытайтесь вспомнить.\n7. Если компьютер выключается сам — не включайте его снова.\n8. Если вы читаете это — вы уже нарушили пункт 7.'],
 ['При отказе связи','Не использовать внешние сайты как доказательство отсутствия сети. Локальные страницы могут загружаться после отключения маршрутизатора. Не связываться с сотрудниками, числящимися пропавшими.'],
 ['При обнаружении записи','Не просматривать её в одиночку. Зафиксировать имя файла и показания часов на бумаге. Не переписывать содержание до окончания воспроизведения.'],
 ['Подтверждение ознакомления','Подпись сотрудника: ____________________\nВремя: 03:33\nОтметка о повторном ознакомлении: 03:33']
 ],'Отдел безопасности A.R.C.H.'));
 M['письмо_маме.txt']=mkt(archDocument('Письмо, которое Уайт не отправил','Уайт','03:33, сегодня',[
 ['Черновик письма','Мама, прости. Я не хотел, чтобы так вышло. Я не могу объяснить, что здесь происходит. Я просто хочу, чтобы ты знала: я не виноват. Я не хотел. Я люблю тебя. Прости.'],
 ['Неотправленный абзац','Я помню, как ты оставляла мне кусочек пирога и говорила не задерживаться на работе. Я должен был позвонить в воскресенье. Я всё ещё собираюсь, хотя уже не знаю, какой сегодня день недели.'],
 ['Вместо обратного адреса','Не ищи меня по рабочему номеру. Если кто-то ответит и скажет, что я вернулся, попроси назвать меня так, как ты называла меня в детстве. Я боюсь, что он тоже это знает.'],
 ['Статус','Сообщение сохранено локально. Подключение отсутствует с 03:33. Отправка не выполнялась.']
 ],'Твой сын. Уайт.','ЛИЧНЫЕ ДОКУМЕНТЫ / НЕ ОТПРАВЛЕНО'));
 saveFS();
}
installArchDocuments();
SYS.push({k:'s:docs',name:'Документы',icon:()=>'folder',open:()=>launch('explorer',P_DOCS),sys:1},
 {k:'s:mydocs',name:'Мои документы',icon:()=>'folder',open:()=>launch('explorer',[...HOME,'Мои документы']),sys:1});

/* Fifteen self-contained archive recordings and a Canvas/Web Audio player. */
const REC_DATA=[
 {scene:'empty',duration:8000,text:'Ты не должен был это видеть.',voice:'Я предупреждал.'},
 {scene:'forest',duration:12000,text:'День 1. Мы приехали проверить сигнал.\nЛес молчит.',voice:'Запись первая. Сигнал идёт откуда-то из глубины леса.'},
 {scene:'forest-shake',duration:12000,text:'День 2. Мы нашли дом.\nОн не был на карте.',voice:'Дом старый. Но дверь открыта. Кто-то был здесь недавно.'},
 {scene:'corridor',duration:14000,text:'День 2, вечер.\nВ коридоре кто-то есть.\nОн не двигается.',voice:'Он стоит и смотрит. Я не могу разглядеть лицо.'},
 {scene:'monitors',duration:12000,text:'День 3. Рон смотрит записи.\nОн говорит, что они меняются.',voice:'Они меняются, когда я не смотрю.'},
 {scene:'corridor-figure',duration:14000,text:'День 3, ночь.\nЯ вижу его.\nОн стоит и смотрит.',voice:'Он ближе, чем был.'},
 {scene:'face',duration:10000,text:'День 4.\nЭто не Рон.\nЭто не Рон.',voice:'Это не Рон. Это не Рон. Это не Рон.'},
 {scene:'forest-night',duration:12000,text:'День 5.\nМы потеряли связь.\nЯ один.',voice:'Я один. Я один. Я один.'},
 {scene:'bedroom',duration:12000,text:'День 5.\nЯ не помню, как сюда попал.',voice:'Я не помню. Я не помню. Я не помню.'},
 {scene:'mirror',duration:10000,text:'День 6.\nВ отражении не я.',voice:'Это не я. Это не я. Это не я.'},
 {scene:'corridor-dark',duration:10000,text:'День 6.\nОн ближе.',voice:'Он ближе. Он ближе. Он ближе.'},
 {scene:'records-room',duration:12000,text:'День 7.\nЯ нашёл record_00.\nЯ не должен был.',voice:'Я не должен был это видеть.'},
 {scene:'screen-face',duration:10000,text:'День 7.\nОн смотрит на меня через экран.',voice:'Я вижу тебя.'},
 {scene:'forest-fog',duration:12000,text:'День 8.\nЯ не помню своего имени.',voice:'Я не помню. Я не помню. Я не помню.'},
 {scene:'empty',duration:14000,text:'День 8.\nЗдесь никого нет.\nТолько я.\nИ он.',voice:'Здесь никого нет. Кроме нас.'}
];
const recName=id=>`record_${pad(id)}.dat`;
const mkrec=id=>({type:'file',kind:'record',recId:id,prot:true});
function installArchRecords(){const folder=resolve(P_REC),trash=TRASH.children;if(!folder)return;for(let i=1;i<REC_DATA.length;i++){delete folder.children[`record_${pad(i)}.txt`];folder.children[recName(i)]=mkrec(i)}
 if(folder.children[recName(0)])folder.children[recName(0)]=mkrec(0);
 else trash[recName(0)]=Object.assign(mkrec(0),{origin:P_REC.slice()});saveFS()}
installArchRecords();
arch.events=[];
function archLogEvent(text){arch.events.push(`${arch.time}:00 — ${text}`);for(const p of [P_TEMP,P_DOCS]){const folder=resolve(p);if(folder&&folder.children['observer.log'])folder.children['observer.log'].content=arch.observerText()}saveFS()}
function recSound(scene){try{audio();if(scene.startsWith('forest')){tone(80,0,2,'sine',.055);tone(120,0,1.5,'triangle',.045)}else if(scene.startsWith('corridor')){tone(60,0,3,'sawtooth',.035);tone(200,.22,.3,'square',.025);tone(200,.75,.3,'square',.025)}else if(scene==='mirror'){tone(400,0,.5,'triangle',.045);tone(800,.4,.2,'square',.025)}else if(scene==='face'||scene==='screen-face'){tone(150,0,1,'sawtooth',.04);tone(300,.3,.5,'square',.025)}else tone(50,0,4,'sine',.025)}catch(e){/* AudioContext may not be offered for local files */}}
function drawRecScene(ctx,kind,seconds){const W=720,H=400,t=seconds;ctx.setTransform(1,0,0,1,0,0);ctx.fillStyle='#010303';ctx.fillRect(0,0,W,H);ctx.save();
 const rectangle=(x,y,w,h,c)=>{ctx.fillStyle=c;ctx.fillRect(x,y,w,h)};
 const stroke=(pts,color,width=1)=>{ctx.beginPath();pts.forEach(([x,y],i)=>i?ctx.lineTo(x,y):ctx.moveTo(x,y));ctx.strokeStyle=color;ctx.lineWidth=width;ctx.stroke()};
 function forest(night=false,fog=false,shake=false){if(shake)ctx.translate((Math.random()-.5)*6,(Math.random()-.5)*6);let grad=ctx.createLinearGradient(0,0,0,H);grad.addColorStop(0,night?'#010504':'#10251b');grad.addColorStop(1,night?'#030907':'#172718');rectangle(-5,-5,W+10,H+10,grad);rectangle(0,305,W,95,night?'#020503':'#0a1810');for(let i=0;i<16;i++){const depth=(i%8+1)/8,x=(i*113+37)%760-20+Math.sin(t*1.2+i)*4*depth,width=4+depth*27,y=-35-depth*15;rectangle(x,y,width,H+55,night?'#040907':i%3?'#0b1510':'#12190f');stroke([[x+width/2,155],[x-48*depth,45],[x-68*depth,-20]],night?'#050b08':'#15251a',Math.max(2,depth*6));stroke([[x+width/2,230],[x+55*depth,80],[x+75*depth,-10]],night?'#050b08':'#0f2016',Math.max(2,depth*5))}if(fog){let f=ctx.createLinearGradient(0,180,0,H);f.addColorStop(0,'rgba(182,212,190,0)');f.addColorStop(1,`rgba(173,205,182,${.19+.13*Math.sin(t*2)})`);rectangle(0,180,W,H-180,f)}}
 function corridor(dark=false,figure=false){let g=ctx.createRadialGradient(360,178,5,360,178,390);g.addColorStop(0,dark?'#232420':'#9b9e83');g.addColorStop(.35,dark?'#0b0d0d':'#4b5048');g.addColorStop(1,'#040605');rectangle(0,0,W,H,g);stroke([[0,0],[282,136],[438,136],[W,0]],'#222921',3);stroke([[0,H],[282,236],[438,236],[W,H]],'#30342f',3);stroke([[282,136],[282,236]],'#31342e',3);stroke([[438,136],[438,236]],'#31342e',3);for(let i=0;i<5;i++){let f=i/5;stroke([[360+(i-2)*64,136],[360+(i-2)*150,0]],'#333c35',1);stroke([[360+(i-2)*64,236],[360+(i-2)*155,H]],'#1b231d',1)}if(figure){let x=359+Math.sin(t*2)*5;rectangle(x-13,166,26,75,'#010202');ctx.beginPath();ctx.arc(x,160,15,0,Math.PI*2);ctx.fillStyle='#010202';ctx.fill()}}
 function face(screen=false){let bg=ctx.createRadialGradient(360,190,10,360,190,320);bg.addColorStop(0,'#4b5a4d');bg.addColorStop(1,'#030605');rectangle(0,0,W,H,bg);ctx.beginPath();ctx.ellipse(360,189,116,150,0,0,Math.PI*2);ctx.fillStyle='#949c87';ctx.fill();ctx.beginPath();ctx.ellipse(322,170,14,27,0,0,Math.PI*2);ctx.ellipse(398,170,14,27,0,0,Math.PI*2);ctx.fillStyle='#020303';ctx.fill();ctx.beginPath();ctx.ellipse(360,260,22,18+Math.abs(Math.sin(t*4))*25,0,0,Math.PI*2);ctx.fill();if(screen){for(let i=0;i<40;i++)rectangle(Math.random()*W,Math.random()*H,Math.random()*18+2,1,'#ccd9ce');rectangle(0,200+Math.sin(t*18)*110,W,3,'#d1e2ce33')}}
 function screens(records=false){rectangle(0,0,W,H,'#080a0c');for(let i=0;i<6;i++){let col=i%3,row=Math.floor(i/3),x=45+col*225,y=55+row*158,c=records?['#123d28','#2f392b','#1d3040'][i%3]:['#264366','#345242','#564238'][i%3];rectangle(x-5,y-5,194,134,'#252b30');rectangle(x,y,184,124,Math.sin(t*8+i)>.1?c:'#12191d');for(let k=0;k<6;k++)rectangle(x+5,y+9+k*17,150,2,records?'#6a997e88':'#a7c9d266');if(records){rectangle(x+72,y+25,14,68,'#101610');rectangle(x+105,y+26,10,67,'#121810')}}}
 switch(kind){case 'forest':forest();break;case 'forest-shake':forest(false,false,true);break;case 'forest-night':forest(true);break;case 'forest-fog':forest(false,true);break;case 'corridor':corridor();break;case 'corridor-figure':corridor(false,true);break;case 'corridor-dark':corridor(true);break;case 'face':face();break;case 'screen-face':face(true);break;case 'mirror':rectangle(0,0,W,H,'#161a19');rectangle(190,20,340,370,'#574436');rectangle(204,33,312,343,'#111d1d');ctx.beginPath();ctx.ellipse(362,184,70,110,0,0,Math.PI*2);ctx.fillStyle='#667374';ctx.fill();rectangle(324,175,15,8,'#080808');rectangle(388,175,15,8,'#080808');stroke([[220,42],[344,115],[311,260],[462,343],[410,365]],'#adc2c1',2);break;
 case 'bedroom':rectangle(0,0,W,H,'#222a2a');rectangle(480,24,178,180,'#10191d');rectangle(494,38,150,152,'#060b11');rectangle(559,38,3,152,'#667377');rectangle(0,300,W,100,'#171818');rectangle(95,241,390,74,'#4d4841');rectangle(113,233,85,30,'#c3c0ac');rectangle(455,202,15,146,'#282018');break;
 case 'monitors':screens();break;case 'records-room':screens(true);break;default:{let g=ctx.createRadialGradient(360,95,3,360,95,280);g.addColorStop(0,Math.sin(t*7)>.3?'#888077':'#33312c');g.addColorStop(.4,'#171717');g.addColorStop(1,'#010101');rectangle(0,0,W,H,g);rectangle(350,39,20,7,'#c5be9c')}}
 ctx.restore();for(let i=0;i<20;i++){let x=Math.random()*W,y=Math.random()*H;rectangle(x,y,Math.random()*2+1,Math.random()*2+1,'rgba(245,250,245,.45)')}ctx.fillStyle='rgba(255,255,255,.45)';ctx.font='11px Consolas, monospace';ctx.fillText('A.R.C.H. // CAM 03:33',12,19);ctx.fillText(`● REC    ${kind.toUpperCase()}`,515,19);for(let y=0;y<H;y+=4)rectangle(0,y,W,1,'rgba(0,0,0,.09)')}
function playRecord(id){id=Number(id);const rec=REC_DATA[id];if(!rec)return;wins.filter(w=>w.app==='record').forEach(w=>closeWin(w,true));const name=recName(id),w=createWindow({app:'record',title:'▶ '+name,icon:'wmp',w:720,h:480,minW:420,minH:300,resizable:false,maxable:false});w.el.classList.add('arch-record-window');$('.tb',w.el).style.display='none';w.body.innerHTML=`<div class="rec-win"><div class="rec-titlebar"><span>▶ ${esc(name)}</span><button class="rec-close" title="Закрыть запись">×</button></div><canvas class="rec-canvas" width="720" height="400" aria-label="Анимированная запись ${esc(name)}"></canvas><div class="rec-text" aria-live="polite"><span class="rec-typed"></span><span class="cursor"></span></div><div class="rec-controls"><button class="rec-stop">■ Стоп</button><div class="rec-progress"><div class="bar"></div></div><span class="rec-time">0:00 / 0:${pad(Math.ceil(rec.duration/1000))}</span></div></div>`;
 const cv=$('.rec-canvas',w.body),ctx=cv.getContext('2d'),text=$('.rec-typed',w.body),cursor=$('.cursor',w.body),bar=$('.bar',w.body),clock=$('.rec-time',w.body);let raf=0,tickText=0,voiceTimer=0,start=performance.now(),done=false,index=0,lastFrame=0;
 const cleanup=()=>{cancelAnimationFrame(raf);clearInterval(tickText);clearTimeout(voiceTimer);try{window.speechSynthesis&&window.speechSynthesis.cancel()}catch(e){}};w.o.onClose=cleanup;
 function finish(complete){if(done)return;done=true;cleanup();if(complete){text.textContent=rec.text+'\n[ЗАПИСЬ ОБОРВАНА]';text.classList.add('rec-ended');bar.style.width='100%';clock.textContent=`0:${pad(Math.ceil(rec.duration/1000))} / 0:${pad(Math.ceil(rec.duration/1000))}`;archRecordViewed(name);if(id===0){arch.viewed00=true;store.set('arch-viewed00',true)}}else{text.textContent+='\n[ВОСПРОИЗВЕДЕНИЕ ОСТАНОВЛЕНО]';text.classList.add('rec-ended')}cursor.remove()}
 $('.rec-close',w.body).onclick=()=>closeWin(w);$('.rec-stop',w.body).onclick=()=>finish(false);
 const titlebar=$('.rec-titlebar',w.body);titlebar.addEventListener('pointerdown',e=>{if(e.button!==0||e.target.closest('button'))return;e.preventDefault();focusWin(w);const x=e.clientX,y=e.clientY,ox=w.rect.x,oy=w.rect.y;titlebar.setPointerCapture(e.pointerId);const move=ev=>{w.rect.x=Math.max(0,Math.min(innerWidth-80,ox+ev.clientX-x));w.rect.y=Math.max(0,Math.min(innerHeight-85,oy+ev.clientY-y));applyRect(w)};const end=()=>{titlebar.removeEventListener('pointermove',move);titlebar.removeEventListener('pointerup',end);titlebar.removeEventListener('pointercancel',end)};titlebar.addEventListener('pointermove',move);titlebar.addEventListener('pointerup',end);titlebar.addEventListener('pointercancel',end)});
 // The frame handler doubles as the playback clock; typing and speech are independent.
 const frame=(now)=>{if(done||!wins.includes(w))return;let elapsed=Math.min(rec.duration,now-start);if(ctx&&now-lastFrame>30){lastFrame=now;drawRecScene(ctx,rec.scene,elapsed/1000)}bar.style.width=(elapsed/rec.duration*100)+'%';clock.textContent=`0:${pad(Math.floor(elapsed/1000))} / 0:${pad(Math.ceil(rec.duration/1000))}`;if(elapsed>=rec.duration){finish(true);return}raf=requestAnimationFrame(frame)};
 tickText=setInterval(()=>{if(index<rec.text.length){text.textContent+=rec.text[index++]}else clearInterval(tickText)},60);
 voiceTimer=setTimeout(()=>{if(done||!wins.includes(w))return;try{if(window.speechSynthesis&&window.SpeechSynthesisUtterance){const u=new SpeechSynthesisUtterance(rec.voice);u.lang='ru-RU';u.rate=.8;u.pitch=.6;window.speechSynthesis.speak(u)}}catch(e){}},1500);
 archLogEvent(`user открыл ${name}`);recSound(rec.scene);raf=requestAnimationFrame(frame);return w}

/* Local A.R.C.H. network: ten connected-looking sites, no HTTP requests. */
const siteLink=(host,label)=>`<a href="#" data-host="${esc(host)}">${esc(label||host)}</a>`;
function siteShell(host,title,body,crumb='Главная'){return `<div class="site-page t-site"><header class="t-header"><div class="t-logo">${esc(title)}</div><nav>${siteLink('tubbyhub.com','Сообщество')} · ${siteLink('tubbycraft.net','Форум')} · ${siteLink('tubby-news.ru','Новости')} · ${siteLink('archive.local','A.R.C.H.')}</nav></header><div class="t-crumb">${siteLink(host,host)} → ${esc(crumb)}</div><div class="t-content">${body}</div><footer class="t-footer">© ${esc(host)} · сохранённая локальная копия · 2012–03:33</footer></div>`}
const SITES={
 'tubbyhub.com':{title:'TubbyHub',html:()=>siteShell('tubbyhub.com','TubbyHub',`<h1>Друзья и знакомые <small>7 профилей</small></h1><div class="t-intro">Добро пожаловать в TubbyHub. Оставайтесь на связи, даже если связь потеряна.</div><div class="t-profiles">${[['Рон','2012'],['Тинки-Винки','2012'],['Дипси','2012'],['Ла-Ла','2012'],['По','2012'],['Ну-Ну','2012'],['Лейн','03:33 сегодня']].map(([n,time],i)=>`<button class="t-profile" data-profile="${esc(n)}"><span class="t-avatar">${esc(n[0])}</span><span><b>${esc(n)}</b><br><small class="${i===6?'t-danger':''}">последний вход: ${esc(time)}</small></span></button>`).join('')}</div><div class="t-hint">Онлайн: 1 · Лейн</div>`,'Профили')},
 'tubbyland.ru':{title:'Туббиленд',html:()=>siteShell('tubbyland.ru','Туббиленд',`<div class="t-hero"><h1>Добро пожаловать в Туббиленд!</h1><p>Официальные новости, друзья и правила безопасного пребывания.</p></div><h2>Объявления</h2><div class="t-news"><b>03:33 — Всё в порядке. Оставайтесь на местах</b><p>Администрация просит не покидать помещения до следующего сообщения.</p></div><div class="t-news"><b>2012 — Лес закрыт. Не заходите в лес</b><p>Проводятся технические работы. Маршрут будет открыт после проверки архивных материалов.</p></div><p>${siteLink('tubby-memories.ru','Список пропавших')} · ${siteLink('tubby-news.ru','Все новости')}</p>`,'Новости')},
 'tubbycraft.net':{title:'TubbyCraft Форум',html:()=>siteShell('tubbycraft.net','TubbyCraft',`<h1>Обсуждения сообщества</h1><div class="t-table-head">Тема <span>Ответов / Просмотров</span></div>${['Кто-нибудь видел Уайта?','Что случилось в 2012?','Не заходите в лес','observer — это кто?'].map((t,i)=>`<button class="t-thread-row" data-topic="${esc(t)}"><span class="t-avatar">${['У','2','Л','O'][i]}</span><span><b>${esc(t)}</b><small>Автор: ${i===3?'white':'ron'} · 03:33 сегодня</small></span><em>${33-i} / ${333-i*33}</em></button>`).join('')}<p class="t-hint">Последняя активность: 03:33 · Модератор: observer</p>`,'Темы форума')},
 'tubby-memories.ru':{title:'Мемориал Туббиленда',html:()=>siteShell('tubby-memories.ru','Мемориал',`<h1>Мы помним</h1><p>Имена не должны исчезнуть вместе с записями.</p><table class="t-table"><tr><th>Имя</th><th>Дата</th><th>Статус</th></tr>${['Рон','Тинки-Винки','Дипси','Ла-Ла','По','Ну-Ну','Уайт','Лейн'].map((n,i)=>`<tr class="${i>5?'t-danger':''}"><td>${esc(n)}</td><td>${i<6?'2012':'03:33 сегодня'}</td><td>${i===0?'пропал в лесу':i<6?'не найден':'пропал без вести'}</td></tr>`).join('')}</table><p class="t-hint">Последнее обновление реестра: сегодня в 03:33.</p>`,'Реестр')},
 'r33.gg':{title:'r33.gg',html:()=>siteShell('r33.gg','r33.gg',`<div class="t-warning"><h1>Правило 33</h1><p>Если этого нет в архиве — оно всё равно есть в архиве.</p><p>Сайт для взрослых. Вы не взрослый. Вы даже не он.</p><button class="site-btn" data-retry-r33="1">Повторить загрузку</button></div>`,'Ошибка 33')},
 'archive.local':{title:'A.R.C.H. Внутренний портал',html:()=>siteShell('archive.local','A.R.C.H.',`<div class="t-login"><h1>Вход в архив</h1><p>Подключение к локальному серверу сохранено с 03:33.</p><label>Логин<input class="t-login-user" autocomplete="off" placeholder="white"></label><label>Пароль<input class="t-login-pass" type="password" placeholder="••••"></label><button class="site-btn" data-arch-login="1">Войти</button><p class="t-login-result" aria-live="polite"></p></div>`,'Авторизация')},
 'tubbytube.com':{title:'TubbyTube',html:()=>siteShell('tubbytube.com','TubbyTube',`<h1>Популярные видео</h1><div class="t-videos">${[['Как испечь заварной крем','1.2М'],['Туббиленд: экскурсия 2012','890К'],['Что случилось в лесу?','33'],['Уайт: последнее видео','1'],['Не смотри это ночью','0, observer'],['Лейн — кто это?','???']].map(([name,count],i)=>`<button class="t-video" data-video="${esc(name)}"><span class="t-thumb"><span>▶</span><small>${i<2?'10:33':'03:33'}</small></span><b>${esc(name)}</b><small>Просмотров: ${esc(count)}</small></button>`).join('')}</div>`,'Видео')},
 'tubbysearch.ru':{title:'TubbySearch',html:()=>siteShell('tubbysearch.ru','TubbySearch',`<div class="t-search"><h1>Поиск по сохранённым страницам</h1><input class="t-search-input" placeholder="Что вы ищете?" value="Туббиленд"><button class="site-btn" data-tubby-search="1">Найти</button><div class="t-search-output"><h2>Результаты</h2>${[['Что случилось в 2012?','tubby-news.ru'],['observer — кто это?','tubbycraft.net'],['Лейн — кто это?','tubbyhub.com'],['Почему записи меняются?','archive.local']].map(([t,h])=>`<div class="t-search-hit">${siteLink(h,t)}<small>${esc(h)} · сохранённая копия</small></div>`).join('')}</div></div>`,'Поиск')},
 'tubby-pedia.ru':{title:'TubbyPedia',html:()=>siteShell('tubby-pedia.ru','TubbyPedia',`<div class="t-wiki"><h1>Туббиленд</h1><div class="t-wiki-box"><b>Туббиленд</b><br>Расположение: неизвестно<br>Архивное время: 03:33<br>Последняя перепись: 2012</div><p>Туббиленд — территория, упоминаемая в полевых журналах A.R.C.H. До 2012 года считалась безопасной. После исчезновения группы исследователей часть карт была изъята.</p><h2>История</h2><p>В 2012 году лес рядом с поселением закрыли. По официальной версии, причиной стали технические работы. На сохранившейся съёмке виден дом, которого не было на карте.</p><h2>Список пропавших</h2><p>Рон, Тинки-Винки, Дипси, Ла-Ла, По, Ну-Ну. Позднее добавлены Уайт и Лейн.</p><h2>См. также</h2>${siteLink('tubby-memories.ru','Мемориал')} · ${siteLink('tubbyland.ru','Официальные новости')} · ${siteLink('archive.local','Архив A.R.C.H.')}</div>`,'Статья: Туббиленд')},
 'tubby-news.ru':{title:'TubbyNews',html:()=>siteShell('tubby-news.ru','TubbyNews',`<h1>Последние новости</h1>${[['03:33 — Всё в порядке','Администрация сообщает, что беспокоиться не о чем. Оставайтесь на местах.'],['03:34 — Если вы читаете это — значит, вы ещё здесь','Время обновления страницы не совпадает с показаниями часов терминала.'],['2012 — Лес закрыт','Не заходите в лес. Возобновление доступа отложено на неопределённый срок.']].map(([t,v],i)=>`<button class="t-news-item" data-news="${i}"><span class="t-news-date">${i===2?'2012':'сегодня'}</span><b>${esc(t)}</b><p>${esc(v)}</p></button>`).join('')}<p>${siteLink('tubby-pedia.ru','История Туббиленда')}</p>`,'Лента')}
};
let archBrowserActive=null;
function openBrowser(startAddr){return appIE(startAddr)}
function ieGo(addr){if(!archBrowserActive||!wins.includes(archBrowserActive))openBrowser(addr);else{focusWin(archBrowserActive);archBrowserActive.ieGo(addr)}return archBrowserActive}
function ieBack(){if(archBrowserActive&&wins.includes(archBrowserActive))archBrowserActive.ieBack()}
function appIE(startAddr='about:blank'){const w=createWindow({app:'ie',title:'Internet Explorer 8 — A.R.C.H.',icon:'ie',w:920,h:600});archBrowserActive=w;
 w.body.innerHTML='<div class="ie-bar"><button class="ex-b arch-back" title="Назад">◀</button><span class="site-tab">▣ Internet Explorer 8</span><input class="arch-address" aria-label="Адрес"><button class="btn arch-go">Перейти</button><button class="btn arch-history">История</button><button class="btn arch-incognito">Инкогнито</button></div><div class="ie-fav arch-favs"></div><div class="ie-view" style="display:flex;min-height:0"><aside class="arch-hist" style="display:none"></aside><main class="arch-result"></main></div><div class="arch-ie-status">Готово · Локальная копия · Внешнее подключение отсутствует</div>';
 const page=$('.arch-result',w.body),hist=$('.arch-hist',w.body),address=$('.arch-address',w.body),back=$('.arch-back',w.body);let stack=[],pos=-1,current=null;
 const hostOf=raw=>{let s=String(raw||'').trim().toLowerCase().replace(/^https?:\/\//,'').replace(/^www\./,'');return s.split(/[\/?#]/)[0]};
 $('.arch-favs',w.body).innerHTML=['tubbyhub.com','tubbyland.ru','tubbycraft.net','tubby-memories.ru','archive.local','tubbytube.com','tubbysearch.ru','tubby-pedia.ru','tubby-news.ru','r33.gg'].map(h=>`<a href="#" data-host="${h}">${h}</a>`).join(' · ');
 function paint(entry){current=entry;page.scrollTop=0;address.value=entry.type==='site'?entry.addr:entry.q;back.disabled=pos<=0;
 if(entry.type==='site'){const host=hostOf(entry.addr),site=SITES[host];page.innerHTML=site?site.html():pageUnavailable(entry.addr,'Нет подключения к сети.');w.setTitle((site?site.title:'Сайт недоступен')+' — Internet Explorer 8');return}
 const {q,v}=entry;w.setTitle(q+' — Internet Explorer 8');
 if(v==='log'){launch('explorer',P_TEMP);launch('notepad',{path:P_TEMP,name:'observer.log'});page.innerHTML=pageArticle(q,'C:\\Windows\\Temp\\observer.log открыт в Блокноте.');return}
 if(v==='record'){page.innerHTML=pageArticle(q,'Файл существует. Открыть?')+'<div class="site-action"><button class="site-btn" data-site="records">Открыть «Записи»</button></div>';return}
 if(v==='table'){page.innerHTML=pageArticle(q,'Последняя запись: Уайт — 03:33 — пропал без вести.');return}
 if(v==='meme'){page.innerHTML=pageArticle(q,'Сохранённая картинка из архива.')+'<div class="site-action" style="width:210px;height:150px;background:linear-gradient(45deg,#f4ae3c,#91a6d4,#55bba1)"></div>';return}
 if(v==='silence'){page.innerHTML=pageUnavailable(q,'СМИХУЯТИНА');setTimeout(()=>{if(wins.includes(w)&&current===entry)page.innerHTML=pageUnavailable(q,'ТИШИНА')},1000);return}
 if(/принтер|камера|вебкамера|скрытые файлы/i.test(q)){page.innerHTML=pageForum(q,v);return}
 if(/протокол|observer\.log|архиве меняются/i.test(q)){page.innerHTML=pageArticle(q,v);return}
 page.innerHTML=pageSearch(q,v)}
 function push(entry){stack=stack.slice(0,pos+1);stack.push(entry);pos++;paint(entry)}
 w.ieGo=(addr)=>push({type:'site',addr:String(addr||'about:blank').trim()||'about:blank'});
 w.ieBack=()=>{if(pos>0){pos--;paint(stack[pos])}};
 function query(q,v){const special=q==='tubbyhub.com'||q==='r33.gg'||v==='portal';if(special){w.ieGo(v==='portal'?'archive.local':q);return}push({type:'query',q,v})}
 function renderHistory(){hist.innerHTML='';ARCH_HISTORY.forEach((group,i)=>{if(i===4&&!arch.viewed00)return;hist.append(el('h4','',`СЕССИЯ ${i+1}${i===4?' (без времени)':''}`));group.forEach(([q,v])=>{const b=el('button','',esc(q));b.onclick=()=>query(q,v);hist.append(b)})})}
 $('.arch-history',w.body).onclick=()=>{renderHistory();hist.style.display=hist.style.display==='none'?'block':'none'};$('.arch-incognito',w.body).onclick=()=>appCmd(true);back.onclick=w.ieBack;
 $('.arch-go',w.body).onclick=()=>w.ieGo(address.value);address.onkeydown=e=>{e.stopPropagation();if(e.key==='Enter')w.ieGo(address.value)};
 page.addEventListener('click',e=>{const a=e.target.closest('a,button');if(!a)return;if(a.matches('a'))e.preventDefault();
 if(a.dataset.host){w.ieGo(a.dataset.host);return}if(a.dataset.retryR33){archBSOD();return}
 if(a.dataset.archLogin){const u=$('.t-login-user',page)?.value.trim().toLowerCase(),p=$('.t-login-pass',page)?.value,result=$('.t-login-result',page);if(result)result.textContent=u==='white'&&p==='0333'?'Добро пожаловать, Уайт. Вас давно не было.':u==='lane'?'Лейн не зарегистрирован. Но он уже здесь.':'Неверный логин или пароль.';return}
 if(a.dataset.profile){const n=a.dataset.profile;const box=el('p','t-hint',`Профиль: ${esc(n)} · ${n==='Лейн'?'последний вход: 03:33 сегодня':'последний вход: 2012'}`);$('.t-content',page).append(box);return}
 if(a.dataset.topic){const q=a.dataset.topic;page.innerHTML=siteShell('tubbycraft.net','TubbyCraft',`<h1>${esc(q)}</h1><section class="site-post"><aside><div class="site-avatar">R</div><b>ron</b><small>Участник · 03:33</small></aside><div class="site-post-text">${esc(q)}<blockquote>Записи меняются, когда я не смотрю.</blockquote>Если кто-то ещё это видит — ответьте.</div></section><section class="site-post"><aside><div class="site-avatar">O</div><b>observer</b><small>Администратор · 03:33</small></aside><div class="site-post-text">Прочитано.</div></section>`,'Тема');return}
 if(a.dataset.video){const name=a.dataset.video;page.innerHTML=siteShell('tubbytube.com','TubbyTube',`<h1>${esc(name)}</h1><div class="t-player">▶<small>Видеофайл недоступен. Счётчик просмотров обновлён.</small></div><p>${siteLink('tubbytube.com','Вернуться к видео')}</p>`,'Просмотр');return}
 if(a.dataset.news!==undefined){let n=Number(a.dataset.news),texts=['03:33 — Всё в порядке','03:34 — Если вы читаете это — значит, вы ещё здесь','2012 — Лес закрыт'];page.innerHTML=siteShell('tubby-news.ru','TubbyNews',`<h1>${esc(texts[n])}</h1><p>Сохранённая заметка. Оставайтесь на местах. Не открывайте record_04.</p><p>${siteLink('tubby-news.ru','К ленте новостей')}</p>`,'Статья');return}
 if(a.dataset.tubbySearch){const text=$('.t-search-input',page)?.value||'Туббиленд';$('.t-search-output',page).insertAdjacentHTML('afterbegin',`<div class="t-hint">Запрос: ${esc(text)} · найдены локальные результаты</div>`);return}
 const act=a.dataset.site;if(!act)return;if(act==='home'){w.ieGo('archive.local')}else if(act==='retry-r33')archBSOD();else if(act==='records')launch('explorer',P_REC);else if(act==='login')w.ieGo('archive.local');else if(act==='result'){page.innerHTML=pageArticle(current?.q||'Архив',current?.v||'Страница сохранена.')}else if(act==='page'){page.innerHTML=pageSearch(current?.q||'Архив',current?.v||'Страница сохранена.')}else if(act==='search'){let q=$('.site-search-head input',page)?.value||'поиск';query(q,'Нет подключения к сети.')}else if(act==='reply'){const field=$('.site-reply textarea',page),txt=field?.value.trim();if(!txt)return;const line=el('div','site-comment',`<b>white</b> <small>03:33</small><p>${esc(txt)}</p>`);$('.site-reply',page).before(line);field.value='';$('.site-feedback',page).textContent='Ответ сохранён локально.'}});
 w.o.onClose=()=>{if(archBrowserActive===w)archBrowserActive=null};w.ieGo(startAddr);return w}

/* ================= init ================= */
applyTheme();applyWall();updVol();tick();setInterval(tick,1000);buildStart();renderDesktop();renderTasks();bootSeq();
</script>
</body>
</html>
