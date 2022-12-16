<h1>Micro-services avec Spring Cloud</h1>

<h3>I. Architecture du projet</h3>
<img src="screens/architectureduprojet.jpg">

<h3>II. Création du service Customer</h3>
     La création ce micro-service comporte :
     <h4>1. l'entité Customer : élément qui sera géré par le micro-service,
     on y définit ses attributs notamment son id, son nom et son email</h4>
     <h4>2. l'interface CustomerRepository : elle permet l'accès aux données</h4>
     <h4>3. l'alimentation de la couche Application de démarrage  : contient des données insérées manuellement</h4>
     <h4>4. la configuration de l'application  : contient les propriétés nécessaires pour le démarrage de l'application</h4>
     <h4>5. une projection CustomerProjection de la classe Customer  : qui permet de récupérer des données précises et non l'intégralité</h4>
     <h4>Illustration de la base des données avec H2 Database</h4>
     <img src="screens/customer-db.jpg">
     <h4>Résultat du micro-service Customer-service avec le navigateur Google Chrome</h4>
     <img src="screens/customer-result.jpg">
     Il y a récupération de toutes les données : l'id, le nom et l'email
     <h4>Résultat de la projection CustomerProjection du micro-service Customer-service</h4>
     <img src="screens/Customer-projection.jpg">
     Il y a récupération de données mais exclusivement celles spécifiées dans le code : l'id et le nom

<h3>III. Création du service Inventory</h3>
     La création ce micro-service comporte :
     <h4>1. l'entité Product : élément qui sera géré par le micro-service,
     on y définit ses attributs notamment son id, son nom, son prix et sa quantité</h4>
     <h4>2. l'interface ProductRepository : elle permet l'accès aux données</h4>
     <h4>3. l'alimentation de la couche Application de démarrage  : contient des données insérées manuellement</h4>
     <h4>4. la configuration de l'application  : contient les propriétés nécessaires pour le démarrage de l'application</h4>
     <h4>Illustration de la base des données avec H2 Database</h4>
     <img src="screens/product-db.jpg">
     <h4>Résultat du micro-service Inventory-service avec le navigateur Google Chrome</h4>
     <img src="screens/product-result.jpg">
     Il y a récupération de toutes les données : l'id, le nom, le prix et la quantité


<h3>IV. Création de la gateway Spring Cloud</h3>
     <img src="screens/gateway.jpg">


<h3>V. Création du service Eureka Discovery</h3>
     <h4>La notation @EnableEurekaServer permet d'activer le service Discovery</h4>
     <img src="screens/eureka.jpg">
     <h4>Disponibilités des micro-servicesv ia Eureka Discovery</h4>
     <img src="screens/discovery.jpg">
     <h4>Résultat du micro-service Customer-service via la Gateway</h4>
     <img src="screens/customer-gateway.jpg">
     <h4>Résultat du micro-service Inventory-service via la Gateway</h4>
     <img src="screens/inventory-gateway.jpg">

<h3>VI. Configuration dynamique des routes de la gateway</h3>
     <img src="screens/gateway-configuration.jpg">

<h3>VII. Création du service Billing</h3>
     <h4>Voici comment se présentent les intéractions entre les différentes classes et tables</h4>
     <img src="screens/diagrammeDeClasseServices.jpg">
     <h4>Base de données bill-db</h4>
     <img src="screens/billdb1.jpg">
     <img src="screens/billdb2.jpg">
     <h4>Résultat du micro-service Billing-service</h4>
     <img src="screens/customerBill.jpg">
     Ici, on aperçoit une facture d'un client avec les différents produits achétés
     <h4>Résultat du micro-service Billing-service</h4>
     <img src="screens/billSet.jpg">
     On aperçoit l'ensemble des factures des tous les clients



<h3>VIII. Création d'un Client Web Angular</h3>
     <h4>Illustration du client Web Angular Product</h4>
     <img src="screens/clientProduct.jpg">
     <h4>Illustration du client Web Angular Customer</h4>
     <img src="screens/clientCustomer.jpg">


<h3>IX. Déploiement du service d'authentification et d'autorisation Keycloak</h3>



<h3>X. Sécurisation des micro-services Back-end et Front-end</h3>



<h3>XI. Fonctionnalité additionnelle</h3>




<h3>XI. Explications des différentes annotations dans le projet</h3>