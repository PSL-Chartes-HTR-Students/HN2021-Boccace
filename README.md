# git-project-Boccace
This repository hosts all the documents, including scans of the sources, transcriptions, bibliographical references and introduction that serve the team Boccace for the validation of the course "Bonnes pratiques du developpement collaboratif : initiation à Git" (prof. Thibault Clérice), of the first semester - Master Humanités Numériques ENC-PSL 2021-2022. At the same time the project is indirectly linked to  biannual project "Per un'edizione digitale della Genealogia deorum gentilium" di Boccaccio" (dir. F. Duval, M. Maulu). Financed in 2021, this project foresees to put on line in XML format the unpublished translation in Middle French entitled "De la genealogie des dieux".

The work: Treatise on mythology. Its first version composed between 1347 and 1360 at the request of Hugues IV de Lusignan, then revised and enlarged after his death in 1359. Its textual tradition is particular as in 1371 Boccaccio allowed a friend to make a copy of an autograph MS, now lost, of the Genealogia, and from that first apograph other copies were made. The text of the lost autograph is now called the Vulgate text[Wilkins_1919,65] which was widely diffused.

The database for the project Boccace has been built with eScriptorium (http://traces6.paris.inria.fr), an interface for HTR ground truth production whose base is the system kraken (http://kraken.re/master/index.html), and, an HTR and layout segmentation engine. The output of the transcribed text are in ALTO XML. As for now it is composed of two documents:
     1. A Middle French incunabulum, namely BnF Rés. J-845 (département Réserve des livres rares, Rés. J-845) written between 1498-1499,scanned in high definition in black and white (notice http://ark.bnf.fr/ark:/12148/cb30116914c).
     2. The editio princeps of the work, namely Bibliothèque Mazarine Inc. 59 (notice https://www.sudoc.fr/135345618) scanned in high definition in color.
     
     This edition contains, first, the Table of Rubrics; second, the Genealogia itself; third, the Alphabetical Index by Domenico Bandini; fourth, the Versus of Domenico di Silvestro. The printer did not undertake to reproduce the genealogical trees which stood presumably in the MS which served him as copy.The edition of 1472 is  the best printed representative of the Vulgate text of the Genealogia, and should be cited, in preference to the edition of 1532, for all portions of the Genealogia, except those printed by Hecker [Hecker_1902] from the autograph, and for any citation in which the reading of the Vulgate text as against that of the autograph is desired (More specifically, Hecker prints from the second autograph the Dedicatory Letter (but not the single chapter of the general Proem, nor the Proem of Book I), the Proems of Books II-XIII, and Books XIV and XV entire).
     
Both documents present for the most part coherent and regular writting which makes it easier to segment the text and train a machine to automatically transcribe the content.

We decided to begin the transcription of both works (approx. 25 pages for each), producing segmentation and trascription models in roder to facilitate the task.

 
Principles of standardisation of the transcriptions, namely transcription norms follow the general lines of the cremma- ledieval/HTR-United initiative guidelines https://github.com/HTR-United/cremma-medieval. More specifically,we chose a graphemic transcription method, to have a sign in the image corresponding to a sign in the text: all the abbreviations are kept, and u/v or i/j are not distinguished. The spaces in the dataset are not homogeneously represented, sometimes transcriptions reproduce the manuscript spacing while others use lexical spaces, especially for the BnF, Rés J-845 _incunabulum_. As per the special characters themselves, we follow the table created by cremma-medieval https://github.com/HTR-United/cremma-medieval/blob/main/table.csv#L156 and compliment where necessary with the public domain mufi characters https://mufi.info/m.php?p=mufi. A more detailed .tex file is included in the repository summing up the proceedure.

How do we ensure our quality of data / implementation of ChocoMufin for the characters. 

The structure of the repository isn't an original conception. We got inspired by the HTR-UNited and decided to present it following this disposition : 

- one folder containing all the data about the ancient french manuscript (BnF Rés. J-845)
- another concerning the latin version (Mazarine Inc59)
- a LaTeX synthesis of the research

Inside those main folders, we can find a similar structure. Both present three subfolders : 

- one for the segmentation and transcription models.
- one for the training corpus used to train the A.I. on escriptorium (documents are exclusively XML Alto with jpg and an odt containing the full text)
- one for the verification corpus.
