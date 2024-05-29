## Licences of source data


## Documentation
- see [this README](./doc/README.md) for more information about the original article and the meaning of FHR and TOCO data.

## Data
- situées dans le répertoire `data` folder.
- 300 sujets, 
    - numérotés de 1 a 300. 
    - pour 300 sujets, 100 issus de trois hopitaux europeens (FR, UK, CZ)

- CTG_Challenge_files_GroundTruth 
    - qui contient la verite
    - 0 :  pH > 7.05 Healthy
    - 1 : pH <=7.05 Non Healthy (suspicion dacidose)

- ctg_data 
    -  qui contient le trace de quelques exemples choisis parce qu’evidents ou au contraire ambigus (TP: true positive, etc)

- CTG_workshop_database 
    - qui contient les données en .mat numerotes de 1 a 300.

- Dans chaque `.mat`, il y a 3 structures :  
    | Name | Size | Bytes Class | Attributes |
    |------|------|-------------|------------|
    |fhr | 45262x1 | 362096 |double             
    |info | 1x1 |  526 | struct |            
    |toco |      45262x1 | 362096 | double             

- info=struct with fields:  
    - fs: 4
    - ind_stageII: 44062
    - id: ‘004'

- frequence d’échantillonnage:
    - 4hZ dans tous les cas.
- L’echantillon auquel demarre le « stage II » - phase d’expulsion en general le statut (Ph >< 7.05) n’est à associer qu’au 20-30 dernieres minutes du signal
- Toco est sans interet ici.

