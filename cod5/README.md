# Call of Duty: World at War (COD5) - Easy-WI Gameserver Template

### Bei der Installation ist zu beachten:

Der Linuxserver erfordert die Englische Version des Spiels. Es sollten also folgende Datein müssen aus dem Gameclient auf den Server hochgeladen werden:

1. main/iw_00.iwd bis main/iw_27.iwd
2. main/localized_english_iw00.iwd bis main/localized_english_iw06.iwd
3. Der gesamte zone/* Ordner

Nachdem ihr diese Datein hochgeladen habt, müsst ihr euch folgende Datei herunterladen ([GIDF](https://lmgtfy.com/?q=codwaw-lnxded-1.6-09142009.tar.bz2)).

Diese mit 7zip oder WinRar entpacken und die Datein per FTP ebenfalls auf den Server laden. Dabei bestätigen, dass eine Datein überschrieben werden dürfen.

Wichtig ist, dass für die Datein ''codwaw_lnxded'' und ''codwaw_lnxded-bin'' die Rechte 745 hat, damit der Server ausgeführt werden kann.

Damit der Server dann einen Namen, Rcon Passwort usw. bekommt, solltet ihr folgendes in eure server.cfg einfügen:
  
'''  
sv_hostname "COD5 Server" // Servername  
rcon_password "lassmichnichtso" // Rcon Passwort  
sv_floodProtect "1" // Schützt den Server gegen Angriffe durch das Spammen von Befehlen in Richtung des Servers  
sv_reconnectLimit "5" // Begrenzt die Anzahl wie oft sich ein einzelner Spieler nach einen Verbindungsabbruch auf den Server zurück verbinden darf  
sv_cheats "0" // Aktiviert/Deaktivert die Möglichkeit, Cheats auf dem Server zu aktivieren  
sv_voice "1" // Aktiviert/Deaktiviert den Voicechat auf dem Server  
scr_teambalance "1" // Aktiviert die automatischer Verteilung von Spielern auf dem Server  
g_allowvote "1" // Aktiviert/Deaktiviert das Voting für die nächste Map nach dem Ende der vorangegangen Map auf dem Server  
'''
