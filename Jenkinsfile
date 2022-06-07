node ('MASTER'){
    stage('scm'){
        git 'https://github.com/DurgaKd/openmrs-core.git'
    }
    stage('build'){
        sh 'mvn package'
    }
    stage('postbuild'){
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}