# Fawn-and-Fang
A business I guess
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fawn & Fang</title>

<style>
:root{
  --bg:#100d12;
  --panel:#19141c;
  --panel2:#241c28;
  --text:#f7edf7;
  --muted:#b9aabd;
  --pink:#dca8c9;
  --green:#b9d9aa;
  --red:#e88998;
  --line:#3a2d3e;
}

*{box-sizing:border-box}

body{
  margin:0;
  background:
    radial-gradient(circle at 10% 0%,#342337 0%,transparent 35%),
    var(--bg);
  color:var(--text);
  font-family:Arial,Helvetica,sans-serif;
}

button,input,select,textarea{font:inherit}

button{
  cursor:pointer;
}

button:disabled{
  cursor:not-allowed;
  opacity:.45;
}

.header{
  position:sticky;
  top:0;
  z-index:50;
  display:flex;
  align-items:center;
  gap:12px;
  padding:12px 18px;
  background:#100d12ee;
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--line);
}

.logo{
  font-weight:900;
  letter-spacing:.08em;
  white-space:nowrap;
  cursor:pointer;
}

.logo span{
  color:var(--green);
}

.search{
  flex:1;
  max-width:650px;
  background:var(--panel);
  border:1px solid var(--line);
  border-radius:999px;
  padding:10px 16px;
  color:var(--text);
  outline:none;
}

.btn{
  border:1px solid var(--line);
  background:var(--panel);
  color:var(--text);
  padding:9px 13px;
  border-radius:11px;
}

.btn:hover{
  background:var(--panel2);
}

.btn.primary{
  background:var(--pink);
  color:#251624;
  border-color:transparent;
  font-weight:800;
}

.btn.green{
  background:var(--green);
  color:#182116;
  border-color:transparent;
  font-weight:800;
}

.btn.danger{
  background:#3a1820;
  color:#ffdce1;
}

.layout{
  display:grid;
  grid-template-columns:220px 1fr;
  min-height:calc(100vh - 63px);
}

.sidebar{
  position:sticky;
  top:63px;
  height:calc(100vh - 63px);
  padding:18px;
  border-right:1px solid var(--line);
  background:#120f14cc;
}

.sidebar-title{
  color:var(--muted);
  font-size:11px;
  text-transform:uppercase;
  letter-spacing:.15em;
  margin-bottom:10px;
}

.nav button{
  display:block;
  width:100%;
  text-align:left;
  border:1px solid transparent;
  background:transparent;
  color:var(--muted);
  padding:10px;
  border-radius:10px;
  margin:4px 0;
}

.nav button:hover,
.nav button.active{
  background:var(--panel2);
  border-color:var(--line);
  color:var(--text);
}

main{
  width:100%;
  max-width:1500px;
  margin:auto;
  padding:26px;
}

.hero{
  padding:32px;
  border:1px solid var(--line);
  border-radius:22px;
  background:linear-gradient(135deg,#2a2030,#151016);
  margin-bottom:25px;
}

.eyebrow{
  color:var(--green);
  font-size:12px;
  font-weight:800;
  letter-spacing:.14em;
  text-transform:uppercase;
}

.hero h1{
  font-size:clamp(38px,6vw,70px);
  line-height:.95;
  margin:10px 0;
}

.hero p{
  max-width:700px;
  color:var(--muted);
  font-size:17px;
}

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(210px,1fr));
  gap:16px;
}

.card{
  background:var(--panel);
  border:1px solid var(--line);
  border-radius:17px;
  overflow:hidden;
}

.photo{
  aspect-ratio:1;
  display:grid;
  place-items:center;
  background:linear-gradient(135deg,#332438,#171319);
  font-size:65px;
}

.card-body{
  padding:14px;
}

.row{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:10px;
  flex-wrap:wrap;
}

.muted{
  color:var(--muted);
}

.price{
  font-size:19px;
  font-weight:900;
}

.pill{
  display:inline-block;
  padding:4px 8px;
  border-radius:999px;
  background:#2c2230;
  color:var(--muted);
  font-size:11px;
}

.new{
  background:var(--green);
  color:#172016;
}

.sold{
  background:#4a2029;
  color:#ffdbe0;
}

.actions{
  display:flex;
  gap:8px;
  flex-wrap:wrap;
}

.panel{
  background:var(--panel);
  border:1px solid var(--line);
  border-radius:17px;
  padding:18px;
  margin:14px 0;
}

.field{
  display:grid;
  gap:6px;
  margin:12px 0;
}

.field label{
  color:var(--muted);
  font-size:12px;
  font-weight:700;
}

.field input,
.field select,
.field textarea{
  width:100%;
  background:#110e13;
  color:var(--text);
  border:1px solid var(--line);
  border-radius:10px;
  padding:10px;
  outline:none;
}

.field textarea{
  min-height:100px;
  resize:vertical;
}

.product{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:28px;
}

.product > .photo{
  border:1px solid var(--line);
  border-radius:20px;
}

.empty{
  text-align:center;
  padding:50px 20px;
  border:1px dashed var(--line);
  border-radius:16px;
  color:var(--muted);
}

.notice{
  padding:13px;
  border:1px solid #5d4960;
  border-radius:12px;
  background:#211925;
  margin:12px 0;
}

.success{
  border-color:#496044;
  background:#182119;
}

.warning{
  border-color:#66533a;
  background:#282116;
}

.danger-box{
  border-color:#66303a;
  background:#29171d;
}

.table-wrap{
  overflow:auto;
  border:1px solid var(--line);
  border-radius:14px;
}

table{
  width:100%;
  min-width:700px;
  border-collapse:collapse;
}

th,td{
  padding:11px;
  border-bottom:1px solid var(--line);
  text-align:left;
}

th{
  color:var(--muted);
  font-size:12px;
  text-transform:uppercase;
}

.status{
  display:inline-block;
  padding:4px 8px;
  border-radius:999px;
  background:#2b2430;
  font-size:11px;
}

.split{
  display:grid;
  grid-template-columns:300px 1fr;
  gap:16px;
}

.list{
  background:var(--panel);
  border:1px solid var(--line);
  border-radius:16px;
  overflow:hidden;
}

.list-item{
  padding:13px;
  border-bottom:1px solid var(--line);
  cursor:pointer;
}

.list-item:hover,
.list-item.selected{
  background:var(--panel2);
}

.chat{
  display:grid;
  grid-template-rows:auto 1fr auto;
  min-height:520px;
  background:var(--panel);
  border:1px solid var(--line);
  border-radius:16px;
  overflow:hidden;
}

.messages{
  padding:18px;
  overflow:auto;
}

.message{
  max-width:75%;
  padding:10px 12px;
  margin:8px 0;
  border-radius:13px;
  background:#2b2230;
}

.message.me{
  margin-left:auto;
  background:#4a3048;
}

.composer{
  display:flex;
  gap:8px;
  padding:12px;
  border-top:1px solid var(--line);
}

.composer input{
  flex:1;
  background:#110e13;
  border:1px solid var(--line);
  color:var(--text);
  border-radius:10px;
  padding:10px;
}

.admin-badge{
  display:inline-block;
  padding:4px 8px;
  border-radius:999px;
  background:var(--green);
  color:#172016;
  font-size:11px;
  font-weight:900;
}

.footer{
  padding:35px 0;
  color:var(--muted);
}

#toast{
  position:fixed;
  right:18px;
  bottom:18px;
  z-index:100;
  display:none;
  padding:13px 16px;
  background:#241b27;
  border:1px solid var(--line);
  border-radius:12px;
  box-shadow:0 15px 40px #0008;
}

#toast.show{
  display:block;
}

@media(max-width:800px){
  .layout{
    grid-template-columns:1fr;
  }

  .sidebar{
    position:static;
    height:auto;
    border-right:0;
    border-bottom:1px solid var(--line);
    overflow:auto;
  }

  .nav{
    display:flex;
    gap:5px;
    overflow:auto;
  }

  .nav button{
    width:auto;
    white-space:nowrap;
  }

  .product,
  .split{
    grid-template-columns:1fr;
  }

  .header{
    flex-wrap:wrap;
  }

  .search{
    order:3;
    flex-basis:100%;
    max-width:none;
  }

  main{
    padding:16px;
  }
}
</style>
</head>

<body>

