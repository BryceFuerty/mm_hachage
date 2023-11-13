# Quelles sont les premiéres méthodes de hachages utilisés? 

sources : 


          https://www.securiteinfo.com/cryptographie/hash-sha1-obsolete.shtml

          https://cours.etsmtl.ca/mgr850/documents/cours/MGR850_A14_Cours-05_hachage.pdf

          Cryptomancie avancée, Algorithme, protocoles et codes sources en C, Bruce Schneier
          

 ## SHA-1 :



SHA-1 est un algortihme de hachage à 160 bits qui à éte publié en 1995 par la National Agency Security (NSA) des Etats-Unis pour remédier aux soucis de sécurité lié au MD4.
SHA-1 à été utilisé pendant presque 30 ans pour assurer l'intégralité des données dans les sites web (Mots de passe par exemple , comparaison du hash entre le mot de passe rentré par l'utilisateur et le hash présent dans la BDD),
La découverte de nombreuses vulnérabilité au fil du temps ont conduits à l'arret de l'utilisation de sha-1 par Microsoft le 16 avril 2022.

Inconvenients du sha-1 : 

Le principale incovénient du sha-1 est la présence de collision. Une collsion est lorsque deux messages différents (ou fichiers) ressortent avec le même hash. Cette probabilité étais a première vu relativement faible,
Mais il n'a fallut que 10 ans pour qu'en 2005 la première collision soit trouvé par un groupe de chercheurs. Cela ouvre la voie pour des cybercriminels afin que ces derniers puissent prendre l'idendité d'un tier pour pouvoir signer un document à sa place par exemple.

L'autre faiblesse de sha-1 est sa vulnérabilité au attaque par force brute. En effet en 2005 il a été prouvé par Wang et al qu'il fallait 2^63 opération pour créer une collision.

## MD5 : 
 MD5 est concu par Ron Rivest, c'est une version amélioré de MD4. Il produit des empreintes sur 128bits. La sortie de l'algortihme est un ensemble de 4 blocs de 32 bits joints ensemble pour former les 128 bits.
 MD5 manipule les textes d'entrés par blocs de 512 bits divisés en 16 blocs de 32 bits.
 
 4 variables de 32 bits sont utilisé :
 A : 0x01234567
 B : 0x89ABCDEF
 C : 0xFEDCBA98
 D : 0x76543210
 Ce sont les variables de chaînage

La boucle principale a 4 rondes , chaque ronde consiste en 16 exécutables d'une opération.Chaque opération calcule une fonction non linéaire de trois variables A,B,C et D.

 
 Securité : 
-Une quatrieme ronde a ete ajouté la ou md4 en avais 3
-Chaque étape a une constance additive unique 
-Chaque étape ajoute le résultat de l'étape précédente. Cela favorise un "effet d'avalanche" plus rapide.


## Attaque de préimage : 

L'attaque par préimage va avoir pour but de trouver un message ayant le même hash qu'un message donnée. Il y'a deux type d'attaques de préimage : 

### L'attaque à la préimage

• Une fonction h est résistante à la préimage s’il est difficile
de trouver à partir d’une empreinte donnée p un message m
tel que h(m) = p.

### L'attaque à la seconde préimage

• Une fonction h est résistante à la seconde préimage s’il
est difficile de trouver à partir d’un message m donné un
autre message m’ tel que h(m) = h(m’




