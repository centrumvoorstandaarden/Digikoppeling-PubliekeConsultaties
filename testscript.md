# get latest release via Git op Github

Onderstaand de stappen die je moet uitvoeren om de de latest release van een repository op te halen met **Git** commando's. 

Github biedt ook een api aan om de latest release op te vragen. Die geeft een response met daarin (onder andere) de links naar de zipfile van die release. Die is voor de usecase met publicatie van een html versie logius.nl misschien minder handig. Vandaar dat ik in onderstaand script mij geheel gefocussed op hoe je de latest release kan ophalen met **git** commando's.  

## Usecase

doel: op logius.nl wordt de meest recente *gereleasede* versie van een standaard getoond

- cvs onderhoudt haar standaarden in repositories op github
- pas als een versie door cvs **gereleased** wordt is een nieuwe versie officieel
- logius.nl (dictu) voert elke nacht een git commando uit om de laatste versie van een standaardpublicatie op te halen
  - de url van de repository wordt eenmalig geconfigureerd (op verzoek van cvs)
- (anticase) als logius.nl een standaard *pull* commando zou gebruiken dan zou de meest recente (werk)versie opgehaald worden, dat is zeker niet wenselijk
- voorwaarde: logus.nl moet dus de laatst *releasede* versie ophalen
- met`create release` kan in Github een branch worden **getagd** 
- met onderstaand script kan de laatste **getagde** versie van een branch worden opgehaald
- (uitzoeken) zijn er andere manieren om een branch te taggen? in dat geval werkt dit git script niet goed
- (uitzoeken) is gegarandeerd dat altijd de laatste versie wordt opgehaald?
- (uitzoeken) zijn er reparatiemogelijkheden als er iets misgaat? Zonder dat we communicatie of dictu moeten inschakelen

## script

nu volgt eerst een overzicht van de gebruikte commando's
daarna het geheel van drie commando's 
`todo` : kunnen de commando 2 en 3 in één regel worden samengevoegd. Ik heb het nu alleen getest in powershell in Windows 10, en weet niet goed hoe je dit moet doen. Het voorbeeld van devconnected laat zien hoe dat moet (in Bash).   


git-tag - Create, list, delete or verify a tag object signed with GPG

get the latest tags from repository

```
git fetch --tags
```

git-rev-list - Lists commit objects in reverse chronological order

get the latest commit

```
$temp2 = git rev-list --tags --max-count=1
```

git-describe - Give an object a human readable name based on an available ref

find the most recent tag that is reachable from a commit

```
$temp = git describe --tags $temp2
```

git-checkout - Switch branches or restore working tree files

get the latest tagged commit
```
git checkout $temp
```

Dus als script gecombineerd wordt uitgevoerd
```
git fetch --tags
$temp2 = git rev-list --tags --max-count=1
$temp = git describe --tags $temp2
git checkout $temp
```

dan wordt de laatste tagged version opgehaald (en dus niet de laatste commit)

source: <https://devconnected.com/how-to-checkout-git-tags/>