---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518023"
---
# Find-AzureRmResourceGroup

## Sinossi
Cerca gruppi di risorse.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Find-AzureRmResourceGroup** Cerca i gruppi di risorse usando i parametri specificati.

## ESEMPI

### Esempio 1: trovare tutti i gruppi di risorse
```
PS C:\>Find-AzureRmResourceGroup
```

Questo comando Trova tutti i gruppi di risorse.

### Esempio 2: trovare i gruppi di risorse per nome di tag
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Questo comando Trova tutti i gruppi di risorse con un tag denominato testtag.

### Esempio 3: trovare i gruppi di risorse per nome di tag e valore
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Questo comando Trova tutti i gruppi di risorse con un tag denominato testtag e il valore testVal.

## PARAMETRI

### -ApiVersion
Specifica la versione dell'API del provider di risorse da usare. Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.

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

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Pre
Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Specifica le informazioni sui tag, come tabella hash, per filtrare i risultati. Usare i formati seguenti:

@ {tagName = $null} o @ {tagName =' tagValue '}.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### System. Management. Automation. PSObject

## Note

## COLLEGAMENTI CORRELATI
