# ΠΧ4. Δημιουργία και προβολή θέματος για Σφάλμα (Create-View Bug/Issue)

**Πρωτεύων Actor** : Developer

**Ενδιαφερόμενοι** 

**Project Owner** :Βλέπει τα bugs σε όλα τα στάδια του κύκλου ζωής τους.

**Component Owner**: θέλει να  βλέπει τα νέα σφάλματα και να τα αναθέτει σε κατάλληλους developer για να επιλυθούν .Επίσης παρακολουθή την πορεία επίλυσης των ήδη υπάρχοντων bug.

**Developer** : δημιουργεί το θέμα για το bug . Επίσης συνεργάζεται με άλλους developers για να επιλύσει.

**Προυποθέσεις** : Να έχει ταυτοποιηθεί ο Developer, να έχει δημιουργηθεί το project και το component

## Βασική Ροή

### Α) Δημιουργία Bug/ Issue
1. Εισαγωγή ονόματος
2. Εισαγωγή περιγραφής 
3. Εισαγωγή προτεραιότητας
4. Υποβολή αιτήματος για δημιουργία θέματος
5. Το σύστημα ενημερώνεται με τη νέα εγγραφή
6. Ενημερώνεται ο Component Owner με μήνυμα από το σύστημα ότι δημιουργήθηκε νέο θέμα
7. Μετά την ανάθεση από τον Component Owner το bug εμφανίζεται στις αναφορές

### Β)Εμφάνιση πορείας bug
Εμφανίζονται οι πληροφορίες και τα βήματα επίλυσης συγκεκριμένου bug. Ειδικότερα εμφανίζονται πληροφορίες για:
1. Όνομα
2. Περιγραφή
3. Προτεραιότητα
4. Project-component στο οποίο ανήκει
5. Αλλαγές με χρονολογική σειρά
6. Υπεύθυνοι developers

## Εναλλακτικές ροές  
* Σε οποιοδήποτε σημείο το λογισμικό καταρρέει
1. Ο χρήστης επαναλαμβάνει την διαδικασία login.
2. Το σύστημα ταυτοποιεί τον χρήστη.
3. Ο Χρήστης εκκινή την περίπτωση χρήσης από την αρχή.

*4α) Λανθασμένη υποβολή σφάλματος*
1. Το σύστημα διαγράφει την παλιά εγγραφή
2. Ενημερώνεται ο Developer για το σημείο της λανθασμένης υποβολής
3. Ενημερώνεται ο Component Owner με μήνυμα ότι έγινε λάθος
4. To bug/issue δεν εμφανίζεται ακόμα στην λίστα αναφορών
5. η ΠΧ τερματίζει.
