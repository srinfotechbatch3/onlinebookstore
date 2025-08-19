node{

stage('clone'){

    git branch: 'feature/2025.08.14', url: 'https://github.com/srinfotechbatch3/onlinebookstore.git'
}
stage('Build'){

    bat 'mvn clean install'
}

stage('Test'){

    bat 'mvn test'
}

stage('Test results Reports'){

    junit 'target/surefire-reports/*.xml'
}

stage('Published Artifacts'){

    archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
}

stage('Deploy'){

    echo 'Deploy to Traget server'
}
}