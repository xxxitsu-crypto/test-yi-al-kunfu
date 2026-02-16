<!doctype html>
<html lang="ja">
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Pixel Fighter (no image)</title>
<style>
  html,body{margin:0;height:100%;background:#111}
  canvas{width:100%;height:100%;display:block;image-rendering:pixelated}
</style>
<canvas id="c"></canvas>
<script>
const canvas = document.getElementById("c");
const ctx = canvas.getContext("2d");

function resize(){
  const dpr = Math.max(1, Math.min(2, devicePixelRatio||1));
  canvas.width = Math.floor(innerWidth*dpr);
  canvas.height = Math.floor(innerHeight*dpr);
}
addEventListener("resize", resize); resize();

// ---- パレット（必要最低限） ----
const P = {
  _: null,         // 透明
  k: "#111111",    // 黒（アウトライン）
  s: "#d8c0b6",    // 肌
  b: "#2d1a12",    // 棒
  p: "#4b22ff",    // ズボン（P1）
  w: "#eaeaea",    // 靴
};

// ---- ドット絵データ（文字の2次元配列）----
// ここが「画像をデータ化」している部分です。
// 仕組みとして動く最小例（あなたの画像に合わせて後でドットを詰めればOK）
const SPR = [
  "__________b__________",
  "__________b__________",
  "__________b__________",
  "__________b__________",
  "_________ksk_________",
  "________ksssk________",
  "_______kssssk________",
  "_____kkssssssk_______",
  "____ksssssssssk______",
  "__kksssssssssskk_____",
  "_kssssssskssssssk____",
  "kssssssssssssssssk___",
  "kssssssssssssssssk___",
  "_kssssssssssssssk____",
  "__ksssssssssssskk_____",
  "___kkppppppppkk_______",
  "____kppppppppk________",
  "___kppppppppppk_______",
  "__kppppppppppppk______",
  "__kppppppppppppk______",
  "___kpppp__ppppk_______",
  "____kpp____ppk________",
  "__www________www______",
  "_wwww________wwww_____",
];

// ---- 描画関数：ドットをfillRectで描く ----
function drawSprite(x, y, scale, palette, flip=false){
  const h = SPR.length;
  const w = SPR[0].length;
  for(let j=0;j<h;j++){
    const row = SPR[j];
    for(let i=0;i<w;i++){
      const ch = row[i];
      const col = palette[ch];
      if(!col) continue;
      const px = flip ? (w-1-i) : i;
      ctx.fillStyle = col;
      ctx.fillRect(x + px*scale, y + j*scale, scale, scale);
    }
  }
}

// ---- 色違い：ズボンだけ変える（p を差し替え）----
function makePalette(pantsColor){
  return { ...P, p: pantsColor };
}

let t = 0;
// ---- 2体表示＋ちょい動き（確認用）----
function loop(){
  t += 0.016;
  ctx.setTransform(1,0,0,1,0,0);
  ctx.clearRect(0,0,canvas.width,canvas.height);

  // 仮想座標（大きさ安定させる）
  const scale = Math.min(canvas.width/960, canvas.height/540);
  ctx.setTransform(scale,0,0,scale, 0, 0);

  // 背景
  ctx.fillStyle = "#181818";
  ctx.fillRect(0,0,960,540);
  ctx.fillStyle = "#0f0f0f";
  ctx.fillRect(0,430,960,110);

  // キャラ位置
  const y = 260 + Math.sin(t)*2; // ちょい上下（動作確認用）
  drawSprite(220, y, 6, makePalette("#4b22ff"), false); // P1
  drawSprite(620, y, 6, makePalette("#ff3b3b"), true);  // P2（色違い＋左右反転）

  requestAnimationFrame(loop);
}
loop();
</script>
</html>
