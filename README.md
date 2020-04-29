# Framester's FrameNet to BabelNet mappings

This repository contains the Framester's FrameNet 1.5 to BabelNet 3.7 mappings.
Starting from the [Framester's FrameNet to WordNet mappings](https://github.com/luigi-asprino/fn2wn), these mappings have been obtained by following the alignment between BabelNet and WordNet synsets.
As FrameNet-WordNet mappings, the BabelNet mappings are organised in three profiles (i.e. Base (B), Direct (D) and Transitive (T)) and two flavors (Reckless (R) and Specific (S)).



### Mapping implementation

The mapping between FrameNet's frames and BabelNet's synsets is implemented by using ``skos:closeMatch`` property as follows:

```
<FRAME_URI> skos:closeMatch <SYNSET_URI>
```

### Statistics 

In this section we provide the statistics among the mapped synsets (i.e. here we do not consider the unmapped synsets).

|Profile|Flavor|Number of Mappings|Max mappings per synset|Avg. of mappings per synset|
|-|-|-|-|-|
|Base||8362|6|1.16|
|Base|S|8243|5|1.14|
|Direct||53498|11|1.29|
|Direct|S|50945|11|1.23|
|Direct|R|64555|11|1.56|
|Direct|RS|60434|11|1.46|
|Transitive||141207|17|1.53|
|Transitive|S|130681|12|1.42|
|Transitive|R|207741|21|2.25|
|Transitive|RS|184260|18|2.00|

To compute the average we used the following query

```[sparql]
SELECT (SUM(?c) AS ?sum)  (MAX(?c) AS ?max) (AVG(?c) AS ?avg){
	SELECT (COUNT(?fn) AS ?c) {
		?fn  skos:closeMatch ?bn
	} GROUP BY ?bn
}
```

## License

- This dataset is distributed under licence [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Authors

- [Aldo Gangemi](mailto:aldo.gangemi@cnr.it) (main contributor)
- [Luigi Asprino](mailto:luigi.asprino@istc.cnr.it) (maintainer)
