# **Presenting the git-project-Boccace by the Boccace team**

This repository hosts all the documents, including scans of the sources, transcriptions, bibliographical references and introduction that serve the team Boccace for the validation of the course "Bonnes pratiques du developpement collaboratif : initiation à Git" (prof. Thibault Clérice), of the first semester - Master Humanités Numériques ENC-PSL 2021-2022. At the same time the project is indirectly linked to  biannual project "Per un'edizione digitale della Genealogia deorum gentilium" di Boccaccio" (dir. F. Duval, M. Maulu). Financed in 2021, this project foresees to put on line in XML format the unpublished translation in Middle French entitled "De la genealogie des dieux".

 # **Getting familiar with the database**

The work: Treatise on mythology. Its first version composed between 1347 and 1360 at the request of Hugues IV de Lusignan, then revised and enlarged after his death in 1359. Its textual tradition is particular as in 1371 Boccaccio allowed a friend to make a copy of an autograph MS, now lost, of the Genealogia, and from that first apograph other copies were made. The text of the lost autograph is now called the Vulgate text[Wilkins_1919,65] which was widely diffused.

The database for the project Boccace has been built with eScriptorium (http://traces6.paris.inria.fr), an interface for HTR ground truth production whose base is the system kraken (http://kraken.re/master/index.html), and, an HTR and layout segmentation engine. The output of the transcribed text are in ALTO XML. As for now it is composed of two documents:
     1. A Middle French incunabulum, namely BnF Rés. J-845 (département Réserve des livres rares, Rés. J-845) written between 1498-1499,scanned in high definition in black and white (notice http://ark.bnf.fr/ark:/12148/cb30116914c).
     2. The editio princeps of the work, namely Bibliothèque Mazarine Inc. 59 (notice https://www.sudoc.fr/135345618) scanned in high definition in color.
     
The editio princeps contains, first, the Table of Rubrics; second, the Genealogia itself; third, the Alphabetical Index by Domenico Bandini; fourth, the Versus of Domenico di Silvestro. The printer did not undertake to reproduce the genealogical trees which stood presumably in the MS which served him as copy.The edition of 1472 is  the best printed representative of the Vulgate text of the Genealogia, and should be cited, in preference to the edition of 1532, for all portions of the Genealogia, except those printed by Hecker [Hecker_1902] from the autograph, and for any citation in which the reading of the Vulgate text as against that of the autograph is desired (More specifically, Hecker prints from the second autograph the Dedicatory Letter (but not the single chapter of the general Proem, nor the Proem of Book I), the Proems of Books II-XIII, and Books XIV and XV entire).
     
# **Brief explaination of the transcription norms**
     
Both documents present for the most part coherent and regular writting which makes it easier to segment the text and train a machine to automatically transcribe the content.We decided to begin the transcription of both works (approx. 25 pages for each), producing segmentation and trascription models in order to facilitate the task.

Principles of standardisation of the transcriptions, namely transcription norms follow the general lines of the cremma- ledieval/HTR-United initiative guidelines https://github.com/HTR-United/cremma-medieval. More specifically,we chose a graphemic transcription method, to have a sign in the image corresponding to a sign in the text: all the abbreviations are kept, and u/v or i/j are not distinguished. The spaces in the dataset are not homogeneously represented, sometimes transcriptions reproduce the manuscript spacing while others use lexical spaces, especially for the BnF, Rés J-845 _incunabulum_. As per the special characters themselves, we follow the table created by cremma-medieval https://github.com/HTR-United/cremma-medieval/blob/main/table.csv#L156 and complement where necessary with the public domain mufi characters https://mufi.info/m.php?p=mufi. A more detailed .tex file is included in the repository summing up the proceedure.

# **Quality control**

We decided, following HTR-United workflows, to implementation of Chocomufin for the characters. Chocomufin is a software-workflow developped by Clérice Thubault and Pinche Ariane that creates a table of the characters (```table.csv```) that exist in the ground truth for both documents, and checks, with every push and pull request that the .xml documents found in the folders are conforming to this particular table. 

# **Guide to reading the repository** 

The structure of the repository isn't an original conception. We got inspired by the HTR-UNited and decided to present it following this disposition : 

- one folder containing all the data about the ancient french manuscript (```BnF Rés. J-845)
- another concerning the latin version (```Mazarine Inc59)
- a LaTeX synthesis of the research (```LaTeX_documentation)

Inside those main folders, we can find a similar structure. Both present three subfolders : 

- one for the segmentation and transcription models(```models).
- one for the training corpus used to train the A.I. on escriptorium (documents are exclusively XML Alto with jpg and a .txt containing the full text) (```training_corpus)
- one for the verification corpus.(```verification_corpus)

 # **Bibliographic references**
 
**Primary sources**

Boccaccio (Giovani),Genealogia deorum ; editio princeps add. Dominico Silvestri ; Raffaele Zovenzoni. – Venise : Wendelin de Spire, 1472. – In-folio. Digitalised and available online at https://mazarinum.bibliotheque-mazarine.fr/records/item/1781-genealogia-deorum?offset=16 IIIF manifest https://mazarinum.bibliotheque-mazarine.fr/iiif/1781/manifest identifier https://mazarinum.bibliotheque-mazarine.fr/ark:/61562/mz1781

Boccace , De la généalogie des dieux, ed. Antoine Vérard 1498-1499, Paris. Digitalised and available online at https://gallica.bnf.fr/ark:/12148/bpt6k105063r/f6.item IIIF manifest https://gallica.bnf.fr/iiif/ark:/12148/bpt6k105063r/manifest.json Identifier https://gallica.bnf.fr/ark:/12148/bpt6k105063r

**Secondary Sources**

BRANCA ,Vittore (1986), « Boccaccio visualizzato », Studi sul Boccaccio 15,107-120.

COULTER, Cornelia Catlin (1923), The Genealogy of the Gods, Vassar Medieval Studies, Yale University Press, New Haven.

GALDERISI, Claudio (2014),Translations médiévales, cinq siècles de traductions en français au Moyen-Age (XIe-XVe siècles): Vol 2, Tome 1, Turnhout, Brepols.

HAUVETTE, Henri (1914), Boccace. Étude biographique et littéraire, Paris, Colin.

HECKER, Oscar (1902),Boccaccio-funde: stücke aus der bislang verschollenen bibliothek des dichters darunter von seiner hand geschriebenes fremdes und eigenes. Braunschweig: G. Westermann.

HORTIS, Attilio (1879), Studj sulle opere latine del Boccaccio, Librerie Juluis Dase Editrice, Trieste.

MOMBELLO, Gianni (1971), «I manoscritti delle opere di Dante, Petrarca e Boccaccio nelle principalei librerie francesi del secolo xv » in: Il Boccaccio nella cultura francese, 81-209

OUY, Gilbert (1999),Les manuscrits de l'abbaye de Saint-Victor.Catalogue établi sur la base du répertoire de Claude de Grandrue (1514),t. 2, Turnhout, Brepols.

WILKINS, Ernest Hatch (1927), The Trees of the ‘Genealogia Deorum’of Boccaccio, The Caxton Club, Chicago.

(1919), « The geneaology of the editions of the ‘Genealogia deorum’ » in Modern Philology 17, 65-78.

**Methodology tools**

CAPELLI, Adriano (1982), _The elements of abbreviation in medieval Latin paleography _,tr. by David Heimann and Richard Kay. Lawrence, Kansas : University of Kansas Libraries https://kuscholarworks.ku.edu/bitstream/handle/1808/1821/47cappelli.pdf.

Collatinus 11.2,web Version web du lemmatiseur et analyseur morphologique de textes latins, https://outils.biblissima.fr/fr/collatinus-web/.

CHAGUE Alix, CLERICE Thibault, ROMARY Laurent (2021), HTR-United : Mutualisons la vérité de terrain!.

CHAGUE, Alix,CLERICE, Thibault. HTR-United, a centralization effort of HTR and OCR ground-truth repositories mainly for French languages [Computer software]

CLERICE, T., PINCHE, A. (2021). Choco-Mufin, a tool for controlling characters used in OCR and HTR projects (Version 0.0.4) [Computer software]. https://doi.org/10.5281/zenodo.5356154


STUZMANN,Dominique (2011), « Paléographie statistique pour décrire, identifier, dater. . . normaliser pour coopérer et aller plus loin ? », in: F. Fischer, C. Fritze, G. Vogeler (Eds.), Kodikologie und Paläographie im digitalen Zeitalter 2 - Codicology and Palaeography in the Digital Age 2, volume 3, Norderstedt,247–277. URL: https://kups.ub.uni-koeln.de/4353/.

## **The team members** 

Noé Leroy , *alias* @apogonoe | Eraslus student, Master HN 2021-2020 @ École nationale des chartes 
Malamatenia Vlachou-Eftsathiou *alias* @malamatenia | Master HN 1 student @ École nationale des chartes 
Marco Maulu *alias* @mmaulu | Sassari University of Sardegnia, invited professor @ École nationale des chartes
