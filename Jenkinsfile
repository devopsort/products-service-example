node ("master") {
    // Checkout custom Jenkinsfiles
    stage ("Checkout pipelines") {
        git url: "https://github.com/devopsort/Pipelines.git", 
            branch: "main", 
            credentialsId: "products-git"
    }

    load ("products-service-example/Jenkinsfile-products.groovy")
}