# Ecoop18-Ostrich

## Device

|name   |cpu    |memory |OS     | GCC | Emscripten|
|----   |---    |-------|-------|-----|-----------|
|ubuntu-deer    |Intel(R) Core(TM) i7-3820 CPU @ 3.60GHz     |  16 GB     |   Ubuntu 16.04 xenial |5.4.0 |1.37.22  |
# Web Environments
|environment    |version | JS Engine Version|
|---            |------- |------- |
|firefox34 |Firefox/34.0|-|
|firefox39|Firefox/39.0|-|
|firefox57|Firefox/57.0|-|
|chrome63|63.0.3239.132|V8 6.3.292.49|
|chromium63|63.0.3229.0|V8 6.3.292|
|chromium38|38.0.2125.0|V8 3.28.71.2|
|node | v8.9.1|V8 6.1.534.47|
|native | - | - |

# Chrome 63
### Invariants (configuration parameters that are the same for all runs) ###

| category    | short-name  |
| ----------- | ----------- |
| platform    | ubuntu-deer |
| environment | chrome63    |
| input-size  | medium      |
platform=ubuntu-deer,environment=chrome63,input-size=medium.csv

### Results ###

| benchmark | implementation | compiler   | mean    | std    | min     | max     | repetitions |
| --------- | -------------- | ---------- | ------- | ------ | ------- | ------- | ----------- |
| backprop  | js             | browserify | 1.4103  | 0.0064 | 1.4015  | 1.4245  | 10          |
| backprop  | c              | wasm       | 0.7691  | 0.0040 | 0.7640  | 0.7760  | 10          |
| bfs       | cpp            | wasm       | 0.1496  | 0.0020 | 0.1480  | 0.1550  | 10          |
| bfs       | js             | browserify | 0.2757  | 0.0017 | 0.2718  | 0.2781  | 10          |
| crc       | c              | wasm       | 1.2013  | 0.0137 | 1.1880  | 1.2250  | 10          |
| crc       | js             | browserify | 0.9827  | 0.0300 | 0.9053  | 1.0232  | 10          |
| fft       | c              | wasm       | 1.0798  | 0.0366 | 1.0420  | 1.1670  | 10          |
| fft       | js             | browserify | 4.9922  | 0.0794 | 4.9002  | 5.1127  | 10          |
| hmm       | c              | wasm       | 2.4696  | 0.0818 | 2.4240  | 2.6980  | 10          |
| hmm       | js             | browserify | 4.0027  | 0.0188 | 3.9736  | 4.0314  | 10          |
| lavamd    | c              | wasm       | 1.3137  | 0.0221 | 1.2870  | 1.3580  | 10          |
| lavamd    | js             | browserify | 1.6998  | 0.0728 | 1.6596  | 1.8891  | 10          |
| lud       | c              | wasm       | 0.8495  | 0.1167 | 0.7990  | 1.1810  | 10          |
| lud       | js             | browserify | 1.2311  | 0.0459 | 1.1870  | 1.3290  | 10          |
| nqueens   | c              | wasm       | 3.9922  | 0.0617 | 3.9520  | 4.1550  | 10          |
| nqueens   | js             | browserify | 6.0809  | 0.0218 | 6.0450  | 6.1270  | 10          |
| nw        | c              | wasm       | 0.5750  | 0.0017 | 0.5730  | 0.5780  | 10          |
| nw        | js             | browserify | 0.9503  | 0.0072 | 0.9427  | 0.9648  | 10          |
| pagerank  | c              | wasm       | 0.7809  | 0.0049 | 0.7780  | 0.7940  | 10          |
| pagerank  | js             | browserify | 0.8708  | 0.0033 | 0.8656  | 0.8776  | 10          |
| spmv      | c              | wasm       | 0.9746  | 0.0150 | 0.9640  | 1.0160  | 10          |
| spmv      | js             | browserify | 23.5353 | 0.1895 | 23.4073 | 24.0321 | 10          |
| srad      | c              | wasm       | 3.7024  | 0.0208 | 3.6580  | 3.7370  | 10          |
| srad      | js             | browserify | 7.1341  | 0.1670 | 7.0334  | 7.5286  | 10          |

### Invariants (configuration parameters that are the same for all runs) ###

| category       | short-name  |
| -------------- | ----------- |
| implementation | js          |
| compiler       | browserify  |
| platform       | ubuntu-deer |
| environment    | chromium38  |
| input-size     | medium      |

### Results ###

