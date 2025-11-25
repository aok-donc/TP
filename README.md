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
