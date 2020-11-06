---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507535"
---
# New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential

## Sinossi
Crittografare le credenziali nel servizio collegato con l'Integration runtime specificato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByFactoryName (impostazione predefinita)
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet New-AzureRmDataFactoryV2LinkedServiceEncryptCredential crittografa le credenziali nel servizio collegato con l'Integration runtime specificato.

## ESEMPI

### Esempio 1: crittografare creadentials in un servizio collegato
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

Questo comando crittografa le credenziali in file D:\sql.jscon il runtime di integrazione denominato myIR.

## PARAMETRI

### -DataFactory
Oggetto Data Factory.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Datafactoryname
Nome della factory di dati.

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

### -DefinitionFile
Percorso del file JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Esegue il cmdlet senza richiedere conferma.

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

### -IntegrationRuntimeName
Nome del runtime di integrazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parametri: DataFactory (ByValue)

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI
