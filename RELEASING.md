# Releasing the dataset

## Recreate the raw data from glottography-data

In case of upstream changes in glottography-data:
```shell
cldfbench download cldfbench_zucchi2017arqueologia.py
```

## Recreate the CLDF data

```shell
cldfbench makecldf cldfbench_zucchi2017arqueologia.py --glottolog-version v5.2
cldfbench cldfreadme cldfbench_zucchi2017arqueologia.py
cldfbench zenodo --communities glottography cldfbench_zucchi2017arqueologia.py
cldfbench readme cldfbench_zucchi2017arqueologia.py
```

## Validation

```shell
cldf validate cldf
```

```shell
cldfbench geojson.validate cldf
```

```shell
cldfbench geojson.glottolog_distance cldf --format pipe
```

| ID | Distance | Contained | NPolys |
|:---------|-----------:|:------------|---------:|
| bare1276 | 1.56 | False | 1 |
| curr1243 | 0.00 | True | 1 |
| guar1293 | 0.19 | False | 1 |
| guin1258 | 0.00 | True | 1 |
| maip1247 | 0.00 | True | 1 |
| mand1448 | 0.00 | True | 1 |
| mawa1268 | 1.08 | False | 1 |
| piap1246 | 0.00 | True | 1 |
| puin1248 | 0.00 | True | 1 |
| yavi1244 | 0.00 | True | 1 |
