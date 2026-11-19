<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>地质褶皱与断层虚拟演化模型</title>
<style>
*{box-sizing:border-box;font-family:"Microsoft Yahei",system-ui}
.container{max-width:850px;margin:20px auto;padding:15px}
canvas{border:2px solid #444;background:#fefefe;display:block;margin:10px 0}
.ctrl-panel{background:#f3f6fa;padding:12px;border-radius:8px;margin:10px 0}
.btn{padding:6px 12px;margin:4px;border:none;border-radius:4px;background:#2b78e4;color:#fff;cursor:pointer}
.btn-group{margin:8px 0}
.info{margin-top:10px;color:#333;font-size:14px;line-height:1.6}
</style>
</head>
<body>
<div class="container">
  <h2>地质褶皱与断层动态演化虚拟模型</h2>
  <div class="ctrl-panel">
    <div>
      <label>地层挤压变形量：<input type="range" id="deformSlider" min="0" max="100" value="0"></label>
    </div>
    <div class="btn-group">
      <button class="btn" id="btnReset">🔄 重置地层</button>
      <button class="btn" id="btnReverseFault">逆断层</button>
      <button class="btn" id="btnNormalFault">正断层</button>
      <button class="btn" id="btnNoFault">清除断层</button>
    </div>
    <div class="info">
      💡操作说明：拖动滑块观察地层挤压形成褶皱；点击断层按钮添加对应断层，可对比不同构造形态
    </div>
  </div>
  <canvas id="geoCanvas" width="780" height="360"></canvas>
</div>

<script>
const canvas = document.getElementById('geoCanvas');
const ctx = canvas.getContext('2d');
const deformSlider = document.getElementById('deformSlider');
const btnReset = document.getElementById('btnReset');
const btnReverseFault = document.getElementById('btnReverseFault');
const btnNormalFault = document.getElementById('btnNormalFault');
const btnNoFault = document.getElementById('btnNoFault');

let deformValue = 0;
let faultType = "none"; // none / reverse / normal

// 地层基础参数
const baseYList = [60,110,160,210,260,310];
const layerColor = ['#8c5138','#3b7ea1','#238b45','#d4a046','#bc4b4b','#6c757d'];

function drawModel(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  // 绘制褶皱地层
  baseYList.forEach((baseY,idx)=>{
    ctx.beginPath();
    ctx.strokeStyle = layerColor[idx];
    ctx.lineWidth = 3;
    for(let x=0;x<=canvas.width;x++){
      // 正弦函数模拟挤压褶皱
      const wave = deformValue * Math.sin( (x / 200) * Math.PI );
      const y = baseY + wave;
      if(x===0) ctx.moveTo(x,y);
      else ctx.lineTo(x,y);
    }
    ctx.stroke();
  })

  // 绘制断层面与断层错动示意
  if(faultType !== "none"){
    ctx.beginPath();
    ctx.strokeStyle="#111";
    ctx.lineWidth=5;
    const faultX = 390;
    if(faultType==="reverse"){
      // 逆断层：上盘上升
      ctx.moveTo(faultX,20);
      ctx.lineTo(faultX+70,340);
      ctx.fillStyle="#000";
      ctx.font="14px yahei";
      ctx.fillText("逆断层｜上盘相对上升",faultX+20,180);
    }else if(faultType==="normal"){
      // 正断层：上盘下降
      ctx.moveTo(faultX,20);
      ctx.lineTo(faultX-70,340);
      ctx.fillStyle="#000";
      ctx.font="14px yahei";
      ctx.fillText("正断层｜上盘相对下降",faultX-100,180);
    }
    ctx.stroke();
  }
}

// 滑块拖动更新褶皱
deformSlider.oninput = ()=>{
  deformValue = Number(deformSlider.value);
  drawModel();
}

// 重置
btnReset.onclick = ()=>{
  deformValue = 0;
  deformSlider.value = 0;
  faultType = "none";
  drawModel();
}
// 逆断层
btnReverseFault.onclick = ()=>{
  faultType = "reverse";
  drawModel();
}
// 正断层
btnNormalFault.onclick = ()=>{
  faultType = "normal";
  drawModel();
}
// 清除断层
btnNoFault.onclick = ()=>{
  faultType = "none";
  drawModel();
}

drawModel();
</script>
</body>
</html>
