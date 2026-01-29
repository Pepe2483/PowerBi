
# Inseminaciones

{
  "InstanceID": "ee7319f0-3c31-4d34-b236-5054a6913521",
  "measures": [
    {
  "name": "VACA N",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "41be4410-a148-4e2c-b25c-8d0b68101b6d",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.8",
  "structureModifiedTime": "2023-08-08T16:33:05.93"
},
    {
  "name": "VACA S",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "9a5d0935-c792-464f-98e4-8ca6778bf78d",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.8",
  "structureModifiedTime": "2023-08-08T16:28:22.546667"
},
    {
  "name": "TS VACAS",
  "expression": "[VACA S]+[VACA N]",
  "formatString": "0",
  "lineageTag": "389ece24-748a-4cbb-bf91-f448d128f11c",
  "dataType": "int64",
  "modifiedTime": "2023-08-09T04:08:04.763333",
  "structureModifiedTime": "2023-08-08T17:31:57.96"
},
    {
  "name": "%TC VACAS",
  "expression": "[VACA S]/[TS VACAS]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "e250311f-8586-4aa7-9a9d-4d7e0e18d25d",
  "dataType": "double",
  "modifiedTime": "2023-08-14T16:11:15.623333",
  "structureModifiedTime": "2023-08-08T17:32:39.22"
},
    {
  "name": "VAQUILLA N",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=0,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "586a6949-8d4e-438c-ae47-911d8553167e",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-08T17:37:38.933333"
},
    {
  "name": "TS VAQUILLA",
  "expression": "[VAQUILLA S]+[VAQUILLA N]",
  "formatString": "0",
  "lineageTag": "ecbe80ac-0fdb-48e5-bb4c-70e92cda2add",
  "dataType": "int64",
  "modifiedTime": "2023-08-08T17:40:18.68",
  "structureModifiedTime": "2023-08-08T17:39:42.21"
},
    {
  "name": "%TCVAQUILLA",
  "expression": "[VAQUILLA S]/[TS VAQUILLA]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "3f581f93-4d03-4019-a198-e95dae738f83",
  "dataType": "double",
  "modifiedTime": "2023-08-08T17:42:04.53",
  "structureModifiedTime": "2023-08-08T17:41:34.086667"
},
    {
  "name": "VAQUILLA S",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=0,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "f99e9c0f-ffc3-4667-ba4e-c9d559c839aa",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-09T00:44:38.356667"
},
    {
  "name": "CALCULO DE MEDIAS",
  "expression": "if(HASONEVALUE(ITEMS[ITEM]),SWITCH(VALUES(ITEMS[ITEM]),\"TASA DE CONCEPCIÓN--------------  >30%\",FORMAT([%TC VACAS],\"percent\"),\"TASA DE CONCEPCIÓN-1 LC---------  >35%\",format([%TC VACAS 1LC],\"percent\"),\"TASA DE CONCEPCIÓN- >1 LC-------  >28%\",format([%TC VACAS >1LC],\"percent\"),\"TASA DETECCION DE CELOS---------  >60%\",format([TASA CELO],\"percent\"),\"% DE PREÑEZ ------------------------  >21%\",format([TASA PREÑEZ],\"percent\"),\"% DEL HATO PREÑADO-------------   >50%\",format([%HATOPREÑADO],\"percent\"),\"%PREÑADO HASTA 150 DIM----------  >40%\",format([%PREÑEZ 150DEL],\"percent\"),\"TASA DE ABORTOS VACAS--------------  <10%\",format([%ABORTO VACAS],\"percent\"),\"PERIÓDO VOL. ESPERA (PVE)  ---- 50-70 D\",60,\"DIM AL 1ST AI-----------------    PVE\",[PROM DEL 1ERSERV],\"DÍAS ABIERTOS--------------- <120DÍAS\",[DIAS ABIERTOS],\"PROM. EDAD AL 1 ER PARTO- 23-24 MESES\",[EDADPP],\" %VACAS QUE NO SE SIRVIERON ------<5%\",\"\",\"%METRITIS\",format([%METRITISG],\"percent\"),\"%MASTITIS\",format([%MASTITISG],\"percent\"),\"%ABORTOS VAQUILLAS\",format([%ABORTO VAQUILLA],\"percent\")))",
  "lineageTag": "8d6ed40f-3aa3-4040-b443-33ee8e9663e3",
  "dataType": "variant",
  "modifiedTime": "2025-02-24T03:29:33.733333",
  "structureModifiedTime": "2023-08-14T03:50:36.56",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2023-08-19T00:55:25.166667"
    }
  ]
},
    {
  "name": "%TC VACAS 1LC",
  "expression": "[VACA S 1LC]/[TS 1LC]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "f2e5c297-c6ef-4da2-bf3a-19a4400dcf62",
  "dataType": "double",
  "modifiedTime": "2023-08-14T16:00:51.96",
  "structureModifiedTime": "2023-08-14T15:40:56.803333"
},
    {
  "name": "VACA S 1LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "ebee8f4e-9d87-4fcf-b075-6d71b626dacb",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T15:47:16.1"
},
    {
  "name": "VACA N 1LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "d1e461f6-11d1-417b-938e-ebe469c65860",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T15:47:59.496667"
},
    {
  "name": "TS 1LC",
  "expression": "[VACA S 1LC]+[VACA N 1LC]",
  "formatString": "0",
  "lineageTag": "fbada985-0409-4736-89f9-db81d45f12ce",
  "dataType": "int64",
  "modifiedTime": "2023-08-14T15:49:18.333333",
  "structureModifiedTime": "2023-08-14T15:48:42.76"
},
    {
  "name": "VACA S >1LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>1,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "67206923-df97-4c7e-8700-63dcbe0b424b",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T16:01:21.346667"
},
    {
  "name": "VACA N >1LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>1,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "832a3668-9ceb-4939-82ff-6ce15b1fc4ea",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T16:02:11.5"
},
    {
  "name": "TS >1LC",
  "expression": "[VACA S >1LC]+[VACA N >1LC]",
  "formatString": "0",
  "lineageTag": "38a8d533-737f-4ceb-a5c4-ca3912390fea",
  "dataType": "int64",
  "modifiedTime": "2023-08-14T16:03:13.463333",
  "structureModifiedTime": "2023-08-14T16:02:47.083333"
},
    {
  "name": "%TC VACAS >1LC",
  "expression": "[VACA S >1LC]/[TS >1LC]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "a61e67e9-e5da-4b97-92a6-080411c0d12d",
  "dataType": "double",
  "modifiedTime": "2023-08-14T16:04:02.503333",
  "structureModifiedTime": "2023-08-14T16:03:20.153333"
},
    {
  "name": "PREÑADA HASTA 150DEL",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"S\",'INSEMINACIONES'[SrvDim]<=150)",
  "formatString": "0",
  "lineageTag": "54c0d785-36ac-47a6-91b9-7eab4b408fdc",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T17:25:02.616667"
},
    {
  "name": "PROM DEL 1ERSERV",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[SrvNumLact]=1)",
  "formatString": "0.00",
  "lineageTag": "81ea7df8-b71b-490e-88a6-612e2c202b93",
  "dataType": "double",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T17:32:50.22"
},
    {
  "name": "DIAS ABIERTOS",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"S\")",
  "lineageTag": "f0189dfc-aec8-4a71-8eef-b70b5a8dda53",
  "dataType": "double",
  "modifiedTime": "2023-08-18T23:41:57.803333",
  "structureModifiedTime": "2023-08-14T18:28:12.616667",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2023-08-14T18:30:23.106667"
    }
  ]
},
    {
  "name": "ELEGIBLES",
  "expression": "SUM('GENERALES VACAS'[HSCountAnimElig.0])",
  "lineageTag": "c6ab22dc-af22-4782-90ef-07adf82f54a3",
  "dataType": "double",
  "modifiedTime": "2023-09-04T15:54:12.553333",
  "structureModifiedTime": "2023-08-20T19:35:03.053333",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2023-08-20T19:44:11.883333"
    }
  ]
},
    {
  "name": "TASA PREÑEZ",
  "expression": "DIVIDE('AAMEDIDAS INSEMINACIONES (2)'[VACA S],'AAMEDIDAS INSEMINACIONES (2)'[ELEGIBLES],\"ERROR\")",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "dfe206a5-5cf7-4ab4-9000-e21942c55f61",
  "dataType": "variant",
  "modifiedTime": "2023-09-04T18:41:17.146667",
  "structureModifiedTime": "2023-08-20T19:47:10.64"
},
    {
  "name": "TASA CELO",
  "expression": "DIVIDE('AAMEDIDAS INSEMINACIONES (2)'[TS VACAS],'AAMEDIDAS INSEMINACIONES (2)'[ELEGIBLES],\"ERROR\")",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "98099637-907e-435b-8b68-cb7fca8ffbd7",
  "dataType": "variant",
  "modifiedTime": "2023-09-29T14:46:56.88",
  "structureModifiedTime": "2023-08-20T19:56:41.106667"
},
    {
  "name": "%PREÑEZ 150DEL",
  "expression": "DIVIDE([PREÑADA HASTA 150DEL],[VACA S],\"ERROR\")",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "cb6e98c2-f1a2-4459-ae61-3d2f668ef3d9",
  "dataType": "variant",
  "modifiedTime": "2023-09-20T22:37:18.883333",
  "structureModifiedTime": "2023-08-20T20:26:16.826667"
},
    {
  "name": "SRVXCONCEP",
  "expression": "DIVIDE(1,[%TC VACAS],\"ERROR\")",
  "lineageTag": "14bb24e5-5d7c-4a04-b75a-403def7e308e",
  "dataType": "variant",
  "modifiedTime": "2023-09-05T02:17:45.66",
  "structureModifiedTime": "2023-09-05T02:14:22.966667",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2023-09-05T02:14:52.563333"
    }
  ]
},
    {
  "name": "PorcentajeVacasSEstablo",
  "expression": "\nVAR EstabloSeleccionado = SELECTEDVALUE(ESTABLOSYCOD[ESTABLO2])\nRETURN\nCALCULATE(\n    [VACA S] / ([VACA S] + [VACA N]),\n    ESTABLOSYCOD[ESTABLO2] = EstabloSeleccionado,\n    ALL(ESTABLOSYCOD[PROVINCIA])\n)\n",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "5c5fbe79-cdf7-4392-9286-052d47e1f9b0",
  "dataType": "double",
  "modifiedTime": "2023-12-05T02:20:37.886667",
  "structureModifiedTime": "2023-12-05T01:19:46.04"
},
    {
  "name": "ALLL INSEMINACIONES",
  "expression": "CALCULATE([VACA S],ALL(INSEMINACIONES))",
  "formatString": "0",
  "lineageTag": "0183b486-e5b8-4082-a401-bbd27aaa9750",
  "dataType": "int64",
  "modifiedTime": "2023-12-05T02:54:42.586667",
  "structureModifiedTime": "2023-12-05T02:43:20.113333"
},
    {
  "name": "ALLLSELECT (TC) INSEMINACIONES",
  "expression": "CALCULATE([%TC VACAS],ALLSELECTED((INSEMINACIONES)))",
  "formatString": "0.0\\ %;-0.0\\ %;0.0\\ %",
  "lineageTag": "1d4ff1cd-b4ba-4ad4-834c-7d2e94514546",
  "dataType": "double",
  "modifiedTime": "2023-12-05T03:00:39.183333",
  "structureModifiedTime": "2023-12-05T02:47:12.496667"
},
    {
  "name": "%TC VACAS Año Anterior",
  "expression": "\nCALCULATE(\n    [VACA S] / ([VACA S] + [VACA N]),\n    SAMEPERIODLASTYEAR('CALENDARIOG'[Date])\n)",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "c6c22d3d-4dd9-4ded-9eec-11195ee8b9e7",
  "dataType": "double",
  "modifiedTime": "2023-12-06T04:57:17.026667",
  "structureModifiedTime": "2023-12-06T04:39:37.94"
},
    {
  "name": "%TC VACAS PROMEDIO AÑO ANTERIOR",
  "expression": "\nCALCULATE([ALLLSELECT (TC) INSEMINACIONES]\n   ,\n    SAMEPERIODLASTYEAR('CALENDARIOG'[Date])\n)",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "e151010f-d5db-4442-9859-d55f44e3586b",
  "dataType": "double",
  "modifiedTime": "2023-12-06T04:57:30.646667",
  "structureModifiedTime": "2023-12-06T04:52:15.736667"
},
    {
  "name": "SPM TC",
  "expression": "CALCULATE('AAMEDIDAS INSEMINACIONES (2)'[%TC VACAS],DATEADD(CALENDARIOG[Date],-12,MONTH))",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "0be48bf6-ce86-4b62-8016-944f4010c419",
  "dataType": "double",
  "modifiedTime": "2024-03-06T04:57:06.536667",
  "structureModifiedTime": "2024-03-06T04:55:21.823333"
},
    {
  "name": "VACA S 2LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=2,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "90c2e78a-58f8-4973-961e-9d59157dee7c",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:21:52.416667",
  "structureModifiedTime": "2024-05-12T23:21:30.106667"
},
    {
  "name": "VACA S 3+LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>=3,'INSEMINACIONES'[DXREAL]=\"S\")",
  "formatString": "0",
  "lineageTag": "3d9748cf-4650-49f5-8ea7-d68da91d5898",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:22:32.6",
  "structureModifiedTime": "2024-05-12T23:22:05.926667"
},
    {
  "name": "VACA N 2LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=2,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "df7e5ec8-0f62-4a21-9e49-ce49c863ba04",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:24:09.986667",
  "structureModifiedTime": "2024-05-12T23:23:48.483333"
},
    {
  "name": "VACA N 3+LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>=3,'INSEMINACIONES'[DXREAL]=\"N\")",
  "formatString": "0",
  "lineageTag": "7217e62a-c0b6-4b85-af6f-07039634e3e7",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:24:42.893333",
  "structureModifiedTime": "2024-05-12T23:24:21.193333"
},
    {
  "name": "TS 2LC",
  "expression": "[VACA S 2LC]+[VACA N 2LC]",
  "formatString": "0",
  "lineageTag": "8695f992-5bbb-4b6d-b24c-72b21e414743",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:26:21.48",
  "structureModifiedTime": "2024-05-12T23:25:14.666667"
},
    {
  "name": "TS 3+LC",
  "expression": "[VACA S 3+LC]+[VACA N 3+LC]",
  "formatString": "0",
  "lineageTag": "f19259d8-3f60-485c-8d56-6c6f40b49014",
  "dataType": "int64",
  "modifiedTime": "2024-05-12T23:27:01.67",
  "structureModifiedTime": "2024-05-12T23:26:35.806667"
},
    {
  "name": "%TC VACAS 2LC",
  "expression": "[VACA S 2LC]/[TS 2LC]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "ea6ad695-0d8b-4080-9886-05f84d632a1e",
  "dataType": "double",
  "modifiedTime": "2024-05-12T23:28:30.413333",
  "structureModifiedTime": "2024-05-12T23:27:18.313333"
},
    {
  "name": "%TC VACAS 3+LC",
  "expression": "[VACA S 3+LC]/[TS 3+LC]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "93009cc3-2bbd-4be7-8f2e-03f1e6d6b05f",
  "dataType": "double",
  "modifiedTime": "2024-05-12T23:32:35.623333",
  "structureModifiedTime": "2024-05-12T23:28:41.406667"
},
    {
  "name": "VACA DIM >1LC",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[LC REAL]>1)",
  "lineageTag": "212b95e1-4ca4-4b4e-b458-a376c5ef9661",
  "dataType": "double",
  "modifiedTime": "2024-05-13T00:31:06.07",
  "structureModifiedTime": "2024-05-13T00:29:51.27",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-13T00:31:06.066667"
    }
  ]
},
    {
  "name": "VACA DIM 1LC",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[LC REAL]=1)",
  "lineageTag": "53c7e305-de50-470b-afc7-002615cf7ce2",
  "dataType": "double",
  "modifiedTime": "2024-05-13T00:32:27.97",
  "structureModifiedTime": "2024-05-13T00:32:05.846667",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-13T00:32:27.966667"
    }
  ]
},
    {
  "name": "VACA DIM 2LC",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[LC REAL]=2)",
  "lineageTag": "20ebbf70-3e11-4bb8-8ba0-b9826d40ab55",
  "dataType": "double",
  "modifiedTime": "2024-05-13T00:34:50.163333",
  "structureModifiedTime": "2024-05-13T00:34:27.07",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-13T00:34:50.16"
    }
  ]
},
    {
  "name": "VACA DIM 3+LC",
  "expression": "CALCULATE(AVERAGE('INSEMINACIONES'[SRVDIM]),'INSEMINACIONES'[LC REAL]>=3)",
  "lineageTag": "7c5f86a8-398d-4619-889f-de9b3812f154",
  "dataType": "double",
  "modifiedTime": "2024-05-13T00:36:05.233333",
  "structureModifiedTime": "2024-05-13T00:35:35.163333",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-13T00:36:05.23"
    }
  ]
},
    {
  "name": "VACA DIM CONCEP >1LC",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>=1,'INSEMINACIONES'[DXREAL]=\"S\")",
  "lineageTag": "f837d260-ad0d-4a35-b995-a74d82939d3b",
  "dataType": "int64",
  "modifiedTime": "2024-05-13T02:47:02.533333",
  "structureModifiedTime": "2024-05-13T00:47:43.246667",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-13T00:48:14.256667"
    }
  ]
},
    {
  "name": "DesvEstPobl Dim",
  "expression": "CALCULATE(STDEV.P('INSEMINACIONES'[SrvDim]), 'INSEMINACIONES'[LC REAL] >= 1, 'INSEMINACIONES'[DXREAL] = \"S\")\n",
  "formatString": "0",
  "lineageTag": "6c0dc4a9-207a-4b24-a250-872003e1c9c1",
  "dataType": "double",
  "modifiedTime": "2024-05-22T02:15:49.243333",
  "structureModifiedTime": "2024-05-22T02:06:44.816667"
},
    {
  "name": "PromedioPoblacional Dim",
  "expression": "CALCULATE(AVERAGEX('INSEMINACIONES', 'INSEMINACIONES'[SrvDim]), 'INSEMINACIONES'[LC REAL] >= 1, 'INSEMINACIONES'[DXREAL] = \"S\")\n",
  "lineageTag": "ae9a71e4-972b-438f-81bd-fb9960f710fb",
  "dataType": "double",
  "modifiedTime": "2024-05-22T02:17:11.273333",
  "structureModifiedTime": "2024-05-22T02:16:51.31",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-22T02:17:11.27"
    }
  ]
},
    {
  "name": "Mediana Dim",
  "expression": "CALCULATE(MEDIANX('INSEMINACIONES', 'INSEMINACIONES'[SrvDim]), 'INSEMINACIONES'[LC REAL] >= 1, 'INSEMINACIONES'[DXREAL] = \"S\")\n\n",
  "lineageTag": "916b1401-324b-455b-b289-9f7146169d12",
  "dataType": "variant",
  "modifiedTime": "2024-05-22T02:20:43.423333",
  "structureModifiedTime": "2024-05-22T02:18:25.773333",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-05-22T02:18:40.136667"
    }
  ]
},
    {
  "name": "CORR ITHMIN-DXREAL",
  "lineageTag": "2fc92fe6-abfe-4544-839d-a4c3880a3a8d",
  "dataType": "int64",
  "modifiedTime": "2024-06-10T17:59:41.71",
  "structureModifiedTime": "2024-06-10T17:51:42.69"
},
    {
  "name": "Promedio poblacionaldimAnterior",
  "expression": "\nCALCULATE(\n   CALCULATE(AVERAGEX('INSEMINACIONES', 'INSEMINACIONES'[SrvDim]), 'INSEMINACIONES'[LC REAL] >= 1, 'INSEMINACIONES'[DXREAL] = \"S\",\n    SAMEPERIODLASTYEAR('CALENDARIOG'[Date])\n))",
  "lineageTag": "42396a92-34c9-492f-bee1-979d632426fa",
  "dataType": "double",
  "modifiedTime": "2024-12-09T18:37:59.576667",
  "structureModifiedTime": "2024-12-09T18:36:15.173333",
  "annotations": [
    {
      "name": "PBI_FormatHint",
      "value": "{\"isGeneralNumber\":true}",
      "modifiedTime": "2024-12-09T18:36:58.106667"
    }
  ]
},
    {
  "name": "T TOROS",
  "expression": "[TS VACAS]+[TS VAQUILLA]",
  "formatString": "0",
  "lineageTag": "3db9dd52-aec9-4949-80da-ba058898af77",
  "dataType": "int64",
  "modifiedTime": "2025-03-17T17:42:13.9",
  "structureModifiedTime": "2025-03-17T17:41:29.83"
},
    {
  "name": "Insem en Rango",
  "expression": "\nVAR d = MIN('Rangos_Aborto'[Desde])\nVAR h = MAX('Rangos_Aborto'[Hasta])\nRETURN\nCALCULATE(\n    COUNTROWS(INSEMINACIONES),\n    FILTER(\n        ALL(INSEMINACIONES),\n        NOT ISBLANK(INSEMINACIONES[SRVDAT]) &&\n        NOT ISBLANK(INSEMINACIONES[RESTAABT-SRVDAT]) &&\n        VAR dias = DATEDIFF(INSEMINACIONES[SRVDAT], INSEMINACIONES[RESTAABT-SRVDAT], DAY)\n        RETURN dias >= d && dias <= h\n    )\n)\n",
  "formatString": "0",
  "lineageTag": "ed83bd4b-2148-4522-a587-0861e9bedc09",
  "dataType": "int64",
  "modifiedTime": "2025-10-02T13:11:51.976667",
  "structureModifiedTime": "2025-10-02T13:09:26.016667"
},
    {
  "name": "%TC VACAS por ITH Rango",
  "expression": "\nVAR FechasITH =\n    VALUES ( TEMPERATURA[FECHA] )\nRETURN\nCALCULATE (\n    [%TC VACAS],\n    TREATAS ( FechasITH, INSEMINACIONES[SrvDat] )\n)\n",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "7ee9bec0-769f-45d0-82ed-8473dd3bf46b",
  "dataType": "double",
  "modifiedTime": "2026-01-22T03:23:03.01",
  "structureModifiedTime": "2026-01-22T03:22:12.216667"
}
  ],
  "datacolumns": [
    {
  "name": "Columna1",
  "dataType": "string",
  "sourceColumn": "Columna1",
  "lineageTag": "bb5d9066-3a39-4911-aa51-30171415fb5c",
  "summarizeBy": "none",
  "modifiedTime": "2023-08-08T16:28:02.216667",
  "structureModifiedTime": "2023-08-08T16:28:02.216667",
  "refreshedTime": "1699-12-31T00:00:00",
  "attributeHierarchy": {
    "state": "ready",
    "modifiedTime": "2025-12-01T19:32:04.196667",
    "refreshedTime": "2025-12-01T19:32:04.196667"
  },
  "annotations": [
    {
      "name": "SummarizationSetBy",
      "value": "Automatic",
      "modifiedTime": "2023-08-08T16:28:02.216667"
    }
  ]
}
  ]
}

