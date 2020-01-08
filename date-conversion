// return 4 type of data, following var $t
// return in 2 lang, it and en, following $lang
function datax($d,$lang,$t){
	
	// types of return
	// C = Domenica, 03 gennaio 2013
	// G = Lunedì
	// M = Ottobre
	// A = 2012
	
	
// $d can be: YYYY-MM-DD or DD/MM/YYYY

			if ( strstr($d, '/') ) {
			$dx1=explode("/", $d);
			$dx[0]=$dx1[2];
			$dx[1]=$dx1[1];
			$dx[2]=$dx1[0];
			}
			
			if ( strstr($d, '-') ) {
			$dx=explode("-", $d);
			}

    $d_ts=mktime(0,0,0,$dx[1],$dx[2],$dx[0]);
    $num_gg=(int)date("N",$d_ts);

   
    if ($lang=="en") {
    $giorno=array('','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday');
  	} else {
  	$giorno=array('','Lunedì','Martedì','Mercoledì','Giovedì','Venerdì','Sabato','Domenica');
  	}	
    
    if ($lang=="en") {
    $mese =array('January','February','March','April','May','June','July','August','September','October','November','December');
  	} else {
  	$mese =array('Gennaio','Febbraio','Marzo','Aprile','Maggio','Giugno','Luglio','Agosto','Settembre','Ottobre','Novembre','Dicembre');
  	}
    
    
if ($t=="C") {
$str = $giorno[$num_gg].", ".$dx[2]." ".$mese[intval($dx[1]-1)]." ".$dx[0];
return $str;
}
if ($t=="G") { return $giorno[$num_gg]; }
if ($t=="M") {return $mese[intval($dx[1]-1)]; }
if ($t=="A") {return $dx[0]; }	


}

//echo datax("2016-01-03","it","C");
