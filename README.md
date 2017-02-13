# ilivalidator-demo-2017-02-14

## INTERLIS 1

### Ohne Fehler

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --modeldir data/ data/254900.itf `

### Mit Fehler

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --modeldir data/ data/254900_err.itf `

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --log data/2549.log --xtflog data/2549_log.xtf --modeldir data/ data/254900_err.itf`

(Bug: XTF-Logfile >= 0.9.0 ohne Errors).

`java -jar apps/ili2gpkg-3.6.1/ili2gpkg.jar --dbfile data/2549.gpkg --modeldir data/ data/2549_log.xtf`


## INTERLIS 2

### Ohne Fehler

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --modeldir "http://models.geo.admin.ch;." data/gewaesserschutz.xtf`

### Mit Fehler

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --modeldir "http://models.geo.admin.ch;." data/gewaesserschutz_mit_fehler.xtf`

### Tolerierte Fehler

`java -jar apps/ilivalidator-0.9.0/ilivalidator.jar --config data/gewaesserschutz.toml --modeldir "http://models.geo.admin.ch;." data/gewaesserschutz_mit_fehler.xtf`


### Eigene Tests

`java -cp 'apps/ilivalidator-0.10.0/ilivalidator.jar:apps/ilivalidator-0.10.0/libs/*' org.interlis2.validator.Main --modeldir "http://models.geo.admin.ch;data/." control_points.xtf`