<div id="app"></div>
<div id="toast"></div>

<script>
"use strict";

/* =========================================================
   FAWN & FANG — OFFICIAL DEMO
   Single-file GitHub Pages prototype.
   ========================================================= */

const STORAGE_KEY = "fawn_fang_demo_v2";

const CATEGORIES = [
  "Masks",
  "Chains and metalwork",
  "Alternative",
  "Cute and preppy",
  "Scene and expressive"
];

const STATUSES = [
  "Pending",
  "Accepted",
  "Making",
  "Ready for Payment",
  "Paid",
  "Shipped",
  "Completed",
  "Cancelled"
];

function makeInitialState(){
  return {
    page:"home",
    category:"All",
    search:"",
    session:null,
    admin:false,

    selectedProduct:null,
    selectedOrder:null,
    selectedChat:null,

    pendingItems:null,
    pendingCustom:false,

    cart:[],
    buckets:{},
    restockRequests:{},

    users:[
      {
        username:"maya",
        password:"demo123",
        email:"maya@example.com",
        phone:"",
        address:""
      }
    ],

    orders:[],

    notifications:[],

    chats:[
      {
        id:"chat-demo",
        order:"DEMO-ORDER",
        user:"maya",
        messages:[
          {
            from:"admin",
            text:"Welcome to the Fawn & Fang demo chat!",
            at:new Date().toLocaleString()
          }
        ]
      }
    ],

    products:[
      {
        id:"p1",
        name:"Fawn Mask",
        price:42,
        quantity:2,
        category:"Masks",
        newArrival:true,
        materials:"Painted resin, faux fur",
        sizes:["Small","Medium","Large"],
        emoji:"🦌",
        description:"A woodland-inspired handmade statement mask."
      },

      {
        id:"p2",
        name:"Fang Chain",
        price:18,
        quantity:4,
        category:"Chains and metalwork",
        newArrival:true,
        materials:"Metal chain and charms",
        sizes:["One size"],
        emoji:"⛓️",
        description:"A dark silver accessory for alternative outfits."
      },

      {
        id:"p3",
        name:"Blossom Charm",
        price:12,
        quantity:6,
        category:"Cute and preppy",
        newArrival:false,
        materials:"Metal and acrylic flower",
        sizes:["One size"],
        emoji:"🌸",
        description:"A small floral charm with a sweet edge."
      },

      {
        id:"p4",
        name:"Void Bracelet",
        price:16,
        quantity:1,
        category:"Scene and expressive",
        newArrival:false,
        materials:"Cord, beads and metal",
        sizes:["Small","Medium","Large"],
        emoji:"🌌",
        description:"A dark, expressive handmade bracelet."
      },

      {
        id:"p5",
        name:"Thorn Collar",
        price:24,
        quantity:0,
        category:"Alternative",
        newArrival:false,
        materials:"Faux leather and metal",
        sizes:["Small","Medium","Large"],
        emoji:"🌹",
        description:"Currently sold out. Request more if you want another."
      }
    ],

    custom:{
      bases:[
        {
          id:"base1",
          name:"Wolf Mask",
          min:20,
          max:30,
          emoji:"🐺"
        },
        {
          id:"base2",
          name:"Cat Mask",
          min:20,
          max:30,
          emoji:"🐈"
        },
        {
          id:"base3",
          name:"Bracelet",
          min:12,
          max:20,
          emoji:"📿"
        },
        {
          id:"base4",
          name:"Chain",
          min:15,
          max:25,
          emoji:"⛓️"
        }
      ],

      accessories:[
        {
          id:"acc1",
          name:"Fangs",
          min:5,
          max:10,
          emoji:"🦷"
        },
        {
          id:"acc2",
          name:"Flowers",
          min:4,
          max:8,
          emoji:"🌸"
        },
        {
          id:"acc3",
          name:"Spikes",
          min:5,
          max:10,
          emoji:"✦"
        },
        {
          id:"acc4",
          name:"Charms",
          min:3,
          max:7,
          emoji:"✨"
        }
      ],

      sizes:["Small","Medium","Large"],

      templates:[
        "Wolf mask outline",
        "Blank canvas"
      ]
    },

    settings:{
      paymentDeadlineDays:5,
      expectedDeliveryDays:7
    },

    customDraft:null
  };
}

function loadState(){
  try{
    const saved = localStorage.getItem(STORAGE_KEY);

    if(!saved){
      return makeInitialState();
    }

    const parsed = JSON.parse(saved);
    const base = makeInitialState();

    return Object.assign(base,parsed);
  }catch(error){
    console.error("Fawn & Fang state error:",error);
    return makeInitialState();
  }
}

let state = loadState();

function save(){
  localStorage.setItem(STORAGE_KEY,JSON.stringify(state));
}

function escapeHTML(value){
  return String(value ?? "")
    .replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");
}

function money(value){
  return "$" + Number(value || 0).toFixed(2);
}

function currentUser(){
  return state.users.find(
    user => user.username === state.session
  ) || null;
}

function requireLogin(){
  if(!currentUser()){
    state.page="login";
    render();
    return false;
  }

  return true;
}

function notify(text){
  state.notifications.unshift({
    id:Date.now() + Math.random(),
    text,
    time:new Date().toLocaleString(),
    read:false
  });

  save();
}

function toast(message){
  const element=document.getElementById("toast");

  element.textContent=message;
  element.classList.add("show");

  setTimeout(()=>{
    element.classList.remove("show");
  },2500);
}

function go(page){
  state.page=page;
  state.selectedProduct=null;
  save();
  render();
}

function category(name){
  state.category=name;
  state.page="home";
  save();
  render();
}

/* =========================================================
   HEADER / NAVIGATION
   ========================================================= */

function header(){
  const user=currentUser();

  return `
  <header class="header">

    <div class="logo" onclick="category('All')">
      FAWN <span>&</span> FANG
    </div>

    <input
      class="search"
      placeholder="Search masks, chains, charms..."
      value="${escapeHTML(state.search)}"
      oninput="state.search=this.value;render()"
    >

    <button class="btn" onclick="go('cart')">
      🛒 ${state.cart.length}
    </button>

    ${
      user
      ?
      `
      <button class="btn" onclick="go('account')">
        @${escapeHTML(user.username)}
      </button>

      <button class="btn" onclick="logout()">
        Log out
      </button>
      `
      :
      `
      <button class="btn primary" onclick="go('login')">
        Sign in
      </button>
      `
    }

  </header>
  `;
}

function sidebar(){
  return `
  <aside class="sidebar">

    <div class="sidebar-title">
      Browse
    </div>

    <nav class="nav">

      ${CATEGORIES.map(categoryName=>`
        <button
          class="${state.category===categoryName?"active":""}"
          onclick="category('${escapeHTML(categoryName)}')"
        >
          ${escapeHTML(categoryName)}
        </button>
      `).join("")}

      <button
        class="${state.page==="customize"?"active":""}"
        onclick="go('customize')"
      >
        Customize
      </button>

      <button
        onclick="category('NEW ARRIVALS')"
      >
        NEW ARRIVALS
      </button>

      <button onclick="go('orders')">
        My Orders
      </button>

      <button onclick="go('cart')">
        🛒 Cart (${state.cart.length})
      </button>

      <button onclick="go('admin')">
        Artist
      </button>

    </nav>

  </aside>
  `;
}

/* =========================================================
   STOREFRONT
   ========================================================= */

function productCard(product){

  const soldOut=product.quantity<=0;

  return `
  <article class="card">

    <div class="photo">
      ${product.emoji}
    </div>

    <div class="card-body">

      <div class="row">
        <b>${escapeHTML(product.name)}</b>

        ${
          product.newArrival
          ? `<span class="pill new">NEW</span>`
          : ""
        }
      </div>

      <p class="muted">
        ${escapeHTML(product.description)}
      </p>

      <div class="row">

        <span class="price">
          ${money(product.price)}
        </span>

        ${
          soldOut
          ? `<span class="pill sold">SOLD OUT</span>`
          : `<span class="pill">${product.quantity} available</span>`
        }

      </div>

      <div class="actions" style="margin-top:10px">

        <button
          class="btn primary"
          onclick="openProduct('${product.id}')"
        >
          View
        </button>

        ${
          soldOut
          ?
          `
          <button
            class="btn"
            onclick="requestRestock('${product.id}')"
          >
            Request More
          </button>
          `
          :
          `
          <button
            class="btn"
            onclick="quickAdd('${product.id}')"
          >
            Add
          </button>
          `
        }

      </div>

    </div>
  </article>
  `;
}

