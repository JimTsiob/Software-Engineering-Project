# ΠΧ5. Ανάθεση bug σε developer(Assign bug)

**Πρωτεύων Actor**:Component Owner  
**Ενδιαφερόμενοι**  
**Component Owner**: Θέλει να αναθέσει bug προς επίλυση σε κατάλληλους developer.  
**Developer**: Θέλει να έχει πρόσβαση στo bug προκειμένου να το επιλύσει και να το υποβάλλει.  
**Προϋποθέσεις**: Να έχει ταυτοποιηθεί ο Developer, να έχει δημιουργηθεί το project και το component και να έχει υποβληθεί καποιο bug προς επίλυση από έναν developer.  

## Βασική Ροή

### Α) Ανάθεση νέου bug
1. O Component Owner ειδοποιείται για την ύπαρξη του νέου bug προς επίλυση
2. Ο Component owner βλέπει την περιγραφή και το είδος του bug 
3. Ο Component owner αλλάζει την περιγραφή , το είδος και την σοβαρότητα του bug εφόσον το κρίνει αναγκαίο
4. Ο Component owner αναθέτει το bug σε κατάλληλο υπαρκτό developer.
5. Ενημέρωση Developer για να ξεκινήσεις την επίλυση του bug.
6. Ενημέρωση αναφορών συστήματος σχετικά με το νέο bug.

## Εναλλακτικές Ροές
*2α. Ο Component Owner αποφασίζει πως δεν χρειάζεται επίλυση το συγκεκριμένο bug και το διαγράφει.
1. Η περίπτωση χρήσης τερματίζει. 

*4α. Ο component owner αναθέτει επιπλέον developers για την επίλυση του bug.*
1. O component owner επιλέγει μέσα από την λίστα των υπάρχοντων developer όσους επιθυμεί να αναθέσει στην επίλυση του bug.
2. Η περίπτωση χρήσης επιστρέφει στο βήμα 5.

## Διαγράμματα
