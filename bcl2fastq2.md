1. Install [bcl2fastq2](https://support.illumina.com/downloads/bcl2fastq-conversion-software-v2-20.html) software.

> As the simplest option, you can install the tool conda. You can refer [this page](https://anaconda.org/bih-cubi/bcl2fastq2).
```bash
conda create -n bcl2fastq -c conda-forge bih-cubi::bcl2fastq2
conda activate bcl2fastq
```

2. Once it is installed, you can test the installation by inserting the command below

```bash
bcl2fastq -h
```

3. Then, move to the `Run folder`. The `Run folder` is the root folder that contains every files from MiSeq. In my case, it was here.
`projects/rrg-whsiao-ab/cidgoh_share/miseq_guano/230830_M05954_0003_000000000-K9KL6`

```bash
cd projects/rrg-whsiao-ab/cidgoh_share/miseq_guano/230830_M05954_0003_000000000-K9KL6
```

4. Finally, simply run the tool.
```bash
bcl2fastq --sample-sheet SampleSheet.csv
```

6. As a output, you can find the generated FASTQ at `Run folder`/Data/Intensities/BaseCalls.
