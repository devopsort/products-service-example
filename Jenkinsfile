node ("master") {
    // Checkout custom Jenkinsfiles
    stage ("Checkout pipelines") {
        git url: "git@github.com:devopsort/Pipelines.git", 
            branch: "main", 
            credentialsId: "products-git"
    }

    load "products-service-example/Jenkinsfile-${env.BRANCH_NAME}".stages()
}