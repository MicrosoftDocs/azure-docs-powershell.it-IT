---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177646"
---
# New-AzVmssIpConfig

## SYNOPSIS
Crea una configurazione IP per un'interfaccia di rete di un VMSS.

## SINTASSI

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVmssIpConfig** crea un oggetto configurazione IP per un'interfaccia di rete di un set di scalabilità delle macchine virtuali (VMSS).
Specificare la configurazione da questo cmdlet come *parametro IPConfiguration* del cmdlet Add-AzVmssNetworkInterfaceConfiguration.

## ESEMPI

### Esempio 1: Creare un oggetto di configurazione IP per un'interfaccia VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface02.
Il comando usa un ID subnet definito in precedenza memorizzato in $SubnetId.
Il comando archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso futuro **con Add-AzVmssNetworkInterfaceConfiguration.**

### Esempio 2: Creare un oggetto di configurazione IP che include le impostazioni del pool NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Questo comando crea un oggetto configurazione IP denominato ContosoVmssInterface03 e quindi lo archivia nella variabile $IPConfiguration per un uso futuro.
Il comando usa un ID subnet definito in precedenza memorizzato in $SubnetId.
Il comando archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso futuro.
Il comando specifica i valori per *i parametri LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId.*

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
Specifica una matrice di riferimenti a pool di indirizzi back-end di servizi di bilanciamento del carico.
Un set di scale può fare riferimento a pool di indirizzi back-end di una bilanciamento del carico pubblico e uno interno.
Più set di scala non possono usare la stessa bilanciamento del carico.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
Le impostazioni dns da applicare agli indirizzi publicIP.
Etichetta del nome di dominio delle impostazioni Dns da applicare agli indirizzi PublicIP.
La concatenazione dell'etichetta del nome di dominio e dell'indice della macchina virtuale sarà l'etichetta dei nomi di dominio delle risorse Indirizzo IP pubblico che verranno create.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifica un ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Specifica una matrice di oggetti Tag IP.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Specifica una matrice di riferimenti a pool NAT (Incoming Network Address Translation) dei servizi di bilanciamento del carico.
Un set di scala può fare riferimento a pool di NAT in ingresso di una bilanciamento del carico pubblico e uno interno.
Più set di scala non possono usare la stessa bilanciamento del carico.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Specifica una matrice di riferimenti a pool NAT in ingresso delle servizi di bilanciamento del carico.
Un set di scala può fare riferimento a pool di NAT in ingresso di una bilanciamento del carico pubblico e uno interno.
Più set di scala non possono usare la stessa bilanciamento del carico.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome della configurazione IP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Principale
Specifica la configurazione IP principale nel caso in cui l'interfaccia di rete abbia più di una configurazione IP.

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

### -PrivateIPAddressVersion
Specificare la configurazione IP per l'indirizzo IP privato.  Il valore predefinito è IPv4.  I valori possibili sono "IPv4" e "IPv6".

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

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Timeout di inattività dell'indirizzo IP pubblico.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Nome di configurazione dell'indirizzo publicIP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Specificare la configurazione IP per l'indirizzo IP pubblico.  Il valore predefinito è IPv4.  I valori possibili sono "IPv4" e "IPv6".

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

### -PublicIPPrefix
ID del prefisso IP pubblico

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

### -SubnetId
Specifica l'ID subnet in cui la configurazione crea l'interfaccia di rete VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## OUTPUT

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


