
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pretty Rack ♡</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&family=Playfair+Display:wght@500;600;700&display=swap');

:root {
  --cream: #fff8ef;
  --paper: #fffdf9;
  --pink: #e8b8bd;
  --rose: #bd7d88;
  --brown: #292522;
  --muted: #89786e;
  --line: #eaded3;
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  background: var(--cream);
  color: var(--brown);
  font-family: 'DM Sans', sans-serif;
}

button, input, select { font: inherit; }
button { cursor: pointer; }

header {
  padding: 20px 6%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid var(--line);
  position: sticky;
  top: 0;
  background: #fff8efee;
  backdrop-filter: blur(12px);
  z-index: 10;
}

.logo {
  font: 700 30px 'Playfair Display';
  letter-spacing: -1px;
}

.logo span { color: var(--rose); }

nav {
  display: flex;
  gap: 22px;
  font-size: 12px;
}

nav a {
  text-decoration: none;
  color: var(--brown);
}

nav a:hover { color: var(--rose); }

.btn {
  background: var(--brown);
  color: white;
  border: none;
  padding: 12px 20px;
  border-radius: 30px;
  font-size: 12px;
  transition: .2s;
}

.btn:hover {
  background: var(--rose);
  transform: translateY(-2px);
}

.light {
  background: white;
  color: var(--brown);
  border: 1px solid var(--line);
}

.hero {
  padding: 75px 7%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 35px;
  align-items: center;
}

.hero h1 {
  font: 700 clamp(48px, 7vw, 90px)/.95 'Playfair Display';
  letter-spacing: -3px;
}

.hero h1 em {
  color: var(--rose);
  font-style: normal;
}

.hero p {
  line-height: 1.8;
  color: var(--muted);
  max-width: 430px;
}

.hero-art {
  background: #f1dfd8;
  height: 350px;
  border-radius: 48% 48% 15px 15px;
  display: grid;
  place-items: center;
  position: relative;
}

.hero-art span {
  font: 700 150px 'Playfair Display';
  color: #d6b2aa;
}

.sticker {
  position: absolute;
  background: white;
  padding: 15px;
  border-radius: 50%;
  font-size: 12px;
  top: 25px;
  right: 20px;
  transform: rotate(10deg);
}

section { padding: 55px 6%; }

.kicker {
  font-size: 10px;
  letter-spacing: 3px;
  color: var(--rose);
  text-transform: uppercase;
}

h2 {
  font: 600 42px 'Playfair Display';
  margin: 10px 0;
}

.muted {
  color: var(--muted);
  font-size: 13px;
}

.builder {
  display: grid;
  grid-template-columns: 270px 1fr;
  gap: 18px;
  margin-top: 25px;
}

.panel, .stage, .card {
  background: var(--paper);
  border: 1px solid var(--line);
  border-radius: 18px;
}

.panel { padding: 23px; }

.panel h3 {
  font: 600 20px 'Playfair Display';
}

label {
  display: block;
  font-size: 12px;
  color: var(--muted);
  margin: 15px 0 7px;
}

select, input {
  width: 100%;
  padding: 11px;
  border: 1px solid var(--line);
  border-radius: 10px;
  background: var(--cream);
  font-size: 12px;
}

