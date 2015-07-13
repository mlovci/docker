#SVM_bpfinder


A simple docker  wrapper for [SVM_bpfinder](http://regulatorygenomics.upf.edu/Software/SVM_BP/).


---

This repository repackages work from these wonderful people:

  - A. Corvelo, M. Hallegger, C.W.J. Smith, E. Eyras. Genome-wide Association between Branch Point Properties and Alternative Splicing. ... (2010) 
  - T. Joachims, Making large-Scale SVM Learning Practical. Advances in Kernel Methods - Support Vector Learning, B. Schölkopf and C. Burges and A. Smola (ed.), MIT-Press, 1999.

##Requirements:

  - `SVM_bp.sh` from this repo
  - [`docker`](http://docker.io/)
  - UNIX-like system, or else you need to replicate the contents of `SVM_bp.sh` for your architecture.

##Installation:

  1. Add `SVM_bp.sh` to a place in $PATH
  2. `docker pull mlovci/svm_bpfinder`

##Test:
You can use test.fa from this repo for testing.

    SVM_bp.sh test.fa Hsap 100

will produce:
  
        seq_id	agez	ss_dist	bp_seq	bp_scr	y_cont	ppt_off	ppt_len	ppt_scr	svm_scr
        intron1	34	29	cgctgacat	3.40276113552	0.75	13	12	29	1.423629
        intron1	34	22	atattatcg	-2.57035278941	0.823529411765	6	12	29	-0.44829131
        intron2	20	47	gattgactg	1.83174485153	0.714285714286	14	10	21	0.65914217
        intron2	20	41	ctgtgactg	1.82301608911	0.75	8	10	21	1.047049
        intron2	20	37	gactgactg	3.16203878284	0.78125	4	10	21	1.8346258

##Usage: `SVM_bp.sh <filename <species (Hsap...)> <length>`


---

#For full documentation:

See [SVM_bpfinder's README](http://regulatorygenomics.upf.edu/Software/SVM_BP/README) for full instructions
