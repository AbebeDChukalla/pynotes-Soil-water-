# Import Tabular Data

Loading data is an essential step when using Python for scientific data analysis. In this tutorial we will cover three ways of importing data. This tutorial will not focus on how to access or analyze the data.

## Function arguments

`"r"` - Read (default

`"a"` - Append

`"w"` - Write

`"x"` - Creates the specified file

`"t"` - Text - Default

`"b"` - Binary (e.g. images)

Source: <https://www.w3schools.com/python/python_file_handling.asp>


```python
# Read data
dna_list = open("../datasets/dna_sequence.txt", "r").read().split('\n')
print(dna_list[0:10])

```

    ['LOCUS: SCU49845', 'ACCESSION: U49845', "ORGANISM: Saccharomyces cerevisiae (baker's yeast)          ", 'AUTHORS: Roemer,T., Madden,K., Chang,J. and Snyder,M.', 'TITLE: Selection of axial growth sites in yeast requires Axl2p, a novel plasma membrane glycoprotein', 'JOURNAL: Genes Dev. 10 (7), 777-793 (1996)', 'PUBMED: 8846915', 'SOURCE: https://www.ncbi.nlm.nih.gov/nuccore/U49845.1?report=genbank&to=5028', 'GATCCTCCATATACAACGGTATCTCCACCTCAGGTTTAGATCTCAACAACGGAACCATTGCCGACATGAG', 'ACAGTTAGGTATCGTCGAGAGTTACAAGCTAAAACGAGCAGTAGTCAGCTCTGCATCTGAAGCCGCTGAA']



```python
# Using a list comprehension
dna_list = [line.strip('\n') for line in open("../datasets/dna_sequence.txt","r")]
print(dna_list[0:10])

```

    ['LOCUS: SCU49845', 'ACCESSION: U49845', "ORGANISM: Saccharomyces cerevisiae (baker's yeast)          ", 'AUTHORS: Roemer,T., Madden,K., Chang,J. and Snyder,M.', 'TITLE: Selection of axial growth sites in yeast requires Axl2p, a novel plasma membrane glycoprotein', 'JOURNAL: Genes Dev. 10 (7), 777-793 (1996)', 'PUBMED: 8846915', 'SOURCE: https://www.ncbi.nlm.nih.gov/nuccore/U49845.1?report=genbank&to=5028', 'GATCCTCCATATACAACGGTATCTCCACCTCAGGTTTAGATCTCAACAACGGAACCATTGCCGACATGAG', 'ACAGTTAGGTATCGTCGAGAGTTACAAGCTAAAACGAGCAGTAGTCAGCTCTGCATCTGAAGCCGCTGAA']

