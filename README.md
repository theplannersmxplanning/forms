
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Formato de Boda — The Planners</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --ink:#1a1a18;--ink2:#4a4a47;--ink3:#8a8a85;--rule:#ddddd8;--rule-light:#eeeeea;--bg:#fafaf8;--white:#ffffff;
}
html{scroll-behavior:smooth}
body{font-family:'Cormorant Garamond',Georgia,serif;background:var(--bg);color:var(--ink);min-height:100vh;}
.page{max-width:680px;margin:0 auto;padding:3rem 2rem 6rem;}

.logo-wrap{text-align:center;padding-bottom:2.5rem;margin-bottom:2.5rem;border-bottom:1px solid var(--rule);}
.logo-line1{display:flex;align-items:baseline;justify-content:center;gap:10px;margin-bottom:10px;}
.logo-sans{font-family:'Montserrat',sans-serif;font-weight:300;font-size:20px;letter-spacing:.32em;color:var(--ink2);}
.logo-serif{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:34px;font-weight:300;color:var(--ink2);line-height:1;}
.logo-rule{width:260px;height:1px;background:var(--rule);margin:0 auto 10px;}
.logo-sub{font-family:'Montserrat',sans-serif;font-weight:300;font-size:9px;letter-spacing:.35em;color:var(--ink3);text-transform:uppercase;}

.progress-wrap{margin-bottom:2.5rem}
.progress-track{height:1px;background:var(--rule-light);position:relative;margin-bottom:10px}
.progress-fill{height:1px;background:var(--ink);transition:width .5s ease}
.progress-meta{display:flex;justify-content:space-between;align-items:center;}
.progress-num{font-family:'Montserrat',sans-serif;font-size:10px;font-weight:300;letter-spacing:.15em;color:var(--ink3);}
.progress-dots{display:flex;gap:6px}
.pdot{width:5px;height:5px;border-radius:50%;background:var(--rule);transition:background .3s;}
.pdot.done{background:var(--ink3)}.pdot.active{background:var(--ink)}

.step{display:none;animation:fadeUp .4s ease both}.step.active{display:block}
@keyframes fadeUp{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:translateY(0)}}

.step-eyebrow{font-family:'Montserrat',sans-serif;font-size:9px;font-weight:400;letter-spacing:.3em;color:var(--ink3);text-transform:uppercase;margin-bottom:10px;}
.step-title{font-size:36px;font-weight:300;color:var(--ink);line-height:1.15;margin-bottom:8px;}
.step-sub{font-family:'Montserrat',sans-serif;font-size:12px;font-weight:300;color:var(--ink3);margin-bottom:2.5rem;line-height:1.8;}

.section{border-top:1px solid var(--rule-light);padding:2rem 0 0.5rem;margin-bottom:0.5rem;}
.section-label{font-family:'Montserrat',sans-serif;font-size:9px;font-weight:400;letter-spacing:.28em;color:var(--ink3);text-transform:uppercase;margin-bottom:1.5rem;}

.field{margin-bottom:1.8rem}.field:last-child{margin-bottom:0}
label{display:block;font-family:'Montserrat',sans-serif;font-size:9px;font-weight:400;letter-spacing:.2em;color:var(--ink3);text-transform:uppercase;margin-bottom:8px;}
input[type=text],input[type=email],input[type=time],input:not([type=checkbox]):not([type=radio]),textarea,select{
  width:100%;font-family:'Cormorant Garamond',serif;font-size:17px;font-weight:300;color:var(--ink);
  background:transparent;border:none;border-bottom:1px solid var(--rule);border-radius:0;
  padding:8px 0 10px;outline:none;transition:border-color .25s;-webkit-appearance:none;appearance:none;
}
input:focus,textarea:focus,select:focus{border-bottom-color:var(--ink)}
textarea{resize:vertical;min-height:80px;line-height:1.6}
select{
  background-image:url("data:image/svg+xml,%3Csvg width='9' height='5' viewBox='0 0 9 5' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M0.5 0.5L4.5 4.5L8.5 0.5' stroke='%238a8a85' fill='none' stroke-width='0.8'/%3E%3C/svg%3E");
  background-repeat:no-repeat;background-position:right 2px center;padding-right:18px;cursor:pointer;
}
input[type=checkbox]{width:13px;height:13px;accent-color:var(--ink);cursor:pointer;}

.g2{display:grid;grid-template-columns:1fr 1fr;gap:2.5rem}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1.5rem}
.hidden{display:none!important}

.check-list{display:flex;flex-wrap:wrap;gap:10px 20px;margin-top:4px}
.check-item{display:flex;align-items:center;gap:8px;font-family:'Cormorant Garamond',serif;font-size:16px;font-weight:300;color:var(--ink);cursor:pointer;}

.family-checks{display:flex;flex-wrap:wrap;gap:8px 12px;margin-bottom:1.8rem;}
.family-check-item{display:flex;align-items:center;gap:7px;font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:300;color:var(--ink2);cursor:pointer;padding:6px 14px;border:1px solid var(--rule);transition:all .2s;}
.family-check-item:has(input:checked){border-color:var(--ink);color:var(--ink);}
.family-check-item input{width:12px;height:12px;accent-color:var(--ink);border:none;background:transparent;padding:0;flex-shrink:0;}
.family-names-block{animation:fadeUp .3s ease both;}
.family-names-hint{font-family:'Montserrat',sans-serif;font-size:10px;font-weight:300;letter-spacing:.15em;color:var(--ink3);margin-bottom:1.4rem;font-style:italic;}

