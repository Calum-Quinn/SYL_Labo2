# SYL_Labo2

## Questions

### Question 1
#### Identifiez et documentez les différents opcodes entraînant une erreur.

### Question 2
#### Reprenez le schéma disponible en Figure `1` et donnez, pour chaque bloc, les bits d'opcode utilisés (l'idée est de répondre aux oints d'interrogation dans le schéma). Vos réponses doivent être de la forme "les bits d'opcode du bloc add/sub sont les bits [X:Y]".

### Question 3
#### Lorsqu'un overflow se produit, le signe n'est plus géré correctement et la sortie `negative_o` n'a donc pas la bonne valeur. Corrigez ce problème et expliquez votre raisonnement dans le fichier pdf.

### Question 4
#### Mettez en place une table de vérité, puis justifiez le développement de votre circuit.

Les nombres binaires qui sont des puissances de 2 ne possèdent qu'un seul 1 et tous les autres bits sont à 0. Ceci est dû au fait qu'un bit à 1 représente une puissance de 2.

Notre fonction logique devra donc contrôler qu'au maximum 1 bit est à 1 dans le nombre en entrée.

La table de vérité que nous voulons obtenir avec notre circuit est donc:

|A	|B	|C	|D	|S	|
|---|---|---|---|---|
|0	|0	|0	|0	|1	|
|0	|0	|0	|1	|1	|
|0	|0	|1	|0	|1	|
|0	|0	|1	|1	|0	|
|0	|1	|0	|0	|1	|
|0	|1	|0	|1	|0	|
|0	|1	|1	|0	|0	|
|0	|1	|1	|1	|0	|
|1	|0	|0	|0	|1	|
|1	|0	|0	|1	|0	|
|1	|0	|1	|0	|0	|
|1	|0	|1	|1	|0	|
|1	|1	|0	|0	|0	|
|1	|1	|0	|1	|0	|
|1	|1	|1	|0	|0	|
|1	|1	|1	|1	|0	|

Nous pouvons donc déduire la fonction `A/B/C/D + /AB/C/D + /A/BC/D + /A/B/CD`. Celle ci peut facilement être simplifiée en `(A/B + /AB)/C/D + (C/D + /CD)/A/B` qui en tour devient `(A^B)/C/D + (C^D)/A/B`.

Cette fonction devient facile à schématiser.

### Question 5
#### En plus des opcodes invalides, certains cas d'utilisation doivent générer une erreur. Déterminez ces différents cas et documentez les avant d'implémenter les modifications nécessaires.

### Question 6
#### Avec `a_i[3:0] = 0001`, `b_i[3:0] = 1001` et `op_i[6:0] = 011011` quelle est la valeur observée pour l'overflow ? Et pour la sortie `erreur_o` ? Cela correspond-t-il à ce que vous attendiez à la suite de la Question 5?
