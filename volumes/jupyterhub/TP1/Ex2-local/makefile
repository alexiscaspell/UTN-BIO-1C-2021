# ---------------------------------------
# VAR
# ---------------------------------------

BIN_PATH=./bin
DB_PATH=./db

SWISSPROT_PATH=$(DB_PATH)/swissprot

MAKEBLASTDB=$(BIN_PATH)/makeblastdb
BLASTP=$(BIN_PATH)/blastp



# ---------------------------------------
# SRC
# ---------------------------------------

.SILENT:
rm-db:
	rm -fr $(DB_PATH)


.SILENT:
install-db:
	wget http://ftp.ncbi.nlm.nih.gov/blast/db/FASTA/swissprot.gz -P $(DB_PATH)
	gzip -d $(DB_PATH)/swissprot.gz
	rm -f $(DB_PATH)/swissprot.gz
	$(MAKEBLASTDB) -dbtype prot -in $(SWISSPROT_PATH)


# ejemplo de uso: make run-blast IN=Ex1_output.fasta OUT=result.txt
.SILENT:
run-blast:
	$(BLASTP) -db $(SWISSPROT_PATH) -query ${IN} -out ${OUT}
