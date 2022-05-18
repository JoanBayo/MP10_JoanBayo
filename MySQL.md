<h1 align=center>MySQL</h1>
<h3>Aquesta pràctica consisteix amb la instal·lació del sistema gestor de base de dades MySQL, per aconseguir això en aquest document mostrarem com fer-ho pas a pas:</h3>


<p>Primer comencem amb la instal·lació del MySQL server, per fer això requerirm de l'ús de la comanda <b>sudo apt-get install mysql-server</b> (en cas de que no us vagi feu primer un <b>sudo apt update</b>)</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167886989-70218741-dd81-4479-a067-7f012c2d85b4.png>
<p/>

<p>Després posarem mysql en el terminal i com és normal no ens deixa accedir amb el nostre usuari, anem a canviar això!</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167886854-26be46d2-b33d-43a7-9f24-70acc623ec57.png>
</p>

<p>Primer farem una cerca del port de MySQL per fer això necessitarem <b>nmap</b> per obtenir-lo utilitzarem la comanda <b>apt-get install nmap</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167885932-38931a83-374f-4e0b-8b85-9410576e3f5c.png>
</p>

<p>Un cop instal·lat el nmap l’utilitzarem per trobar el port del MySQL, com podem veure és el 3306/tcp open mysql</p>

<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167887324-55a5cf7b-b00e-4eb3-b03c-1db9cf45bb28.png>
</p>
     
<p>Ara farem un <b>cat /etc/mysql/debian.cnf</b> podem veure un usuari anomenat debian-sys-maint amb la seva contrasenya U4iIzMATcuFlPfyg</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888005-0669b02e-4159-41c7-bd42-4e5933cc4552.png>
</p>
     
<p>Obtenim aquesta contrasenya i gràcies aquesta informació  ja podem accedir al MySQL posan <b>mysql -p -u debian-sys-maint</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888440-e6ada027-bf1b-4a7c-b5a1-796096f56344.png>
</p>
     
<h3>Ara ja ens trobem dintre la base de dades de MySQL anem a provar algunes coses: </h3>
<p>Primer posem la comanda <b>SHOW DATABASE;</b> hi podem veure bases de dades creades pel propi sistema</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888631-b3cea920-2581-4292-88c8-bb4fc003bff3.png>
</p>
     
<p>Ara crearem una base de dades de la següent forma <b>CREATE DATABASE tasks;</b> tindrà el nom de tasks </p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888742-b8e19142-6bae-4f7d-9a81-61ea3750d0de.png>
</p>
<p>Tornem a posar <b>SHOW DATABASE</b> i comprovem que ja està creada</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888801-2eefcc63-bd51-4959-b424-c2ddb7022ffe.png
</p>     
<p>Amb la comanda <b>USE tasks</b> comencem a treballar amb tasks</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167888878-a7a7ee72-a803-48ff-9b4d-d7cfd2e499aa.png>
</p>     
<p>Ara procedirem a crear taules dintre de dintre de tasks posan <b>CREATE TABLE tasks (descripion text, completed boolean);</b> i comprovem la seva creació amb un <b>SHOW tables;</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167889018-b1fea6c0-cf02-4976-912e-f00d69ef51b5.png>
</p>     
<p>Ara procedirem a descarregar MySQL Workbench, per fer això accedim a MySQL community downloads en el nostre buscador i en l'apartat de MySQL Workbench</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167889088-bffdcc98-ffa8-482f-b8d2-d5104c307cd6.png>
</p>
     
<p>Quan ens trobem dins descarreguem el següent fitxer</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167897817-ed2d827e-94e4-4c81-9891-4b9d71361cba.png>
</p>

