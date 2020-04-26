# Tema-2-SSC-IBM-Watson




WEB CRAWLER



  Date de identificare
Nume student: Olarescu Stefan <br>
Universitatea: Politehnica Bucuresti
Facultatea: Automatica si Calculatoare
Anul de studii, grupa: anul 4, 342 A3 


 Descrierea aplicaţiei

Motivaţie alegere tema: 
 Am ales aceasta tema din necesitatea de a verifica preturile unor produse cu un interes ridicat de pe anumite magazine online.

Utilitatea aplicaţiei: 
 Analiza pe timp indelungat a unor produse din cadrul unor magazine online.

Servicii, tehnologii folosite: 
 IBM Watson Studio, Jupyter Notebook, Cloud Object Storage ( 2 Buckets), Connections from IBM Watson Studio, Jobs


Descrierea aplicaţiei şi modul de utilizare:

    
  Aplicatia este scrisa in Python si foloseste libraria Beautiful Soup ce are rolul de a analiza si extrage documente de tip HTML si XML. O alta librarie utilizata este Pandas ce am utilizat-o pentru a crea un dataframe, un tabel ce poate fi exportat drept CSV si XLSX (Excel).
  Initial am luat url-urile produselor care m-au interesat si le-am pus in niste variabile, urmatorul pas a fost sa ma folosesc de libraria requests si de metoda get pentru a putea prelua datele transmise de catre server pe paginile respective. Am parsat datele folosind parserul de HTML astfel am putut sa preiau continutul fiecarei pagini. Utilizand inspect am putut sa verific div-ul in care se afla numele produsului si pretul produsului, facand astfel o parsare utilizand metoda find ce are rolul de a extrage doar informatia din interiorul div-ului. Am printat aceste valori si le am introdus intr-un tabel apoi am create un data frame pe care l-am exportat drept fisier cu extensia csv si xlsx. 
   Am creat o conexiune intre proiectul meu ce continue notebook si object storage-ul meu, mai exact cu un nou bucket creat de mine prin API key, ID-ul instantei si numele bucket-ului aceste notiuni putand fi gasite in sectiunea de.
(cloud-object-storage-so-display-data)
   In sectiunea Data assets se pot vizualiza fisiererele data.xlsx si data.csv.
 Pentru acest script am creat un job, un fel de proces ce se executa automat conform deciziilor utilizatorului si are rolul de a rula conform frecventei dorite. Job-ul se executa o data pe saptamana in ziua de duminica iar informatiile sunt salvate in cloud object storage.  Putem intra sa vedem noile tabele pentru a ne forma o idee in legatura cu evolutia preturilor produselor dorite. Unde apare numele notebook-ului apare o iconita cu ceas pe coloana scheduled ce indica acest job.
  Am integrat acest proiect cu GitHub folosind un token de access generat si un secret pentru a mentine o conexiune sigura intre platforma de IBM Watson si  Repository-ul de pe GitHub.

  Aceasta aplicatie este in esenta un WEB CRAWLER, adica are la baza un script ce cauta diferite date de pe anumite site-uri pentru analiza si extractie de date utilizand anumite librarii si metode 
foarte bine definite. Aplicatia mea are in vedere cateva produse de pe anumite site-uri si salveaza numele si pretul acestora pentru a avea o anumita intelegere asupra evolutiei preturilor si a putea lua decizii privind cumpararea unui produs. 

In crearea acestui proiect am urmarit urmatorii pasi:
-	Am create un proiect in Watson Studio
-	Am create un notebook ( Similar cu Jupyter Notebook ce are rolul de a parcurge aplicatia creata pas cu pas folosind limbajul Python ultima versiune)
-	Am creat o baza de date (cloud-object-storage-so) in care voi avea salvate diferitele versiuni ale aplicatiei dar si datele extrase
-	Am creat un script in Python
-	Am rulat scriptul
-	Am adaugat un job ce are rolul de a executa script-ul o data pe saptamana
-	Aceste date sunt salvate in baza de date intr-un nou bucket create (data.csv, data.xlsl)
-	Putem vedea aceste tabele din Watson Studio (Data Assets)
