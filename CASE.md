# Use case.

La société Mirow, qui héberge actuellement son site web chez AWS sur un seul serveur EC2 a de gros problèmes de montée en charge. Les soldes arrivants, l'équipe de devops doit changer l'architecture du site pour le rendre plus scalable.

Le site web de Mirow est basique. Une API utilisant PHP 5, et un front-end utilisant VueJS. 

L'API utilise une base de données sqlite en local sur le serveur EC2 actuellement, mais est compatible avec Mysql, Postgres, ou DynamoDB. Cette base de données permet uniquement de stocker des informations sur les comptes utilisateurs, et les différents produits en vente sur le site. 

Dans le cadre du projet d'amélioration du site, une feature de tracking des actions va être mise en place

L'api est aussi disponible sous forme d'une image docker, mais celle-ci n'est pas encore utilisée.


#### Quel serait ton choix d'architecture pour ce projet d'amelioration des performances ?
```
Attentes: une description de la nouvelle architecture, la plus complète possible. Le projet est une simple modernisation de l'architecture. 
L'utilisation de services AWS est privilégiée. Un schéma est aussi possible, ou un script terraform

```
I will try to explain as clear as possible with my knowledge.

First, We need to separate the database from the frontend. That means migrating it, let's choose DynamoDB as we are going to Amazon. 

Then, we need to dockerise the front end to be able to use ECS (as the API is already dockerised) (We can of course install Docker on a EC2 instance)

A load balancer will be required to increase the performances.

I made 2 schemes (one with EC2 and another with ECS, depending on the dockerisation of the app or not)

I will be honest and tell you that I'm new with Terraform so I only documented myself on how to use it, how to provision things so I tried directly with many trainings.

I did that using https://medium.com/avmconsulting-blog/how-to-deploy-a-dockerised-node-js-application-on-aws-ecs-with-terraform-3e6bceb48785

and 

https://medium.com/swlh/deploy-aws-lambda-and-dynamodb-using-terraform-6e04f62a3165

So I won't copy paste the code they provided on the trainings because it's clearly not mine but at least you have an idea of what I learnt and what I can do.

For the tracking feature, I don't know what to use.

```

#### Quel serait ton choix de technologie pour stocker les futures données de tracking ?
```
As mentioned above, I don't know what to use for the tracking feature, and I don't really know how sensitive the data can be so I cannot recommand something relevant.
```

####  Quel serait ta solution de CI/CD idéale pour automatiser les deploiements de cette nouvelle infrastructure (Coté applicatif) ?
```
I used to use Gitlab and it includes Gitlab CI so why not ?
```
