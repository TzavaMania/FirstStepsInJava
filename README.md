# Γεια Σου Κόσμε - Πρώτο Μάθημα
## Στόχοι
- Γνωριμία με Εντολές Κελύφους Bash
- Γνωριμία με Επεξεργαστή Κειμένου Emacs
- Εγκατάσταση JVM κτλπ
- Γνωριμία με το git
- Πρώτο Πρόγραμμα στη Java

## Απαιτούμενα
- Λειτουργικό Centos7
- Όρεξη

## Εγκατάσταση Προαπαιτούμενων
   Για την άσκηση αυτή χρειάζεται να εγκαταστήσουμε τα πιο κάτω μέσω της γραμμής εντολών
```bash
   sudo yum install git emacs java-1.8.0-openjdk-devel
```
Με τη πιο πάνω εντολή εγκαθιστούμε με το διαχειριστή πακεων [yum](https://en.wikipedia.org/wiki/Yellowdog_Updater,_Modified)
- Το εργαλείο διαχείρησης κώδικα [git](https://git-scm.com/)
- Επεξεργαστή Κειμένου [GNU Emacs](https://www.gnu.org/software/emacs/) και
- [OpenJDK](http://openjdk.java.net/) (Open Java Development Kit)
	 
## Ρύθμιση git και "πιρούνιασμα" αποθετηρίου
	
1. Δημιουργία Λογαριασμού στο [github](https://github.com/)
2. Ρύθμιση git τοπικά
```bash
	git config --global user.name "YOUR NAME"
	git config --global user.email "YOUR EMAIL ADDRESS"
```
3. Δημιουργία Κλειδιού [ssh](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/). Περισσότερα για την [Ασσύμετρη Κρυπτογραφία](https://en.wikipedia.org/wiki/Public-key_cryptography)
4. Αντιγραφή κλειδιού στο github ακολούθησε τις οδηγίες [εδώ](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/). Αντί του πρώτου βήματος μπορείς να το αντιγράψεις από εδώ.
```bash
	cat ~/.ssh/id_rsa.pub
```
5. Δημιουργία Αποθετηρίου, Κλόνου και Πιρούνιασμα Κώδικα [εδώ](https://help.github.com/articles/fork-a-repo/)
```bash
	git clone https://github.com/TzavaMania/GeiaSouKosme-TeamOne
	cd GeiaSouKosme-TeamOne
	git remote -v
	git remote add upstream https://github.com/TzavaMania/GeiaSouKosme
	git remote -v
```
	
