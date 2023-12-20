# MethylationDetection


MethylationDetection is an integrative pipeline to methylation analysis from raw paired-end sequences obtained from massive parallel bisulfite sequencing.
## Installation

**Dependencies**
* [Bowtie2 v2.4.5](http://bowtie-bio.sourceforge.net/bowtie2/manual.shtml#building-from-source)
* [Bismark v0.23.0](https://www.bioinformatics.babraham.ac.uk/projects/bismark/)
* [fastqc v0.11.9](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
* [TrimGalore v0.6.6](https://github.com/FelixKrueger/TrimGalore)
* [wget v1.21.2](https://www.gnu.org/software/wget/)
* [curl v7.81.0](https://curl.se/)
* UnZip v6.0
* [cutadapt v3.5](https://cutadapt.readthedocs.io/en/stable/installation.html)

**Local installation**
For the installation is necessary to install all the dependencies detailed in greater detail in the documentation
Once the dependencies are installed, move the dependencies in the scr folder to the $PATH (usually `/usr/bin/`)

```
git clone https://github.com/UBIMED-Lab13/MethylationDetection.git
cd MethylationDetection
sudo find . -maxdepth 1 -type f ! -name "README.md" -exec cp {} $PATH \;
```

## Example
To run it we made a demonstration to facilitate its use
```
wget -O example.zip https://sourceforge.net/projects/automethycexample/files/latest/download
unzip example.zip && cd example
mkdir output
methylationdetection -i FastqSamples -r [hg19_reference_genome_file] -o output
```
