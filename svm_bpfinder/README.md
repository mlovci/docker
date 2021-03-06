#SVM_bpfinder


A simple docker  wrapper for [`SVM_bpfinder`](http://regulatorygenomics.upf.edu/Software/SVM_BP/). `SVM_bpfinder` uses binaries from [`SVM_light`](http://svmlight.joachims.org/) to predict the location and quality of branch-point signals.


---

This repository repackages work from these wonderful people:

  - A. Corvelo, M. Hallegger, C.W.J. Smith, E. Eyras. Genome-wide Association between Branch Point Properties and Alternative Splicing. ... (2010) 
  - T. Joachims, Making large-Scale SVM Learning Practical. Advances in Kernel Methods - Support Vector Learning, B. Schölkopf and C. Burges and A. Smola (ed.), MIT-Press, 1999.

##Requirements:

  - `SVM_bp.sh` from this repo
  - [`docker`](http://docker.io/)
  - UNIX-like system, or else you need to replicate the contents of `SVM_bp.sh` for your architecture.

##Installation:

  1. Add [`SVM_bp.sh`](https://raw.githubusercontent.com/mlovci/docker/master/svm_bpfinder/SVM_bp.sh) to a place in $PATH
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

##Usage: 

`SVM_bp.sh <filename> <species (i.e. Hsap)> <length>`


---

#For full documentation:

See [SVM_bpfinder's README](http://regulatorygenomics.upf.edu/Software/SVM_BP/README) for full instructions

#License

Permission is granted for unrestricted academic use. Limitations are placed on the use of this container only where prohibited by the constituent packages. Contact the authors to obtain permission for non-academic uses: [`SVM_bpfinder`](http://regulatorygenomics.upf.edu/Software/SVM_BP/README) and [`SVM_light`](http://svmlight.joachims.org/)
