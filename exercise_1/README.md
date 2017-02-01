# Γεια Σου Κόσμε - Μάθημα 1
Author: Savvas
## Στόχοι
- Γνωριμία με Εντολές Κελύφους Bash
- Γνωριμία με Επεξεργαστή Κειμένου Emacs
- Εγκατάσταση JVM
- Γνωριμία με το git
- Πρώτο Πρόγραμμα στη Java

## Απαιτούμενα
- Λειτουργικό Centos7
- Όρεξη

## Εγκατάσταση Προαπαιτούμενων
- Για την άσκηση αυτή χρειάζεται να εγκαταστήσουμε τα πιο κάτω μέσω της γραμμής εντολών
	```bash
	sudo yum install git emacs java-1.8.0-openjdk-devel
	```
- Με τη πιο πάνω εντολή εγκαθιστούμε με το διαχειριστή πακέτων [yum](https://en.wikipedia.org/wiki/Yellowdog_Updater,_Modified)
- Το εργαλείο διαχείρισης κώδικα [git](https://git-scm.com/)
- Επεξεργαστή Κειμένου [GNU Emacs](https://www.gnu.org/software/emacs/) και
- [OpenJDK](http://openjdk.java.net/) (Open Java Development Kit)

## Ρύθμιση git και "πιρούνιασμα" αποθετηρίου

1. Δημιουργία Λογαριασμού στο [github](https://github.com/)
2. Ρύθμιση git τοπικά

	```sh
	git config --global user.name "YOUR NAME"
	git config --global user.email "YOUR EMAIL ADDRESS"
	```

3. Δημιουργία Κλειδιού [ssh](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/). Περισσότερα για την [Ασύμμετρη Κρυπτογραφία](https://en.wikipedia.org/wiki/Public-key_cryptography)
4. Αντιγραφή κλειδιού στο github ακολούθησε τις οδηγίες [εδώ](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/). Αντί του πρώτου βήματος μπορείς να το αντιγράψεις από εδώ.

	```bash
	cat ~/.ssh/id_rsa.pub
	```

5. Δημιουργία Αποθετηρίου, Κλώνου και Πιρούνιασμα Κώδικα [εδώ](https://help.github.com/articles/fork-a-repo/)
   Δημιούργησε ένα αποθετήριο με το όνομα GeiaSouKosme-TeamOne στο TzavaMania

	```bash
	git clone git@github.com:TzavaMania/FirstStepsInJava-TeamOne.git
	cd FirstStepsInJava-TeamOne
	git remote -v
	git remote add upstream git@github.com:TzavaMania/FirstStepsInJava.git
	git remote -v
	git fetch upstream
	git checkout master
	```

6. Επεξεργασία README.md και αποθήκευση κάτω από του Καινούργιο Αποθετήριο
	```bash
	cd exercise_1
	emacs README.md
	```
	Βάλε στο author το όνομα σου, αποθήκευση με <kbd>C-x C-s</kbd> και "minimize" <kbd>C-z</kbd>
	```bash
	git add README.md
	git commit -m "my first commit"
	git push origin
	```
## Δημιουργία Προγράμματος και Μεταγλώττιση προγράμματος
	```bash
	touch HelloWorld.java
	emacs HelloWorld.java
	```
	- Ακολούθως γράψε το πιο κάτω κώδικα
	```java
	public class HelloWorld {

		public static void main(String[] args) {
			// Τυπώνει "Hello, World" στο τερματικό.
			System.out.println("Hello, World");
		}
	}
	```
	- Αποθήκευσε και ελαχιστοποίησε.
	- Compile Ποργράμματος
	```sh
	javac HelloWorld.java
	java HelloWorld
	```
	- Σβήσε το αρχείο που έχει δημιουργηθεί από τον compiler και ανέβασε με τη χρήση του git
