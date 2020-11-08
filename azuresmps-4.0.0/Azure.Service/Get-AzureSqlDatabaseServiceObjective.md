---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023526"
---
# Get-AzureSqlDatabaseServiceObjective

## Sinossi
Ottiene gli obiettivi di servizio per un server di database SQL di Azure.

## SINTASSI

### ByConnectionContext (impostazione predefinita)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureSqlDatabaseServiceObjective** ottiene gli obiettivi di servizio per un server di database SQL di Azure.
Gli obiettivi di servizio sono definiti livelli di prestazioni.
Se non specifichi un obiettivo di servizio, questo cmdlet restituisce tutti gli obiettivi di servizio validi per il server specificato.

Questo cmdlet si applica ai livelli di servizio di base, standard e Premium.

## ESEMPI

### Esempio 1: ottenere tutti gli obiettivi del servizio usando un contesto di connessione
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Questo comando ottiene tutti gli obiettivi di servizio per il server che il contesto di connessione $Context specifica.

### Esempio 2: ottenere tutti gli obiettivi del servizio usando un nome di server
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Questo comando ottiene tutti gli obiettivi di servizio per il server denominato Server01.

## PARAMETRI

### -Contesto
Specifica il contesto di connessione di un server.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome di un server.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjective
Specifica un oggetto che rappresenta l'obiettivo del servizio ottenuto da questo cmdlet.
I valori validi sono: 

- Base: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973C-54e79e15235b
- Standard (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-B5FA-177c226f28b7
- * Standard (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-CFB1-464B-b252-925be0a19446

* Standard (S3) fa parte del più recente aggiornamento di database SQL V12 (Preview).
Per altre informazioni, vedere [novità di Azure SQL database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) in Azure Library.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Specifica il nome di un obiettivo di servizio da ottenere.
I valori validi sono: Basic, S0, S1, S2, S3, P1, P2 e P3.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServiceObjective

## OUTPUT

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## Note

## COLLEGAMENTI CORRELATI

[Database SQL di Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Ottenere un obiettivo a livello di servizio](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Operazioni per i database SQL di Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


