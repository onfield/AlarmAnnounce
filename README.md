# AlarmAnnounce
Monitor Envisalink 3 and announce opening and closing of DSC alarm zones.

This perl server monitors a Envisalink for zone events and uses Festival TTS to announce the opening and closing of
partition zones.

A TCP proxy is created so the single connection to the Envisalink is not consumed by this script. When a client connects
to the server a connection to the Envisalink is established. The connection from the server is dropped when the client
disconnects.

I created this tool so I can do my own automation adn still allow the VeraEdge DSC Alarm Panel pluging to continue
functioning.

Installation on a Raspberry Pi -

festival
/etc/init/envisa.conf
/opt/onfield/audio/155.wav
/opt/onfield/cfg/announce.cfg
/opt/onfield/bin/envisa-announce.pl