.add-row{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1.5rem;margin-bottom:1.5rem}
.add-row2{display:grid;grid-template-columns:1fr 1fr;gap:2rem;margin-bottom:1.5rem}

.nav{display:flex;justify-content:space-between;align-items:center;padding-top:2.5rem;margin-top:1rem;border-top:1px solid var(--rule-light);}
.btn{font-family:'Montserrat',sans-serif;font-size:9px;font-weight:400;letter-spacing:.28em;text-transform:uppercase;padding:13px 32px;border:1px solid var(--ink);background:transparent;color:var(--ink);cursor:pointer;transition:all .25s;}
.btn:hover{background:var(--ink);color:var(--white)}
.btn-inv{background:var(--ink);color:var(--white)}
.btn-inv:hover{background:var(--ink2);border-color:var(--ink2)}
.btn-ghost{border-color:var(--rule);color:var(--ink3)}
.btn-ghost:hover{background:transparent;border-color:var(--ink2);color:var(--ink2)}
.btn-sm{padding:9px 20px;font-size:8px}

.confirm-box{border:1px solid var(--rule);padding:2.5rem 2rem;text-align:center;margin-top:2.5rem;}
.confirm-title{font-size:24px;font-weight:300;color:var(--ink);margin-bottom:12px;}
.confirm-text{font-family:'Montserrat',sans-serif;font-size:12px;font-weight:300;color:var(--ink3);line-height:1.9;margin-bottom:2rem;}
.confirm-email-wrap{max-width:340px;margin:0 auto 2rem}
.status{font-family:'Montserrat',sans-serif;font-size:11px;font-weight:300;color:var(--ink2);margin-top:16px;line-height:1.7;min-height:20px;}

.sum-block{margin-bottom:2rem}
.sum-block-title{font-family:'Montserrat',sans-serif;font-size:9px;font-weight:400;letter-spacing:.28em;color:var(--ink3);text-transform:uppercase;padding-bottom:10px;border-bottom:1px solid var(--rule);margin-bottom:14px;}
.sum-row{display:flex;justify-content:space-between;align-items:flex-start;padding:6px 0;border-bottom:1px solid var(--rule-light);gap:1rem;}
.sum-row:last-child{border-bottom:none}
.sum-lbl{font-family:'Montserrat',sans-serif;font-size:10px;font-weight:300;letter-spacing:.1em;color:var(--ink3);min-width:140px;padding-top:2px;}
.sum-val{font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:300;color:var(--ink);text-align:right;line-height:1.5;}

