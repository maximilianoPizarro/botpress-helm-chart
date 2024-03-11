# Deploy Botpress Server Community Helm Charts on Red Hat OpenShift
<p align="left">
<img src="https://img.shields.io/badge/redhat-CC0000?style=for-the-badge&logo=redhat&logoColor=white" alt="Redhat">
<img src="https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white" alt="kubernetes">
<img src="https://img.shields.io/badge/helm-0db7ed?style=for-the-badge&logo=helm&logoColor=white" alt="Helm">
<img src="https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="shell">
<a href="https://www.linkedin.com/in/maximiliano-gregorio-pizarro-consultor-it"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin" /></a>  
</p>

<p align="left">
  <img src="https://raw.githubusercontent.com/maximilianoPizarro/botpress-server-v12/master/examples/image/botpress-helm.PNG" width="900" title="Run On Openshift">
    <img src="https://raw.githubusercontent.com/maximilianoPizarro/botpress-server-v12/master/examples/image/botpress-helm-install.PNG" width="900" title="Run On Openshift">
</p>
<p align="left">
  <img src="https://github.com/maximilianoPizarro/botpress-server-v12/blob/master/examples/image/Captura7.PNG?raw=true" width="900" title="Run On Openshift">
  <img src="https://github.com/maximilianoPizarro/botpress-server-v12/blob/master/examples/image/Captura8.PNG?raw=true" width="900" title="Run On Openshift">  
</p>
<br>

El propósito de este proyecto consiste en generar los objetos kubernetes en base a la imagen del nodo del repositorio oficial <a href="https://botpress.com">botpress</a> para el despliegue sobre las plataformas de contenedores por medio de la estrategía Helm Charts.

Se verifico el funcionamiento en <a href="https://developers.redhat.com/developer-sandbox">Sandbox RedHat OpenShift Dedicated</a> (Openshift 4.14.1).
</p>

<table>
  <caption>
    Charts Values Parameters
  </caption>
  <thead>
    <tr>
      <th scope="col">Parameter</th>
      <th scope="col">Value</th>
      <th scope="col">Default</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">env.EXTERNAL_URL</th>
      <td>https://my-botpress-NAMESPACE-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com</td>
      <td>https://botpress-server-maximilianopizarro5-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com</td>
    </tr>
    <tr>
      <th scope="row">route.host</th>
      <td>my-botpress-NAMESPACE-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com</td>
      <td>botpress-server-maximilianopizarro5-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com</td>
    </tr>
    <tr>
      <th scope="row">image.repository</th>
      <td>botpress/server</td> <td>quay.io/maximilianopizarro/botpress-server-v12</td>
    </tr>
  </tbody>
</table>

<a> Add repository and Install</a>
<a href="https://maximilianopizarro.github.io/botpress-helm/">https://maximilianopizarro.github.io/botpress-helm/</a>
<p>
<ol>
 <li><b>helm repo add botpress https://maximilianopizarro.github.io/botpress-helm/</b></li>
 <li><b>helm install my-botpress botpress/botpress --version 0.1.0 --set route.host="Your-WilcardDNS-hostname",env.EXTERNAL_URL="Your-WilcardDNS-with-https"</b></li>
<li>Example: <b>helm install my-botpress botpress/botpress --version 0.1.0 --set route.host="my-botpress-maximilianopizarro5-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com",env.EXTERNAL_URL="https://my-botpress--maximilianopizarro5-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com"</b></li>
</ol>
<br>
<a> Uninstall </a>
<ol>
<li>helm uninstall botpress-server </li>
</ol>

<a> Package Info </a>

<a href="https://github.com/maximilianoPizarro/botpress-helm">https://github.com/maximilianoPizarro/botpress-helm</a>

<ol>
<li>helm package . -d . </li>
<li>helm repo index .</li>
</ol>




