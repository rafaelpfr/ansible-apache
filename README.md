# Automating the Deploy of a Web Page in Apache with Ansible

## The master and managed nodes run CentOS 7 and the Ansible playbook for this project is divided into the following 3 plays:

* The tasks in the first play install and start apache on the managed node, copy to it the index file used for the website and start and configure firewalld to allow http connections.

<p align="center">
  <img src="images/play1.png"/>
</p>

* The second play tests if the page provided by Apache is available. If not, something went wrong and the playbook is interrupted.

<p align="center">
  <img src="images/play2.png"/>
</p>

<p align="center">
  <img src="images/page.png"/>
</p>

* The third play uninstalls Apache, removes the website index file and configures firewalld to refuse http connections again.

<p align="center">
  <img src="images/play3.png"/>
</p>
