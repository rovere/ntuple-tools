**General settings**

verbosity_level:  0

### range of ntuples to test (will be appended to the inputPath string below)
min_Ntuple:  1
max_Ntuple:  3

### stop analyzing each ntuple after that many events: 
analyze_events_per_tuple:	30

### input and output paths

input_path: ../../data/MultiParticleInConeGunProducer_PDGid22_nPart1_Pt6p57_Eta2p2_InConeDR0p10_PDGid22_predragm_cmssw1020pre1_20180730/NTUP/partGun_PDGid22_x96_Pt6.57To6.57_NTUP_

output_path: ../clusteringResultsCXX/geneticOptimizer/

score_output_path: tmp/output.txt

**HGCal Imaging Algo parameters**

### should detector thickness be taken into account?
depend_sensor:	0

### Energy density inclusion funciton. Defines a way to include or reject hit when calculating local energy density.
### Possible options:
### *step* - include 100% of hit energy if distance smaller than *critical_distance*  
### *gaus* - include fraction of hit's energy based on the distance scaled by a gaussian distribution with width *critical_distance*
### *exp* - exponential for distances smaller than *critical_distance*, don't include above

energy_density_function:  step


### Critical distance for energy density ρ calculation (in cartesian coordiantes in cm, separately for each detector)
### Hits that are further than d_c from given hit will not be included in the energy density calculation for this hit.
critial_distance_EE:	15.0
critial_distance_FH:	18.7
critial_distance_BH:	37.0

### Critical distance to higher ρ hit (in cartesian coordiantes in cm, separately for each detector)
### Hits that are further than δ_c from any hit with higher ρ will be considered as potential cluster seeds.
deltac_EE:	7.5
deltac_FH:	32.5
deltac_BH:	12.5

### Critical energy density is defined as ρ_c = max(ρ)/κ. Hits with ρ > ρ_c will be considered as potential cluster seeds.
kappa:  124.1

### cut on energy (relative to the noise):
energy_min:	0.019

### Request at least minClusters+1 2D clusters  (*clarification needed*)
min_clusters:	5

### test only within this layers range:
min_layer: 0
max_layer: 52

### Include only events were all particles reached EE before converting
reachedEE_only:	1


**Cluster Matching parameters**

### Sim clusters further than matching_max_distance from the clostest rec cluster will not be matched 
matching_max_distance:	17.0