function homePage(){

  const search=state.search.trim().toLowerCase();

  const products=state.products.filter(product=>{

    const searchable=[
      product.name,
      product.category,
      product.description,
      product.materials
    ].join(" ").toLowerCase();

    const matchesSearch=
      !search || searchable.includes(search);

    let matchesCategory=true;

    if(state.category!=="All"){
      if(state.category==="NEW ARRIVALS"){
        matchesCategory=product.newArrival;
      }else{
        matchesCategory=
          product.category===state.category;
      }
    }

    return matchesSearch && matchesCategory;
  });

  return `
  <section class="hero">

    <div class="eyebrow">
      handmade • alternative • woodland
    </div>

    <h1>
      Made with fangs.<br>
      Made with love.
    </h1>

    <p>
      Fawn & Fang is a handmade little corner for masks,
      chains, metalwork, cute pieces, scene accessories,
      and custom creations.
    </p>

    <div class="actions">

      <button
        class="btn primary"
        onclick="category('All')"
      >
        Shop everything
      </button>

      <button
        class="btn"
        onclick="go('customize')"
      >
        Build something custom
      </button>

    </div>

  </section>

  <div class="row">

    <div>
      <h2>
        ${
          state.category==="All"
          ? "Featured pieces"
          : escapeHTML(state.category)
        }
      </h2>

      <p class="muted">
        ${products.length}
        item${products.length===1?"":"s"} shown
      </p>
    </div>

  </div>

  ${
    products.length
    ?
    `<div class="grid">
      ${products.map(productCard).join("")}
    </div>`
    :
    `<div class="empty">
      Nothing matches that search yet.
    </div>`
  }
  `;
}

/* =========================================================
   PRODUCT PAGE
   ========================================================= */

function openProduct(id){
  state.selectedProduct=id;
  state.page="product";
  save();
  render();
}

function productPage(){

  const product=state.products.find(
    item=>item.id===state.selectedProduct
  );

  if(!product){
    return homePage();
  }

  const soldOut=product.quantity<=0;

  return `
  <button class="btn" onclick="go('home')">
    ← Back
  </button>

  <div class="product" style="margin-top:18px">

    <div class="photo">
      ${product.emoji}
    </div>

    <div>

      <div class="eyebrow">
        ${escapeHTML(product.category)}
      </div>

      <h1>
        ${escapeHTML(product.name)}
      </h1>

      <div class="price">
        ${money(product.price)}
      </div>

      <p class="muted">
        ${escapeHTML(product.description)}
      </p>

      <div class="panel">

        <b>Materials</b>

        <p class="muted">
          ${escapeHTML(product.materials)}
        </p>

        <div class="field">

          <label>SIZE</label>

          <select id="productSize">
            ${product.sizes.map(size=>`
              <option value="${escapeHTML(size)}">
                ${escapeHTML(size)}
              </option>
            `).join("")}
          </select>

        </div>

        ${
          soldOut
          ?
          ""
          :
          `
          <div class="field">

            <label>
              QUANTITY — MAX 4
            </label>

            <input
              id="productQuantity"
              type="number"
              min="1"
              max="4"
              value="1"
            >

          </div>
          `
        }

      </div>

      ${
        soldOut
        ?
        `
        <div class="notice danger-box">

          <b>SOLD OUT</b>

          <br>

          The item remains visible so customers
          can request another batch.

        </div>

        <button
          class="btn"
          onclick="requestRestock('${product.id}')"
        >
          Request More of This Item
        </button>
        `
        :
        `
        <div class="actions">

          <button
            class="btn primary"
            onclick="purchaseProduct('${product.id}')"
          >
            Purchase / Request
          </button>

          <button
            class="btn"
            onclick="addProductToCart('${product.id}')"
          >
            Add to Cart
          </button>

        </div>

        <p class="muted">
          Purchase means submitting a request.
          You are not charged at this stage.
        </p>
        `
      }

    </div>

  </div>
  `;
}

/* =========================================================
   CART
   ========================================================= */

function ensureBuckets(){
  if(!state.buckets || typeof state.buckets!=="object"){
    state.buckets={};
  }
}

function quickAdd(id){

  if(!requireLogin()) return;

  const product=state.products.find(
    item=>item.id===id
  );

  if(!product || product.quantity<=0){
    toast("This item is sold out.");
    return;
  }

  state.cart.push({
    id:crypto.randomUUID(),
    productId:id,
    size:product.sizes[0],
    quantity:1,
    bucket:null
  });

  save();

  toast("Added to cart!");
  render();
}

function addProductToCart(id){

  if(!requireLogin()) return;

  const product=state.products.find(
    item=>item.id===id
  );

  const size=document.getElementById("productSize").value;

  let quantity=Number(
    document.getElementById("productQuantity").value
  );

  if(!Number.isFinite(quantity)){
    quantity=1;
  }

  quantity=Math.max(1,Math.min(4,quantity));

  state.cart.push({
    id:crypto.randomUUID(),
    productId:id,
    size:size,
    quantity:quantity,
    bucket:null
  });

  save();

  toast("Added to cart!");

  go("cart");
}

function purchaseProduct(id){

  if(!requireLogin()) return;

  const size=document.getElementById("productSize").value;

  let quantity=Number(
    document.getElementById("productQuantity").value
  );

  if(!Number.isFinite(quantity)){
    quantity=1;
  }

  quantity=Math.max(1,Math.min(4,quantity));

  startRequest([
    {
      productId:id,
      size:size,
      quantity:quantity
    }
  ]);
}

function cartLine(item){

  const product=state.products.find(
    product=>product.id===item.productId
  );

  if(!product) return "";

  return `
  <div class="panel">

    <div class="row">

      <div>
        ${product.emoji}
        <b>${escapeHTML(product.name)}</b>

        <span class="muted">
          · ${escapeHTML(item.size)}
          × ${item.quantity}
        </span>
      </div>

      <div>

        <b>
          ${money(product.price * item.quantity)}
        </b>

        <button
          class="btn"
          onclick="moveCartItem('${item.id}')"
        >
          Move
        </button>

        <button
          class="btn danger"
          onclick="removeCartItem('${item.id}')"
        >
          Remove
        </button>

      </div>

    </div>

  </div>
  `;
}

function cartSection(items){

  if(!items.length){
    return `<p class="muted">No items here.</p>`;
  }

  return items.map(cartLine).join("");
}

function cartPage(){

  if(!requireLogin()) return "";

  ensureBuckets();

  const mainCart=state.cart.filter(
    item=>!item.bucket
  );

  const buckets=Object.keys(state.buckets);

  return `
  <div class="row">

    <div>
      <h1>Your Cart</h1>

      <p class="muted">
        Organize items into buckets.
        Each bucket becomes one order request.
      </p>
    </div>

    <button
      class="btn"
      onclick="createBucket()"
    >
      ＋ New Bucket
    </button>

  </div>

  <div class="panel">

    <h2>Main Cart</h2>

    ${cartSection(mainCart)}

    ${
      mainCart.length
      ?
      `
      <button
        class="btn primary"
        onclick="requestCart(null)"
      >
        Request Main Cart
      </button>
      `
      :
      ""
    }

  </div>

  ${buckets.map(name=>{

    const items=state.cart.filter(
      item=>item.bucket===name
    );

    return `
    <div class="panel">

      <div class="row">

        <h2>${escapeHTML(name)}</h2>

        <button
          class="btn primary"
          onclick="requestCart('${escapeHTML(name)}')"
        >
          Request This Bucket
        </button>

      </div>

      ${cartSection(items)}

    </div>
    `;

  }).join("")}

  ${
    !state.cart.length
    ?
    `<div class="empty">
      Your cart is empty.
    </div>`
    :
    ""
  }
  `;
}

function removeCartItem(id){

  state.cart=state.cart.filter(
    item=>item.id!==id
  );

  save();
  render();
}

