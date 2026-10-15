[review1_units1-4_quiz.html](https://github.com/user-attachments/files/33469422/review1_units1-4_quiz.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1">
<title>Review 1 | Units 1–4 Quiz Battle</title>
<style>
:root{--navy:#172554;--purple:#6d45c7;--teal:#16a89a;--ink:#202747;--muted:#69718c;--paper:#fff;--line:#e3e7f1}
*{box-sizing:border-box}body{margin:0;min-height:100vh;padding:22px;font-family:system-ui,-apple-system,Segoe UI,Arial,sans-serif;background:linear-gradient(135deg,#102b63,#6038a7 55%,#159e9a);color:var(--ink);display:grid;place-items:center}
.app{width:min(900px,100%);background:var(--paper);border-radius:24px;overflow:hidden;box-shadow:0 24px 70px #08123c55}
header{padding:26px clamp(20px,5vw,42px);color:white;background:linear-gradient(110deg,#176e9b,#159b94);position:relative}
header:after{content:"";position:absolute;inset:0;pointer-events:none;opacity:.16;background:repeating-linear-gradient(35deg,transparent 0 8px,#fff 9px 10px)}
header>*{position:relative;z-index:1} .eyebrow{font-weight:800;letter-spacing:1.8px;font-size:.8rem;opacity:.9}h1{font-size:clamp(1.7rem,5vw,2.7rem);margin:8px 0}header p{margin:0;opacity:.92;line-height:1.5}
main{padding:clamp(20px,4vw,38px)}.stats{display:flex;gap:10px;flex-wrap:wrap;align-items:center;justify-content:space-between;margin-bottom:20px}
.pill{padding:8px 12px;border-radius:999px;background:#f0edff;color:#5433a0;font-size:.85rem;font-weight:800}.progress{height:9px;background:#edf0f7;border-radius:20px;overflow:hidden;margin:16px 0 25px}.bar{height:100%;width:0;background:linear-gradient(90deg,var(--purple),var(--teal));transition:width .3s}
.section{color:#12877e;text-transform:uppercase;font-size:.78rem;letter-spacing:1.3px;font-weight:900;margin-bottom:9px}
.q{font-size:clamp(1.12rem,2.5vw,1.4rem);font-weight:800;line-height:1.45;margin:0 0 20px;white-space:pre-line}
.answers{display:grid;grid-template-columns:1fr 1fr;gap:12px}.option{border:2px solid var(--line);background:white;border-radius:14px;padding:15px;text-align:left;font:inherit;color:var(--ink);cursor:pointer;transition:.15s;line-height:1.4}.option:hover:not(:disabled){border-color:#9b82e3;background:#faf8ff;transform:translateY(-1px)}.option:disabled{cursor:default}.option.correct{border-color:#19a47b;background:#e9faf3}.option.wrong{border-color:#db5369;background:#fff0f2}.letter{display:inline-grid;place-items:center;width:27px;height:27px;border-radius:8px;background:#efedfa;color:#6542b5;font-weight:900;margin-right:8px;font-size:.85rem}
.feedback{min-height:28px;margin-top:17px;font-weight:700;line-height:1.5}.bottom{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:20px;flex-wrap:wrap}.score{font-weight:800;color:#535c78}.btn{border:0;border-radius:12px;padding:13px 20px;background:var(--purple);color:white;font-size:1rem;font-weight:800;cursor:pointer}.btn:hover{filter:brightness(.92)}.btn:disabled{opacity:.4;cursor:not-allowed}.hidden{display:none!important}.start{text-align:center;padding:12px 0 18px}.start .big{font-size:4rem}.start h2,.results h2{font-size:2rem;margin:10px 0}.start p,.results p{color:var(--muted);line-height:1.6;max-width:620px;margin:10px auto 22px}.startgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin:24px 0}.tile{padding:15px 8px;background:#f6f7fc;border-radius:14px;font-weight:800}.tile span{display:block;font-size:1.5rem;margin-bottom:5px}.results{text-align:center;padding:20px 0}.results .big{font-size:4rem}.review{margin-top:24px;text-align:left;background:#f7f8fc;border-radius:14px;padding:16px}.review h3{margin-top:0}.review p{margin:10px 0;color:var(--ink)}
@media(max-width:580px){body{padding:10px}.answers{grid-template-columns:1fr}.startgrid{grid-template-columns:1fr}.bottom .btn{width:100%}}
</style></head>
<body><div class="app">
<header><div class="eyebrow">ENGLISH • UNITS 1–4</div><h1>REVIEW 1: QUIZ BATTLE</h1><p>Vocabulary · Grammar · Reading · Think fast, choose wisely, and beat your best score!</p></header>
<main>
<section id="welcome" class="start">
<div class="big">🎯</div><h2>Ready for the challenge?</h2>
<p>Test yourself on the Review 1 workbook pages. Each question is worth one point. Read carefully—some answers are easy to mix up!</p>
<div class="startgrid"><div class="tile"><span>📚</span>Vocabulary</div><div class="tile"><span>✍️</span>Grammar</div><div class="tile"><span>🔎</span>Reading</div></div>
<button class="btn" id="start">Start the quiz →</button>
</section>
<section id="game" class="hidden">
<div class="stats"><span class="pill" id="section">VOCABULARY</span><span class="pill" id="count">Question 1 of 30</span></div>
<div class="progress"><div class="bar" id="bar"></div></div>
<p class="q" id="question"></p><div class="answers" id="answers"></div>
<div class="feedback" id="feedback" aria-live="polite"></div>
<div class="bottom"><span class="score" id="score">⭐ Score: 0</span><button class="btn" id="next" disabled>Next question →</button></div>
</section>
<section id="results" class="results hidden"><div class="big" id="emoji">🏆</div><h2>Quiz complete!</h2><p id="final"></p><p id="message"></p><button class="btn" id="again">Play again ↻</button><div id="review" class="review"></div></section>
</main></div>
<script>
const questions = [
{ s:"Vocabulary · Exercise 1", q:"The shop exchanged the item ___ .", o:["and she won a medal","because I had a receipt","there were a lot of floods","we beat the other team"], a:1, e:"A receipt is proof of purchase, so the shop can exchange the item."},
{ s:"Vocabulary · Exercise 1", q:"We scored a goal in the last minute and ___ .", o:["missed the opportunity to go on the trip","he’s just entered an international competition","we beat the other team","there were a lot of floods"], a:2, e:"Scoring a late goal can mean your team beat the other team."},
{ s:"Vocabulary · Exercise 1", q:"The young tennis player was confident ___ .", o:["because I had a receipt","and she won a medal","there were a lot of floods","we beat the other team"], a:1, e:"The sentence halves match: the confident tennis player won a medal."},
{ s:"Vocabulary · Exercise 1", q:"It poured with rain all night and I’m not surprised that ___ .", o:["there were a lot of floods","we beat the other team","she won a medal","I had a receipt"], a:0, e:"Heavy rain can cause floods."},
{ s:"Vocabulary · Exercise 1", q:"Mike is a talented canoeist ___ .", o:["because I had a receipt","and he’s just entered an international competition","there were a lot of floods","we beat the other team"], a:1, e:"A talented canoeist might enter an international competition."},
{ s:"Vocabulary · Exercise 1", q:"I didn’t receive the letter in time, so ___ .", o:["I missed the opportunity to go on the trip","we beat the other team","she won a medal","there were a lot of floods"], a:0, e:"The late letter meant the opportunity was missed."},
{ s:"Vocabulary · Exercise 2", q:"“Did you see the ___ on TV last night?” “Yes, it would be sensible to take an umbrella.”", o:["forecast","promotion","storm","refund"], a:0, e:"A weather forecast tells us what weather to expect."},
{ s:"Vocabulary · Exercise 2", q:"“Did you know the girl who ___ you in the shop?” “Yes, she joined the tennis club last week.”", o:["served","burned down","gave","missed"], a:0, e:"A shop assistant serves customers."},
{ s:"Vocabulary · Exercise 2", q:"“That’s the house that ___ last week.” “I know. I think someone did it deliberately.”", o:["burned down","gave a refund","served","joined"], a:0, e:"A house can burn down in a fire."},
{ s:"Vocabulary · Exercise 2", q:"“That shop has ___ for students on Thursdays.” “We’d better go there.”", o:["a promotion","a snowstorm","a refund","a forecast"], a:0, e:"A promotion is a special offer or sales deal."},
{ s:"Vocabulary · Exercise 2", q:"“There was a heavy ___ on Sunday, wasn’t there?” “We couldn’t go anywhere!”", o:["snowstorm","promotion","refund","forecast"], a:0, e:"A heavy snowstorm can make travel difficult."},
{ s:"Vocabulary · Exercise 2", q:"“But, ___ me the chance to do my homework.”", o:["you gave","you served","you burned down","you forecast"], a:0, e:"The phrase is “give someone the chance to do something.”"},
{ s:"Vocabulary · Exercise 3", q:"There was a really bad storm, with thunder and ___ .", o:["lightning","refund","sociable","send back"], a:0, e:"Thunder and lightning are associated with storms."},
{ s:"Vocabulary · Exercise 3", q:"I took the item back to the store and got a ___ .", o:["refund","lightning","sociable","send back"], a:0, e:"A refund is money returned to a customer."},
{ s:"Vocabulary · Exercise 3", q:"We had to ___ the game because it didn’t work on our computer.", o:["send back","lightning","refund","sociable"], a:0, e:"“Send back” means return something."},
{ s:"Vocabulary · Exercise 3", q:"Tess loves being with other people—she’s very ___ .", o:["sociable","lightning","refund","send back"], a:0, e:"A sociable person enjoys being with other people."},
{ s:"Vocabulary · Exercise 4", q:"If Mel says she’ll do something, she will. She’s very ___ .", o:["reliable","sensible","sensitive","sociable"], a:0, e:"A reliable person does what they promise."},
{ s:"Vocabulary · Exercise 4", q:"Angela always knows the answer—she’s really ___ .", o:["intelligent","sensitive","reliable","sociable"], a:0, e:"Intelligent means clever or good at understanding things."},
{ s:"Vocabulary · Exercise 4", q:"Our team is the best—we didn’t ___ last year!", o:["lose","loose","lost","losing"], a:0, e:"After “didn’t,” use the base form: lose."},
{ s:"Vocabulary · Exercise 4", q:"You can’t say anything to Michelle. She’s very ___ and is easily upset.", o:["sensitive","sensible","reliable","intelligent"], a:0, e:"A sensitive person may be easily upset by comments."},
{ s:"Vocabulary · Exercise 4", q:"This is an expensive bag, but the shop gave me a really big ___ on it.", o:["discount","promotion","forecast","refund"], a:0, e:"A discount is a reduction in the price."},
{ s:"Vocabulary · Exercise 4", q:"It rained for days and we watched the water ___ and get closer to our house.", o:["rise","raise","arise","rose"], a:0, e:"Water levels rise; “rise” does not take an object."},
{ s:"Grammar · Exercise 1", q:"Lucy didn’t buy ___ shoes on Saturday.", o:["any","much","many much"], a:0, e:"Use “any” in negative sentences with plural countable nouns."},
{ s:"Grammar · Exercise 1", q:"Sophia wants to buy some / any new pens for school. Choose the correct word.", o:["some","any","many"], a:0, e:"“Some” is common in affirmative sentences."},
{ s:"Grammar · Exercise 1", q:"There are ___ places that sell accessories for phones.", o:["plenty of","much","a plenty"], a:0, e:"“Plenty of” can be used with plural countable nouns."},
{ s:"Grammar · Exercise 1", q:"I haven’t got ___ time—I have to go in 10 minutes.", o:["much","many","plenty"], a:0, e:"Time is uncountable, so use “much” in this negative sentence."},
{ s:"Grammar · Exercise 1", q:"How ___ exercises do we have to do?", o:["many","much","plenty"], a:0, e:"Exercises are countable plural nouns, so use “many”."},
{ s:"Grammar · Exercise 1", q:"___ teens under the age of 18 can watch that film—it’s for over-18s only.", o:["Any","No","Much"], a:1, e:"“No teens” means zero teens are allowed."},
{ s:"Grammar · Exercise 2", q:"Jason considered ___ a football club.", o:["joining","join","to join"], a:0, e:"“Consider” is followed by a verb in the -ing form."},
{ s:"Grammar · Exercise 2", q:"My mum couldn’t stand ___ sports when she was at school.", o:["doing","do","to do"], a:0, e:"“Can’t stand” is followed by the -ing form."},
{ s:"Grammar · Exercise 2", q:"Jasmine and her mum enjoyed ___ time together.", o:["spending","spend","to spend"], a:0, e:"“Enjoy” is followed by the -ing form."},
{ s:"Grammar · Exercise 2", q:"My brother doesn’t mind ___ me to your house.", o:["driving","drive","to drive"], a:0, e:"“Mind” is followed by the -ing form."},
{ s:"Grammar · Exercise 2", q:"She imagined herself ___ an ice cream.", o:["eating","eat","to eat"], a:0, e:"“Imagine” is followed by a noun or an -ing form."},
{ s:"Grammar · Exercise 2", q:"___ for exams can be really hard.", o:["Studying","Study","To studying"], a:0, e:"An -ing form can function as the subject of a sentence."},
{ s:"Grammar · Exercise 3", q:"Mara ___ going for a run every morning. (enjoy)", o:["enjoys","is enjoying","enjoy"], a:0, e:"Use the present simple for routines; with Mara, add -s."},
{ s:"Grammar · Exercise 3", q:"Look! The weather ___ worse. (get)", o:["is getting","gets","get"], a:0, e:"“Look!” signals something happening now: present continuous."},
{ s:"Grammar · Exercise 3", q:"I ___ the answer to the question. (know)", o:["know","am knowing","knows"], a:0, e:"“Know” is usually a stative verb and is used in the simple form."},
{ s:"Grammar · Exercise 3", q:"It’s a really expensive bike. It ___ over $400. (cost)", o:["costs","is costing","cost"], a:0, e:"Use the present simple for a general fact or price."},
{ s:"Grammar · Exercise 3", q:"She ___ a book on her phone at the moment. (read)", o:["is reading","reads","read"], a:0, e:"“At the moment” indicates an action happening now."},
{ s:"Grammar · Exercise 3", q:"Marcia and Maisy ___ their friends at the shopping centre tonight. (meet)", o:["are meeting","meet","meets"], a:0, e:"Present continuous can describe a planned future arrangement."},
{ s:"Grammar · Exercise 5", q:"I used to spend ___ money on clothes.", o:["a lot of","much","many"], a:0, e:"“A lot of” works naturally with uncountable “money” in an affirmative sentence."},
{ s:"Grammar · Exercise 5", q:"Many people are tired ___ spending so much time looking at screens.", o:["of","in","at"], a:0, e:"The expression is “tired of doing something.”"},
{ s:"Grammar · Exercise 5", q:"Remember that we ___ at the shopping centre at 8 pm tonight.", o:["are meeting","meet at","meeting"], a:0, e:"Present continuous describes a planned arrangement."},
{ s:"Grammar · Exercise 5", q:"Could you give us the same discount we ___ to get?", o:["used","use","are used"], a:0, e:"“Used to” describes a past habit or situation."},
{ s:"Grammar · Exercise 6", q:"Choose the corrected sentence: “Last night, I bought a shirt and a trousers online.”", o:["Last night, I bought a shirt and trousers online.","Last night, I bought a shirt and a trouser online.","Last night, I buy a shirt and trousers online."], a:0, e:"“Trousers” is plural and normally does not take “a.”"},
{ s:"Grammar · Exercise 6", q:"Choose the corrected sentence: “My best friend is very good in sailing.”", o:["My best friend is very good at sailing.","My best friend is very good on sailing.","My best friend very good at sailing."], a:0, e:"The correct collocation is “good at” an activity."},
{ s:"Grammar · Exercise 6", q:"Choose the corrected sentence: “I really like buy clothes online.”", o:["I really like buying clothes online.","I really like to buying clothes online.","I really likes buying clothes online."], a:0, e:"“Like” can be followed by an -ing form: “like buying.”"},
{ s:"Grammar · Exercise 6", q:"Choose the corrected sentence: “When we were younger, we use to visit my grandparents every weekend.”", o:["When we were younger, we used to visit my grandparents every weekend.","When we were younger, we are used to visit my grandparents every weekend.","When we were younger, we use visiting my grandparents every weekend."], a:0, e:"The past-habit expression is “used to + base verb.”"},
{ s:"Reading · Online shopping", q:"Online shopping first ___ available in the mid-1990s after the World Wide Web was created.", o:["became","turned","grew","started"], a:0, e:"The natural phrase is “became available.”"},
{ s:"Reading · Online shopping", q:"Many people first began shopping on the internet to ___ less expensive items.", o:["purchase","spend","save","give"], a:0, e:"“Purchase” means buy."},
{ s:"Reading · Online shopping", q:"Online shopping gave people the chance to shop without leaving home. It ___ people the chance to shop from home.", o:["provided","presented","created","turned"], a:0, e:"“Provided people the chance” is the intended collocation."},
{ s:"Reading · Online shopping", q:"Goods arrived quickly and people could ___ items back if there was a problem.", o:["send","change","return","put"], a:2, e:"You can return items to a shop if there is a problem."},
{ s:"Reading · Online shopping", q:"They received ___ of their money quickly, and exchange security also improved.", o:["refunds","prices","promotions","changes"], a:0, e:"A refund is money returned to a customer."},
{ s:"Reading · Online shopping", q:"Soon, everyone was ___ to go shopping on the internet.", o:["doing","going","having","making"], a:1, e:"The phrase is “go shopping.”"},
{ s:"Reading · Competition", q:"“There can only be one answer to this question: yes! Of course, it feels great when you ___ scoring goals or your team wins the match.”", o:["enjoy","avoid","consider","mind"], a:0, e:"“Enjoy” fits the positive experience described."},
{ s:"Reading · Competition", q:"“But you don’t have to be good ___ sport to benefit from it.”", o:["at","in","on","for"], a:0, e:"The correct expression is “good at sport.”"},
{ s:"Reading · Competition", q:"“Competing against others teaches you ___ lot of things about yourself and other people.”", o:["a","an","the","many"], a:0, e:"The expression is “a lot of things.”"},
{ s:"Reading · Competition", q:"“It makes you try harder and become more sociable. It teaches you to win and lose well and no longer be afraid ___ trying new things.”", o:["of","to","at","for"], a:0, e:"The expression is “afraid of doing something.”"},
{ s:"Reading · Competition", q:"“When you work hard to achieve your aims, you feel more confident, whether you are successful ___ not.”", o:["or","and","but","so"], a:0, e:"The fixed phrase is “whether ... or not.”"},
{ s:"Reading · Competition", q:"“Any negative feelings you have ___ disappear.”", o:["will","would have","are","did"], a:0, e:"“Will disappear” expresses the result the writer predicts."}
];
let index=0, score=0, locked=false, missed=[];
const $=id=>document.getElementById(id);
function start(){index=0;score=0;missed=[];$("welcome").classList.add("hidden");$("results").classList.add("hidden");$("game").classList.remove("hidden");render()}
function render(){locked=false;let item=questions[index];$("section").textContent=item.s;$("count").textContent=`Question ${index+1} of ${questions.length}`;$("bar").style.width=`${index/questions.length*100}%`;$("question").textContent=item.q;$("answers").innerHTML="";$("feedback").textContent="";$("next").disabled=true;$("next").textContent=index===questions.length-1?"See results →":"Next question →";item.o.forEach((opt,i)=>{let b=document.createElement("button");b.className="option";b.innerHTML=`<span class="letter">${String.fromCharCode(65+i)}</span>${opt}`;b.onclick=()=>answer(i);$("answers").appendChild(b)});$("score").textContent=`⭐ Score: ${score}`}
function answer(choice){if(locked)return;locked=true;let item=questions[index],buttons=[...$("answers").children];buttons.forEach((b,i)=>{b.disabled=true;if(i===item.a)b.classList.add("correct");if(i===choice&&i!==item.a)b.classList.add("wrong")});if(choice===item.a){score++;$("feedback").textContent="✅ Correct! "+item.e;$("feedback").style.color="#087d59"}else{missed.push({q:item.q,correct:item.o[item.a]});$("feedback").textContent="❌ Not quite. "+item.e;$("feedback").style.color="#b12b43"}$("score").textContent=`⭐ Score: ${score}`;$("bar").style.width=`${(index+1)/questions.length*100}%`;$("next").disabled=false}
function results(){ $("game").classList.add("hidden");$("results").classList.remove("hidden");let pct=Math.round(score/questions.length*100);$("final").textContent=`You scored ${score} out of ${questions.length} (${pct}%).`; $("emoji").textContent=pct>=90?"🏆":pct>=70?"🎉":pct>=50?"💪":"📚";$("message").textContent=pct>=90?"Outstanding! You’re a Review 1 champion.":pct>=70?"Great work! Review the tricky questions and aim even higher.":"Keep practising—you can improve with every round.";let review=$("review");review.innerHTML="<h3>🔍 Questions to review</h3>";if(!missed.length)review.innerHTML+="<p>Perfect round! You answered every question correctly.</p>";else{missed.forEach(m=>{let p=document.createElement("p");p.textContent="• "+m.q+" — Answer: "+m.correct;review.appendChild(p)})}}
$("start").onclick=start;$("next").onclick=()=>{if(!locked)return;index++;if(index<questions.length)render();else results()};$("again").onclick=start;
</script></body></html>
