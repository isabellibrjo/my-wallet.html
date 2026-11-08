# my-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>My Wallet - Personal Planner 2027</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;1,400;1,500&display=swap" rel="stylesheet">
<style>
:root {
  --cream: #FAF5F0;
  --rose: #B88E8A;
  --blush: #E9D5D2;
  --brown: #795D61;
  --ink: #60464B;
}
* {box-sizing:border-box}
body {
  margin:0;
  padding:12px;
  background:transparent;
  font-family:"DM Sans",sans-serif;
  color:var(--ink);
}
.wallet {
  max-width:680px;
  margin:auto;
  padding:25px;
  background:var(--cream);
  border:1px solid var(--rose);
  border-radius:25px;
}
header {
  display:flex;
  justify-content:space-between;
  align-items:center;
}
h1 {
  font:italic 30px "Playfair Display",serif;
  margin:0;
}
.sparkles {color:var(--rose)}
.main {
  display:flex;
  align-items:center;
  gap:20px;
  margin:25px 0;
}
.bear {width:125px;flex-shrink:0}
.balance {flex:1;min-width:0}
.small {
  color:#A18C91;
  font-size:12px;
  letter-spacing:.5px;
}
.amount {
  font:italic 39px "Playfair Display",serif;
  margin:6px 0;
}
.bar {
  background:var(--blush);
  height:9px;
  border-radius:20px;
  overflow:hidden;
  margin-top:14px;
}
.fill {
  height:100%;
  width:0%;
  background:var(--brown);
  transition:width .3s;
}
form {
  display:grid;
  grid-template-columns:1fr 1.3fr auto;
  gap:9px;
}
input,select {
  width:100%;
  min-width:0;
  padding:12px;
  border:1px solid var(--blush);
  background:#FFFCFA;
  border-radius:13px;
  color:var(--ink);
  font:inherit;
}
button {
  cursor:pointer;
  font:inherit;
}
.add {
  border:0;
  background:var(--brown);
  color:white;
  padding:12px 20px;
  border-radius:13px;
  font-weight:600;
}
.summary {
  display:flex;
  justify-content:space-between;
  gap:10px;
  flex-wrap:wrap;
  border-top:1px solid var(--blush);
  margin-top:22px;
  padding-top:16px;
  font-size:13px;
}
.settings {
  display:flex;
  align-items:center;
  gap:10px;
  margin-bottom:20px;
  font-size:12px;
}
.settings input {max-width:100px}
.expense {
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:10px;
  border-bottom:1px solid var(--blush);
  padding:11px 0;
  font-size:13px;
}
.remove {
  border:0;
  background:none;
  color:#A45C65;
  font-size:20px;
}
.empty {
  font-size:12px;
  color:#A18C91;
  font-style:italic;
}
@media(max-width:480px) {
  .wallet {padding:17px}
  h1 {font-size:25px}
  .bear {width:90px}
  .main {gap:12px}
  .amount {font-size:29px}
  form {grid-template-columns:1fr 1fr}
  .add {grid-column:1/-1}
}
</style>
</head>
<body>

