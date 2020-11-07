---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687115"
---
# <span data-ttu-id="4be29-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4be29-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="4be29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4be29-102">SYNOPSIS</span></span>
<span data-ttu-id="4be29-103">Imposta le proprietà di ripristino, ad esempio la rete di destinazione e la dimensione della macchina virtuale per l'elemento protetto della replica specificato.</span><span class="sxs-lookup"><span data-stu-id="4be29-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4be29-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be29-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4be29-105">DESCRIPTION</span></span>
<span data-ttu-id="4be29-106">Il cmdlet **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="4be29-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="4be29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4be29-107">EXAMPLES</span></span>

### <span data-ttu-id="4be29-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4be29-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="4be29-109">Avvia l'operazione di aggiornamento della protezione della replica delle impostazioni degli elementi con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4be29-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4be29-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4be29-110">PARAMETERS</span></span>

### <span data-ttu-id="4be29-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be29-111">-InputObject</span></span>
<span data-ttu-id="4be29-112">Oggetto di input per il cmdlet: oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto da replica per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4be29-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4be29-113">-LicenseType</span></span>
<span data-ttu-id="4be29-114">Specificare la selezione del tipo di licenza da usare per le macchine virtuali di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4be29-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="4be29-115">Se si ha diritto all'uso di Azure Hybrid use benefit (HUB) per le migrazioni e si vuole specificare che l'impostazione HUB venga usata durante il superamento di questo elemento protetto, impostare il tipo di licenza su WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="4be29-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4be29-116">-Name</span></span>
<span data-ttu-id="4be29-117">Specifica il nome della macchina virtuale di ripristino che verrà creata in failover.</span><span class="sxs-lookup"><span data-stu-id="4be29-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="4be29-118">-NicSelectionType</span></span>
<span data-ttu-id="4be29-119">Specifica le proprietà della scheda di rete (NIC, Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4be29-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="4be29-120">Puoi specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4be29-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="4be29-121">-PrimaryNic</span></span>
<span data-ttu-id="4be29-122">Specifica la scheda NIC della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4be29-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="4be29-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="4be29-124">Specifica l'ID della rete virtuale di Azure a cui deve essere fallito l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="4be29-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="4be29-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="4be29-126">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda NIC primaria al ripristino.</span><span class="sxs-lookup"><span data-stu-id="4be29-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="4be29-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="4be29-128">Specifica il nome della subnet nella rete virtuale di Azure di ripristino a cui deve essere connessa questa NIC dell'elemento protetto per il failover.</span><span class="sxs-lookup"><span data-stu-id="4be29-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4be29-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="4be29-130">ID del gruppo di risorse Azure nell'area di ripristino in cui verrà recuperato l'elemento protetto in failover.</span><span class="sxs-lookup"><span data-stu-id="4be29-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-131">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="4be29-131">-Size</span></span>
<span data-ttu-id="4be29-132">Specifica la dimensione della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4be29-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="4be29-133">Il valore deve essere del set di dimensioni supportate da macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="4be29-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be29-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4be29-134">-Confirm</span></span>
<span data-ttu-id="4be29-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4be29-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be29-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be29-136">-WhatIf</span></span>
<span data-ttu-id="4be29-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4be29-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4be29-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4be29-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be29-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be29-139">CommonParameters</span></span>
<span data-ttu-id="4be29-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be29-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be29-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be29-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be29-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4be29-142">INPUTS</span></span>

### <span data-ttu-id="4be29-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4be29-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4be29-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4be29-144">OUTPUTS</span></span>

### <span data-ttu-id="4be29-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4be29-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4be29-146">Note</span><span class="sxs-lookup"><span data-stu-id="4be29-146">NOTES</span></span>

## <span data-ttu-id="4be29-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4be29-147">RELATED LINKS</span></span>

[<span data-ttu-id="4be29-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4be29-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4be29-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4be29-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4be29-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4be29-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
