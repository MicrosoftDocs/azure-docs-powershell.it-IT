---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189783"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
Ottiene le posizioni in cui sono disponibili le risorse ExpressRoutePort.

## SINTASSI

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzExpressRoutePortsLocation** viene usato per recuperare le posizioni in cui sono disponibili le risorse di ExpressRoutePort. Dato un percorso specifico come input, il cmdlet visualizza i dettagli della posizione, ad esempio l'elenco di larghezze di banda disponibili in tale posizione.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Elenca le posizioni in cui sono disponibili le risorse ExpressRoutePort.

### Esempio 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Elenca le larghezze di banda di ExpressRoutePort disponibili nella posizione $loc.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -LocationName
Nome della posizione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation

## NOTE

## COLLEGAMENTI CORRELATI
