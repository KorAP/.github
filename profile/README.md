**KorAP** is a corpus analysis platform that is suitable for very large, multiply annotated corpora and complex search queries, independent of specific research questions.

The [main instance of KorAP](https://korap.ids-mannheim.de/) serves the [German Reference Corpus DeReKo](https://www.ids-mannheim.de/digspra/kl/projekte/korpora/).

The platform consists of several components, which are published as separate repositories.
It is mainly developed at the [Leibniz Institute for German Language](https://www.ids-mannheim.de).

## Run and test KorAP locally

Prerequisite: [docker](https://www.docker.com/) (including the docker-compose-v2-plugin)

To run KorAP with an example corpus, use the following command:

```bash
curl https://raw.githubusercontent.com/KorAP/KorAP-Docker/master/compose.yaml | INDEX='example-index' docker compose -p korap -f - --profile=lite --profile=example up
```

This will download the necessary images, start KorAP, and make the web UI available at [http://localhost:64543/](http://localhost:64543/).
