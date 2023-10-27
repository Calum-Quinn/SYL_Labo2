# Opcodes
## Opcode avec erreurs:
- Aucun qui commence avec 00????
- Aucun qui commence avec 10????
- Aucun qui commence avec 11????
- Tous qui commence avec  010???
- 011000
- 011111

## Quels bits font quel bloc (pas sûr d'avoir compris, là c'est les bits qui définissent quel opération faire à l'intérieur du bloc):
### add/sub:
Les bits d'opcode du bloc add/sub sont les bits [3:2]

### comparateur:
Les bits d'opcode du bloc comparateur sont les bits [2:0]

### unité logique:
Les bits d'opcode du bloc unité logique sont les bits [1:0]

### custom:
Les bits d'opcode du bloc custom sont les bits [5:4]



## Quels bits font quel bloc (pas sûr d'avoir compris, là c'est les bits qui définissent quel bloc choisir):
### add/sub:
Les bits d'opcode du bloc add/sub sont les bits [5:4]

### comparateur:
Les bits d'opcode du bloc comparateur sont les bits [5:4]

### unité logique:
Les bits d'opcode du bloc unité logique sont les bits [5:4]

### custom:
Les bits d'opcode du bloc custom sont les bits [5:4]