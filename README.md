# Pinterest-Photo-Downloader
This script is able to download all photos from a Pinterest Board


# Instructions

1. andare sulla pagina pinterest desiderata (i.e. a specific board to download) e zoommare al minimo la pagina cosi che pinterest carichi la maggior parte delle foto

2. premere Ctrl + Shift + C ed indivuare l'elemento <div></div> che contiene tutte le foto

3. copiare l'elemento <div></div> 
	( se si preferisce si può espandere ricorsivamente tale elemento per controllare il suo interno)

4. copiare tale elemento in un file (i.e. div_content)

5. creare una cartella nella quale salvare le immagini (i.e. Images): 
	<code> mkdir Images </code>

6. eseguire il seguente comando: 
	<code> cat div_content | sed 's/ /\n/g' | grep originals > Images/images </code>

7. spostarsi nella cartella Images:
	<code> cd Images </code>

8. eseguire il seguente comando:
	<code>  wget -i images </code>

9. aspettare che le immagini si scarichino!
