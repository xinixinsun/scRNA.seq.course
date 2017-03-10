---
# knit: bookdown::preview_chapter
output: html_document
---



# Overview of experimental methods for generating scRNA-seq data

Development of new methods and protocols for scRNA-seq is currently a very active area of research, and several protocols have been published over the last few years. The methods can be categorized in different ways, but the two most important aspects are __quantification__ and __capture__. 

For quantification, there are two types, __full-length__ and __tag-based__. The former tries to achieve a uniform read coverage of each transcript. By contrast, tag-based protocols only capture either the 5'- or 3'-end of each RNA. The choice of quantification method has important implications for what types of analyses the data can be used for. In theory, full-length protocols should provide an even coverage of transcripts, but as we shall see, there are often biases in the coverage. The main advantage of tag-based protocol is that they can be combined with unique molecular identifiers (UMIs) which can help improve the quantification (see chapter 6). On the other hand, being restricted to one end of the transcript may reduce the mappability and it also makes it harder to distinguish different isoforms[@Archer2016-zq].

The strategy used for capture determines how the cells can be selected as well as what kind of additional information besides the sequencing that can be obtained. The three most widely used options are __microwell-__, __microfluidic-__ and __droplet-__based.

For well-based platforms, cells are isolated using for example pipette or laser capture and placed in microfluidic wells. One advantage of well-based methods can be combined with fluorescent activated cell sorting (FACS), making it possible to select cells based on surface markers. This strategy is thus very useful for situations when one wants to isolate a specific subset of cells for sequencing. Another advantage is that one can take pictures of the cells. The image provides an additional modality and a particularly useful application is to identify wells containg damaged cells or doublets. The main drawback of these methods is that they are low-throughput and the amount of work required per cell may be considerable.

Microfluidic platforms, such as Fluidigm's C1, provide a more integrated system for capturing cells and for carrying out the reactions necessary for the library preparations. Thus, they provide a higher throughput than microwell based platforms. Typically, only around 10% of cells are captured in a microfluidic platform and thus they are not appropriate if one is dealing with rare cell-types or very small amounts of input. Moreover, the chip is relatively expensive, but since reactions can be carried out in a smaller volume money can be saved on reagents.

The idea behind droplet based methods is to encapsulate each individual cell inside a nanoliter droplet together with a bead. The bead is loaded with the enzymes required to construct the library. In particular, each bead contains a unique barcode which is attached to all of the reads originating from that cell. Thus, all of the droplets can be pooled, sequenced together and the reads can subsequently be assigned to the cell of origin based on the barcodes. Droplet platforms typically have the highest throughput since the library preparation costs are on the order of .05 USD/cell. Instead, sequencing costs often become the limiting factor and a typical experiment the coverage is low with only a few thousand different transcripts detected[@Ziegenhain2017-cu].