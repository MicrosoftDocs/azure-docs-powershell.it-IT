---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 41b147307d253271e24667bd61d827c245f4500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686439"
---
# Save-AzureRmDataFactoryLog

## Sinossi
Scarica i file di log dall'elaborazione di Azure HDInsight.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByFactoryName (impostazione predefinita)
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Save-AzureRmDataFactoryLog** Scarica i file di log associati all'elaborazione di Azure HDInsight di progetti di suini o hive o per attività personalizzate nel disco rigido locale.
Viene eseguito prima di tutto il cmdlet Get-AzureRmDataFactoryRun per ottenere un ID per un'attività eseguita per una fetta di dati e quindi usare tale ID per recuperare i file di log dall'archiviazione BLOB (Binary Large Object) associata al cluster HDInsight.
Se non specifichi il parametro *DownloadLogs* , il cmdlet restituisce semplicemente la posizione dei file di log.
Se specifichi *DownloadLogs* senza specificare una directory di output (parametro di *output* ), i file di log vengono scaricati nella cartella documenti predefiniti.
Se specifichi *DownloadLogs* insieme a una cartella di output ( *output* ), i file di log vengono scaricati nella cartella specificata.

## ESEMPI

### Esempio 1: salvare i file di log in una cartella specifica
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Questo comando Salva i file di log per l'attività eseguita con l'ID di 841b77c9-d56c-48D1-99A3-8c16c3e77d39 in cui l'attività appartiene a una pipeline nella Factory di dati denominata LogProcessingFactory nel gruppo di risorse denominato ADF.
I file di log vengono salvati nella cartella C:\Test.

### Esempio 2: salvare i file di log nella cartella documenti predefiniti
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Questo comando Salva i file di log nella cartella documenti (impostazione predefinita).

### Esempio 3: ottenere la posizione dei file di log
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Questo comando restituisce la posizione dei file di log.
Tieni presente che *DownloadLogs* non è specificato.

## PARAMETRI

### -DataFactory
Specifica un oggetto **PSDataFactory** .

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Specifica il nome di una data factory.
Questo cmdlet Scarica i file di log per il data factory specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -DownloadLogs
Indica che questo cmdlet Scarica i file di log nel computer locale.
Se non si specifica la cartella *ouptut* , i file vengono salvati nella cartella documenti in una sottocartella.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID dell'esecuzione dell'attività per la sezione dati.
Usa il cmdlet Get-AzureRmDataFactoryRun per ottenere un ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Output
Specifica la cartella di output in cui vengono salvati i file di log scaricati.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse Azure.
Questo cmdlet crea una factory di dati che appartiene al gruppo specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## OUTPUT

### Microsoft. Azure. Commands. datafactories. Models. PSRunLogInfo

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory

## COLLEGAMENTI CORRELATI

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Get-AzureRmDataFactoryPipeline](./Get-AzureRmDataFactoryPipeline.md)

[New-AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Remove-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Suspend-AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


