## The test of DiffDock-Pocket

I tried two types of commands:
1) with all the residues as flexible
2) with no flexible residue

Both of them ran about 20 hours on the cluster (8 GPUs), and for the fasudil and ligand47, most of the frames failed ( I'm trying to figure it out). For the ligand 23,
The success rate is over 90% but I haven't validated the credibility of these results.


# Updated 
I found this tool can only change the torsion of the bonds in the side chains, but cannot change the secondary structure,
which means the shape of the protein can only be changed in a limited range but cannot be changed thoroughly.

## ligand23
For ligand23, it ran very well, the ligands can interact with the protein and don't collide.
<img width="644" height="446" alt="Screenshot from 2025-12-02 14-35-29" src="https://github.com/user-attachments/assets/ad12b7f5-5706-424e-8966-8e417a4708f7" />

But for ligand47 and fasudil, I solved problem that their ligand atoms will seperate by changing the input file from pdb to sdf(with charge), but still failed to locate
these ligands position ( they are so far away  from the protein )