@media(max-width:560px){
  .page{padding:2rem 1.2rem 4rem}
  .g2,.g3{grid-template-columns:1fr}
  .add-row{grid-template-columns:1fr}.add-row2{grid-template-columns:1fr}
  .step-title{font-size:28px}.logo-sans{font-size:16px}.logo-serif{font-size:28px}
  .family-checks{gap:6px 8px}
}
</style>
</head>
<body>
<div class="page">

  <div class="logo-wrap">
    <div class="logo-line1">
      <span class="logo-sans">O S C A R &nbsp; +</span>
      <span class="logo-serif">Ana</span>
    </div>
    <div class="logo-rule"></div>
    <div class="logo-sub">The Planners &nbsp;&bull;&nbsp; Event Management</div>
  </div>

  <div class="progress-wrap">
    <div class="progress-track"><div class="progress-fill" id="prog" style="width:12.5%"></div></div>
    <div class="progress-meta">
      <div class="progress-dots" id="dotsRow">
        <div class="pdot active"></div><div class="pdot"></div><div class="pdot"></div>
        <div class="pdot"></div><div class="pdot"></div><div class="pdot"></div>
        <div class="pdot"></div><div class="pdot"></div>
      </div>
      <span class="progress-num" id="stepCount">01 / 08</span>
    </div>
  </div>

  <!-- S1 -->
  <div class="step active" id="s1">
    <div class="step-eyebrow">Paso 01</div>
    <div class="step-title">Datos generales</div>
    <div class="step-sub">La información base de su boda</div>
    <div class="section">
      <div class="section-label">Los novios</div>
      <div class="g2">
        <div class="field"><label>Nombre de la novia</label><input id="bride" type="text" placeholder="Nombre completo"></div>
        <div class="field"><label>Nombre del novio</label><input id="groom" type="text" placeholder="Nombre completo"></div>
      </div>
    </div>
    <div class="section">
      <div class="section-label">¿Qué eventos tendrán?</div>
      <div class="field">
        <label>Seleccionen todos los que apliquen</label>
        <div class="check-list" id="eventChecks">
          <label class="check-item"><input type="checkbox" value="civil" onchange="onEventChange()"> Ceremonia civil</label>
          <label class="check-item"><input type="checkbox" value="catolica" onchange="onEventChange()"> Ceremonia religiosa católica</label>
          <label class="check-item"><input type="checkbox" value="cristiana" onchange="onEventChange()"> Ceremonia religiosa cristiana</label>
          <label class="check-item"><input type="checkbox" value="recepcion" onchange="onEventChange()"> Recepción</label>
        </div>
      </div>
      <div id="eventTimes"></div>
    </div>
  </div>

  <!-- S2 -->
  <div class="step" id="s2">
    <div class="step-eyebrow">Paso 02</div>
    <div class="step-title">Círculo cercano</div>
    <div class="step-sub">Cuéntenle al equipo quiénes son las personas más importantes en su día</div>

    <div class="section">
      <div class="section-label">Familia de la novia</div>
      <div class="field">
        <label>¿Quiénes conforman el círculo cercano de la novia?</label>
        <div class="family-checks" id="brideCircleChecks">
          <label class="family-check-item"><input type="checkbox" value="bFather" onchange="buildFamilyNames('bride')"> Papá</label>
          <label class="family-check-item"><input type="checkbox" value="bMother" onchange="buildFamilyNames('bride')"> Mamá</label>
          <label class="family-check-item"><input type="checkbox" value="bBrothers" onchange="buildFamilyNames('bride')"> Hermanos</label>
          <label class="family-check-item"><input type="checkbox" value="bSisters" onchange="buildFamilyNames('bride')"> Hermanas</label>
          <label class="family-check-item"><input type="checkbox" value="bKids" onchange="buildFamilyNames('bride')"> Hijos</label>
        </div>
      </div>
      <div id="brideNamesBlock"></div>
    </div>

    <div class="section">
      <div class="section-label">Familia del novio</div>
      <div class="field">
        <label>¿Quiénes conforman el círculo cercano del novio?</label>
        <div class="family-checks" id="groomCircleChecks">
          <label class="family-check-item"><input type="checkbox" value="gFather" onchange="buildFamilyNames('groom')"> Papá</label>
          <label class="family-check-item"><input type="checkbox" value="gMother" onchange="buildFamilyNames('groom')"> Mamá</label>
          <label class="family-check-item"><input type="checkbox" value="gBrothers" onchange="buildFamilyNames('groom')"> Hermanos</label>
          <label class="family-check-item"><input type="checkbox" value="gSisters" onchange="buildFamilyNames('groom')"> Hermanas</label>
          <label class="family-check-item"><input type="checkbox" value="gKids" onchange="buildFamilyNames('groom')"> Hijos</label>
        </div>
      </div>
      <div id="groomNamesBlock"></div>
    </div>
  </div>

  <!-- S3 -->
  <div class="step" id="s3">
    <div class="step-eyebrow">Paso 03</div>
    <div class="step-title">Fotografías</div>
    <div class="step-sub">Agreguen sus peticiones especiales para cada momento</div>
    <div class="section">
      <div class="section-label">Getting Ready — Novia</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_bride" placeholder="Momentos que desean capturar durante el getting ready de la novia..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Getting Ready — Novio</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_groom" placeholder="Momentos que desean capturar durante el getting ready del novio..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Ceremonia</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_ceremony" placeholder="Momentos específicos que desean capturar durante la ceremonia..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Sesión de esposos</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_couple" placeholder="Tomas, poses o locaciones que desean para su sesión..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Fotos con familias</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_family" placeholder="Grupos familiares específicos, combinaciones, personas que no pueden faltar..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Recepción</div>
      <div class="field"><label>Peticiones especiales</label><textarea id="ptExtra_reception" placeholder="Momentos de la recepción que desean capturar..."></textarea></div>
    </div>
  </div>

  <!-- S4 -->
  <div class="step" id="s4">
    <div class="step-eyebrow">Paso 04</div>
    <div class="step-title">Música</div>
    <div class="step-sub">Las canciones que acompañarán cada momento de su día</div>
    <div class="section">
      <div class="section-label">Entrada y primer baile</div>
      <div class="g2">
        <div class="field"><label>Canción de entrada — artista</label><input id="entrArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Canción de entrada — título</label><input id="entrSong" type="text" placeholder="Nombre de la canción"></div>
      </div>
      <div class="g2">
        <div class="field"><label>Primer baile — artista</label><input id="firstArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Primer baile — título</label><input id="firstSong" type="text" placeholder="Nombre de la canción"></div>
      </div>
      <div class="field"><label>¿Cuándo será el primer baile?</label>
        <select id="firstWhen">
          <option value="">Seleccionar...</option>
          <option>Justo después de la entrada</option>
          <option>Después de la cena</option>
          <option>En cualquier momento</option>
        </select>
      </div>
    </div>
    <div class="section">
      <div class="section-label">Vals con familia</div>
      <div id="parentDanceFields"><p style="font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:300;color:var(--ink3)">Completen el círculo cercano en el paso 2 para configurar los vals.</p></div>
    </div>
    <div class="section">
      <div class="section-label">Momentos especiales</div>
      <div class="g2">
        <div class="field"><label>Corte de pastel — artista</label><input id="cakeArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Corte de pastel — canción</label><input id="cakeSong" type="text" placeholder="Canción"></div>
      </div>
      <div class="g2">
        <div class="field"><label>Apertura de pista — artista</label><input id="danceArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Apertura de pista — canción</label><input id="danceSong" type="text" placeholder="Canción"></div>
      </div>
      <div class="g2">
        <div class="field"><label>Última canción — artista</label><input id="lastArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Última canción — título</label><input id="lastSong" type="text" placeholder="Canción"></div>
      </div>
    </div>
    <div class="section">
      <div class="section-label">Preferencias generales</div>
      <div class="field"><label>Géneros y artistas que les gustan</label><textarea id="musicLike" placeholder="Ej. Pop en español, reggaetón, baladas, Maluma, Bad Bunny..."></textarea></div>
      <div class="field"><label>Canciones o géneros que no quieren</label><textarea id="musicNope" placeholder="Ej. Cumbia, rock pesado..."></textarea></div>
      <div class="field"><label>¿Permiten solicitudes del público?</label>
        <select id="requests">
          <option value="">Seleccionar...</option>
          <option>Sí</option><option>No</option><option>Solo algunas</option>
        </select>
      </div>
      <div class="field"><label>Link de Spotify / Apple Music (opcional)</label><input id="playlist" type="text" placeholder="https://..."></div>
    </div>
  </div>

  <!-- S5 -->
  <div class="step" id="s5">
    <div class="step-eyebrow">Paso 05</div>
    <div class="step-title">Recepción</div>
    <div class="step-sub">Cena, discursos y dinámica del evento</div>
    <div class="section">
      <div class="section-label">Presentación de los novios</div>
      <div class="field"><label>¿Cómo desean que los anuncien?</label><textarea id="announce" placeholder="Ej. Por primera vez como esposos, ¡Ana Martínez y Óscar Salcedo!"></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Cena</div>
      <div class="g2">
        <div class="field"><label>Tipo de servicio</label>
          <select id="dinnerType">
            <option value="">Seleccionar...</option>
            <option>Buffet</option><option>Plato servido</option><option>Estaciones</option><option>Mixto</option>
          </select>
        </div>
        <div class="field"><label>Música durante la cena</label><input id="dinnerMusic" type="text" placeholder="Tipo de música, artistas..."></div>
      </div>
      <div id="prayerBlock" class="hidden" style="margin-top:1.5rem">
        <div class="g2">
          <div class="field"><label>¿Habrá oración antes de cenar?</label>
            <select id="prayer"><option value="">Seleccionar...</option><option>Sí</option><option>No</option></select>
          </div>
          <div class="field"><label>¿Quién realizará la oración?</label><input id="prayerWho" type="text" placeholder="Nombre y relación"></div>
        </div>
      </div>
    </div>
    <div class="section">
      <div class="section-label">Discursos / brindis</div>
      <div id="speeches"></div>
      <button class="btn btn-ghost btn-sm" onclick="addSpeech()" style="margin-top:10px">+ Agregar discurso</button>
    </div>
    <div class="section">
      <div class="section-label">Observaciones para el DJ / animador</div>
      <div class="field"><textarea id="djNotes" placeholder="Momentos especiales, señales, indicaciones importantes..."></textarea></div>
    </div>
  </div>

  <!-- S6: solo si hay ceremonia religiosa -->
  <div class="step" id="s6">
    <div class="step-eyebrow">Paso 06</div>
    <div class="step-title">Ceremonia religiosa</div>
    <div class="step-sub">Padrinos y testigos</div>
    <div id="ceremonyBlock"></div>
  </div>

  <!-- S7 -->
  <div class="step" id="s7">
    <div class="step-eyebrow">Paso 07</div>
    <div class="step-title">Momentos especiales</div>
    <div class="step-sub">Los detalles que hacen único su día</div>
    <div class="section">
      <div class="section-label">Dinámicas</div>
      <div class="g2">
        <div class="field"><label>¿Habrá lanzamiento de ramo?</label>
          <select id="bouquet"><option value="">Seleccionar...</option><option>Sí</option><option>No</option></select>
        </div>
        <div class="field"><label>¿Habrá lanzamiento de liga?</label>
          <select id="garter"><option value="">Seleccionar...</option><option>Sí</option><option>No</option></select>
        </div>
      </div>
    </div>
    <div class="section">
      <div class="section-label">Sorpresas o momentos especiales</div>
      <div class="field"><textarea id="surprises" placeholder="Videos sorpresa, performance, entradas especiales, juegos con invitados..."></textarea></div>
    </div>
    <div class="section">
      <div class="section-label">Notas para el equipo</div>
      <div class="field"><label>Para el fotógrafo / videógrafo</label><textarea id="photoNotes" placeholder="Momentos clave, personas especiales, locaciones, timing..."></textarea></div>
      <div class="field"><label>Para la coordinadora</label><textarea id="plannerNotes" placeholder="Cualquier detalle adicional que quieran que tengamos en cuenta..."></textarea></div>
    </div>
  </div>

  <!-- S8 -->
  <div class="step" id="s8">
    <div class="step-eyebrow">Paso 08</div>
    <div class="step-title">Enviar a The Planners</div>
    <div class="step-sub">Su formato está listo. Revísenlo y envíenlo a nuestro equipo.</div>
    <div id="summaryContent"></div>
    <div class="confirm-box">
      <div class="confirm-title">Todo listo</div>
      <p class="confirm-text">Al presionar el botón, su formato completo llegará directamente<br>a nuestro equipo. Nos pondremos en contacto con ustedes pronto.</p>
      <div class="confirm-email-wrap">
        <div class="field"><label>Su correo electrónico (para confirmación)</label><input type="email" id="clientEmail" placeholder="correo@ejemplo.com"></div>
      </div>
      <button class="btn btn-inv" id="sendBtn" onclick="sendToPlanner()">Enviar a The Planners</button>
      <div class="status" id="sendStatus"></div>
    </div>
  </div>

  <div class="nav">
    <button class="btn btn-ghost" id="prevBtn" onclick="navigate(-1)" style="visibility:hidden">← Anterior</button>
    <button class="btn btn-inv" id="nextBtn" onclick="navigate(1)">Siguiente</button>
  </div>

