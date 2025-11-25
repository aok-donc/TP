# TP 1

#TP 2

| VLAN | Département | PC   | IP        | Masque        | Passerelle |
| ---- | ----------- | ---- | --------- | ------------- | ---------- |
| 10   | RH          | PC0  | 10.0.10.2 | 255.255.255.0 | 10.0.10.1  |
| 10   | RH          | PC1  | 10.0.10.3 | 255.255.255.0 | 10.0.10.1  |
| 10   | RH          | PC2  | 10.0.10.4 | 255.255.255.0 | 10.0.10.1  |
| 10   | RH          | PC3  | 10.0.10.5 | 255.255.255.0 | 10.0.10.1  |
| 20   | Production  | PC4  | 10.0.20.2 | 255.255.255.0 | 10.0.20.1  |
| 20   | Production  | PC5  | 10.0.20.3 | 255.255.255.0 | 10.0.20.1  |
| 20   | Production  | PC6  | 10.0.20.4 | 255.255.255.0 | 10.0.20.1  |
| 20   | Production  | PC7  | 10.0.20.5 | 255.255.255.0 | 10.0.20.1  |
| 20   | Production  | PC8  | 10.0.20.6 | 255.255.255.0 | 10.0.20.1  |
| 20   | Production  | PC9 | 10.0.20.7 | 255.255.255.0 | 10.0.20.1  |
| 30   | Direction   | PC10 | 10.0.30.2 | 255.255.255.0 | 10.0.30.1  |
| 30   | Direction   | PC11 | 10.0.30.3 | 255.255.255.0 | 10.0.30.1  |
| 30   | Direction   | PC12 | 10.0.30.4 | 255.255.255.0 | 10.0.30.1  |

1) Fa0/0 n’a pas d’IP car chaque sous-interface reçoit l’IP pour son VLAN et Fa0/0 sert juste de trunk.
2) Oui, un trunk peut transporter théoriquement jusqu’à 4094 VLANs.
3) Sans passerelle, un PC communique seulement dans son VLAN, pas avec les autres.
4) Oui, plusieurs trunks sont possibles, mais un seul suffit généralement pour le routage inter-VLAN.
## TP 3 Tableau d'adressage et réponse aux questions

| Site  | VLAN | Département  | PC    | IP               | Masque           | Passerelle        |
|-------|------|--------------|-------|------------------|------------------|-------------------|
| A     | 10   | Ventes       | PC0   | 192.168.10.2     | 255.255.255.0    | 192.168.10.1      |
| A     | 10   | Ventes       | PC1   | 192.168.10.3     | 255.255.255.0    | 192.168.10.1      |
| A     | 10   | Ventes       | PC2   | 192.168.10.4     | 255.255.255.0    | 192.168.10.1      |
| A     | 10   | Ventes       | PC3   | 192.168.10.5     | 255.255.255.0    | 192.168.10.1      |
| A     | 20   | Support      | PC4   | 192.168.20.2     | 255.255.255.0    | 192.168.20.1      |
| A     | 20   | Support      | PC5   | 192.168.20.3     | 255.255.255.0    | 192.168.20.1      |
| A     | 20   | Support      | PC6   | 192.168.20.4     | 255.255.255.0    | 192.168.20.1      |
| A     | 20   | Support      | PC7   | 192.168.20.5     | 255.255.255.0    | 192.168.20.1      |
| B     | 30   | Marketing    | PC0(1)| 192.168.30.2     | 255.255.255.0    | 192.168.30.1      |
| B     | 30   | Marketing    | PC1(1)| 192.168.30.3     | 255.255.255.0    | 192.168.30.1      |
| B     | 30   | Marketing    | PC2(1)| 192.168.30.4     | 255.255.255.0    | 192.168.30.1      |
| B     | 40   | Logistique   | PC5(1)| 192.168.40.2     | 255.255.255.0    | 192.168.40.1      |
| B     | 40   | Logistique   | PC6(1)| 192.168.40.3     | 255.255.255.0    | 192.168.40.1      |
| B     | 40   | Logistique   | PC7(1)| 192.168.40.4     | 255.255.255.0    | 192.168.40.1      |

| Liaison         | Appareil         | IP         | Masque             |
|-----------------|------------------|------------|--------------------|
| Inter-routeurs  | Routeur Site A   | 10.0.0.1   | 255.255.255.252    |
| Inter-routeurs  | Routeur Site B   | 10.0.0.2   | 255.255.255.252    |


### Questions:

- Que se passerait-il si on supprimait une route statique sur R1 ?
Si on supprime une route statique sur R1, il ne pourra plus atteindre le réseau correspondant et le trafic sera bloqué.

- Pourquoi utiliser un masque /30 pour la liaison WAN ?
Un masque /30 est utilisé sur une liaison WAN car il fournit exactement 2 adresses utilisables

- Pouvons-nous ajouter un 3ème site ?
Oui, on peut ajouter un 3e site en créant de nouvelles routes et en modifiant le masque utilisé.

- Quels sont les avantages et inconvénients du routage statique ?
Le routage statique est simple, rapide et sécurisé, mais ne s’adapte pas automatiquement et devient difficile à gérer sur de grands réseaux.

- Que se passerait-il si la liaison WAN tombait en panne ?
Si la liaison WAN tombe en panne, les sites ne pourront plus communiquer entre eux et seules les communications locales resteront possibles.