<section class="wallet">
  <header>
    <h1>My Wallet ♡</h1>
    <span class="sparkles">✦ ✧ ✦</span>
  </header>

  <div class="main">
    <!-- Teddy bear drawn with SVG -->
    <svg class="bear" viewBox="0 0 130 145"
      xmlns="http://www.w3.org/2000/svg"
      role="img" aria-label="Cute teddy bear">
      <circle cx="32" cy="30" r="21" fill="#C9A58F"/>
      <circle cx="98" cy="30" r="21" fill="#C9A58F"/>
      <circle cx="32" cy="30" r="11" fill="#E9C9BD"/>
      <circle cx="98" cy="30" r="11" fill="#E9C9BD"/>
      <ellipse cx="65" cy="105" rx="44" ry="36" fill="#C9A58F"/>
      <circle cx="65" cy="56" r="46" fill="#C9A58F"/>
      <ellipse cx="65" cy="73" rx="23" ry="17" fill="#F1DDD0"/>
      <circle cx="49" cy="53" r="4" fill="#513C3C"/>
      <circle cx="81" cy="53" r="4" fill="#513C3C"/>
      <ellipse cx="65" cy="68" rx="7" ry="5" fill="#795D61"/>
      <path d="M65 73 Q59 82 54 77 M65 73 Q71 82 76 77"
        fill="none" stroke="#795D61"
        stroke-width="2" stroke-linecap="round"/>
      <ellipse cx="43" cy="69" rx="9" ry="5"
        fill="#DBA2A2" opacity=".7"/>
      <ellipse cx="87" cy="69" rx="9" ry="5"
        fill="#DBA2A2" opacity=".7"/>
      <ellipse cx="65" cy="111" rx="25" ry="22" fill="#F1DDD0"/>
      <ellipse cx="30" cy="124" rx="16" ry="12" fill="#C9A58F"/>
      <ellipse cx="100" cy="124" rx="16" ry="12" fill="#C9A58F"/>
      <path d="M65 91 L53 85 Q45 88 54 98 Z" fill="#B88E8A"/>
      <path d="M65 91 L77 85 Q85 88 76 98 Z" fill="#B88E8A"/>
      <circle cx="65" cy="91" r="5" fill="#795D61"/>
    </svg>

    <div class="balance">
      <div class="small">YOUR WEEKLY BALANCE</div>
      <div class="amount" id="remaining">$150.00</div>
      <div class="small" id="budgetLabel">of $150.00 this week</div>
      <div class="bar"><div class="fill" id="fill"></div></div>
    </div>
  </div>

  <div class="settings">
    <label for="budget">Weekly budget ($)</label>
    <input type="number" id="budget"
      min="0" step="0.01" value="150">
  </div>

  <form id="expenseForm">
    <input type="number" id="expenseAmount"
      min="0.01" step="0.01"
      placeholder="Amount" required>
    <select id="category" required>
      <option value="">Category</option>
      <option>Food</option>
      <option>Shopping</option>
      <option>Beauty</option>
      <option>Transport</option>
      <option>Other</option>
    </select>
    <button class="add" type="submit">Add +</button>
  </form>

  <div class="summary">
    <span id="spent">Spent: $0.00</span>
    <span id="left">Left: $150.00</span>
  </div>
  <div id="expenses"></div>
</section>

<script>
const storageKey = "personal2027_mywallet_v1";
const $ = id => document.getElementById(id);

let data;
try {
  data = JSON.parse(localStorage.getItem(storageKey));
} catch {
  data = null;
}
if (!data || typeof data !== "object") {
  data = {budget:150,expenses:[]};
}
if (!Array.isArray(data.expenses)) data.expenses=[];
if (!Number.isFinite(data.budget) || data.budget<0) {
  data.budget=150;
}

function save() {
  try {
    localStorage.setItem(storageKey,JSON.stringify(data));
  } catch {}
}
function dateKey(date=new Date()) {
  const y=date.getFullYear();
  const m=String(date.getMonth()+1).padStart(2,"0");
  const d=String(date.getDate()).padStart(2,"0");
  return `${y}-${m}-${d}`;
}
function weekKey() {
  const d=new Date();
  d.setDate(d.getDate()-(d.getDay()+6)%7);
  return dateKey(d);
}
function money(n) {
  return "$"+n.toFixed(2);
}
function render() {
  const week=weekKey();
  const current=data.expenses.filter(e=>e.week===week);
  const spent=current.reduce((s,e)=>s+e.amount,0);
  const left=data.budget-spent;

  $("remaining").textContent=money(left);
  $("budgetLabel").textContent=
    "of "+money(data.budget)+" this week";
  $("spent").textContent="Spent: "+money(spent);
  $("left").textContent="Left: "+money(left);
  $("fill").style.width=
    Math.min(100,data.budget>0?spent/data.budget*100:0)+"%";
  $("budget").value=data.budget;

  const list=$("expenses");
  list.replaceChildren();

  if (!current.length) {
    const p=document.createElement("p");
    p.className="empty";
    p.textContent="Nothing spent yet this week ♡";
    list.appendChild(p);
  }

  current.slice().reverse().forEach(e=>{
    const row=document.createElement("div");
    row.className="expense";

    const label=document.createElement("span");
    label.textContent=e.category+" · "+money(e.amount);

    const btn=document.createElement("button");
    btn.className="remove";
    btn.textContent="×";
    btn.setAttribute("aria-label","Delete expense");
    btn.onclick=()=>{
      data.expenses=data.expenses.filter(x=>x.id!==e.id);
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

$("expenseForm").addEventListener("submit",e=>{
  e.preventDefault();
  const amount=Number($("expenseAmount").value);
  const category=$("category").value;
  if (!Number.isFinite(amount)||amount<=0||!category) return;

  data.expenses.push({
    id:crypto.randomUUID(),
    amount,
    category,
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



