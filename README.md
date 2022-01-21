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
_*Για κάθε configuration υπάρχει text file με τον κώδικα του terminal (code.txt), μέσα στον αντίστοιχο φάκελο του repository!_ 

Συγκεκριμένα το CPI μεταβλήθηκε ως εξής: 

![2.2.2](https://github.com/John120196/GEM5_Assignment2/blob/main/CPI.png)

Είναι προφανές ότι όσο πιο πλόυσιο σε ποσότητα και ποιότητα μνήμης cache configuration κάνουμε, τόσο καλύτερα αποτελέσματα (CPI) θα έχουμε για ένα δεδομένο clock speed. Παρά ταύτα, το κόστος του configuration ανεβαίνει σχεδόν εκθετικά με την αύξηση της μνήμης cache και της περιπλοκότητάς της, κάτι που σημαίνει ότι το "ιδανικό" configuration δεν είναι αυτό με το καλύτερο CPI και χρόνο εκτέλεσης, αλλά αυτό που βρίσκει τη "χρυσή τομή" μεταξύ κόστους και απόδοσης! 


**3.1**

Παρατηρώντας τα δεδομένα του δεύτερου ερωτήματος και με περαιτέρω αναζήτηση στο διαδίκτυο καταλήξαμε (έστω προσεγγιστικά) στην συνάρτηση κόστους:


**C = A * (10 * l1 + l2)** <br />
_*Όπου C -> Cost με αυθαίρετη μονάδα κόστους και Α -> Associativity Level_ <br />
_*Όπου l1 & l2, η ποσότητα της l1 και l2 μνήμης cache σε ΚΒ_


Με συνάρτηση κόστους/απόδοσης:

**P = a^C = a^(A * (10 * l1 + l2))**<br />
_*Όπου P -> Performance, με αυθαίρετη μονάδα απόδοσης και a = constant_
  

Sources:<br />
https://www.gem5.org/<br />
https://www.cs.utexas.edu/users/mckinley/352/lectures/21.pdf<br />
https://www.hardwaretimes.com/difference-between-l1-l2-and-l3-cache-how-does-cpu-cache-work/#:~:text=L2%20cache%20is%20much%20larger,the%20cores%20on%20a%20die.<br />
https://www.extremetech.com/extreme/188776-how-l1-and-l2-cpu-caches-work-and-why-theyre-an-essential-part-of-modern-chips<br />
https://www.makeuseof.com/tag/what-is-cpu-cache/<br />
https://cpuninja.com/cpu-cache/<br />
https://www.extremetech.com/extreme/188776-how-l1-and-l2-cpu-caches-work-and-why-theyre-an-essential-part-of-modern-chips#:~:text=An%20eight%2Dway%20associative%20cache,rate%20improves%20with%20set%20associativity.<br />
http://csillustrated.berkeley.edu/PDFs/handouts/cache-3-associativity-handout.pdf<br />

