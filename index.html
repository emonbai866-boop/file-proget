<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RDCS CYBER OFFICIAL</title>
<style>
  body {
    margin:0;
    font-family: Arial, sans-serif;
    background-color: #0f172a;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: #fff;
  }

  /* Card */
  .card {
    width: 340px;
    background: #1e293b;
    border-radius: 20px;
    padding: 25px;
    text-align: center;
    box-shadow: 0 10px 25px rgba(0,0,0,0.5);
  }

  /* Lock icon */
  .lock-icon {
    width: 60px;
    height: 60px;
    margin: 0 auto 15px;
    background-color: #2563eb;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 28px;
  }

  h1 { margin:5px 0 5px; font-size: 20px; color:#38bdf8; }
  p { margin:0 0 20px; font-size:12px; color:#94a3b8; }

  label { display:block; text-align:left; font-size:13px; margin-bottom:5px; }

  /* Custom file input container */
  .file-upload {
    position: relative;
    border: 2px dashed #64748b;
    border-radius: 12px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    margin-bottom: 15px;
    transition: border-color 0.3s;
    background: #0f172a;
  }
  .file-upload:hover { border-color: #2563eb; }
  .file-upload span { color:#94a3b8; font-size:14px; }
  .file-upload input[type=file] {
    position: absolute;
    opacity: 0;
    width:100%;
    height:100%;
    cursor: pointer;
  }

  /* Password input */
  input[type=password] {
    width:100%;
    padding:12px;
    border-radius:12px;
    border:none;
    outline:none;
    background:#0f172a;
    color:white;
    margin-bottom:15px;
  }
  input[type=password]::placeholder { color:#94a3b8; }

  /* Buttons */
  .btn {
    width:100%;
    padding:12px;
    margin-bottom:10px;
    border-radius:12px;
    border:none;
    font-size:16px;
    font-weight:bold;
    cursor:pointer;
    color:white;
    transition:0.2s;
  }
  .encrypt { background:#2563eb; }
  .encrypt:hover { background:#1d4ed8; }
  .decrypt { background:#16a34a; }
  .decrypt:hover { background:#15803d; }

</style>
</head>
<body>

<div class="card">
  <div class="lock-icon">🔒</div>
  <h1>RDCS CYBER OFFICIAL</h1>
  <p>CREATOR EMON KHAN</p>

  <label>1. Select Your File</label>
  <div class="file-upload">
    <span>Click to upload file</span>
    <input type="file" id="fileInput">
  </div>

  <label>2. Your Secret Password</label>
  <input type="password" id="password" placeholder="Enter Password">

  <button class="btn encrypt" onclick="encryptFile()">Encrypt</button>
  <button class="btn decrypt" onclick="decryptFile()">Decrypt</button>
</div>

<script>
async function getKey(password){
  const enc = new TextEncoder();
  const keyMaterial = await crypto.subtle.importKey("raw", enc.encode(password), "PBKDF2", false, ["deriveKey"]);
  return crypto.subtle.deriveKey({
    name: "PBKDF2",
    salt: enc.encode("RDCS-CYBER-OFFICIAL-SALT"),
    iterations: 100000,
    hash: "SHA-256"
  }, keyMaterial, {name:"AES-GCM", length:256}, false, ["encrypt","decrypt"]);
}

async function encryptFile(){
  const file = document.getElementById("fileInput").files[0];
  const password = document.getElementById("password").value;
  if(!file || !password){ alert("Select file & enter password"); return; }

  const data = await file.arrayBuffer();
  const key = await getKey(password);
  const iv = crypto.getRandomValues(new Uint8Array(12));
  const encrypted = await crypto.subtle.encrypt({name:"AES-GCM", iv}, key, data);
  const blob = new Blob([iv, new Uint8Array(encrypted)]);
  download(blob, file.name+".enc");
}

async function decryptFile(){
  const file = document.getElementById("fileInput").files[0];
  const password = document.getElementById("password").value;
  if(!file || !password){ alert("Select file & enter password"); return; }

  const buffer = await file.arrayBuffer();
  const iv = buffer.slice(0,12);
  const data = buffer.slice(12);
  const key = await getKey(password);

  try{
    const decrypted = await crypto.subtle.decrypt({name:"AES-GCM", iv}, key, data);
    const blob = new Blob([decrypted]);
    download(blob, "decrypted_"+file.name.replace(".enc",""));
  }catch{
    alert("Wrong password or invalid file");
  }
}

function download(blob, filename){
  const a=document.createElement("a");
  a.href=URL.createObjectURL(blob);
  a.download=filename;
  a.click();
}
</script>

</body>
</html>
