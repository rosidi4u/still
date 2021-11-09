<!DOCTYPE html>
<html>

<head>
	<title>Tolong inget terus Yaa </title>
</head>
<body onload="tes()">
 <style>
body {
  background-image: url('bun.gif');
}


</style> 

<div id="tanggal"></div>
 
	<script language="JavaScript">
    var tanggallengkap = new String();
    var namahari = ("Minggu Senin Selasa Rabu Kamis Jumat Sabtu");
    namahari = namahari.split(" ");
    var namabulan = ("Januari Februari Maret April Mei Juni Juli Agustus September Oktober November Desember");
    namabulan = namabulan.split(" ");
    var tgl = new Date();
    var hari = tgl.getDay();
    var tanggal = tgl.getDate();
    var bulan = tgl.getMonth();
    var tahun = tgl.getFullYear();
    tanggallengkap = namahari[hari] + ", " +tanggal + " " + namabulan[bulan] + " " + tahun;
    </script>
<center><h1><script language='JavaScript'>document.write(tanggallengkap);</script></h1></center>
	<style>
	h1,h2,p,a{
		font-family: sans-serif;
		font-weight: normal;
		color:	 	#000000  ;
		;
	}

	.jam-digital-foryou {
		overflow: hidden;
		width: 330px;
		margin: 20px auto;
		
	}
	.kotak{
		float: left;
		width: 110px;
		height: 80px;
		
	}
	.jam-digital-foryou p {
		color: #000000 ;
		font-size: 36px;
		text-align: center;
		margin-top: 30px;
	}
.jam_analog_foryou {
		
		position: relative;
		width: 150px;
		height: 150px;
		border: 16px solid #FF007F ;
		border-radius: 50%;
		padding: 20px;
		margin:20px auto;
	}

	.xxx {
		height: 100%;
		width: 100%;
		position: relative;
	}

	.jarum {
		position: absolute;
		width: 50%;
		background: #232323;
		top: 50%;
		transform: rotate(90deg);
		transform-origin: 100%;
		transition: all 0.05s cubic-bezier(0.1, 2.7, 0.58, 1);
	}

	.lingkaran_tengah {
		width: 20px;
		height: 20px;
		background: #FFC0CB ;
		border: 4px solid #FF007F ;
		position: absolute;
		top: 50%;
		left: 50%;
		margin-left: -14px;
		margin-top: -14px;
		border-radius: 50%;
	}

	.jarum_detik {
		height: 2px;
		border-radius: 1px;
		background: #F0C952;
	}

	.jarum_menit {
		height: 4px;
		border-radius: 4px;
	}

	.jarum_jam {
		height: 8px;
		border-radius: 4px;
		width: 35%;
		left: 15%;
	}
</style>



<div class="jam-digital-foryou">
	<div class="kotak">
		<p id="jam"></p>
	</div>
	<div class="kotak">
		<p id="menit"></p> 
	</div>
	<div class="kotak">
		<p id="detik"></p>
	</div>

</div>

     
<script>
function tes(){

var b=new Date();
var c=b.getHours();
if(c>0 && c<4){
c="Dah lewat tengah malam sayang..susah tidur ya...";
}else if(c>=0 && c<4){
c="Dah lewat tengah malam sayang...susah tidur ya...?";
}else if(c>=4 && c<9){
c="Selamat pagi sayang...dah sarapan belum, kamu kan susah kalo sarapan ...subuhnya kelewat ga tadi?";
}else if(c>=9 && c<15){
c="Selamat siang sayang... dah mam belum...inget zuhurnya ?";
}else if(c>=15 && c<18){
c="Selamat sore beb.. siap-siap istirahat ya.. jangan lupa mandi..Asharnya jangan lupa ";
}else if(c>=18 && c<21){
c="Selamat malam.. Magribnya jangan kelewat sama isyanya jangan males";
}else if(c>=21 && c<22){
c="Dah malam selamat bobo ya ";
}else if(c>=22 ){
c="Jangan begadang yaa";
}
{
document.getElementById("salam").innerHTML=c;

}
}</script>


<script>
	window.setTimeout("waktu()", 1000);

	function waktu() {
		var waktu = new Date();
		setTimeout("waktu()", 1000);
		document.getElementById("jam").innerHTML = waktu.getHours();
		document.getElementById("menit").innerHTML = waktu.getMinutes();
		document.getElementById("detik").innerHTML = waktu.getSeconds();
		
}

</script>

<div class="jam_analog_foryou">
	<div class="xxx">
		<div class="jarum jarum_detik"></div>
		<div class="jarum jarum_menit"></div>
		<div class="jarum jarum_jam"></div>
		<div class="lingkaran_tengah"></div>
	</div>
</div>


<script type="text/javascript">
	const secondHand = document.querySelector('.jarum_detik');
	const minuteHand = document.querySelector('.jarum_menit');
	const jarum_jam = document.querySelector('.jarum_jam');

	function setDate(){
		const now = new Date();

		const seconds = now.getSeconds();
		const secondsDegrees = ((seconds / 60) * 360) + 90;
		secondHand.style.transform = `rotate(${secondsDegrees}deg)`;
		if (secondsDegrees === 90) {
			secondHand.style.transition = 'none';
		} else if (secondsDegrees >= 91) {
			secondHand.style.transition = 'all 0.05s cubic-bezier(0.1, 2.7, 0.58, 1)'
		}

		const minutes = now.getMinutes();
		const minutesDegrees = ((minutes / 60) * 360) + 90;
		minuteHand.style.transform = `rotate(${minutesDegrees}deg)`;

		const hours = now.getHours();
		const hoursDegrees = ((hours / 12) * 360) + 90;
		jarum_jam.style.transform = `rotate(${hoursDegrees}deg)`;
	}

	setInterval(setDate, 1000)

	</script>



	<center>
	  
	 <table>
     <tr >
        <td style = "center"><h1 id="salam"></h1></td>
     </tr>
     <tr >
         <td style = "center"><h2>Hallo Bella Salsabilla sayang ... Setiap jam, menit, detik.. aku tetap sayang dan pastinya rindu kamu..</h2>		 
ketuk love di nama aku</td>
     <tr  onclick="play()"  onmouseover="this.src='like.gif"  >
       
         <td font-style = "bold"><h3><img src="love.png" id="b1" width="30" height="30" onmouseover="mouseOver()"   />ocid (Dimas Rosidi) hehe ......</h3>
I Love You</td>
     </tr>

 
  </table>
    <script>
      function play() {
        var audio = document.getElementById("audio");
        audio.play();
      }
    </script>
    <audio id="audio" src="lagu3.mp3"></audio>

	<script type="text/javascript">
		function mouseOver()
		{
			document.getElementById("b1").src="like.gif";
		}
		
	</script>
</center>


</body>
</html>
