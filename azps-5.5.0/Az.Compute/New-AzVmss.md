---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177654"
---
# New-AzVmss

## SYNOPSIS
Crea un VMSS.

## SINTASSI

### DefaultParameter (Default)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVmss crea** un set di scalabilità delle macchine virtuali (VMSS) in Azure.
Usare il set di parametri semplice ( ) per `SimpleParameterSet` creare rapidamente un VMSS pre-impostato e risorse associate. Usare il set di parametri predefinito ( ) per scenari più avanzati quando è necessario configurare con precisione ogni componente del sistema VMSS e ogni risorsa associata `DefaultParameter` prima della creazione.

## ESEMPI

### Esempio 1: creare un VMSS usando il **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Il comando precedente crea quanto segue con il `$vmssName` nome:
* Gruppo di risorse
* Una rete virtuale
* Servizio di bilanciamento del carico
* Un indirizzo IP pubblico
* VMSS con 2 istanze

L'immagine predefinita scelta per le macchine virtuali nel sistema VMSS è `2016-Datacenter Windows Server` e lo SKU è `Standard_DS1_v2`

### Esempio 2: crea un VMSS utilizzando il **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

Nell'esempio complesso riportato sopra viene creato un VMSS, di seguito è riportata una spiegazione di quello che accade:
* Il primo comando crea un gruppo di risorse con il nome e il percorso specificati.
* Il secondo comando usa il cmdlet **New-AzStorageAccount** per creare un account di archiviazione.
* Il terzo comando usa quindi il cmdlet **Get-AzStorageAccount** per ottenere l'account di archiviazione creato nel secondo comando e archivia il risultato nella $STOAccount variabile.
* Il quinto comando usa il cmdlet **New-AzVirtualNetworkSubnetConfig** per creare una subnet e archivia il risultato nella variabile $SubNet.
* Il sesto comando usa il cmdlet **New-AzVirtualNetwork** per creare una rete virtuale e archivia il risultato nella variabile $VNet.
* Il settimo comando usa **Get-AzVirtualNetwork** per ottenere informazioni sulla rete virtuale creata nel sesto comando e le archivia nella variabile $VNet.
* L'ottavo e il nono comando usa **New-AzPublicIpAddress** e **Get- AzureRmPublicIpAddress** per creare e ottenere informazioni da tale indirizzo IP pubblico.
* I comandi archiviano le informazioni nella variabile denominata $PubIP.
* Il decimo comando usa il cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** per creare una bilanciamento del carico frontend e archivia il risultato nella variabile $Frontend.
* L'undicesimo comando usa **New-AzLoadBalancerBackendAddressPoolConfig** per creare una configurazione del pool di indirizzi back-end e archivia il risultato nella variabile $BackendAddressPool.
* Il dodicesimo comando usa **New-AzLoadBalancerProbeConfig** per creare un'e-$Probe.
* Il tredicesimo comando usa il cmdlet **New-AzLoadBalancerInboundNatPoolConfig per** creare una configurazione di pool NAT (Network Address Translation) in ingresso di bilanciamento del carico.
* Il quattordicesimo comando usa **New-AzLoadBalancerRuleConfig** per creare una configurazione di regola di bilanciamento del carico e archivia il risultato nella variabile $LBRule.
* Il quindicesimo comando usa il cmdlet **New-AzLoadBalancer** per creare una bilanciamento del carico e archivia il risultato nella variabile $ActualLb.
* Il sediciesimo comando usa **Get-AzLoadBalancer** per ottenere informazioni sulla bilanciamento del carico creata nel quindicesimo comando e archivia le informazioni nella variabile $ExpectedLb.
* Il diciassettesesimo comando usa il cmdlet **New-AzVmssIPConfig** per creare una configurazione IP VMSS e archivia le informazioni nella variabile denominata $IPCfg.
* Il diciottesimo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione VMSS e archivia il risultato nella variabile $VMSS.
* Il comando #D0 /c0 #D1 usa il cmdlet **New-AzVmss** per creare VMSS.

## PARAMETERS

### -AllocationMethod
Metodo di allocazione per l'indirizzo IP pubblico del set di scale (statico o dinamico).  Se non viene fornito alcun valore, l'allocazione sarà statica.

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
Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.

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
Nome del pool di indirizzi back-end da usare nella bilanciamento del carico per questo set di scale.  Se non viene fornito alcun valore, verrà creato un nuovo pool back-end con lo stesso nome del set di scale.

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
Numeri di porta back-end usati dalla bilanciamenta del carico set di scala per comunicare con le macchine virtuali nel set di scale.  Se non si specifica alcun valore, verranno usate le porte 3389 e 5985 per Windows VMS e la porta 22 per le macchine virtuali Linux.

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

### -Credential
Credenziali di amministratore (nome utente e password) per le macchine virtuali in questo set di scale.

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
Specifica le dimensioni dei dischi dati in GB.

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

### -DomainNameLabel
Etichetta del nome di dominio per il nome Fully-Qualified di dominio (FQDN) per questo set di scale. Primo componente del nome di dominio assegnato automaticamente al set di scale. I nomi di dominio assegnati automaticamente usano il formato ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Se non viene fornito alcun valore, l'etichetta predefinita del nome di dominio sarà la concatenazione di <ScaleSetName> e <ResourceGroupName> .

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

### -EnableUltrasSD
Usare dischi UltraSSD per le macchine virtuali nel set di scale.

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

### -EncryptionAtHost
Questo parametro abiliterà la crittografia per tutti i dischi, incluso il disco Risorsa/Temp nell'host stesso. Impostazione predefinita: la crittografia nell'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.

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

