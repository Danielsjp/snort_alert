# snort_alert

alert tcp any any -> $HOME_NET any (msg:"ALERTA - POSIBLE ESCANEO NMAP SYN"; flags:S; detection_filter:track by_src, count 10, seconds 5; sid:1000001; rev:1;)
