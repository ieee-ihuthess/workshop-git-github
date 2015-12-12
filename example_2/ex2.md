# "Συνεργασία και Συνεισφορά μέσω Git και GitHub"
## Άσκηση 2η - Merge Branches και Conflicts

1. Ανοίγουμε το τερματικό και εκτελούμε την εντολή `git init example_2` για να δημιουργήσουμε κατευθείαν το φάκελο και το repository
2. Μπαίνουμε στο φάκελο με την εντολή `cd example_2`
3. Δημιουργούμε ένα αρχείο μέσα στο φάκελο (πχ ratings.txt)
4. Το κάνουμε add στο staging mode με την εντολή `git add ratings.txt` και κάνουμε commit με την εντολή `commit -m "add file"`
5. Πληκτρολογούμε την έντολή `git branch`
6. Φτιάχνουμε ένα νέο branch με το όνομα firstratings με την εντολή `git branch firstratings`
7. Ξαναπληκτρολογούμε την εντολή `git branch` για να δούμε το νέο branch που δημιουργήσαμε
8. Για να αλλάξουμε branch εκτελούμε την εντολή `git checkout firstratings`
9. Στη συνέχεια επεξεργαζόμαστε το αρχείο ratings.txt, προσθέτοντας σε κάθε σειρά ένα αντικείμενο και από δίπλα την βαθμολογία του (πχ Spectre 7)
10. Πληκτρολογούμε την εντολή `git status` για να δούμε τι γίνεται με το αρχείο μας
13. Προσθέτουμε το αρχείο ratings.txt σε staging mode με την εντολή `git add ratings.txt`
14. Κάνουμε commit τις αλλαγές μας με την εντολή `commit -m "First ratings!"`
15. Επιστρέφουμε στο αρχικό μας branch με την εντολή `git checkout master`
16. Βλέπουμε ότι οι αλλαγές μας δεν έχουν γίνει στο αρχείο ratings.txt, επειδή βρίσκονται σε άλλο branch
17. Πληκτρολογούμε την εντολή `git merge firstratings` για να ενωθούν οι αλλαγές μας
18. Διαγράφουμε το branch firstratings με την εντολή `git branch -d firstratings`
19. Δημιουργούμε ένα νέο branch και μεταφερόμαστε σε αυτό κατευθείαν με την εντολή `git checkout -b moreratings`
20. Προσθέτουμε μερικές ακόμη βαθμολογίες και κάνουμε add και commit της αλλαγές μας με την εντολή `git commit -am "more ratings!"`
21. Γυρνάμε στο αρχικό branch master με την εντολή `git checkout master` και επεξεργαζόμαστε το αρχείο ratings.txt
22. Στη συνέχεια κάνουμε stage και commit τις αλλαγές μας `commit -am "some editing"`
23. Τώρα θα προσπαθήσουμε να κάνουμε merge τα branches με την εντολή `git merge moreratings`
24. Μας βγάζει conflict! Πρέπει να το λύσουμε. Πάμε στο αρχείο και το ερευνάμε. Κρατάμε αυτά που θέλουμε και κάνουμε `commit -am "resolved conflict"`
25. Αφού γίνει το commit ελέγχουμε εάν το αρχείο είναι ανανεωμένο με τις αλλαγές που θέλαμε
26. Διαγράφουμε το branch moreratings με την εντολή `git branch -d moreratings`
