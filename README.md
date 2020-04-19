# Framester's FrameNet to BabelNet mappings

This repository contains the Framester's FrameNet 1.5 to BabelNet 3.7 mappings.
Starting from the [Framester's FrameNet to WordNet mappings](https://github.com/luigi-asprino/fn2wn), these mappings have been obtained by following the alignment between BabelNet and WordNet synsets.
As FrameNet-WordNet mappings, the BabelNet mappings are organised in three profiles, i.e.: Base (B), Direct (D) and Transitive (T).



### Mapping implementation

The mapping between FrameNet's frames and BabelNet's synsets is implemented by using ``skos:closeMatch`` property as follows:

```
<FRAME_URI> skos:closeMatch <SYNSET_URI>
```

### Statistics 

||Number of mappings|
|-|-|
|Base Profile|8367|

||Number of conservative mappings|Number of reckless mappings|
|-|-|-|
|Direct Profile|53518|64586|
|Transitive Profile|141243|207818|


## License

- This dataset is distributed under licence [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Authors

- [Aldo Gangemi](mailto:aldo.gangemi@cnr.it) (main contributor)
- [Luigi Asprino](mailto:luigi.asprino@istc.cnr.it) (maintainer)