| benchmark | mean    | std       | min     | max     | repetitions |
| --------- | ------- | --------- | ------- | ------- | ----------- |
| bfs       | 0.2334s | +-0.0052s | 0.2264s | 0.2474s | 40          |
| backprop  | 1.4851s | +-0.0574s | 1.3977s | 1.6454s | 40          |
| nw        | 1.1394s | +-0.0754s | 1.0563s | 1.2915s | 40          |
| crc       | 1.3389s | +-0.0500s | 1.2884s | 1.5035s | 40          |
| fft       | 3.3252s | +-0.1239s | 3.1856s | 3.8797s | 40          |
| hmm       | 3.6497s | +-0.1197s | 3.5381s | 3.9495s | 40          |
| lavamd    | 0.7429s | +-0.0080s | 0.7291s | 0.7791s | 40          |
| nqueens   | 4.4390s | +-0.0833s | 4.3260s | 4.7550s | 40          |
| pagerank  | 0.4421s | +-0.0137s | 0.4333s | 0.5201s | 40          |
| spmv      | 2.0003s | +-0.0167s | 1.9683s | 2.0467s | 40          |
| srad      | 7.3764s | +-0.0569s | 7.3139s | 7.5768s | 40          |

NOTE:Compatibility problem Chromium 38 for ndarray library in Lud benchmark



# Firefox 34

| category       | short-name  |
| -------------- | ----------- |
| implementation | js          |
| compiler       | browserify  |
| platform       | ubuntu-deer |
| environment    | firefox34   |
| input-size     | medium      |

### Results ###
| benchmark | mean    | std       | min     | max     | repetitions |
| --------- | ------- | --------- | ------- | ------- | ----------- |
| backprop  | 1.8031s | +-0.0364s | 1.6898s | 1.8521s | 30          |
| bfs       | 0.2201s | +-0.0023s | 0.2168s | 0.2258s | 30          |
| crc       | 2.7744s | +-0.0473s | 2.7378s | 2.9896s | 30          |
| fft       | 4.1097s | +-0.0627s | 4.0009s | 4.2117s | 30          |
| hmm       | 4.4997s | +-0.0511s | 4.4195s | 4.6114s | 30          |
| lavamd    | 2.0716s | +-0.0343s | 2.0220s | 2.1302s | 30          |
| nqueens   | 5.1704s | +-0.0976s | 5.0370s | 5.4120s | 30          |
| nw        | 0.9458s | +-0.0604s | 0.7689s | 1.0264s | 30          |
| srad      | 7.4233s | +-0.4662s | 6.2080s | 7.8199s | 30          |
| pagerank  | 0.4931s | +-0.1333s | 0.4335s | 0.8528s | 30          |
| spmv      | 1.2013s | +-0.0724s | 1.1385s | 1.5554s | 30          |

NOTE:Compatibility problem Firefox 34.0 for ndarray library in Lud benchmark

### Invariants (configuration parameters that are the same for all runs) ###

| category    | short-name  |
| ----------- | ----------- |
| platform    | ubuntu-deer |
| environment | firefox57   |
| input-size  | medium      |

### Results ###

| benchmark | implementation | compiler   | mean    | std       | min     | max     | repetitions |
| --------- | -------------- | ---------- | ------- | --------- | ------- | ------- | ----------- |
| backprop  | js             | browserify | 1.7117s | +-0.0177s | 1.6851s | 1.7496s | 30          |
| backprop  | c              | wasm       | 0.7635s | +-0.0099s | 0.7500s | 0.7930s | 30          |
| lud       | js             | browserify | 1.1933s | +-0.0660s | 1.1300s | 1.4780s | 30          |
| lud       | c              | wasm       | 0.7420s | +-0.0652s | 0.6930s | 1.0220s | 30          |
| bfs       | js             | browserify | 0.2154s | +-0.0050s | 0.2119s | 0.2328s | 30          |
| bfs       | cpp            | wasm       | 0.1102s | +-0.0018s | 0.1080s | 0.1160s | 30          |
| crc       | js             | browserify | 2.5821s | +-0.0318s | 2.5515s | 2.6758s | 30          |
| crc       | c              | wasm       | 1.0372s | +-0.0126s | 1.0130s | 1.0670s | 30          |
| fft       | c              | wasm       | 0.8628s | +-0.0279s | 0.8210s | 0.9590s | 30          |
| fft       | js             | browserify | 1.6278s | +-0.0260s | 1.6024s | 1.7128s | 30          |
| hmm       | js             | browserify | 4.1518s | +-0.0702s | 4.0194s | 4.4509s | 90          |
| hmm       | c              | wasm       | 1.9910s | +-0.0462s | 1.8740s | 2.1470s | 31          |
| lavamd    | js             | browserify | 1.2316s | +-0.0154s | 1.2102s | 1.2648s | 30          |
| lavamd    | c              | wasm       | 1.3826s | +-0.0432s | 1.2740s | 1.4960s | 30          |
| nw        | js             | browserify | 0.8966s | +-0.0183s | 0.8660s | 0.9476s | 30          |
| nw        | c              | wasm       | 0.7355s | +-0.0222s | 0.6320s | 0.7620s | 30          |
| nqueens   | js             | browserify | 5.6643s | +-0.1832s | 5.3630s | 6.3180s | 30          |
| nqueens   | c              | wasm       | 3.6386s | +-0.0653s | 3.5690s | 3.8010s | 30          |
| pagerank  | js             | browserify | 0.4001s | +-0.0148s | 0.3858s | 0.4332s | 30          |
| pagerank  | c              | wasm       | 0.2919s | +-0.0123s | 0.2500s | 0.3270s | 30          |
| spmv      | js             | browserify | 1.3705s | +-0.0280s | 1.3312s | 1.4346s | 30          |
| spmv      | c              | wasm       | 0.9242s | +-0.0386s | 0.8990s | 1.0860s | 30          |
| srad      | js             | browserify | 7.3579s | +-0.1458s | 7.1386s | 7.6458s | 30          |
| srad      | c              | wasm       | 3.5365s | +-0.0674s | 3.4730s | 3.7650s | 30          |
# Chrome 63
### Invariants (configuration parameters that are the same for all runs) ###