</div>

<script>
const TOTAL=8; let cur=1; let scCnt=0; let padCnt=0;

function getEvents(){return Array.from(document.querySelectorAll('#eventChecks input:checked')).map(c=>c.value);}
function hasReligiosa(){const ev=getEvents();return ev.includes('catolica')||ev.includes('cristiana');}
function gv(id){const e=document.getElementById(id);return e&&e.value&&e.value.trim()?e.value.trim():'';}

// S1
function onEventChange(){
  const sel=getEvents();
  const labels={civil:'Ceremonia civil',catolica:'Ceremonia religiosa católica',cristiana:'Ceremonia religiosa cristiana',recepcion:'Recepción'};
  const order=['civil','catolica','cristiana','recepcion'];
  let html='';
  order.forEach(v=>{
    if(!sel.includes(v))return;
    html+=`<div style="margin-top:1.8rem"><div style="font-family:'Montserrat',sans-serif;font-size:9px;letter-spacing:.2em;color:#8a8a85;text-transform:uppercase;margin-bottom:1rem">${labels[v]}</div>`;
    html+=`<div class="g2"><div class="field"><label>Lugar</label><input id="loc_${v}" type="text" placeholder="Nombre y dirección"></div>`;
    html+=`<div class="field"><label>Hora de inicio</label><input id="start_${v}" type="time"></div></div>`;
    if(v==='recepcion')html+=`<div class="field" style="max-width:200px;margin-top:1.5rem"><label>Hora de fin</label><input id="end_${v}" type="time"></div>`;
    html+=`</div>`;
  });
  document.getElementById('eventTimes').innerHTML=html;
}

