Issues found during preparations for the Greenland course 26-30.6.2017. To be
solved as part of the week, as an excercise.


# Undefined multichar


```
  HINTRSCT generator-raw-gt-desc.tmp1.hfst
/usr/local/bin/hfst-compose-intersect: warning: 
Found output multi-char symbols ("«7") in 
transducer in file <stdin> which are not found on the
input tapes of transducers in file phonology/kal-phon.rev.hfst.
```


# Zero analysis


```
$ echo inuuissiortunga | hfst-lookup -q src/analyser-gt-desc.hfstol 
0	0
0	0
0	0
0	0
0	0
inuuissiortunga	inuk+U+nv+VIK+vn+SIUR+nv+V+Par+1Sg	0,000000
inuuissiortunga	inuk+U+nv+VIK+vn+SSAQ+nn+LIUR+nv+V+Par+1Sg	0,000000
inuuissiortunga	inuuik+SSAQ+nn+LIUR+nv+V+Par+1Sg	0,000000
inuuissiortunga	inuuik+SIUR+nv+V+Par+1Sg	0,000000
inuuissiortunga	inuuissior+V+Par+1Sg	0,000000
```


and


```
$ echo nalunngilara | hfst-lookup -q src/analyser-gt-desc.hfstol 
0	0
0	0
nalunngilara	nalu+NNGIT+vv+V+Ind+1Sg+3SgO	0,000000
nalunngilara	nalup+NNGIT+vv+V+Ind+1Sg+3SgO	0,000000
```


But not:


```
$ echo inuuissiortoq | hfst-lookup -q src/analyser-gt-desc.hfstol 
inuuissiortoq	inuk+U+nv+VIK+vn+SIUR+nv+TUQ+vn+N+Abs+Sg	0,000000
inuuissiortoq	inuk+U+nv+VIK+vn+SIUR+nv+V+Par+3Sg	0,000000
inuuissiortoq	inuk+U+nv+VIK+vn+SSAQ+nn+LIUR+nv+TUQ+vn+N+Abs+Sg	0,000000
inuuissiortoq	inuk+U+nv+VIK+vn+SSAQ+nn+LIUR+nv+V+Par+3Sg	0,000000
inuuissiortoq	inuuik+SSAQ+nn+LIUR+nv+TUQ+vn+N+Abs+Sg	0,000000
inuuissiortoq	inuuik+SSAQ+nn+LIUR+nv+V+Par+3Sg	0,000000
inuuissiortoq	inuuik+SIUR+nv+TUQ+vn+N+Abs+Sg	0,000000
inuuissiortoq	inuuik+SIUR+nv+V+Par+3Sg	0,000000
inuuissiortoq	inuuissior+TUQ+vn+N+Abs+Sg	0,000000
inuuissiortoq	inuuissior+V+Par+3Sg	0,000000
inuuissiortoq	inuuissiortoq+N+Abs+Sg	0,000000
```
