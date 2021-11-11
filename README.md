# git-project-Boccace
This repository hosts all the documents, including scans of the sources, transcriptions, bibliographical references and introduction that serve the team Boccace for the validation of the course "Bonnes pratiques du developpement collaboratif : initiation à Git" (prof. Thibault Clérice), of the first semester - Master Humanités Numériques ENC-PSL 2021-2022. At the same time the project is indirectly linked to ++++

The work: Treatise on mythology. - First version composed between 1347 and 1360 at the request of Hugues IV de Lusignan, then revised and enlarged after his death in 1359. Its textual tradition is particular as it comes down to us in two different versions,[cf. +++]

The database for the project Boccace has been built with eScriptorium (http://traces6.paris.inria.fr), an interface for HTR ground truth production whose base is the system kraken (http://kraken.re/master/index.html), and, an HTR and layout segmentation engine. The output of the transcribed text are in ALTO XML. As for now it is composed of two documents:
     1. A Middle French incunabulum, namely BnF Rés. J-845 (département Réserve des livres rares, Rés. J-845) written between 1498-1499,scanned in high definition in black and white (notice http://ark.bnf.fr/ark:/12148/cb30116914c).
     2. The editio princeps of the work, namely Bibliothèque Mazarine Inc. 59 (notice https://www.sudoc.fr/135345618) scanned in high definition in color.
     
Both documents present for the most part coherent and regular writting which makes it easier to segment the text and train a machine to automatically transcribe the content.
We decided to transcribe the first chapter of the work with its proper introduction, since the genral introduction and the "table of contents" is not included in the Middle French version. The chapter corresponds to feuillet i-iii (6 pages in total) for BnF Rés. J-845, and respectiveley to folio 14v-17r (pagination marks on the top right of each bifolio) for Bibliothèque Mazarine Inc. 59 (5 1/2 pages in total) which makes a good balance ratio between latin and french text. The French texts is odered in two columns for each page and include drawings whereas the latin text is continuous ordered in paragraphs without drawings.

 
Principles of standardisation of the transcriptions
+++

https://github.com/HTR-United/cremma-medieval/blob/main/table.csv#L156 We chose a graphemic transcription method, following D. Stutzmann definitions (see bibliography), to have a sign in the image corresponding to a sign in our text: all the abbreviations are kept, and u/v or i/j are not distinguished. The spaces in the dataset are not homogeneously represented, sometimes transcriptions reproduce the manuscript spacing while others use lexical spaces.

+++++++

Choices of transcription were made. They're all summed up in a document available in the repository. It goes by the name "Transcription_norms". 

How do we ensure our quality of data (continuous integration workflow via Github Actions)

We can add bibliography here instead of a separate odt file.