// S2
const familyConfig={
  bride:{
    checksId:'brideCircleChecks',blockId:'brideNamesBlock',
    fields:{
      bFather:{label:'Nombre del papá de la novia',placeholder:'Nombre completo',type:'input'},
      bMother:{label:'Nombre de la mamá de la novia',placeholder:'Nombre completo',type:'input'},
      bBrothers:{label:'Hermanos de la novia',placeholder:'Ej: Alberto, Ramón y su pareja Yessica',type:'textarea'},
      bSisters:{label:'Hermanas de la novia',placeholder:'Ej: Sofía, María y su esposo Luis',type:'textarea'},
      bKids:{label:'Hijos de la novia',placeholder:'Nombres separados por coma',type:'textarea'},
    }
  },
  groom:{
    checksId:'groomCircleChecks',blockId:'groomNamesBlock',
    fields:{
      gFather:{label:'Nombre del papá del novio',placeholder:'Nombre completo',type:'input'},
      gMother:{label:'Nombre de la mamá del novio',placeholder:'Nombre completo',type:'input'},
      gBrothers:{label:'Hermanos del novio',placeholder:'Ej: Carlos, Emilio y su pareja Andrea',type:'textarea'},
      gSisters:{label:'Hermanas del novio',placeholder:'Ej: Daniela, Valeria',type:'textarea'},
      gKids:{label:'Hijos del novio',placeholder:'Nombres separados por coma',type:'textarea'},
    }
  }
};

function buildFamilyNames(who){
  const cfg=familyConfig[who];
  const checked=Array.from(document.querySelectorAll(`#${cfg.checksId} input:checked`)).map(c=>c.value);
  const block=document.getElementById(cfg.blockId);
  if(!checked.length){block.innerHTML='';return;}
  const saved={};
  Object.keys(cfg.fields).forEach(id=>{const el=document.getElementById(id);if(el)saved[id]=el.value;});
  let html='<div class="family-names-block"><p class="family-names-hint">Completen los nombres de quienes seleccionaron</p>';
  for(let i=0;i<checked.length;i+=2){
    const pair=checked.slice(i,i+2);
    if(pair.length===2)html+='<div class="g2">';
    pair.forEach(key=>{
      const f=cfg.fields[key];
      html+=`<div class="field"><label>${f.label}</label>`;
      if(f.type==='textarea')html+=`<textarea id="${key}" placeholder="${f.placeholder}">${saved[key]||''}</textarea>`;
      else html+=`<input id="${key}" type="text" placeholder="${f.placeholder}" value="${(saved[key]||'').replace(/"/g,'&quot;')}">`;
      html+=`</div>`;
    });
    if(pair.length===2)html+='</div>';
  }
  html+='</div>';
  block.innerHTML=html;
}

