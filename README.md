# pfp-thresholds
Computing thresholds from Prefix-free parsing
Forked from https://github.com/maxrossi91/pfp-thresholds to add run-length encoding setting and augmented thresholds computation.

## Download

```console
git clone https://github.com/drnatebrown/pfp-thresholds
```

## Compile

```console
mkdir build
cd build; cmake ..
make
```

### Debug

```console
mkdir build
cd build; cmake -DCMAKE_BUILD_TYPE=Debug ..
make
```

## Contents

### LCP computation

* `pfp_lcp`: Build array storing pairs $min(LCP[i..j-1])$ and $min(LCP[j+1..k])$ where $j$ is a threshold, $i$ is the end of previous corresponding run, and $k$ is the start of the next corresponding run. See [aug_phoni](https://github.com/drnatebrown/aug_phoni)

### Thresholds computation

* `pfp_thrersolds`: build the thresholds from the prefix-free parsing. (`BigBWT`, `pfp_thresholds.cpp`)

* `gsacak_thresholds`: build the thresholds using `gsacak`. (`gsacak`)

* `bwt_lcp_thresholds`: build the thresholds using `RLBWT2LCP`. (`BigBWT`,`RLBWT2LCP`)

### Matching Statistics

* `matching_statistics`: computes the matching statistics from the BWT and the thresholds, using the parsing for random access.

* `sdsl_matching_statistics`: computes the matching statistics from the text using `sdsl`.

## Authors 

### Theoretical results:

* Christina Boucher
* Travis Gagie
* Massimiliano Rossi

### Implementation:

* Massimiliano Rossi

### Experiments:

* Massimiliano Rossi
* Marco Oliva
