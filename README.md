**Gem5 : 2nd Assignment**

**Lab B <br />
Team 4 <br />
ΑΕΜ: 8726 / 8399<br />**

**1.1**

![1.1](https://github.com/John120196/GEM5_Assignment2/blob/main/Results/1.1/1.1.png)

Θα μπορούσαμε εναλλακτικά να υπολογίσουμε τα συνολικά accesses της L2 cache χρησιμοποιώντας τα metrics: _system.l2.overall_mshr_miss_rate::total_  &   _system.l2.overall_mshr_misses::total_ <br />
Δηλαδή ισχύει:<br /> **system.l2.overall_accesses::total  =  system.l2.overall_mshr_misses::total / system.l2.overall_mshr_miss_rate::total**


**1.2**

![1.2](https://github.com/John120196/GEM5_Assignment2/blob/main/Results/1.2/1.2.png)

![1.2.2](https://github.com/John120196/GEM5_Assignment2/blob/main/Results/1.2/res.png)


**1.3**

![1.3](https://github.com/John120196/GEM5_Assignment2/blob/main/Results/1.3/1.3.png)

![1.3.2](https://github.com/John120196/GEM5_Assignment2/blob/main/Results/1.3/Untitled.png)

Δεν υπάρχει τέλειο scaling διότι το αποτέλεσμα (χρόνος εκτέλεσης) επηρεάζεται και από άλλες παραμέτρους όπως π.χ. οι μνήμες l1 και l2 cache. <br />
Αυτό φαίνεται εξάλλου και στο διαφορετικό CPI (στον 2GHz CPU είναι μεγαλύτερο/χειρότερο απ'ότι στον 1.5GHz)


**2.1 - 2.2**

Ύστερα από αρκετές δοκιμές στο benchmark speclibm με χρήση διαφορετικών configuration και σκοπό την βελτιστοποίηση του CPI μας είχαμε τα παρακάτω αποτελέσματα:

![2.2](https://github.com/John120196/GEM5_Assignment2/blob/main/trials.png)
*Για κάθε configuration υπάρχει screenshot με τον κώδικα στο terminal, μέσα στον αντίστοιχο φάκελο του repository! 

Συγκεκριμένα το CPI μεταβλήθηκε ως εξής: 

![2.2.2](https://github.com/John120196/GEM5_Assignment2/blob/main/CPI.png)

Είναι προφανές ότι όσο πιο πλόυσιο σε ποσότητα και ποιότητα μνήμης cache configuration κάνουμε, τόσο καλύτερα αποτελέσματα (CPI) θα έχουμε για ένα δεδομένο clock speed. Παρά ταύτα, το κόστος του configuration ανεβαίνει σχεδόν εκθετικά με την αύξηση της μνήμης cache και της περιπλοκότητάς της, κάτι που σημαίνει ότι το "ιδανικό" configuration δεν είναι αυτό με το καλύτερο CPI και χρόνο εκτέλεσης, αλλά αυτό που βρίσκει τη "χρυσή τομή" μεταξύ κόστους και απόδοσης! 


**3.1**


