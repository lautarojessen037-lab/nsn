<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Wiki The Doors of the Purgatory</title>
<link rel="icon" id="favicon" href="data:,">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=VT323&display=swap" rel="stylesheet">
<style>
/* ==================== RESET + VARIABLES ==================== */
*{margin:0;padding:0;box-sizing:border-box;border-radius:0 !important}
:root{
  --fondo:#060b10;
  --panel:#0c141f;
  --panel2:#0e1a26;
  --borde:#3a5a78;
  --borde-osc:#06131c;
  --verde:#3fdc86;
  --verde-osc:#1f9e5c;
  --azul:#3b9eff;
  --oro:#f6b545;
  --rojo:#ff5d5d;
  --violeta:#7a5cff;
  --violeta-cl:#c9a2ff;
  --texto:#c9dcd6;
  --texto-suave:#8ba5ad;
  --pixel:'Press Start 2P',monospace;
  --fuente:'VT323',monospace;
}
html{scroll-behavior:smooth}
body{
  font-family:var(--fuente);font-size:21px;line-height:1.5;color:var(--texto);
  background:var(--fondo);overflow-x:hidden;
}
body.boot-activo{overflow:hidden}
body::before{
  content:"";position:fixed;inset:0;pointer-events:none;z-index:0;
  background-image:conic-gradient(rgba(255,255,255,.028) 25%,transparent 0 50%,rgba(255,255,255,.028) 0 75%,transparent 0);
  background-size:26px 26px;
}
::selection{background:var(--verde);color:#04140b}
::-webkit-scrollbar{width:14px}
::-webkit-scrollbar-track{background:#080d13}
::-webkit-scrollbar-thumb{background:var(--verde-osc);border:3px solid #060b10}

/* ==================== SCANLINES CRT ==================== */
.scanlines{position:fixed;inset:0;pointer-events:none;z-index:3000;
  background:repeating-linear-gradient(0deg,rgba(0,0,0,.13) 0 1px,transparent 1px 3px)}

/* ==================== ESTRELLAS DE FONDO ==================== */
#estrellas{position:fixed;inset:0;z-index:0;pointer-events:none;overflow:hidden}
.estrella{position:absolute;animation:titilar 2s steps(2) infinite}
@keyframes titilar{0%,100%{opacity:.9}50%{opacity:.08}}

/* ==================== SPRITES ==================== */
.px{display:inline-block;line-height:0;vertical-align:middle;flex-shrink:0}
.px svg{width:100%;height:100%;display:block}

/* ==================== ÍCONO WHATSAPP (PNG del canal) ==================== */
.wa-img{display:inline-block;vertical-align:middle;flex-shrink:0;line-height:0;
  image-rendering:pixelated;image-rendering:crisp-edges}
.wa-img.sm{height:22px;width:auto}
.wa-img.md{height:28px;width:auto}
.wa-img.lg{height:64px;width:auto}

/* ==================== ÍCONO CABALLERO SOMBRÍO (PNG) ==================== */
.espada-img{display:inline-block;vertical-align:middle;flex-shrink:0;line-height:0;
  image-rendering:pixelated;image-rendering:crisp-edges}
.espada-img.sm{height:22px;width:auto}
.espada-img.lg{height:64px;width:auto}

/* ==================== FLECHA SUBIR (PNG) ==================== */
.flecha-img{display:block;width:32px;height:32px;object-fit:contain;
  image-rendering:pixelated;image-rendering:crisp-edges}

/* ==================== BARRA DE PROGRESO (segmentada) ==================== */
.barra-progreso{position:fixed;top:0;left:0;right:0;height:12px;z-index:4000;
  background:#08121a;border-bottom:3px solid var(--borde-osc)}
.barra-relleno{height:100%;width:0;position:relative;
  background:repeating-linear-gradient(90deg,var(--verde) 0 8px,var(--verde-osc) 8px 16px);
  border-right:4px solid #fff;box-shadow:4px 0 0 var(--borde-osc)}

/* ==================== CABECERA ==================== */
.cabecera{position:sticky;top:0;z-index:1000;background:var(--fondo);
  border-bottom:3px solid var(--borde);box-shadow:0 4px 0 var(--borde-osc)}
.cabecera-inner{max-width:1100px;margin:auto;padding:12px 20px;
  display:flex;align-items:center;gap:14px}
@keyframes salto{0%,49%{transform:translateY(0)}50%,100%{transform:translateY(-4px)}}
/* puerta del logo: cerrada / abierta al hover */
.logo-puerta{position:relative;display:inline-block;line-height:0;
  animation:salto 1.6s step-end infinite}
.puerta-abierta{position:absolute;top:0;left:0;opacity:0;transition:opacity .12s steps(2)}
.logo-puerta:hover .puerta-cerrada{opacity:0;transition:opacity .12s steps(2)}
.logo-puerta:hover .puerta-abierta{opacity:1}
.titulo-header{display:flex;flex-direction:column;gap:5px}
.logo-juego{font-family:var(--pixel);font-size:clamp(7px,1.5vw,10px);color:var(--verde);
  line-height:1.5;text-shadow:2px 2px 0 #000}
.logo-wiki{font-family:var(--pixel);font-size:7px;color:var(--azul);letter-spacing:4px}

/* ==================== SECCIONES ==================== */
main{position:relative;z-index:1}
.seccion{max-width:1100px;margin:0 auto;padding:64px 20px 24px;position:relative}
.divisor{max-width:1040px;margin:0 auto;display:flex;align-items:center;gap:14px;padding:0 20px}
.divisor::before,.divisor::after{content:"";flex:1;height:4px;
  background:repeating-linear-gradient(90deg,var(--borde) 0 8px,transparent 8px 16px)}

h2.titulo-seccion{
  display:flex;align-items:center;gap:14px;flex-wrap:wrap;
  font-family:var(--pixel);font-size:clamp(10px,2vw,13px);color:#eaf6ee;
  background:var(--panel);border:2px solid var(--borde);border-left:8px solid var(--verde);
  box-shadow:0 0 0 3px var(--borde-osc),5px 5px 0 rgba(0,0,0,.45);
  padding:14px 16px;margin-bottom:28px;text-shadow:2px 2px 0 #000}
.titulo-nota{margin-left:auto;font-family:var(--pixel);font-size:7px;color:var(--azul);
  background:var(--azul-fondo,#0c1a2b);border:2px solid #2a4a6a;padding:6px 8px}

.caja{background:var(--panel);border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),6px 6px 0 rgba(0,0,0,.4);
  padding:24px}
.caja h3{display:flex;align-items:center;gap:10px;color:#eaf6ee;
  font-family:var(--pixel);font-size:10px;line-height:1.8;margin-bottom:14px}
.caja h3 .verde{color:var(--verde)}

/* ==================== BADGES DE ESTADO ==================== */
.estado{display:inline-flex;align-items:center;gap:6px;font-family:var(--pixel);font-size:7px;
  padding:5px 7px;border:2px solid;white-space:nowrap;line-height:1.4;vertical-align:middle}
.hecho{color:var(--verde);border-color:var(--verde);background:#0c2016}
.proceso{color:var(--oro);border-color:var(--oro);background:#241a06}
.descartado{color:var(--rojo);border-color:var(--rojo);background:#2a0f0f}
.pensando{color:var(--azul);border-color:var(--azul);background:#0c1a2b}
.indefinido{color:#93a6b4;border-color:#93a6b4;background:#141b22}
.estado.inflexion{color:var(--violeta-cl);border-color:var(--violeta);background:#170f2a}
kbd{font-family:var(--pixel);font-size:9px;color:#cfe6ff;background:#15222f;
  border:2px solid var(--borde);box-shadow:0 3px 0 var(--borde-osc),inset 0 2px 0 rgba(255,255,255,.07);
  padding:5px 7px;vertical-align:middle}

/* ==================== HERO ==================== */
.miga{font-size:19px;color:var(--texto-suave);margin-bottom:14px;text-transform:uppercase}
.miga::before{content:"> ";color:var(--verde)}
.miga::after{content:"█";color:var(--verde);animation:caret 1s steps(1) infinite;margin-left:4px}
@keyframes caret{50%{opacity:0}}
.hero h1{font-family:var(--pixel);font-size:clamp(13px,3.4vw,26px);color:#fff;line-height:1.8;
  text-shadow:3px 3px 0 #000;margin-bottom:16px}
.destacado{color:var(--verde)}
.hero-intro{max-width:780px;font-size:22px}
.hero-intro b{color:var(--verde)}
.chips{display:flex;gap:10px;flex-wrap:wrap;margin:22px 0 26px}
.chip{display:inline-flex;align-items:center;gap:8px;background:#0c1a2b;border:2px solid #2a4a6a;
  color:#a9d2ff;font-family:var(--pixel);font-size:8px;padding:8px 10px;
  box-shadow:3px 3px 0 rgba(0,0,0,.4)}
.chip:hover{animation:chip-menea .18s steps(1) infinite}
@keyframes chip-menea{0%,49%{transform:translate(0,0)}50%,100%{transform:translate(2px,-2px)}}
.hero-grid{display:grid;grid-template-columns:1.4fr 1fr;gap:18px;align-items:start}
.guia{counter-reset:paso;list-style:none}
.guia li{position:relative;padding:12px 12px 12px 54px;margin-bottom:10px;font-size:20px;
  background:rgba(255,255,255,.03);border:2px solid #1c2e3f;counter-increment:paso}
.guia li::before{content:counter(paso);position:absolute;left:12px;top:50%;transform:translateY(-50%);
  width:30px;height:30px;display:grid;place-items:center;font-family:var(--pixel);font-size:11px;
  color:#04140b;background:var(--verde);box-shadow:2px 2px 0 #000}
.toc{border:2px dashed var(--borde);background:#0a121b}
.toc a{display:flex;align-items:center;gap:10px;color:var(--texto);text-decoration:none;
  padding:7px 8px;font-size:21px;border-left:4px solid var(--borde)}
.toc a:hover{border-color:var(--verde);color:var(--verde);background:rgba(63,220,134,.06)}
.toc a:hover .px{animation:titilar .4s steps(1) infinite}
.sabias{margin-top:22px;display:flex;gap:14px;align-items:flex-start;flex-wrap:wrap;font-size:21px;
  background:#0c2016;border:2px solid var(--verde-osc);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc);
  border-left:8px solid var(--verde);padding:16px 18px}
.sabias strong{color:var(--verde);font-family:var(--pixel);font-size:8px;white-space:nowrap;
  display:flex;align-items:center;gap:10px;line-height:1.6}
.sabias .px{animation:titilar 3s steps(2) infinite}
#datoCurioso{transition:opacity .3s steps(3)}
.aviso{margin-top:14px;display:flex;gap:14px;align-items:flex-start;font-size:20px;
  background:#0c1a2b;border:2px solid var(--azul);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc);
  border-left:8px solid var(--azul);padding:14px 18px;color:var(--texto-suave)}
.aviso b{color:#bcdcff}
.aviso-inflexion{background:#170f2a;border-color:var(--violeta);border-left-color:var(--violeta)}
.aviso-inflexion b{color:var(--violeta-cl)}

/* ==================== LORE ==================== */
.lore-grid{display:grid;grid-template-columns:1.6fr .9fr;gap:18px;align-items:start}
.texto-lore p{margin-bottom:16px;font-size:22px}
.capital::first-letter{float:left;font-family:var(--pixel);font-size:44px;line-height:1.1;
  padding:6px 12px 0 0;color:var(--verde);text-shadow:2px 2px 0 #000}
.texto-lore blockquote{margin:18px 0;padding:12px 16px;border-left:6px solid var(--verde);
  background:#0c2016;border-top:2px solid #14301f;border-right:2px solid #14301f;
  border-bottom:2px solid #14301f;color:#bfe9d2;font-size:22px}
.infobox{background:var(--panel);border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),6px 6px 0 rgba(0,0,0,.4);
  min-width:0}
.infobox-titulo{background:var(--verde-osc);color:#fff;text-align:center;font-family:var(--pixel);
  font-size:11px;padding:14px;text-shadow:2px 2px 0 #000}
.infobox-sub{background:#0a1a12;color:var(--verde);font-family:var(--pixel);font-size:7px;
  padding:8px;letter-spacing:1px;text-transform:uppercase;border-bottom:2px solid var(--borde-osc)}
.infobox-imagen{display:grid;place-items:center;
  background:#000;
  border-bottom:2px solid var(--borde-osc);
  padding:16px 10px}
.infobox-imagen img{width:100%;height:auto;object-fit:contain;
  image-rendering:pixelated;image-rendering:crisp-edges}
.infobox table{width:100%;border-collapse:collapse;font-size:19px;table-layout:fixed}
.infobox td{padding:10px 12px;border-bottom:2px solid #1c2e3f;
  overflow-wrap:break-word;word-break:break-word;vertical-align:top}
.infobox td:first-child{color:var(--texto-suave);width:40%;text-transform:uppercase;font-size:17px}
.infobox td:last-child{color:#eaf6ee}

/* ==================== DIFICULTAD ==================== */
.rutas{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:18px;margin-bottom:18px}
.ruta-1{border-top:6px solid var(--verde)}
.ruta-2{border-top:6px solid var(--rojo)}
.ruta h3{font-family:var(--pixel);font-size:9px;margin-bottom:16px;
  display:flex;align-items:center;gap:10px}
.ruta-1 h3{color:var(--verde)}
.ruta-2 h3{color:var(--rojo)}
.modo{display:flex;gap:16px;align-items:flex-start;padding:14px;border:2px solid #1c2e3f;
  background:rgba(255,255,255,.03);margin-bottom:12px}
.modo:last-child{margin-bottom:0}
.modo > .px{margin-top:4px}
.modo-cuerpo{flex:1;min-width:0}
.modo h4{color:#eaf6ee;font-size:24px;display:flex;justify-content:space-between;gap:10px;
  align-items:center;flex-wrap:wrap;line-height:1.2}
.modo p{font-size:19px;color:var(--texto-suave)}
.vidas{display:flex;flex-wrap:wrap;gap:4px;margin:10px 0 6px;align-items:center}
.vidas .txt{font-family:var(--pixel);font-size:7px;color:var(--texto-suave);margin-left:8px}
.late{animation:latido 1.2s steps(2) infinite}
@keyframes latido{0%,100%{transform:scale(1)}50%{transform:scale(1.2)}}
.nota-dif{border-left:8px solid var(--oro);font-size:21px}
.nota-dif b{color:var(--oro)}
.nota-dif i{color:var(--texto-suave)}

/* ==================== JEFES ==================== */
.leyenda{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:24px}
.jefes-destacados{display:grid;grid-template-columns:repeat(auto-fit,minmax(235px,1fr));gap:16px;margin-bottom:26px}
.carta-jefe{position:relative;background:var(--panel);border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),5px 5px 0 rgba(0,0,0,.4);
  padding:20px;transition:transform .15s steps(2),box-shadow .15s steps(2)}
.carta-jefe:hover{transform:translate(-3px,-3px);
  border-color:var(--verde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--verde-osc),9px 9px 0 rgba(0,0,0,.5)}
.carta-jefe.jefe-inflexion{border-top:6px solid var(--violeta)}
.carta-jefe.jefe-inflexion:hover{border-color:var(--violeta)}
.puerta{position:absolute;top:10px;right:10px;font-family:var(--pixel);font-size:6px;color:var(--azul);
  background:#0c1a2b;border:2px solid #2a4a6a;padding:5px 6px}
.icono-jefe{display:block;margin-bottom:12px}
.carta-jefe h3{color:#eaf6ee;font-family:var(--pixel);font-size:10px;margin-bottom:8px;line-height:1.6}
.carta-jefe.jefe-inflexion h3{color:var(--violeta-cl)}
.desc-jefe{font-size:19px;color:var(--texto-suave);margin-bottom:12px;min-height:58px}
.mas-puertas{display:flex;gap:18px;align-items:flex-start;border-top:6px solid var(--azul)}
.mas-puertas > .px{flex-shrink:0;margin-top:4px;animation:salto 1.8s step-end infinite}
.mas-puertas h3{color:var(--azul)}
.mas-puertas p{font-size:19px;color:var(--texto-suave)}
.mas-puertas p b{color:#a9d2ff}
.puertas-pendientes{display:flex;flex-wrap:wrap;gap:8px;margin-top:14px}
.puerta-chip{font-family:var(--pixel);font-size:7px;color:#93a6b4;border:2px dashed var(--borde);
  padding:6px 8px;background:rgba(255,255,255,.02)}
.tabla-wrap{overflow-x:auto;border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc);background:var(--panel)}
.tabla-wrap table{width:100%;border-collapse:collapse;font-size:19px;min-width:680px}
.tabla-wrap thead th{background:#123522;color:var(--verde);font-family:var(--pixel);font-size:8px;
  padding:12px 14px;border:2px solid #1c2e3f;text-align:left;letter-spacing:1px}
.tabla-wrap tbody td{padding:11px 14px;border:2px solid #16232f;vertical-align:middle}
.tabla-wrap tbody tr:nth-child(odd){background:rgba(255,255,255,.028)}
.tabla-wrap tbody tr:hover{background:#0c2016}
td.num{font-family:var(--pixel);font-size:9px;color:var(--azul);text-align:center;white-space:nowrap}
.celda-jefe{display:flex;align-items:center;gap:10px}
.nombre-jefe{color:#eaf6ee}
.fila-misterio td{color:#6d8291}

/* ==================== MECÁNICAS ==================== */
.mecanicas-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:16px}
.mecanica{background:var(--panel);border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),5px 5px 0 rgba(0,0,0,.4);
  padding:20px;transition:transform .15s steps(2)}
.mecanica:hover{transform:translate(-3px,-3px)}
.mecanica.e-hecho{border-top:6px solid var(--verde)}
.mecanica.e-descartado{border-top:6px solid var(--rojo);opacity:.75}
.mecanica.e-pensando{border-top:6px solid var(--azul)}
.mec-cabecera{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px;
  min-height:48px}
.mecanica h3{color:#eaf6ee;font-family:var(--pixel);font-size:9px;margin-bottom:8px;line-height:1.7}
.mecanica p{font-size:19px;color:var(--texto-suave)}

/* ==================== MAPAS ==================== */
.mapas-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:16px;margin-bottom:18px}
.mapa-caja{background:var(--panel);border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),5px 5px 0 rgba(0,0,0,.4);
  padding:20px;display:flex;gap:16px;align-items:flex-start}
.mapa-positivo{border-top:6px solid var(--verde)}
.mapa-negativo{border-top:6px solid var(--rojo)}
.mapa-caja h3{color:#eaf6ee;font-family:var(--pixel);font-size:9px;margin-bottom:8px;line-height:1.7}
.mapa-caja p{font-size:19px;color:var(--texto-suave)}

/* ==================== WHATSAPP ==================== */
.whatsapp-caja{background:#0e7d63;border:2px solid #25D366;
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px #062c1e,8px 8px 0 rgba(0,0,0,.45);
  padding:28px 24px}
.wa-contenido{display:flex;gap:22px;align-items:center;flex-wrap:wrap}
.wa-icono{flex-shrink:0;padding:14px;background:#25D366;border:3px solid #062c1e;
  box-shadow:inset -5px -5px 0 #1a9e4f,inset 5px 5px 0 #6fe89b;animation:salto 1.8s step-end infinite}
.wa-texto{flex:1;min-width:230px}
.wa-texto h3{color:#fff;font-family:var(--pixel);font-size:11px;margin-bottom:10px;
  text-shadow:2px 2px 0 #000;line-height:1.7}
.wa-texto p{color:#d3f3e4;font-size:21px}
.wa-texto b{color:#8ff0bb}
.wa-btn{display:inline-flex;align-items:center;gap:14px;margin-top:22px;background:#25D366;
  color:#04220f;font-family:var(--pixel);font-size:9px;text-decoration:none;
  border:3px solid #0a3d24;padding:16px 20px;line-height:1.6;
  box-shadow:inset -5px -5px 0 #1a9e4f,inset 5px 5px 0 #6fe89b,5px 5px 0 #000;
  transition:transform .1s steps(1),box-shadow .1s steps(1)}
.wa-btn:hover{transform:translate(2px,2px);
  box-shadow:inset -5px -5px 0 #1a9e4f,inset 5px 5px 0 #6fe89b,3px 3px 0 #000}
.wa-btn:active{transform:translate(5px,5px);
  box-shadow:inset -5px -5px 0 #1a9e4f,inset 5px 5px 0 #6fe89b}
.wa-link{margin-top:14px;font-size:17px;color:#9fd8c2;opacity:.85;word-break:break-all}

/* ==================== ESTADÍSTICAS ==================== */
.fecha{color:var(--azul);font-size:20px;margin-bottom:16px}
.stat-lineas div{display:flex;justify-content:space-between;gap:12px;padding:9px 2px;font-size:20px;
  background-image:repeating-linear-gradient(90deg,#2a3947 0 4px,transparent 4px 8px);
  background-size:100% 2px;background-position:bottom;background-repeat:no-repeat}
.stat-lineas span{color:var(--texto-suave)}
.stat-lineas b{color:#eaf6ee}
.stat-lineas .verde{color:var(--verde)}

/* ==================== FOOTER + CRÉDITOS ==================== */
footer{border-top:4px solid var(--borde);background:var(--fondo);margin-top:70px;position:relative;z-index:1}
.footer-inner{max-width:1100px;margin:auto;padding:36px 20px;text-align:center}
.footer-logo{display:flex;justify-content:center;align-items:center;gap:12px;
  font-family:var(--pixel);font-size:8px;color:var(--verde);margin-bottom:18px;line-height:1.8}
.footer-logo span{color:var(--azul)}
.creditos{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:14px;
  max-width:720px;margin:0 auto 20px}
.credito{display:flex;align-items:center;gap:14px;background:var(--panel);
  border:2px solid var(--borde);
  box-shadow:0 0 0 3px var(--borde-osc),inset 0 0 0 2px var(--borde-osc),4px 4px 0 rgba(0,0,0,.4);
  padding:14px 16px;text-align:left}
.credito > .px{flex-shrink:0}
.credito-rol{display:block;font-family:var(--pixel);font-size:6px;color:var(--texto-suave);
  margin-bottom:6px;letter-spacing:1px}
.credito-nombre{display:block;font-family:var(--pixel);font-size:9px;line-height:1.5}
.credito-nombre.verde{color:var(--verde)}
.credito-nombre.azul{color:var(--azul)}
footer p{font-size:19px;color:var(--texto-suave);margin-bottom:8px}
.licencia b{color:#a9d2ff}
.afiliados{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin:18px 0 6px}
.afiliado{display:inline-flex;align-items:center;gap:8px;border:2px solid var(--borde);
  background:var(--panel);font-family:var(--pixel);font-size:7px;color:var(--texto);padding:10px 12px;
  box-shadow:3px 3px 0 rgba(0,0,0,.4)}

/* ==================== BOTÓN SUBIR ==================== */
.btn-subir{position:fixed;bottom:24px;right:24px;width:52px;height:52px;border:3px solid #06231a;
  background:var(--verde);display:grid;place-items:center;z-index:900;
  box-shadow:inset -4px -4px 0 var(--verde-osc),inset 4px 4px 0 #8ff0bb,5px 5px 0 #000;
  opacity:0;pointer-events:none;transition:opacity .3s steps(3),transform .1s steps(1)}
.btn-subir.visible{opacity:1;pointer-events:auto}
.btn-subir:hover{transform:translate(2px,2px);
  box-shadow:inset -4px -4px 0 var(--verde-osc),inset 4px 4px 0 #8ff0bb,3px 3px 0 #000}
.btn-subir:active{transform:translate(5px,5px);
  box-shadow:inset -4px -4px 0 var(--verde-osc),inset 4px 4px 0 #8ff0bb}

/* ==================== ANIMACIÓN REVEAL ==================== */
.reveal{opacity:0;transform:translateY(24px);
  transition:opacity .45s steps(4),transform .45s steps(4);transition-delay:var(--d,0s)}
.reveal.visible{opacity:1;transform:translateY(0)}

/* ============================================================
   ============ ANIMACIONES (todo a steps) ============
   ============================================================ */

/* --- GLITCH: título del héroe --- */
.hero h1{animation:glitch-titulo 3.6s steps(1) infinite}
@keyframes glitch-titulo{
  0%,88%{text-shadow:3px 3px 0 #000;transform:translate(0,0)}
  89%{text-shadow:-3px 0 var(--rojo),3px 3px 0 #000;transform:translate(2px,0)}
  90%{text-shadow:3px 0 var(--azul),3px 3px 0 #000;transform:translate(-2px,1px)}
  91%{text-shadow:-2px 0 var(--rojo),3px 3px 0 #000;transform:translate(1px,-1px)}
  92%,100%{text-shadow:3px 3px 0 #000;transform:translate(0,0)}
}

/* --- GLITCH: nombre de MIRROR (carta) --- */
.carta-jefe.jefe-inflexion h3{animation:glitch-mirror 4.4s steps(1) infinite}
@keyframes glitch-mirror{
  0%,84%{text-shadow:none;transform:translate(0,0)}
  85%{text-shadow:-3px 0 var(--violeta),3px 0 var(--azul);transform:translate(2px,0)}
  86%{text-shadow:3px 0 var(--violeta-cl),-2px 0 var(--rojo);transform:translate(-2px,0)}
  87%{text-shadow:2px 0 var(--violeta),0 0 0 #000;transform:translate(1px,0)}
  88%,100%{text-shadow:none;transform:translate(0,0)}
}

/* --- TEMBLOR 2-FRAMES: sprites de jefes al hover --- */
.carta-jefe:hover .icono-jefe{animation:temblor-sprite .24s steps(1) infinite}
@keyframes temblor-sprite{
  0%,49%{transform:translate(0,0);filter:none}
  50%,100%{transform:translate(2px,-2px);filter:brightness(1.35) saturate(1.4)}
}

/* --- BOB FLOTANTE: íconos de las cartas (steps, desfasado por carta) --- */
.carta-jefe .icono-jefe{animation:flotar-sprite 1.3s steps(1) infinite}
.carta-jefe:nth-child(2n) .icono-jefe{animation-duration:1.7s;animation-delay:.4s}
.carta-jefe:nth-child(3n) .icono-jefe{animation-duration:1.1s;animation-delay:.15s}
.carta-jefe:nth-child(5n) .icono-jefe{animation-duration:1.5s;animation-delay:.6s}
@keyframes flotar-sprite{
  0%,49.9%{transform:translateY(0)}
  50%,100%{transform:translateY(-5px)}
}

/* --- DAÑO: corazones al hacer click --- */
.vidas.dano{animation:vida-shake .4s steps(5)}
@keyframes vida-shake{
  0%,100%{transform:translateX(0)}
  20%{transform:translateX(-5px)}
  40%{transform:translateX(5px)}
  60%{transform:translateX(-3px)}
  80%{transform:translateX(3px)}
}
.vidas.dano .px{animation:vida-flash .16s steps(1) infinite}
@keyframes vida-flash{
  0%,49%{filter:none}
  50%,100%{filter:brightness(2.2) saturate(0)}
}
.vidas .px.apagado{filter:grayscale(1) brightness(.35)}

/* --- CENIZA DIGITAL cayendo en el héroe --- */
.ceniza{position:absolute;inset:0;overflow:hidden;pointer-events:none}
.hero > *:not(.ceniza){position:relative;z-index:1}
.copo{position:absolute;top:-4px;
  animation-name:caer;animation-timing-function:steps(24);animation-iteration-count:infinite}
@keyframes caer{
  0%{transform:translate(0,0);opacity:0}
  6%{opacity:1}
  90%{opacity:.9}
  100%{transform:translate(-32px,105vh);opacity:0}
}

/* --- BARRA DE PROGRESO: borde tipo consola (parpadeo) --- */
.barra-relleno{animation:parpadeo-borde .56s steps(1) infinite}
@keyframes parpadeo-borde{
  0%,49%{border-right-color:#fff;box-shadow:4px 0 0 var(--borde-osc),0 0 8px rgba(63,220,134,.55)}
  50%,100%{border-right-color:var(--verde);box-shadow:4px 0 0 var(--borde-osc)}
}

/* --- DEMO DE TECLAS: Z y X se presionan solas en la guía --- */
.guia li:nth-child(2) kbd:first-of-type{animation:kbd-demo 2.8s steps(1) infinite}
.guia li:nth-child(2) kbd:last-of-type{animation:kbd-demo 2.8s steps(1) 1.4s infinite}
@keyframes kbd-demo{
  0%,34%{transform:translateY(0);box-shadow:0 3px 0 var(--borde-osc),inset 0 2px 0 rgba(255,255,255,.07)}
  35%,49%{transform:translateY(3px);box-shadow:0 0 0 var(--borde-osc),inset 0 2px 0 rgba(255,255,255,.07)}
  50%,100%{transform:translateY(0);box-shadow:0 3px 0 var(--borde-osc),inset 0 2px 0 rgba(255,255,255,.07)}
}

/* ============================================================
   ============ ANIMACIONES NUEVAS (ronda 2) ============
   ============================================================ */

/* --- A. PANTALLA DE ARRANQUE (boot CRT) --- */
#boot{position:fixed;inset:0;z-index:5000;background:var(--fondo);
  display:grid;place-items:center;cursor:pointer}
.boot-centro{display:flex;flex-direction:column;align-items:center;gap:18px;
  animation:boot-flicker .8s steps(1) .15s backwards}
@keyframes boot-flicker{0%{opacity:0}10%{opacity:1}20%{opacity:.2}30%{opacity:1}45%{opacity:.4}60%,100%{opacity:1}}
.boot-puerta{animation:salto 1.6s step-end infinite}
.boot-logo{font-family:var(--pixel);font-size:clamp(11px,3vw,20px);color:var(--verde);
  text-shadow:3px 3px 0 #000;text-align:center;line-height:1.8}
.boot-sub{font-family:var(--pixel);font-size:9px;color:var(--azul);letter-spacing:8px}
.boot-barra{width:230px;height:16px;border:2px solid var(--borde);
  box-shadow:0 0 0 2px var(--borde-osc);background:#08121a;padding:2px}
.boot-relleno{height:100%;width:0;
  background:repeating-linear-gradient(90deg,var(--verde) 0 8px,var(--verde-osc) 8px 16px);
  animation:boot-carga 1.4s steps(12) .35s forwards}
@keyframes boot-carga{to{width:100%}}
.boot-txt{font-family:var(--pixel);font-size:8px;color:var(--texto-suave);
  animation:parpadeo-suave .5s steps(1) infinite}
@keyframes parpadeo-suave{50%{opacity:.25}}
.boot-skip{position:absolute;bottom:26px;left:0;right:0;text-align:center;
  font-family:var(--pixel);font-size:7px;color:#5a6a75;
  animation:parpadeo-suave .9s steps(1) infinite}
/* ráfaga de estática al cerrar el boot (cambio de canal) */
#boot.boot-ruido::after{content:"";position:absolute;inset:0;opacity:.55;
  background:
    repeating-linear-gradient(0deg,rgba(255,255,255,.12) 0 1px,transparent 1px 3px),
    repeating-linear-gradient(90deg,rgba(255,255,255,.10) 0 1px,transparent 1px 2px),
    conic-gradient(rgba(255,255,255,.16) 25%,transparent 0 50%,rgba(255,255,255,.16) 0 75%,transparent 0);
  background-size:100% 100%,100% 100%,5px 5px}

/* --- B. CHISPAS PIXEL al hacer click (elementos JS) --- */
.chispa{position:fixed;z-index:3500;pointer-events:none;
  box-shadow:1px 1px 0 rgba(0,0,0,.4)}

/* --- C. MOTITAS de polvo detrás del cursor (elementos JS) --- */
.motita{position:fixed;z-index:3500;pointer-events:none}

/* --- D. TOAST DEL CÓDIGO KONAMI --- */
.konami-toast{position:fixed;top:70px;left:50%;transform:translateX(-50%);z-index:4500;
  background:var(--panel);border:2px solid var(--verde);
  box-shadow:0 0 0 3px var(--borde-osc),6px 6px 0 rgba(0,0,0,.5);
  font-family:var(--pixel);font-size:10px;color:var(--verde);text-align:center;
  padding:16px 22px;line-height:2;text-shadow:2px 2px 0 #000;
  animation:toast-in .25s steps(3),toast-out .3s steps(3) 2.8s forwards}
@keyframes toast-in{from{opacity:0;transform:translateX(-50%) translateY(-16px)}
  to{opacity:1;transform:translateX(-50%) translateY(0)}}
@keyframes toast-out{to{opacity:0;transform:translateX(-50%) translateY(-16px)}}
.konami-corazon{position:fixed;z-index:4400;pointer-events:none}

/* --- E. TÍTULOS DE SECCIÓN: se "encienden" como tubo fluorescente --- */
.titulo-seccion.visible{animation:encender .55s steps(1) 1}
@keyframes encender{
  0%{opacity:.15}
  20%{opacity:.85}
  30%{opacity:.25}
  45%{opacity:1}
  55%{opacity:.4}
  70%,100%{opacity:1}
}

/* --- F. FILAS DE LA TABLA en cascada --- */
.tabla-wrap.visible tbody tr{animation:fila-entra .28s steps(3) backwards}
.tabla-wrap tbody tr:nth-child(1){animation-delay:.04s}
.tabla-wrap tbody tr:nth-child(2){animation-delay:.09s}
.tabla-wrap tbody tr:nth-child(3){animation-delay:.14s}
.tabla-wrap tbody tr:nth-child(4){animation-delay:.19s}
.tabla-wrap tbody tr:nth-child(5){animation-delay:.24s}
.tabla-wrap tbody tr:nth-child(6){animation-delay:.29s}
.tabla-wrap tbody tr:nth-child(7){animation-delay:.34s}
.tabla-wrap tbody tr:nth-child(8){animation-delay:.39s}
.tabla-wrap tbody tr:nth-child(9){animation-delay:.44s}
.tabla-wrap tbody tr:nth-child(10){animation-delay:.49s}
.tabla-wrap tbody tr:nth-child(11){animation-delay:.54s}
.tabla-wrap tbody tr:nth-child(12){animation-delay:.59s}
.tabla-wrap tbody tr:nth-child(13){animation-delay:.64s}
@keyframes fila-entra{from{opacity:0;transform:translateX(-14px)}to{opacity:1;transform:none}}

/* --- G. PASOS DE LA GUÍA aparecen en secuencia --- */
.reveal.visible .guia li{animation:paso-pop .3s steps(3) backwards}
.guia li:nth-child(1){animation-delay:.12s}
.guia li:nth-child(2){animation-delay:.26s}
.guia li:nth-child(3){animation-delay:.4s}
.guia li:nth-child(4){animation-delay:.54s}
@keyframes paso-pop{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}

/* ==================== RESPONSIVE ==================== */
@media(max-width:860px){
  .hero-grid,.lore-grid{grid-template-columns:1fr}
  .infobox{max-width:420px;margin:0 auto;width:100%}
}
@media(max-width:560px){
  .seccion{padding:52px 14px 20px}
  .logo-wiki{letter-spacing:2px}
  .wa-contenido{flex-direction:column;text-align:center}
  .modo{flex-direction:column}
  .mas-puertas{flex-direction:column}
  /* botón subir en teléfonos: 86% de la pantalla, abajo pero sin tocar el borde */
  .btn-subir{bottom:auto;top:86%;margin-top:-26px;right:16px}
}
/* Desactiva TODAS las animaciones y transiciones (incluye las nuevas) */
@media(prefers-reduced-motion:reduce){
  *{animation:none !important;transition:none !important}
  .reveal{opacity:1;transform:none}
  #boot{display:none}
}
</style>
</head>
<body>

<!-- ==================== PANTALLA DE ARRANQUE ==================== -->
<div id="boot" aria-hidden="true">
  <div class="boot-centro">
    <span class="px boot-puerta" data-sprite="puerta" data-escala="5"></span>
    <div class="boot-logo">THE DOORS OF<br>THE PURGATORY</div>
    <div class="boot-sub">WIKI</div>
    <div class="boot-barra"><div class="boot-relleno"></div></div>
    <div class="boot-txt">CARGANDO WIKI...</div>
  </div>
  <div class="boot-skip">CLIC PARA SALTAR</div>
</div>

<div class="scanlines" aria-hidden="true"></div>
<div id="estrellas" aria-hidden="true"></div>
<div class="barra-progreso"><div class="barra-relleno" id="barraRelleno"></div></div>

<!-- ==================== CABECERA ==================== -->
<header class="cabecera">
  <div class="cabecera-inner">
    <span class="logo-puerta">
      <span class="px puerta-cerrada" data-sprite="puerta" data-escala="3"></span>
      <span class="px puerta-abierta" data-sprite="puertaAbierta" data-escala="3"></span>
    </span>
    <div class="titulo-header">
      <span class="logo-juego">THE DOORS OF THE PURGATORY</span>
      <span class="logo-wiki">WIKI</span>
    </div>
  </div>
</header>

<main>

<!-- ==================== INICIO ==================== -->
<section id="inicio" class="seccion hero">
  <div class="ceniza" aria-hidden="true"></div>
  <p class="miga reveal">wiki_the_doors / página_principal</p>
  <h1 class="reveal">¡BIENVENID@ A LA <span class="destacado">WIKI</span>!</h1>
  <p class="hero-intro reveal" style="--d:.05s">
    La enciclopedia en español sobre <b>The Doors of the Purgatory</b>, el juego de acción en
    desarrollo donde un caballero condenado debe sobrevivir a las 21 puertas del purgatorio.
    Aquí encontrarás todo sobre su <b>lore</b>, sus <b>22 jefes</b>, sus <b>mecánicas</b> y sus
    <b>rutas de dificultad</b>.
  </p>
  <div class="chips reveal" style="--d:.1s">
    <span class="chip"><span class="px" data-sprite="puerta" data-escala="1.4"></span>21 PUERTAS</span>
    <span class="chip"><span class="px" data-sprite="calavera" data-escala="1.4"></span>22 JEFES</span>
    <span class="chip"><span class="px" data-sprite="bandera" data-escala="1.4"></span>2 RUTAS</span>
    <span class="chip"><span class="px" data-sprite="reloj" data-escala="1.4"></span>1-2 HS</span>
    <span class="chip"><span class="px" data-sprite="rayo" data-escala="1.4"></span>DIFICULTAD MUY ALTA</span>
  </div>

  <div class="hero-grid">
    <div class="caja reveal">
      <h3><span class="px" data-sprite="libro" data-escala="2.2"></span><span class="verde">GUÍA DEL PRINCIPIANTE</span></h3>
      <ol class="guia">
        <li>Elige tu ruta: <b>Normal</b>, <b>Medio</b> o <b>Difícil</b>. Cada una cambia tus vidas y tu escudo.</li>
        <li>Domina el <kbd>Z</kbd> (Dash) y la <kbd>X</kbd> (Presión de Caballero): son tu supervivencia.</li>
        <li>Recuerda la regla de oro: no tienes que matar a los dioses… tienes que <b>sobrevivirlos</b>.</li>
        <li>Cruza las 21 puertas del purgatorio. <i>Si es que puedes.</i></li>
      </ol>
    </div>
    <aside class="caja toc reveal" style="--d:.1s">
      <h3>CONTENIDO</h3>
      <a href="#lore"><span class="px" data-sprite="play" data-escala="1.6"></span>Lore del juego</a>
      <a href="#dificultad"><span class="px" data-sprite="play" data-escala="1.6"></span>Rutas y dificultad</a>
      <a href="#jefes"><span class="px" data-sprite="play" data-escala="1.6"></span>Jefes del juego</a>
      <a href="#jugabilidad"><span class="px" data-sprite="play" data-escala="1.6"></span>Jugabilidad y mecánicas</a>
      <a href="#mapas"><span class="px" data-sprite="play" data-escala="1.6"></span>Mapas con efectos</a>
      <a href="#comunidad"><span class="px" data-sprite="play" data-escala="1.6"></span>Únete a la comunidad</a>
    </aside>
  </div>

  <div class="sabias reveal">
    <strong><span class="px" data-sprite="bombilla" data-escala="2.4"></span>¿SABÍAS QUE...?</strong>
    <span id="datoCurioso"></span>
  </div>

  <div class="aviso reveal">
    <span class="px" data-sprite="signo" data-escala="2.6"></span>
    <span><b>Wiki en construcción.</b> The Doors of the Purgatory se encuentra en desarrollo activo:
    parte de la información de esta página puede cambiar con el tiempo.</span>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== LORE ==================== -->
<section id="lore" class="seccion">
  <h2 class="titulo-seccion reveal">
    <span class="px" data-sprite="libro" data-escala="2.4"></span>LORE DEL JUEGO
  </h2>
  <div class="lore-grid">
    <article class="caja texto-lore reveal">
      <p class="capital">Un caballero llamado <b style="color:var(--verde)">Slash</b> se encuentra convaleciente
      tras la guerra contra los dioses. Después de <b>21 batallas</b> contra ellos, muere a manos del
      <b>Dios Supremo</b>… pero él se niega a morir.</p>
      <p>Su determinación llama la atención de un <b>ser superior</b>, quien le ofrece un trato:</p>
      <blockquote>«Pasa mis desafíos y te traeré de vuelta, con el poder suficiente para lograr lo que no pudiste hacer.»</blockquote>
      <p>Slash acepta, y es condenado a cruzar las <b>21 puertas del purgatorio</b>, cada una guardada por
      un dios que él mismo derrotó en la guerra. Pero su misión no es matar:</p>
      <blockquote>«Tu misión no es matar. Es <b style="color:var(--verde)">sobrevivir</b>.» — La condición del trato.</blockquote>
      <p style="margin-bottom:0">Así, Slash despierta en el purgatorio, a punto de iniciar su desafío…</p>
      <div class="aviso aviso-inflexion reveal" style="margin-top:18px">
        <span class="px" data-sprite="mirror" data-escala="2.6"></span>
        <span><b>El punto de inflexión — Puerta 14:</b> al derrotar a <b>Mirror</b>, el remordimiento y la
        determinación transforman a Slash en una nueva forma. De ahí en adelante, el camino solo trae
        sufrimiento: el tono del resto del juego cambia para siempre.</span>
      </div>
    </article>

    <aside class="infobox reveal" style="--d:.1s">
      <div class="infobox-titulo">SLASH</div>
      <div class="infobox-sub">El caballero condenado</div>
      <div class="infobox-imagen">
        <img src="https://i.imgur.com/5PFiBy6.jpeg" alt="Slash, el caballero condenado">
      </div>
      <table>
        <tr><td>Rol</td><td>Caballero</td></tr>
        <tr><td>Estado</td><td>Condenado al purgatorio</td></tr>
        <tr><td>Objetivo</td><td>Sobrevivir las 21 puertas</td></tr>
        <tr><td>Habilidades</td><td>Dash · Presión de Caballero</td></tr>
        <tr><td>Enemigos</td><td>Los 21 dioses y el Dios Supremo</td></tr>
        <tr><td>Causa de muerte</td><td>La guerra contra los dioses</td></tr>
        <tr><td>Rutas</td><td>Ruta 1 y Ruta 2</td></tr>
      </table>
    </aside>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== DIFICULTAD ==================== -->
<section id="dificultad" class="seccion">
  <h2 class="titulo-seccion reveal">
    <span class="px" data-sprite="bandera" data-escala="2.4"></span>RUTAS Y DIFICULTAD
  </h2>
  <div class="rutas">
    <div class="caja ruta ruta-1 reveal">
      <h3><span class="px" data-sprite="play" data-escala="1.6"></span>RUTA 1</h3>
      <div class="modo">
        <span class="px" data-sprite="escudo" data-escala="3.4"></span>
        <div class="modo-cuerpo">
          <h4>Modo Normal <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></h4>
          <div class="vidas" data-corazones="15"></div>
          <p>Escudo completo y 15 vidas. La forma recomendada de afrontar el purgatorio por primera vez.</p>
        </div>
      </div>
      <div class="modo">
        <span class="px" data-sprite="escudoRoto" data-escala="3.4"></span>
        <div class="modo-cuerpo">
          <h4>Modo Medio <span class="estado proceso"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN PROCESO</span></h4>
          <div class="vidas" data-corazones="7"></div>
          <p>Escudo roto y 7 vidas. Los dioses no perdonan tanto.</p>
        </div>
      </div>
    </div>
    <div class="caja ruta ruta-2 reveal" style="--d:.1s">
      <h3><span class="px" data-sprite="calavera" data-escala="2"></span>RUTA 2</h3>
      <div class="modo">
        <span class="px" data-sprite="calavera" data-escala="3.4"></span>
        <div class="modo-cuerpo">
          <h4>Modo Difícil <span class="estado proceso"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN PROCESO</span></h4>
          <div class="vidas">
            <span class="px late" data-sprite="corazon" data-escala="4"></span>
            <span class="txt">1 SOLA VIDA · SIN ESCUDO</span>
          </div>
          <p>Sin escudo. <b>1 sola vida.</b> Y al final del camino te espera el <b>jefe final
          verdadero</b>. Solo para quienes ya murieron lo suficiente como para aprender.</p>
        </div>
      </div>
    </div>
  </div>
  <div class="caja nota-dif reveal">
    <b>Dificultad muy alta:</b> se estima entre <b>1 y 2 horas</b> de juego continuo para completar el
    desafío. <i>pd del desarrollador: si tienen ideas para el juego, díganlas y veo si las pongo.</i>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== JEFES ==================== -->
<section id="jefes" class="seccion">
  <h2 class="titulo-seccion reveal">
    <span class="px" data-sprite="calavera" data-escala="2.2"></span>JEFES DEL JUEGO
    <span class="titulo-nota">22 EN TOTAL · 9 REVELADOS</span>
  </h2>

  <div class="leyenda reveal">
    <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span>
    <span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span>
    <span class="estado inflexion"><span class="px" data-sprite="estrella" data-escala="1.6"></span>PUNTO DE INFLEXIÓN</span>
    <span class="estado indefinido"><span class="px" data-sprite="pregunta" data-escala="1.6"></span>POR REVELAR</span>
  </div>

  <div class="jefes-destacados">
    <article class="carta-jefe reveal">
      <span class="puerta">P-01</span>
      <span class="px icono-jefe" data-sprite="cristal" data-escala="5"></span>
      <h3>CRYSTALASER</h3>
      <p class="desc-jefe">Un gólem de cristal. El jefe más fácil del juego: la primera prueba del purgatorio.</p>
      <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.06s">
      <span class="puerta">P-04</span>
      <span class="px icono-jefe" data-sprite="chaoz" data-escala="5"></span>
      <h3>CHAOZ</h3>
      <p class="desc-jefe">Encarnación del caos puro. Implementado, aunque aún sin sprite oficial.</p>
      <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO (SIN SPRITE)</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.12s">
      <span class="puerta">P-05</span>
      <span class="icono-jefe"><img src="https://i.imgur.com/TQdxOsP.png" alt="Caballero Sombrío" class="espada-img lg"></span>
      <h3>CABALLERO SOMBRÍO</h3>
      <p class="desc-jefe">Un caballero de diseño similar a Thantanatos. Aún en desarrollo.</p>
      <span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.18s">
      <span class="puerta">P-06</span>
      <span class="px icono-jefe" data-sprite="thanatos" data-escala="5"></span>
      <h3>THANTANATOS</h3>
      <p class="desc-jefe">La muerte misma, convertida en jefe. Implementado sin sprite oficial.</p>
      <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO (SIN SPRITE)</span>
    </article>
    <article class="carta-jefe jefe-inflexion reveal" style="--d:.24s">
      <span class="puerta">P-14</span>
      <span class="px icono-jefe" data-sprite="mirror" data-escala="5"></span>
      <h3>MIRROR</h3>
      <p class="desc-jefe">Un jefe que te muestra tu peor versión. Al derrotarlo, el remordimiento y la
      determinación transforman a Slash en una nueva forma: de ahí en adelante, el camino solo trae
      sufrimiento.</p>
      <span class="estado inflexion"><span class="px" data-sprite="estrella" data-escala="1.6"></span>PUNTO DE INFLEXIÓN</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.3s">
      <span class="puerta">P-15</span>
      <span class="px icono-jefe" data-sprite="duality" data-escala="5"></span>
      <h3>DUALITY</h3>
      <p class="desc-jefe">Representa la línea entre el bien y el mal.</p>
      <span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.36s">
      <span class="puerta">P-16</span>
      <span class="px icono-jefe" data-sprite="cosmoc" data-escala="5"></span>
      <h3>COSMOC</h3>
      <p class="desc-jefe">Un dios del cosmos.</p>
      <span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.42s">
      <span class="puerta">P-17</span>
      <span class="px icono-jefe" data-sprite="gusano" data-escala="5"></span>
      <h3>EL GUSANO</h3>
      <p class="desc-jefe">Un gusano colosal que recorre su puerta.</p>
      <span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span>
    </article>
    <article class="carta-jefe reveal" style="--d:.48s">
      <span class="puerta">P-18</span>
      <span class="px icono-jefe" data-sprite="phoex" data-escala="5"></span>
      <h3>PHOENIX</h3>
      <p class="desc-jefe">El ave ígnea renacida de las cenizas. Completado con sprite incluido.</p>
      <span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO (CON SPRITE)</span>
    </article>
  </div>

  <!-- ===== MÁS PUERTAS EN CAMINO... ===== -->
  <div class="caja mas-puertas reveal">
    <span class="px" data-sprite="puerta" data-escala="3.4"></span>
    <div>
      <h3>MÁS PUERTAS EN CAMINO...</h3>
      <p>Las puertas <b>2</b>, <b>3</b>, <b>7 a la 13</b> y <b>19 a la 22</b> todavía no tienen diseño
      definido. El resto de los jefes sigue en desarrollo: cada uno será revelado en esta wiki
      apenas cruce esa puerta.</p>
      <div class="puertas-pendientes">
        <span class="puerta-chip">P-02</span>
        <span class="puerta-chip">P-03</span>
        <span class="puerta-chip">P-07</span>
        <span class="puerta-chip">P-08</span>
        <span class="puerta-chip">P-09</span>
        <span class="puerta-chip">P-10</span>
        <span class="puerta-chip">P-11</span>
        <span class="puerta-chip">P-12</span>
        <span class="puerta-chip">P-13</span>
        <span class="puerta-chip">P-19</span>
        <span class="puerta-chip">P-20</span>
        <span class="puerta-chip">P-21</span>
        <span class="puerta-chip">P-22</span>
      </div>
    </div>
  </div>

  <!-- ===== TABLA RESUMEN ===== -->
  <div class="tabla-wrap reveal" style="margin-top:18px">
    <table>
      <thead>
        <tr><th>#</th><th>JEFE</th><th>DESCRIPCIÓN</th><th>ESTADO</th></tr>
      </thead>
      <tbody>
        <tr><td class="num">01</td><td><span class="celda-jefe"><span class="px" data-sprite="cristal" data-escala="1.8"></span><span class="nombre-jefe">Crystalaser</span></span></td><td>Gólem de cristal. El jefe más fácil del juego.</td><td><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></td></tr>
        <tr class="fila-misterio"><td class="num">02</td><td><span class="celda-jefe"><span class="px" data-sprite="pregunta" data-escala="1.8"></span>???</span></td><td>Sin diseño definido.</td><td><span class="estado indefinido"><span class="px" data-sprite="pregunta" data-escala="1.6"></span>POR REVELAR</span></td></tr>
        <tr class="fila-misterio"><td class="num">03</td><td><span class="celda-jefe"><span class="px" data-sprite="pregunta" data-escala="1.8"></span>???</span></td><td>Sin diseño definido.</td><td><span class="estado indefinido"><span class="px" data-sprite="pregunta" data-escala="1.6"></span>POR REVELAR</span></td></tr>
        <tr><td class="num">04</td><td><span class="celda-jefe"><span class="px" data-sprite="chaoz" data-escala="1.8"></span><span class="nombre-jefe">Chaoz</span></span></td><td>Entidad de caos puro. Hecho sin sprite.</td><td><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></td></tr>
        <tr><td class="num">05</td><td><span class="celda-jefe"><img src="https://i.imgur.com/TQdxOsP.png" alt="Caballero Sombrío" class="espada-img sm">Caballero sombrío</span></td><td>Un caballero de diseño similar a Thantanatos.</td><td><span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span></td></tr>
        <tr><td class="num">06</td><td><span class="celda-jefe"><span class="px" data-sprite="thanatos" data-escala="1.8"></span><span class="nombre-jefe">Thantanatos</span></span></td><td>La muerte misma, convertida en jefe.</td><td><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></td></tr>
        <tr class="fila-misterio"><td class="num">07-13</td><td><span class="celda-jefe"><span class="px" data-sprite="pregunta" data-escala="1.8"></span>??? ??? ??? ??? ??? ??? ???</span></td><td>Siete puertas aún sin revelar.</td><td><span class="estado indefinido"><span class="px" data-sprite="pregunta" data-escala="1.6"></span>POR REVELAR</span></td></tr>
        <tr><td class="num">14</td><td><span class="celda-jefe"><span class="px" data-sprite="mirror" data-escala="1.8"></span><span class="nombre-jefe">Mirror</span></span></td><td>Te muestra tu peor versión. El punto de inflexión de la historia.</td><td><span class="estado inflexion"><span class="px" data-sprite="estrella" data-escala="1.6"></span>PUNTO DE INFLEXIÓN</span></td></tr>
        <tr><td class="num">15</td><td><span class="celda-jefe"><span class="px" data-sprite="duality" data-escala="1.8"></span><span class="nombre-jefe">Duality</span></span></td><td>Representa la línea entre el bien y el mal.</td><td><span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span></td></tr>
        <tr><td class="num">16</td><td><span class="celda-jefe"><span class="px" data-sprite="cosmoc" data-escala="1.8"></span><span class="nombre-jefe">Cosmoc</span></span></td><td>Un dios del cosmos.</td><td><span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span></td></tr>
        <tr><td class="num">17</td><td><span class="celda-jefe"><span class="px" data-sprite="gusano" data-escala="1.8"></span>El Gusano</span></td><td>Un gusano colosal que recorre su puerta.</td><td><span class="estado pensando"><span class="px" data-sprite="medio" data-escala="1.6"></span>EN DESARROLLO</span></td></tr>
        <tr><td class="num">18</td><td><span class="celda-jefe"><span class="px" data-sprite="phoex" data-escala="1.8"></span><span class="nombre-jefe">Phoenix</span></span></td><td>Ave ígnea legendaria. Hecho con sprite.</td><td><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></td></tr>
        <tr class="fila-misterio"><td class="num">19-22</td><td><span class="celda-jefe"><span class="px" data-sprite="pregunta" data-escala="1.8"></span>??? ??? ??? ???</span></td><td>Las últimas cuatro puertas aguardan su diseño.</td><td><span class="estado indefinido"><span class="px" data-sprite="pregunta" data-escala="1.6"></span>POR REVELAR</span></td></tr>
      </tbody>
    </table>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== JUGABILIDAD ==================== -->
<section id="jugabilidad" class="seccion">
  <h2 class="titulo-seccion reveal">
    <span class="px" data-sprite="rayo" data-escala="2.4"></span>JUGABILIDAD Y MECÁNICAS
  </h2>
  <div class="mecanicas-grid">
    <div class="mecanica e-hecho reveal">
      <div class="mec-cabecera"><kbd>Z</kbd><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></div>
      <h3>DASH</h3>
      <p>Impulso veloz para esquivar ataques. Terminado, con un posible buff a futuro.</p>
    </div>
    <div class="mecanica e-hecho reveal" style="--d:.06s">
      <div class="mec-cabecera"><kbd>X</kbd><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></div>
      <h3>PRESIÓN DE CABALLERO</h3>
      <p>Elimina todos los proyectiles en pantalla. Recarga: 20 segundos.</p>
    </div>
    <div class="mecanica e-pensando reveal" style="--d:.12s">
      <div class="mec-cabecera"><span class="px" data-sprite="gravedad" data-escala="2.4"></span><span class="estado pensando"><span class="px" data-sprite="delta" data-escala="1.6"></span>PENSANDO</span></div>
      <h3>GRAVEDAD INVERTIDA</h3>
      <p>Voltea las flechas de movimiento: el control se invierte y todo se vuelve caótico.</p>
    </div>
    <div class="mecanica e-pensando reveal" style="--d:.18s">
      <div class="mec-cabecera"><span class="px" data-sprite="cruz" data-escala="2.6"></span><span class="estado pensando"><span class="px" data-sprite="delta" data-escala="1.6"></span>PENSANDO</span></div>
      <h3>CURA DE VIDA</h3>
      <p>Recuperación de vida en pleno combate. Aún en fase de diseño.</p>
    </div>
    <div class="mecanica e-hecho reveal" style="--d:.24s">
      <div class="mec-cabecera"><span class="px" data-sprite="reloj" data-escala="2.4"></span><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></div>
      <h3>ENFRENTAMIENTO CON TIEMPO</h3>
      <p>Cada combate contra un jefe tiene un temporizador. (Sí, un timer xd).</p>
    </div>
    <div class="mecanica e-hecho reveal" style="--d:.3s">
      <div class="mec-cabecera"><span class="px" data-sprite="diana" data-escala="2.4"></span><span class="estado hecho"><span class="px" data-sprite="check" data-escala="1.6"></span>HECHO</span></div>
      <h3>JEFES CON MOVIMIENTO</h3>
      <p>Los jefes se desplazan por la arena y atacan de forma dinámica.</p>
    </div>
    <div class="mecanica e-descartado reveal" style="--d:.36s">
      <div class="mec-cabecera"><span class="px" data-sprite="espadasX" data-escala="2.2"></span><span class="estado descartado"><span class="px" data-sprite="cross" data-escala="1.6"></span>DESCARTADO</span></div>
      <h3>PARRY</h3>
      <p>La parada de ataques. Terminó convirtiéndose en otra mecánica por completo.</p>
    </div>
    <div class="mecanica e-descartado reveal" style="--d:.42s">
      <div class="mec-cabecera"><span class="px" data-sprite="swap" data-escala="2.2"></span><span class="estado descartado"><span class="px" data-sprite="cross" data-escala="1.6"></span>DESCARTADO</span></div>
      <h3>CAMBIO DE MOVIMIENTO</h3>
      <p>Pasar de un juego top-down a uno con gravedad. Idea descartada.</p>
    </div>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== MAPAS ==================== -->
<section id="mapas" class="seccion">
  <h2 class="titulo-seccion reveal">
    <span class="px" data-sprite="mapa" data-escala="2.4"></span>MAPAS CON EFECTOS
    <span class="titulo-nota">EN DISEÑO</span>
  </h2>
  <div class="mapas-grid">
    <div class="mapa-caja mapa-positivo reveal">
      <span class="px" data-sprite="estrella" data-escala="3.2"></span>
      <div>
        <h3>EFECTOS POSITIVOS</h3>
        <p>Algunos mapas otorgan beneficios al jugador que sabe aprovecharlos. La arena puede
        convertirse en tu aliada… si la entiendes.</p>
      </div>
    </div>
    <div class="mapa-caja mapa-negativo reveal" style="--d:.1s">
      <span class="px" data-sprite="calavera" data-escala="2.8"></span>
      <div>
        <h3>EFECTOS NEGATIVOS</h3>
        <p>Otros mapas complican el combate: la dificultad de cada puerta determina cuánto
        se vuelve el campo en tu contra.</p>
      </div>
    </div>
  </div>
  <div class="caja reveal">
    <h3><span class="px" data-sprite="mapa" data-escala="2.2"></span>¿CÓMO FUNCIONAN?</h3>
    <p style="font-size:21px">Cada mapa de jefe puede tener un efecto propio, positivo o negativo, acorde a la
    dificultad. Ninguna puerta del purgatorio es igual a la anterior.</p>
  </div>
</section>

<div class="divisor"><span class="px" data-sprite="puerta" data-escala="1.6"></span></div>

<!-- ==================== ÚNETE A LA COMUNIDAD ==================== -->
<section id="comunidad" class="seccion">
  <h2 class="titulo-seccion reveal">
    <img src="https://i.imgur.com/QlhirAo.png" alt="WhatsApp" class="wa-img md">ÚNETE A LA COMUNIDAD
  </h2>

  <div class="whatsapp-caja reveal">
    <div class="wa-contenido">
      <span class="wa-icono"><img src="https://i.imgur.com/QlhirAo.png" alt="Canal de WhatsApp" class="wa-img lg"></span>
      <div class="wa-texto">
        <h3>CANAL DE COMUNICADOS OFICIAL</h3>
        <p>Seguí el canal de Comunicados Oficial de <b>The Doors of the Purgatory</b> para enterarte
        primero de todas las novedades: nuevos jefes, mecánicas, avances del desarrollo y anuncios
        importantes. Todo directo a tu WhatsApp.</p>
      </div>
    </div>
    <a class="wa-btn" href="https://whatsapp.com/channel/0029VbDpz3ICMY0Kf0xXj328" target="_blank" rel="noopener noreferrer">
      <img src="https://i.imgur.com/QlhirAo.png" alt="WhatsApp" class="wa-img sm">
      ¡SEGUÍ EL CANAL HACIENDO CLIC AQUÍ!
    </a>
    <p class="wa-link">&gt; whatsapp.com/channel/0029VbDpz3ICMY0Kf0xXj328</p>
  </div>

  <div class="caja reveal" style="margin-top:18px;--d:.08s">
    <h3><span class="px" data-sprite="barras" data-escala="2.2"></span>ESTADÍSTICAS</h3>
    <p class="fecha">Hoy, <span id="fechaHoy"></span>.</p>
    <div class="stat-lineas">
      <div><span>Jefes documentados</span><b data-contar>22</b></div>
      <div><span>Jefes revelados</span><b data-contar>9 (41 %)</b></div>
      <div><span>Puertas del purgatorio</span><b data-contar>21</b></div>
      <div><span>Punto de inflexión</span><b class="verde" data-contar>Puerta 14</b></div>
      <div><span>Mecánicas</span><b data-contar>8</b></div>
      <div><span>Rutas de juego</span><b data-contar>2</b></div>
      <div><span>Duración estimada</span><b>1-2 hs</b></div>
      <div><span>Estado del juego</span><b class="verde">En desarrollo</b></div>
      <div><span>Última edición</span><b>14/09/2026</b></div>
    </div>
  </div>
</section>

</main>

<!-- ==================== FOOTER + CRÉDITOS ==================== -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">
      <span class="px" data-sprite="puerta" data-escala="2"></span>
      THE DOORS OF THE PURGATORY <span>WIKI</span>
    </div>

    <div class="creditos">
      <div class="credito">
        <span class="px" data-sprite="corona" data-escala="2.4"></span>
        <div>
          <span class="credito-rol">CREADOR DEL JUEGO</span>
          <span class="credito-nombre verde">THIAGO PEREYRA</span>
        </div>
      </div>
      <div class="credito">
        <span class="px" data-sprite="libro" data-escala="2.4"></span>
        <div>
          <span class="credito-rol">CREADOR DE LA PÁGINA</span>
          <span class="credito-nombre azul">LAUTARO JESSEN</span>
        </div>
      </div>
    </div>

    <p>The Doors of the Purgatory es un juego independiente en desarrollo.</p>
    <p class="licencia">El contenido está disponible bajo <b>CC BY-NC-SA</b> · Diseño inspirado en la Wiki Terraria.</p>
    <div class="afiliados">
      <div class="afiliado"><img src="https://i.imgur.com/QlhirAo.png" alt="WhatsApp" class="wa-img sm">CANAL OFICIAL DE WHATSAPP</div>
      <div class="afiliado"><span class="px" data-sprite="puerta" data-escala="1.6"></span>WIKI TERRARIA (INSPIRACIÓN)</div>
    </div>
    <p>© 2026 — The Doors of the Purgatory.</p>
  </div>
</footer>

<button class="btn-subir" id="btnSubir" aria-label="Volver arriba">
  <img src="https://i.imgur.com/1wnoCcH.png" alt="Volver arriba" class="flecha-img">
</button>

<script>
/* ============================================================
   SISTEMA DE SPRITES PIXEL ART
   Cada sprite es una matriz de caracteres; cada carácter
   es un color de la paleta. '.' = píxel transparente.
   ============================================================ */
const PALETA = {
  '0':'#0a141d','g':'#1f9e5c','G':'#3fdc86','Y':'#b8ffd9',
  'b':'#1b5a9e','B':'#3b9eff','C':'#a9dcff','w':'#eaf6ee',
  'd':'#4a5a68','D':'#2a3947','o':'#f6b545','O':'#8a5a1a',
  'r':'#8a2b2b','R':'#ff5d5d','s':'#ffe98a','m':'#7a5cff','v':'#c9a2ff'
};

const SPRITES = {
puerta:[
"oooooooooooo",
"oD00000000Do",
"oD0bbbbbb0Do",
"oD0b0bb0b0Do",
"oD0b0bb0b0Do",
"oD0bb00Gb0Do",
"oD0bb00bb0Do",
"oD0b0bb0b0Do",
"oD0b0bb0b0Do",
"oD0bbbbbb0Do",
"oD00000000Do",
"oooooooooooo"],
puertaAbierta:[
"oooooooooooo",
"oD00000000Do",
"oD00G00G00Do",
"oD00G00G00Do",
"oD00000000Do",
"oD00G00G00Do",
"oD00G00G00Do",
"oD00000000Do",
"oD00G00G00Do",
"oD00G00G00Do",
"oD00000000Do",
"oooooooooooo"],
espada:[
"GY..........",
"GYG.........",
".GYG........",
"..GYG.......",
"...GYG......",
"....GYG.....",
"..OOOOOO....",
"....d.......",
".....d......",
"......d.....",
".......o...."],
cursor:[
"G...........",
"GG..........",
"GwG.........",
"GwwG........",
"GwwwG.......",
"GwwwwG......",
"GwwwwwG.....",
"GwwwwwwG....",
"GwwGwwwG....",
"GwGGGwG.....",
"GG..GwG.....",
"G....GG....."],
corazon:[
".RR.RR.",
"RsRRRRR",
"RRRRRRR",
".RRRRR.",
"..RRR..",
"...R..."],
escudo:[
"gggggggg",
"gGGGGGGg",
"gGGYYGGg",
"gGGYYGGg",
"gGGGGGGg",
".gGGGGg.",
".gGGGGg.",
"..gGGg..",
"...gg..."],
escudoRoto:[
"gggg0ggg",
"gGGG0GGg",
"gGG0YGGg",
"gG0YYGGg",
"gGG0YGGg",
".g0GGg..",
"..gGg...",
"...gg..."],
calavera:[
".wwwwww.",
"wwwwwwww",
"w00ww00w",
"w00ww00w",
"wwwwwwww",
".ww0w0w.",
".wwwwww.",
".w.ww.w.",
"..w..w.."],
thanatos:[
"....DDDD....",
"..DDwwwwDD..",
".DDwwwwwwDD.",
".DwRRwwRRwD.",
".DwwwwwwwwD.",
".DDwww0wwDD.",
"..DwwwwwwD..",
"..DDwwwwDD..",
"...DDDDDD...",
"....D..D....",
"...DD..DD..."],
cristal:[
"....CBBC....",
"....CBBC....",
"..CCBBBBCC..",
".CCBBooBBCC.",
"CCBBBBBBBBCC",
"CCBbBBBBbBCC",
".CCBBBBBBCC.",
"..CCBBBBCC..",
"...CC..CC...",
"...00..00..."],
chaoz:[
".....mm.....",
".....mm.....",
"..mmmvvmmm..",
"..mmmvvmmm..",
"mmmmvvvvmmmm",
"mmmmvssvmmmm",
"mmmmvvvvmmmm",
"..mmmvvmmm..",
"..mmmvvmmm..",
".....mm.....",
".....mm....."],
mirror:[
"..oooooo..",
".obbbbbbo.",
".obCbbbbo.",
".obCCbbbo.",
".obbCCbbo.",
".obbbCCbo.",
".obbbbCbo.",
".obbbbbbo.",
"..oooooo..",
"....oo....",
"...oooo..."],
duality:[
"...www000...",
"..wwww0000..",
".wwwww00000.",
".ww0ww00w00.",
"wwwww0000000",
"wwwww0000000",
"wwwww0000000",
"wwwww0000000",
".wwwww00000.",
".wwwww00000.",
"..wwww0000..",
"...www000..."],
cosmoc:[
".....s......",
"....BBBB....",
"..BBBBBBBB..",
".BBbBBBBbBB.",
".BbBBBBBBbB.",
"oBBbBBBBbBBo",
"ooBBBBBBBBoo",
".oBbBBBBbBo.",
"..BBBBBBBB..",
"....BBBB....",
".....s......"],
gusano:[
"....gggg....",
"..ggGGGGgg..",
"..gG0GG0Gg..",
"..gGGGGGGg..",
"...gGGGGg...",
"...gGGGGg...",
"..gGGGGg....",
".gGGGGg.....",
"gGGGGg......",
"gGGg........",
".gg........."],
phoex:[
"......o.....",
".....oo.....",
"....ooo.....",
"....oooo....",
"...oo.soo...",
"..oo.ssoo...",
".oo.sssso...",
".oo.ssYsso..",
".ooossssso..",
"..oosssso...",
"...ossso....",
"....ooo....."],
pregunta:[
"..ssss..",
".ss..ss.",
".ss..ss.",
"....ss..",
"...ss...",
"...ss...",
"........",
"...ss...",
"...ss..."],
reloj:[
"...wwww...",
"..w....w..",
".w......w.",
".w...s..w.",
".w...sssw.",
".w......w.",
".w......w.",
"..w....w..",
"...wwww..."],
estrella:[
"....s....",
"....s....",
"...sss...",
"sssssssss",
".sssssss.",
"..sssss..",
".sss.sss.",
"ss..s..ss",
"s...s...s"],
bombilla:[
"..ssss..",
".ssYYss.",
".sYYYYs.",
".ssYYss.",
"..ssss..",
"...dd...",
"...dd...",
"..dddd.."],
signo:[
".oooo.",
".oooo.",
".oooo.",
".oooo.",
"......",
".oooo.",
".oooo."],
libro:[
"..dd..dd..",
".dwwddwwd.",
".dwwddwwd.",
".dwwddwwd.",
".dwwddwwd.",
"..dddddd..",
"...gggg..."],
corona:[
"o...o...o.",
"oo..oo..oo",
"oooooooooo",
"oooooooooo",
".oooooooo."],
rayo:[
"...ss...",
"..ss....",
".ss.....",
"ssssss..",
"...ss...",
"..ss....",
".ss.....",
"ss......"],
gravedad:[
"...b....",
"..bbb...",
".bbbbb..",
"...b....",
"...b....",
"........",
"...b....",
"...b....",
".bbbbb..",
"..bbb...",
"...b...."],
cruz:[
"..rr..",
"..rr..",
"rrrrrr",
"rrrrrr",
"..rr..",
"..rr.."],
diana:[
"..bbbb..",
".b....b.",
"b..ww..b",
"b.wwww.b",
"b.wwww.b",
"b..ww..b",
".b....b.",
"..bbbb.."],
espadasX:[
"o........o",
"oG......Go",
".G......G.",
"..G....G..",
"...G..G...",
"....GG....",
"...G..G...",
"..G....G..",
".G......G.",
"o........o"],
swap:[
"......b...",
"bbbbbbbbb.",
"......b...",
"..........",
"...b......",
".bbbbbbbbb",
"...b......"],
mapa:[
"dddddddddd",
"dwwwwwwwwd",
"dwwbwwwwwd",
"dwwRwRwwwd",
"dwwwRwwwwd",
"dwwRwRwwwd",
"dwwwwwwwwd",
"dwwwwwbwwd",
"dwwwwwwwwd",
"dddddddddd"],
bandera:[
"dGGGGGG.",
"dGGGGGG.",
"dGGGGGG.",
"dGGGGGG.",
"dGGGGGG.",
"d.......",
"d.......",
"d......."],
barras:[
"........",
".....o..",
"....Bo..",
"....Bo..",
"..G.Bo..",
"..G.Bo..",
"..G.Bo..",
"dddddddd"],
flechaUp:[
"...GG...",
"..GGGG..",
".GGGGGG.",
"GGGGGGGG",
"...GG...",
"...GG...",
"...GG...",
"...GG..."],
play:[
"G...",
"GG..",
"GGG.",
"GG.."],
check:[
".....G",
"....G.",
"...G..",
"G..G..",
".GG...",
"..G..."],
cross:[
"R....R",
".R..R.",
"..RR..",
"..RR..",
".R..R.",
"R....R"],
medio:[
"oooooo",
"ooooo.",
"oooo..",
"ooo...",
"oo....",
"o....."],
delta:[
"...B..",
"..BBB.",
".BBBBB",
"BBBBBB"]
};

/* ---- Generador: convierte una matriz en SVG de rects (píxel perfecto) ---- */
function dimsDe(filas){
  return {w:Math.max(...filas.map(f=>f.length)), h:filas.length};
}
function rectsDe(filas){
  let rects = '';
  filas.forEach((fila,y)=>{
    let x = 0;
    while(x < fila.length){
      const color = PALETA[fila[x]];
      if(color){
        let ancho = 1;
        while(x+ancho < fila.length && fila[x+ancho] === fila[x]) ancho++;
        rects += `<rect x="${x}" y="${y}" width="${ancho}" height="1" fill="${color}"/>`;
        x += ancho;
      } else x++;
    }
  });
  return rects;
}
function spriteDataURL(nombre, px){
  const filas = SPRITES[nombre];
  const {w,h} = dimsDe(filas);
  const svg = `<svg xmlns="http://www.w3.org/2000/svg" width="${w*px}" height="${h*px}" viewBox="0 0 ${w} ${h}" shape-rendering="crispEdges">${rectsDe(filas)}</svg>`;
  return 'data:image/svg+xml;utf8,' + encodeURIComponent(svg);
}

/* ---- Corazones de vidas (se generan antes del render general) ---- */
document.querySelectorAll('[data-corazones]').forEach(el=>{
  const n = +el.dataset.corazones;
  for(let i=0;i<n;i++){
    const s = document.createElement('span');
    s.className = 'px';
    s.dataset.sprite = 'corazon';
    s.dataset.escala = 2;
    el.appendChild(s);
  }
  const txt = document.createElement('span');
  txt.className = 'txt';
  txt.textContent = n + (n===1?' VIDA':' VIDAS');
  el.appendChild(txt);
});

/* ---- Render de un sprite individual (reutilizable) ---- */
function renderizarSprite(el){
  const nombre = el.dataset.sprite;
  if(!SPRITES[nombre]) return;
  const filas = SPRITES[nombre];
  const {w,h} = dimsDe(filas);
  const escala = parseFloat(el.dataset.escala || 3);
  el.innerHTML = `<svg viewBox="0 0 ${w} ${h}" shape-rendering="crispEdges" aria-hidden="true">${rectsDe(filas)}</svg>`;
  el.style.width  = Math.round(w*escala) + 'px';
  el.style.height = Math.round(h*escala) + 'px';
}

/* ---- Render de todos los sprites de la página ---- */
document.querySelectorAll('.px').forEach(renderizarSprite);

/* ---- Fallback de la flecha: si el PNG no carga, vuelve al sprite pixel ---- */
(() => {
  const imgFlecha = document.querySelector('.btn-subir img.flecha-img');
  if (imgFlecha) imgFlecha.addEventListener('error', () => {
    const s = document.createElement('span');
    s.className = 'px';
    s.dataset.sprite = 'flechaUp';
    s.dataset.escala = '2.6';
    imgFlecha.replaceWith(s);
    renderizarSprite(s);
  });
})();

/* ---- Favicon pixel art (generado desde el sprite puerta) ---- */
document.getElementById('favicon').href = spriteDataURL('puerta', 4);

/* ---- Cursor base: flecha pixel para navegar + espada pixel de respaldo ---- */
const estiloCursor = document.createElement('style');
estiloCursor.textContent = `
  html{cursor:url("${spriteDataURL('cursor',2)}") 0 0, auto}
  a,button,.toc a,.wa-btn,.carta-jefe{cursor:url("${spriteDataURL('espada',2)}") 0 0, pointer}
`;
document.head.appendChild(estiloCursor);

/* ---- Espada personalizada como cursor (elementos clicables) ---- */
(() => {
  const URL_ESPADA = 'https://i.imgur.com/nrNgkJQ.png';
  const img = new Image();
  img.crossOrigin = 'anonymous';
  img.onload = () => {
    const w0 = img.naturalWidth || 16, h0 = img.naturalHeight || 16;
    const lado = Math.max(w0, h0);
    let escala = 1;
    if (lado < 32) escala = Math.max(1, Math.floor(32 / lado));
    else if (lado > 32) escala = 32 / lado;
    const w = Math.max(1, Math.round(w0 * escala));
    const h = Math.max(1, Math.round(h0 * escala));
    let urlCursor = URL_ESPADA;
    try {
      const canvas = document.createElement('canvas');
      canvas.width = w; canvas.height = h;
      const ctx = canvas.getContext('2d');
      ctx.imageSmoothingEnabled = escala < 1;
      ctx.drawImage(img, 0, 0, w, h);
      urlCursor = canvas.toDataURL('image/png');
    } catch(e) { /* CORS bloqueó el canvas: uso la URL directa */ }
    const hx = Math.min(w - 1, Math.round(w * 0.9));
    const hy = Math.max(0, Math.round(h * 0.08));
    const estiloEspada = document.createElement('style');
    estiloEspada.textContent = `
      a,button,.toc a,.wa-btn,.carta-jefe{cursor:url("${urlCursor}") ${hx} ${hy}, url("${spriteDataURL('espada',2)}") 0 0, pointer}
    `;
    document.head.appendChild(estiloEspada);
  };
  img.onerror = () => {};
  img.src = URL_ESPADA;
})();

/* ---- Estrellas pixel de fondo (tipo Terraria nocturno) ---- */
(() => {
  const cont = document.getElementById('estrellas');
  const colores = ['#eaf6ee','#3fdc86','#3b9eff','#ffe98a'];
  for(let i=0;i<70;i++){
    const e = document.createElement('div');
    e.className = 'estrella';
    const t = Math.random() < .7 ? 2 : 3;
    e.style.width = e.style.height = t+'px';
    e.style.left = Math.random()*100+'%';
    e.style.top = Math.random()*100+'%';
    e.style.background = colores[Math.floor(Math.random()*colores.length)];
    e.style.animationDuration = (1.8+Math.random()*3)+'s';
    e.style.animationDelay = (Math.random()*3)+'s';
    cont.appendChild(e);
  }
})();

/* ============================================================
   ============ ANIMACIONES (JS) ============
   ============================================================ */
const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

/* --- A. PANTALLA DE ARRANQUE: carga y corta con estática.
   Clic = saltar. Reduce motion = no existe. --- */
(() => {
  const boot = document.getElementById('boot');
  if (!boot) return;
  if (reduceMotion) { boot.remove(); return; }
  document.body.classList.add('boot-activo');
  const cerrar = () => {
    if (!boot.parentNode) return;
    boot.classList.add('boot-ruido');            /* ráfaga de estática */
    setTimeout(() => {
      boot.remove();
      document.body.classList.remove('boot-activo');
    }, 130);
  };
  boot.addEventListener('click', cerrar);
  setTimeout(cerrar, 2200);
})();

/* --- CENIZA DIGITAL: partículas pixel cayendo en el héroe --- */
(() => {
  if (reduceMotion) return;
  const cont = document.querySelector('.ceniza');
  if (!cont) return;
  const colores = ['#4a5a68','#2a3947','#3fdc86','#3b9eff','#8ba5ad'];
  for (let i = 0; i < 26; i++) {
    const c = document.createElement('div');
    c.className = 'copo';
    const t = Math.random() < .75 ? 2 : 3;
    c.style.width = c.style.height = t + 'px';
    c.style.left = Math.random() * 100 + '%';
    c.style.background = colores[Math.floor(Math.random() * colores.length)];
    c.style.animationDuration = (8 + Math.random() * 9) + 's';
    c.style.animationDelay = -(Math.random() * 16) + 's';
    cont.appendChild(c);
  }
})();

/* --- DAÑO EN CORAZONES: click = shake + flash + un corazón se apaga --- */
(() => {
  if (reduceMotion) return;
  document.querySelectorAll('.vidas').forEach(v => {
    v.addEventListener('click', () => {
      v.classList.remove('dano');
      void v.offsetWidth;
      v.classList.add('dano');
      const corazones = v.querySelectorAll('.px');
      const c = corazones[Math.floor(Math.random() * corazones.length)];
      if (c) c.classList.add('apagado');
      setTimeout(() => {
        v.classList.remove('dano');
        if (c) c.classList.remove('apagado');
      }, 650);
    });
  });
})();

/* --- CHISPAS PIXEL al hacer click en cualquier lado --- */
(() => {
  if (reduceMotion) return;
  const colores = ['#3fdc86', '#3b9eff', '#f6b545', '#eaf6ee'];
  let ultimo = 0;
  document.addEventListener('click', e => {
    const ahora = performance.now();
    if (ahora - ultimo < 60) return;
    ultimo = ahora;
    for (let i = 0; i < 7; i++) {
      const p = document.createElement('div');
      p.className = 'chispa';
      const t = 3 + Math.round(Math.random() * 2);
      p.style.width = p.style.height = t + 'px';
      p.style.left = e.clientX + 'px';
      p.style.top = e.clientY + 'px';
      p.style.background = colores[Math.floor(Math.random() * colores.length)];
      document.body.appendChild(p);
      const ang = Math.random() * Math.PI * 2;
      const dist = 24 + Math.random() * 34;
      const dx = Math.cos(ang) * dist;
      const dy = Math.sin(ang) * dist - 18;
      const caida = dy + 46;
      p.animate([
        { transform: 'translate(-50%,-50%)', opacity: 1 },
        { transform: `translate(calc(-50% + ${dx}px), calc(-50% + ${dy}px))`, opacity: 1, offset: .45 },
        { transform: `translate(calc(-50% + ${dx}px), calc(-50% + ${caida}px))`, opacity: 0 }
      ], { duration: 420 + Math.random() * 260, easing: 'steps(7)' });
      setTimeout(() => p.remove(), 750);
    }
  });
})();

/* --- MOTITAS de polvo pixel detrás del cursor (solo PC) --- */
(() => {
  if (reduceMotion) return;
  let ultimo = 0;
  document.addEventListener('mousemove', e => {
    const ahora = performance.now();
    if (ahora - ultimo < 80) return;
    if (document.querySelectorAll('.motita').length > 30) return;
    ultimo = ahora;
    const m = document.createElement('div');
    m.className = 'motita';
    const t = Math.random() < .7 ? 2 : 3;
    m.style.width = m.style.height = t + 'px';
    m.style.left = e.clientX + 'px';
    m.style.top = e.clientY + 'px';
    m.style.background = Math.random() < .5 ? '#3fdc86' : '#3b9eff';
    m.style.opacity = .8;
    document.body.appendChild(m);
    m.animate([
      { transform: 'translate(-50%,-50%)', opacity: .8 },
      { transform: 'translate(-50%, 26px)', opacity: 0 }
    ], { duration: 700 + Math.random() * 400, easing: 'steps(8)' });
    setTimeout(() => m.remove(), 1200);
  });
})();

/* --- CONTADORES: los números de Estadísticas suben al entrar --- */
(() => {
  const nums = document.querySelectorAll('[data-contar]');
  if (!nums.length) return;
  const animar = el => {
    if (reduceMotion) return;
    const original = el.textContent;
    const m = original.match(/\d+/);
    if (!m) return;
    const objetivo = parseInt(m[0], 10);
    if (objetivo < 2) return;
    let actual = 0;
    const demora = Math.max(40, Math.floor(700 / objetivo));
    const paso = () => {
      actual++;
      el.textContent = original.replace(String(objetivo), String(actual));
      if (actual < objetivo) setTimeout(paso, demora);
      else el.textContent = original;
    };
    paso();
  };
  const obs = new IntersectionObserver(es => {
    es.forEach(e => { if (e.isIntersecting) { obs.unobserve(e.target); animar(e.target); } });
  }, { threshold: .6 });
  nums.forEach(n => obs.observe(n));
})();

/* --- CÓDIGO KONAMI: ↑↑↓↓←→←→ B A = lluvia de corazones + toast --- */
(() => {
  const seq = ['ArrowUp','ArrowUp','ArrowDown','ArrowDown','ArrowLeft','ArrowRight','ArrowLeft','ArrowRight','b','a'];
  let idx = 0;
  document.addEventListener('keydown', e => {
    const k = e.key.length === 1 ? e.key.toLowerCase() : e.key;
    if (k === seq[idx]) {
      idx++;
      if (idx === seq.length) { idx = 0; activar(); }
    } else {
      idx = (k === seq[0]) ? 1 : 0;
    }
  });
  function activar() {
    if (reduceMotion) return;
    for (let i = 0; i < 18; i++) {
      const c = document.createElement('span');
      c.className = 'px konami-corazon';
      c.dataset.sprite = 'corazon';
      c.dataset.escala = 3;
      document.body.appendChild(c);
      renderizarSprite(c);
      c.style.left = Math.random() * 100 + 'vw';
      c.style.top = '-30px';
      const dur = 2200 + Math.random() * 1800;
      const giro = (Math.random() < .5 ? -1 : 1) * 90;
      c.animate([
        { transform: 'translateY(0) rotate(0deg)' },
        { transform: `translateY(${window.innerHeight + 60}px) rotate(${giro}deg)` }
      ], { duration: dur, easing: 'steps(22)' });
      setTimeout(() => c.remove(), dur + 100);
    }
    const t = document.createElement('div');
    t.className = 'konami-toast';
    t.innerHTML = '¡CÓDIGO KONAMI!<br>+15 VIDAS · MODO DIOSES';
    document.body.appendChild(t);
    setTimeout(() => t.remove(), 3200);
  }
})();

/* ---- Revelado al hacer scroll (a saltos, 8-bit) ---- */
const revelados = document.querySelectorAll('.reveal');
if ('IntersectionObserver' in window) {
  const obs = new IntersectionObserver(entradas => {
    entradas.forEach(e => {
      if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); }
    });
  }, { threshold: 0.12 });
  revelados.forEach(el => obs.observe(el));
} else {
  revelados.forEach(el => el.classList.add('visible'));
}

/* ---- Barra de progreso + botón subir ---- */
const barra = document.getElementById('barraRelleno');
const btnSubir = document.getElementById('btnSubir');
window.addEventListener('scroll', () => {
  const y = window.scrollY;
  const alto = document.documentElement.scrollHeight - window.innerHeight;
  barra.style.width = Math.min(100, (y / alto) * 100) + '%';
  btnSubir.classList.toggle('visible', y > 400);
}, { passive: true });
btnSubir.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));

/* ---- Fecha de hoy ---- */
const fecha = new Date();
let texto = fecha.toLocaleDateString('es-ES', { weekday:'long', day:'numeric', month:'long', year:'numeric' });
texto = texto.charAt(0).toUpperCase() + texto.slice(1);
document.getElementById('fechaHoy').textContent = texto;

/* ---- ¿Sabías que...? ---- */
const datos = [
  'La misión de Slash no es matar a los dioses: es sobrevivir.',
  'Se estima entre 1 y 2 horas de juego continuo para completar el desafío.',
  'La Puerta 14 (Mirror) marca el punto de inflexión de toda la historia.',
  'Mirror te muestra tu peor versión… y nadie sale igual de esa puerta.',
  'Duality representa la línea exacta entre el bien y el mal.',
  'Cosmoc es un dios del cosmos: uno de los últimos guardianes revelados.',
  'La Presión de Caballero borra todos los proyectiles… pero tarda 20 segundos en recargar.',
  'Todos los comunicados oficiales del juego se publican en el canal de WhatsApp.'
];
let i = 0;
const datoEl = document.getElementById('datoCurioso');
function mostrarDato(){
  datoEl.style.opacity = 0;
  setTimeout(() => { datoEl.textContent = datos[i % datos.length]; i++; datoEl.style.opacity = 1; }, 300);
}
mostrarDato();
setInterval(mostrarDato, 7000);
</script>
</body>
</html>