<p>Situats al terminal ens desplacem al directori Baixades i comprovem la existencia del paquet descarregat amb un <b>ls | grep mysql</b></p>  
<p>Amb <b>dpkg -i + “ElPaquetDescarregat”</b> l'instal·lem:</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167898053-a330a114-689f-4bf1-8a2a-c16b2f31d4b0.png>
</p>     
<p>Abans d'instal·lar-lo necessitem el mysql-workbench-community i procedim a instalarlo amb <b>mysql-workbench-community</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167898249-081a9aa1-d091-4f0a-9667-77af436dd1be.png>
</p>     
<p>Ens dona un error i primerament instal·lem <b>apt --fix-broken install</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167898534-a82f3e82-82fb-4586-a216-4806d0e7385d.png>
</p>     
<p>Per acabar fiquem la següent comanda per acabar de instalar-ho tot <b>sudo apt-get install libopengl0 libpcrecpp0v5 libproj15 libzip5</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167898675-5060afd7-4945-48a5-8e20-f4ebe9395a08.png>
<img src=https://user-images.githubusercontent.com/91154202/167898889-91553409-e9af-49f3-b6ac-63f792abd854.png>
</p>     
<p>Un cop solucionat tots els problemes i instal·lar-ho tot passem al següent pas:</p>  
<p>Posem la comanda <b>/usr/bin/mysql-workbench</b> per tal de executar el workbench i obrir la següent pestanya: </p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167898978-1acdda55-6b18-456f-9c28-c1dac7e09108.png>
</p>     
<p>No ens deixa accedir ja que l’usuari no és el correcte, per tal de soluciona-ho, editem la connexió posant l’usuari i la contrasenya adequats, i son els que hem vist en apartats anteriors</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167899066-2f5474ad-3a6f-45ad-9669-6c05578b7f81.png>
</p>   
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167899494-94a1667e-2417-4aba-b408-7ef9648f98a9.png>
</p>   
<p>Un cop solucionat aquest problema obrim i trobem la base de dades creada, i al fer click sobre ella i escrivim <b>SELECT * FROM tasks.tasks</b> mostra el següent text, demostran que esta buida: </p>  
database</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167899857-c5f9a1a3-3396-4648-8cc0-ea3cc69ef716.png>
</p>   
<p>Ara procedirem a instalar el PhpSorm amb el toolbox i crear un nou projecte i accedim a l’apartat de database</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167901092-1f7837bc-e24b-469c-b7fa-2dad3a0b41a6.png>
</p>     
<p>Accedim a l'apartat que mostra la imatge i en aquesta pestanya que ens mostra és el configurador de MySQL</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167901850-52ac90c0-e0b9-4dbc-b1be-01fa4d0c259c.png>
</p>    
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167902199-e961da6d-06c3-4405-988a-2d9d338a45e5.png>
</p>         
<p>Com és veu en la parti inferior de l’anterior imatge ens falten drivers, procedim a instalar-los amb la següent comanda <b>sudo apt-get install php7.4-mysql</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167902471-8719152c-4a6a-41dd-9bce-23171b07aa9f.png>
</p>     
<p>Tornem al Php, a la pestanya de la imatge antrior i fem clic en download, posteriorment on posa user i password posem l’usuari i la contrasenya que hem trobat anteriorment, <b>també on fica database, posem tasks, importan ja que en la imatge no esta</b> i fem clic al botó de apply</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/168545821-8f84c2c5-929b-4db8-bc83-24083497daaf.png>
</p>    
<p>Aquí veiem com se’ns té que mostra actualment el Php</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/167905090-07d29654-5488-405d-aab0-72a1d11d9913.png>
</p>     
<p>Fem doble clic sobre taska, se'ns obrira una pestanya nova i allí afetgim la primera tasca fent clic dret i Add Row, quan ja l'hem afegit fem clic en la fletxa verda per penjar-ho al servidor</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169117059-82e546c0-9fc4-4b86-865b-527f7b54436c.png>
</p>     
<p>Tornem al workbench i fent clic en el botó del llamp ja podem veure com es mostra la taula creada al PhpStorm</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169117738-8072dbae-7256-42fb-92f5-da0bafd661c1.png>
</p>    
<p>Una altra forma de veure com s’ha creat es amb un <b>SELECT*FROM tasks</b> dintre del MySQL</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169117897-1c379d8c-ae31-42a2-9c04-2ff2857ac3e2.png>
</p>     
<p>Obrim un altre terminal i accedim a la carpeta Code i posteriorment al directori personal allí creem una carpeta anomenada PHP_PDO, comprovem que existeix accedin al seu interior</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169118127-092fe475-5d08-4558-85a6-52ec0eccf72c.png>
</p>    
<p>Obrim el Toolbox, settings, i activem la opció de <b>Generate shell scripts</b> que es trova dintre de Tools i fem clic en change</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169118543-75be8f46-50de-427d-886f-9c004fc87810.png>
</p>
<p>Se'ns obrira una nova pestanya i allí fem click en new folder per crear una nova carpeta la qual anomenarem phpstorm, la seleccionem en els Folders i finalment presionem  OK, tornem al Toolbox i fem clic en Apply</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169119606-a161caca-cf90-492e-9020-77efa6de84d7.png>
<img src=https://user-images.githubusercontent.com/91154202/169119903-2a8ec550-a32b-46e8-9382-8ac645399e0e.png>
</p>  
<p>Accedim a la carpeta mitjançant el terminal i fem un ls i podem veure els següents executables:</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169121087-f0915e26-ab01-4b92-a9a5-be6056a12dec.png>
</p>   
<p>Accedim a la carpeta de phpstorm i amb <b>joe ~/.zshrc</b> obrim l’editor i escrivim la ruta en la que es trova la carpeta phpstorm en la part inferior del fitxer</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169125354-e2a1a5b5-ac8d-4505-8a3f-1f9f29750ad4.png>
</p>  
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169125725-1b90ab52-f07c-41f3-8dc9-663057bfd2e6.png>
</p>   
<p>Tornem a la carpeta PHP_PDO i executem <b>phpstorm .</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169134626-6cf447ab-ba8e-41c3-986f-17e033bf663e.png>
</p>  
<p>Automàticament quan entrem al phpstorm ens apareix una carpeta per obrir el PHP_PDO, l’obrim i creem un fitxer anomenat <b>index.php</b> </p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169135926-2b75a95d-b8d6-4a85-bff8-b07489ad4be8.png>
</p>
<p>Dintre del fitxer creat escrivim el següent</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169137836-6102cb3e-df23-4d29-9596-8967bfd10343.png>
</p>    
<p>Torno al terminal a la carpeta de PHP_PDO allí amb un ls ens mostra l'índex creat, llavors si fem <b>php index.php</b> ens mostra el text escrit</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169137727-a602c0cf-bf70-4f58-ad79-361b252aed38.png>
</p> 

<p>Si es vol es pot fer que ho retorni al servidor amb <b>php -S localhost:3306 index.php</b>, quan executem aquesta comanda se'ns obrira un link al qual accedim fent Ctrl clic esquerre</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169138662-4f637c55-016d-4126-ad91-ef6b6ddaa72f.png>
</p>
<p>Per fer una altra prova generar un codi més consisten on escrivim la següent infomració:</p>
<p>Per una banda ficarem tot això en el index.php</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169143449-90ef098d-08fb-45ee-afb5-e0ed62312e2b.png>
</p>
<p>I per l'altra crarem un petit fitxer nou anomenat Task.php on introduirem aquesta classe per tal de poder completar de fomra correcta el index.php</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169143499-4ddda2c6-aa9e-4423-8f64-e9edb35f0907.png>
</p>
     
<p>I tornem al terminal i tornem a executar  <b>php index.php</b>Per a que ens retorni el següent codi: </p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169144856-33c95068-1a49-432b-afd4-06e58f05c005.png>
