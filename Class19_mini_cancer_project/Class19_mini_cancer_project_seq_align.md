# Class 19: Mini Cancer Project
Andrew Sue PID:A13006809

``` r
library(bio3d)

s <- read.fasta("A13006809_mutant_seq.fa")
s
```

                   1        .         .         .         .         .         60 
    wt_healthy     MKAPAVLAPGILVLLFTLVQRSNGECKEALAKSEMNVNMKYQLPNFTAETPIQNVILHEH
    mutant_tumor   MKAPAVLAPGILVLLFTLVQRSNGECKEALAKSEMNVNMKYQLPNFTAETPIQNVILHEH
                   ************************************************************ 
                   1        .         .         .         .         .         60 

                  61        .         .         .         .         .         120 
    wt_healthy     HIFLGATNYIYVLNEEDLQKVAEYKTGPVLEHPDCFPCQDCSSKANLSGGVWKDNINMAL
    mutant_tumor   HIFLGATNYIYVLNEEDLQKVAEYKTGPVLEHPDCFPCQDCSSKANLSGGVWKDNINMAL
                   ************************************************************ 
                  61        .         .         .         .         .         120 

                 121        .         .         .         .         .         180 
    wt_healthy     VVDTYYDDQLISCGSVNRGTCQRHVFPHNHTADIQSEVHCIFSPQIEEPSQCPDCVVSAL
    mutant_tumor   VVDTYYDDQLISCGSVNRGTCQRHVFPHNHTADIQSEVHCIFSPQIEEPSQCPDCVVSAL
                   ************************************************************ 
                 121        .         .         .         .         .         180 

                 181        .         .         .         .         .         240 
    wt_healthy     GAKVLSSVKDRFINFFVGNTINSSYFPDHPLHSISVRRLKETKDGFMFLTDQSYIDVLPE
    mutant_tumor   GAKVLSSVKDRFINFFVGNTINSSYFPDHPLHSISVRRLKETKDGFMFLTDQSYIDVLPE
                   ************************************************************ 
                 181        .         .         .         .         .         240 

                 241        .         .         .         .         .         300 
    wt_healthy     FRDSYPIKYVHAFESNNFIYFLTVQRETLDAQTFHTRIIRFCSINSGLHSYMEMPLECIL
    mutant_tumor   FRDSYPIKYVHAFESNNFIYFLTVQRETLDAQTFHTRIIRFCSINSGLHSYMEMPLECIL
                   ************************************************************ 
                 241        .         .         .         .         .         300 

                 301        .         .         .         .         .         360 
    wt_healthy     TEKRKKRSTKKEVFNILQAAYVSKPGAQLARQIGASLNDDILFGVFAQSKPDSAEPMDRS
    mutant_tumor   TEKRKKRSTKKEVFNILQAAYVSKPGAQLARQIGASLNDDILFGVFAQSKPDSAEPMDRS
                   ************************************************************ 
                 301        .         .         .         .         .         360 

                 361        .         .         .         .         .         420 
    wt_healthy     AMCAFPIKYVNDFFNKIVNKNNVRCLQHFYGPNHEHCFNRTLLRNSSGCEARRDEYRTEF
    mutant_tumor   AMCAFPIKYVNDFFNKIVNKNNVRCLQHFYGPNHEHCFNRTLLRNSSGCEARRDEYRTEF
                   ************************************************************ 
                 361        .         .         .         .         .         420 

                 421        .         .         .         .         .         480 
    wt_healthy     TTALQRVDLFMGQFSEVLLTSISTFIKGDLTIANLGTSEGRFMQVVVSRSGPSTPHVNFL
    mutant_tumor   TTALQRVDLFMGQFSEVLLTSISTFIKGDLTIANLGTSEGRFMQVVVSRSGPSTPHVNFL
                   ************************************************************ 
                 421        .         .         .         .         .         480 

                 481        .         .         .         .         .         540 
    wt_healthy     LDSHPVSPEVIVEHTLNQNGYTLVITGKKITKIPLNGLGCRHFQSCSQCLSAPPFVQCGW
    mutant_tumor   LDSHPVSPEVIVEHTLNQNGYTLVITGKKITKIPLNGLGCRHFQSCSQCLSAPPFVQCGW
                   ************************************************************ 
                 481        .         .         .         .         .         540 

                 541        .         .         .         .         .         600 
    wt_healthy     CHDKCVRSEECLSGTWTQQICLPAIYKVFPNSAPLEGGTRLTICGWDFGFRRNNKFDLKK
    mutant_tumor   CHDKCVRSEECLSGTWTQQICLPAIYKVFPNSAPLEGGTRLTICGWDFGFRRNNKFDLKK
                   ************************************************************ 
                 541        .         .         .         .         .         600 

                 601        .         .         .         .         .         660 
    wt_healthy     TRVLLGNESCTLTLSESTMNTLKCTVGPAMNKHFNMSIIISNGHGTTQYSTFSYVDPVIT
    mutant_tumor   TRVLLGNESCTLTLSESTMNTLKCTVGPAMNKHFNMSIIISNGHGTTQYSTFSYVDPVIT
                   ************************************************************ 
                 601        .         .         .         .         .         660 

                 661        .         .         .         .         .         720 
    wt_healthy     SISPKYGPMAGGTLLTLTGNYLNSGNSRHISIGGKTCTLKSVSNSILECYTPAQTISTEF
    mutant_tumor   SISPKYGPMAGGTLLTLTGNYLNSGNSRHISIGGKTCTLKSVSNSILECYTPAQTISTEF
                   ************************************************************ 
                 661        .         .         .         .         .         720 

                 721        .         .         .         .         .         780 
    wt_healthy     AVKLKIDLANRETSIFSYREDPIVYEIHPTKSFISGGSTITGVGKNLNSVSVPRMVINVH
    mutant_tumor   AVKLKIDLANRETSIFSYREDPIVYEIHPTKSFISGGSTITGVGKNLNSVSVPRMVINVH
                   ************************************************************ 
                 721        .         .         .         .         .         780 

                 781        .         .         .         .         .         840 
    wt_healthy     EAGRNFTVACQHRSNSEIICCTTPSLQQLNLQLPLKTKAFFMLDGILSKYFDLIYVHNPV
    mutant_tumor   EAGRNFTVACQHRSNSEIICCTTPSLQQLNLQLPLKTKAFFMLDGILSKYFDLIYVHNPV
                   ************************************************************ 
                 781        .         .         .         .         .         840 

                 841        .         .         .         .         .         900 
    wt_healthy     FKPFEKPVMISMGNENVLEIKGNDIDPEAVKGEVLKVGNKSCENIHLHSEAVLCTVPNDL
    mutant_tumor   FKPFEKPVMISMGNENVLEIKGNDIDPEAVKGEVLKVGNKSCENIHLHSEAVLCTVPNDL
                   ************************************************************ 
                 841        .         .         .         .         .         900 

                 901        .         .         .         .         .         960 
    wt_healthy     LKLNSELNIEWKQAISSTVLGKVIVQPDQNFTGLIAGVVSISTALLLLLGFFLWLKKRKQ
    mutant_tumor   LKLNSELNIEWKQAISSTVLGKVIVQPDQNFTGLIAGVVSISTALLLLLGFFLWLKKRKQ
                   ************************************************************ 
                 901        .         .         .         .         .         960 

                 961        .         .         .         .         .         1020 
    wt_healthy     IKDLGSELVRYDARVHTPHLDRLVSARSVSPTTEMVSNESVDYRATFPEDQFPNSSQNGS
    mutant_tumor   IKDLGSELVRYDARVHTPHLDRLVSARSVSPTTEMVSNESVDYRATFPEDQFPNSSQNGS
                   ************************************************************ 
                 961        .         .         .         .         .         1020 

                1021        .         .         .         .         .         1080 
    wt_healthy     CRQVQYPLTDMSPILTSGDSDISSPLLQNTVHIDLSALNPELVQAVQHVVIGPSSLIVHF
    mutant_tumor   CRQVQYPLTDMSPILTSGDSDISSPLLQNTVHIDLSALNPELVQAVQHVVIGPSSLIVHF
                   ************************************************************ 
                1021        .         .         .         .         .         1080 

                1081        .         .         .         .         .         1140 
    wt_healthy     NEVIGRGHFGCVYHGTLLDNDGKKIHCAVKSLNRITDIGEVSQFLTEGIIMKDFSHPNVL
    mutant_tumor   NEVIGRGHFGCVYHGTLLDNDGKKIHCAVKSLNRITDIGEVSQFLTEGIIMKVFEHPNVL
                   **************************************************** * ***** 
                1081        .         .         .         .         .         1140 

                1141        .         .         .         .         .         1200 
    wt_healthy     SLLGICLRSEGSPLVVLPYMKHGDLRNFIRNETHNPTVKDLIGFGLQVAKGMKYLASKKF
    mutant_tumor   SLRGICLRSEGSPLVVLPYMKHGDLRNFIRNETHNPTVKDLIGFGLQVAKGMKYLASKKF
                   ** ********************************************************* 
                1141        .         .         .         .         .         1200 

                1201        .         .         .         .         .         1260 
    wt_healthy     VHRDLAARNCMLDEKFTVKVADFGLARDMYDKEYYSVHNKTGAKLPVKWMALESLQTQKF
    mutant_tumor   VHRDLAARNCMLDEKFTVKVADFGLARDMYDKEYYSVHNKTGAKLPVKWMALESLQTQKF
                   ************************************************************ 
                1201        .         .         .         .         .         1260 

                1261        .         .         .         .         .         1320 
    wt_healthy     TTKSDVWSFGVLLWELMTRGAPPYPDVNTFDITVYLLQGRRLLQPEYCPDPLYEVMLKCW
    mutant_tumor   TTKSDVWSFGVLLWELMTRGAPPYPDYNTFDITVYLLQGRRLLQPEYCPDPLYEVMLKCW
                   ************************** ********************************* 
                1261        .         .         .         .         .         1320 

                1321        .         .         .         .         .         1380 
    wt_healthy     HPKAEMRPSFSELVSRISAIFSTFIGEHYVHVNATYVNVKCVAPYPSLLSSEDNADDEVD
    mutant_tumor   HPKAEMRPSFSELVSRISAIFSTFIGEHYVHVNATYVNVKCVAPYPSLLSSEDNADDEVD
                   ************************************************************ 
                1321        .         .         .         .         .         1380 

                1381        1390 
    wt_healthy     TRPASFWETS
    mutant_tumor   TRPASFWETS
                   ********** 
                1381        1390 

    Call:
      read.fasta(file = "A13006809_mutant_seq.fa")

    Class:
      fasta

    Alignment dimensions:
      2 sequence rows; 1390 position columns (1390 non-gap, 0 gap) 

    + attr: id, ali, call

