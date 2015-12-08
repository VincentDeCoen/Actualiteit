###Deeltaak 2: Ansible Vault

#####1. Wat is Vault?
'Vault' is een nieuwe feature in ansible die gevoelige informatie zoals passwoorden kan encrypteren. 

Tijdens onze labo-opdrachten doorheen het semester, hebben we gebruikerspasswoorden meestal in een niet-geëncrypteerde vorm opgeslagen in een host_vars file. Voor administrators hebben we de passwoorden geëncrypteerd via de site mkpasswd.net, maar het passwoord werd gewoon te grabbel gegooid in de host_vars file en dit is allesbehalve goed voor de beveiliging, indien de labo-servers worden beschouwd als 'echte' servers die in gebruik genomen worden door bedrijven. 

######1.1 Enkel passwoorden?
Niet alleen passwoorden kunnen worden geëncrypteerd maar ook volledige ansible taskfiles en handlers. 

#####2. Hoe werkt Vault?

1. Aanmaken van een geëncrypteerde file  
```ansible-vault create foo.yml```

2. Aanpassen van een geëncrypteerde file  
```ansible-vault edit foo.yml```

3. Authenticatie aanpassen  
```ansible-vault rekey foo.yml```

4. File encrypteren  
```ansible-vault encrypt foo.yml```

5. File decrypteren  
```ansible-vault decrypt foo.yml```

6. Inhoud van geëncrypteerde file tonen  
```ansible-vault view foo.yml```

7. Playbook met geëncrypteerde bestanden uitvoeren  
```ansible-playbook site.yml --ask-vault-pass```

#####3. Toepassing op een labo uit de cursus Enterprise Linux

1. Centos VM opstarten
2. ```vagrant ssh [VMNaam]``` 
2. Naar de Home directory van ansible gaan
3. ```sudo ansible-playbook -i host_vars site.yml --ask-vault-pass```

U ziet dat de playbook nu uitgevoerd wordt.



 
