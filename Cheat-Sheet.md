# Cheatsheet Linux
==================

## Git Commando's
-----------------

|Commando|Beschrijving|
|-------|-----------|
|git clone --config core.autocrlf=input git@bitbucket.org:BITBUCKET_USERNAME/REPO.git|Clone de git repo naar je lokale omgeving|

## Vagrant Commando's
---------------------

|Commando|Beschrijving|
|-------|-----------|
|vagrant status|Geeft een overzicht van de Vagrant-omgeving|
|vagrant up [VM]|Start de VM op|
|vagrant provision [VM]|Draai het configuratiescript op VM|
|vagrant ssh VM|Log in op VM als gebruiker vagrant|
|vagrant halt [VM]|Stop VM|
|vagrant reload [VM]|Herstart VM|
|vagrant destroy -f [VM]|Vernietig VM|

## Ansible Vault Commando's
----------------------------

|Commando|Beschrijving|
|--------|------------|
|ansible-vault create foo.yml|Een geëncrypteerd bestand aanmaken|
|ansible-vault edit foo.yml|Een geëncrypteerd bestand aanpassen|
|ansible-vault encrypt foo.yml|Een bestand encrypteren|
|ansible-vault rekey foo.yml|Authenticatie van een geëncrypteerd bestand vernieuwen|
|ansible-vault decrypt foo.yml|Een bestand decrypteren|
|ansible-vault view foo.yml|De inhoud van een geëncrypteerd bestand weergeven|
|ansible-playbook site.yml --ask-vault-pass foo.yml|Ansible playbook met geëncrypteerde bestanden uitvoeren|


## Algemene Commando's
------------------------

|Commando|Beschrijving|
|-------|-----------|
|[in home dir van de repo] ./scripts/role-deps.sh|Dit voegt de te installeren ansible rollen toe aan je lokale repo|
|[in windows cmd van de host] nslookup linuxlab.lan 192.168.56.10|Doet een NSLookup bij de DNS. linuxlab.lan is het domein en het ip adres is van de DNS server|
|dig @192.168.56.42 butterfree.cynalco.com|Op de DNS server een dig commando uitvoeren naar de host met alias 'butterfree' in domein 'cynalco.com'|
|[in VM] sudo /vagrant/test/runbats.sh|De acceptatietesten van de host uitvoeren|
|[in VM] sudo loadkeys be-latin1|In de VM de keyboardinstellingen van qwerty naar azerty veranderen|

## Firewall Commando's
|Commando|Beschrijving|
|--------|-----------|
|sudo systemctl start firewalld.service|De firewall activeren|
|firewall-cmd --state|De status controlleren|
|firewall-cmd --reload|De service herladen|
|sudo firewall-cmd --add-service=dns|In de VM een service toelaten bij de firewall (hier dns)|

