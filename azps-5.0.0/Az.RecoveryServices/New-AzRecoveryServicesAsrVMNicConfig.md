---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200504"
---
# <span data-ttu-id="affca-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="affca-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="affca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="affca-102">SYNOPSIS</span></span>
<span data-ttu-id="affca-103">Crea una configurazione di NIC ASR che contiene i dettagli di failover e test correlati al failover.</span><span class="sxs-lookup"><span data-stu-id="affca-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="affca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="affca-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="affca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="affca-105">DESCRIPTION</span></span>
<span data-ttu-id="affca-106">Il cmdlet **New-AzRecoveryServicesAsrVMNicConfig** crea un oggetto config di tipo NIC ASR che contiene i dettagli relativi al failover e al test.</span><span class="sxs-lookup"><span data-stu-id="affca-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="affca-107">Nel caso in cui le informazioni non vengano passate, i valori corrispondenti vengono selezionati dall'elemento protetto da replica per evitare che questi valori vengano aggiornati a null.</span><span class="sxs-lookup"><span data-stu-id="affca-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="affca-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="affca-108">EXAMPLES</span></span>

### <span data-ttu-id="affca-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="affca-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="affca-110">Crea un oggetto ASRVmNicConfig con le impostazioni di rete per il failover e il test faiover configurate per la scheda NIC.</span><span class="sxs-lookup"><span data-stu-id="affca-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="affca-111">Tutte le proprietà non passate vengono recuperate dall'elemento protetto passato.</span><span class="sxs-lookup"><span data-stu-id="affca-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="affca-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="affca-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="affca-113">Crea un oggetto ASRVmNicConfig con le impostazioni di rete di test faiover configurate per la ridenominazione della scheda NIC.</span><span class="sxs-lookup"><span data-stu-id="affca-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="affca-114">Tutte le proprietà non passate vengono recuperate dall'elemento protetto passato.</span><span class="sxs-lookup"><span data-stu-id="affca-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="affca-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="affca-115">Example 3</span></span>

<span data-ttu-id="affca-116">Crea una configurazione di NIC ASR che contiene i dettagli di failover e test correlati al failover.</span><span class="sxs-lookup"><span data-stu-id="affca-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="affca-117">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="affca-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="affca-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="affca-118">PARAMETERS</span></span>

### <span data-ttu-id="affca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affca-119">-DefaultProfile</span></span>
<span data-ttu-id="affca-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="affca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="affca-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="affca-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="affca-122">Specifica se la rete accelerata è abilitata nella scheda di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="affca-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="affca-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="affca-124">Specifica se la rete accelerata è abilitata nella scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="affca-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="affca-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="affca-125">-NicId</span></span>
<span data-ttu-id="affca-126">Specificare il GUID NIC ASR.</span><span class="sxs-lookup"><span data-stu-id="affca-126">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affca-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="affca-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="affca-128">Specifica gli ID dei pool di indirizzi backend per la NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affca-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="affca-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="affca-130">Specifica l'ID della NSG associata alla scheda di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="affca-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="affca-131">-RecoveryNicName</span></span>
<span data-ttu-id="affca-132">Specifica il nome della NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="affca-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affca-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="affca-134">Specifica il nome del gruppo di risorse NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="affca-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="affca-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="affca-136">Specifica l'indirizzo IP della NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="affca-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="affca-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="affca-138">Specifica l'ID dell'indirizzo IP pubblico associato alla scheda NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="affca-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="affca-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="affca-140">Specifica l'ID della rete virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="affca-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="affca-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="affca-142">Specifica il nome della subnet di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="affca-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="affca-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="affca-144">Specificare l'elemento protetto per la replica ASR.</span><span class="sxs-lookup"><span data-stu-id="affca-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affca-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="affca-145">-ReuseExistingNic</span></span>
<span data-ttu-id="affca-146">Specifica se una scheda NIC esistente può essere usata durante il failover.</span><span class="sxs-lookup"><span data-stu-id="affca-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="affca-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="affca-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="affca-148">Specifica gli ID dei pool di indirizzi backend per la NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="affca-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affca-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="affca-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="affca-150">Specifica l'ID del NSG associato alla scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="affca-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="affca-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="affca-151">-TfoNicName</span></span>
<span data-ttu-id="affca-152">Specifica il nome della NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="affca-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="affca-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affca-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="affca-154">Specifica il nome del gruppo di risorse del NIC di failover di test.</span><span class="sxs-lookup"><span data-stu-id="affca-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="affca-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="affca-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="affca-156">Specifica l'indirizzo IP della NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="affca-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="affca-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="affca-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="affca-158">Specifica l'ID dell'indirizzo IP pubblico associato alla scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="affca-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="affca-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="affca-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="affca-160">Specifica se una scheda NIC esistente può essere usata durante il failover del test.</span><span class="sxs-lookup"><span data-stu-id="affca-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="affca-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="affca-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="affca-162">Specifica l'ID della rete virtuale di failover di test.</span><span class="sxs-lookup"><span data-stu-id="affca-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="affca-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="affca-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="affca-164">Specifica il nome della subnet di failover test.</span><span class="sxs-lookup"><span data-stu-id="affca-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="affca-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="affca-165">-Confirm</span></span>
<span data-ttu-id="affca-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="affca-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="affca-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="affca-167">-WhatIf</span></span>
<span data-ttu-id="affca-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="affca-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="affca-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="affca-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="affca-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affca-170">CommonParameters</span></span>
<span data-ttu-id="affca-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affca-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affca-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="affca-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affca-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="affca-173">INPUTS</span></span>

### <span data-ttu-id="affca-174">Nessuno</span><span class="sxs-lookup"><span data-stu-id="affca-174">None</span></span>

## <span data-ttu-id="affca-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="affca-175">OUTPUTS</span></span>

### <span data-ttu-id="affca-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="affca-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="affca-177">Note</span><span class="sxs-lookup"><span data-stu-id="affca-177">NOTES</span></span>

## <span data-ttu-id="affca-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="affca-178">RELATED LINKS</span></span>