function createBucket(){

  if(!requireLogin()) return;

  const name=prompt("Bucket name:");

  if(!name || !name.trim()){
    return;
  }

  ensureBuckets();

  const clean=name.trim();

  if(state.buckets[clean]){
    toast("That bucket already exists.");
    return;
  }

  state.buckets[clean]=true;

  save();
  render();
}

function moveCartItem(id){

  ensureBuckets();

  const item=state.cart.find(
    item=>item.id===id
  );

  if(!item) return;

  const names=[
    "Main Cart",
    ...Object.keys(state.buckets)
  ];

  const destination=prompt(
    "Move to:\n\n"+names.join("\n")
  );

  if(!destination) return;

  if(destination==="Main Cart"){
    item.bucket=null;
  }else{
    if(!state.buckets[destination]){
      state.buckets[destination]=true;
    }

    item.bucket=destination;
  }

  save();
  render();
}

function requestCart(bucket){

  const items=state.cart
    .filter(item=>bucket ? item.bucket===bucket : !item.bucket)
    .map(item=>({
      productId:item.productId,
      size:item.size,
      quantity:item.quantity
    }));

  if(!items.length){
    toast("There are no items here.");
    return;
  }

  const overLimit=items.some(
    item=>item.quantity>4
  );

  if(overLimit){
    toast("Maximum 4 of one item per request.");
    return;
  }

  startRequest(items);
}

/* =========================================================
   REQUESTS
   ========================================================= */

function startRequest(items,custom=false){

  if(!requireLogin()) return;

  state.pendingItems=items;
  state.pendingCustom=custom;
  state.page="request";

  save();
  render();
}

function requestPage(){

  if(!requireLogin()) return "";

  const items=state.pendingItems || [];

  let total=0;

  items.forEach(item=>{

    if(item.productId){

      const product=state.products.find(
        product=>product.id===item.productId
      );

      if(product){
        total += product.price * item.quantity;
      }
    }
  });

  return `
  <button
    class="btn"
    onclick="go('home')"
  >
    ← Continue Shopping
  </button>

  <div
    class="panel"
    style="max-width:750px;margin:18px auto"
  >

    <h1>
      ${state.pendingCustom ? "Custom Request" : "Purchase Request"}
    </h1>

    <div class="notice">

      <b>
        Please come back in an hour,
        artist is currently reviewing the order.
      </b>

      <br><br>

      No payment is taken right now.

    </div>

    <h3>Items</h3>

    ${
      items.map(item=>{

        if(item.custom){
          return `
          <div class="row">
            <span>${escapeHTML(item.name)}</span>
            <span>Custom</span>
          </div>
          `;
        }

        const product=state.products.find(
          p=>p.id===item.productId
        );

        if(!product) return "";

        return `
        <div class="row">

          <span>
            ${escapeHTML(product.name)}
            · ${escapeHTML(item.size)}
            × ${item.quantity}
          </span>

          <b>
            ${money(product.price * item.quantity)}
          </b>

        </div>
        `;

      }).join("")
    }

    <hr style="border-color:var(--line)">

    <div class="row">

      <b>Current item total</b>

      <b>${money(total)}</b>

    </div>

    <div class="field">

      <label>PHONE / CONTACT</label>

      <input
        id="requestPhone"
        value="${escapeHTML(currentUser().phone || "")}"
      >

    </div>

    <div class="field">

      <label>SHIPPING ADDRESS</label>

      <textarea id="requestAddress">${escapeHTML(currentUser().address || "")}</textarea>

    </div>

    <div class="field">

      <label>ORDER NOTES</label>

      <textarea
        id="requestNotes"
        placeholder="Anything the artist should know?"
      ></textarea>

    </div>

    <button
      class="btn primary"
      onclick="submitRequest()"
    >
      Submit Request
    </button>

  </div>
  `;
}

function submitRequest(){

  const user=currentUser();

  const phone=document.getElementById("requestPhone").value;
  const address=document.getElementById("requestAddress").value;
  const notes=document.getElementById("requestNotes").value;

  user.phone=phone;
  user.address=address;

  const order={
    id:"FF-"+Date.now().toString().slice(-7),
    user:user.username,
    created:new Date().toISOString(),
    items:state.pendingItems || [],
    custom:state.pendingCustom,
    status:"Pending",
    phone,
    address,
    notes,
    price:null,
    payBy:null,
    expectedDelivery:null,
    receipt:false,
    cancellationReason:null,
    history:[
      {
        status:"Pending",
        at:new Date().toISOString()
      }
    ]
  };

  state.orders.unshift(order);

  state.cart=state.cart.filter(
    cartItem=>!(
      order.items.some(
        item=>
          !item.custom &&
          item.productId===cartItem.productId &&
          item.size===cartItem.size &&
          item.quantity===cartItem.quantity
      )
    )
  );

  state.pendingItems=null;
  state.pendingCustom=false;

  state.selectedOrder=order.id;
  state.page="orders";

  notify(
    `New ${order.custom ? "custom " : ""}request ${order.id} from @${order.user}`
  );

  save();

  toast("Request sent!");

  render();
}

/* =========================================================
   CUSTOMIZER
   ========================================================= */

function getCustomDraft(){

  if(!state.customDraft){

    state.customDraft={
      base:"base1",
      accessories:[],
      size:"Medium",
      notes:"",
      reference:"",
      drawing:""
    };
  }

  return state.customDraft;
}

function customizePage(){

  if(!requireLogin()) return "";

  const draft=getCustomDraft();

  const base=state.custom.bases.find(
    item=>item.id===draft.base
  );

  const accessories=state.custom.accessories.filter(
    item=>draft.accessories.includes(item.id)
  );

  let min=base ? base.min : 0;
  let max=base ? base.max : 0;

  accessories.forEach(item=>{
    min+=item.min;
    max+=item.max;
  });

  return `
  <section class="hero">

    <div class="eyebrow">
      custom studio
    </div>

    <h1>
      Make it yours.
    </h1>

    <p>
      Choose a base, design it, add instructions,
      and send it to the artist for review.
    </p>

  </section>

  <div class="panel">

    <div class="field">

      <label>BASE</label>

      <select onchange="changeCustomBase(this.value)">

        ${state.custom.bases.map(item=>`

          <option
            value="${item.id}"
            ${item.id===draft.base ? "selected" : ""}
          >
            ${item.emoji}
            ${escapeHTML(item.name)}
            · ${money(item.min)}–${money(item.max)}
          </option>

        `).join("")}

      </select>

    </div>

    <div class="field">

      <label>ACCESSORIES / OPTIONS</label>

      ${state.custom.accessories.map(item=>`

        <label>

          <input
            type="checkbox"
            ${draft.accessories.includes(item.id) ? "checked" : ""}
            onchange="toggleCustomAccessory('${item.id}',this.checked)"
          >

          ${item.emoji}
          ${escapeHTML(item.name)}

          (+${money(item.min)}–${money(item.max)})

        </label>

      `).join("")}

    </div>

    <div class="field">

      <label>SIZE</label>

      <select onchange="setCustomSize(this.value)">

        ${state.custom.sizes.map(size=>`

          <option
            ${size===draft.size ? "selected" : ""}
          >
            ${escapeHTML(size)}
          </option>

        `).join("")}

      </select>

    </div>

    <div class="notice success">

      <b>
        Estimated price:
        ${money(min)}–${money(max)}
      </b>

      <br>

      <span class="muted">
        Final price is personally determined
        by the artist after reviewing the design.
      </span>

    </div>

    <div class="field">

      <label>EXTRA INSTRUCTIONS</label>

      <textarea
        onchange="setCustomField('notes',this.value)"
        placeholder="Colours, vibe, details, changes..."
      >${escapeHTML(draft.notes)}</textarea>

    </div>

    <div class="field">

      <label>REFERENCE IMAGE / FILE</label>

      <input
        value="${escapeHTML(draft.reference)}"
        placeholder="Demo: reference.png"
        onchange="setCustomField('reference',this.value)"
      >

    </div>

    <div class="panel">

      <h3>Create by Hand</h3>

      <p class="muted">
        This demo stores a drawing/reference description.
        The production version will use a real drawing canvas
        and secure file storage.
      </p>

      <button
        class="btn"
        onclick="createDrawing()"
      >
        ✏️ Draw / Upload Reference
      </button>

      ${
        draft.drawing
        ?
        `
        <div class="notice success">
          Drawing/reference:
          ${escapeHTML(draft.drawing)}
        </div>
        `
        :
        ""
      }

    </div>

    <button
      class="btn primary"
      onclick="submitCustomRequest()"
    >
      Send Custom Request
    </button>

  </div>
  `;
}

