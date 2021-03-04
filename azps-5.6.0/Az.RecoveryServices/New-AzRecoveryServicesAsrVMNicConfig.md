---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f28c1f8abf0da8363a860c9daffff9fc98a9a9d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953405"
---
# <span data-ttu-id="60c53-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="60c53-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="60c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c53-102">SYNOPSIS</span></span>
<span data-ttu-id="60c53-103">Crea una configurazione NIC ASR contenente i dettagli della configurazione correlata al failover e al failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="60c53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60c53-104">SYNTAX</span></span>

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

## <span data-ttu-id="60c53-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60c53-105">DESCRIPTION</span></span>
<span data-ttu-id="60c53-106">Il cmdlet **New-AzRecoveryServicesAsrVMNicConfig** crea un oggetto configurazione NIC ASR che contiene i dettagli correlati al failover e al failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="60c53-107">Nel caso in cui qualsiasi informazione non venga passata, i valori corrispondenti vengono selezionati dall'elemento protetto da replica per evitare che questi valori vengano aggiornati a Null.</span><span class="sxs-lookup"><span data-stu-id="60c53-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="60c53-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60c53-108">EXAMPLES</span></span>

### <span data-ttu-id="60c53-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60c53-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="60c53-110">Crea un oggetto ASRVmNicConfig con le impostazioni di rete di failover e test configurate per nic.</span><span class="sxs-lookup"><span data-stu-id="60c53-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="60c53-111">Qualsiasi proprietà non passata sopra viene recuperata dall'elemento protetto passato.</span><span class="sxs-lookup"><span data-stu-id="60c53-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="60c53-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="60c53-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="60c53-113">Crea un oggetto ASRVmNicConfig con le impostazioni di rete del faiover del test configurate per la ridenominazione NIC.</span><span class="sxs-lookup"><span data-stu-id="60c53-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="60c53-114">Qualsiasi proprietà non passata sopra viene recuperata dall'elemento protetto passato.</span><span class="sxs-lookup"><span data-stu-id="60c53-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="60c53-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="60c53-115">Example 3</span></span>

<span data-ttu-id="60c53-116">Crea una configurazione NIC ASR che contiene i dettagli della configurazione correlata al failover e al failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="60c53-117">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="60c53-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="60c53-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60c53-118">PARAMETERS</span></span>

### <span data-ttu-id="60c53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c53-119">-DefaultProfile</span></span>
<span data-ttu-id="60c53-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60c53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60c53-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="60c53-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="60c53-122">Specifica se la rete accelerata è abilitata al NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="60c53-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="60c53-124">Specifica se la rete accelerata è abilitata al nic di failover di test.</span><span class="sxs-lookup"><span data-stu-id="60c53-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="60c53-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="60c53-125">-NicId</span></span>
<span data-ttu-id="60c53-126">Specificare il GUID di NIC asr.</span><span class="sxs-lookup"><span data-stu-id="60c53-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="60c53-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="60c53-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="60c53-128">Specifica gli ID dei pool di indirizzi back-end per il nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="60c53-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="60c53-130">Specifica l'ID del gruppo di rete associato a NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="60c53-131">-RecoveryNicName</span></span>
<span data-ttu-id="60c53-132">Specifica il nome del nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c53-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="60c53-134">Specifica il nome del gruppo di risorse NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="60c53-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="60c53-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="60c53-136">Specifica l'indirizzo IP del nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="60c53-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="60c53-138">Specifica l'ID dell'indirizzo IP pubblico associato a NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="60c53-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="60c53-140">Specifica l'ID della rete virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="60c53-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="60c53-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="60c53-142">Specifica il nome della subnet di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="60c53-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="60c53-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="60c53-144">Specificare l'elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="60c53-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="60c53-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="60c53-145">-ReuseExistingNic</span></span>
<span data-ttu-id="60c53-146">Specifica se una NIC esistente può essere usata durante il failover.</span><span class="sxs-lookup"><span data-stu-id="60c53-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="60c53-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="60c53-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="60c53-148">Specifica gli ID dei pool di indirizzi back-end per il nic di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60c53-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="60c53-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="60c53-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="60c53-150">Specifica l'ID del gruppo di rete associato a NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="60c53-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="60c53-151">-TfoNicName</span></span>
<span data-ttu-id="60c53-152">Specifica il nome della NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="60c53-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c53-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="60c53-154">Specifica il nome del gruppo di risorse NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="60c53-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="60c53-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="60c53-156">Specifica l'indirizzo IP della NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="60c53-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="60c53-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="60c53-158">Specifica l'ID dell'indirizzo IP pubblico associato a NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="60c53-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="60c53-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="60c53-160">Specifica se una NIC esistente può essere usata durante il failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="60c53-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="60c53-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="60c53-162">Specifica l'ID della rete virtuale di failover dei test.</span><span class="sxs-lookup"><span data-stu-id="60c53-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="60c53-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="60c53-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="60c53-164">Specifica il nome della subnet di failover del test.</span><span class="sxs-lookup"><span data-stu-id="60c53-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="60c53-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60c53-165">-Confirm</span></span>
<span data-ttu-id="60c53-166">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c53-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c53-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c53-167">-WhatIf</span></span>
<span data-ttu-id="60c53-168">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60c53-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60c53-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60c53-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c53-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c53-170">CommonParameters</span></span>
<span data-ttu-id="60c53-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c53-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c53-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60c53-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c53-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="60c53-173">INPUTS</span></span>

### <span data-ttu-id="60c53-174">Nessuno</span><span class="sxs-lookup"><span data-stu-id="60c53-174">None</span></span>

## <span data-ttu-id="60c53-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60c53-175">OUTPUTS</span></span>

### <span data-ttu-id="60c53-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="60c53-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="60c53-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="60c53-177">NOTES</span></span>

## <span data-ttu-id="60c53-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60c53-178">RELATED LINKS</span></span>
