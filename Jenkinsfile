node ("master") {
    // sondea el repositorio cada 2 minutos para ver los cambios
    pollSCM('*/2 * * * *')
    // Checkout custom Jenkinsfiles
    stage ("Checkout pipelines") {
        git url: "git@github.com:devopsort/Pipelines.git", 
            branch: "Prod", 
            credentialsId: "products-git"
    }

    load "products-service-example/Jenkinsfile-${env.BRANCH_NAME}".stages()
}