I want to match the columns between my two sequences to see where they
match or dont match. Taking indexes of columns

``` r
mt_pos <- which(s$ali[1,] != s$ali[2,])
mt_pos
```

    [1] 1133 1135 1143 1287

The amino acid sequences are this (using the column indexes)

``` r
s$ali[,mt_pos]
```

                 [,1] [,2] [,3] [,4]
    wt_healthy   "D"  "S"  "L"  "V" 
    mutant_tumor "V"  "E"  "R"  "Y" 

Now we want to put it in a string and write it like biologist do

``` r
paste(s$ali[1,mt_pos], mt_pos, s$ali[2,mt_pos], sep = "")
```

    [1] "D1133V" "S1135E" "L1143R" "V1287Y"

``` r
mutant_seq <- ("MKAPAVLAPGILVLLFTLVQRSNGECKEALAKSEMNVNMKYQLPNFTAETPIQNVILHEHHIFLGATNYIYVLNEEDLQKVAEYKTGPVLEHPDCFPCQDCSSKANLSGGVWKDNINMALVVDTYYDDQLISCGSVNRGTCQRHVFPHNHTADIQSEVHCIFSPQIEEPSQCPDCVVSALGAKVLSSVKDRFINFFVGNTINSSYFPDHPLHSISVRRLKETKDGFMFLTDQSYIDVLPEFRDSYPIKYVHAFESNNFIYFLTVQRETLDAQTFHTRIIRFCSINSGLHSYMEMPLECILTEKRKKRSTKKEVFNILQAAYVSKPGAQLARQIGASLNDDILFGVFAQSKPDSAEPMDRSAMCAFPIKYVNDFFNKIVNKNNVRCLQHFYGPNHEHCFNRTLLRNSSGCEARRDEYRTEFTTALQRVDLFMGQFSEVLLTSISTFIKGDLTIANLGTSEGRFMQVVVSRSGPSTPHVNFLLDSHPVSPEVIVEHTLNQNGYTLVITGKKITKIPLNGLGCRHFQSCSQCLSAPPFVQCGWCHDKCVRSEECLSGTWTQQICLPAIYKVFPNSAPLEGGTRLTICGWDFGFRRNNKFDLKKTRVLLGNESCTLTLSESTMNTLKCTVGPAMNKHFNMSIIISNGHGTTQYSTFSYVDPVITSISPKYGPMAGGTLLTLTGNYLNSGNSRHISIGGKTCTLKSVSNSILECYTPAQTISTEFAVKLKIDLANRETSIFSYREDPIVYEIHPTKSFISGGSTITGVGKNLNSVSVPRMVINVHEAGRNFTVACQHRSNSEIICCTTPSLQQLNLQLPLKTKAFFMLDGILSKYFDLIYVHNPVFKPFEKPVMISMGNENVLEIKGNDIDPEAVKGEVLKVGNKSCENIHLHSEAVLCTVPNDLLKLNSELNIEWKQAISSTVLGKVIVQPDQNFTGLIAGVVSISTALLLLLGFFLWLKKRKQIKDLGSELVRYDARVHTPHLDRLVSARSVSPTTEMVSNESVDYRATFPEDQFPNSSQNGSCRQVQYPLTDMSPILTSGDSDISSPLLQNTVHIDLSALNPELVQAVQHVVIGPSSLIVHFNEVIGRGHFGCVYHGTLLDNDGKKIHCAVKSLNRITDIGEVSQFLTEGIIMKVFEHPNVLSLRGICLRSEGSPLVVLPYMKHGDLRNFIRNETHNPTVKDLIGFGLQVAKGMKYLASKKFVHRDLAARNCMLDEKFTVKVADFGLARDMYDKEYYSVHNKTGAKLPVKWMALESLQTQKFTTKSDVWSFGVLLWELMTRGAPPYPDYNTFDITVYLLQGRRLLQPEYCPDPLYEVMLKCWHPKAEMRPSFSELVSRISAIFSTFIGEHYVHVNATYVNVKCVAPYPSLLSSEDNADDEVDTRPASFWETS")
```

