# DiscoMark

---

Discover phylogenetic markers from orthologous sequences.

---

## Requirements

DiscoMark, uses the following programs:
* [Python](https://www.python.org) (>= 2.7)
* [NCBI Blast+](http://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST) (>= 2.2.29)
* [MAFFT](http://mafft.cbrc.jp/alignment/software) (>= 6.864b)
* [TrimAl](https://github.com/scapella/trimal) (>= 1.2)

For Linux and Mac, we include binary files for BLASTn, MAFFT and TrimAl in the respective `bin/` folders. See the [Installation](#installation) section on how to use them.

Additionally, you'll need the following Python packages:
* [Biopython](http://biopython.org/) (>= 1.62)
* [SqlAlchemy](http://www.sqlalchemy.org/) (>= 0.9)

## Installation

Download DiscoMark (when setting the `PATH` environment variable, replace `linux` with `mac` if you're on a Mac):
```
git clone https://github.com/hdetering/discomark.git
export PYTHONPATH=/path/to/discomark/util/
export PATH=/path/to/discomark/bin/linux:$PATH
```

If you have the programs BLAST+, MAFFT and TrimAl installed on your system you don't need the `export PATH=[...]` statement.

## How to run DiscoMark

Make sure your [input data](https://github.com/hdetering/discomark/wiki#input-data) is properly formatted. 

```
cd discomark
python run_project.py -i example/hamstr/Cloeon -i example/hamstr/Baetis -r example/reference/Cloeon.fasta -d output
```

See the wiki for more info on the [command line options](https://github.com/hdetering/discomark/wiki/Command-Line-Options).


## Results

Inspect the marker report in the output directory at `7_report/discomark_results.html`.  
(In the example above that would be: `output/7_report/discomark_results.html`.)

The primer table can also be found in CSV format in `7_report/primers.xls`.

## Acknowledgements

DiscoMark uses [PriFi](http://cgi-www.cs.au.dk/cgi-chili/PriFi/main) for primer design. We thank [Jakob Fredslund](mailto:jakobf@birc.au.dk), who kindly provided us with the source code to PriFi.