.stage {
  background: #f5e8e2;
  padding: 22px;
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.stage-head {
  width: 100%;
  display: flex;
  justify-content: space-between;
  font-size: 10px;
  letter-spacing: 2px;
  color: #967d73;
}

.outfit {
  width: min(100%, 450px);
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin: auto;
}

.slot {
  border: 1px dashed #d8c3b8;
  background: #fffaf5b9;
  border-radius: 15px;
  min-height: 140px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 12px;
  text-align: center;
}

.slot.wide { grid-column: span 2; }

.slot.filled {
  border: 1px solid var(--pink);
  background: #fffaf5;
}

.slot .emoji { font-size: 50px; }

.slot small {
  font-size: 11px;
  color: var(--muted);
}

.slot img {
  max-height: 80px;
  max-width: 100%;
  object-fit: contain;
}

.actions {
  display: flex;
  justify-content: center;
  gap: 10px;
  flex-wrap: wrap;
  margin: 18px 0;
}

.tip {
  font-size: 11px;
  color: var(--muted);
  text-align: center;
}

.wardrobe {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
  margin-top: 20px;
}

.card { padding: 14px; }

.visual {
  height: 120px;
  background: #f7eae5;
  border-radius: 12px;
  display: grid;
  place-items: center;
  font-size: 45px;
}

.visual img {
  height: 100%;
  max-width: 100%;
  object-fit: contain;
}

.card h4 {
  font: 600 17px 'Playfair Display';
}

.card p {
  color: var(--muted);
  font-size: 12px;
}

.card button {
  width: 100%;
  padding: 9px;
  border-radius: 20px;
  border: 1px solid var(--line);
  background: white;
  font-size: 11px;
}

.upload {
  padding: 23px;
  background: white;
  border: 1px dashed var(--pink);
  border-radius: 16px;
  margin-top: 20px;
}

.upload p {
  font-size: 12px;
  color: var(--muted);
  line-height: 1.7;
}

.saved-grid, .features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  margin-top: 20px;
}

.saved, .feature {
  padding: 22px;
  background: white;
  border: 1px solid var(--line);
  border-radius: 15px;
}

.saved h3, .feature h3 {
  font: 600 20px 'Playfair Display';
}

.saved p, .feature p {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.7;
}

.empty {
  border: 1px dashed var(--line);
  border-radius: 15px;
  padding: 25px;
  color: var(--muted);
  text-align: center;
  grid-column: 1/-1;
}

footer {
  padding: 30px 6%;
  border-top: 1px solid var(--line);
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  color: var(--muted);
  font-size: 12px;
}

.toast {
  position: fixed;
  bottom: 25px;
  left: 50%;
  transform: translateX(-50%);
  background: var(--brown);
  color: white;
  padding: 14px 20px;
  border-radius: 30px;
  font-size: 12px;
  display: none;
  z-index: 20;
}

@media(max-width:800px) {
  nav { display: none; }
  .hero, .builder { grid-template-columns: 1fr; }
  .hero-art { height: 250px; }
  .wardrobe { grid-template-columns: repeat(2,1fr); }
  .saved-grid, .features { grid-template-columns: 1fr; }
}
</style>
</head>

<body>

<header>
  <a class="logo" href="#" style="text-decoration:none;color:inherit">
    pretty <span>rack</span>
  </a>

  <nav>
    <a href="#builder">STYLE</a>
    <a href="#closet">MY CLOSET</a>
    <a href="#saved">LOOKBOOK</a>
    <a href="#about">ABOUT</a>
  </nav>

  <button class="btn" onclick="go('builder')">Style me ↗</button>
</header>

<div class="hero">
  <div>
    <div class="kicker">Your closet, reimagined</div>
    <h1>Wear what you<br><em>already love.</em></h1>
    <p>
      Your entire closet at your fingertips.
      Mix, match, and make something new
      without buying something new.
    </p>
    <button class="btn" onclick="go('builder')">Let's style ♡</button>
  </div>

  <div class="hero-art">
    <span>pr</span>
    <div class="sticker">style sustainably ✦</div>
  </div>
</div>

