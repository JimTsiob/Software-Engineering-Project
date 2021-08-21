# ΠΧ8. Διαχείριση μέρους (Manage Component)

**Πρωτεύων Actor** : Component Owner

**Ενδιαφερόμενοι** 

**Component Owner** : Ο Component Owner θα επιβλέπει την πρόοδο του component , θα αναθέτει developers να δουλέψουν πάνω σε μέρη του component ή σε bugs και θα αναφέρει τυχόν bugs στον Project Owner.

**Project Owner** : Ο Project Owner θα επιβλέπει την πρόοδο των components που βρίσκονται στο project του και θα διαβάζει αναφορές των component Owners.

**Προυποθέσεις** : Να έχει ταυτοποιηθεί ο Component Owner

## Βασική Ροή
### Α) Ανάθεση εργασίας

1. Ο Component Owner αναθέτει σε developers να υλοποιήσουν ένα component.
2. Αλλαγή του status του κομματιού/bug σε In Progress.
3. Το σύστημα ενημερώνεται με τέτοιο τρόπο ώστε κάθε developer να αντιστοιχίζεται στο κομμάτι που δουλεύει.


*1α) Λανθασμένη ανάθεση developer*

1. Ενημερώνεται ο developer από το σύστημα ότι θα αλλάξει θέση και θα δουλέψει σε άλλο κομμάτι/bug.
2. Το σύστημα διαγράφει την παλιά εγγραφή.
3. η ΠΧ επιστρέφει στο βήμα 1.

### Β) Ολοκλήρωση υλοποίησης κομματιού
1. O Component Owner αναφέρει στον Project Owner την ολοκλήρωση του κομματιού.
2. Οι Developers ενημερώνονται για την ολοκλήρωση του κομματιού και περιμένουν νέα ανάθεση.
