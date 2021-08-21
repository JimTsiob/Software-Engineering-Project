# INF138 Project Template

Ένα απλό πρότυπο οργάνωσης του κώδικα και της τεχνικής τεκμηρίωσης για τις εξαμηνιαίες εργασίες του μαθήματος Τεχνολογία Λογισμικού ([INF138](https://eclass.aueb.gr/courses/INF138/)) του Τμήματος Πληροφορικής Οικονομικού Πανεπιστημίου Αθηνών.

Η τρέχουσα έκδοση περιλαμβάνει την [προδιαγραφή των απαιτήσεων λογισμικού](docs/markdown/software-requirements.md) με προσαρμογή του `IEEE Std 830-1998` για την ενσωμάτωση απαιτήσεων σε μορφή περιπτώσεων χρήσης. Για περισσότερες λεπτομέρειες μπορείτε να ανατρέξετε στο βιβλίο [Μ Γιακουμάκης, Ν. Διαμαντίδης, Τεχνολογία Λογισμικού, Σταμούλης, 2009](https://www.softeng.gr).

# Οδηγίες χρήσης

Στην παρούσα αρχική σελίδα `README.md` προσθέστε σε μορφή Markdown την περιγραφή του Project όπως σας ζητείται στο παραδοτέο R1. Στη σελίδα αυτή θα προστεθούν σύνδεσμοι προς τα έγγραφα Markdown που περιλαμβάνουν την προδιαγραφή και ανάλυση των απαιτήσεων [software-requirements.md](docs/markdown/software-requirements.md) και τη σχεδίαση του συστήματος [design.md](docs/markdown/design.md).

Η τεκμηρίωση/διαγράμματα που ζητούνται στα επόμενα παραδοτέα θα τοποθετηθούν στους εξής φακέλους:
* `docs/markdown`: αρχεία Markdown με την τεκμηρίωση του συστήματος που απαιτείται για τα παραδοτέα R2-R4. H τεκμηρίωση θα συμπεριληφθεί στα ακόλουθα αρχεία:
     *  `software-requirements.md`: προδιαγραφή και ανάλυση των απαιτήσεων. Προκειμένου να διευκολυνθεί η συνεργασία σας, οι περιγραφές των περιπτώσεων χρήσης μπορούν να εισαχθούν σε διαφορετικά αρχεία `*.md`. Προϋπόθεση είναι να υπάρχουν κατάλληλοι σύνδεσμοι από το `software-requirements.md` προς αυτά έτσι ώστε να διευκολύνεται η πλοήγηση στην τεκμηρίωση μέσω του Gitlab. Τα διαγράμματα που θα δημιουργηθούν στα πλαίσια του R2 θα ενσωματωθούν στα παραπάνω έγγραφα (δεν θα λάβουμε υπόψιν διαγράμματα με μορφή εικόνας/uxf που δεν θα φαίνονται ως μέρος της τεκμηρίωσης).
     *  `design.md`: περιγραφή της σχεδίασης του συστήματος όπως ζητείται στα παραδοτέα R3 και R4. To έγγραφο θα ενσωματώνει όλα τα διαγράμματα που θα δημιουργηθούν στα παραδοτέα R3, R4. Οι εικόνες των διαγραμμάτων θα είναι διαθέσιμες στο φάκελο `docs/markdown/uml`, όπως παράγονται από το εργαλείο Gradle.
* `docs/uml`: αρχεία Umlet (`*.uxf`) με τα διαγράμματα που έχουν υλοποιηθεί στα πλαίσια των παραδοτέων R2-R4. Μπορούν να οργανωθούν σε υποφακέλους (πχ. `requirements`, `design`).

Η αυτοματοποιημένη μετατροπή των διαγραμμάτων Umlet σε PNG εικόνες, έτοιμες προς ενσωμάτωση στην Markdown τεκμηρίωσή σας μπορεί να γίνει με χρήση του εργαλείου Gradle. Προϋπόθεση για τη σωστή λειτουργία της διαδικασίας είναι η [λήψη](https://maven.apache.org/download.cgi), [εγκατάσταση](https://maven.apache.org/install.html) και προσθήκη στο PATH του συστήματος του εργαλείου Maven.

Μετά την εγκατάσταση του Maven, μπορείτε να παράξετε όλα τα διαγράμματα που βρίσκονται στον κατάλογο `docs\uml` (και υποκαταλόγους) με τη βοήθεια του Gradle (δε χρειάζεται εγκατάσταση):

Από γραμμή εντολών Windows:
```bash
gradlew.bat umlet
```

Από γραμμή εντολών Linux:
```bash
./gradlew umlet
```

Η εκτέλεση της εντολής θα εγκαταστήσει το Gradle και θα παράξει τα διαγράμματα στον κατάλογο `docs\markdown\uml` διατηρώντας την οργάνωση σε καταλόγους των Umlet αρχείων. Στη συνέχεια, μπορείτε να ενσωματώσετε στην τεκμηρίωσή σας τις εικόνες του παραπάνω καταλόγου.

# Εισαγωγή

Σκοπός της εργασίας είναι η ανάπτυξη λογισμικού **bug tracker** για διευκόλυνση της καταγραφής, παρακολούθησης και διόρθωσης σφαλμάτων που προκύπτουν κατά την διαδικασία ανάπτυξης λογισμικού. Οι χρήστες αυτης της εφαρμογής αποσκοπούν στην αύξηση της απόδοσης των ομάδων τους, στην μείωση των bug στην βάση κώδικα και  στην ταχύτερη ολοκλήρωση των επιμέρους project.

## ΚΥΡΙΟΙ ΡΟΛΟΙ

* Ο Project Owner :
  * αναθέτει ρόλο στους users
  * δημιουργεί νέα projects
  * διαγράφει projects
  * αναθέτει component σε Component Owners
  * παρακολουθεί την πορεία όλων των projects του συστήματος
  
* Ο Component owner:
  * αναθέτει επίλυση bug σε developers
  * παρακολουθεί την πορεία του component του

* O Developer:
  * εντοπίζει και αναφέρει την ύπαρξη bug με περιγραφή 
  * διορθώνει και παρακολουθεί τα bug που του έχουν ανατεθεί
  * όλοι οι χρήστες έχουν την ιδιότητα του Developer
# 1. Πριν την ανάδειξη bug
* Το σύστημα απαιτεί την εγγραφή και την ταυτοποίηση χρήση 
  * Οι χρήστες θα μπορούν να δημιουργήσουν λογαριασμό μέσω του λογισμικού και θα ανατίθεται ρόλος από τον Admin.
  
      Τα στοιχεία που θα πρέπει να εισαχθούν θα έχουν κλασική δομή signup form δηλαδή θα χρειάζεται : 

    * Username
    * Password
    * Email
    * Όνομα
    * Επώνυμο

    Aφού εγκριθεί ο λογαριασμός ο χρήστης θα μπορεί να επανασυνδεθεί στην εφαρμογή με το username και το password του.
* Τo σύστημα επιτρέπει την παρακολούθηση πολλαπλών project
* Κάθε project έχει έναν ιδιοκτήτη(Project Owner) και έναν ή περισσότερους συμμετέχοντες (developers-component Owners)
  * Ο ιδιοκτήτης προσθέτει τους συμμετέχοντες στο κάθε project μετά από αναζήτηση
* Κάθε project μπορεί να έχει ένα ή περισσότερα components προς υλοποίηση
  * Κάθε component έχει επικεφαλής έναν developer-component owner
  * O developer-component owner είναι υπεύθυνος για την υλοποίηση του συγκεκριμένου component
  * Ο developer-component owner είναι ένας εκ των συμμετεχόντων στο συγκεκριμένο project
    
  # 2. Καταχώρηση bug

* Οι προγραμματιστές (Developers) μπορούν να δημιουργήσουν και να υποβάλλουν bugs/issues για το project τους
* Το κάθε bug/issue περιγράφεται με:
  * ID 
  * Όνομα
  * Προτεραιότητα
  * Περιγραφή σε μορφή κειμένου
  * Status
  * Ημερομηνία Καταχώρησης
  * Username του developer που το καταχώρησε

* Μόλις καταχωρηθεί το bug το status του είναι ToDo.
* Ο component owner βλέπει τα bug που αφορούν στο component και τα αναθέτει στα κατάλληλα μέλη της ομάδας του.
* Μόλις γίνει η ανάθεση το status του bug γίνεται In Progress.
* Ο προγραμματιστής (Developer) προσθέτει σταδιακά τα βήματα επίλυσης του bug/issue κάνοντας update το status του.

# 3. Επίλυση bug
* Αφού επιλυθεί το bug το status του γίνεται Done.
* Αφαιρείται το bug από τη λίστα των bugs.
* Ο προγραμματιστής (Developer) που ασχολιόταν με αυτό μεταφέρεται από τον Component owner σε άλλο bug εφόσον απαιτείται. 


  ## System Reports
  Το σύστημά μας θα δίνει στους χρήστες(Component Owner, Project Owner) τη δυνατότητα καλύτερης κατανόησης της πορείας ανάπτυξης λογισμικού μέσα από την παραγωγή αναφορών και στατιστικών στοιχείων που θα τους  πληροφορούν σχετικά με:
  * Συνολικά bug στα επιμέρους υποσυστήματα
  * Μέση χρονική διάρκεια επίλυσης bug ανά υποσύστημα
  * Αριθμό bug που επίλυσε ο κάθε Developer
  * Πλήθος bug ανά component


Το ανάλογο use case diagram βρίσκεται [εδώ](docs/markdown/uml/requirements/bug_tracker_UC_diagram.png)

### Software requirements αρχείο [εδώ](docs/markdown/bt-software-requirements.md)

### Design αρχείο [εδώ](docs/markdown/design.md)


