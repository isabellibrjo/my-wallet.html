
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>My Wallet ♡</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=Playfair+Display:ital,wght@0,500;1,500&display=swap');

:root {
  --cream:#FCF8F5;
  --rose:#C99DA2;
  --pink:#F3E3E5;
  --brown:#806269;
  --text:#644E54;
}
* { box-sizing:border-box; }
body {
  margin:0;
  padding:8px;
  background:transparent;
  color:var(--text);
  font-family:'DM Sans',sans-serif;
}
.wallet {
  max-width:650px;
  margin:auto;
  padding:24px;
  background:var(--cream);
  border:1px solid #E9D5D7;
  border-radius:22px;
}
header {
  display:flex;
  justify-content:space-between;
  align-items:center;
}
h1 {
  margin:0;
  font:italic 29px 'Playfair Display',serif;
}
.subtitle {
  font-size:11px;
  color:var(--rose);
  letter-spacing:1.5px;
}
.hero {
  display:flex;
  align-items:center;
  gap:22px;
  margin:23px 0;
}
.bear { width:115px; flex-shrink:0; }
.balance { flex:1; min-width:0; }
.small {
  font-size:11px;
  color:#A58A91;
  letter-spacing:.7px;
}
.amount {
  font:italic 35px 'Playfair Display',serif;
  margin:7px 0;
}
.bar {
  height:8px;
  border-radius:20px;
  background:var(--pink);
  overflow:hidden;
  margin-top:14px;
}
.fill {
  width:0;
  height:100%;
  background:var(--rose);
  transition:width .3s;
}
.settings {
  display:flex;
  align-items:center;
  gap:10px;
  margin:16px 0;
  font-size:12px;
}
input,select {
  min-width:0;
  width:100%;
  border:1px solid #E8D3D6;
  background:#FFFDFC;
  padding:11px;
  border-radius:11px;
  color:var(--text);
  font:inherit;
}
.settings input { width:110px; }
form {
  display:grid;
  grid-template-columns:1fr 1fr auto;
  gap:8px;
}
button {
  cursor:pointer;
  font:inherit;
}
.add {
  background:var(--brown);
  border:0;
  border-radius:11px;
  color:white;
  padding:11px 16px;
}
.summary {
  display:flex;
  justify-content:space-between;
  gap:10px;
  margin-top:20px;
  padding:16px 0;
  border-top:1px solid #E9D7DA;
  font-size:13px;
}
.section-title {
  font:italic 19px 'Playfair Display',serif;
  margin:8px 0;
}
.transaction {
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid #EEDFE1;
  padding:11px 0;
  font-size:12px;
}
.delete {
  border:0;
  background:transparent;
  color:#B77780;
  font-size:19px;
}
.empty {
  color:#AA9398;
  font-size:12px;
  font-style:italic;
}
.footer {
  text-align:center;
  font-size:10px;
  color:#B89BA1;
  margin-top:22px;
}
@media(max-width:450px) {
  .wallet {padding:16px;}
  .bear {width:85px;}
  .hero {gap:12px;}
  .amount {font-size:27px;}
  h1 {font-size:25px;}
  form {grid-template-columns:1fr 1fr;}
  .add {grid-column:1/-1;}
}
</style>
</head>
<body>

<div class="wallet">
  <header>
    <div>
      <h1>My Wallet ♡</h1>
      <div class="subtitle">LITTLE MONEY DIARY</div>
    </div>
    <span style="color:#C99DA2">✧ ♡ ✧</span>
  </header>

  <div class="hero">
    <svg class="bear" viewBox="0 0 150 155"
      xmlns="http://www.w3.org/2000/svg"
      aria-label="Cute teddy bear">
      <ellipse cx="75" cy="140" rx="48" ry="8"
        fill="#EAD9D7"/>
      <circle cx="39" cy="38" r="24"
        fill="#BE9280"/>
      <circle cx="111" cy="38" r="24"
        fill="#BE9280"/>
      <circle cx="39" cy="38" r="12"
        fill="#EBC8BE"/>
      <circle cx="111" cy="38" r="12"
        fill="#EBC8BE"/>
      <ellipse cx="75" cy="112" rx="43" ry="38"
        fill="#C9A18F"/>
      <circle cx="75" cy="65" r="54"
        fill="#C9A18F"/>
      <ellipse cx="75" cy="84" rx="24" ry="19"
        fill="#F5E4D9"/>
      <circle cx="57" cy="65" r="4"
        fill="#59434A"/>
      <circle cx="93" cy="65" r="4"
        fill="#59434A"/>
      <ellipse cx="75" cy="80" rx="7" ry="5"
        fill="#78575B"/>
      <path d="M75 85 Q68 94 63 88
               M75 85 Q82 94 87 88"
        fill="none" stroke="#78575B"
        stroke-width="2" stroke-linecap="round"/>
      <ellipse cx="45" cy="82" rx="9" ry="5"
        fill="#E8A7AA" opacity=".65"/>
      <ellipse cx="105" cy="82" rx="9" ry="5"
        fill="#E8A7AA" opacity=".65"/>
      <ellipse cx="75" cy="118" rx="24" ry="25"
        fill="#F5E4D9"/>
      <ellipse cx="35" cy="113" rx="13" ry="20"
        fill="#BE9280" transform="rotate(25 35 113)"/>
      <ellipse cx="115" cy="113" rx="13" ry="20"
        fill="#BE9280" transform="rotate(-25 115 113)"/>
      <ellipse cx="49" cy="139" rx="18" ry="12"
        fill="#BE9280"/>
      <ellipse cx="101" cy="139" rx="18" ry="12"
        fill="#BE9280"/>
      <path d="M75 106 C55 88 49 112 75 127
               C101 112 95 88 75 106Z"
        fill="#DFA9B1"/>
      <circle cx="70" cy="111" r="2" fill="#FFF5F5"/>
    </svg>

    <div class="balance">
      <div class="small">YOUR WEEKLY BALANCE</div>
      <div class="amount" id="remaining">$150.00</div>
      <div class="small" id="budgetLabel">
        of $150.00 this week
      </div>
      <div class="bar">
        <div class="fill" id="fill"></div>
      </div>
    </div>
  </div>

  <div class="settings">
    <label for="budget">Weekly budget ($)</label>
    <input id="budget" type="number"
      min="0" step="0.01" value="150">
  </div>

  <form id="transactionForm">
    <select id="type" aria-label="Transaction type">
      <option value="expense">Expense</option>
      <option value="income">Income</option>
    </select>
    <select id="category" aria-label="Category">
      <option value="Food">Food</option>
      <option value="Shopping">Shopping</option>
      <option value="Beauty">Beauty</option>
      <option value="Transport">Transport</option>
      <option value="Work">Work</option>
      <option value="Other">Other</option>
    </select>
    <input id="value" type="number"
      placeholder="Amount $" min="0.01"
      step="0.01" required>
    <button class="add" type="submit">Add +</button>
  </form>

  <div class="summary">
    <span id="income">Income: $0.00</span>
    <span id="spent">Spent: $0.00</span>
    <span id="left">Left: $150.00</span>
  </div>

  <div class="section-title">Little transactions ♡</div>
  <div id="transactions"></div>

  <div class="footer">
    made with love ♡ · my little money diary
  </div>
