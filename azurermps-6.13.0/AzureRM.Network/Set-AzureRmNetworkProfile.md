---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507387"
---
# Set-AzureRmNetworkProfile

## Sinossi
Imposta lo stato obiettivo per un profilo di rete esistente

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmPublicIpPrefix** imposta lo stato dell'obiettivo per un profilo di rete.

## ESEMPI

### Esempio 1
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

Il primo comando ottiene un profilo di rete esistente. Il secondo comando aggiorna un tag e il terzo aggiunge una configurazione di interfaccia di rete nel profilo di rete. Il quarto comando Aggiorna il profilo di rete.

## PARAMETRI

### -AsJob
Esegui cmdlet in background

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

### -NetworkProfile
Profilo di rete

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

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

### Microsoft. Azure. Commands. Network. Models. PSNetworkProfile

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSNetworkProfile

## Note

## COLLEGAMENTI CORRELATI
