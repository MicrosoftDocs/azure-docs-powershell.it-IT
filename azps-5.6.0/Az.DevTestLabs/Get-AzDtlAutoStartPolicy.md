---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 1a9e095aa12b456d2758986328c442952b959d6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977133"
---
# Get-AzDtlAutoStartPolicy

## SYNOPSIS
Recupera i criteri di avvio automatico di un laboratorio nei laboratori DevTest.

## SINTASSI

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDtlAutoStartPolicy** ottiene il criterio di avvio automatico di un lab che pianifica le macchine virtuali di laboratorio per l'avvio automatico.
Il cmdlet restituisce lo stato abilitato o disabilitato del criterio e i giorni della settimana e dell'ora del giorno impostati per consentire alle macchine virtuali lab di essere pianificate per l'avvio automatico.

## ESEMPI

### Esempio 1

Recupera i criteri di avvio automatico di un laboratorio nei laboratori DevTest. (autogenerati)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDtlAutoStartPolicy -LabName <String> -ResourceGroupName MyResourceGroup
```

## PARAMETERS

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

### -LabName
Specifica il nome del lab per cui questo cmdlet ottiene i criteri di avvio automatico.

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule

## NOTE

## COLLEGAMENTI CORRELATI

[Set-AzDtlAutoStartPolicy](./Set-AzDtlAutoStartPolicy.md)


