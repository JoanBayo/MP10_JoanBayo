<h1 align=center>MySQL</h1>
<h3>Aquesta pràctica consisteix amb la instal·lació del sistema gestor de base de dades MySQL, per aconseguir això en aquest document mostrarem com fer-ho pas a pas:</h3>


<p>Primer comencem amb la instal·lació del MySQL server, per fer això requerirm de l'ús de la comanda <b>sudo apt-get install mysql-server</b> (en cas de que no us vagi feu primer un <b>sudo apt update</b>)</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167886989-70218741-dd81-4479-a067-7f012c2d85b4.png>
<p/>

<p>Després posarem mysql en el terminal i com és normal no ens deixa accedir amb el nostre usuari, anem a canviar això!</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167886854-26be46d2-b33d-43a7-9f24-70acc623ec57.png>
</p>

<p>Primer farem una cerca del port de MySQL per fer això necessitarem <b>nmap</b> per obtenir-lo utilitzarem la comanda <b>apt-get install nmap</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167885932-38931a83-374f-4e0b-8b85-9410576e3f5c.png>
</p>

<p>Un cop instal·lat el nmap l’utilitzarem per trobar el port del MySQL, com podem veure és el 3307/tcp open mysql</p>

<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167887324-55a5cf7b-b00e-4eb3-b03c-1db9cf45bb28.png>
</p>
     
<p>Ara farem un <b>cat /etc/mysql/debian.cnf</b> podem veure un usuari anomenat debian-sys-maint amb la seva contrasenya U4iIzMATcuFlPfyg</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888005-0669b02e-4159-41c7-bd42-4e5933cc4552.png>
</p>
     
<p>Obtenim aquesta contrasenya i gràcies aquesta informació  ja podem accedir al MySQL posan <b>mysql -p -u debian-sys-maint</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888440-e6ada027-bf1b-4a7c-b5a1-796096f56344.png>
</p>
     
<h3>Ara ja ens trobem dintre la base de dades de MySQL anem a provar algunes coses: </h3>
<p>Primer posem la comanda <b>SHOW DATABASE;</b> hi podem veure bases de dades creades pel propi sistema</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888631-b3cea920-2581-4292-88c8-bb4fc003bff3.png>
</p>
     
<p>Ara crearem una base de dades de la següent forma <b>CREATE DATABASE tasks;</b> tindrà el nom de tasks </p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888742-b8e19142-6bae-4f7d-9a81-61ea3750d0de.png>
</p>
<p>Tornem a posar <b>SHOW DATABASE</b> i comprovem que ja està creada</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888801-2eefcc63-bd51-4959-b424-c2ddb7022ffe.png
</p>     
<p>Amb la comanda <b>USE tasks</b> comencem a treballar amb tasks</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167888878-a7a7ee72-a803-48ff-9b4d-d7cfd2e499aa.png>
</p>     
<p>Ara procedirem a crear taules dintre de dintre de tasks posan <b>CREATE TABLE tasks (descripion text, completed boolean);</b> i comprovem la seva creació amb un <b>SHOW tables;</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167889018-b1fea6c0-cf02-4976-912e-f00d69ef51b5.png>
</p>     
<p>Ara procedirem a descarregar MySQL Workbench, per fer això accedim a MySQL community downloads en el nostre buscador i en l'apartat de MySQL Workbench</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167889088-bffdcc98-ffa8-482f-b8d2-d5104c307cd6.png>
</p>
     
<p>Quan ens trobem dins descarreguem el següent fitxer</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167897817-ed2d827e-94e4-4c81-9891-4b9d71361cba.png>
</p>