<!-- OUTFIT BUILDER -->
<section id="builder">
  <div class="kicker">The fun part</div>
  <h2>Build your outfit.</h2>
  <p class="muted">Mix it up. Make it yours.</p>

  <div class="builder">
    <div class="panel">
      <h3>Choose your pieces</h3>

      <label>Category</label>
      <select id="category">
        <option value="tops">Tops</option>
        <option value="bottoms">Bottoms</option>
        <option value="shoes">Shoes</option>
        <option value="accessories">Accessories</option>
      </select>

      <label>Clothing item</label>
      <select id="piece"></select>

      <label>Color palette</label>
      <select id="palette">
        <option>Soft neutrals</option>
        <option>Blush pink</option>
        <option>Chocolate brown</option>
        <option>Baby blue</option>
        <option>Sage green</option>
        <option>Black & white</option>
      </select>

      <label>Occasion</label>
      <select id="occasion">
        <option>Everyday</option>
        <option>School</option>
        <option>Going out</option>
        <option>Cozy day</option>
        <option>Special occasion</option>
      </select>

      <label>Outfit name</label>
      <input id="lookName" placeholder="Sunday café ♡">

      <div class="actions">
        <button class="btn" onclick="addPiece()">Add to outfit +</button>
        <button class="btn light" onclick="randomOutfit()">Surprise me ✧</button>
      </div>
    </div>

    <div class="stage">
      <div class="stage-head">
        <span>YOUR LOOK</span>
        <span>PRETTY RACK ♡</span>
      </div>

      <div class="outfit">
        <div class="slot wide" id="slot-tops">
          <span class="emoji">👚</span><small>Your top</small>
        </div>
        <div class="slot wide" id="slot-bottoms">
          <span class="emoji">👖</span><small>Your bottoms</small>
        </div>
        <div class="slot wide" id="slot-shoes">
          <span class="emoji">👟</span><small>Your shoes</small>
        </div>
        <div class="slot" id="slot-accessories">
          <span class="emoji">🎀</span><small>Accessory 1</small>
        </div>
        <div class="slot" id="slot-extra">
          <span class="emoji">👜</span><small>Accessory 2</small>
        </div>
      </div>

      <div class="actions">
        <button class="btn light" onclick="clearOutfit()">Clear</button>
        <button class="btn" onclick="saveOutfit()">Save look ♡</button>
      </div>

      <div class="tip">Create outfits with pieces you already own!</div>
    </div>
  </div>
</section>

<!-- MY CLOSET -->
<section id="closet">
  <div class="kicker">Your personal wardrobe</div>
  <h2>My closet.</h2>
  <p class="muted">Upload your clothes and use them in your outfits.</p>

  <div class="upload">
    <h3>Add a clothing item ♡</h3>
    <p>Choose a picture, name your item, and add it to your digital closet.</p>

    <input type="file" id="photo" accept="image/*">
    <br><br>

    <input id="customName" placeholder="Name your clothing item">

    <br><br>

    <select id="customCat">
      <option value="tops">Top</option>
      <option value="bottoms">Bottom</option>
      <option value="shoes">Shoes</option>
      <option value="accessories">Accessory</option>
    </select>

    <br><br>
    <button class="btn" onclick="uploadItem()">Add to my closet ♡</button>
  </div>

  <div class="wardrobe" id="wardrobe"></div>
</section>

<!-- SAVED LOOKS -->
<section id="saved">
  <div class="kicker">Your personal lookbook</div>
  <h2>Saved looks.</h2>
  <p class="muted">All your favorite outfit combinations.</p>

  <button class="btn light" onclick="clearSaved()">Clear saved outfits</button>

  <div class="saved-grid" id="savedGrid"></div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="kicker">A little more than outfits</div>
  <h2>Style with a purpose.</h2>

  <div class="features">
    <div class="feature">
      <h3>♻ Shop your closet</h3>
      <p>Rediscover clothes you already own and make the most of your wardrobe.</p>
    </div>

    <div class="feature">
      <h3>✧ Try a new you</h3>
      <p>Experiment with colors, combinations, and aesthetics.</p>
    </div>

    <div class="feature">
      <h3>♡ Feel like yourself</h3>
      <p>Build outfits that make you feel confident and creative.</p>
    </div>
  </div>
</section>

<footer>
  <div class="logo">pretty <span style="color:var(--rose)">rack</span></div>
  <span>Less shopping. More styling. ♡</span>
  <span>Made with love.</span>
</footer>

<div class="toast" id="toast"></div>

