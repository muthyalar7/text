&lt; ?php
 

$rImg = ImageCreateFromJPEG("ex-img.jpg");
$cor = imagecolorallocate($rImg, 0, 0, 0);
imagestring($rImg,5,126,22,urldecode($_GET['nome']),$cor);
 
header('Content-type: image/jpeg');
imagejpeg($rImg,NULL,100);
 
?&gt;