<p>Situats al terminal ens desplacem al directori Baixades i comprovem la existencia del paquet descarregat amb un <b>ls | grep mysql</b></p>  
<p>Amb <b>dpkg -i + “ElPaquetDescarregat”</b> l'instal·lem:</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167898053-a330a114-689f-4bf1-8a2a-c16b2f31d4b0.png)>
</p>     
<p>Abans d'instal·lar-lo necessitem el mysql-workbench-community i procedim a instalarlo amb <b>mysql-workbench-community</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167898249-081a9aa1-d091-4f0a-9667-77af436dd1be.png>
</p>     
<p>Ens dona un error i primerament instal·lem <b>apt --fix-broken install</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167898534-a82f3e82-82fb-4586-a216-4806d0e7385d.png>
</p>     
<p>Per acabar fiquem la següent comanda per acabar de instalar-ho tot <b>sudo apt-get install libopengl0 libpcrecpp0v5 libproj15 libzip5</b></p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167898675-5060afd7-4945-48a5-8e20-f4ebe9395a08.png>
<img src=https://user-images.githubusercontent.com/91154202/167898889-91553409-e9af-49f3-b6ac-63f792abd854.png>
</p>     
<p>Un cop solucionat tots els problemes i instal·lar-ho tot passem al següent pas:</p>  
<p>Posem la comanda <b>/usr/bin/mysql-workbench</b> per tal de executar el workbench i obrir la següent pestanya: </p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167898978-1acdda55-6b18-456f-9c28-c1dac7e09108.png>
</p>     
<p>No ens deixa accedir ja que l’usuari no és el correcte, per tal de soluciona-ho, editem la connexió posant l’usuari i la contrasenya adequats, i son els que hem vist en apartats anteriors</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167899066-2f5474ad-3a6f-45ad-9669-6c05578b7f81.png>
</p>   
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167899494-94a1667e-2417-4aba-b408-7ef9648f98a9.png>
</p>   
<p>Un cop solucionat aquest problema obrim i trobem la base de dades creada, i al fer click sobre ella i escrivim <b>SELECT * FROM tasks.tasks</b> mostra el següent text, demostran que esta buida: </p>  
database</p>
<p align=center>
<img align=center src=https://user-images.githubusercontent.com/91154202/167899857-c5f9a1a3-3396-4648-8cc0-ea3cc69ef716.png>
</p>   
<p>Ara procedirem a instalar el PhpSorm amb el toolbox i crear un nou projecte i accedim a l’apartat de database</p>
<p align=center>
<img align=center src=
</p>     
<p>Allí coma seguim la següent ruta DataSource/MySQL i la següent pestanya la qual és el configurador de MySQL</p>
<p align=center>
<img align=center src=
</p>    
<p>Com és veu en la parti inferior de l’anterior imatge ens falten drivers, procedim a instalar-los amb la següent comanda <b>sudo apt-get install php7.4-mysql</b></p>
<p align=center>
<img align=center src=
</p>     
<p>Tornem al Php i on posa user i password posem l’usuari i la contrasenya que hem trobat anteriorment i fem clic al botó de apply</p>
<p align=center>
<img align=center src=
</p>    
<p>Aquí veiem com se’ns té que mostra actualment el Php</p>
<p align=center>
<img align=center src=
</p>     
<p>Afgim la primera tasca amb clic dret i Add now, quan ja l'hem afegit fem clic en la fletxa verda per penjar-ho al servidor</p>
<p align=center>
<img align=center src=
</p>     
<p>Tornem al workbench i fent clic en el botó del llamp i podem veure com es mostra la taula creada al PhpStorm</p>
<p align=center>
<img align=center src=
</p>    
<p>Una altra forma de veure com s’ha creat es amb un <b>SELECT*FROM tasks</b> dintre del MySQL</p>
<p align=center>
<img align=center src=
</p>     
<p>Obrim un altre terminal i accedim a la carpeta Code i posteriorment al directori personal allí creen una carpeta anomenada PHP_PDO</p>
<p align=center>
<img align=center src=
</p>    
<p>Tornem al Toolbox, settings, i activem la opció de <b>Generate shell scripts</b> i també fem clic en change</p>
<p align=center>
<img align=center src=
</p>
<p>Allí crem una carpeta anomenada phpstorm de d’aquesta forma, ens surt el direcotri on es guarda i fem clic en apply</p>
<p align=center>
<img align=center src=
</p>  
<p>Accedim a la carpeta mitjançant el terminal i fem un ls i podem veure els següents executables</p>
<p align=center>
<img align=center src=
</p>   
<p>Accedim a la carpeta de phpstorm i amb <b>joe ***/.zshrc</b> obrim l’editor i escrivim la ruta en la que es trova la carpeta phpstorm</p>
<p align=center>
<img align=center src=
</p>   
<p>Tornem a la carpeta PHP_PDO i executem <b>phpstorm .</b></p>
<p align=center>
<img align=center src=
</p>  
<p>Automàticament quan entrem al phpstorm ens apareix una carpeta per obrir el PHP_PDO, l’obrim i creem un fitxer anomenat index.php </p>
<p align=center>
<img align=center src=
</p>
<p>Dintre del fitxer creat escrivim el següent</p>
<p align=center>
<img align=center src=
</p>    
<p>Torno al terminal a la carpeta de PHP_PDO allí amb un ls ens mostra l'índex creat, llavors si fem <b>php index.php</b> ens mostra el text escrit</p>
<p align=center>
<img align=center src=
</p> 
<p>Si es vol es pot fer que ho retorni al servidor amb <b>-S localhost:8095 index.php</b></p>
<p align=center>
<img align=center src=
</p>
<p>Per fer ho millor generar un codi més consisten en el index.php</p>
<p align=center>
<img align=center src=
</p>
     
<p>Generem el fitxer task.php creant-lo amb aquest petit fragment de codi</p>
<p align=center>
<img align=center src=
     
<p>I tornem al terminal i tornem a executar  <b>php index.php</b>Per a que ens retorni el següent codi: </p>
<p align=center>
<img align=center src=
