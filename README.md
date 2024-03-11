# Deploy Botpress Server Community Helm Charts on Red Hat OpenShift Dedicated
<p align="left">
El propósito de este proyecto consiste en generar los objetos kubernetes en base a la imagen del nodo del repositorio oficial [botpress](https://botpress.com) para el despliegue sobre las plataformas de contenedores por medio Helm Charts.

Se verifico el funcionamiento en [Sandbox RedHat OpenShift Dedicated](https://developers.redhat.com/developer-sandbox) (Openshift 4.14.1). 

<img src="https://img.shields.io/badge/redhat-CC0000?style=for-the-badge&logo=redhat&logoColor=white" alt="Redhat">
<img src="https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white" alt="kubernetes">
<img src="https://img.shields.io/badge/docker-0db7ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="shell">
<a href="https://www.linkedin.com/in/maximiliano-gregorio-pizarro-consultor-it"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin">   
</p>



<p align="left">
  <img src="https://raw.githubusercontent.com/maximilianoPizarro/botpress-server-v12/master/examples/image/botpress-helm.PNG" width="684" title="Run On Openshift">
</p>
<p align="left">
  <img src="https://github.com/maximilianoPizarro/botpress-server-v12/blob/master/examples/image/Captura7.PNG?raw=true" width="684" title="Run On Openshift">
  <img src="https://github.com/maximilianoPizarro/botpress-server-v12/blob/master/examples/image/Captura8.PNG?raw=true" width="684" title="Run On Openshift">  
</p>  

<p>
## Install

1. Run helm install command from web terminal on Red Hat OpenShift Dedicated

```bash
helm install botpress-server .
```

2. Package
```bash
 helm package . -d charts/
 helm repo index charts/
```


## Uninstall

```bash
helm uninstall botpress-server
```

</p>