| category    | short-name  |
| ----------- | ----------- |
| platform    | ubuntu-deer |
| environment | chrome63    |
| input-size  | medium      |
platform=ubuntu-deer,environment=chrome63,input-size=medium.csv

### Results ###

| benchmark | implementation | compiler   | mean    | std    | min     | max     | repetitions |
| --------- | -------------- | ---------- | ------- | ------ | ------- | ------- | ----------- |
| backprop  | js             | browserify | 1.4103  | 0.0064 | 1.4015  | 1.4245  | 10          |
| backprop  | c              | wasm       | 0.7691  | 0.0040 | 0.7640  | 0.7760  | 10          |
| bfs       | cpp            | wasm       | 0.1496  | 0.0020 | 0.1480  | 0.1550  | 10          |
| bfs       | js             | browserify | 0.2757  | 0.0017 | 0.2718  | 0.2781  | 10          |
| crc       | c              | wasm       | 1.2013  | 0.0137 | 1.1880  | 1.2250  | 10          |
| crc       | js             | browserify | 0.9827  | 0.0300 | 0.9053  | 1.0232  | 10          |
| fft       | c              | wasm       | 1.0798  | 0.0366 | 1.0420  | 1.1670  | 10          |
| fft       | js             | browserify | 4.9922  | 0.0794 | 4.9002  | 5.1127  | 10          |
| hmm       | c              | wasm       | 2.4696  | 0.0818 | 2.4240  | 2.6980  | 10          |
| hmm       | js             | browserify | 4.0027  | 0.0188 | 3.9736  | 4.0314  | 10          |
| lavamd    | c              | wasm       | 1.3137  | 0.0221 | 1.2870  | 1.3580  | 10          |
| lavamd    | js             | browserify | 1.6998  | 0.0728 | 1.6596  | 1.8891  | 10          |
| lud       | c              | wasm       | 0.8495  | 0.1167 | 0.7990  | 1.1810  | 10          |
| lud       | js             | browserify | 1.2311  | 0.0459 | 1.1870  | 1.3290  | 10          |
| nqueens   | c              | wasm       | 3.9922  | 0.0617 | 3.9520  | 4.1550  | 10          |
| nqueens   | js             | browserify | 6.0809  | 0.0218 | 6.0450  | 6.1270  | 10          |
| nw        | c              | wasm       | 0.5750  | 0.0017 | 0.5730  | 0.5780  | 10          |
| nw        | js             | browserify | 0.9503  | 0.0072 | 0.9427  | 0.9648  | 10          |
| pagerank  | c              | wasm       | 0.7809  | 0.0049 | 0.7780  | 0.7940  | 10          |
| pagerank  | js             | browserify | 0.8708  | 0.0033 | 0.8656  | 0.8776  | 10          |
| spmv      | c              | wasm       | 0.9746  | 0.0150 | 0.9640  | 1.0160  | 10          |
| spmv      | js             | browserify | 23.5353 | 0.1895 | 23.4073 | 24.0321 | 10          |
| srad      | c              | wasm       | 3.7024  | 0.0208 | 3.6580  | 3.7370  | 10          |
| srad      | js             | browserify | 7.1341  | 0.1670 | 7.0334  | 7.5286  | 10          |



# Node 
| category    | short-name              |
| ----------- | ----------------------- |
| platform    | ubuntu-deer             |
| environment | node-remote-ubuntu-deer |
| input-size  | medium                  |
| file |platform=ubuntu-deer,environment=node-remote-ubuntu-deer,input-size=medium.csv |


### Results ###

