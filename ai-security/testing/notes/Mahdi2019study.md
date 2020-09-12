## DL Oracle

### Motivation
1. There is little work on the quality assurance on DL framework tesing.
2. The source of the OA and the sufference threshold in DL testing is hard to choose.

### Effect
1. They have done relatively adequate research on the use of OA, code changes and reasons.

### Detail
1. why has OA:
    Machine representation error;Mathematical approximation error;
    Defects in implementations;
    Modeling error;
    Physical measurement error
2. how to find OA:
    AST: abstract syntax and the conrresponding assert method.

After the authors analyzed the OA munually, they design 5 labels: 
    manually defined (D), differential
    testing (DT), a naive implementation (NI), a relevant internal
    function (RI), and the same code under test (SCUT).

3. They designed a automatic method to collect the OA update message in the github commits.
commit--> OA line --> OA type

4. TO understand the commit on OA, they categorized the commits based on the effects of code changes and reasons
behind.
