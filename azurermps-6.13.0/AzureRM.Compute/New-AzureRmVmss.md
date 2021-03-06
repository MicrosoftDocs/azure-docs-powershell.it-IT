---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507588"
---
# New-AzureRmVmss

## Sinossi
Crea un VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### DefaultParameter (impostazione predefinita)
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmVmss** crea un set di scale della macchina virtuale (VMSS) in Azure.
Usa il set di parametri Simple ( `SimpleParameterSet` ) per creare rapidamente una vmss preimpostata e le risorse associate. Usa il set di parametri predefinito ( `DefaultParameter` ) per scenari più avanzati quando devi configurare con precisione ogni componente di vmss e ogni risorsa associata prima della creazione.

## ESEMPI

### Esempio 1: creare un VMSS usando il **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Il comando precedente crea il seguente nome `$vmssName` :
* Gruppo di risorse
* Una rete virtuale
* Un bilanciamento del carico
* Un IP pubblico
* VMSS con 2 istanze

L'immagine predefinita scelta per le VM in VMSS è `2016-Datacenter Windows Server` e l'USK è `Standard_DS1_v2`

### Esempio 2: creare un VMSS usando il **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

L'esempio complesso precedente crea un VMSS, in seguito è una spiegazione di quanto sta accadendo:
* Il primo comando crea un gruppo di risorse con il nome e il percorso specificati.
* Il secondo comando usa il cmdlet **New-AzureRmStorageAccount** per creare un account di archiviazione.
* Il terzo comando usa quindi il cmdlet **Get-AzureRmStorageAccount** per ottenere l'account di archiviazione creato nel secondo comando e archivia il risultato nella variabile $STOAccount.
* Il quinto comando usa il cmdlet **New-AzureRmVirtualNetworkSubnetConfig** per creare una subnet e archivia il risultato nella variabile denominata $subnet.
* Il sesto comando usa il cmdlet **New-AzureRmVirtualNetwork** per creare una rete virtuale e archivia il risultato nella variabile denominata $VNet.
* Il settimo comando USA **Get-AzureRmVirtualNetwork** per ottenere informazioni sulla rete virtuale creata nel sesto comando e archivia le informazioni nella variabile denominata $VNet.
* Il comando ottavo e nono usa la **nuova-AzureRmPublicIpAddress** e **Get-AzureRmPublicIpAddress** per creare e ottenere informazioni da tale indirizzo IP pubblico.
* I comandi archiviano le informazioni nella variabile denominata $PubIP.
* Il decimo comando usa il cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** per creare un bilanciamento del carico frontend e archivia il risultato nella variabile denominata $frontend.
* L'undicesimo comando usa il **nuovo-AzureRmLoadBalancerBackendAddressPoolConfig** per creare una configurazione del pool di indirizzi back-end e archivia il risultato nella variabile denominata $BackendAddressPool.
* Il dodicesimo comando usa il **nuovo-AzureRmLoadBalancerProbeConfig** per creare un probe e archivia le informazioni sulla sonda nella variabile denominata $Probe.
* Il comando tredicesimo usa il cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** per creare una configurazione del pool NAT (Network Address Translation) in ingresso per il bilanciamento del carico.
* Il comando quattordicesima usa il **nuovo-AzureRmLoadBalancerRuleConfig** per creare una configurazione della regola di bilanciamento del carico e archivia il risultato nella variabile denominata $LBRule.
* Il comando quindicesimo usa il cmdlet **New-AzureRmLoadBalancer** per creare un bilanciamento del carico e archivia il risultato nella variabile denominata $ActualLb.
* Il comando sedicesimo USA **Get-AzureRmLoadBalancer** per ottenere informazioni sul bilanciamento del carico creato nel quindicesimo comando e archivia le informazioni nella variabile denominata $ExpectedLb.
* Il comando diciassettesimo usa il cmdlet **New-AzureRmVmssIPConfig** per creare una configurazione IP di vmss e archivia le informazioni nella variabile denominata $IPCfg.
* Il comando diciottesimo usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.
* Il comando diciannovesimo usa il cmdlet **New-AzureRmVmss** per creare vmss.

## PARAMETRI

### -AllocationMethod
Metodo di assegnazione per l'indirizzo IP pubblico del set di proporzioni (statico o dinamico).  Se non viene specificato alcun valore, l'allocazione sarà statica.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.

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

