<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Finans Sepeti</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #fff;
}
.container {
    max-width: 400px;
    margin: auto;
    padding: 20px;
}
.card {
    background: rgba(255,255,255,0.08);
    border-radius: 15px;
    padding: 25px;
}
input {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border-radius: 8px;
    border: none;
}
button {
    width: 100%;
    padding: 12px;
    border-radius: 8px;
    border: none;
    background: #00c6ff;
    font-weight: bold;
}
.link {
    text-align: center;
    margin-top: 10px;
}
.link span {
    color: #00c6ff;
}
</style>
</head>

<body>

<div class="container" id="login">
<div class="card">
<h2>Finans Sepeti</h2>
<input type="email" placeholder="E-mail">
<input type="password" placeholder="Şifre">
<button type="button" onclick="show('dashboard')">Giriş Yap</button>
<div class="link">
<span onclick="show('register')">Üye Ol</span> •
<span onclick="show('forgot')">Şifremi Unuttum</span>
</div>
</div>
</div>

<div class="container" id="register" style="display:none;">
<div class="card">
<h2>Üye Ol</h2>
<input type="email" placeholder="E-mail">
<button type="button" onclick="show('verify')">Kod Gönder</button>
</div>
</div>

<div class="container" id="verify" style="display:none;">
<div class="card">
<h2>Kod Doğrula</h2>
<input type="text" placeholder="Kod">
<button type="button" onclick="show('password')">Devam</button>
</div>
</div>

<div class="container" id="password" style="display:none;">
<div class="card">
<h2>Şifre Oluştur</h2>
<input type="password" placeholder="Yeni Şifre">
<button type="button" onclick="show('login')">Kaydet</button>
</div>
</div>

<div class="container" id="forgot" style="display:none;">
<div class="card">
<h2>Şifremi Unuttum</h2>
<input type="email" placeholder="E-mail">
<button type="button" onclick="show('verify')">Kod Gönder</button>
</div>
</div>

<div class="container" id="dashboard" style="display:none;">
<div class="card">
<h2>Benim Sayfam</h2>
<p>🟡 Altın</p>
<p>⚪ Gümüş</p>
<p>📈 Borsa</p>
<p>₿ Kripto</p>
</div>
</div>

<script>
function show(id){
document.querySelectorAll('.container').forEach(e => e.style.display = 'none');
document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>
