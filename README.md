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
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

h1 {
    text-align: center;
}

input {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border-radius: 8px;
    border: none;
    font-size: 16px;
}

button {
    width: 100%;
    padding: 12px;
    margin-top: 10px;
    border: none;
    border-radius: 8px;
    background: #00c6ff;
    font-size: 16px;
    font-weight: bold;
}

.link {
    text-align: center;
    margin-top: 15px;
    font-size: 14px;
}

.link span {
    color: #00c6ff;
    cursor: pointer;
}
</style>
</head>

<body>

<!-- GİRİŞ -->
<div class="container" id="login">
<div class="card">
<h1>Finans Sepeti</h1>
<input type="email" placeholder="E-mail">
<input type="password" placeholder="Şifre">
<button onclick="show('dashboard')">Giriş Yap</button>

<div class="link">
<span onclick="show('register')">Üye Ol</span> •
<span onclick="show('forgot')">Şifremi Unuttum</span>
</div>
</div>
</div>

<!-- ÜYE OL -->
<div class="container" id="register" style="display:none;">
<div class="card">
<h1>Üye Ol</h1>
<input type="email" placeholder="E-mail adresi">
<button onclick="show('verify')">Kod Gönder</button>
</div>
</div>

<!-- KOD DOĞRULAMA -->
<div class="container" id="verify" style="display:none;">
<div class="card">
<h1>Kod Doğrulama</h1>
<input type="text" placeholder="Mailinize gelen kod">
<button onclick="show('password')">Doğrula</button>
</div>
</div>

<!-- ŞİFRE OLUŞTUR -->
<div class="container" id="password" style="display:none;">
<div class="card">
<h1>Şifre Oluştur</h1>
<input type="password" placeholder="Yeni şifre">
<button onclick="show('login')">Kaydet</button>
</div>
</div>

<!-- ŞİFREMİ UNUTTUM -->
<div class="container" id="forgot" style="display:none;">
<div class="card">
<h1>Şifremi Unuttum</h1>
<input type="email" placeholder="E-mail adresi">
<button onclick="show('verify')">Kod Gönder</button>
</div>
</div>

<!-- DASHBOARD -->
<div class="container" id="dashboard" style="display:none;">
<h1>Benim Sayfam</h1>
<div class="card">
<p>📊 Yatırımlarım</p>
<p>🟡 Altın</p>
<p>⚪ Gümüş</p>
<p>📈 Borsa</p>
<p>₿ Kripto</p>
</div>
</div>

<script>
function show(id) {
    document.querySelectorAll('.container').forEach(c => c.style.display = 'none');
    document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>
