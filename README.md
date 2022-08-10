# Herdin_Nor_Saputra-Tugas2
tugas fixbug BDI

. bug_variable-score
-bug
  The name '_score' does not exist in the current context in GameManager.cs line 68 and 69
-fix
  mencari kesalahanya dengan cara mengklik peran error yang ada di console editor unity,
mengecek apakah variabel _score sudah pernah dibuat atau variable yang memiliki fungsi dan kegunaan sama,
terdapat variable score yang sesuai,
jadi untuk mengatasinya mengubah variabel "_score" pada line 69 dan 69 serta menambahkan ".toString()" pada variabel "score" di line 69

. fixbug/cowndowntex_not_set
-bug
  NullReferenceException: Object reference not set to an instance of an object
CountdownText+d__6.MoveNext () (at Assets/scripts/CountdownText.cs:31)
OnCountdownFinished tidak pernah diinisialisasi di CountDownText.cs dalam method OnEnable di GameManager.cs
-fix
  tambahkan baris kode " CountdownText.OnCountdownFinished += OnCountdownFinished; " di dalan method OnEnable() di GameManager.cs
  
-bug
  state tidak pernah netral, object StartPage selalu active
-fix
  ubah " !gameOver " di GamaManager.cs(28,38) menjadi " gameOver "

-bug
  plane tetap jatuh ketika di klik,
memeriksa fungsi yang menggerakan plane,
arah pergerakan plane ketika diklik Vector2.down, jadi plane tidak bergerak keatas.
-fix
  ubah Vector2.down ke vectore2.up di TapController.cs(66,32) agar pergerakan plane ke atas jika diklik
