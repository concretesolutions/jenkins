# Esse Dockerfile é baseado no

Official Jenkins Docker image
The Jenkins Continuous Integration and Delivery server.
This is a fully functional Jenkins server, based on the Long Term Support release
http://jenkins-ci.org/
[Para mais informações...] (https://github.com/jenkinsci/docker/)

<img src="http://jenkins-ci.org/sites/default/files/jenkins_logo.png"/>

Acrescentamos ao Jenkins:
Git plugin

Acrescentamso a imagem:
AWS Cli
Acrescente um Role ao seu Container e dê as permissões necessárias através do IAM.
http://docs.aws.amazon.com/AmazonECS/latest/developerguide/instance_IAM_role.html

A variável de ambiente cibucket define o bucket utilizado para carregar os jobs salvos e credenciais iniciais de usuários.
Os jobs devem ficar em s3://$cibucket/jobs.

Os usuários devem ser salvos em s3://$cibucket/users, um job para salvar os usuários pode ser útil.
