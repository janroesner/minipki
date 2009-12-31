## Einführung

minipki ist eine Sammlung von einfachen Shell Aufrufen ohne Fehlerbehandlung und Nutzerinterakktivität. In der Grundkonfigration wird eine Root- sowie eine SubCA angelegt, so dass nachträglich mit der SubCA Entity Zertifikate ausgegeben werden können. Ausserdem lassen sich CRL's für Root- und SubCA ausgeben, sowie Entity Zertifikate als PKCS#7 und PKCS#12 Container exportieren.

## Benötigt

Recent release of [openssl](http://www.openssl.org)

## Kickstart

ToDo

	cd minipki
	./init_filesystem

In den Verzeichnissen der Root- und der SubCA nachfolgend die ca.config, ca.ext und die user.ext anpassen. 

	./init_root
	./init_sub
	./issue_root_crl
	./issue_subcrl

Your done. Entity Zertifikate können nun mit 

	./issue_user

erzeugt werden. Für den Rueckruf von Zertifikaten ist in `revoke_user`sowie in `revoke_subca`die id des Zertifikates von Hand anzugeben. � 

## Caveats

Jede Menge

## Copyright

Tu damit, was auch immer Du willst. Changes sind willkommen.
