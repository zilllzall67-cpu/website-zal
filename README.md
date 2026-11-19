# website-zal
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Perubahan Kecil, Dampak Besar</title>
<style>
body{margin:0;font-family:system-ui,sans-serif;background:#eef3f0;color:#10231c;line-height:1.6}
main{max-width:640px;margin:0 auto;padding:20px}
h1{font-size:2.8rem;line-height:1.05;margin:48px 0 16px}
h2{margin-top:40px}
.lead{font-size:1.2rem;color:#4a5e55}
.hasil{font-size:3.5rem;font-weight:800;color:#0a7c66}
input{width:100%}
li{margin-bottom:8px}
</style>
</head>
<body>
<main>
<h1>Satu persen setiap hari.</h1>
<p class="lead">Perubahan kecil terasa tidak berarti hari ini. Tapi diulang terus, hasilnya bisa mengubah hidup.</p>

<h2>Hitung sendiri</h2>
<p>Jika Anda membaik 1% setiap hari, setelah <b id="h">180</b> hari:</p>
<input id="s" type="range" min="1" max="365" value="180">
<div class="hasil" id="o"></div>

<h2>Kebiasaan kecil dalam setahun</h2>
<ul>
<li>Membaca 10 menit sehari: sekitar 61 jam</li>
<li>Jalan kaki 15 menit sehari: sekitar 91 jam</li>
<li>Menabung Rp5.000 sehari: Rp1.825.000</li>
</ul>

<h2>Mulai dari yang paling kecil</h2>
<ol>
<li>Pilih satu kebiasaan saja.</li>
<li>Perkecil sampai terasa mudah.</li>
<li>Kaitkan dengan rutinitas yang sudah ada.</li>
<li>Jangan putus dua hari berturut-turut.</li>
</ol>
</main>
<script>
var s=document.getElementById('s');
function r(){var d=+s.value;document.getElementById('h').textContent=d;
document.getElementById('o').textContent=Math.pow(1.01,d).toFixed(1).replace('.',',')+'×'}
s.oninput=r;r();
</script>
</body>
</html>