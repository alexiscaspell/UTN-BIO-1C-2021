nucleotids_file := "CYP1B1.gb"
aminoacids_file := "MYOC.fasta"

.SILENT:
install: 
	sudo apt-get install emboss

.SILENT:
getorf orfrun: 
	getorf in/${nucleotids_file} out/orf.fasta

.SILENT:
getmotifs motifsrun:
	sudo prosextract -prositedir prosite && patmatmotifs in/${aminoacids_file} out/motifs.patmatmotifs

.SILENT:
clean:
	rm -rf out/*
	
.SILENT:
run: clean orfrun motifsrun 
	echo 'PROCESAMIENTO FINALIZADO'