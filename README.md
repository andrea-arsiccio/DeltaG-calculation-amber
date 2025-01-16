# DeltaG-calculation

The python script DeltaG-calculation.py can be used to compute transfer free energies that describe the transfer of a protein from water at 298 K and 1 bar to different osmolyte solutions [1], at any temperature [2] and pressure [3] value.

Usage:

python3 DeltaG-calculation.py osmolyte-type osmolyte-concentration T-value T-approach P

where:

osmolyte-type: can be sucrose, urea, TMAO, proline, betaine or none. In all cases, free-energy values extracted from the work by Auton, Bolen and coworkers are employed [4].

osmolyte-concentration: concentration of the selected osmolyte, in M.

T-value: temperature value, in K.

T-approach: can be 2 or 3. Refers to the approaches for the inclusion of temperature effects in implicit solvent simulations described in [2].

P: pressure value, in bar. 

Example:

python3 DeltaG-calculation.py sucrose 1 310 2 3500 

computes the free energies of transfer for a protein in 1M sucrose, at 310 K (using approach 2 as described in [2]) and 3500 bar.

The output is a file DeltaG.dat in the form:


ala = -0.24272932268485, arg = -0.7089564542301577, asn = -0.37067584949673443, asp = 0.04007902770858002, cys = -0.3716866186409432, gln = -0.17884882773338417, glu = -0.3694063983760302, gly = 0.0, his = -0.29395542554681126, hip = -0.29395542554681126, ile = -1.041274851791287, leu = -1.6238248000845537, lys = -0.31918037153745527, met = -0.5594681334419379, phe = -1.5261859676423817, pro = -0.20899177523812199, ser = 0.6753963064483499, thr = -0.0243360337647955, triptophan = -1.885635099985589, tyr = -1.1033755628133617, valine = -0.8958783807836065, bb = 0.2806966350996659


where free energy of transfer values, in kJ/mol, are provided for each sidechain/backbone. The output is compatible for use with Amber.

REFERENCES:

[1] Arsiccio, Andrea; Ganguly, Pritam; Shea, Joan-Emma (2022): A Transfer Free Energy Based Implicit Solvent Model for Protein Simulations in Solvent Mixtures: Urea-Induced Denaturation as a Case Study. In The Journal of Physical Chemistry B 126 (24), pp. 4472–4482. DOI: 10.1021/acs.jpcb.2c00889.

[2] Arsiccio, Andrea; Shea, Joan-Emma (2021): Protein Cold Denaturation in Implicit Solvent Simulations: A Transfer Free Energy Approach. In The Journal of Physical Chemistry B 125 (20), pp. 5222–5232. DOI: 10.1021/acs.jpcb.1c01694.

[3] Arsiccio, Andrea; Shea, Joan-Emma (2021a): Pressure Unfolding of Proteins: New Insights into the Role of Bound Water. In The Journal of Physical Chemistry B 125 (30), pp. 8431–8442. DOI: 10.1021/acs.jpcb.1c04398.

[4] Auton, Matthew; Bolen, D. Wayne (2007): Application of the Transfer Model to Understand How Naturally Occurring Osmolytes Affect Protein Stability. In D. Häussinger, H. Sies (Eds.): Methods in enzymology. Volume 428, Osmosensing and osmosignaling, vol. 428. Amsterdam, New York: Elsevier (Methods in Enzymology, v. 428), pp. 397–418.
