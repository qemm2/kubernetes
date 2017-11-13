node {
//
 def project = 'https://github.com/qemm2/kubernetes'
 def imageTag = "https://github.com/qemm2/kubernetes.git"
checkout scm
sh("kubectl get ns ${env.BRANCH_NAME} || kubectl create ns ${env.BRANCH_NAME}")
 stage 'Sonar'
//sh ("cd /opt/lamp/dockerfiles/myapp-php && sudo docker build -t myapp-php .")

//sh ("cd /opt/lamp/dockerfiles/myapp-php && sudo docker build -t myapp-apache .")
// stage 'Run'
///sh ("kubectl create --namespace=staging -f mariadb-controller.yml")
//sh ("kubectl create --namespace=staging -f mariadb-service.yml")
//sh ("kubectl delete secrets myapp-secrets")
//stage 'Create secrets'
//sh ("base64 -w128 <<< \"secretpassword\"")
//sh ("kubectl create -f myapp-secrets.yml")
//sh ("kubectl create --namespace=staging -f myapp-controller.yml")
///sh ("kubectl create --namespace=staging -f myapp-service.yml")
//stage 'Myapp service review'
//sh ("kubectl get services myapp-php")
//sh ("kubectl create --namespace=staging -f apache-controller.yml")
//sh ("kubectl create --namespace=staging -f apache-service.yml")



 switch (env.BRANCH_NAME) {
   case "pre2":
	sh ("cd /opt/lamp/dockerfiles/myapp-php && sudo /var/lib/jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonar-scanner/bin/sonar-scanner")


}
//   // Roll out to production
//   case "master":
//       // Change deployed image in staging to the one we just built
//       sh("kubectl --namespace=production apply -f k8s/services/")
//       sh("kubectl --namespace=production apply -f k8s/production/")
//       sh("echo http://`kubectl --namespace=production get service/${feSvcName} --output=json | jq -r '.status.loadBalancer.ingress[0].ip'` > ${feSvcName}")
//       break

//   // Roll out a dev environment
//   default:
//       // Create namespace if it doesn't exist
//       sh("kubectl get ns ${env.BRANCH_NAME} || kubectl create ns ${env.BRANCH_NAME}")
//       // Don't use public load balancing for development branches
//      // sh("sed -i.bak 's#LoadBalancer#ClusterIP#' ./k8s/services/frontend.yaml")
//       ((sh("sed -i.bak 's#gcr.io/cloud-solutions-images/gceme:1.0.0#${imageTag}#' ./k8s/dev/*.yaml")
//       sh("kubectl --namespace=${env.BRANCH_NAME} apply -f k8s/services/")
//       sh("kubectl --namespace=${env.BRANCH_NAME} apply -f k8s/dev/")
//       echo 'To access your environment run `kubectl proxy`'
//       echo "Then access your service via http://localhost:8001/api/v1/proxy/namespaces/${env.BRANCH_NAME}/services/${feSvcName}:80/"
//}
}
