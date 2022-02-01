# github-pages

## To run in docker locally:
```bash
$ docker build -t github-pages .
$ docker run -it -p 1313:1313 -v $(pwd):/website github-pages /bin/bash -x run.sh
```

### Funding acknowledment

<img alt="European Flag" src="https://erigrid2.eu/wp-content/uploads/2020/03/europa_flag_low.jpg" align="left" style="margin-right: 10px"/> The development of test-case-descriptions has been supported by the [ERIGrid 2.0](https://erigrid2.eu) project of the H2020 Programme under [Grant Agreement No. 870620](https://cordis.europa.eu/project/id/870620)