// S4: vals con base en círculo cercano
function buildParentDances(){
  const bFather=gv('bFather');
  const bMother=gv('bMother');
  const gFather=gv('gFather');
  const gMother=gv('gMother');
  const brideChecked=Array.from(document.querySelectorAll('#brideCircleChecks input:checked')).map(c=>c.value);
  const groomChecked=Array.from(document.querySelectorAll('#groomCircleChecks input:checked')).map(c=>c.value);
  let html='';

  if(brideChecked.includes('bFather')){
    html+=`<div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novia y papá</div>
      <div class="g3">
        <div class="field"><label>Artista</label><input id="bdadArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Canción</label><input id="bdadSong" type="text" placeholder="Canción"></div>
        <div class="field"><label>Nombre del papá</label><input id="bdadName" type="text" placeholder="${bFather||'Nombre completo'}" value="${bFather}"></div>
      </div></div>`;
  }
  if(brideChecked.includes('bMother')){
    html+=`<div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novia y mamá</div>
      <div class="g3">
        <div class="field"><label>Artista</label><input id="bmomArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Canción</label><input id="bmomSong" type="text" placeholder="Canción"></div>
        <div class="field"><label>Nombre de la mamá</label><input id="bmomName" type="text" placeholder="${bMother||'Nombre completo'}" value="${bMother}"></div>
      </div></div>`;
  }
  if(groomChecked.includes('gFather')){
    html+=`<div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novio y papá</div>
      <div class="g3">
        <div class="field"><label>Artista</label><input id="gdadArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Canción</label><input id="gdadSong" type="text" placeholder="Canción"></div>
        <div class="field"><label>Nombre del papá</label><input id="gdadName" type="text" placeholder="${gFather||'Nombre completo'}" value="${gFather}"></div>
      </div></div>`;
  }
  if(groomChecked.includes('gMother')){
    html+=`<div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novio y mamá</div>
      <div class="g3">
        <div class="field"><label>Artista</label><input id="gmomArt" type="text" placeholder="Artista"></div>
        <div class="field"><label>Canción</label><input id="gmomSong" type="text" placeholder="Canción"></div>
        <div class="field"><label>Nombre de la mamá</label><input id="gmomName" type="text" placeholder="${gMother||'Nombre completo'}" value="${gMother}"></div>
      </div></div>`;
  }
  if(!html){
    html+=`<div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novia — persona especial</div>
      <div class="field"><label>¿Con quién bailará la novia?</label>
        <select id="brideSpecialDance" onchange="toggleSpecialDance('bride')">
          <option value="">Seleccionar...</option>
          <option value="si">Sí, bailará con alguien especial</option>
          <option value="no">No habrá vals para la novia</option>
        </select>
      </div>
      <div id="brideSpecialFields" class="hidden">
        <div class="g3">
          <div class="field"><label>¿Con quién?</label><input id="brideSpecialWho" type="text" placeholder="Nombre y relación"></div>
          <div class="field"><label>Artista</label><input id="brideSpecialArt" type="text" placeholder="Artista"></div>
          <div class="field"><label>Canción</label><input id="brideSpecialSong" type="text" placeholder="Canción"></div>
        </div>
      </div>
    </div>
    <div style="margin-bottom:2rem">
      <div class="section-label" style="margin-bottom:1rem">Vals novio — persona especial</div>
      <div class="field"><label>¿Con quién bailará el novio?</label>
        <select id="groomSpecialDance" onchange="toggleSpecialDance('groom')">
          <option value="">Seleccionar...</option>
          <option value="si">Sí, bailará con alguien especial</option>
          <option value="no">No habrá vals para el novio</option>
        </select>
      </div>
      <div id="groomSpecialFields" class="hidden">
        <div class="g3">
          <div class="field"><label>¿Con quién?</label><input id="groomSpecialWho" type="text" placeholder="Nombre y relación"></div>
          <div class="field"><label>Artista</label><input id="groomSpecialArt" type="text" placeholder="Artista"></div>
          <div class="field"><label>Canción</label><input id="groomSpecialSong" type="text" placeholder="Canción"></div>
        </div>
      </div>
    </div>`;
  }
  document.getElementById('parentDanceFields').innerHTML=html;
}

function toggleSpecialDance(who){
  const sel=document.getElementById(who+'SpecialDance');
  const fields=document.getElementById(who+'SpecialFields');
  if(sel&&fields)fields.classList.toggle('hidden',sel.value!=='si');
}

// S5
function updatePrayerBlock(){
  document.getElementById('prayerBlock').classList.toggle('hidden',!hasReligiosa());
}

// S6
function buildCeremonyBlock(){
  const ev=getEvents();
  let html='';
  if(ev.includes('civil')){
    html+=`<div class="section"><div class="section-label">Testigos — ceremonia civil</div>
      <div class="g2">
        <div class="field"><label>Testigo 1 de la novia</label><input id="tBride1" type="text" placeholder="Nombre completo"></div>
        <div class="field"><label>Testigo 2 de la novia</label><input id="tBride2" type="text" placeholder="Nombre completo"></div>
      </div>
      <div class="g2">
        <div class="field"><label>Testigo 1 del novio</label><input id="tGroom1" type="text" placeholder="Nombre completo"></div>
        <div class="field"><label>Testigo 2 del novio</label><input id="tGroom2" type="text" placeholder="Nombre completo"></div>
      </div>
    </div>`;
  }
  if(ev.includes('catolica')||ev.includes('cristiana')){
    html+=`<div class="section"><div class="section-label">Padrinos — ceremonia religiosa</div>
      <div id="padList"></div>
      <button class="btn btn-ghost btn-sm" onclick="addPadrino()" style="margin-top:10px">+ Agregar padrino / madrina</button>
    </div>`;
  }
  if(!html)html=`<div class="section"><p style="font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:300;color:var(--ink3)">No seleccionaron ninguna ceremonia en el paso 1.</p></div>`;
  document.getElementById('ceremonyBlock').innerHTML=html;
  if(ev.includes('catolica')||ev.includes('cristiana')){addPadrino();addPadrino();addPadrino();}
}

function addPadrino(){
  padCnt++;
  const c=document.getElementById('padList');if(!c)return;
  const d=document.createElement('div');d.className='add-row2';
  d.innerHTML=`<input type="text" placeholder="Nombre del padrino / madrina" id="padName${padCnt}"><input type="text" placeholder="Tipo (arras, lazo, biblia...)" id="padType${padCnt}">`;
  c.appendChild(d);
}

