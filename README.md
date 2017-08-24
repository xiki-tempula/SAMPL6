# The SAMPL6 Blind Prediction Challenge for Computational Chemistry

This repository gives challenge details and inputs for the SAMPL6 challenge. 
This cycle we have migrated the data download package to GitHub so it will be version controlled and more broadly acccessible.
**Because these files are available publicly, we have no record of who downloads them. Therefore, you should sign up for notifications**.
Specifically, if you want to receive updates if we uncover any problems, it is imperative that you either (a) sign up for the SAMPL e-mail list via the D3R site, or (b) sign up for notifications of changes to this GitHub repository (the ``Watch'' button, above); ideally you would do both. 

## What's Here
- [Challenge Overview](#challenge-overview)
- `host_guest`: Directory containing inputs for the host-guest challenges, as well as supporting files and a README detailing their organization
- [Host-guest challenge instructions](host_guest_instructions.md): Detailed instructions on the host-guest component of the challenge.
- [Detailed host-guest description](host_guest_description.md): Detailed description of the hosts, guests, and background information.

## What's forthcoming
- Physical property challenge files (see description, below) 
- SAMPLing challenge files (see description, below) for both host-guest and physical properties
 
## Challenge Overview 
(This is reproduced from the [SAMPL6 Website](https://drugdesigndata.org/about/sampl6))

SAMPL6 includes challenges based on aqueous host-guest binding data (binding free energies and, optionally, binding enthalpies) for three different host molecules; and on physical properties (distribution coefficients and possibly solubilities), for a set of fragment-like molecules.
The host-guest systems are useful to test simulation methods, force fields, and solvent models, in the context of binding, without posing the setup issues and computational burden of protein simulations.
The physical properties offer efficient tests of force field accuracy when detailed simulations are used, and can also test pKa prediction methods, continuum solvation models, and knowledge-based prediction methods.
SAMPL6 will also introduce a new challenge component, the “SAMPLing challenge”, in which computational methods will be evaluated on how efficiently their calculations approach well-converged reference results generated by the organizers.
Participants will be provided with machine readable setup files for the molecular systems, including force field setups, along with recommended cutoffs and treatments of long-ranged interactions.
The SAMPLing challenge is expected to include one or more cases from each challenge component (host-guest binding on each system; log D calculation).

**As of August 24, all of the information and data files needed to start on the host-guest component, including machine-readable structure files for the hosts and guests are posted, so this challenge is open!
Files are hosted at github.com/mobleylab/SAMPL6.**
We estimate that the physical property and SAMPling parts of SAMPL6 will open in October 15, 2017 and September 20, 2017, respectively.
Status updates will be posted here and announced by email to the D3R SAMPL list and on the D3R Twitter account; we also encourage participants to “watch” the GitHub repository for notifications of file changes/availability and relevant discussions.

Further information on both the host-guest and physical property components of SAMPL6 follow. 
Thanks to Drs. Bruce Gibb (Tulane U.) and Lyle Isaacs (U. Maryland) for providing the host-guest data, and Dr. John Chodera, Mehtap Isik, and Merck for the distribution coefficient data.

### Gibb Deep Cavity Cavitand (Octa Acids) binding of guests

One host-guest series is based on the Gibb Deep Cavity Cavitands (GDCCs), or octa-acids, previously used in SAMPL4 and SAMPL5.
The two hosts, OA and TEMOA (previously OAH and OAME) are identical, except that TEMOA has four additional methyl groups, which alter the shape and depth of the hydrophobic cavity.
Both were developed in the laboratory of Dr. Bruce Gibb (Tulane U), who will provide binding free energies and enthalpies, measured by ITC, for eight guest molecules interacting with each host.
The measurements are done in 10 mM sodium phosphate buffer at pH 11.7 ± 0.1, and T = 298 K.
Host OA is described here: doi:10.1021/ja200633d; and host TEMOA is described here doi:10.1007/s10822-013-9690-2.
There are also a number of papers from SAMPL4 and SAMPL5 which discuss calculations for these systems, as summarized, respectively, in doi:10.1007/s10822-014-9735-1 and doi:10.1007/s10822-016-9974-4.
Existing benchmark datasets based on these hosts also may be of interest for those preparing to tackle these new complexes: https://github.com/MobleyLab/benchmarksets; this ``perpetual'' review paper also provides a good introduction to the sampling and experimental issues which are known to be relevant in these systems. 

### Cucubit[8]uril (CB8) binding of guests

This host-guest series is based on the host cucurbit[8]uril (CB8), which was used in SAMPL3, as previously summarized (DOI 10.1007/s10822-012-9554-1).
CB8 is the eight-membered relative of cucurbit[7uril, which was used in several other prior SAMPL challenges.
Data will be provided for ~14 guests, including several FDA approved drugs.
Background information on CB8 may be found in a number of publications, including DOI 10.1021/jp2110067, 10.1002/chem.201403405, and 10.1021/ja055013x.

### Physical properties
The SAMPL6 physical property challenge will center on predicting physicochemical properties for 25-50 fragment- and drug-like small molecules that small molecule protein kinase inhibitors (or fragments thereof).
Because the SAMPL5 logD challenge highlighted the difficulty in correctly predicting transfer free energies involving protonation states, we will provide participants with experimental pKa values for these compounds.
We will ask participants to predict distribution coefficients (logD) at a single pH and (as a separate challenge), provided the measurements can be completed in time, pH-dependent solubilities for these compounds.

The experimental data being measured include pKa values, measured by electrochemical and/or UV-metric titration; and pH-dependent distribution coefficients (logD) of one or both of the following types:
- water and cyclohexane (as in SAMPL5) 
- water and octanol (new in SAMPL6) 

There is also a possibility that solubilities will be measured, using the CheqSol method. All of these measurements will be performed on Sirius T3 instruments from Sirius Analytical at Merck’s Rahway site.
The exact size of the dataset will depend on practical data collection throughput.
An initial batch of ~25 fragment-like compounds is currently being assayed, with the prospect for additional measurements performed subsequently.
Post-challenge follow-up experiments are possible and will be conducted as needed.
We hope to provide a preliminary list of compounds by September 15 to allow participants to begin planning. The final challenge will include logD and, if available, solubility prediction.


Distribution coefficients were included in the SAMPL5 challenge (overview doi:10.1007/s10822-016-9954-8 and experiment doi:10.1007/s10822-016-9971-7; JCAMD special issue https://link.springer.com/journal/10822/30/11/page/1); in many cases, they were predicted as if they were partition coefficients, using solvation free energies in the relevant solvents.
The difference between distribution coefficients (logD, which reflects the transfer free energy at a given pH including the effects of accessing all equilibrium  protonation states of the solute in each phase) and partition coefficients (logP, which reflects the free energy of transfer for the neutral form only) proved particularly important.
In some cases, other effects like the presence of small amount of water in cyclohexane may also have played a role.
