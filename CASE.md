# Use case.

La société Mirow, qui héberge actuellement son site web chez AWS sur un seul serveur EC2 a de gros problèmes de montée en charge. Les soldes arrivants, l'equipe de devops doit changer l'architecture du site pour le rendre plus scalable.

Le site web de Mirow est basique. Une API utilisant PHP 5, et un front-end utilisant VueJS. 

L'API utilise une base de données sqlite en local sur le serveur EC2 actuellement, mais est compatible avec Mysql, Postgres, ou DynamoDB. Cette base de données permet uniquement de stocker des informations sur les comptes utilisateurs, et les differents produits en vente sur le site. 

Dans le cadre du projet d'amelioration du site, une feature de tracking des actions va etre mise en place

L'api est aussi disponible sous forme d'une image docker, mais celle-ci n'est pas encore utilisée.


#### Quel serait ton choix d'architecture pour ce projet d'amelioration des performances ?
```
Attentes: une description de la nouvelle architecture, la plus complete possible. Le projet est une simple modernisation de l'architecture. L'utilisation de services AWS est privilegiée. Un shemas est aussi possible.



```

#### Quel serait ton choix de technologie pour stocker les futures données de tracking ?
```

```

####  Quel serait ta solution de CI/CD idéale pour automatiser les deploiements de cette nouvelle infrastructure (Coté applicatif) ?
```

```