function changeCustomBase(value){
  getCustomDraft().base=value;
  save();
  render();
}

function toggleCustomAccessory(id,enabled){

  const draft=getCustomDraft();

  if(enabled && !draft.accessories.includes(id)){
    draft.accessories.push(id);
  }

  if(!enabled){
    draft.accessories=draft.accessories.filter(
      item=>item!==id
    );
  }

  save();
  render();
}

function setCustomSize(value){
  getCustomDraft().size=value;
  save();
}

function setCustomField(field,value){
  getCustomDraft()[field]=value;
  save();
}

function createDrawing(){

  const description=prompt(
    "Demo drawing/reference description:"
  );

  if(!description) return;

  getCustomDraft().drawing=description;

  save();
  render();
}

function submitCustomRequest(){

  const draft=getCustomDraft();

  const base=state.custom.bases.find(
    item=>item.id===draft.base
  );

  const accessories=state.custom.accessories.filter(
    item=>draft.accessories.includes(item.id)
  );

  let min=base.min;
  let max=base.max;

  accessories.forEach(item=>{
    min+=item.min;
    max+=item.max;
  });

  state.pendingItems=[
    {
      custom:true,
      name:base.name,
      size:draft.size,
      quantity:1,
      estimate:[min,max],
      accessories:accessories.map(item=>item.name)
    }
  ];

  state.pendingCustom=true;
  state.customDraft=null;

  state.page="request";

  save();
  render();
}

/* =========================================================
   LOGIN
   ========================================================= */

function loginPage(){

  return `
  <div
    class="panel"
    style="max-width:520px;margin:40px auto"
  >

    <h1>Sign in</h1>

    <p class="muted">
      Browse without an account.
      Sign in when you want to request or purchase.
    </p>

    <div class="field">

      <label>USERNAME</label>

      <input id="loginUsername">

    </div>

    <div class="field">

      <label>PASSWORD</label>

      <input
        id="loginPassword"
        type="password"
      >

    </div>

    <div class="actions">

      <button
        class="btn primary"
        onclick="login()"
      >
        Sign in
      </button>

      <button
        class="btn"
        onclick="go('signup')"
      >
        Create account
      </button>

      <button
        class="btn"
        onclick="go('forgot')"
      >
        Forgot password
      </button>

    </div>

    <div class="notice">

      Demo customer:
      <b>maya</b>
      /
      <b>demo123</b>

    </div>

  </div>
  `;
}

function login(){

  const username=
    document.getElementById("loginUsername")
      .value.trim();

  const password=
    document.getElementById("loginPassword")
      .value;

  const found=state.users.find(
    user=>
      user.username===username &&
      user.password===password
  );

  if(!found){
    toast("Incorrect username or password.");
    return;
  }

  state.session=found.username;

  save();

  toast("Welcome back!");

  go("home");
}

function signupPage(){

  return `
  <div
    class="panel"
    style="max-width:520px;margin:40px auto"
  >

    <h1>Create Account</h1>

    <div class="field">

      <label>USERNAME</label>

      <input id="signupUsername">

    </div>

    <div class="field">

      <label>PASSWORD</label>

      <input
        id="signupPassword"
        type="password"
      >

    </div>

    <div class="field">

      <label>EMAIL</label>

      <input
        id="signupEmail"
        type="email"
      >

    </div>

    <button
      class="btn primary"
      onclick="signup()"
    >
      Create Account
    </button>

  </div>
  `;
}

function signup(){

  const username=
    document.getElementById("signupUsername")
      .value.trim();

  const password=
    document.getElementById("signupPassword")
      .value;

  const email=
    document.getElementById("signupEmail")
      .value.trim();

  if(!username || !password || !email){
    toast("Please fill everything in.");
    return;
  }

  if(state.users.some(
    user=>user.username.toLowerCase()===username.toLowerCase()
  )){
    toast("That username already exists.");
    return;
  }

  state.users.push({
    username,
    password,
    email,
    phone:"",
    address:""
  });

  state.session=username;

  save();

  go("home");
}

function forgotPage(){

  return `
  <div
    class="panel"
    style="max-width:520px;margin:40px auto"
  >

    <h1>Forgot Password</h1>

    <p class="muted">
      Production version will send a secure
      password reset email.
    </p>

    <div class="field">

      <label>EMAIL</label>

      <input
        id="forgotEmail"
        type="email"
      >

    </div>

    <button
      class="btn primary"
      onclick="demoForgotPassword()"
    >
      Send Reset Email
    </button>

  </div>
  `;
}

function demoForgotPassword(){

  toast(
    "Demo reset email sent. Production will use a secure reset link."
  );
}

function logout(){

  state.session=null;
  state.admin=false;

  save();

  go("home");
}

/* =========================================================
   ACCOUNT
   ========================================================= */

function accountPage(){

  if(!requireLogin()) return "";

  const user=currentUser();

  return `
  <div
    class="panel"
    style="max-width:650px"
  >

    <h1>
      @${escapeHTML(user.username)}
    </h1>

    <p class="muted">
      ${escapeHTML(user.email)}
    </p>

    <div class="field">

      <label>PHONE</label>

      <input
        id="accountPhone"
        value="${escapeHTML(user.phone || "")}"
      >

    </div>

    <div class="field">

      <label>SAVED SHIPPING ADDRESS</label>

      <textarea id="accountAddress">${escapeHTML(user.address || "")}</textarea>

    </div>

    <button
      class="btn primary"
      onclick="saveAccount()"
    >
      Save
    </button>

  </div>
  `;
}

function saveAccount(){

  const user=currentUser();

  user.phone=
    document.getElementById("accountPhone").value;

  user.address=
    document.getElementById("accountAddress").value;

  save();

  toast("Account saved.");

  render();
}

/* =========================================================
   CUSTOMER ORDERS
   ========================================================= */

function orderStatusClass(status){
  return status.toLowerCase().replace(/\s+/g,"-");
}

function customerOrdersPage(){

  if(!requireLogin()) return "";

  const orders=state.orders.filter(
    order=>order.user===state.session
  );

  if(!orders.length){

    return `
    <h1>My Orders</h1>

    <div class="empty">
      You haven't submitted any orders yet.
    </div>
    `;
  }

  let selected=orders.find(
    order=>order.id===state.selectedOrder
  );

  if(!selected){
    selected=orders[0];
  }

  return `
  <h1>My Orders</h1>

  <div class="split">

    <div class="list">

      ${orders.map(order=>`

        <div
          class="list-item ${
            selected.id===order.id ? "selected" : ""
          }"
          onclick="selectOrder('${order.id}')"
        >

          <b>${order.id}</b>

          <br>

          <span class="status">
            ${escapeHTML(order.status)}
          </span>

          <br>

          <small class="muted">
            ${new Date(order.created).toLocaleString()}
          </small>

        </div>

      `).join("")}

    </div>

    <div class="panel">

      ${orderDetails(selected,false)}

    </div>

  </div>
  `;
}

function selectOrder(id){

  state.selectedOrder=id;

  save();
  render();
}