function addSpeech(){
  scCnt++;
  const d=document.createElement('div');d.className='add-row';d.style.marginBottom='1.5rem';
  d.innerHTML=`<input type="text" placeholder="Nombre" id="spName${scCnt}"><input type="text" placeholder="Relación con los novios" id="spRole${scCnt}"><input type="text" placeholder="Hora aprox." id="spTime${scCnt}">`;
  document.getElementById('speeches').appendChild(d);
}
addSpeech();addSpeech();

// Navegación — salta paso 6 si no hay ceremonia religiosa
function getNextStep(from,dir){
  let next=from+dir;
  if(next===6&&!hasReligiosa())next+=dir;
  return Math.min(Math.max(next,1),TOTAL);
}

function navigate(dir){
  document.getElementById('s'+cur).classList.remove('active');
  cur=getNextStep(cur,dir);
  if(cur===4)buildParentDances();
  if(cur===5)updatePrayerBlock();
  if(cur===6)buildCeremonyBlock();
  if(cur===8)buildSummary();
  document.getElementById('s'+cur).classList.add('active');
  document.getElementById('prog').style.width=(cur/TOTAL*100)+'%';
  document.getElementById('stepCount').textContent=(cur<10?'0'+cur:cur)+' / 0'+TOTAL;
  const dots=document.querySelectorAll('.pdot');
  dots.forEach((d,i)=>{d.classList.remove('active','done');if(i===cur-1)d.classList.add('active');else if(i<cur-1)d.classList.add('done');});
  document.getElementById('prevBtn').style.visibility=cur>1?'visible':'hidden';
  const nb=document.getElementById('nextBtn');
  if(cur===TOTAL){nb.style.display='none';}
  else{nb.style.display='';nb.textContent=cur===TOTAL-1?'Ver resumen':'Siguiente';}
  window.scrollTo({top:0,behavior:'smooth'});
}

// Resumen
function buildTextSummary(){
  const ev=getEvents();
  const evL={civil:'Civil',catolica:'Religiosa católica',cristiana:'Religiosa cristiana',recepcion:'Recepción'};
  let sp='';
  for(let i=1;i<=scCnt;i++){const n=gv('spName'+i),r=gv('spRole'+i),t=gv('spTime'+i);if(n)sp+=`${n} (${r}) a las ${t}; `;}
  let pad='';
  for(let i=1;i<=padCnt;i++){const n=gv('padName'+i),t=gv('padType'+i);if(n)pad+=`${n} — ${t}; `;}
  const bride=gv('bride')||'—';
  const groom=gv('groom')||'—';
  let txt=`FORMATO DE BODA\n${bride.toUpperCase()} & ${groom.toUpperCase()}\n${'─'.repeat(50)}\n\n`;
  txt+=`DATOS GENERALES\nNovia: ${bride}\nNovio: ${groom}\nEventos: ${ev.map(v=>evL[v]).join(', ')||'—'}\n`;
  ev.forEach(v=>{txt+=`Lugar ${evL[v]}: ${gv('loc_'+v)||'—'}\nHorario ${evL[v]}: ${gv('start_'+v)||'—'}${v==='recepcion'&&gv('end_'+v)?' – '+gv('end_'+v):''}\n`;});
  txt+=`\nFAMILIA DE LA NOVIA\nPadre: ${gv('bFather')||'—'}\nMadre: ${gv('bMother')||'—'}\nHermanos: ${gv('bBrothers')||'—'}\nHermanas: ${gv('bSisters')||'—'}\nHijos: ${gv('bKids')||'—'}\nOtros: ${gv('bOthers')||'—'}\n`;
  txt+=`\nFAMILIA DEL NOVIO\nPadre: ${gv('gFather')||'—'}\nMadre: ${gv('gMother')||'—'}\nHermanos: ${gv('gBrothers')||'—'}\nHermanas: ${gv('gSisters')||'—'}\nHijos: ${gv('gKids')||'—'}\nOtros: ${gv('gOthers')||'—'}\n`;
  txt+=`\nFOTOGRAFÍAS\nGetting Ready Novia: ${gv('ptExtra_bride')||'—'}\nGetting Ready Novio: ${gv('ptExtra_groom')||'—'}\nCeremonia: ${gv('ptExtra_ceremony')||'—'}\nSesión esposos: ${gv('ptExtra_couple')||'—'}\nFamilias: ${gv('ptExtra_family')||'—'}\nRecepción: ${gv('ptExtra_reception')||'—'}\n`;
  txt+=`\nMÚSICA\nEntrada: ${gv('entrArt')||'—'} — ${gv('entrSong')||'—'}\nPrimer baile: ${gv('firstArt')||'—'} — ${gv('firstSong')||'—'}\nCuándo: ${gv('firstWhen')||'—'}\n`;
  if(gv('bdadArt')||gv('bdadSong')||gv('bdadName'))txt+=`Vals novia y papá: ${gv('bdadArt')||'—'} — ${gv('bdadSong')||'—'} (${gv('bdadName')||'—'})\n`;
  if(gv('bmomArt')||gv('bmomSong')||gv('bmomName'))txt+=`Vals novia y mamá: ${gv('bmomArt')||'—'} — ${gv('bmomSong')||'—'} (${gv('bmomName')||'—'})\n`;
  if(gv('gdadArt')||gv('gdadSong')||gv('gdadName'))txt+=`Vals novio y papá: ${gv('gdadArt')||'—'} — ${gv('gdadSong')||'—'} (${gv('gdadName')||'—'})\n`;
  if(gv('gmomArt')||gv('gmomSong')||gv('gmomName'))txt+=`Vals novio y mamá: ${gv('gmomArt')||'—'} — ${gv('gmomSong')||'—'} (${gv('gmomName')||'—'})\n`;
  if(gv('brideSpecialWho'))txt+=`Vals novia con persona especial: ${gv('brideSpecialWho')} — ${gv('brideSpecialArt')||'—'} — ${gv('brideSpecialSong')||'—'}\n`;
  if(gv('groomSpecialWho'))txt+=`Vals novio con persona especial: ${gv('groomSpecialWho')} — ${gv('groomSpecialArt')||'—'} — ${gv('groomSpecialSong')||'—'}\n`;
  txt+=`Corte pastel: ${gv('cakeArt')||'—'} — ${gv('cakeSong')||'—'}\nApertura pista: ${gv('danceArt')||'—'} — ${gv('danceSong')||'—'}\nÚltima canción: ${gv('lastArt')||'—'} — ${gv('lastSong')||'—'}\nLes gusta: ${gv('musicLike')||'—'}\nNo quieren: ${gv('musicNope')||'—'}\nSolicitudes: ${gv('requests')||'—'}\nPlaylist: ${gv('playlist')||'—'}\n`;
  txt+=`\nRECEPCIÓN\nAnuncio: ${gv('announce')||'—'}\nTipo de cena: ${gv('dinnerType')||'—'}\nMúsica cena: ${gv('dinnerMusic')||'—'}\n`;
  if(hasReligiosa())txt+=`Oración: ${gv('prayer')||'—'} — ${gv('prayerWho')||'—'}\n`;
  txt+=`Discursos: ${sp||'—'}\nNotas DJ: ${gv('djNotes')||'—'}\n`;
  if(ev.includes('civil'))txt+=`\nTESTIGOS CIVIL\nNovia T1: ${gv('tBride1')||'—'}, T2: ${gv('tBride2')||'—'}\nNovio T1: ${gv('tGroom1')||'—'}, T2: ${gv('tGroom2')||'—'}\n`;
  if(pad)txt+=`\nPADRINOS\n${pad}\n`;
  txt+=`\nMOMENTOS ESPECIALES\nLanzamiento de ramo: ${gv('bouquet')||'—'}\nLanzamiento de liga: ${gv('garter')||'—'}\nSorpresas: ${gv('surprises')||'—'}\nNotas fotógrafo: ${gv('photoNotes')||'—'}\nNotas coordinadora: ${gv('plannerNotes')||'—'}\n`;
  txt+=`\nCorreo de los novios: ${gv('clientEmail')||'—'}\n`;
  return txt;
}