<script>
const clothes = {
  tops: [
    ["Baby tee","👕"],["Cardigan","🧶"],["Blouse","👚"],
    ["Tank top","🎽"],["Sweater","🧥"],["Button-up","👔"],
    ["Hoodie","🧥"]
  ],
  bottoms: [
    ["Straight-leg jeans","👖"],["Pleated skirt","👗"],
    ["Wide-leg pants","👖"],["Cargo pants","🩳"],
    ["Mini skirt","👗"],["Shorts","🩳"]
  ],
  shoes: [
    ["Mary Janes","🥿"],["Sneakers","👟"],
    ["Loafers","👞"],["Ballet flats","🥿"],
    ["Platform shoes","👠"],["Sandals","🩴"]
  ],
  accessories: [
    ["Bow","🎀"],["Gold jewelry","💍"],
    ["Hair clip","🪮"],["Sunglasses","🕶️"],
    ["Scarf","🧣"],["Bag","👜"]
  ]
};

let closetItems = [];
let outfit = {
  tops:null,
  bottoms:null,
  shoes:null,
  accessories:null,
  extra:null
};

const slotNames = {
  tops:"Your top",
  bottoms:"Your bottoms",
  shoes:"Your shoes",
  accessories:"Accessory 1",
  extra:"Accessory 2"
};

function go(id) {
  document.getElementById(id).scrollIntoView({behavior:"smooth"});
}

function toast(message) {
  const t = document.getElementById("toast");
  t.textContent = message;
  t.style.display = "block";
  setTimeout(()=>t.style.display="none",2500);
}

function updatePieces() {
  const cat = document.getElementById("category").value;
  const select = document.getElementById("piece");
  select.innerHTML="";

  clothes[cat].forEach((item,i)=>{
    const option=document.createElement("option");
    option.value="default-"+i;
    option.textContent=item[0];
    select.appendChild(option);
  });

  closetItems.filter(item=>item.category===cat).forEach(item=>{
    const option=document.createElement("option");
    option.value="custom-"+item.id;
    option.textContent="♡ "+item.name;
    select.appendChild(option);
  });
}

document.getElementById("category").onchange=updatePieces;
updatePieces();

function renderSlot(key,item) {
  const slot=document.getElementById("slot-"+key);
  slot.classList.toggle("filled",!!item);

  const emoji=slot.querySelector(".emoji");

  if(item && item.image) {
    emoji.innerHTML='<img src="'+item.image+'" alt="'+item.name+'">';
  } else {
    emoji.textContent=item?item.emoji:
      ({tops:"👚",bottoms:"👖",shoes:"👟",accessories:"🎀",extra:"👜"}[key]);
  }

  slot.querySelector("small").textContent=item?item.name:slotNames[key];
}

function putInOutfit(item,category) {
  let key=category;

  if(category==="accessories") {
    key=outfit.accessories?"extra":"accessories";
  }

  outfit[key]=item;
  renderSlot(key,item);
}

function addPiece() {
  const cat=document.getElementById("category").value;
  const value=document.getElementById("piece").value;
  let item;

  if(value.startsWith("custom-")) {
    item=closetItems.find(x=>x.id===Number(value.replace("custom-","")));
  } else {
    const index=Number(value.replace("default-",""));
    item={name:clothes[cat][index][0],emoji:clothes[cat][index][1]};
  }

  if(item) {
    putInOutfit(item,cat);
    toast(item.name+" added to your outfit ♡");
  }
}

function randomOutfit() {
  Object.keys(clothes).forEach(cat=>{
    const list=clothes[cat];
    const chosen=list[Math.floor(Math.random()*list.length)];
    putInOutfit({name:chosen[0],emoji:chosen[1]},cat);
  });
  toast("Your surprise outfit is ready ✧");
}

function clearOutfit() {
  Object.keys(outfit).forEach(key=>{
    outfit[key]=null;
    renderSlot(key,null);
  });
  toast("Fresh start ♡");
}

function saveOutfit() {
  const saved=JSON.parse(localStorage.getItem("prettyRackLooks")||"[]");

  saved.unshift({
    name:document.getElementById("lookName").value||"My pretty look",
    occasion:document.getElementById("occasion").value,
    palette:document.getElementById("palette").value,
    pieces:Object.fromEntries(
      Object.entries(outfit).map(([key,item])=>[key,item?item.name:""])
    )
  });

  localStorage.setItem("prettyRackLooks",JSON.stringify(saved));
  renderSaved();
  toast("Look saved to your lookbook ♡");
}

