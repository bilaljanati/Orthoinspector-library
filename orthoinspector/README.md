Interacting with the Orthoinspector database through the Orthoinspector python package

Functions:
	orthoDB(): returns a list of available databases with their name and 
release dates

	Database(name, release): creates a Database objects which stores the
the informations required for all the interactions

Objects and their methods:
Database:
	.get_species_list(): returns a list of species and their identifiers
	.get_species(taxid): returns the species object storing the
informations on this species
	.get_tree_newick(): returns the phylogeny tree of the clades and
species contained in the database, in the newick format
	.get_all_clades(): returns the clades contained in the database
	.get_clade_species(clade): returns the species contained in a given
clade

Species:
	.get_all_proteins(): returns a list containing Protein objects for all
the proteins in the species
	.get_proteins_profiles(): returns the phylogenetic profiles of all
the proteins in the species
	.orthologs_with(): returns all the orthology relationship involving
proteins from the species and proteins from a specified species
	.get_protein(access): returns a Protein object describing the
specified protein

Protein:
	.desc(): returns a short description with, for example, the sequence,
the phylogenetic profile...
	.get_orthologs(taxid2=None): returns the list of all the orthologous 
proteins, with the possibility to specify a species in which to search
exclusively in
	.profile(): returns the phylogenetic profile of the protein

Ortholog:

