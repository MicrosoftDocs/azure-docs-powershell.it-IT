---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 341e2b4ad820b3a18e5515b54388ce517762d0ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855401"
---
# New-AzPeering

## Sinossi
Crea una nuova risorsa peering ARM

## SINTASSI

### Exchange (impostazione predefinita)
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ConvertLegacyPeering
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Diretto
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Crea un peering ARM per l'abbonamento. Per altre informazioni sulla creazione di un oggetto di connessione, vedere [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) o [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .

## ESEMPI

### Creare un nuovo peering diretto
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

Creare un nuovo peering diretto con una singola connessione presso la struttura di Seattle con PeerAsn 65000

### Creare un nuovo peering di Exchange
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

Creare un nuovo peering di Exchange

### Convertire il peering legacy in peering ARM
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## PARAMETRI

### -AsJob
Eseguire in background.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectConnection
Creare un nuovo collegamento diretto usando la New-AzExchangePeeringConnection e la pipe al comando.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeConnection
Creare una nuova connessione di Exchange usando la New-AzExchangePeeringConnection e la pipe al comando.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
USA Get-AzLegacyPeering per recuperare questo oggetto.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome univoco di PSPeering.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeerAsnResourceId
ID risorsa ASN peer. usare Get-AzPeerAsn per recuperare l'ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringLocation
Posizione fisica diversa dall'area di Azure.
Usa il tipo Get-AzPeeringLocation-kind \< \> use City Name come Key.

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Selezionare Basic_Direct_Free o Premium_Direct_Free a meno che non venga detto esplicitamente di selezionare un'altra opzione.

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Tag da associare al servizio peering Microsoft.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering

## Note

## COLLEGAMENTI CORRELATI
