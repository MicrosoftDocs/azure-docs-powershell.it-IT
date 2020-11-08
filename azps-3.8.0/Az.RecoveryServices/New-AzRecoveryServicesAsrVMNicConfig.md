---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020644"
---
# <span data-ttu-id="9a66b-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="9a66b-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="9a66b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a66b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a66b-103">Crea una configurazione di NIC ASR che contiene i dettagli di failover e test correlati al failover.</span><span class="sxs-lookup"><span data-stu-id="9a66b-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="9a66b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a66b-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a66b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a66b-105">DESCRIPTION</span></span>
<span data-ttu-id="9a66b-106">Il cmdlet **New-AzRecoveryServicesAsrVMNicConfig** crea un oggetto config di tipo NIC ASR che contiene i dettagli relativi al failover e al test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="9a66b-107">Nel caso in cui le informazioni non vengano passate, i valori corrispondenti vengono selezionati dall'elemento protetto da replica per evitare che questi valori vengano aggiornati a null.</span><span class="sxs-lookup"><span data-stu-id="9a66b-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="9a66b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a66b-108">EXAMPLES</span></span>

### <span data-ttu-id="9a66b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a66b-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="9a66b-110">Crea un oggetto ASRVmNicConfig con le impostazioni di rete per il failover e il test faiover configurate per la scheda NIC.</span><span class="sxs-lookup"><span data-stu-id="9a66b-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="9a66b-111">Tutte le proprietà non passate vengono recuperate dall'elemento protetto passato.</span><span class="sxs-lookup"><span data-stu-id="9a66b-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="9a66b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a66b-112">PARAMETERS</span></span>

### <span data-ttu-id="9a66b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a66b-113">-DefaultProfile</span></span>
<span data-ttu-id="9a66b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a66b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a66b-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="9a66b-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="9a66b-116">Specifica se la rete accelerata è abilitata nella scheda di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="9a66b-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="9a66b-118">Specifica se la rete accelerata è abilitata nella scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="9a66b-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="9a66b-119">-NicId</span></span>
<span data-ttu-id="9a66b-120">Specificare il GUID NIC ASR.</span><span class="sxs-lookup"><span data-stu-id="9a66b-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="9a66b-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a66b-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="9a66b-122">Specifica gli ID dei pool di indirizzi backend per la NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9a66b-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="9a66b-124">Specifica l'ID della NSG associata alla scheda di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a66b-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="9a66b-126">Specifica l'indirizzo IP della NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9a66b-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="9a66b-128">Specifica l'ID dell'indirizzo IP pubblico associato alla scheda NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9a66b-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="9a66b-130">Specifica l'ID della rete virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="9a66b-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="9a66b-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="9a66b-132">Specifica il nome della subnet di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="9a66b-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a66b-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9a66b-134">Specificare l'elemento protetto per la replica ASR.</span><span class="sxs-lookup"><span data-stu-id="9a66b-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="9a66b-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a66b-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="9a66b-136">Specifica gli ID dei pool di indirizzi backend per la NIC di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9a66b-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="9a66b-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9a66b-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="9a66b-138">Specifica l'ID del NSG associato alla scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="9a66b-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a66b-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="9a66b-140">Specifica l'indirizzo IP della NIC di failover del test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="9a66b-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="9a66b-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="9a66b-142">Specifica l'ID dell'indirizzo IP pubblico associato alla scheda di failover di test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="9a66b-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9a66b-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="9a66b-144">Specifica l'ID della rete virtuale di failover di test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="9a66b-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="9a66b-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="9a66b-146">Specifica il nome della subnet di failover test.</span><span class="sxs-lookup"><span data-stu-id="9a66b-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="9a66b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a66b-147">CommonParameters</span></span>
<span data-ttu-id="9a66b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a66b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a66b-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a66b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a66b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a66b-150">INPUTS</span></span>

### <span data-ttu-id="9a66b-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9a66b-151">None</span></span>

## <span data-ttu-id="9a66b-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a66b-152">OUTPUTS</span></span>

### <span data-ttu-id="9a66b-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="9a66b-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="9a66b-154">Note</span><span class="sxs-lookup"><span data-stu-id="9a66b-154">NOTES</span></span>

## <span data-ttu-id="9a66b-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a66b-155">RELATED LINKS</span></span>
