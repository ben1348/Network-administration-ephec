# Labo 1
dans cette note je vais parler de notre infrastructure pour se cours.

pour ce laboratoire on nous demande : 
1. d'installer un firewall Pfsense 
2. d'installer un serveur Proxmox
3. de deployer une premiere VM


## infrastructure
![infra donné par le prof](image/infra_prof.png)
ici c'est l'interface proxmox professeur (hyp-04) sur la quel nous devont nous connecter pour lancer nos hyperviseurs proxmox student(hyps-1601, hyps-1602) qui sont virtualiser. nous avons aussi un firewall Pfsense (fwns1601)

si on fait un schema de notre infrastructure, on obtient :
![schema de l'infra](image/notre_infra_redarrow.png)
le fleche rouge indique les 3 vm virtualiser par l'hyperviseur parent (hyp-04)

l'infra sera encore modifier par la suite dans le cours

## 1. PfSense

sur l'interface proxmox du professeur on va commencer par installer un firewall Pfsense (fwns1601) on lancer donc l'installation jusqu'a arriver a cette image : 
![installation de pfsense selection du wan](image/interface_du_firewall.png)
il nous demande de selectionner l'interface Wan
allons voir les interface disponibles et selectionner stuWan qui correspond a la sortie vers l'hyperviseur parent (hyp-04) : 
![interface reseau du firewall students](image/image_1.png)

## 2. Proxmox
