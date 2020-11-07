---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863602"
---
# New-AzVmssIpConfig

## Sinossi
Crea una configurazione IP per un'interfaccia di rete di un VMSS.

## SINTASSI

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzVmssIpConfig** crea un oggetto di configurazione IP per un'interfaccia di rete di un set di scale della macchina virtuale (VMSS).
Specifica la configurazione di questo cmdlet come parametro *IPConfiguration* del cmdlet Add-AzVmssNetworkInterfaceConfiguration.

## ESEMPI

### Esempio 1: creare un oggetto di configurazione IP per un'interfaccia VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface02.
Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.
Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo con **Add-AzVmssNetworkInterfaceConfiguration**.

### Esempio 2: creare un oggetto di configurazione IP che include le impostazioni del pool NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface03 e lo archivia nella variabile $IPConfiguration per un uso successivo.
Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.
Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo.
Il comando specifica i valori per i parametri *LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId* .

## PARAMETRI

### -ApplicationGatewayBackendAddressPoolsId
Specifica una matrice di riferimenti ai pool di indirizzi back-end di bilanciamento del carico.
Un set di proporzioni può fare riferimento a pool di indirizzi backend di uno pubblico e di un bilanciamento del carico interno.
Più set di scale non possono usare lo stesso bilanciamento del carico.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
Impostazioni DNS da applicare agli indirizzi di publicIP.
L'etichetta del nome di dominio delle impostazioni DNS da applicare agli indirizzi di publicIP.
La concatenazione dell'etichetta del nome di dominio e dell'indice VM saranno le etichette dei nomi di dominio delle risorse degli indirizzi IP pubblici che verranno create.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Specifica un ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Specifica una matrice di riferimenti ai pool NAT (Network Address Translation) in ingresso dei gruppi di bilanciamento del carico.
Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.
Più set di scale non possono usare lo stesso bilanciamento del carico.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Specifica una matrice di riferimenti ai pool NAT in arrivo dei gruppi di bilanciamento del carico.
Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.
Più set di scale non possono usare lo stesso bilanciamento del carico.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della configurazione IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primaria
Specifica la configurazione IP primaria nel caso in cui l'interfaccia di rete abbia più di una configurazione IP.

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

### -PrivateIPAddressVersion
Specifica la configurazione IP è IPv4 o IPv6. Il valore predefinito viene considerato IPv4.  I valori possibili sono: "IPv4" e "IPv6".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Timeout inattivo dell'indirizzo IP pubblico.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Nome della configurazione dell'indirizzo publicIP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Specifica l'ID subnet in cui la configurazione crea l'interfaccia di rete VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration

## Note

## COLLEGAMENTI CORRELATI

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