``` r
kinase_domain_mut <-substring(mutant_seq, 1038, 1345)
kinase_domain_mut
```

    [1] "GDSDISSPLLQNTVHIDLSALNPELVQAVQHVVIGPSSLIVHFNEVIGRGHFGCVYHGTLLDNDGKKIHCAVKSLNRITDIGEVSQFLTEGIIMKVFEHPNVLSLRGICLRSEGSPLVVLPYMKHGDLRNFIRNETHNPTVKDLIGFGLQVAKGMKYLASKKFVHRDLAARNCMLDEKFTVKVADFGLARDMYDKEYYSVHNKTGAKLPVKWMALESLQTQKFTTKSDVWSFGVLLWELMTRGAPPYPDYNTFDITVYLLQGRRLLQPEYCPDPLYEVMLKCWHPKAEMRPSFSELVSRISAIFSTFI"

``` r
s2 <- s$ali[1:2,1038:1345]
s2
```

                 [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10] [,11] [,12]
    wt_healthy   "G"  "D"  "S"  "D"  "I"  "S"  "S"  "P"  "L"  "L"   "Q"   "N"  
    mutant_tumor "G"  "D"  "S"  "D"  "I"  "S"  "S"  "P"  "L"  "L"   "Q"   "N"  
                 [,13] [,14] [,15] [,16] [,17] [,18] [,19] [,20] [,21] [,22] [,23]
    wt_healthy   "T"   "V"   "H"   "I"   "D"   "L"   "S"   "A"   "L"   "N"   "P"  
    mutant_tumor "T"   "V"   "H"   "I"   "D"   "L"   "S"   "A"   "L"   "N"   "P"  
                 [,24] [,25] [,26] [,27] [,28] [,29] [,30] [,31] [,32] [,33] [,34]
    wt_healthy   "E"   "L"   "V"   "Q"   "A"   "V"   "Q"   "H"   "V"   "V"   "I"  
    mutant_tumor "E"   "L"   "V"   "Q"   "A"   "V"   "Q"   "H"   "V"   "V"   "I"  
                 [,35] [,36] [,37] [,38] [,39] [,40] [,41] [,42] [,43] [,44] [,45]
    wt_healthy   "G"   "P"   "S"   "S"   "L"   "I"   "V"   "H"   "F"   "N"   "E"  
    mutant_tumor "G"   "P"   "S"   "S"   "L"   "I"   "V"   "H"   "F"   "N"   "E"  
                 [,46] [,47] [,48] [,49] [,50] [,51] [,52] [,53] [,54] [,55] [,56]
    wt_healthy   "V"   "I"   "G"   "R"   "G"   "H"   "F"   "G"   "C"   "V"   "Y"  
    mutant_tumor "V"   "I"   "G"   "R"   "G"   "H"   "F"   "G"   "C"   "V"   "Y"  
                 [,57] [,58] [,59] [,60] [,61] [,62] [,63] [,64] [,65] [,66] [,67]
    wt_healthy   "H"   "G"   "T"   "L"   "L"   "D"   "N"   "D"   "G"   "K"   "K"  
    mutant_tumor "H"   "G"   "T"   "L"   "L"   "D"   "N"   "D"   "G"   "K"   "K"  
                 [,68] [,69] [,70] [,71] [,72] [,73] [,74] [,75] [,76] [,77] [,78]
    wt_healthy   "I"   "H"   "C"   "A"   "V"   "K"   "S"   "L"   "N"   "R"   "I"  
    mutant_tumor "I"   "H"   "C"   "A"   "V"   "K"   "S"   "L"   "N"   "R"   "I"  
                 [,79] [,80] [,81] [,82] [,83] [,84] [,85] [,86] [,87] [,88] [,89]
    wt_healthy   "T"   "D"   "I"   "G"   "E"   "V"   "S"   "Q"   "F"   "L"   "T"  
    mutant_tumor "T"   "D"   "I"   "G"   "E"   "V"   "S"   "Q"   "F"   "L"   "T"  
                 [,90] [,91] [,92] [,93] [,94] [,95] [,96] [,97] [,98] [,99] [,100]
    wt_healthy   "E"   "G"   "I"   "I"   "M"   "K"   "D"   "F"   "S"   "H"   "P"   
    mutant_tumor "E"   "G"   "I"   "I"   "M"   "K"   "V"   "F"   "E"   "H"   "P"   
                 [,101] [,102] [,103] [,104] [,105] [,106] [,107] [,108] [,109]
    wt_healthy   "N"    "V"    "L"    "S"    "L"    "L"    "G"    "I"    "C"   
    mutant_tumor "N"    "V"    "L"    "S"    "L"    "R"    "G"    "I"    "C"   
                 [,110] [,111] [,112] [,113] [,114] [,115] [,116] [,117] [,118]
    wt_healthy   "L"    "R"    "S"    "E"    "G"    "S"    "P"    "L"    "V"   
    mutant_tumor "L"    "R"    "S"    "E"    "G"    "S"    "P"    "L"    "V"   
                 [,119] [,120] [,121] [,122] [,123] [,124] [,125] [,126] [,127]
    wt_healthy   "V"    "L"    "P"    "Y"    "M"    "K"    "H"    "G"    "D"   
    mutant_tumor "V"    "L"    "P"    "Y"    "M"    "K"    "H"    "G"    "D"   
                 [,128] [,129] [,130] [,131] [,132] [,133] [,134] [,135] [,136]
    wt_healthy   "L"    "R"    "N"    "F"    "I"    "R"    "N"    "E"    "T"   
    mutant_tumor "L"    "R"    "N"    "F"    "I"    "R"    "N"    "E"    "T"   
                 [,137] [,138] [,139] [,140] [,141] [,142] [,143] [,144] [,145]
    wt_healthy   "H"    "N"    "P"    "T"    "V"    "K"    "D"    "L"    "I"   
    mutant_tumor "H"    "N"    "P"    "T"    "V"    "K"    "D"    "L"    "I"   
                 [,146] [,147] [,148] [,149] [,150] [,151] [,152] [,153] [,154]
    wt_healthy   "G"    "F"    "G"    "L"    "Q"    "V"    "A"    "K"    "G"   
    mutant_tumor "G"    "F"    "G"    "L"    "Q"    "V"    "A"    "K"    "G"   
                 [,155] [,156] [,157] [,158] [,159] [,160] [,161] [,162] [,163]
    wt_healthy   "M"    "K"    "Y"    "L"    "A"    "S"    "K"    "K"    "F"   
    mutant_tumor "M"    "K"    "Y"    "L"    "A"    "S"    "K"    "K"    "F"   
                 [,164] [,165] [,166] [,167] [,168] [,169] [,170] [,171] [,172]
    wt_healthy   "V"    "H"    "R"    "D"    "L"    "A"    "A"    "R"    "N"   
    mutant_tumor "V"    "H"    "R"    "D"    "L"    "A"    "A"    "R"    "N"   
                 [,173] [,174] [,175] [,176] [,177] [,178] [,179] [,180] [,181]
    wt_healthy   "C"    "M"    "L"    "D"    "E"    "K"    "F"    "T"    "V"   
    mutant_tumor "C"    "M"    "L"    "D"    "E"    "K"    "F"    "T"    "V"   
                 [,182] [,183] [,184] [,185] [,186] [,187] [,188] [,189] [,190]
    wt_healthy   "K"    "V"    "A"    "D"    "F"    "G"    "L"    "A"    "R"   
    mutant_tumor "K"    "V"    "A"    "D"    "F"    "G"    "L"    "A"    "R"   
                 [,191] [,192] [,193] [,194] [,195] [,196] [,197] [,198] [,199]
    wt_healthy   "D"    "M"    "Y"    "D"    "K"    "E"    "Y"    "Y"    "S"   
    mutant_tumor "D"    "M"    "Y"    "D"    "K"    "E"    "Y"    "Y"    "S"   
                 [,200] [,201] [,202] [,203] [,204] [,205] [,206] [,207] [,208]
    wt_healthy   "V"    "H"    "N"    "K"    "T"    "G"    "A"    "K"    "L"   
    mutant_tumor "V"    "H"    "N"    "K"    "T"    "G"    "A"    "K"    "L"   
                 [,209] [,210] [,211] [,212] [,213] [,214] [,215] [,216] [,217]
    wt_healthy   "P"    "V"    "K"    "W"    "M"    "A"    "L"    "E"    "S"   
    mutant_tumor "P"    "V"    "K"    "W"    "M"    "A"    "L"    "E"    "S"   
                 [,218] [,219] [,220] [,221] [,222] [,223] [,224] [,225] [,226]
    wt_healthy   "L"    "Q"    "T"    "Q"    "K"    "F"    "T"    "T"    "K"   
    mutant_tumor "L"    "Q"    "T"    "Q"    "K"    "F"    "T"    "T"    "K"   
                 [,227] [,228] [,229] [,230] [,231] [,232] [,233] [,234] [,235]
    wt_healthy   "S"    "D"    "V"    "W"    "S"    "F"    "G"    "V"    "L"   
    mutant_tumor "S"    "D"    "V"    "W"    "S"    "F"    "G"    "V"    "L"   
                 [,236] [,237] [,238] [,239] [,240] [,241] [,242] [,243] [,244]
    wt_healthy   "L"    "W"    "E"    "L"    "M"    "T"    "R"    "G"    "A"   
    mutant_tumor "L"    "W"    "E"    "L"    "M"    "T"    "R"    "G"    "A"   
                 [,245] [,246] [,247] [,248] [,249] [,250] [,251] [,252] [,253]
    wt_healthy   "P"    "P"    "Y"    "P"    "D"    "V"    "N"    "T"    "F"   
    mutant_tumor "P"    "P"    "Y"    "P"    "D"    "Y"    "N"    "T"    "F"   
                 [,254] [,255] [,256] [,257] [,258] [,259] [,260] [,261] [,262]
    wt_healthy   "D"    "I"    "T"    "V"    "Y"    "L"    "L"    "Q"    "G"   
    mutant_tumor "D"    "I"    "T"    "V"    "Y"    "L"    "L"    "Q"    "G"   
                 [,263] [,264] [,265] [,266] [,267] [,268] [,269] [,270] [,271]
    wt_healthy   "R"    "R"    "L"    "L"    "Q"    "P"    "E"    "Y"    "C"   
    mutant_tumor "R"    "R"    "L"    "L"    "Q"    "P"    "E"    "Y"    "C"   
                 [,272] [,273] [,274] [,275] [,276] [,277] [,278] [,279] [,280]
    wt_healthy   "P"    "D"    "P"    "L"    "Y"    "E"    "V"    "M"    "L"   
    mutant_tumor "P"    "D"    "P"    "L"    "Y"    "E"    "V"    "M"    "L"   
                 [,281] [,282] [,283] [,284] [,285] [,286] [,287] [,288] [,289]
    wt_healthy   "K"    "C"    "W"    "H"    "P"    "K"    "A"    "E"    "M"   
    mutant_tumor "K"    "C"    "W"    "H"    "P"    "K"    "A"    "E"    "M"   
                 [,290] [,291] [,292] [,293] [,294] [,295] [,296] [,297] [,298]
    wt_healthy   "R"    "P"    "S"    "F"    "S"    "E"    "L"    "V"    "S"   
    mutant_tumor "R"    "P"    "S"    "F"    "S"    "E"    "L"    "V"    "S"   
                 [,299] [,300] [,301] [,302] [,303] [,304] [,305] [,306] [,307]
    wt_healthy   "R"    "I"    "S"    "A"    "I"    "F"    "S"    "T"    "F"   
    mutant_tumor "R"    "I"    "S"    "A"    "I"    "F"    "S"    "T"    "F"   
                 [,308]
    wt_healthy   "I"   
    mutant_tumor "I"   

``` r
mt_pos_2 <- which(s2[1,] != s2[2,])
mt_pos_2
```

    [1]  96  98 106 250
