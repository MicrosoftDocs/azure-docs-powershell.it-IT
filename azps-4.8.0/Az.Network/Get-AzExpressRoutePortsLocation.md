---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192109"
---
# Get-AzExpressRoutePortsLocation

## Sinossi
Ottiene le posizioni in cui sono disponibili le risorse di ExpressRoutePort.

## SINTASSI

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzExpressRoutePortsLocation** viene usato per recuperare le posizioni in cui sono disponibili le risorse di ExpressRoutePort. Data una posizione specifica come input, il cmdlet Visualizza i dettagli di tale posizione, ovvero l'elenco delle larghezze di banda disponibili in tale posizione.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Elenca le posizioni in cui sono disponibili le risorse di ExpressRoutePort.

### Esempio 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Elenca le larghezze di banda ExpressRoutePort disponibili in posizione $loc.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation

## Note

## COLLEGAMENTI CORRELATI
