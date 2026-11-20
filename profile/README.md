**KorAP** is a corpus analysis platform for very large, multiply annotated corpora and complex search queries.
It is developed at the [Leibniz Institute for the German Language (IDS)](https://www.ids-mannheim.de) and serves the
[German Reference Corpus DeReKo](https://www.ids-mannheim.de/digspra/kl/projekte/korpora/) at
**[korap.ids-mannheim.de](https://korap.ids-mannheim.de/)**.

## Try it locally

With [Docker](https://www.docker.com/) (or rootless [Podman](https://podman.io/)) installed, this command starts KorAP with an example corpus:

```bash
curl -s https://raw.githubusercontent.com/KorAP/KorAP-Docker/master/compose.yaml | \
  COMPOSE_PROFILES=open,example INDEX=example-index docker compose -p korap -f - up
```

Then open [http://localhost:64543](http://localhost:64543) and search for `geht`.

## Use your own corpus

[KorAP-Ingestion](https://github.com/KorAP/KorAP-Ingestion) takes your TEI XML files, annotates and indexes them,
and starts a KorAP instance on the result – by just typing `make`.
To run KorAP on an existing index or with login, see [KorAP-Docker](https://github.com/KorAP/KorAP-Docker).

## Access KorAP from your code

- [RKorAPClient](https://github.com/KorAP/RKorAPClient) – R package for queries, frequencies and collocations
- [PythonKorAPClient](https://github.com/KorAP/PythonKorAPClient) – the same for Python
- [KorapSRU](https://github.com/KorAP/KorapSRU) – CLARIN Federated Content Search endpoint

## Components

| | Repository | Purpose |
|---|---|---|
| 🐙 | [Kalamar](https://github.com/KorAP/Kalamar) | Web user interface |
| 🚤 | [Kustvakt](https://github.com/KorAP/Kustvakt) | API, user and access management |
| 🔍 | [Krill](https://github.com/KorAP/Krill) | Lucene-based search index |
| 📝 | [Koral](https://github.com/KorAP/Koral) | Query language translation to KoralQuery |
| 🐳 | [KorAP-Docker](https://github.com/KorAP/KorAP-Docker) | Run all components with one command |

Conversion and annotation tools: [KorAP-XML-TEI](https://github.com/KorAP/KorAP-XML-TEI) ·
[korapxmltool](https://github.com/KorAP/korapxmltool) ·
[KorAP-Tokenizer](https://github.com/KorAP/KorAP-Tokenizer) ·
[Datok](https://github.com/KorAP/Datok)

## Feedback

Software bugs: open an issue in the component's repository, e.g. [Kalamar](https://github.com/KorAP/Kalamar/issues).
Problems with corpus content (texts, metadata, annotations): [DeReKo-Issues](https://github.com/KorAP/DeReKo-Issues).
