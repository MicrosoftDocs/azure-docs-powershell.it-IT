---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: bd61b666dd321ec9007d413030cb899eeeb92778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520744"
---
# Start-AzureRmSqlServerUpgrade

## Sinossi
Avvia l'aggiornamento di un server di database SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureRmSqlServerUpgrade** avvia l'aggiornamento di un server di database SQL di Azure versione 11 alla versione 12.
È possibile monitorare lo stato di avanzamento di un aggiornamento usando il cmdlet Get-AzureRmSqlServerUpgrade.

## ESEMPI

### Esempio 1: aggiornare un server
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Questo comando consente di aggiornare il server denominato Server01 assegnato al gruppo di risorse TesourceGroup01.

### Esempio 2: aggiornare un server usando le indicazioni per orari e database
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Il primo comando crea un tempo di cinque minuti in futuro usando il cmdlet Get-Date.
Il comando Archivia la data nella variabile $ScheduleTime.
Per altre informazioni, digitare `Get-Help Get-Date` .

Il secondo comando crea un oggetto **RecommendedDatabaseProperties** e quindi archivia l'oggetto nella variabile $DatabaseMap.

I tre comandi seguenti assegnano i valori alle proprietà dell'oggetto archiviato in $DatabaseMap.

Il comando finale consente di aggiornare il server esistente denominato Server01 alla versione 12,0.
Il momento più recente per l'aggiornamento è di cinque minuti dopo l'esecuzione del comando, come specificato dalla variabile $ScheduleTime.
Dopo l'aggiornamento, il database ContosoDB eseguirà l'edizione standard e avrà l'obiettivo di livello di servizio S0.

## PARAMETRI

### -DatabaseCollection
Specifica una matrice di oggetti **RecommendedDatabaseProperties** che questo cmdlet USA per l'aggiornamento del server.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
Specifica una matrice di oggetti **UpgradeRecommendedElasticPoolProperties** da usare per l'aggiornamento del server.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
Specifica il tempo più iniziale, come oggetto **DateTime** , per aggiornare il server.
Specificare un valore nel formato ISO8601, in ora UTC (Coordinated Universal Time).
Per altre informazioni, digitare `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server che questo cmdlet aggiorna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Specifica la versione a cui questo cmdlet aggiorna il server.
L'unico valore valido è 12,0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Stop-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)