function buildSummary(){
  const txt=buildTextSummary();
  const lines=txt.split('\n');
  let html='';let inBlock=false;
  const headers=['DATOS GENERALES','FAMILIA DE LA NOVIA','FAMILIA DEL NOVIO','FOTOGRAFÍAS','MÚSICA','RECEPCIÓN','TESTIGOS CIVIL','PADRINOS','MOMENTOS ESPECIALES'];
  lines.forEach(line=>{
    if(!line.trim())return;
    const isHeader=headers.some(h=>line.startsWith(h))||(/^[A-ZÁÉÍÓÚÑ\s—&\-]+$/.test(line)&&line.length>4&&!line.includes(':'));
    if(isHeader){
      if(inBlock)html+='</div>';
      html+=`<div class="sum-block"><div class="sum-block-title">${line}</div>`;
      inBlock=true;
    } else if(line.includes(':')){
      const idx=line.indexOf(':');
      const lbl=line.substring(0,idx).trim();
      const val=line.substring(idx+1).trim();
      if(val&&val!=='—'&&val!=='— — —')html+=`<div class="sum-row"><span class="sum-lbl">${lbl}</span><span class="sum-val">${val}</span></div>`;
    }
  });
  if(inBlock)html+='</div>';
  document.getElementById('summaryContent').innerHTML=html;
}

// Envío Formspree
async function sendToPlanner(){
  const st=document.getElementById('sendStatus');
  const btn=document.getElementById('sendBtn');
  const email=gv('clientEmail');
  if(!email||!email.includes('@')){st.textContent='Por favor ingresa tu correo electrónico.';return;}
  st.textContent='Enviando...';
  btn.disabled=true;btn.style.opacity='0.5';
  const summary=buildTextSummary();
  const bride=gv('bride')||'—';
  const groom=gv('groom')||'—';
  try{
    const resp=await fetch('https://formspree.io/f/mojrdvvb',{
      method:'POST',
      headers:{'Content-Type':'application/json','Accept':'application/json'},
      body:JSON.stringify({
        _subject:`Formato de boda — ${bride} & ${groom}`,
        _replyto:email,
        novios:`${bride} & ${groom}`,
        correo_novios:email,
        formato_completo:summary
      })
    });
    const data=await resp.json();
    if(data.ok){
      st.style.color='var(--ink)';
      st.innerHTML='✓ &nbsp;Formato enviado. El equipo de The Planners se pondrá en contacto pronto.';
    } else {
      st.textContent='Hubo un problema. Por favor intenta de nuevo.';
      btn.disabled=false;btn.style.opacity='1';
    }
  } catch(e){
    st.textContent='Error de conexión. Intenta de nuevo o escríbenos a hola@theplannersmx.com';
    btn.disabled=false;btn.style.opacity='1';
  }
}
</script>
</body>
</html>