function uploadItem() {
  const file=document.getElementById("photo").files[0];
  const name=document.getElementById("customName").value.trim();
  const category=document.getElementById("customCat").value;

  if(!file || !name) {
    toast("Choose a picture and name your item!");
    return;
  }

  const reader=new FileReader();

  reader.onload=()=>{
    closetItems.push({
      id:Date.now(),
      name,
      category,
      image:reader.result
    });

    localStorage.setItem("prettyRackCloset",JSON.stringify(closetItems));

    renderCloset();
    updatePieces();

    document.getElementById("photo").value="";
    document.getElementById("customName").value="";

    toast("Added to your closet ♡");
  };

  reader.readAsDataURL(file);
}

function renderCloset() {
  const box=document.getElementById("wardrobe");
  box.innerHTML="";

  if(!closetItems.length) {
    box.innerHTML='<div class="empty">Your closet is waiting for its first piece ♡</div>';
    return;
  }

  closetItems.forEach(item=>{
    const card=document.createElement("div");
    card.className="card";

    card.innerHTML=`
      <div class="visual">
        <img src="${item.image}" alt="${item.name}">
      </div>
      <h4>${item.name}</h4>
      <p>${item.category}</p>
      <button>Add to outfit</button>
      <br><br>
      <button onclick="deleteClosetItem(${item.id})">Remove item</button>
    `;

    card.querySelector("button").onclick=()=>{
      putInOutfit(item,item.category);
      toast(item.name+" added ♡");
    };

    box.appendChild(card);
  });
}

function deleteClosetItem(id) {
  closetItems=closetItems.filter(item=>item.id!==id);
  localStorage.setItem("prettyRackCloset",JSON.stringify(closetItems));
  renderCloset();
  updatePieces();
  toast("Item removed");
}

function renderSaved() {
  const box=document.getElementById("savedGrid");
  const saved=JSON.parse(localStorage.getItem("prettyRackLooks")||"[]");
  box.innerHTML="";

  if(!saved.length) {
    box.innerHTML='<div class="empty">No saved outfits yet. Make your first look! ♡</div>';
    return;
  }

  saved.forEach((look,index)=>{
    const card=document.createElement("div");
    card.className="saved";

    card.innerHTML=`
      <h3>${look.name}</h3>
      <p>${look.occasion} · ${look.palette}</p>
      <p>${Object.values(look.pieces).filter(Boolean).join(" / ")}</p>
      <button class="btn light" onclick="loadLook(${index})">Load look</button>
      <br><br>
      <button class="btn light" onclick="deleteLook(${index})">Delete</button>
    `;

    box.appendChild(card);
  });
}

function loadLook(index) {
  const saved=JSON.parse(localStorage.getItem("prettyRackLooks")||"[]");
  const look=saved[index];

  Object.entries(look.pieces).forEach(([key,name])=>{
    if(!name)return;

    let item=closetItems.find(x=>x.name===name);

    if(!item) {
      for(const cat in clothes) {
        const found=clothes[cat].find(x=>x[0]===name);
        if(found)item={name:found[0],emoji:found[1]};
      }
    }

    if(item) {
      outfit[key]=item;
      renderSlot(key,item);
    }
  });

  document.getElementById("lookName").value=look.name;
  go("builder");
  toast("Look loaded ♡");
}

function deleteLook(index) {
  const saved=JSON.parse(localStorage.getItem("prettyRackLooks")||"[]");
  saved.splice(index,1);
  localStorage.setItem("prettyRackLooks",JSON.stringify(saved));
  renderSaved();
}

function clearSaved() {
  if(confirm("Delete all your saved outfits?")) {
    localStorage.removeItem("prettyRackLooks");
    renderSaved();
    toast("Lookbook cleared");
  }
}

closetItems=JSON.parse(localStorage.getItem("prettyRackCloset")||"[]");
renderCloset();
renderSaved();
</script>

</body>
</html>
