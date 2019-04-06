# Git 101
## Branches

###### Εξοικείωση με το checkout.
1. Θέλουμε να δούμε πως ήταν το αρχείο στο πρώτο commit. Γράφουμε την εντολή `git log` και αντιγράφουμε το hash από το πρώτο commit (ή τα πρώτα 7 ψηφία).
2. Γράφουμε την εντολή `git checkout HASH`.
>Έστω ότι το hash είναι `e7bd819`. Γράφουμε την εντολή `git checkout e7bd819`.

3. Βλέπουμε ότι τα περιεχόμενα είναι όπως ήταν στο πρώτο commit. Γράφουμε `git log` και βλέπουμε ότι υπάρχει ένα μόνο commit.
4. Γράφουμε `git checkout master`.
5. χρησιμοποιώντας το `git log` βλέπουμε ότι βλέπουμε και πάλι 2 commits.


###### Kαινούριο branch.
6. Γράφουμε την εντολή `git branch`. Περιμένουμε να έχει μία εγγραφή "master".
7. Γράφουμε την εντολή `git branch new_branch` και πάλι `git branch`. Βλέπουμε πως υπάρχουν δύο εγγραφές.
> Το ενεργό branch έχει έναν αστερίσκο αριστερά του.

8. Με την εντολή `git checkout new_branch`, θέτουμε το `new_branch` ως ενεργό branch. Τώρα "βρισκόμαστε" στο new_branch. Ότι αλλαγές κάνουμε θα είναι διαθέσημες μόνο εδώ.
9. Χρησιμοποιήσουμε το `git branch` και βλέπουμε ότι το ενεργό branch είναι το new_branch.
10. Προσθέτουμε μία γραμμή στο αρχείο `todolist.txt`.
11. Γράφουμε `git add .` και `git commit -m "Add a new task."` (Μπορείς να συνδυάσεις τις εντολές σε μία `git commit -am "Add a new task."`).
12. Γράφουμε την εντολή `git log`. Βλέπουμε ότι έχουμε 3 commits.

###### Tο πρώτο merge!
13. Θέλουμε να "πάμε" στο master branch. Γράφουμε την εντολή `git checkout master`. Βλέπουμε πως το αρχείο βρίσκεται στην κατάσταση που είχαμε πριν κάνουμε το  τελευταίο commit.
14. Χρησιμοποιήσουμε το `git branch` και βλέπουμε ότι το ενεργό branch είναι το master.
15. Γράφουμε `git log` και βλέπουμε ότι όντως έχουμε 2 commits.
16. Για να οριστικοποιήσουμε τις αλλαγές μας, πρέπει να τις "μεταφέρουμε" στο master branch. Γράφουμε `git merge new_branch`.
17. Με την εντολή `git log` μπορούμε να δούμε ότι οι αλλαγές που είχαμε κάνει στο new_branch είναι πλέον διαθέσημες και στο master.