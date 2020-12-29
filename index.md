<html>
<head>
 <title>Genesis : Robot parleur (chatterbot, ou chatbot)</title>
 <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0" />
 <script language="JavaScript">
	window.onload = function() {
   document.getElementById('input').focus();
   document.getElementById('sauveinput').value="";
document.getElementById('input').value="";
	document.getElementById('boutonEnvoyerForm').disabled=true;
   }

   function verifChampUsersay(){
		if(document.getElementById('input').value!=""){
			document.getElementById('boutonEnvoyerForm').disabled=false;
		}else{
			document.getElementById('boutonEnvoyerForm').disabled=true;
		}
   }

//var verif = window.setInterval(validation,10000000);
var verif = window.setInterval(validation,1800000); //toutes les 180sec

function validation()
{
document.getElementById('sauveinput').value=document.getElementById('input').value;
document.getElementById('autorefresh').value="TRUE";
document.getElementById('input').value="";
    document.forms['form_parler'].submit();
}

function envoiemot(mot)
{
document.getElementById('input').value=mot;
    document.forms['form_parler'].submit();
}
</script>
 <link rel="stylesheet" type="text/css" href="defaut.css">
 </head>
 <body>

<a href="chatterbot23.php">Reset</a>
<br>
<br>
<br>
<div id="divCorpsPage">
	<img id="imgVisage" src="intro.gif?1609261681">
	<div id="divEspaceEnhautDesMessages"></div>
	<div id="divZoneMessagesEtEntreeTexte"><div id="divZoneEntreeTexte"><form method="POST" action="chatterbot23.php" id="form_parler"><bR><INPUT NAME="sauveinput" id="sauveinput" TYPE="HIDDEN" ><INPUT NAME="var" value="" id="var" TYPE="HIDDEN" ><INPUT NAME="vartemp" value="" id="vartemp" TYPE="HIDDEN" ><INPUT NAME="cerveau" value="AR.txt" id="cerveau" TYPE="HIDDEN" ><INPUT NAME="vraiesvars" value="" id="vraiesvars" TYPE="HIDDEN" ><INPUT NAME="nom" value="" id="nom" TYPE="HIDDEN" ><INPUT NAME="noreut" value="" id="noreut" TYPE="HIDDEN" ><INPUT NAME="vraiesvars" value="" id="vraiesvars" TYPE="HIDDEN" ><INPUT NAME="premiereOuverturePage" value="non" id="vraiesvars" TYPE="HIDDEN"><INPUT NAME="numUniquePourLog" value="1609261681" id="numUniquePourLog" TYPE="HIDDEN"><INPUT NAME="rappel" value="" id="rappel" TYPE="HIDDEN" ><INPUT NAME="autorefresh" id="autorefresh" TYPE="HIDDEN" value="FALSE"><input type=submit id="boutonEnvoyerForm" value="Envoyer"></div></div>

	</body>
 </html>
