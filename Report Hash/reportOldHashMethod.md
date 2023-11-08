Quelles sont les premiéres méthodes de hachages utilisés? 

SHA-1 :

source : https://www.securiteinfo.com/cryptographie/hash-sha1-obsolete.shtml
          Cryptomancie avancée, Algorithme, protocoles et codes sources en C, Bruce Schneier

SHA-1 est un algortihme de hachage à 160 bits qui à éte publié en 1995 par la National Agency Security (NSA) des Etats-Unis pour remédier aux soucis de sécurité lié au MD4.
SHA-1 à été utilisé pendant presque 30 ans pour assurer l'intégralité des données dans les sites web (Mots de passe par exemple , comparaison du hash entre le mot de passe rentré par l'utilisateur et le hash présent dans la BDD),
La découverte de nombreuses vulnérabilité au fil du temps ont conduits à l'arret de l'utilisation de sha-1 par Microsoft le 16 avril 2022.

Inconvenients du sha-1 : 

Le principale incovénient du sha-1 est la présence de collision. Une collsion est lorsque deux messages différents (ou fichiers) ressortent avec le même hash. Cette probabilité étais a première vu relativement faible,
Mais il n'a fallut que 10 ans pour qu'en 2005 la première collision soit trouvé par un groupe de chercheurs. Cela ouvre la voie pour des cybercriminels afin que ces derniers puissent prendre l'idendité d'un tier pour pouvoir signer un document à sa place par exemple.

L'autre faiblesse de sha-1 est sa vulnérabilité au attaque par force brute. En effet en 2005 il a été prouvé par Wang et al qu'il fallait 2^63 opération pour créer une collision.

MD5 : 
 MD5 est concu par Ron Rivest, c'est une version amélioré de MD4. Il produit des empreintes sur 128bits.