### -BackendPoolName
Nome del pool di indirizzi di backend da usare in bilanciamento del carico per questo set di proporzioni.  Se non viene specificato alcun valore, verrà creato un nuovo pool di backend con lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Numeri di porta backend usati dal bilanciamento del carico impostato su scala per comunicare con le VM nel set di proporzioni.  Se non sono specificati valori, le porte 3389 e 5985 verranno usate per le VM di Windows e la porta 22 verrà usata per le VM di Linux.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credenziale
Credenziali di amministratore (nome utente e password) per VM in questo set di proporzioni.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Specifica le dimensioni dei dischi di dati in GB.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
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

### -DomainNameLabel
L'etichetta del nome di dominio per il nome di dominio pubblico Fully-Qualified (FQDN) per questo set di proporzioni. Questo è il primo componente del nome di dominio assegnato automaticamente al set di proporzioni. I nomi di dominio assegnati automaticamente usano il modulo ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Se non viene specificato alcun valore, l'etichetta del nome di dominio predefinito sarà la concatenazione di <ScaleSetName> e <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Nome del pool di indirizzi frontend da usare nel set di bilanciamento del carico di scala.  Se non viene specificato alcun valore, verrà creato un nuovo pool di indirizzi frontend con lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Nome dell'immagine per VM in questo set di proporzioni. Se non viene specificato alcun valore, verrà usata l'immagine "Windows Server 2016 datacenter".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Numero di immagini VM nel set di proporzioni.  Se non viene specificato alcun valore, verranno create 2 istanze.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Il nome del bilanciamento del carico da usare con questo set di proporzioni.  Se non viene specificato alcun valore, viene creato un nuovo gruppo di bilanciamento del carico che usa lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Posizione di Azure in cui verrà creato questo set di proporzioni.  Se non viene specificato alcun valore, la posizione verrà dedotta dalla posizione di altre risorse a cui si fa riferimento nei parametri.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Porta backend per la traduzione degli indirizzi di rete in ingresso.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Nome dell'indirizzo IP pubblico da usare con questo set di proporzioni.  Se non viene specificato alcun valore, verrà creato un nuovo IPAddress pubblico con lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse di VMSS.  Se non viene specificato alcun valore, verrà creato un nuovo ResourceGroup con lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
Il nome del gruppo di sicurezza di rete da applicare al set di proporzioni.  Se non viene specificato alcun valore, un gruppo di sicurezza di rete predefinito con lo stesso nome del set di proporzioni verrà creato e applicato al set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Usare questa opzione per creare il set di proporzioni in un singolo gruppo di posizionamento, il valore predefinito è più gruppi

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Il prefisso dell'indirizzo della subnet che verrà usato da questo Scalet. Le impostazioni di subnet predefinite (192.168.1.0/24) verranno applicate se non viene specificato alcun valore.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Nome della subnet da usare con questo set di proporzioni.  Verrà creata una nuova subnet con lo stesso nome del set di proporzioni se non viene specificato alcun valore.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Se il parametro è presente, le VM (s) nel set di proporzioni è (sono) assegnato un'identità di sistema gestita che viene generata automaticamente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Modalità di aggiornamento dei criteri per le istanze VM in questo set di proporzioni.  I criteri di aggiornamento possono specificare aggiornamenti automatici, manuali o a rotazione.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Nome dell'identità di un servizio gestito che deve essere assegnata alle VM nel set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica l'oggetto **VirtualMachineScaleSet** che contiene le proprietà della vmss creata da questo cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Nome della rete virtuale da usare con questo set di proporzioni.  Se non viene specificato alcun valore, verrà creata una nuova rete virtuale con lo stesso nome del set di proporzioni.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Specifica il nome della VMSS creata da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Dimensioni delle istanze VM in questo set di proporzioni.  Se non è specificata alcuna dimensione, verrà usata una dimensione predefinita (Standard_DS1_v2).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Prefisso dell'indirizzo per la rete virtuale usata con questo set di proporzioni.  Se non viene specificato alcun valore, verranno usate le impostazioni predefinite del prefisso dell'indirizzo di rete virtuale (192.168.0.0/16).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zona
Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet
Parametri: VirtualMachineScaleSet (ByValue)

### System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## OUTPUT

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Riavviare-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Stop-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


