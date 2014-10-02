Millerplot
==========

Draw linear plots to depict variants.

## Details
This includes ``varplot'', a module that reads in a specification file and 
prints out a linear plot showing the variants in the samples when compared to a 
chosen reference.

The specification should have a header where each line starts with a "@". "@"
should be followed by a tag and value separated by a "=". Currently the
following tags are defined:

- GN, the name of the reference genome/sample.
- GL, the genome length of the genome under consideration.
- GA, the genome annotation for a zero based half-open interval.

The genome annotation should be include the start of the interval, end of the
interval, and optionally the name of the region as well as the type of the
region (such as tRNA, gene, rRNA and so on).

The lines after the header should be one for each genome. The first column
should be the name of the individual/genome followed by the space separated
positions which need to be marked.

An example spec file is shown here

```
@GN=IR_3
@GL=14574
@GA=0:64::tRNA
@GA=64:1035:nad2:gene
@GA=1035:1100::tRNA
@GA=1092:1153::tRNA
@GA=1160:1226::tRNA
@GA=1218:2757:cox1:gene
@GA=2764:3440:cox2:gene
@GA=3440:3509::tRNA
@GA=3508:3574::tRNA
@GA=3574:3730:atp8:gene
@GA=3723:4389:atp6:gene
@GA=4395:5173:cox3:gene
@GA=5173:5236::tRNA
@GA=5236:5572:nad3:gene
@GA=5572:5633::tRNA
@GA=5632:5696::tRNA
@GA=5695:5763::tRNA
@GA=5765:5820::tRNA
@GA=5820:5885::tRNA
@GA=5883:5948::tRNA
@GA=5948:7617:nad5:gene
@GA=7617:7678::tRNA
@GA=7680:8997:nad4:gene
@GA=8990:9266:nad4L:gene
@GA=9268:9330::tRNA
@GA=9330:9395::tRNA
@GA=9397:9826:nad6:gene
@GA=9829:10910:cob:gene
@GA=10910:10976::tRNA
@GA=10993:11912:nad1:gene
@GA=11912:11978::tRNA
@GA=11992:12053::tRNA
@GA=12034:13289:rrnL:gene
@GA=12034:13289:16S:rRNA
@GA=13289:13351::tRNA
@GA=13351:14069:rrnS:gene
@GA=13351:14069:12S:rRNA
@GA=14423:14492::tRNA
@GA=14499:14569::tRNA
@CL=rRNA:#2B83BA
@CL=tRNA:#FFFFBF
@CL=gene:#D7191C
@CL=special:#000000
@CL=indel:#FDAE61
@CL=missing:#ABDDA4
IR_65 2618 3267 3752 7768 8523 special=10177 10848 12790 13157 indel=3500:3560 missing=4000:6000
IR_66 2618 3267 3752 7768 8523 special=10177 10848 12790 13157 missing=4000:6000
IR_63 2618 3267 3752 4883 8523 9798 10848 13157 missing=1:1000
```