function orderDetails(order,isAdmin){

  if(!order){
    return `<div class="empty">Order not found.</div>`;
  }

  const items=order.items.map(item=>{

    if(item.custom){

      return `
      <li>
        ${escapeHTML(item.name)}
        · ${escapeHTML(item.size)}
        × ${item.quantity}

        <br>

        <span class="muted">
          Estimate:
          ${money(item.estimate[0])}
          –
          ${money(item.estimate[1])}
        </span>
      </li>
      `;
    }

    const product=state.products.find(
      product=>product.id===item.productId
    );

    return `
    <li>
      ${escapeHTML(product?.name || "Item")}
      · ${escapeHTML(item.size)}
      × ${item.quantity}
    </li>
    `;
  }).join("");

  return `
  <div class="row">

    <h2>${order.id}</h2>

    <span class="status">
      ${escapeHTML(order.status)}
    </span>

  </div>

  <p class="muted">
    Created:
    ${new Date(order.created).toLocaleString()}
  </p>

  <h3>Items</h3>

  <ul>
    ${items}
  </ul>

  <p>
    <b>Price:</b>
    ${
      order.price===null
      ? "Pending artist review"
      : money(order.price)
    }
  </p>

  ${
    order.payBy
    ?
    `
    <p>
      <b>Pay by:</b>
      ${new Date(order.payBy).toLocaleDateString()}
    </p>
    `
    :
    ""
  }

  ${
    order.expectedDelivery
    ?
    `
    <p>
      <b>Expected delivery:</b>
      ${new Date(order.expectedDelivery).toLocaleDateString()}
    </p>
    `
    :
    ""
  }

  <p>
    <b>Shipping address:</b>
    ${escapeHTML(order.address || "Not supplied")}
  </p>

  <p>
    <b>Notes:</b>
    ${escapeHTML(order.notes || "—")}
  </p>

  ${
    order.status==="Ready for Payment" && !isAdmin
    ?
    `
    <button
      class="btn primary"
      onclick="openPayment('${order.id}')"
    >
      Open Payment
    </button>
    `
    :
    ""
  }

  ${
    !isAdmin &&
    !["Paid","Shipped","Completed","Cancelled"].includes(order.status)
    ?
    `
    <button
      class="btn danger"
      onclick="customerCancel('${order.id}')"
    >
      Request Cancellation
    </button>
    `
    :
    ""
  }

  ${
    isAdmin
    ?
    `
    <div class="actions">

      <button
        class="btn"
        onclick="adminChangeStatus('${order.id}')"
      >
        Change Status
      </button>

      <button
        class="btn"
        onclick="adminSetPrice('${order.id}')"
      >
        Set Price
      </button>

      <button
        class="btn green"
        onclick="adminReadyPayment('${order.id}')"
      >
        Ready for Payment
      </button>

      <button
        class="btn danger"
        onclick="adminCancel('${order.id}')"
      >
        Cancel
      </button>

    </div>
    `
    :
    ""
  }
  `;
}

/* =========================================================
   PAYMENT DEMO
   ========================================================= */

function openPayment(id){

  state.selectedOrder=id;
  state.page="payment";

  save();
  render();
}

function paymentPage(){

  const order=state.orders.find(
    order=>order.id===state.selectedOrder
  );

  if(!order){
    return `<div class="empty">Order not found.</div>`;
  }

  return `
  <div
    class="panel"
    style="max-width:600px;margin:30px auto"
  >

    <h1>Payment</h1>

    <div class="notice warning">

      <b>DEMO PAYMENT</b>

      <br>

      Do not enter real card information.
      This demo does not process real money.

    </div>

    <p>
      Order:
      <b>${order.id}</b>
    </p>

    <p>
      Total:
      <b>${money(order.price)}</b>
    </p>

    <div class="field">

      <label>CARD NUMBER</label>

      <input
        placeholder="4242 4242 4242 4242"
      >

    </div>

    <div class="field">

      <label>CARDHOLDER NAME</label>

      <input>

    </div>

    <div class="field">

      <label>EXPIRY / CVC</label>

      <input placeholder="12/30 · 123">

    </div>

    <button
      class="btn primary"
      onclick="demoPayment('${order.id}')"
    >
      Pay ${money(order.price)}
    </button>

  </div>
  `;
}

function demoPayment(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  order.status="Paid";

  order.history.push({
    status:"Paid",
    at:new Date().toISOString()
  });

  order.expectedDelivery=
    new Date(
      Date.now() +
      state.settings.expectedDeliveryDays *
      86400000
    ).toISOString();

  order.receipt=confirm(
    "Would you like a digital receipt emailed to you?"
  );

  notify(
    `${order.id} was paid by @${order.user}`
  );

  save();

  toast("Demo payment recorded.");

  go("orders");
}

/* =========================================================
   ADMIN
   ========================================================= */

function adminPage(){

  if(!state.admin){

    return `
    <div
      class="panel"
      style="max-width:520px;margin:40px auto"
    >

      <span class="admin-badge">
        PRIVATE ADMIN
      </span>

      <h1>Artist Access</h1>

      <div class="field">

        <label>PASSWORD</label>

        <input
          id="adminPassword"
          type="password"
        >

      </div>

      <button
        class="btn primary"
        onclick="adminLogin()"
      >
        Continue
      </button>

      <div class="notice">
        Demo password:
        <b>FawnDemo!</b>
      </div>

      <p class="muted">
        This is intentionally only prototype security.
        Production will use real authentication,
        server-side authorization, password hashing,
        protected sessions and rate limiting.
      </p>

    </div>
    `;
  }

  const page=state.adminPage || "requests";

  return `
  <section class="hero">

    <span class="admin-badge">
      ADMIN / ARTIST
    </span>

    <h1>
      What needs attention?
    </h1>

    <p>
      Fawn & Fang private control room.
    </p>

  </section>

  <div class="actions">

    ${[
      ["requests","New Requests"],
      ["chats","Chats"],
      ["orders","Orders"],
      ["products","Products"],
      ["inventory","Inventory"],
      ["custom","Customize"],
      ["notifications","Notifications"],
      ["settings","Settings"]
    ].map(([id,label])=>`

      <button
        class="btn ${
          page===id ? "primary" : ""
        }"
        onclick="openAdminSection('${id}')"
      >
        ${label}
      </button>

    `).join("")}

  </div>

  ${
    page==="requests" ? adminRequests() :
    page==="chats" ? adminChats() :
    page==="orders" ? adminOrders() :
    page==="products" ? adminProducts() :
    page==="inventory" ? adminInventory() :
    page==="custom" ? adminCustomizer() :
    page==="notifications" ? adminNotifications() :
    adminSettings()
  }
  `;
}

function adminLogin(){

  const password=
    document.getElementById("adminPassword").value;

  if(password!=="FawnDemo!"){
    toast("Incorrect password.");
    return;
  }

  state.admin=true;
  state.adminPage="requests";

  save();
  render();
}

function openAdminSection(section){

  state.adminPage=section;

  save();
  render();
}

/* REQUESTS */

function adminRequests(){

  const requests=state.orders.filter(
    order=>order.status==="Pending"
  );

  return `
  <div class="panel">

    <h2>
      New Requests (${requests.length})
    </h2>

    ${
      requests.length
      ?
      requests.map(order=>`

        <div class="panel">

          <div class="row">

            <b>${order.id}</b>

            <span>
              @${escapeHTML(order.user)}
            </span>

            <span class="muted">
              ${new Date(order.created).toLocaleString()}
            </span>

          </div>

          <p>
            ${
              order.custom
              ? "Custom request"
              : "Normal purchase request"
            }
          </p>

          <button
            class="btn primary"
            onclick="adminOpenOrder('${order.id}')"
          >
            Review
          </button>

        </div>

      `).join("")
      :
      `
      <div class="empty">
        Nothing waiting. ✨
      </div>
      `
    }

  </div>
  `;
}

/* ORDERS */

function adminOrders(){

  const orders=state.orders;

  return `
  <div class="panel">

    <h2>
      Permanent Order Book
    </h2>

    <div class="table-wrap">

      <table>

        <tr>
          <th>Order</th>
          <th>Customer</th>
          <th>Date</th>
          <th>Status</th>
          <th>Price</th>
          <th></th>
        </tr>

        ${
          orders.map(order=>`

            <tr>

              <td>${order.id}</td>

              <td>
                @${escapeHTML(order.user)}
              </td>

              <td>
                ${new Date(order.created).toLocaleDateString()}
              </td>

              <td>
                <span class="status">
                  ${escapeHTML(order.status)}
                </span>
              </td>

              <td>
                ${
                  order.price===null
                  ? "—"
                  : money(order.price)
                }
              </td>

              <td>

                <button
                  class="btn"
                  onclick="adminOpenOrder('${order.id}')"
                >
                  Open
                </button>

              </td>

            </tr>

          `).join("")
        }

      </table>

    </div>

    ${
      state.selectedOrder
      ?
      `
      <div class="panel">

        ${
          orderDetails(
            state.orders.find(
              order=>order.id===state.selectedOrder
            ),
            true
          )
        }

      </div>
      `
      :
      ""
    }

  </div>
  `;
}

