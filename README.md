# Herdin_Nor_Saputra-Tugas2
tugas fixbug BDI

. bug_variable-score<br />
prioritas = Low \
:interrobang:-bug<br />
  The name '_score' does not exist in the current context in GameManager.cs line 68 and 69<br /> 
:heavy_check_mark:-fix<br />
  mencari kesalahanya dengan cara mengklik peran error yang ada di console editor unity,
mengecek apakah variabel _score sudah pernah dibuat atau variable yang memiliki fungsi dan kegunaan sama,
terdapat variable score yang sesuai,<br />
jadi untuk mengatasinya mengubah variabel "_score" pada line 69 dan 69 serta menambahkan ".toString()" pada variabel "score" di line 69<br />

. fixbug/cowndowntex_not_set<br />
prioritas = Low \
:interrobang:-bug<br />
  NullReferenceException: Object reference not set to an instance of an object
CountdownText+d__6.MoveNext () (at Assets/scripts/CountdownText.cs:31)
OnCountdownFinished tidak pernah diinisialisasi di CountDownText.cs dalam method OnEnable di GameManager.cs<br />
:heavy_check_mark:-fix<br />
  tambahkan baris kode " CountdownText.OnCountdownFinished += OnCountdownFinished; " di dalan method OnEnable() di GameManager.cs<br />
  
:interrobang:-bug<br />
  state tidak pernah netral, object StartPage selalu active<br />
:heavy_check_mark:-fix<br />
  ubah " !gameOver " di GamaManager.cs(28,38) menjadi " gameOver "

:interrobang:-bug<br />
  plane tetap jatuh ketika di klik,
memeriksa fungsi yang menggerakan plane,
arah pergerakan plane ketika diklik Vector2.down, jadi plane tidak bergerak keatas.<br />
:heavy_check_mark:-fix<br />
  ubah Vector2.down ke vectore2.up di TapController.cs(66,32) agar pergerakan plane ke atas jika diklik

. fixbug/DeadZone_bug\
prioritas = Low \
:interrobang:-bug <br />
  deadzone tidak terdeteksi olaeh plane<br />
:heavy_check_mark:-fix<br />
  plane tidak mendeteksi Wood, sehingga plane dapat melewati Woods tanpa Gameover,
maslah terdapat di method yang mendeteksi collider di sript TapController.cd(83,29),
cara mengatasinya dengan mengubah string yang ada di TapController.cd(ln83,ch29) dari "DeadZones" menjadi "DeadZone"
  setelah mengubah script, tambahkan tag DeadZone ke object Woods
