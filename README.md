<!DOCTYPE html>
<html lang="pt-BR" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Felix Beauty Studio — alisamento, coloração e corte em Guarulhos</title>
<meta name="description" content="Progressiva, botox capilar, alisamento, coloração e cortes em Guarulhos. Atendimento por hora marcada.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Gloock&family=Karla:ital,wght@0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">
<style>
  :root{
    --carvao:#111010;
    --painel:#1B1917;
    --leite:#F3EDE2;
    --suave:#B3A895;
    --linha:#33302B;
    --ouro:#C9A227;
    --ouro-claro:#E8CE7A;
    --tom:#C9A227;
    --tom-claro:#E8CE7A;
    --raio:2px;
    --serif:"Gloock", Georgia, "Times New Roman", serif;
    --sans:"Karla", "Helvetica Neue", Arial, sans-serif;
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    margin:0;
    background:var(--carvao);
    color:var(--leite);
    font-family:var(--sans);
    font-size:17px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img{max-width:100%}
  a{color:inherit}
  h1,h2,h3{font-family:var(--serif);font-weight:400;line-height:1.05;margin:0}
  h1{font-size:clamp(2.6rem,7.5vw,5.2rem);letter-spacing:-0.015em}
  h2{font-size:clamp(1.9rem,4.2vw,3rem)}
  h3{font-size:1.3rem}
  p{margin:0 0 1rem}
  .env{width:min(1120px,100% - 2.5rem);margin-inline:auto}
  .faixa{padding:clamp(3.5rem,9vw,7rem) 0}
  :focus-visible{outline:2.5px solid var(--ouro);outline-offset:3px}

  /* topo */
  .topo{
    position:sticky;top:0;z-index:20;
    background:color-mix(in srgb, var(--carvao) 88%, transparent);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--linha);
  }
  .topo .env{display:flex;align-items:center;gap:1.5rem;min-height:68px}
  .marca{font-family:var(--serif);font-size:1.3rem;text-decoration:none;letter-spacing:.01em;line-height:1}
  .marca span{color:var(--ouro)}
  .menu{margin-left:auto;display:flex;gap:1.6rem;font-size:.95rem}
  .menu a{text-decoration:none;padding-block:.3rem;border-bottom:1px solid transparent}
  .menu a:hover{border-bottom-color:var(--ouro)}
  .btn{
    display:inline-block;background:var(--ouro);color:#14120E;text-decoration:none;
    padding:.72rem 1.4rem;border:0;border-radius:var(--raio);
    font-family:var(--sans);font-size:.98rem;font-weight:600;cursor:pointer;
    transition:background .25s ease;
  }
  .btn:hover{background:var(--ouro-claro)}
  @media (max-width:760px){.menu{display:none}}

  /* hero */
  .hero{display:grid;grid-template-columns:1.05fr .95fr;gap:clamp(2rem,5vw,4rem);align-items:center;padding-top:clamp(2.5rem,6vw,4.5rem);padding-bottom:clamp(2.5rem,6vw,4.5rem)}
  .hero p.linha-fina{font-size:1.1rem;color:var(--suave);max-width:40ch}
  .hero .acoes{display:flex;flex-wrap:wrap;gap:1rem;align-items:center;margin-top:2rem}
  .tel{text-decoration:none;border-bottom:1px solid var(--linha);padding-bottom:2px}
  .tel:hover{border-bottom-color:var(--ouro)}

  .vitrine{position:relative}
  .fios{display:block;width:100%;height:auto;border-radius:var(--raio)}
  .fios path{transition:stroke .5s ease}

  .cartela{margin-top:1.4rem}
  .cartela h2{font-family:var(--sans);font-size:.98rem;font-weight:600;margin-bottom:.7rem}
  .tons{display:flex;flex-wrap:wrap;gap:.5rem;padding:0;margin:0;list-style:none}
  .tons button{
    width:42px;height:42px;border-radius:50%;border:2px solid transparent;
    cursor:pointer;padding:0;box-shadow:inset 0 -10px 14px rgba(0,0,0,.35);
    transition:transform .2s ease, border-color .2s ease;
  }
  .tons button:hover{transform:translateY(-3px)}
  .tons button[aria-pressed="true"]{border-color:var(--leite);transform:translateY(-3px)}
  .legenda{margin-top:.85rem;font-size:.95rem;color:var(--suave);min-height:3em}
  .legenda strong{color:var(--leite);font-weight:600}
  @media (max-width:860px){
    .hero{grid-template-columns:1fr}
    .vitrine{order:-1}
  }

  /* menu de serviços */
  .servicos{background:var(--painel);border-block:1px solid var(--linha)}
  .cabeca{display:flex;flex-wrap:wrap;gap:1rem 3rem;align-items:end;justify-content:space-between;margin-bottom:2.6rem}
  .cabeca p{max-width:46ch;color:var(--suave);margin:0}
  .lista{list-style:none;margin:0;padding:0;border-top:1px solid var(--linha)}
  .lista li{
    display:grid;grid-template-columns:1fr auto;gap:.3rem 2rem;
    padding:1.35rem 0;border-bottom:1px solid var(--linha);align-items:baseline;
  }
  .lista .nome{font-family:var(--serif);font-size:1.45rem}
  .lista .preco{font-size:1.05rem;font-variant-numeric:tabular-nums;white-space:nowrap;color:var(--ouro-claro)}
  .lista .detalhe{grid-column:1/-1;color:var(--suave);font-size:.96rem;max-width:62ch;margin:0}
  .lista .tempo{color:var(--ouro);font-weight:600}
  .obs{margin-top:1.6rem;font-size:.92rem;color:var(--suave);max-width:62ch}

  /* equipe */
  .equipe-grade{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:2.2rem;margin-top:2.6rem}
  .pessoa h3{margin-bottom:.35rem}
  .pessoa .funcao{color:var(--ouro);font-weight:600;font-size:.92rem;margin-bottom:.6rem}
  .pessoa p{color:var(--suave);font-size:.97rem;margin:0}
  .retrato{
    aspect-ratio:3/4;width:100%;background:var(--painel);
    border-radius:var(--raio);margin-bottom:1rem;overflow:hidden;
  }
  .retrato svg{display:block;width:100%;height:100%}

  /* agendamento */
  .agenda{border-block:1px solid var(--linha);background:var(--painel)}
  .agenda-grade{display:grid;grid-template-columns:1fr 1.1fr;gap:clamp(2rem,6vw,4.5rem)}
  .agenda .sobre p{color:var(--suave)}
  .horarios{list-style:none;padding:0;margin:1.8rem 0 0;font-size:.98rem}
  .horarios li{display:flex;justify-content:space-between;gap:2rem;padding:.55rem 0;border-bottom:1px solid var(--linha);max-width:22rem}
  form{display:grid;gap:1.1rem}
  .campo{display:grid;gap:.4rem}
  label{font-size:.92rem;font-weight:600}
  input,select{
    font-family:var(--sans);font-size:1rem;color:var(--leite);
    background:transparent;border:1px solid var(--linha);
    border-radius:var(--raio);padding:.8rem .9rem;width:100%;
  }
  select option{color:#14120E}
  input:focus,select:focus{border-color:var(--ouro)}
  .dupla{display:grid;grid-template-columns:1fr 1fr;gap:1.1rem}
  .agenda .btn{justify-self:start;padding-inline:1.8rem}
  .recado{font-size:.95rem;border-left:3px solid var(--ouro);padding-left:.9rem;margin:0;color:var(--leite)}
  .recado[hidden]{display:none}
  @media (max-width:820px){.agenda-grade{grid-template-columns:1fr}.dupla{grid-template-columns:1fr}}

  /* rodapé */
  .rodape{padding:3rem 0 2.5rem;font-size:.95rem}
  .rodape-grade{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:2rem}
  .rodape h3{font-family:var(--sans);font-size:.92rem;font-weight:600;margin-bottom:.5rem}
  .rodape p,.rodape a{color:var(--suave);margin:0 0 .3rem;text-decoration:none;display:block}
  .rodape a:hover{color:var(--ouro)}
  .creditos{margin-top:2.5rem;padding-top:1.2rem;border-top:1px solid var(--linha);color:var(--suave);font-size:.88rem}

  @media (prefers-reduced-motion:reduce){
    *{transition:none !important;animation:none !important}
    html{scroll-behavior:auto}
  }
</style>
</head>
<body>

<header class="topo">
  <div class="env">
    <a class="marca" href="#topo">Felix <span>Beauty Studio</span></a>
    <nav class="menu" aria-label="Seções do site">
      <a href="#servicos">Serviços</a>
      <a href="#equipe">Quem atende</a>
      <a href="#agendar">Horários</a>
      <a href="#onde">Onde ficamos</a>
    </nav>
    <a class="btn" href="#agendar">Marcar horário</a>
  </div>
</header>

<main id="topo">

  <section class="env hero">
    <div>
      <h1>Escolha o tom.<br>O resto é com a gente.</h1>
      <p class="linha-fina">Alisamento, coloração e cortes em Guarulhos. Uma cliente por profissional, sempre com hora marcada.</p>
      <div class="acoes">
        <a class="btn" href="#agendar">Marcar horário</a>
        <a class="tel" href="tel:+551124087719">(11) 2408-7719</a>
      </div>
    </div>

    <div class="vitrine">
      <svg class="fios" viewBox="0 0 420 460" role="img" aria-labelledby="tituloFios">
        <title id="tituloFios">Mechas de cabelo no tom selecionado</title>
        <rect width="420" height="460" fill="#1B1917"/>
        <g fill="none" stroke-linecap="round">
          <path d="M70 -10 C 40 130, 120 230, 80 470" stroke="var(--tom)" stroke-width="26" opacity=".9"/>
          <path d="M125 -10 C 105 140, 175 250, 130 470" stroke="var(--tom)" stroke-width="34"/>
          <path d="M180 -10 C 165 150, 230 240, 190 470" stroke="var(--tom-claro)" stroke-width="18" opacity=".95"/>
          <path d="M232 -10 C 215 130, 285 250, 245 470" stroke="var(--tom)" stroke-width="36"/>
          <path d="M292 -10 C 275 150, 340 230, 300 470" stroke="var(--tom)" stroke-width="28" opacity=".85"/>
          <path d="M345 -10 C 330 140, 390 240, 355 470" stroke="var(--tom-claro)" stroke-width="14" opacity=".8"/>
          <path d="M160 -10 C 148 140, 208 245, 168 470" stroke="#F3EDE2" stroke-width="3" opacity=".35"/>
          <path d="M268 -10 C 252 140, 315 245, 278 470" stroke="#F3EDE2" stroke-width="3" opacity=".3"/>
        </g>
      </svg>

      <div class="cartela">
        <h2 id="rotuloCartela">Nossa cartela de cor</h2>
        <ul class="tons" id="tons" aria-labelledby="rotuloCartela"></ul>
        <p class="legenda" id="legenda" aria-live="polite"></p>
      </div>
    </div>
  </section>

  <section class="faixa servicos" id="servicos">
    <div class="env">
      <div class="cabeca">
        <h2>O que fazemos</h2>
        <p>Trabalhamos com alisamento em cabelo cacheado: antes de qualquer química, avaliamos a fibra e explicamos como o fio vai crescer nos próximos meses.</p>
      </div>

      <ul class="lista">
        <li>
          <span class="nome">Progressiva</span>
          <span class="preco">a partir de R$ 380</span>
          <p class="detalhe">Alisamento sem formol, com teste de mecha antes de aplicar. Preço fecha na avaliação, conforme volume e comprimento. <span class="tempo">3h a 4h</span></p>
        </li>
        <li>
          <span class="nome">Botox capilar</span>
          <span class="preco">R$ 260</span>
          <p class="detalhe">Reduz volume e frizz sem alterar o formato do cacho. Dura de dois a três meses. <span class="tempo">2h</span></p>
        </li>
        <li>
          <span class="nome">Alisamento definitivo</span>
          <span class="preco">a partir de R$ 490</span>
          <p class="detalhe">Para cabelo cacheado e crespo que quer o fio liso desde a raiz. Retoque a cada quatro meses. <span class="tempo">4h a 5h</span></p>
        </li>
        <li>
          <span class="nome">Corte feminino</span>
          <span class="preco">a partir de R$ 180</span>
          <p class="detalhe">Corte a seco ou molhado, finalização incluída. <span class="tempo">1h</span></p>
        </li>
        <li>
          <span class="nome">Corte masculino</span>
          <span class="preco">R$ 120</span>
          <p class="detalhe">Tesoura e máquina, ajuste de barba por mais R$ 40. <span class="tempo">45min</span></p>
        </li>
        <li>
          <span class="nome">Coloração de raiz</span>
          <span class="preco">R$ 260</span>
          <p class="detalhe">Cobertura de brancos ou manutenção do tom, com tonalizante de brilho. <span class="tempo">2h</span></p>
        </li>
        <li>
          <span class="nome">Mechas e balayage</span>
          <span class="preco">a partir de R$ 690</span>
          <p class="detalhe">Preço fecha na avaliação, conforme o comprimento e o histórico de química. <span class="tempo">3h a 5h</span></p>
        </li>
        <li>
          <span class="nome">Reconstrução</span>
          <span class="preco">R$ 240</span>
          <p class="detalhe">Para cabelo elástico ou poroso depois de descoloração ou alisamento. <span class="tempo">1h15</span></p>
        </li>
        <li>
          <span class="nome">Penteado para festa</span>
          <span class="preco">R$ 320</span>
          <p class="detalhe">Prova de penteado por R$ 120, abatida no valor do dia. <span class="tempo">1h30</span></p>
        </li>
      </ul>

      <p class="obs">A avaliação é gratuita e leva 15 minutos. Dá para fazer no mesmo dia do corte, sem compromisso de fechar a química.</p>
    </div>
  </section>

  <section class="faixa env" id="equipe">
    <div class="cabeca">
      <h2>Quem atende</h2>
      <p>Três profissionais dividem o estúdio. Você escolhe com quem quer marcar.</p>
    </div>

    <div class="equipe-grade">
      <article class="pessoa">
        <div class="retrato">
          <svg viewBox="0 0 120 160" aria-hidden="true"><rect width="120" height="160" fill="#211E1A"/><circle cx="60" cy="62" r="30" fill="#C9A227"/><path d="M30 160 C 32 108, 88 108, 90 160 Z" fill="#0F0E0C"/></svg>
        </div>
        <h3>Nara Ferrari</h3>
        <p class="funcao">Coloração e correção de cor</p>
        <p>Atende quem já tentou clarear em casa e quer voltar para um tom que dá para manter.</p>
      </article>

      <article class="pessoa">
        <div class="retrato">
          <svg viewBox="0 0 120 160" aria-hidden="true"><rect width="120" height="160" fill="#26221C"/><circle cx="60" cy="62" r="30" fill="#E8CE7A"/><path d="M30 160 C 32 108, 88 108, 90 160 Z" fill="#0F0E0C"/></svg>
        </div>
        <h3>Bia Nakamura</h3>
        <p class="funcao">Cortes curtos</p>
        <p>Pixie, chanel e nucas raspadas. Corta a seco para ver como o cabelo cai de verdade.</p>
      </article>

      <article class="pessoa">
        <div class="retrato">
          <svg viewBox="0 0 120 160" aria-hidden="true"><rect width="120" height="160" fill="#1E1B17"/><circle cx="60" cy="62" r="30" fill="#8C6D1F"/><path d="M30 160 C 32 108, 88 108, 90 160 Z" fill="#0F0E0C"/></svg>
        </div>
        <h3>Tainá Prado</h3>
        <p class="funcao">Alisamento e progressiva</p>
        <p>Especialista em química para cabelo cacheado e crespo, com acompanhamento a cada retoque.</p>
      </article>
    </div>
  </section>

  <section class="faixa agenda" id="agendar">
    <div class="env agenda-grade">
      <div class="sobre">
        <h2>Marcar horário</h2>
        <p>Preencha e a gente confirma no WhatsApp em até duas horas, dentro do horário de funcionamento. Se precisar desmarcar, avise com um dia de antecedência.</p>
        <ul class="horarios">
          <li><span>Terça a sexta</span><span>10h às 20h</span></li>
          <li><span>Sábado</span><span>9h às 18h</span></li>
          <li><span>Domingo e segunda</span><span>fechado</span></li>
        </ul>
      </div>

      <form id="formAgenda" novalidate>
        <div class="campo">
          <label for="nome">Seu nome</label>
          <input id="nome" name="nome" type="text" autocomplete="name" required>
        </div>
        <div class="dupla">
          <div class="campo">
            <label for="fone">WhatsApp</label>
            <input id="fone" name="fone" type="tel" inputmode="tel" placeholder="(11) 90000-0000" autocomplete="tel" required>
          </div>
          <div class="campo">
            <label for="servico">Serviço</label>
            <select id="servico" name="servico">
              <option>Progressiva</option>
              <option>Botox capilar</option>
              <option>Alisamento definitivo</option>
              <option>Corte feminino</option>
              <option>Corte masculino</option>
              <option>Coloração de raiz</option>
              <option>Mechas e balayage</option>
              <option>Reconstrução</option>
              <option>Penteado para festa</option>
              <option>Só a avaliação</option>
            </select>
          </div>
        </div>
        <div class="dupla">
          <div class="campo">
            <label for="dia">Dia de preferência</label>
            <input id="dia" name="dia" type="date">
          </div>
          <div class="campo">
            <label for="periodo">Período</label>
            <select id="periodo" name="periodo">
              <option>Manhã</option>
              <option>Tarde</option>
              <option>Fim da tarde</option>
            </select>
          </div>
        </div>
        <button class="btn" type="submit">Enviar pedido de horário</button>
        <p class="recado" id="recado" hidden></p>
      </form>
    </div>
  </section>

  <section class="faixa env" id="onde">
    <div class="cabeca">
      <h2>Onde ficamos</h2>
      <p>Av. Paulo Faccini, 1.020 — Macedo, Guarulhos. Cinco minutos de carro do Shopping Internacional.</p>
    </div>
    <p class="obs">Entrada pela portaria lateral, ao lado da farmácia. Há estacionamento conveniado na esquina.</p>
  </section>

</main>

<footer class="rodape">
  <div class="env">
    <div class="rodape-grade">
      <div>
        <h3>Felix Beauty Studio</h3>
        <p>Av. Paulo Faccini, 1.020</p>
        <p>Macedo, Guarulhos — SP</p>
      </div>
      <div>
        <h3>Falar com a gente</h3>
        <a href="tel:+551124087719">(11) 2408-7719</a>
        <a href="mailto:oi@felixbeautystudio.com.br">oi@felixbeautystudio.com.br</a>
      </div>
      <div>
        <h3>Funcionamento</h3>
        <p>Terça a sexta, 10h às 20h</p>
        <p>Sábado, 9h às 18h</p>
      </div>
      <div>
        <h3>Acompanhe</h3>
        <a href="#topo">Instagram</a>
        <a href="#topo">Pinterest</a>
      </div>
    </div>
    <p class="creditos">© 2026 Felix Beauty Studio.</p>
  </div>
</footer>

<script>
  const tons = [
    { nome:"Preto azulado", codigo:"1.1", cor:"#1B1B22", claro:"#5A5A6B", texto:"Fecha o tom sem achatar o brilho. Boa saída para quem quer disfarçar brancos com pouca manutenção." },
    { nome:"Castanho chocolate", codigo:"4.0", cor:"#4A2C21", claro:"#8E6450", texto:"Tom mais pedido da casa. Cresce bonito e aceita mechas finas depois." },
    { nome:"Acaju", codigo:"5.5", cor:"#8E2B3A", claro:"#C8737B", texto:"Vermelho quente com fundo marrom. Pede tonalizante a cada seis semanas." },
    { nome:"Mel", codigo:"7.3", cor:"#C98A34", claro:"#E3BC7E", texto:"Clareia dois tons sem descolorir a raiz. Fica dourado no sol." },
    { nome:"Loiro perolado", codigo:"9.1", cor:"#D9C9A6", claro:"#F0E6CE", texto:"Precisa de descoloração e matização quinzenal. A gente avalia a fibra antes." },
    { nome:"Grafite", codigo:"8.11", cor:"#6E6E75", claro:"#A9A9B2", texto:"Cinza frio sobre base clara. Desbota rápido, e é essa a graça." },
    { nome:"Rosé", codigo:"9.26", cor:"#C67B86", claro:"#E5B2B9", texto:"Pigmento direto, sem amônia. Dura de oito a dez lavagens." }
  ];

  const listaTons = document.getElementById("tons");
  const legenda = document.getElementById("legenda");
  const raiz = document.documentElement;

  function selecionar(i){
    const t = tons[i];
    raiz.style.setProperty("--tom", t.cor);
    raiz.style.setProperty("--tom-claro", t.claro);
    legenda.innerHTML = "<strong>" + t.nome + " " + t.codigo + ".</strong> " + t.texto;
    listaTons.querySelectorAll("button").forEach((b, j) => b.setAttribute("aria-pressed", j === i ? "true" : "false"));
  }

  tons.forEach((t, i) => {
    const li = document.createElement("li");
    const b = document.createElement("button");
    b.type = "button";
    b.style.background = t.cor;
    b.setAttribute("aria-pressed", "false");
    b.setAttribute("aria-label", "Ver o tom " + t.nome + " " + t.codigo);
    b.addEventListener("click", () => selecionar(i));
    li.appendChild(b);
    listaTons.appendChild(li);
  });

  selecionar(3);

  const form = document.getElementById("formAgenda");
  const recado = document.getElementById("recado");

  form.addEventListener("submit", (e) => {
    e.preventDefault();
    const nome = document.getElementById("nome");
    const fone = document.getElementById("fone");
    recado.hidden = false;

    if (!nome.value.trim()) {
      recado.textContent = "Falta o seu nome para a gente saber quem chamar.";
      nome.focus();
      return;
    }
    if (fone.value.replace(/\D/g, "").length < 10) {
      recado.textContent = "O WhatsApp está incompleto. Inclua o DDD, com 10 ou 11 números.";
      fone.focus();
      return;
    }

    const primeiro = nome.value.trim().split(" ")[0];
    recado.textContent = "Pedido enviado, " + primeiro + ". Confirmamos no seu WhatsApp em até duas horas.";
    form.reset();
  });
</script>
</body>
</html>
