node('test')
{
    stage('scm-checkout')
{
    git credentialsId: '9e43eb0e-ee2a-4f93-afec-2a22218fb6d5', url: 'https://github.com/parthsarathi11/MavenProject.git'
}
stage('build')
{
    sh "mvn clean package"
}
stage('deploy')
{
    sh "cp -f $WORKSPACE/target/project.war /opt/tomcat/webapps/project.war"
}
}
