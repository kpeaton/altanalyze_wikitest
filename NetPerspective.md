## NetPerspective: AltAnalyze Biological Network Analysis Tool ##

NetPerspective is a new tool in AltAnalyze designed to visualize biological interactions between gene, proteins, RNAs, metabolites and drugs in a coherent and easy way.

![http://altanalyze.org/image/NetPerspective.jpg](http://altanalyze.org/image/NetPerspective.jpg)

Interactions can be based on:
  1. Highly validated protein and metabolite interactions from annotated pathways (WikiPathways, KEGG, HMDB).
  1. Experimentally derived protein-protein or protein-DNA interactions (BioGRID, Amadeus, Pazar).
  1. Drug interactions (DrugBank).
  1. Sequence predicted miRNA interactions.

Networks can be built from various sources including:
  1. User supplied gene/metabolite ID files (e.g., AltAnalyze/[GO-Elite](GOElite.md) produced).
  1. Selected pathways/ontologies/gene-sets.
  1. Existing interaction tables (e.g., SIF format).

Multiple interaction algorithms can be used to identify:
  1. Direct interacting nodes.
  1. Nodes indirectly connecting through other genes/metabolites.
  1. The shortest possible path between two or more genes/metabolites.
  1. All available interactions.

When loaded with a differential expression file in the AltAnalyze produced [GO-Elite](GOElite.md) input file format, nodes will be colored as red or blue, depending on their assigned numerical value (positive or negative column #3). Additionally, IDs specifically in the input file can be used to augment a network (e.g., regulated protein expression in a metabolite network).

### Using NetPerspective ###

NetPerspective can be run independent of the standard AltAnalyze workflows. To run, simply start AltAnalyze, select the appropriate species and ANY platform/vendor type (ignored for NetPerspective) and continue to the main analysis window. When presented, selected "Additional Analyses" then "Network Analysis". The above interface will be presented. Here you can select various options as outlined in the previous section. When providing a list of IDs, versus existing interactions, the input file type will need to be specified (option 2).