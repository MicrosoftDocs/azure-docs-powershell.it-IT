---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 17bc16b38bc967f9997b22d7dd86b056253d8a18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856441"
---
# Get-AzLocation

## Sinossi
Ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.

## SINTASSI

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzLocation** ottiene tutti i percorsi e i provider di risorse supportati per ogni posizione.

## ESEMPI

### Esempio 1: ottenere tutti i percorsi e i provider di risorse supportati
```
PS C:\>Get-AzLocation
```

Questo comando consente di ottenere tutte le posizioni e i provider di risorse supportati per ogni posizione.

## PARAMETRI

### -ApiVersion
Specifica la versione dell'API supportata dal provider di risorse.
Puoi specificare una versione diversa rispetto alla versione predefinita.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProviderLocation

## Note

## COLLEGAMENTI CORRELATI
