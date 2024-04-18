<h1>Déploiement d'un cluster Kafka sur kubernetes avec STRIMZI</h1>

 Dans un premier, on installe l'opérateur Strimzi, qui a un manifeste préconfiguré pour Kafka, en utilisant helm : 

 <code>helm repo add strimzi https://strimzi.io/charts</code>

 <code>helm repo update</code>

 <code>helm install strimzi strimzi/strimzi-kafka-operator</code>


 <h2>Déployer à présent le cluster Kafka dans kubernetes</h2>

 créer un fichier kafka.yml et y mettre le contenu du repository

 Enregistrer puis appliquer le fichier 

 <code>kubectl apply -f kafka.yml</code>

 Vérifier que tous les pods sont en mode running avec la commande : 
 <code>kubectl get pod</code>

 Toujours grâce à strimzi, on peut créer le manifeste pour créer un topic : 
 <code>kubectl apply -f kafka-topic.yml</code


 <h2></h2>