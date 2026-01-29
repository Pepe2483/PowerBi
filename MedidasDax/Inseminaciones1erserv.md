{
  "InstanceID": "ee7319f0-3c31-4d34-b236-5054a6913521",
  "measures": [
    {
  "name": "1 VACA S 1LC 50D",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"S\",'INSEMINACIONES'[SrvNumLact]=1,'INSEMINACIONES'[SrvDim]<50)",
  "formatString": "0",
  "lineageTag": "a2a938fd-e2f6-403c-98fd-0c3101a96d62",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.806667",
  "structureModifiedTime": "2023-08-09T00:44:56.736667"
},
    {
  "name": "1 VACAS 1LC 50D",
  "expression": "[1 VACA S 1LC 50D]+[1 VACA N 1LC 50D]",
  "formatString": "0",
  "lineageTag": "df211a0c-ff17-4d5b-8fd7-ff12f970d276",
  "dataType": "int64",
  "modifiedTime": "2023-08-09T00:50:19.233333",
  "structureModifiedTime": "2023-08-09T00:44:47.976667"
},
    {
  "name": "1 VACA N 1LC 50D",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"N\",'INSEMINACIONES'[SrvNumLact]=1,'INSEMINACIONES'[SrvDim]<50)",
  "formatString": "0",
  "lineageTag": "1fa89f4d-8404-4ecf-9c35-e7ba9d82434c",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.806667",
  "structureModifiedTime": "2023-08-09T00:45:07.083333"
},
    {
  "name": "1 TC 1LC 50 D",
  "expression": "[1 VACAS 1LC 50D]/[1 VACAS 1LC 50D]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "1725fffe-e1e6-4583-833e-3f495fbefd22",
  "dataType": "double",
  "modifiedTime": "2023-08-09T00:50:19.276667",
  "structureModifiedTime": "2023-08-09T00:46:01.89"
},
    {
  "name": "2 VACA S 1LC 50-60D",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"S\",'INSEMINACIONES'[SrvNumLact]=1,'INSEMINACIONES'[SrvDim]>=50,'INSEMINACIONES'[SrvDim]<60)",
  "formatString": "0",
  "lineageTag": "3807560c-5ceb-42f5-9c9b-ea86859579ba",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.806667",
  "structureModifiedTime": "2023-08-09T00:51:37.806667"
},
    {
  "name": "2 VACA N 1LC 50-60D",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]=1,'INSEMINACIONES'[DXREAL]=\"N\",'INSEMINACIONES'[SrvNumLact]=1,'INSEMINACIONES'[SrvDim]>=50,'INSEMINACIONES'[SrvDim]<60)",
  "formatString": "0",
  "lineageTag": "6307bc69-cc3c-44de-b1cc-29b867457ca7",
  "dataType": "int64",
  "modifiedTime": "2023-08-18T23:41:57.806667",
  "structureModifiedTime": "2023-08-09T00:54:08.89"
},
    {
  "name": "2 VACAS 1LC 50-60D",
  "expression": "[2 VACA S 1LC 50-60D]+[2 VACA N 1LC 50-60D]",
  "formatString": "0",
  "lineageTag": "f6ccb292-361d-4bb9-aa44-514aab8a9dce",
  "dataType": "int64",
  "modifiedTime": "2023-08-09T00:58:46.206667",
  "structureModifiedTime": "2023-08-09T00:56:31.806667"
},
    {
  "name": "VACA N 1erserv",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"N\",inseminaciones[SrvNumLact]=1)",
  "formatString": "0",
  "lineageTag": "326211b0-1e3b-4b92-b9b8-56a49fbba66d",
  "dataType": "int64",
  "modifiedTime": "2023-09-26T21:33:46.726667",
  "structureModifiedTime": "2023-09-26T21:33:46.39"
},
    {
  "name": "VACA S 1erserv",
  "expression": "CALCULATE(COUNT('INSEMINACIONES'[COW]),'INSEMINACIONES'[LC REAL]>0,'INSEMINACIONES'[DXREAL]=\"S\",inseminaciones[SrvNumLact]=1)",
  "formatString": "0",
  "lineageTag": "30efa412-aaa4-4880-a21f-14afddf515f9",
  "dataType": "int64",
  "modifiedTime": "2023-09-26T21:33:58.463333",
  "structureModifiedTime": "2023-09-26T21:33:58.086667"
},
    {
  "name": "TS VACAS 1ER SERV",
  "expression": "[VACA S 1erserv]+[VACA N 1erserv]",
  "formatString": "0",
  "lineageTag": "af20414c-584d-4919-835a-5d7864b13577",
  "dataType": "int64",
  "modifiedTime": "2023-09-26T21:35:32.79",
  "structureModifiedTime": "2023-09-26T21:34:35"
},
    {
  "name": "%TC 1ER SERV",
  "expression": "[VACA S 1erserv]/[TS VACAS 1ER SERV]",
  "formatString": "0.00\\ %;-0.00\\ %;0.00\\ %",
  "lineageTag": "14b1c5e8-b73a-43eb-b9f5-85d7cd2b8035",
  "dataType": "double",
  "modifiedTime": "2023-09-26T21:37:03.266667",
  "structureModifiedTime": "2023-09-26T21:35:46.216667"
}
  ],
  "datacolumns": [
    {
  "name": "Columna1",
  "dataType": "string",
  "sourceColumn": "Columna1",
  "lineageTag": "19f5e683-384c-4078-b2f7-7306def07447",
  "summarizeBy": "none",
  "modifiedTime": "2023-08-09T00:36:42.66",
  "structureModifiedTime": "2023-08-09T00:36:42.66",
  "refreshedTime": "1699-12-31T00:00:00",
  "attributeHierarchy": {
    "state": "ready",
    "modifiedTime": "2025-12-01T19:32:00.413333",
    "refreshedTime": "2025-12-01T19:32:00.413333"
  },
  "annotations": [
    {
      "name": "SummarizationSetBy",
      "value": "Automatic",
      "modifiedTime": "2023-08-09T00:36:42.66"
    }
  ]
}
  ]
}
