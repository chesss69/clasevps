<h1 align="center"><strong>Recursos Para VPS</strong></h1>
<u>
  <li><a target="_blank" href="https://learn.microsoft.com/es-es/windows/wsl/install">Como instalar WSL en windows</a></li>
  <li><a target="_blank" href="https://apps.microsoft.com/detail/9pn20msr04dw?hl=es-ar&gl=AR">Ubuntu 22.4.5 WSL</a></li>
  <li>
    <strong>Configuraciones iniciales de Ubuntu</strong>
    <ul>
      <li>Actualizar los paquetes del sistema:
        <pre><code>sudo apt update && sudo apt upgrade</code></pre>
      </li>
      <li>Crear la contraseña para usuario ROOT:
        <pre><code>sudo passwd root</code></pre>
      </li>
      <li>Usar la terminal como root (opcional):
        <pre><code>su -</code></pre>
      </li>
      <li>Configurar el firewall:
        <pre><code>sudo ufw enable</code></pre>
      </li>
    </ul>
  </li>
  <li><a target="_blank" href="https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-22-04">INSTALAR NGINX</a></li>
  <li><a target="_blank" href="https://www.digitalocean.com/community/tutorials/how-to-install-mariadb-on-ubuntu-22-04">INSTALAR MARIADB</a></li>
  <li>
    <strong>Habilitar acceso remoto Mariadb</strong>
    <ul>
      <li>Agregar el puerto 3306 al firewall:
        <pre><code>sudo ufw allow 3306</code></pre>
      </li>
      <li>Reiniciar el firewall:
        <pre><code>sudo ufw reload</code></pre>
      </li>
      <li>Editar Configuracion de MARIADB:
        <pre><code>sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf</code></pre>
      </li>
      <li>Buscar la lines bind-address y modificarla:
        <pre><code>bind-address = 0.0.0.0</code></pre>
      </li>
      <li>Reiniciar el servicio de MariaDB:
        <pre><code>sudo systemctl restart mariadb</code></pre>
      </li>
    </ul>
  </li>
  <li>
    <strong>Instalar Php y sus extensiones</strong>
    <ul>
      <li>Instalar Software Properties common:
        <pre><code>sudo apt install software-properties-common</code></pre>
      </li>
      <li>Agregar el repositorio:
        <pre><code>sudo add-apt-repository ppa:ondrej/php</code></pre>
        <pre><code>sudo apt update</code></pre>
      </li>
      <li>Instalar el core de php:
        <pre><code>sudo apt install php8.2 php8.2-cli php8.2-fpm</code></pre>
      </li>
      <li>Instalar extensiones de php:
        <pre><code>sudo apt install php-mysql php-mbstring php-xml php-bcmath php-curl</code></pre>
        <pre><code>sudo apt-get install php8.2-xml</code></pre>
      </li>
    </ul>
  </li>
  <ul>
    <li>Dar permisos a las carpetas del proyecto que van a crear o modificar archivos:
      <pre><code>sudo chown -R www-data:www-data /var/www/tuproyecto/storage</code></pre>
      <pre><code>sudo chown -R www-data:www-data /var/www/tuproyecto/bootstrap/cache</code></pre>
    </li>
  </ul>
  
</u>
