```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>聊天记录阅读器</title>
<link rel="manifest" href="manifest.json">
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{max-width:900px;margin:16px auto;padding:0 10px;font-family:-apple-system,BlinkMacSystemFont,sans-serif;background:#fafafa}
#chatBox{height:70vh;border:1px solid #ddd;padding:12px;overflow-y:auto;margin:10px 0;background:#fff;border-radius:12px}
.msg{margin:8px 0;padding:10px;border-radius:12px;max-width:75%}
.user{background:#e3f2fd;margin-left:auto}
.other{background:#eeeeee;margin-right:auto}
.time{font-size:12px;color:#555;margin-top:4px}
#control{margin-bottom:10px}
button{padding:8px 14px;cursor:pointer;margin-left:6px;border-radius:8px;border:none;background:#4285f4;color:#fff}
#fileInput{padding:5px}
.empty-tip{text-align:center;color:#999;margin-top:200px}
</style>
</head>
<body>
<div id="control">
<input type="file" id="fileInput" accept=".json">
<button onclick="clearChat()">清空视图</button>
</div>
<div id="chatBox">
<div class="empty-tip">请选择本地聊天记录json文件加载</div>
</div>

<script>
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('service-worker.js');
}

const chatBox = document.getElementById("chatBox");
const fileInput = document.getElementById("fileInput");

fileInput.onchange = function(e){
  const file = e.target.files[0];
  if(!file) return;
  const reader = new FileReader();
  reader.onload = function(event){
    try{
      const data = JSON.parse(event.target.result);
      renderChat(data);
    }catch(err){
      alert("JSON解析失败！检查文件格式\n"+err.message);
    }
  }
  reader.readAsText(file);
}

function renderChat(list){
  chatBox.innerHTML = "";
  if(!Array.isArray(list)){
    chatBox.innerHTML = '<div class="empty-tip">数据不是数组，请核对json格式</div>';
    return;
  }
  list.forEach(item=>{
    const div = document.createElement("div");
    const role = item.role === "user" ? "user" : "other";
    div.className = "msg " + role;
    div.innerHTML = `
      <div>${escapeHtml(item.content || "")}</div>
      <div class="time">${item.time || "无时间"}</div>
    `;
    chatBox.appendChild(div);
  })
  chatBox.scrollTop = chatBox.scrollHeight;
}

function escapeHtml(str) {
  return str.replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");
}

function clearChat(){
  chatBox.innerHTML = '<div class="empty-tip">请选择本地聊天记录json文件加载</div>';
  fileInput.value = "";
}
</script>
</body>
</html>

```
