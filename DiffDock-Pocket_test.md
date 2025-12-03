## The test of DiffDock-Pocket

I tried two types of commands:
1) with all the residues as flexible
2) with no flexible residue

Both of them ran about 20 hours on the cluster (8 GPUs), and for the fasudil and ligand47, most of the frames failed ( I'm trying to figure it out). For the ligand 23,
The success rate is over 90% but I haven't validated the credibility of these results.


# Updated 
### 12022025
I found this tool can only change the torsion of the bonds in the side chains, but cannot change the secondary structure,
which means the shape of the protein can only be changed in a limited range but cannot be changed thoroughly.

## ligand23
For ligand23, it ran very well, the ligands can interact with the protein and don't collide.
but the program only changes a very limited amount of side chain 
<img width="644" height="446" alt="Screenshot from 2025-12-02 14-35-29" src="https://github.com/user-attachments/assets/ad12b7f5-5706-424e-8966-8e417a4708f7" />
<img width="624" height="537" alt="Screenshot from 2025-12-02 14-47-56" src="https://github.com/user-attachments/assets/f1e3a2e2-3724-4696-8d66-cb9948de804b" />
<img width="577" height="388" alt="Screenshot from 2025-12-02 14-51-05" src="https://github.com/user-attachments/assets/dcdfb359-f671-499e-aa6a-550f0e99f690" />
<img width="661" height="400" alt="Screenshot from 2025-12-02 14-54-23" src="https://github.com/user-attachments/assets/4044b2b9-8e41-44b1-8715-3d55cdbdc1e2" />



But for ligand47 and fasudil, I solved problem that their ligand atoms will seperate by changing the input file from pdb to sdf(with charge), but still failed to locate
these ligands position ( they are so far away  from the protein that I even can't put them into one screenshot)
I think this problem might be caused by the seven-membered ring in both fasudil and ligand47 which ligans23 dosen't have.
