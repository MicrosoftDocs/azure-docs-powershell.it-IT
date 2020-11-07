---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687919"
---
# New-AzureRmDataMigrationService

## Sinossi
Crea una nuova istanza del servizio di migrazione del database di Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## Descrizione
Il cmdlet New-AzureRmDataMigrationService crea una nuova istanza del servizio di migrazione del database di Azure. Questo cmdlet accetta il nome del gruppo di risorse Azure esistente, il nome univoco per la nuova istanza del servizio di migrazione del database di Azure da creare, l'area in cui viene eseguito il provisioning dell'istanza, il nome del codice di lavoro DMS e il nome della subnet virtuale di Azure in cui il servizio deve risiedere. Non esiste alcun parametro per il nome dell'abbonamento, perché è previsto che l'utente specifichi l'abbonamento predefinito della sessione di accesso di Azure o esegua Get-AzureRmSubscription-Subscriptionname "abbonamento" | Select-AzureRmSubscription per selezionare un altro abbonamento.

## ESEMPI

### Esempio 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

Nell'esempio precedente viene illustrato come creare una nuova istanza del servizio di migrazione del database di Azure denominata TestService nell'area centrale degli Stati Uniti.


## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Posizione dell'istanza del servizio di migrazione del database di Azure da creare, che corrisponde a un'area di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Nome dell'istanza del servizio di migrazione del database di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
SKU per l'istanza del servizio di migrazione del database di Azure. I valori possibili attualmente sono Basic_1vCore, Basic_2vCores, GeneralPurpose_4vCores

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualSubnetId
Nome della subnet nella rete virtuale specificata da usare per l'istanza del servizio di migrazione del database di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## OUTPUT

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## Note

## COLLEGAMENTI CORRELATI

