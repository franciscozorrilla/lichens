# Metabolic modeling of lichen metagenomes
Lichens are complex symbiotic assemblies of microorganisms. On the 28th of March 2022 we received [22 selected metagenome assembled genomes](https://github.com/franciscozorrilla/lichens/tree/main/data/MAGs) (MAGs) representing 2 metagenomic communities (VT1, X11). Along with @arianccbasile we reconstructed [genome scale metabolic models](https://github.com/franciscozorrilla/lichens/tree/main/data/GEMs) (GEMs) and carried out flux balance analysis (FBA) based simulations for the two lichen communities.

## 📑 Metadata

```
Genome	metagenome_ID	metagenomes_sample_name	depth_coverage	completeness	contamination	domain	phylum	order	family	genus	full_taxonomy_bacteria	gram_stain
private_T1888_metawrap_bin.19	VT1	Platismatia glauca	7.004340898	83.14	0.86	bacteria	Acidobacteriota	Acidobacteriales	Acidobacteriaceae	Tous-C9LFEB	d__Bacteria;p__Acidobacteriota;c__Acidobacteriae;o__Acidobacteriales;f__Acidobacteriaceae;g__Tous-C9LFEB;s__	neg
private_TS1974_metawrap_bin.12	VT1	Platismatia glauca	3.397432446	98.24	1.52	bacteria	Acidobacteriota	Acidobacteriales	Acidobacteriaceae	Granulicella_C	d__Bacteria;p__Acidobacteriota;c__Acidobacteriae;o__Acidobacteriales;f__Acidobacteriaceae;g__Granulicella_C;s__	neg
private_X3_concoct_bin.10	VT1	Platismatia glauca	86.77040165	99.62	0.75	eukaryotes	Fungi	NA	NA	NA	NA	NA
private_X11_metabat2_bin.10	X11	Ramalina menziesii	201.9128775	93.61	0.38	eukaryotes	Fungi	NA	NA	NA	NA	NA
public_SRR7232211_concoct_bin.8	VT1	Platismatia glauca	2.600714332	94.6	4	eukaryotes	Chlorophyta	NA	NA	NA	NA	NA
private_X15_metawrap_bin.2	VT1	Platismatia glauca	2.080059245	95.27	1.01	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	CAHJXG01	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__CAHJXG01;s__	neg
private_T1889_metawrap_bin.7	VT1	Platismatia glauca	3.022102585	69.19	1.1	bacteria	Proteobacteria	Rhizobiales	Beijerinckiaceae	Lichenihabitans	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Rhizobiales;f__Beijerinckiaceae;g__Lichenihabitans;s__	neg
private_T1889_metawrap_bin.7	X11	Ramalina menziesii	3.790149716	69.19	1.1	bacteria	Proteobacteria	Rhizobiales	Beijerinckiaceae	Lichenihabitans	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Rhizobiales;f__Beijerinckiaceae;g__Lichenihabitans;s__	neg
private_VT2_metawrap_bin.3	VT1	Platismatia glauca	7.725129698	88.46	0.85	bacteria	Acidobacteriota	Acidobacteriales	Acidobacteriaceae	CAHJWL01	d__Bacteria;p__Acidobacteriota;c__Acidobacteriae;o__Acidobacteriales;f__Acidobacteriaceae;g__CAHJWL01;s__	neg
private_VT1_metawrap_bin.3	VT1	Platismatia glauca	22.65182559	95.86	1.24	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	Acetobacteraceae gen. sp.	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__;s__	neg
private_VT1_metawrap_bin.2	VT1	Platismatia glauca	12.57524573	95.43	3.46	bacteria	Verrucomicrobiota	Chthoniobacterales	UBA10450	CAHJWO01	d__Bacteria;p__Verrucomicrobiota;c__Verrucomicrobiae;o__Chthoniobacterales;f__UBA10450;g__CAHJWO01;s__	neg
private_VT1_metawrap_bin.1	VT1	Platismatia glauca	46.82191387	96.35	0.75	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	LMUY01	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__LMUY01;s__	neg
private_T1904_concoct_bin.38	VT1	Platismatia glauca	2.711315944	95.2	3.6	eukaryotes	Chlorophyta	NA	NA	NA	NA	NA
private_X11_metawrap_bin.1	X11	Ramalina menziesii	50.6617192	91.36	1.72	bacteria	Acidobacteriota	Acidobacteriales	Acidobacteriaceae	Bryocella	d__Bacteria;p__Acidobacteriota;c__Acidobacteriae;o__Acidobacteriales;f__Acidobacteriaceae;g__Bryocella;s__	neg
private_X11_metawrap_bin.2	X11	Ramalina menziesii	23.80920946	94.66	2.03	bacteria	Proteobacteria	Caulobacterales	Caulobacteraceae	Caulobacteraceae gen. sp.	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Caulobacterales;f__Caulobacteraceae;g__;s__	neg
private_X11_metawrap_bin.3	X11	Ramalina menziesii	28.25045705	95.02	1.24	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	Acetobacteraceae gen. sp.	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__;s__	neg
private_X11_metawrap_bin.4	X11	Ramalina menziesii	6.32876225	81.14	1.66	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	CAIMSN01	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__CAIMSN01;s__	neg
public_ERR4179389_metawrap_bin.6	VT1	Platismatia glauca	2.113180873	54.8	0.85	bacteria	Acidobacteriota	Acidobacteriales	Acidobacteriaceae	Granulicella_C	d__Bacteria;p__Acidobacteriota;c__Acidobacteriae;o__Acidobacteriales;f__Acidobacteriaceae;g__Granulicella_C;s__	neg
public_SRR7232211_metawrap_bin.1	X11	Ramalina menziesii	1.387729411	97.22	0.75	bacteria	Proteobacteria	Acetobacterales	Acetobacteraceae	CAIMSN01	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Acetobacterales;f__Acetobacteraceae;g__CAIMSN01;s__	neg
private_T1916_metawrap_bin.4	X11	Ramalina menziesii	1.162669853	96.5	0.22	bacteria	Proteobacteria	Sphingomonadales	Sphingomonadaceae	Sphingomonas_N	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Sphingomonadales;f__Sphingomonadaceae;g__Sphingomonas_N;s__	neg
private_T1916_metawrap_bin.6	VT1	Platismatia glauca	1.701699443	95.99	1.3	bacteria	Proteobacteria	Rhizobiales	Beijerinckiaceae	Lichenihabitans	d__Bacteria;p__Proteobacteria;c__Alphaproteobacteria;o__Rhizobiales;f__Beijerinckiaceae;g__Lichenihabitans;s__	neg
private_X11_concoct_bin.15	X11	Ramalina menziesii	9.5366119	93	4.8	eukaryotes	Chlorophyta	NA	NA	NA	NA	NA
```

## 🧬 MAG taxonomies

Taxonomic breakdown of MAGs across communities based on metadata file provided by Gulnara.

1. Gram negative bacteria (x17)
2. Algae (x3)
3. Yeast (x2)

Bacterial species are only defined up to genus level of taxonomy, perhaps suggesting novelty in genomes. Eukaryotic species are only defined at the phylum level of taxonomy.

## ⛰️ Community composition

VT1 seems to be more diverse in terms of bacterial composition compared to X11. In particular, bin private_VT1_metawrap_bin.2 (belonging to genus CAHJWO01) is a member of the Verrucomicrobiota phylum and is found only in community VT1. Furthermore, VT1 contains an additional 3 acidobacteriota species compared to X11. VT1 also contains an additional Cholorphyta genome, while X11 contains an additional Proteobacteria species.

👉 [Taxonomy](https://github.com/franciscozorrilla/lichens/blob/main/figures/lichen_taxonomy.pdf)

## 📊 Completeness & depth of coverage

All MAGs meet the medium quality (MQ) threshold of completeness ≥ 50% & contamination ≤ 10%. All but 6 MAGs pass the high quality (HQ) threshold of completeness ≥ 90% & contamination ≤ 5%. 4 of these MQ MAGs are from community VT1 (3 Acidobacteriota, 1 Proteobacteria), while 2 MAGs are Proteobacteria from community X11.

X11 appears to be heavily dominated by the fungal species, which shows an ~2-fold increase in the depth of coverage compared to community VT1. Although X11 contains a single Acidobacteriota species, this community member has more than twice the depth of coverage of all Acideobacteriota species in community VT1.

👉 [Coverage](https://github.com/franciscozorrilla/lichens/blob/main/figures/lichen_metadata.pdf)

## 🐛 Bacterial metabolic models

### 1. Get ORF-annotated protein files

```bash
# get ORF fasta files
while read file;do 
	prodigal -i $file -a ../protein/${file%.*}.faa;
done < <(ls|grep fa)
```

### 2. Generate models without any media-based gapfilling, using the gram negative template

```bash
# get GEMs w/o gapfilling gramneg model
while read file;do 
	carve -v --fbc2 -u gramneg -o gramneg_nogf/$(basename ${file%.*}.xml) $file; 
done< <(ls protein/*.faa);
```

### 3. Organize models into sample specific folders

```bash
# move X11 species into folder
while read sample;do 
	mv ${sample}.xml X11/;
done< <(less ../lichen_metadata_metaGEM.txt|tail -n +2|cut -f1,2|grep X11|cut -f1)

# move VT1 species into folder, note that private_T1889_metawrap_bin.7 is present in both communities
while read sample;do 
	mv ${sample}.xml VT1/;
done< <(less ../lichen_metadata_metaGEM.txt|tail -n +2|cut -f1,2|grep VT1|cut -f1)
```

## 🍄 Eukaryotic models

TBC by @arianccbasile

### 4. Generate models

## 🥠 Simulation & visualization

### 5. VT1 models for SMETANA simulations

```bash
# put bacterial + eukaryotic models in foldr for VT1
while read model;do 
	mv ${model}.xml bacteria/;
done< <(less ../../lichen_metadata_metaGEM.txt |cut -f1,2,7|grep bacteria|grep VT1|cut -f1)

# SMETANA 
for i in {1..20}; do 
	echo "Running simulation $i out of 20 ... "; 
	smetana --flavor fbc2 -o sim_${i} -v -d --zeros --molweight *.xml;
done
```

### 5. X11 models for SMETANA simulations

```bash
# put bacterial models in foldr for X11
while read model;do 
	mv ${model}.xml bacteria/;
done< <(less ../../lichen_metadata_metaGEM.txt |cut -f1,2,7|grep bacteria|grep X11|cut -f1)

# SMETANA 
for i in {1..20}; do 
	echo "Running simulation $i out of 20 ... "; 
	smetana --flavor fbc2 -o sim_${i} -v -d --zeros --molweight *.xml;
done
```

### 6. Summarize SMETANA simulations

```bash
cd lichen/gramneg_nogf/VT1/bacteria # summarize VT1 simulations
while read sim;do 
	var=$(echo $sim|sed 's/_detailed.tsv//g');
	paste $sim|sed "s/^all/$var/g"|grep -v community;
done< <(ls|grep _detailed.tsv)|sed 's/minimal/VT1/g' >> ../detailed_summary.tsv

cd lichen/gramneg_nogf/X11/bacteria # summarize X11 simulations
while read sim;do 
	var=$(echo $sim|sed 's/_detailed.tsv//g');
	paste $sim|sed "s/^all/$var/g"|grep -v community;
done< <(ls|grep _detailed.tsv)|sed 's/minimal/X11/g' >> ../detailed_summary.tsv

cd lichen/gramneg_nogf/ # combine into gramneg_detailed.tsv file
while read file;do 
	paste $file;
done< <(find . -name "detailed_summary.tsv") >> smetana_detailed.tsv
```

### 7. Manipulate data and plot in R: visualize interactions with average SMETANA score ≥ 0.75 across simulations

```r
# load libraries
library(tidyverse)
library(ggalluvial)

# load data
lichen_smetana = read.delim("smetana_detailed.tsv")
lichen_meta = read.delim("metadata.tsv") %>% mutate(receiver_taxonomy=genus,receiver=Genome,donor_taxonomy=genus,donor=Genome)
bigg_mets = read.delim("bigg_classes.tsv")

# manipulate data to summarize across simulations by calculating mean, sd, and median
lichen_smetana %>% 
  group_by(medium,receiver,donor,compound) %>% 
  summarize(smet_ave=mean(smetana),smet_sd=sd(smetana),smet_med=median(smetana)) -> lichen_df

ggplot(lichen_df %>% 
         mutate(compound = gsub("M_","",compound),compound = gsub("_e","",compound)) %>%
         left_join(.,lichen_meta%>%select(receiver,receiver_taxonomy)) %>% 
         left_join(.,lichen_meta%>%select(donor,donor_taxonomy)) %>%  
         left_join(.,bigg_mets) %>%
         filter(smet_ave>= 0.75) %>%
         mutate(category=ifelse(smet_ave>=0.7,"high",
                                ifelse(smet_ave<0.7&smet_ave>0.4,"medium","low"))),
       aes(axis1 = donor_taxonomy, axis2 = name, axis3 = receiver_taxonomy,
           y = smet_ave)) +
    scale_x_discrete(limits = c("Donor", "Metabolite", "Reciever")) +
    xlab("Interaction") +
    geom_alluvium(aes(fill = name)) +
    geom_stratum(width=0.3) +
    theme_minimal() + geom_text(stat = "stratum", aes(label = after_stat(stratum)),min.y=0.2)+theme_bw() + 
    theme(panel.border = element_blank(), panel.grid.major = element_blank(),panel.grid.minor = element_blank(), axis.line = element_line(colour = "black"),axis.line.y = element_blank(),axis.ticks.y = element_blank(),axis.text.y = element_blank(),axis.title.y = element_blank(),axis.line.x = element_blank(),axis.ticks.x = element_blank(),legend.position = "none") + facet_wrap(~medium)

ggsave("lichen_v3_smetana.pdf",height = 10,width = 18)
```

👉 [Predicted interactions](https://github.com/franciscozorrilla/lichens/blob/main/figures/lichen_v3_smetana.pdf)