function adminOpenOrder(id){

  state.selectedOrder=id;
  state.adminPage="orders";

  save();
  render();
}

/* PRODUCTS */

function adminProducts(){

  return `
  <div class="panel">

    <div class="row">

      <h2>Products</h2>

      <button
        class="btn primary"
        onclick="adminAddProduct()"
      >
        ＋ Add Product
      </button>

    </div>

    ${state.products.map(product=>`

      <div class="panel">

        <div class="row">

          <div>

            <b>
              ${escapeHTML(product.name)}
            </b>

            <br>

            <span class="muted">
              ${money(product.price)}
              · ${product.quantity} stock
              · ${escapeHTML(product.category)}
            </span>

          </div>

          <div class="actions">

            <button
              class="btn"
              onclick="adminEditProduct('${product.id}')"
            >
              Edit
            </button>

            <button
              class="btn danger"
              onclick="adminDeleteProduct('${product.id}')"
            >
              Remove
            </button>

          </div>

        </div>

      </div>

    `).join("")}

  </div>
  `;
}

function adminAddProduct(){

  const name=prompt("Product name:");

  if(!name) return;

  const price=Number(
    prompt("Price:","20")
  );

  const quantity=Number(
    prompt("Quantity:","1")
  );

  const categoryName=prompt(
    "Category:",
    CATEGORIES[0]
  );

  state.products.push({
    id:"p"+Date.now(),
    name,
    price:Number.isFinite(price)?price:20,
    quantity:Number.isFinite(quantity)?Math.max(0,quantity):1,
    category:CATEGORIES.includes(categoryName)
      ? categoryName
      : CATEGORIES[0],
    newArrival:confirm("Mark as NEW ARRIVAL?"),
    materials:"Handmade materials",
    sizes:["Small","Medium","Large"],
    emoji:"✨",
    description:"A new handmade Fawn & Fang piece."
  });

  save();
  render();
}

function adminEditProduct(id){

  const product=state.products.find(
    item=>item.id===id
  );

  if(!product) return;

  product.name=
    prompt("Product name:",product.name)
    || product.name;

  const price=Number(
    prompt("Price:",product.price)
  );

  if(Number.isFinite(price)){
    product.price=Math.max(0,price);
  }

  const quantity=Number(
    prompt("Quantity:",product.quantity)
  );

  if(Number.isFinite(quantity)){
    product.quantity=Math.max(0,quantity);
  }

  const categoryName=prompt(
    "Category:",
    product.category
  );

  if(CATEGORIES.includes(categoryName)){
    product.category=categoryName;
  }

  product.newArrival=
    confirm("Mark as NEW ARRIVAL?");

  save();
  render();
}

function adminDeleteProduct(id){

  if(!confirm("Remove this product?")){
    return;
  }

  state.products=
    state.products.filter(
      product=>product.id!==id
    );

  save();
  render();
}

/* INVENTORY */

function adminInventory(){

  return `
  <div class="panel">

    <h2>Manual Inventory</h2>

    <p class="muted">
      Inventory represents finished physical stock.
      Purchase requests do not reserve inventory.
    </p>

    <div class="table-wrap">

      <table>

        <tr>
          <th>Product</th>
          <th>Quantity</th>
          <th>Status</th>
          <th></th>
        </tr>

        ${state.products.map(product=>`

          <tr>

            <td>
              ${escapeHTML(product.name)}
            </td>

            <td>
              ${product.quantity}
            </td>

            <td>
              ${
                product.quantity>0
                ? "Available"
                : "Sold out"
              }
            </td>

            <td>

              <button
                class="btn"
                onclick="changeInventory('${product.id}')"
              >
                Set Quantity
              </button>

            </td>

          </tr>

        `).join("")}

      </table>

    </div>

  </div>
  `;
}

function changeInventory(id){

  const product=state.products.find(
    item=>item.id===id
  );

  if(!product) return;

  const quantity=Number(
    prompt(
      "Set quantity:",
      product.quantity
    )
  );

  if(!Number.isFinite(quantity)){
    return;
  }

  product.quantity=Math.max(0,quantity);

  save();
  render();
}

/* CUSTOMIZER ADMIN */

function adminCustomizer(){

  return `
  <div class="panel">

    <h2>Customizer Controls</h2>

    <p class="muted">
      These options can eventually be managed without
      editing website code.
    </p>

    <h3>Bases</h3>

    ${state.custom.bases.map(base=>`

      <div class="panel">

        <div class="row">

          <span>
            ${base.emoji}
            ${escapeHTML(base.name)}
            · ${money(base.min)}–${money(base.max)}
          </span>

          <button
            class="btn"
            onclick="editCustomBase('${base.id}')"
          >
            Edit
          </button>

        </div>

      </div>

    `).join("")}

    <button
      class="btn"
      onclick="addCustomBase()"
    >
      ＋ Add Base
    </button>

    <h3>Accessories</h3>

    ${state.custom.accessories.map(item=>`

      <div class="panel">

        <div class="row">

          <span>
            ${item.emoji}
            ${escapeHTML(item.name)}
            · ${money(item.min)}–${money(item.max)}
          </span>

          <button
            class="btn"
            onclick="editCustomAccessory('${item.id}')"
          >
            Edit
          </button>

        </div>

      </div>

    `).join("")}

    <button
      class="btn"
      onclick="addCustomAccessory()"
    >
      ＋ Add Accessory
    </button>

    <h3>Sizes</h3>

    <p class="muted">
      ${state.custom.sizes.map(escapeHTML).join(" · ")}
    </p>

    <h3>Drawing Templates</h3>

    <p class="muted">
      ${state.custom.templates.map(escapeHTML).join(" · ")}
    </p>

  </div>
  `;
}

function editCustomBase(id){

  const base=state.custom.bases.find(
    item=>item.id===id
  );

  if(!base) return;

  base.name=
    prompt("Name:",base.name)
    || base.name;

  const min=Number(
    prompt("Minimum:",base.min)
  );

  const max=Number(
    prompt("Maximum:",base.max)
  );

  if(Number.isFinite(min)){
    base.min=Math.max(0,min);
  }

  if(Number.isFinite(max)){
    base.max=Math.max(base.min,max);
  }

  save();
  render();
}

function addCustomBase(){

  const name=prompt("Base name:");

  if(!name) return;

  const min=Number(
    prompt("Minimum price:","20")
  );

  const max=Number(
    prompt("Maximum price:","30")
  );

  state.custom.bases.push({
    id:"base"+Date.now(),
    name,
    min:Number.isFinite(min)?min:20,
    max:Number.isFinite(max)?max:30,
    emoji:"✨"
  });

  save();
  render();
}

function editCustomAccessory(id){

  const item=state.custom.accessories.find(
    item=>item.id===id
  );

  if(!item) return;

  item.name=
    prompt("Name:",item.name)
    || item.name;

  const min=Number(
    prompt("Minimum:",item.min)
  );

  const max=Number(
    prompt("Maximum:",item.max)
  );

  if(Number.isFinite(min)){
    item.min=Math.max(0,min);
  }

  if(Number.isFinite(max)){
    item.max=Math.max(item.min,max);
  }

  save();
  render();
}

function addCustomAccessory(){

  const name=prompt("Accessory name:");

  if(!name) return;

  const min=Number(
    prompt("Minimum price:","3")
  );

  const max=Number(
    prompt("Maximum price:","7")
  );

  state.custom.accessories.push({
    id:"acc"+Date.now(),
    name,
    min:Number.isFinite(min)?min:3,
    max:Number.isFinite(max)?max:7,
    emoji:"✨"
  });

  save();
  render();
}

/* NOTIFICATIONS */

function adminNotifications(){

  return `
  <div class="panel">

    <h2>Notifications</h2>

    ${
      state.notifications.length
      ?
      state.notifications.map(notification=>`

        <div class="notice">

          <b>
            ${escapeHTML(notification.text)}
          </b>

          <br>

          <small class="muted">
            ${escapeHTML(notification.time)}
          </small>

        </div>

      `).join("")
      :
      `<div class="empty">
        No notifications.
      </div>`
    }

  </div>
  `;
}

/* SETTINGS */

