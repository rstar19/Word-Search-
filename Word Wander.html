<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="apple-mobile-web-app-capable" content="yes">
<title>Word Wander</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Atkinson+Hyperlegible:wght@400;700&family=Fredoka:wght@500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#E6F2F5; --card:#FFFFFF; --ink:#14264A; --muted:#46597B; --line:#C5D6E0;
  --primary:#1E5BC6; --primary-ink:#FFFFFF; --accent:#FFC83D;
  --sel-ink:#14264A; --found-ink:#14264A; --shadow:0 8px 28px rgba(20,38,74,.14);
  --overlay:rgba(12,24,48,.55);
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px);
  padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#0E1A33; --card:#182849; --ink:#F2F6FF; --muted:#AEBDDA; --line:#2C4170;
    --primary:#6AA6FF; --primary-ink:#0B1630; --accent:#FFC83D;
    --sel-ink:#14264A; --found-ink:#14264A; --shadow:0 8px 28px rgba(0,0,0,.4);
    --overlay:rgba(0,0,0,.65);
  }
}
:root[data-theme="dark"]{
  --bg:#0E1A33; --card:#182849; --ink:#F2F6FF; --muted:#AEBDDA; --line:#2C4170;
  --primary:#6AA6FF; --primary-ink:#0B1630; --accent:#FFC83D;
  --sel-ink:#14264A; --found-ink:#14264A; --shadow:0 8px 28px rgba(0,0,0,.4);
  --overlay:rgba(0,0,0,.65);
}
html{font-size:18px;scroll-padding-top:env(safe-area-inset-top,0px);-webkit-text-size-adjust:100%}
html[data-size="large"]{font-size:21px}
html[data-size="xl"]{font-size:24px}
*{box-sizing:border-box}
body{
  margin:0;background:var(--bg);color:var(--ink);
  font-family:'Atkinson Hyperlegible',system-ui,-apple-system,'Segoe UI',Arial,sans-serif;
  line-height:1.4;-webkit-tap-highlight-color:transparent;
}
.app{max-width:1100px;margin:0 auto;padding:12px max(14px,env(safe-area-inset-left)) 28px max(14px,env(safe-area-inset-right))}
header{display:flex;flex-wrap:wrap;align-items:center;gap:10px 14px;justify-content:space-between;margin-bottom:6px}
h1{font-family:'Fredoka','Trebuchet MS',system-ui,sans-serif;font-weight:600;font-size:1.7rem;margin:0;letter-spacing:.01em}
.stats{display:flex;gap:8px;align-items:center;flex-wrap:wrap}
.pill{background:var(--card);border:2px solid var(--line);border-radius:999px;padding:.25rem .85rem;font-weight:700;font-size:1rem;white-space:nowrap}
.pill b{color:var(--ink)}
.star{color:#E8A400}
.msg{margin:6px 0 12px;font-size:1.05rem;min-height:2.9em;color:var(--ink)}
.layout{display:block}
.boardWrap{display:flex;justify-content:center}
.board{
  --board:min(calc(100vw - 28px),680px);
  width:var(--board);aspect-ratio:1;padding:10px;background:var(--card);
  border-radius:24px;box-shadow:var(--shadow);border:3px solid var(--ink);
}
.inner{position:relative;width:100%;height:100%}
#overlay{position:absolute;inset:0;width:100%;height:100%;pointer-events:none;z-index:0}
.grid{
  position:absolute;inset:0;display:grid;z-index:1;touch-action:none;
  -webkit-user-select:none;user-select:none;-webkit-touch-callout:none;cursor:pointer;
}
.cell{
  display:grid;place-items:center;border-radius:50%;
  font-family:'Atkinson Hyperlegible',system-ui,sans-serif;font-weight:700;text-transform:uppercase;
  font-size:calc((var(--board) - 26px) / var(--n) * .56);line-height:1;color:var(--ink);
  pointer-events:none;
}
.cell.f{color:var(--found-ink)}
.cell.on{color:var(--sel-ink)}
.cell.hint{background:var(--accent);color:#14264A;box-shadow:0 0 0 3px var(--ink),0 0 16px 4px var(--accent);animation:pulse 1.1s ease-in-out infinite}
@keyframes pulse{50%{transform:scale(1.12)}}
.cell.shake{animation:none}
.board.shake{animation:shake .35s}
@keyframes shake{20%{transform:translateX(-6px)}40%{transform:translateX(6px)}60%{transform:translateX(-4px)}80%{transform:translateX(4px)}}
.side{margin-top:16px}
.progress{margin-bottom:12px}
.count{font-weight:700;font-size:1.05rem;margin-bottom:6px}
.bar{height:14px;border-radius:99px;background:var(--line);overflow:hidden}
.bar i{display:block;height:100%;width:0;background:var(--primary);border-radius:99px;transition:width .35s ease}
.actions{display:flex;gap:10px;flex-wrap:wrap}
.btn{
  min-height:3.1rem;padding:0 1.25rem;border-radius:16px;border:2px solid var(--ink);background:var(--card);color:var(--ink);
  font:700 1.05rem/1 'Atkinson Hyperlegible',system-ui,sans-serif;cursor:pointer;touch-action:manipulation;
  display:inline-flex;align-items:center;justify-content:center;gap:.5rem;flex:1 1 auto;
}
.btn.primary{background:var(--primary);border-color:var(--primary);color:var(--primary-ink)}
.btn:active{transform:translateY(1px)}
.btn:focus-visible,.segbtn:focus-visible{outline:4px solid var(--accent);outline-offset:2px;box-shadow:0 0 0 2px var(--ink)}
.btn.ghost{flex:0 0 auto;min-height:2.6rem;padding:0 1rem}
.words{list-style:none;display:flex;flex-wrap:wrap;gap:8px;padding:0;margin:14px 0 0}
.chip{
  padding:.4rem .85rem;border-radius:999px;background:var(--card);border:2px solid var(--line);
  font-weight:700;letter-spacing:.07em;font-size:1.05rem;text-transform:uppercase;
}
.chip.done{background:var(--c);border-color:transparent;color:var(--found-ink);text-decoration:line-through;text-decoration-thickness:2px}
.chip.hl{border-color:var(--ink);box-shadow:0 0 0 3px var(--accent)}
.modal{position:fixed;inset:0;z-index:50;background:var(--overlay);display:flex;align-items:center;justify-content:center;padding:max(16px,env(safe-area-inset-top)) 16px max(16px,env(safe-area-inset-bottom))}
.modal[hidden]{display:none}
.sheet{background:var(--card);border-radius:26px;border:3px solid var(--ink);box-shadow:var(--shadow);padding:22px 20px;width:100%;max-width:460px;max-height:100%;overflow:auto;text-align:center}
.sheet h2{font-family:'Fredoka','Trebuchet MS',system-ui,sans-serif;font-weight:600;font-size:1.6rem;margin:0 0 8px}
.sheet p{margin:8px 0 16px}
.bigstars{font-size:2.8rem;letter-spacing:.15em;color:#E8A400;line-height:1.1;margin:6px 0}
.bigstars .off{color:var(--line)}
.row{text-align:left;margin:14px 0}
.rowlabel{font-weight:700;margin-bottom:6px}
.small{font-size:.85rem;color:var(--muted);margin:6px 0 0}
.seg{display:flex;gap:6px;flex-wrap:wrap}
.segbtn{
  flex:1 1 auto;min-height:2.8rem;padding:0 .9rem;border-radius:14px;border:2px solid var(--line);background:var(--bg);color:var(--ink);
  font:700 1rem/1 'Atkinson Hyperlegible',system-ui,sans-serif;cursor:pointer;touch-action:manipulation
}
.segbtn[aria-pressed="true"]{background:var(--primary);color:var(--primary-ink);border-color:var(--primary)}
.sheet .btn{width:100%;margin-top:10px}
#confetti{position:fixed;inset:0;width:100%;height:100%;pointer-events:none;z-index:60}
@media (min-width:920px){
  .layout{display:grid;grid-template-columns:auto minmax(300px,1fr);gap:32px;align-items:start}
  .board{--board:min(56vw,calc(100svh - 190px),720px)}
  .side{margin-top:0}
}
@media (prefers-reduced-motion: reduce){
  .cell.hint{animation:none}
  .board.shake{animation:none}
  .bar i{transition:none}
}
</style>
</head>
<body>
<div class="app">
  <header>
    <h1>Word Wander</h1>
    <div class="stats">
      <span class="pill" id="levelPill">Level 1</span>
      <span class="pill"><span class="star" aria-hidden="true">★</span> <b id="starCount">0</b> <span class="sr">stars</span></span>
      <button class="btn ghost" id="settingsBtn" type="button">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.7 1.7 0 0 0 .3 1.8l.1.1a2 2 0 1 1-2.8 2.8l-.1-.1a1.7 1.7 0 0 0-1.8-.3 1.7 1.7 0 0 0-1 1.5V21a2 2 0 1 1-4 0v-.1a1.7 1.7 0 0 0-1.1-1.5 1.7 1.7 0 0 0-1.8.3l-.1.1a2 2 0 1 1-2.8-2.8l.1-.1a1.7 1.7 0 0 0 .3-1.8 1.7 1.7 0 0 0-1.5-1H3a2 2 0 1 1 0-4h.1a1.7 1.7 0 0 0 1.5-1.1 1.7 1.7 0 0 0-.3-1.8l-.1-.1a2 2 0 1 1 2.8-2.8l.1.1a1.7 1.7 0 0 0 1.8.3H9a1.7 1.7 0 0 0 1-1.5V3a2 2 0 1 1 4 0v.1a1.7 1.7 0 0 0 1 1.5 1.7 1.7 0 0 0 1.8-.3l.1-.1a2 2 0 1 1 2.8 2.8l-.1.1a1.7 1.7 0 0 0-.3 1.8V9a1.7 1.7 0 0 0 1.5 1H21a2 2 0 1 1 0 4h-.1a1.7 1.7 0 0 0-1.5 1z"/></svg>
        Settings
      </button>
    </div>
  </header>
  <p class="msg" id="msg" aria-live="polite"></p>
  <main class="layout">
    <section class="boardWrap">
      <div class="board" id="board">
        <div class="inner">
          <svg id="overlay" aria-hidden="true"></svg>
          <div class="grid" id="grid" role="group" aria-label="Word search letters"></div>
        </div>
      </div>
    </section>
    <section class="side">
      <div class="progress">
        <div class="count" id="count">0 of 0 found</div>
        <div class="bar"><i id="barFill"></i></div>
      </div>
      <div class="actions">
        <button class="btn primary" id="hintBtn" type="button">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M9 18h6M10 21h4M12 3a6 6 0 0 0-3.5 10.9c.6.5 1 1.2 1 2.1h5c0-.9.4-1.6 1-2.1A6 6 0 0 0 12 3z"/></svg>
          Hint
        </button>
        <button class="btn" id="newBtn" type="button">
          <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M21 12a9 9 0 1 1-3-6.7L21 8"/><path d="M21 3v5h-5"/></svg>
          New words
        </button>
      </div>
      <ul class="words" id="words" aria-label="Words to find"></ul>
    </section>
  </main>
</div>

<div class="modal" id="modal" hidden>
  <div class="sheet" id="sheet" role="dialog" aria-modal="true" aria-live="polite"></div>
</div>
<canvas id="confetti" aria-hidden="true"></canvas>

<style>.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap}</style>

<script>
(function(){
'use strict';

/* ---------- Word bank ---------- */
var RAW = "\
cat dog bird fish frog duck goose horse sheep goat cow pig hen rooster rabbit mouse squirrel deer bear wolf fox lion tiger zebra giraffe monkey panda koala kangaroo camel donkey pony turkey eagle hawk owl robin sparrow swan crane parrot penguin dolphin whale shark seal otter turtle snail spider ant bee butterfly ladybug beetle cricket firefly worm crab lobster shrimp octopus walrus moose bison llama alpaca badger raccoon hedgehog chipmunk gecko lizard salmon trout puppy kitten chicken pigeon peacock flamingo pelican ostrich cheetah leopard gorilla elephant hippo rhino bat bull calf lamb mule ox stork finch wren dove magpie falcon heron toucan iguana newt toad minnow tadpole sloth lemur ferret hamster gerbil canary budgie mongoose antelope buffalo porcupine platypus jellyfish starfish seahorse oyster clam mussel \
apple banana cherry grape lemon lime orange peach pear plum melon mango berry strawberry blueberry raspberry pineapple coconut apricot cranberry grapefruit tangerine papaya guava kiwi fig date prune raisin bread toast bagel muffin cookie cake pie donut pancake waffle butter cheese cream yogurt milk egg bacon sausage ham steak soup salad pasta noodle rice bean pea corn carrot celery onion garlic potato tomato pepper cucumber lettuce spinach cabbage broccoli radish pumpkin squash olive pickle honey sugar syrup jelly jam peanut almond walnut pecan cashew popcorn pretzel cracker candy chocolate vanilla cinnamon ginger mint sandwich pizza burger taco burrito tea coffee juice lemonade cocoa biscuit cupcake brownie pudding custard fudge caramel toffee oatmeal cereal granola omelet butterscotch meatball dumpling pastry scone crumpet tart cobbler sherbet sundae smoothie cider soda broth stew chili curry gravy sauce mustard ketchup relish salsa pepper parsley basil thyme sage oregano nutmeg clove \
tree leaf branch root flower rose tulip daisy lily violet orchid sunflower lavender clover fern moss grass shrub meadow forest woods jungle desert valley canyon mountain hill cliff cave island beach shore sand ocean sea lake river creek stream pond waterfall spring marsh swamp harbor bay coast reef rock stone pebble boulder crystal diamond ruby emerald pearl amber gold silver copper iron petal blossom bud stem seed acorn pinecone maple oak pine birch willow cedar elm palm bamboo ivy vine thorn bloom garden orchard prairie plain plateau glacier volcano lagoon delta oasis dune cove peak ridge summit trail brook \
sun moon star comet planet galaxy cloud rain snow sleet hail storm thunder lightning wind breeze gale fog mist frost ice rainbow sunrise sunset dawn dusk twilight midnight morning evening night autumn winter summer season weather climate drizzle shower puddle flood drought tornado hurricane blizzard snowflake icicle raindrop sunshine moonlight starlight skyline horizon breezy sunny cloudy windy foggy stormy rocket astronaut orbit lunar solar meteor asteroid satellite telescope universe eclipse \
house home cabin cottage castle tower barn shed garage porch deck roof wall floor door window stairs hallway kitchen bedroom bathroom attic basement fence gate chimney fireplace table chair sofa couch bench stool desk shelf drawer closet cabinet lamp candle clock mirror picture frame carpet rug curtain pillow blanket quilt sheet towel bucket broom mop basket bottle jar cup mug plate bowl spoon fork knife kettle teapot pan pot oven stove toaster fridge sink faucet shower bathtub doorbell mailbox doormat balcony patio yard lawn hedge trellis windmill lantern vase teacup saucer tray napkin tablecloth cushion hammock rocker recliner bookcase \
hat cap scarf glove mitten coat jacket sweater shirt blouse dress skirt pants jeans shorts sock shoe boot sandal slipper apron belt button zipper pocket collar sleeve pajamas ribbon bonnet bowtie necktie vest cardigan overalls raincoat umbrella purse wallet handbag backpack buckle lace thread needle thimble scissors tape glue yarn cotton wool silk velvet denim linen \
car bus train plane jet boat ship canoe kayak sailboat ferry taxi truck bike bicycle scooter tractor wagon trolley subway airport station road street avenue bridge tunnel highway path map compass ticket passport suitcase luggage tent journey voyage adventure vacation holiday hotel resort cruise sailor harbor dock pier lighthouse anchor paddle oar sail engine wheel pedal horn brake gas parking traffic signal corner crossing roundabout detour \
baker farmer doctor nurse teacher pilot captain driver carpenter plumber painter artist singer dancer writer author poet actor chef cook waiter banker lawyer judge mayor police fireman builder tailor barber florist gardener mechanic engineer scientist dentist pharmacist librarian musician clerk cashier grocer butcher miller weaver potter sculptor cobbler blacksmith shepherd rancher fisherman sailor inventor explorer pioneer \
knit sew quilt paint draw sketch craft bake read write sing dance chess cards puzzle bingo checkers dominoes crossword poetry theater movie picnic bowling golf tennis soccer baseball hockey swim ski skate surf kite jogging yoga walking music guitar piano violin drum flute harp trumpet banjo organ cello clarinet trombone ukulele accordion harmonica tambourine xylophone saxophone orchestra concert melody rhythm chorus choir tune lullaby carol anthem ballad opera waltz polka jazz band parade festival carnival circus fair \
happy joyful merry cheerful gentle kind warm cozy calm quiet peaceful brave clever wise funny silly lucky proud sweet bright shiny sparkle glow golden gleaming friendly lively playful humble honest loyal patient curious eager grateful hopeful radiant splendid wonderful marvelous delightful fantastic cheery sunny jolly jovial lovely pretty handsome graceful elegant charming smiling laughing dazzling brilliant magical mighty noble gallant generous thoughtful caring tender soothing relaxing refreshing delicious \
mother father mom dad sister brother aunt uncle cousin nephew niece grandma grandpa granny family parent child baby toddler friend neighbor buddy pal twin teen youth elder grandson granddaughter relative guest host partner team crew club group \
book story page paper pencil pen crayon marker eraser ruler notebook letter word poem song tale myth riddle joke game toy doll block drum whistle balloon bubble marble jigsaw teddy robot rattle sticker poster card gift present bow wrapping cookie candle cake birthday wedding party dinner lunch breakfast supper snack dessert feast banquet picnic barbecue \
run walk jump skip hop climb swim fly sail ride drive laugh smile giggle cheer play bloom grow plant shine twinkle wander explore discover imagine create build gather collect harvest travel hike stroll wave hug share thank greet visit invite welcome celebrate enjoy relax rest nap dream wish hope wonder listen whisper shout sing hum chat talk tell ask answer learn teach study think remember \
red blue green yellow orange purple pink brown black white gray teal navy tan ivory scarlet crimson indigo turquoise maroon lilac coral peach beige lavender magenta violet amber bronze golden silver \
day week month year hour minute second today tomorrow yesterday weekend noon dawn season january february march april june july august september october november december monday tuesday wednesday thursday friday saturday sunday \
city town village farm market store shop bakery library museum school church park zoo theater cinema stadium gallery cafe diner bank office factory harbor ranch vineyard mill dairy nursery playground fountain plaza square statue monument castle palace temple chapel cottage cabin lodge inn tavern station depot \
hammer nail screw saw drill wrench pliers ladder shovel rake spade hose bucket sander chisel level plank board beam brick cement paint brush roller lumber toolbox workbench \
north south east west left right up down above below inside outside near far over under around across between beyond \
heart mind smile hand finger thumb knee elbow shoulder ankle wrist chin cheek eyebrow eyelash forehead nose mouth ear eye hair beard tooth tongue \
puzzle riddle secret treasure mystery clue map quest legend fable fairy dragon wizard giant knight king queen prince princess castle crown jewel sword shield armor unicorn mermaid elf gnome pirate ghost \
water fire earth air energy light shadow sound echo magnet battery bulb switch wire circuit radio phone camera video photo screen keyboard computer laptop tablet printer email message letter stamp envelope postcard package parcel \
hobby sport soccer rugby cricket archery fencing rowing sailing diving fishing hunting camping gardening cooking baking sewing knitting painting drawing reading writing dancing singing racing running cycling hiking swimming skating skiing bowling golfing curling marathon trophy medal ribbon prize champion winner coach referee score goal \
";

var BANK = (function(){
  var seen = {}, out = [];
  RAW.split(/\s+/).forEach(function(w){
    w = w.toLowerCase();
    if(/^[a-z]{3,10}$/.test(w) && !seen[w]){ seen[w]=1; out.push(w); }
  });
  return out;
})();

/* ---------- Constants ---------- */
var DIRS = {R:[0,1],D:[1,0],DR:[1,1],UR:[-1,1],L:[0,-1],U:[-1,0],DL:[1,-1],UL:[-1,-1]};
var BACK = {L:1,U:1,DL:1,UL:1};
var STEPS = [{lvl:1,d:['R','D']},{lvl:3,d:['DR']},{lvl:5,d:['UR']},{lvl:7,d:['L','U']},{lvl:10,d:['DL','UL']}];
var COLORS = ['#FFB59E','#8EDAD0','#FFE08A','#C3B1F0','#A8E0A2','#9CCBFF','#FFA9C6','#E8C79A'];
var PRAISE = ['Nice find!','Well spotted!','You got it!','Sharp eyes!','Wonderful!','Lovely work!','That\u2019s one!','Great job!'];
var FILLER = 'aaaabbcccddddeeeeeeffgghhiiiijkllllmmnnnnooooppqrrrrssssttttuuvvwwxyyz';

/* ---------- Storage ---------- */
var store = {
  get:function(k,d){ try{ var v=localStorage.getItem(k); return v==null?d:JSON.parse(v);}catch(e){return d;} },
  set:function(k,v){ try{ localStorage.setItem(k,JSON.stringify(v)); }catch(e){} }
};
var S = {
  level: store.get('ww_level',1), stars: store.get('ww_stars',0),
  sound: store.get('ww_sound',true), size: store.get('ww_size','normal'),
  easy: store.get('ww_easy',false), seen: store.get('ww_seen',false)
};
function save(){
  store.set('ww_level',S.level); store.set('ww_stars',S.stars); store.set('ww_sound',S.sound);
  store.set('ww_size',S.size); store.set('ww_easy',S.easy); store.set('ww_seen',S.seen);
}

/* ---------- Elements ---------- */
var $ = function(id){ return document.getElementById(id); };
var elBoard=$('board'), elGrid=$('grid'), elSvg=$('overlay'), elMsg=$('msg'), elWords=$('words');
var elCount=$('count'), elBar=$('barFill'), elLevel=$('levelPill'), elStars=$('starCount');
var elModal=$('modal'), elSheet=$('sheet');

/* ---------- Game state ---------- */
var N=6, G=null, cells=[], found=new Map(), hints=0, sel=null, tapStart=null, hintWord=null, locked=false;
var down=null, dragging=false, curEnd=null, lastFocus=null;

/* ---------- Helpers ---------- */
function shuffle(a){ for(var i=a.length-1;i>0;i--){ var j=Math.floor(Math.random()*(i+1)); var t=a[i]; a[i]=a[j]; a[j]=t; } return a; }
function rev(s){ return s.split('').reverse().join(''); }
function conflicts(a,b){ var r=rev(a); return a.indexOf(b)>-1||b.indexOf(a)>-1||b.indexOf(r)>-1||r.indexOf(b)>-1; }
function pick(a){ return a[Math.floor(Math.random()*a.length)]; }

function sizeFor(level){
  var narrow = Math.min(window.innerWidth, window.innerHeight) < 600;
  return Math.min(6 + Math.floor((level-1)/2), narrow?10:12);
}
function params(level){
  var size=sizeFor(level), dirs=[];
  STEPS.forEach(function(s){ if(level>=s.lvl) dirs=dirs.concat(s.d); });
  if(S.easy) dirs=dirs.filter(function(d){ return !BACK[d]; });
  var maxCount=Math.floor(size*size/6.5);
  var count=Math.max(3,Math.min(4+Math.floor((level-1)*0.75),maxCount,22));
  var minLen=3+(level>=6?1:0)+(level>=14?1:0);
  var maxLen=Math.max(minLen+1,Math.min(size,4+Math.floor(level/3)));
  var trick=Math.min(0.08+level*0.04,0.65);
  return {size:size,dirs:dirs,count:count,minLen:minLen,maxLen:maxLen,trick:trick};
}

/* ---------- Puzzle generation ---------- */
function tryPlace(grid,w,dirs,n){
  for(var t=0;t<80;t++){
    var d=DIRS[pick(dirs)], dr=d[0], dc=d[1], len=w.length;
    var rMin=dr<0?len-1:0, rMax=dr>0?n-len:n-1;
    var cMin=dc<0?len-1:0, cMax=dc>0?n-len:n-1;
    if(rMax<rMin||cMax<cMin) continue;
    var r=rMin+Math.floor(Math.random()*(rMax-rMin+1));
    var c=cMin+Math.floor(Math.random()*(cMax-cMin+1));
    var ok=true;
    for(var i=0;i<len;i++){
      var ch=grid[r+dr*i][c+dc*i];
      if(ch && ch!==w[i]){ ok=false; break; }
    }
    if(!ok) continue;
    for(var k=0;k<len;k++) grid[r+dr*k][c+dc*k]=w[k];
    return {r:r,c:c,dr:dr,dc:dc};
  }
  return null;
}
function generate(level){
  var p=params(level), n=p.size, best=null;
  for(var attempt=0;attempt<40;attempt++){
    var grid=[]; for(var i=0;i<n;i++){ grid.push(new Array(n).fill('')); }
    var pool=shuffle(BANK.filter(function(w){ return w.length>=p.minLen && w.length<=p.maxLen; }));
    var placed=[];
    for(var j=0;j<pool.length && placed.length<p.count;j++){
      var w=pool[j];
      if(placed.some(function(x){ return conflicts(x.word,w); })) continue;
      var pos=tryPlace(grid,w,p.dirs,n);
      if(pos) placed.push({word:w,r:pos.r,c:pos.c,dr:pos.dr,dc:pos.dc});
    }
    if(!best || placed.length>best.placed.length) best={grid:grid,placed:placed};
    if(placed.length>=p.count) break;
  }
  var used=''; best.placed.forEach(function(x){ used+=x.word; });
  for(var r=0;r<n;r++) for(var c=0;c<n;c++){
    if(!best.grid[r][c]){
      best.grid[r][c] = (Math.random()<p.trick && used) ? used[Math.floor(Math.random()*used.length)] : FILLER[Math.floor(Math.random()*FILLER.length)];
    }
  }
  return {N:n,grid:best.grid,placed:best.placed};
}

/* ---------- Rendering ---------- */
function build(){
  elGrid.innerHTML=''; cells=[];
  elGrid.style.gridTemplateColumns='repeat('+N+',1fr)';
  elGrid.style.gridTemplateRows='repeat('+N+',1fr)';
  elBoard.style.setProperty('--n',N);
  elSvg.setAttribute('viewBox','0 0 '+N+' '+N);
  for(var r=0;r<N;r++) for(var c=0;c<N;c++){
    var d=document.createElement('div');
    d.className='cell'; d.textContent=G.grid[r][c]; d.setAttribute('aria-hidden','true');
    elGrid.appendChild(d); cells.push(d);
  }
}
function renderWords(){
  elWords.innerHTML='';
  G.placed.slice().sort(function(a,b){ return a.word<b.word?-1:1; }).forEach(function(p){
    var li=document.createElement('li'); li.className='chip'; li.textContent=p.word; li.dataset.word=p.word;
    elWords.appendChild(li);
  });
}
function updateChips(){
  Array.prototype.forEach.call(elWords.children,function(li){
    var f=found.get(li.dataset.word);
    li.classList.toggle('done',!!f);
    if(f) li.style.setProperty('--c',f.color);
    li.classList.toggle('hl',hintWord===li.dataset.word && !f);
  });
}
function updateProgress(){
  var total=G.placed.length, n=found.size;
  elCount.textContent=n+' of '+total+' found';
  elBar.style.width=(total?100*n/total:0)+'%';
}
function updatePills(){
  elLevel.textContent='Level '+S.level;
  elStars.textContent=S.stars;
}
function lineCells(a,b){
  var dr=b.r-a.r, dc=b.c-a.c, steps=Math.max(Math.abs(dr),Math.abs(dc));
  var sr=Math.sign(dr), sc=Math.sign(dc), out=[];
  for(var i=0;i<=steps;i++) out.push([a.r+sr*i,a.c+sc*i]);
  return out;
}
function capsule(a,b,color,op){
  var x1=a.c+.5,y1=a.r+.5,x2=b.c+.5,y2=b.r+.5;
  if(x1===x2&&y1===y2) return '<circle cx="'+x1+'" cy="'+y1+'" r=".43" fill="'+color+'" opacity="'+op+'"/>';
  return '<line x1="'+x1+'" y1="'+y1+'" x2="'+x2+'" y2="'+y2+'" stroke="'+color+'" stroke-width=".84" stroke-linecap="round" opacity="'+op+'"/>';
}
function paint(){
  var fc={}, sc={};
  found.forEach(function(f){ f.cells.forEach(function(p){ fc[p[0]*N+p[1]]=1; }); });
  if(sel) sel.cells.forEach(function(p){ sc[p[0]*N+p[1]]=1; });
  cells.forEach(function(el,i){ el.classList.toggle('f',!!fc[i]); el.classList.toggle('on',!!sc[i]); });
  var h='';
  found.forEach(function(f){ h+=capsule(f.a,f.b,f.color,.92); });
  if(sel) h+=capsule(sel.a,sel.b,'#FFC83D',.96);
  elSvg.innerHTML=h;
}
function say(t){ elMsg.textContent=t; }

/* ---------- Level flow ---------- */
function levelNote(level){
  var n=[];
  if(level>1 && sizeFor(level)>sizeFor(level-1)) n.push('The board just got bigger.');
  if(level===3) n.push('New: words can also run diagonally.');
  if(level===5) n.push('New: diagonals can now go upward too.');
  if(level===7 && !S.easy) n.push('New: words can run backwards or upward.');
  if(level===10 && !S.easy) n.push('New: words can run in every direction.');
  return n.join(' ');
}
function startLevel(){
  G=generate(S.level); N=G.N;
  found=new Map(); hints=0; sel=null; tapStart=null; hintWord=null; locked=false; down=null; dragging=false;
  build(); renderWords(); updateProgress(); updatePills(); updateChips(); paint();
  var total=G.placed.length;
  var base='Find the '+total+' words below. Drag across the letters, or tap the first and last letter.';
  var note=levelNote(S.level);
  say(note ? note+' '+base : base);
  elGrid.setAttribute('aria-label','Word search, '+N+' by '+N+' letters');
}

/* ---------- Selection ---------- */
var VECS=[[0,1],[1,1],[1,0],[1,-1],[0,-1],[-1,-1],[-1,0],[-1,1]];
function cellFromPoint(x,y){
  var rect=elGrid.getBoundingClientRect();
  var c=Math.floor((x-rect.left)/rect.width*N), r=Math.floor((y-rect.top)/rect.height*N);
  return {r:Math.max(0,Math.min(N-1,r)), c:Math.max(0,Math.min(N-1,c))};
}
function snapEnd(a,b){
  var dr=b.r-a.r, dc=b.c-a.c;
  if(dr===0&&dc===0) return a;
  var k=((Math.round(Math.atan2(dr,dc)/(Math.PI/4))%8)+8)%8, v=VECS[k];
  var len=Math.max(0,Math.round((dr*v[0]+dc*v[1])/(v[0]*v[0]+v[1]*v[1])));
  while(len>0){
    var rr=a.r+v[0]*len, cc=a.c+v[1]*len;
    if(rr>=0&&rr<N&&cc>=0&&cc<N) break;
    len--;
  }
  return {r:a.r+v[0]*len,c:a.c+v[1]*len};
}
function setSel(a,b){ sel={a:a,b:b,cells:lineCells(a,b)}; paint(); }
function clearSel(){ sel=null; paint(); }

function evaluate(a,b){
  b=snapEnd(a,b);
  var cs=lineCells(a,b);
  if(cs.length<2){ clearSel(); return; }
  var str=cs.map(function(p){ return G.grid[p[0]][p[1]]; }).join('');
  var rs=rev(str), hit=null, already=null;
  G.placed.forEach(function(p){
    if(p.word===str||p.word===rs){ if(found.has(p.word)) already=p.word; else hit=p.word; }
  });
  if(hit){
    var color=COLORS[found.size%COLORS.length];
    found.set(hit,{a:a,b:b,cells:cs,color:color});
    if(hintWord===hit){ hintWord=null; cells.forEach(function(c){ c.classList.remove('hint'); }); }
    sel=null; updateChips(); updateProgress(); paint(); sfx('found');
    var left=G.placed.length-found.size;
    if(left===0){ complete(); }
    else say(pick(PRAISE)+' '+left+(left===1?' word':' words')+' to go.');
  } else if(already){
    clearSel(); say('You already found '+already.toUpperCase()+'. Look for another one.'); sfx('miss');
  } else {
    clearSel(); sfx('miss'); say('Not quite. Try again from the first letter to the last.');
    elBoard.classList.remove('shake'); void elBoard.offsetWidth; elBoard.classList.add('shake');
  }
}
function handleTap(cell){
  sfx('tap');
  if(!tapStart){ tapStart=cell; setSel(cell,cell); say('Good. Now tap the last letter of the word.'); return; }
  if(tapStart.r===cell.r && tapStart.c===cell.c){ tapStart=null; clearSel(); say('Selection cleared. Tap the first letter of a word.'); return; }
  var dr=Math.abs(cell.r-tapStart.r), dc=Math.abs(cell.c-tapStart.c);
  if(dr===0||dc===0||dr===dc){ var s=tapStart; tapStart=null; evaluate(s,cell); }
  else { tapStart=cell; setSel(cell,cell); say('Those two letters are not in a straight line. Starting again from this letter.'); }
}

elGrid.addEventListener('pointerdown',function(e){
  if(locked) return;
  e.preventDefault(); ensureAudio();
  try{ elGrid.setPointerCapture(e.pointerId); }catch(err){}
  down=cellFromPoint(e.clientX,e.clientY); curEnd=down; dragging=false;
});
elGrid.addEventListener('pointermove',function(e){
  if(!down||locked) return;
  var c=cellFromPoint(e.clientX,e.clientY);
  if(!dragging && (c.r!==down.r||c.c!==down.c)){ dragging=true; tapStart=null; }
  if(dragging){ curEnd=snapEnd(down,c); setSel(down,curEnd); }
});
elGrid.addEventListener('pointerup',function(e){
  if(!down) return;
  var d=down, end=curEnd, wasDrag=dragging;
  down=null; dragging=false;
  if(locked) return;
  if(wasDrag) evaluate(d,end); else handleTap(d);
});
elGrid.addEventListener('pointercancel',function(){ down=null; dragging=false; if(!tapStart) clearSel(); });
elGrid.addEventListener('contextmenu',function(e){ e.preventDefault(); });

/* ---------- Hint ---------- */
function hint(){
  if(locked||!G) return;
  var rem=G.placed.filter(function(p){ return !found.has(p.word); });
  if(!rem.length) return;
  var w=pick(rem); hints++; hintWord=w.word;
  cells.forEach(function(c){ c.classList.remove('hint'); });
  cells[w.r*N+w.c].classList.add('hint');
  updateChips(); sfx('hint');
  say('Look for '+w.word.toUpperCase()+'. It starts at the glowing letter.');
}

/* ---------- Completion ---------- */
function complete(){
  locked=true; sfx('win'); confetti();
  var stars=hints===0?3:(hints<=2?2:1);
  S.stars+=stars; var done=S.level; S.level+=1; save(); updatePills();
  say('You found every word!');
  var starHtml='';
  for(var i=0;i<3;i++) starHtml+='<span class="'+(i<stars?'':'off')+'">★</span>';
  var line = hints===0 ? 'No hints needed. Excellent!' : 'You used '+hints+(hints===1?' hint':' hints')+'. Great effort!';
  setTimeout(function(){
    openModal('<h2>Level '+done+' complete!</h2><div class="bigstars" aria-label="'+stars+' of 3 stars">'+starHtml+'</div><p>'+line+'</p>'
      +'<button class="btn primary" type="button" data-act="next">Start level '+S.level+'</button>');
  },900);
}

/* ---------- Modal ---------- */
function openModal(html){
  lastFocus=document.activeElement;
  elSheet.innerHTML=html; elModal.hidden=false;
  var b=elSheet.querySelector('button'); if(b) b.focus({preventScroll:true});
}
function closeModal(){
  elModal.hidden=true; elSheet.innerHTML='';
  if(lastFocus && lastFocus.focus) try{ lastFocus.focus({preventScroll:true}); }catch(e){}
}
function seg(label,name,opts,value,note){
  return '<div class="row"><div class="rowlabel" id="l-'+name+'">'+label+'</div><div class="seg" role="group" aria-labelledby="l-'+name+'">'
    +opts.map(function(o){ return '<button class="segbtn" type="button" data-act="'+name+'" data-v="'+o[0]+'" aria-pressed="'+(String(o[0])===String(value))+'">'+o[1]+'</button>'; }).join('')
    +'</div>'+(note?'<p class="small">'+note+'</p>':'')+'</div>';
}
var resetArmed=false;
function renderSettings(){
  openModalKeepFocus('<h2>Settings</h2>'
    +seg('Sound','sound',[['on','On'],['off','Off']],S.sound?'on':'off')
    +seg('Text size','size',[['normal','Normal'],['large','Large'],['xl','Extra large']],S.size)
    +seg('Easy reading','easy',[['on','On'],['off','Off']],S.easy?'on':'off','When on, words never run backwards. Applies to the next puzzle. Tap New words to use it right away.')
    +'<button class="btn" type="button" data-act="reset">'+(resetArmed?'Tap again to restart at level 1':'Start over at level 1')+'</button>'
    +'<button class="btn primary" type="button" data-act="close">Done</button>');
}
function openModalKeepFocus(html){
  var active=document.activeElement && document.activeElement.getAttribute && document.activeElement.getAttribute('data-act');
  var v=document.activeElement && document.activeElement.getAttribute && document.activeElement.getAttribute('data-v');
  var wasOpen=!elModal.hidden;
  if(!wasOpen){ lastFocus=document.activeElement; }
  elSheet.innerHTML=html; elModal.hidden=false;
  var sel2=active ? (v?'[data-act="'+active+'"][data-v="'+v+'"]':'[data-act="'+active+'"]') : null;
  var b=(wasOpen&&sel2&&elSheet.querySelector(sel2))||elSheet.querySelector('button');
  if(b) b.focus({preventScroll:true});
}
function applySize(){ document.documentElement.setAttribute('data-size',S.size); }

elSheet.addEventListener('click',function(e){
  var t=e.target.closest('[data-act]'); if(!t) return;
  var act=t.getAttribute('data-act'), v=t.getAttribute('data-v');
  ensureAudio();
  if(act==='next'){ closeModal(); startLevel(); }
  else if(act==='play'){ S.seen=true; save(); closeModal(); }
  else if(act==='close'){ resetArmed=false; closeModal(); }
  else if(act==='sound'){ S.sound=(v==='on'); save(); renderSettings(); if(S.sound){ ensureAudio(); sfx('tap'); } }
  else if(act==='size'){ S.size=v; applySize(); save(); renderSettings(); }
  else if(act==='easy'){ S.easy=(v==='on'); save(); renderSettings(); }
  else if(act==='reset'){
    if(!resetArmed){ resetArmed=true; renderSettings(); }
    else { resetArmed=false; S.level=1; S.stars=0; save(); closeModal(); startLevel(); }
  }
});
elModal.addEventListener('click',function(e){ if(e.target===elModal && elSheet.querySelector('[data-act="close"]')){ resetArmed=false; closeModal(); } });
document.addEventListener('keydown',function(e){
  if(e.key==='Escape' && !elModal.hidden && elSheet.querySelector('[data-act="close"]')){ resetArmed=false; closeModal(); }
});

$('settingsBtn').addEventListener('click',function(){ resetArmed=false; renderSettings(); });
$('hintBtn').addEventListener('click',function(){ ensureAudio(); hint(); });
$('newBtn').addEventListener('click',function(){ ensureAudio(); if(!elModal.hidden) return; startLevel(); say('Here are fresh words. '+elMsg.textContent); });

/* ---------- Sound ---------- */
var ac=null;
function ensureAudio(){
  if(!S.sound) return;
  try{
    if(!ac){ var C=window.AudioContext||window.webkitAudioContext; if(C) ac=new C(); }
    if(ac && ac.state==='suspended') ac.resume();
  }catch(e){}
}
function tone(f,t,d,type,v){
  if(!ac) return;
  try{
    var o=ac.createOscillator(), g=ac.createGain(), s=ac.currentTime+t;
    o.type=type||'sine'; o.frequency.value=f;
    g.gain.setValueAtTime(0.0001,s); g.gain.exponentialRampToValueAtTime(v||.12,s+.02); g.gain.exponentialRampToValueAtTime(.0001,s+d);
    o.connect(g); g.connect(ac.destination); o.start(s); o.stop(s+d+.05);
  }catch(e){}
}
function sfx(k){
  if(!S.sound) return; ensureAudio();
  if(k==='found'){ tone(660,0,.18); tone(880,.1,.3); }
  else if(k==='miss'){ tone(220,0,.2,'triangle',.08); }
  else if(k==='hint'){ tone(520,0,.14); tone(520,.2,.14); }
  else if(k==='tap'){ tone(440,0,.06,'sine',.05); }
  else if(k==='win'){ [523,659,784,1047].forEach(function(f,i){ tone(f,i*.12,.4); }); }
}

/* ---------- Confetti ---------- */
function confetti(){
  if(window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches) return;
  var cv=$('confetti'), ctx=cv.getContext('2d'), dpr=window.devicePixelRatio||1;
  var w=window.innerWidth, h=window.innerHeight;
  cv.width=w*dpr; cv.height=h*dpr; ctx.setTransform(dpr,0,0,dpr,0,0);
  var ps=[]; for(var i=0;i<150;i++) ps.push({x:Math.random()*w,y:-20-Math.random()*h*.4,vx:(Math.random()-.5)*4,vy:2+Math.random()*4,s:6+Math.random()*8,r:Math.random()*6,vr:(Math.random()-.5)*.3,c:COLORS[i%COLORS.length]});
  var start=performance.now();
  (function frame(now){
    var t=now-start; ctx.clearRect(0,0,w,h);
    ps.forEach(function(p){ p.x+=p.vx; p.y+=p.vy; p.vy+=.05; p.r+=p.vr; ctx.save(); ctx.translate(p.x,p.y); ctx.rotate(p.r); ctx.fillStyle=p.c; ctx.fillRect(-p.s/2,-p.s/3,p.s,p.s*.6); ctx.restore(); });
    if(t<3200) requestAnimationFrame(frame); else ctx.clearRect(0,0,w,h);
  })(start);
}

/* ---------- Start ---------- */
applySize();
startLevel();
if(!S.seen){
  openModal('<h2>Welcome to Word Wander</h2>'
    +'<p>Words are hiding in the letters. Drag your finger across a word, or tap its first letter and then its last letter.</p>'
    +'<p>There is no timer and no rush. The levels never run out, and they get a little trickier as you go.</p>'
    +'<button class="btn primary" type="button" data-act="play">Let\u2019s play</button>');
}
window.__wwBankSize = BANK.length;
})();
</script>
</body>
</html>