</div>

<script>
const KEY="my_wallet_bear_2027_v1";
const $=id=>document.getElementById(id);

let data;
try {
  data=JSON.parse(localStorage.getItem(KEY));
} catch {
  data=null;
}
if (!data || typeof data!=="object") {
  data={budget:150,transactions:[]};
}
if (!Array.isArray(data.transactions)) {
  data.transactions=[];
}
if (!Number.isFinite(data.budget) || data.budget<0) {
  data.budget=150;
}

function save() {
  try {
    localStorage.setItem(KEY,JSON.stringify(data));
  } catch(e) {
    console.warn("Storage unavailable",e);
  }
}

function weekKey() {
  const d=new Date();
  d.setHours(12,0,0,0);
  d.setDate(d.getDate()-(d.getDay()+6)%7);
  return d.getFullYear()+"-"+
    String(d.getMonth()+1).padStart(2,"0")+"-"+
    String(d.getDate()).padStart(2,"0");
}

function money(n) {
  return "$"+n.toFixed(2);
}

function render() {
  const current=data.transactions.filter(
    t=>t.week===weekKey()
  );
  const income=current
    .filter(t=>t.type==="income")
    .reduce((s,t)=>s+t.amount,0);
  const spent=current
    .filter(t=>t.type==="expense")
    .reduce((s,t)=>s+t.amount,0);
  const left=data.budget+income-spent;

  $("remaining").textContent=money(left);
  $("budgetLabel").textContent=
    "of "+money(data.budget)+" weekly budget";
  $("income").textContent="Income: "+money(income);
  $("spent").textContent="Spent: "+money(spent);
  $("left").textContent="Left: "+money(left);
  $("fill").style.width=
    Math.min(100,data.budget>0
      ?spent/data.budget*100
      :spent>0?100:0)+"%";
  $("budget").value=data.budget;

  const list=$("transactions");
  list.replaceChildren();

  if (!current.length) {
    const p=document.createElement("p");
    p.className="empty";
    p.textContent="No transactions yet, lovely ♡";
    list.appendChild(p);
  }

  current.slice().reverse().forEach(t=>{
    const row=document.createElement("div");
    row.className="transaction";

    const label=document.createElement("span");
    label.textContent=
      (t.type==="income"?"+ ":"− ")+
      money(t.amount)+" · "+t.category;

    const btn=document.createElement("button");
    btn.className="delete";
    btn.textContent="×";
    btn.setAttribute("aria-label","Delete transaction");
    btn.onclick=()=>{
      data.transactions=data.transactions
        .filter(x=>x.id!==t.id);
      save();
      render();
    };

    row.append(label,btn);
    list.appendChild(row);
  });
}

$("budget").addEventListener("change",e=>{
  const n=Number(e.target.value);
  if (!Number.isFinite(n)||n<0) {
    render();
    return;
  }
  data.budget=n;
  save();
  render();
});

$("transactionForm").addEventListener("submit",e=>{
  e.preventDefault();
  const amount=Number($("value").value);
  if (!Number.isFinite(amount)||amount<=0) return;

  data.transactions.push({
    id:Date.now()+"-"+Math.random(),
    amount,
    type:$("type").value,
    category:$("category").value,
    week:weekKey()
  });

  save();
  e.target.reset();
  render();
});

render();
</script>
</body>
</html>