### -EvictionPolicy
Criterio di sgomento per il set di scala delle macchine virtuali con priorità bassa.  Solo i valori supportati sono "Deassegnazione" ed "Elimina".

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
Nome del pool di indirizzi frontend da usare nella bilanciamento del carico set di scale.  Se non viene fornito alcun valore, verrà creato un nuovo pool di indirizzi Frontend con lo stesso nome del set di scale.

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

### -HostGroupId
Specifica il gruppo host dedicato in cui risiede il set di scalabilità della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ImageName
Nome dell'immagine per le macchine virtuali in questo set di scale. Se non viene fornito alcun valore, verrà usata l'immagine "Windows Server 2016 DataCenter".

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
Il numero di immagini della macchina virtuale nel set di scale.  Se non viene fornito alcun valore, verranno create 2 istanze.

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
Nome della bilanciamento del carico da usare con questo set di scale.  Se non si imposta alcun valore, verrà creata una nuova bilanciamento del carico con lo stesso nome del set di scale.

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

### -Location
Posizione di Azure in cui verrà creato il set di scale.  Se non si specifica alcun valore, la posizione verrà dedotto dalla posizione delle altre risorse a cui si fa riferimento nei parametri.

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

### -MaxPrice
Prezzo massimo per la fatturazione di un set di scale per le macchine virtuali con priorità bassa.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Porta back-end per la traduzione degli indirizzi di rete in ingresso.

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

### -PlatformFaultDomainCount
Fault Domain count for each placement group.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Priorità della macchina virtuale nel set di scale.  Solo i valori supportati sono "Normale", "Posizione" e "Basso".
"Normale" è per la macchina virtuale normale.
"Spot" è per una macchina virtuale spot.
"Low" è anche per la macchina virtuale spot, ma viene sostituito da "Spot". Usare "Spot" invece di "Low".

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

### -ProximityPlacementGroupId
ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di scale.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Nome dell'indirizzo IP pubblico da usare con questo set di scalabilità.  Se non viene fornito alcun valore, verrà creato un nuovo IPAddress pubblico con lo stesso nome del set di scale.

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
Specifica il nome del gruppo di risorse del sistema VMSS.  Se non viene specificato alcun valore, verrà creato un nuovo Gruppo di risorse con lo stesso nome del set di scale.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Regole da seguire quando si ridimensiona un set di scalabilità delle macchine virtuali.  I valori possibili sono " Default", "OldestVM" e "NewestVM".  "Impostazione predefinita" quando un set di scalabilità delle macchine virtuali viene ridimensionato, viene prima bilanciato tra le aree, se si tratta di un set di scala di zona.  Quindi, verrà bilanciato il più possibile tra i domini di errore.  All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno le più recenti non protette dalla scalabilità.  Quando il set di scale di una macchina virtuale viene ridimensionato, per la rimozione vengono scelte le macchine virtuali meno recenti che non sono protette dal scale-in.  Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.  All'interno di ogni area vengono scelte le macchine virtuali meno recenti non protette per la rimozione.  Nel caso di un set di scale per macchine virtuali in fase di ridimensionamento, per la rimozione verranno scelte le macchine virtuali più recenti non protette dal scale-in.  Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.  All'interno di ogni area vengono scelte le macchine virtuali più recenti non protette per la rimozione.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Nome del gruppo di sicurezza di rete da applicare a questo set di scale.  Se non viene fornito alcun valore, verrà creato e applicato al set di scale un gruppo di sicurezza di rete predefinito con lo stesso nome del set di scale.

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
Usare questa opzione per creare il set di scale in un singolo gruppo di posizionamento, il valore predefinito è più gruppi

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

### -SkipExtensionsOnOverprovisionedVMs
Specifica che le estensioni non vengono eseguite nelle macchine virtuali con overprovisioning aggiuntivo.

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
Prefisso dell'indirizzo della subnet che verrà utilizzata da questo ScaleSet. Le impostazioni predefinite della subnet (192.168.1.0/24) verranno applicate se non viene fornito alcun valore.

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
Nome della subnet da usare con questo set di scale.  Se non viene specificato alcun valore, verrà creata una nuova subnet con lo stesso nome del set di scale.

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
Se il parametro è presente, alle macchine virtuali nel set di scalabilità viene (o sono) assegnate un'identità di sistema gestita generata automaticamente.

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
Modalità dei criteri di aggiornamento per le istanze di VM in questo set di scale.  I criteri di aggiornamento possono specificare aggiornamenti automatici, manuali o in sequenza.

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
Nome di un'identità del servizio gestito che deve essere assegnata alle macchine virtuali nel set di scale.

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
Specifica **l'oggetto VirtualMachineScaleSet** che contiene le proprietà del sistema VMSS creato da questo cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Il nome della rete virtuale da usare con questo set di scale.  Se non viene fornito alcun valore, verrà creata una nuova rete virtuale con lo stesso nome del set di scale.

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
Specifica il nome del sistema VMS creato da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Le dimensioni delle istanze della macchina virtuale in questo set di scale.  Se non si Standard_DS1_v2 Size, verrà usata una dimensione predefinita (Standard_DS1_v2).

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
Prefisso dell'indirizzo della rete virtuale usata con questo set di scale.  Le impostazioni predefinite per i prefissi degli indirizzi di rete virtuale (192.168.0.0/16) verranno usate se non viene fornito alcun valore.

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

### -Zone
Elenco di aree di disponibilità che denota l'indirizzo IP allocato per la risorsa.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUT

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


