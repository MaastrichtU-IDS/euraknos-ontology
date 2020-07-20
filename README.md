![Generate documentation](https://github.com/MaastrichtU-IDS/euraknos-ontology/workflows/Generate%20documentation/badge.svg) 

OWL Ontology for the EURAKNOS project, and documentation website

### Generate docs

See Ontospy documentation: http://lambdamusic.github.io/Ontospy

Install Ontospy:

```bash
pip install ontospy[FULL]
```

Using Ontospy, from the commandline

> Choose the visualization type

We are generating 4 differents pages in subfolder of the `docs/` folder. The folder where the documentation will be generated needs to exist:

```bash
mkdir -p docs/summary
ontospy gendocs -o docs/summary --type 1 --nobrowser euraknos-ontology.owl
# >1

mkdir -p docs/browse
ontospy gendocs -o docs/browse --type 2 --nobrowser euraknos-ontology.owl
# >2

mkdir -p docs/classtree
ontospy gendocs -o docs/classtree --type 4 --nobrowser euraknos-ontology.owl
# >4

mkdir -p docs/graph
ontospy gendocs -o docs/graph --type 10 --nobrowser euraknos-ontology.owl
# >10
```

> See the source code for [more details on parameters](https://github.com/lambdamusic/Ontospy/blob/master/ontospy/cli.py#L169).

The Graph visualisation can be improved at:
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/viz/viz_html_multi.py
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/media/templates/misc/sigmajs.html

### See also

[WebVOWL](http://www.visualdataweb.de/webvowl/), d3.js graph viewer: 

http://www.visualdataweb.de/webvowl/#iri=https://raw.githubusercontent.com/MaastrichtU-IDS/euraknos-ontology/master/euraknos-ontology.owl
