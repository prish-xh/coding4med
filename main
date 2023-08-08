def translate_codon(codon):
    genetic_code = {
        "ATA": "I", "ATC": "I", "ATT": "I", "ATG": "M",
        "ACA": "T", "ACC": "T", "ACG": "T", "ACT": "T",
        "AAC": "N", "AAT": "N", "AAA": "K", "AAG": "K",
        "AGC": "S", "AGT": "S", "AGA": "R", "AGG": "R",
        "CTA": "L", "CTC": "L", "CTG": "L", "CTT": "L",
        "CCA": "P", "CCC": "P", "CCG": "P", "CCT": "P",
        "CAC": "H", "CAT": "H", "CAA": "Q", "CAG": "Q",
        "CGA": "R", "CGC": "R", "CGG": "R", "CGT": "R",
        "GTA": "V", "GTC": "V", "GTG": "V", "GTT": "V",
        "GCA": "A", "GCC": "A", "GCG": "A", "GCT": "A",
        "GAC": "D", "GAT": "D", "GAA": "E", "GAG": "E",
        "GGA": "G", "GGC": "G", "GGG": "G", "GGT": "G",
        "TCA": "S", "TCC": "S", "TCG": "S", "TCT": "S",
        "TTC": "F", "TTT": "F", "TTA": "L", "TTG": "L",
        "TAC": "Y", "TAT": "Y", "TAA": "*", "TAG": "*",
        "TGC": "C", "TGT": "C", "TGA": "*", "TGG": "W",
    }
    return genetic_code[codon]

def translate(dna_sequence):
    protein_sequence = ""
    codon = ""

    start_index = dna_sequence.find("ATG")
    if start_index == -1:
        return "No start codon found"

    for i in range(start_index, len(dna_sequence), 3):
        codon = dna_sequence[i:i + 3]
        if codon in ["TAA", "TAG", "TGA"]:
            break
        protein_sequence += translate_codon(codon)

    return protein_sequence

dna_sequence = "ATGAAACGCATTAGCACCACCATTACCACCACCATCACCATTACCACAGGTAACGGTGCGGGCTGA"
protein_sequence = translate(dna_sequence)

print("Protein sequence:", protein_sequence)
