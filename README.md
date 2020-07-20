![Generate documentation](https://github.com/MaastrichtU-IDS/euraknos-ontology/workflows/Generate%20documentation/badge.svg) 

OWL Ontology, with its documentation website, for the EURAKNOS and [EUREKA](https://h2020eureka.eu/about) projects.

Access the Euraknos ontology documentation at [**https://maastrichtu-ids.github.io/euraknos-ontology 📖**](https://maastrichtu-ids.github.io/euraknos-ontology) 

The documentation website will be updated automatically when a change is made to the [euraknos-ontology.owl](https://github.com/MaastrichtU-IDS/euraknos-ontology/blob/master/euraknos-ontology.owl) file on the `master` branch 🔃

### Generate docs locally

Install Ontospy:

```bash
pip install ontospy[FULL]
```

> See [Ontospy official documentation](http://lambdamusic.github.io/Ontospy) for more details.

Clone the repository:

```bash
git clone https://github.com/MaastrichtU-IDS/euraknos-ontology.git
cd euraknos-ontology
```

We are generating 4 differents types of documentation/visualization in subfolders of the `docs/` folder. The folder where the documentation will be generated needs to exist:

```bash
mkdir -p docs/summary
ontospy gendocs -o docs/summary --type 1 --nobrowser euraknos-ontology.owl

mkdir -p docs/browse
ontospy gendocs -o docs/browse --type 2 --nobrowser euraknos-ontology.owl

mkdir -p docs/classtree
ontospy gendocs -o docs/classtree --type 4 --nobrowser euraknos-ontology.owl

mkdir -p docs/graph
ontospy gendocs -o docs/graph --type 10 --nobrowser euraknos-ontology.owl

# Try a new visualization
mkdir -p docs/new
ontospy gendocs -o docs/new --nobrowser euraknos-ontology.owl
```

> See the source code for [more details on parameters](https://github.com/lambdamusic/Ontospy/blob/master/ontospy/cli.py#L169).

The Graph visualisation can be improved at:
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/viz/viz_html_multi.py
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/media/templates/misc/sigmajs.html

### See also

[WebVOWL](http://www.visualdataweb.de/webvowl/), d3.js graph viewer: 

http://www.visualdataweb.de/webvowl/#iri=https://raw.githubusercontent.com/MaastrichtU-IDS/euraknos-ontology/master/euraknos-ontology.owl