function adminSettings(){

  return `
  <div class="panel">

    <h2>Settings</h2>

    <div class="field">

      <label>
        PAYMENT DEADLINE — DAYS
      </label>

      <input
        id="paymentDeadlineDays"
        type="number"
        min="1"
        value="${state.settings.paymentDeadlineDays}"
      >

    </div>

    <div class="field">

      <label>
        EXPECTED DELIVERY — DAYS AFTER PAYMENT
      </label>

      <input
        id="expectedDeliveryDays"
        type="number"
        min="1"
        value="${state.settings.expectedDeliveryDays}"
      >

    </div>

    <button
      class="btn primary"
      onclick="saveAdminSettings()"
    >
      Save Settings
    </button>

    <div class="notice warning">

      <b>Prototype security notice</b>

      <br><br>

      The demo uses browser storage and is NOT
      production-secure.

      A real launch needs server-side authentication,
      password hashing, authorization, secure sessions,
      protected storage, rate limiting, real payment
      processing and real email.

    </div>

    <button
      class="btn danger"
      onclick="exitAdmin()"
    >
      Exit Admin
    </button>

  </div>
  `;
}

function saveAdminSettings(){

  const paymentDays=Number(
    document.getElementById("paymentDeadlineDays").value
  );

  const deliveryDays=Number(
    document.getElementById("expectedDeliveryDays").value
  );

  if(Number.isFinite(paymentDays)){
    state.settings.paymentDeadlineDays=
      Math.max(1,paymentDays);
  }

  if(Number.isFinite(deliveryDays)){
    state.settings.expectedDeliveryDays=
      Math.max(1,deliveryDays);
  }

  save();

  toast("Settings saved.");
}

function exitAdmin(){

  state.admin=false;

  save();

  go("home");
}

/* =========================================================
   ADMIN ORDER ACTIONS
   ========================================================= */

function adminChangeStatus(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  const value=prompt(
    "Choose status:\n\n"+
    STATUSES.join("\n"),
    order.status
  );

  if(!value || !STATUSES.includes(value)){
    return;
  }

  order.status=value;

  order.history.push({
    status:value,
    at:new Date().toISOString()
  });

  notify(
    `${order.id} status changed to ${value}`
  );

  save();
  render();
}

function adminSetPrice(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  const price=Number(
    prompt(
      "Final price:",
      order.price ?? ""
    )
  );

  if(!Number.isFinite(price) || price<0){
    return;
  }

  order.price=price;

  save();

  toast("Final price saved.");

  render();
}

function adminReadyPayment(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  if(order.price===null){
    toast("Set the final price first.");
    return;
  }

  order.status="Ready for Payment";

  order.payBy=
    new Date(
      Date.now() +
      state.settings.paymentDeadlineDays *
      86400000
    ).toISOString();

  order.history.push({
    status:"Ready for Payment",
    at:new Date().toISOString()
  });

  notify(
    `${order.id} is Ready for Payment.`
  );

  save();

  render();
}

function customerCancel(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  if(
    ["Paid","Shipped","Completed","Cancelled"]
      .includes(order.status)
  ){
    toast(
      "This order cannot be cancelled at this stage."
    );
    return;
  }

  const reason=prompt(
    "Cancellation reason:"
  );

  if(!reason) return;

  order.status="Cancelled";
  order.cancellationReason=reason;

  order.history.push({
    status:"Cancelled",
    at:new Date().toISOString()
  });

  notify(
    `${order.id} was cancelled by @${order.user}.`
  );

  save();

  render();
}

function adminCancel(id){

  const order=state.orders.find(
    order=>order.id===id
  );

  if(!order) return;

  if(
    ["Paid","Shipped","Completed"]
      .includes(order.status)
  ){
    toast(
      "Paid/shipped/completed orders cannot be cancelled."
    );
    return;
  }

  const reason=prompt(
    "Cancellation reason:"
  );

  if(!reason) return;

  order.status="Cancelled";
  order.cancellationReason=reason;

  order.history.push({
    status:"Cancelled",
    at:new Date().toISOString()
  });

  notify(
    `${order.id} was cancelled by the artist.`
  );

  save();

  render();
}

/* =========================================================
   CHATS
   ========================================================= */

function adminChats(){

  const chats=state.chats;

  if(!chats.length){
    return `
    <div class="empty">
      No active chats.
    </div>
    `;
  }

  let selected=chats.find(
    chat=>chat.id===state.selectedChat
  );

  if(!selected){
    selected=chats[0];
  }

  return `
  <div class="split">

    <div class="list">

      ${chats.map(chat=>`

        <div
          class="list-item ${
            chat.id===selected.id ? "selected" : ""
          }"
          onclick="selectChat('${chat.id}')"
        >

          <b>
            @${escapeHTML(chat.user)}
          </b>

          <br>

          <span class="muted">
            ${
              escapeHTML(
                chat.messages[chat.messages.length-1]?.text ||
                "No messages"
              )
            }
          </span>

        </div>

      `).join("")}

    </div>

    <div class="chat">

      <div class="panel" style="margin:0;border:0;border-bottom:1px solid var(--line);border-radius:0">

        <b>
          @${escapeHTML(selected.user)}
        </b>

        ·

        ${escapeHTML(selected.order)}

      </div>

      <div class="messages">

        ${selected.messages.map(message=>`

          <div
            class="message ${
              message.from==="admin" ? "me" : ""
            }"
          >

            ${escapeHTML(message.text)}

            <br>

            <small class="muted">
              ${escapeHTML(message.at)}
            </small>

          </div>

        `).join("")}

      </div>

      <div class="composer">

        <input
          id="adminChatInput"
          placeholder="Message customer..."
        >

        <button
          class="btn primary"
          onclick="sendAdminMessage('${selected.id}')"
        >
          Send
        </button>

      </div>

    </div>

  </div>
  `;
}

function selectChat(id){

  state.selectedChat=id;

  save();
  render();
}

function sendAdminMessage(id){

  const chat=state.chats.find(
    chat=>chat.id===id
  );

  if(!chat) return;

  const input=
    document.getElementById("adminChatInput");

  const text=input.value.trim();

  if(!text) return;

  chat.messages.push({
    from:"admin",
    text,
    at:new Date().toLocaleString()
  });

  save();

  render();
}

/* =========================================================
   RESTOCK
   ========================================================= */

function requestRestock(id){

  if(!requireLogin()) return;

  const key=
    state.session + ":" + id;

  if(state.restockRequests[key]){
    toast("You've already requested more of this item.");
    return;
  }

  state.restockRequests[key]=true;

  const product=state.products.find(
    product=>product.id===id
  );

  notify(
    `Restock request from @${state.session} for ${product?.name || "item"}`
  );

  save();

  toast("✅ You've requested more of this item.");

  render();
}

/* =========================================================
   RENDER
   ========================================================= */

function render(){

  ensureBuckets();

  let content;

  switch(state.page){

    case "product":
      content=productPage();
      break;

    case "login":
      content=loginPage();
      break;

    case "signup":
      content=signupPage();
      break;

    case "forgot":
      content=forgotPage();
      break;

    case "request":
      content=requestPage();
      break;

    case "cart":
      content=cartPage();
      break;

    case "customize":
      content=customizePage();
      break;

    case "orders":
      content=customerOrdersPage();
      break;

    case "payment":
      content=paymentPage();
      break;

    case "account":
      content=accountPage();
      break;

    case "admin":
      content=adminPage();
      break;

    default:
      content=homePage();
  }

  document.getElementById("app").innerHTML=`

    ${header()}

    <div class="layout">

      ${sidebar()}

      <main>

        ${content}

        <div class="footer">
          Fawn & Fang · Official Demo
          · Handmade with claws & care 🦌
        </div>

      </main>

    </div>
  `;
}

/* =========================================================
   HIDDEN ADMIN SHORTCUT
   ========================================================= */

document.addEventListener(
  "keydown",
  function(event){

    if(
      event.ctrlKey &&
      event.shiftKey &&
      event.key.toLowerCase()==="a"
    ){

      state.page="admin";
      state.admin=false;

      save();
      render();
    }
  }
);

/* =========================================================
   DEMO RESET
   ========================================================= */

window.FawnFang={
  resetDemo:function(){
    localStorage.removeItem(STORAGE_KEY);
    location.reload();
  }
};

/* =========================================================
   START
   ========================================================= */

save();
render();

</script>

</body>
</html>