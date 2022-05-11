<h1 align=center>MySQL</h1>
<h3>Aquesta pràctica consisteix amb la instal·lació del sistema gestor de base de dades MySQL, per aconseguir això en aquest document mostrarem com fer-ho pas a pas:</h3>




<p>Primer comencem amb la instal·lació del MySQL server, per fer això requerirm de l'ús de la comanda <b>sudo apt-get install mysql,server</b> (en cas de que no us vagi feu primer un <b>sudo apt update</b>)</p>
<img align=center src=https://user-images.githubusercontent.com/91154202/167885932-38931a83-374f-4e0b-8b85-9410576e3f5c.png>
<p>Després posarem mysql en el terminal i com és normal no ens deixa accedir amb el nostre usuari, anem a canviar això!</p>
<img align=center src=https://user-images.githubusercontent.com/91154202/167886266-70ed5018-b6f6-4f99-b22e-ebcf7e45678e.png>

<p>Primer farem una cerca del port de MySQL per fer això necessitarem <b>nmap</b> per obtenir-lo utilitzarem la comanda <b>apt-get install nmap</b></p>
<p>Un cop instal·lat el nmap l’utilitzarem per trobar el port del MySQL, com podem veure és el *******</p>
<p>Ara farem un <b>cat /etc/mysql/debian.cnf</b> podem veure un usuari anomenat user amb la seva contrasenya *****************</p>
<p>Obtenim aquesta contrasenya i gràcies aquesta informació  ja podem accedir al MySQL posan <b>mysql -p -u ****************</b></p>
<h3>Ara ja ens trobem dintre la base de dades de MySQL anem a provar algunes coses: </h3>
<p>Primer posem la comanda <b>SHOW DATABASE</b> hi podem veure bases de dades creades pel propi sistema</p>
<p>Ara crearem una base de dades de la següent forma <b>CREATE DATABASE tasks;</b> tindrà el nom de tasks </p>
<p>Tornem a posar <b>SHOW DATABASE</b> i comprovem que ja està creada</p>
<p>Amb la comanda <b>USE tasks</b> comencem a treballar amb tasks</p>
<p>Ara procedirem a crear taules dintre de dintre de tasks posan <b>CREATE TABLE tasks (descripion text, completed boolean);</b> i comprovem la seva creació amb un <b>SHOW tables;</b></p>
<p>Ara procedirem a descarregar MySQL Workbench, per fer això accedim a MySQL community downloads en el nostre buscador i en l'apartat de MySQL Workbench</p>
<p>Quan ens trobem dins descarreguem el següent fitxer</p>
<p>Situats al terminal ens desplacem al directori Baixades i comprovem la existencia del paquet descarregat amb un <b>ls | grep mysql</b></p>
<p>Amb <b>dpkg -i + “ElPaquetDescarregat”</b> l'instal·lem:</p>
<p>Abans d'instal·lar-lo necessitem el mysql-workbench-community i procedim a instalarlo amb <b>mysql-workbench-community</b></p>
<p>Ens dona un error i primerament instal·lem <b>apt --fix-broken install</b></p>
<p>Per acabar fiquem la següent comanda per acabar de instalar-ho tot <b>sudo apt-get install libopengl0 libpcrecpp0v5 libproj15 libzip5</b></p>
<p>Un cop solucionat tots els problemes i instal·lar-ho tot passem al següent pas:</p>
<p>Posem la comanda <b>/usr/bin/mysql-workbench</b> per tal de executar el workbench i obrir la següent pestanya: </p>
<p>No ens deixa accedir ja que l’usuari no és el correcte, per tal de soluciona-ho, editem la connexió posant l’usuari i la contrasenya adequats, i son els que hem vist en apartats anteriors</p>
<p>Un cop solucionat aquest problema obrim i trobem la base de dades creada, i al fer click sobre ella es mostra el següent text: </p>
<p>Ara procedirem a instalar el PhpSorm amb el toolbox i crear un nou projecte i accedim a l’apartat de database</p>
<p>Allí coma seguim la següent ruta DataSource/MySQL i la següent pestanya la qual és el configurador de MySQL</p>
<p>Com és veu en la parti inferior de l’anterior imatge ens falten drivers, procedim a instalar-los amb la següent comanda <b>sudo apt-get install php7.4-mysql</b></p>
<p>Tornem al Php i on posa user i password posem l’usuari i la contrasenya que hem trobat anteriorment i fem clic al botó de apply</p>
<p>Aquí veiem com se’ns té que mostra actualment el Php</p>
<p>Afgim la primera tasca amb clic dret i Add now, quan ja l'hem afegit fem clic en la fletxa verda per penjar-ho al servidor</p>
<p>Tornem al workbench i fent clic en el botó del llamp i podem veure com es mostra la taula creada al PhpStorm</p>
<p>Una altra forma de veure com s’ha creat es amb un <b>SELECT*FROM tasks</b> dintre del MySQL</p>
<p>Obrim un altre terminal i accedim a la carpeta Code i posteriorment al directori personal allí creen una carpeta anomenada PHP_PDO</p>
<p>Tornem al Toolbox, settings, i activem la opció de <b>Generate shell scripts</b> i també fem clic en change</p>
<p>Allí crem una carpeta anomenada phpstorm de d’aquesta forma, ens surt el direcotri on es guarda i fem clic en apply</p>
<p>Accedim a la carpeta mitjançant el terminal i fem un ls i podem veure els següents executables</p>
<p>Accedim a la carpeta de phpstorm i amb <b>joe ***/.zshrc</b> obrim l’editor i escrivim la ruta en la que es trova la carpeta phpstorm</p>
<p>Tornem a la carpeta PHP_PDO i executem <b>phpstorm .</b></p>
<p>Automàticament quan entrem al phpstorm ens apareix una carpeta per obrir el PHP_PDO, l’obrim i creem un fitxer anomenat index.php </p>
<p>Dintre del fitxer creat escrivim el següent</p>
<p>Torno al terminal a la carpeta de PHP_PDO allí amb un ls ens mostra l'índex creat, llavors si fem <b>php index.php</b> ens mostra el text escrit</p>
<p>Si es vol es pot fer que ho retorni al servidor amb <b>-S localhost:8095 index.php</b></p>
<p>Per fer ho millor generar un codi més consisten en el index.php</p>
<p>Generem el fitxer task.php creant-lo amb aquest petit fragment de codi</p>
<p>I tornem al terminal i tornem a executar  <b>php index.php</b>Per a que ens retorni el següent codi: </p>