| benchmark | implementation | compiler    | mean(s) | std(s) | min(s)  | max(s)  | repetitions |
| --------- | -------------- | ----------- | ------- | ------ | ------- | ------- | ----------- |
| backprop  | c              | server-wasm | 4.4377  | 0.0667 | 4.4180  | 4.7650  | 30          |
| backprop  | js             | browserify  | 1.4221  | 0.0067 | 1.4140  | 1.4510  | 30          |
| bfs       | cpp            | server-wasm | 0.1352  | 0.0022 | 0.1330  | 0.1440  | 30          |
| bfs       | js             | browserify  | 1.3297  | 0.0678 | 1.3070  | 1.6870  | 30          |
| crc       | c              | server-wasm | 1.0244  | 0.0464 | 1.0090  | 1.2000  | 30          |
| crc       | js             | browserify  | 0.9001  | 0.0422 | 0.8860  | 1.0740  | 30          |
| fft       | c              | server-wasm | 0.9658  | 0.1113 | 0.9330  | 1.5540  | 30          |
| fft       | js             | browserify  | 3.3655  | 0.0619 | 3.3320  | 3.5650  | 30          |
| hmm       | c              | server-wasm | 47.4534 | 0.1952 | 47.3260 | 48.3060 | 30          |
| hmm       | js             | browserify  | 47.6717 | 0.2106 | 47.4280 | 48.2050 | 30          |
| lavamd    | c              | server-wasm | 1.2746  | 0.0221 | 1.2640  | 1.3550  | 30          |
| lavamd    | js             | browserify  | 3.7620  | 0.0871 | 3.7140  | 4.1460  | 30          |
| lud       | c              | server-wasm | 0.8331  | 0.0096 | 0.8140  | 0.8650  | 30          |
| lud       | js             | browserify  | 1.3525  | 0.0421 | 1.2760  | 1.4460  | 30          |
| nqueens   | c              | server-wasm | 4.0442  | 0.1830 | 3.9890  | 5.0060  | 30          |
| nqueens   | js             | browserify  | 6.1517  | 0.0904 | 6.0130  | 6.5300  | 30          |
| nw        | c              | server-wasm | 0.5452  | 0.0027 | 0.5440  | 0.5590  | 30          |
| nw        | js             | browserify  | 1.0017  | 0.0106 | 0.9920  | 1.0540  | 30          |
| pagerank  | c              | server-wasm | 0.3306  | 0.0033 | 0.3270  | 0.3470  | 30          |
| pagerank  | js             | browserify  | 0.5890  | 0.0195 | 0.5770  | 0.6860  | 30          |
| spmv      | c              | server-wasm | 22.0882 | 0.0706 | 22.0400 | 22.3000 | 30          |
| spmv      | js             | browserify  | 23.5859 | 0.2007 | 23.3810 | 24.0690 | 60          |
| srad      | c              | server-wasm | 47.7410 | 1.6126 | 47.3150 | 56.2610 | 30          |
| srad      | js             | browserify  | 55.8755 | 0.3237 | 55.5240 | 56.6780 | 30          |

# Native

### Invariants (configuration parameters that are the same for all runs) ###

| category    | short-name         |
| ----------- | ------------------ |
| platform    | ubuntu-deer        |
| environment | native |
| input-size  | medium             |
platform=ubuntu-deer,environment=native-ubuntu-deer,input-size=medium.csv

### Results ###

| benchmark | implementation | compiler | mean   | std    | min    | max    | repetitions |
| --------- | -------------- | -------- | ------ | ------ | ------ | ------ | ----------- |
| backprop  | c              | gcc      | 0.4434 | 0.0016 | 0.4409 | 0.4456 | 10          |
| bfs       | cpp            | g++      | 0.1044 | 0.0021 | 0.1034 | 0.1103 | 10          |
| crc       | c              | gcc      | 0.7556 | 0.0434 | 0.7295 | 0.8707 | 10          |
| fft       | c              | gcc      | 1.1289 | 0.0133 | 1.1146 | 1.1559 | 10          |
| hmm       | c              | gcc      | 1.8158 | 0.0286 | 1.7817 | 1.8584 | 10          |
| lavamd    | c              | gcc      | 3.4651 | 0.0375 | 3.4261 | 3.5436 | 10          |
| lud       | c              | gcc      | 0.6026 | 0.0290 | 0.5703 | 0.6494 | 10          |
| nqueens   | c              | gcc      | 2.7059 | 0.0378 | 2.6663 | 2.7734 | 10          |
| nw        | c              | gcc      | 0.1007 | 0.0073 | 0.0954 | 0.1142 | 10          |
| pagerank  | c              | gcc      | 0.6023 | 0.1622 | 0.1705 | 0.7113 | 10          |
| spmv      | c              | gcc      | 0.6596 | 0.0289 | 0.6275 | 0.7191 | 10          |
| srad      | c              | gcc      | 2.8692 | 0.0346 | 2.8310 | 2.9532 | 10          |
