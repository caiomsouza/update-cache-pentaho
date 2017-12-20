# update-cache-pentaho
ETL using PDI to update Mondrian Cache for Pentaho 7


# known issues
French Special Characters in the password like <b>é</b>

# Error log:
```
2017/12/20 11:15:37 - Clear_Mondrian_Schema_Cache - Distribution démarrée pour la tranformation [Clear_Mondrian_Schema_Cache]
2017/12/20 11:15:37 - Generate Rows.0 - Fin exécution étape (Entrées=0, Sorties=0, Lues=0, Ecrites=1, Maj=0, Erreurs=0)
2017/12/20 11:15:37 - HTTP Client.0 - ERROR (version 6.1.0.1-196, build 1 from 2016-04-07 12.08.49 by buildguy) : Un erreur interdit l'exécution de cette étape: 
2017/12/20 11:15:37 - HTTP Client.0 - Impossible d'obtenir un retour depuis l'URL spécifiée: http://10.201.5.46:8080/pentaho/api/repos/xanalyzer/service/ajax/clearCache?catalog=SFR_SAV_Callback
2017/12/20 11:15:37 - HTTP Client.0 - 
2017/12/20 11:15:37 - HTTP Client.0 - Vous devez être authentifié pour accéder à cette ressource http://10.201.5.46:8080/pentaho/api/repos/xanalyzer/service/ajax/clearCache?catalog=SFR_SAV_Callback.
2017/12/20 11:15:37 - HTTP Client.0 - Fin exécution étape (Entrées=0, Sorties=0, Lues=1, Ecrites=0, Maj=0, Erreurs=1)
2017/12/20 11:15:37 - Clear_Mondrian_Schema_Cache - Transformation détectée 
2017/12/20 11:15:37 - Clear_Mondrian_Schema_Cache - La transformation est en train d'arrêter l'exécution des autres étapes!
2017/12/20 11:15:37 - Clear_Mondrian_Schema_Cache - ERROR (version 6.1.0.1-196, build 1 from 2016-04-07 12.08.49 by buildguy) : Erreurs détectées!
2017/12/20 11:15:37 - Clear_Mondrian_Schema_Cache - ERROR (version 6.1.0.1-196, build 1 from 2016-04-07 12.08.49 by buildguy) : Erreurs détectées!
```

# Solution 
Create a user called mondrian, make this user an administrator of Pentaho BA Server and create a password without Special Characters.

