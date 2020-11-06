---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511544"
---
# <span data-ttu-id="1460c-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1460c-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="1460c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1460c-102">SYNOPSIS</span></span>
<span data-ttu-id="1460c-103">Imposta le proprietà di ripristino, ad esempio la rete di destinazione e la dimensione della macchina virtuale per l'elemento protetto della replica specificato.</span><span class="sxs-lookup"><span data-stu-id="1460c-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1460c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1460c-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1460c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1460c-105">DESCRIPTION</span></span>
<span data-ttu-id="1460c-106">Il cmdlet **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="1460c-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="1460c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1460c-107">EXAMPLES</span></span>

### <span data-ttu-id="1460c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1460c-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="1460c-109">Avvia l'operazione di aggiornamento della protezione della replica delle impostazioni degli elementi con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1460c-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1460c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1460c-110">PARAMETERS</span></span>

### <span data-ttu-id="1460c-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="1460c-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="1460c-112">Specifica l'aggiornamento della reliquia configurazione.</span><span class="sxs-lookup"><span data-stu-id="1460c-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1460c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1460c-113">-DefaultProfile</span></span>
<span data-ttu-id="1460c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1460c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1460c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1460c-115">-InputObject</span></span>
<span data-ttu-id="1460c-116">Oggetto di input per il cmdlet: oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto da replica per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1460c-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1460c-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1460c-117">-LicenseType</span></span>
<span data-ttu-id="1460c-118">Specificare la selezione del tipo di licenza da usare per le macchine virtuali di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="1460c-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="1460c-119">Se si ha diritto all'uso di Azure Hybrid use benefit (HUB) per le migrazioni e si vuole specificare che l'impostazione HUB venga usata durante il superamento di questo elemento protetto, impostare il tipo di licenza su WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="1460c-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1460c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1460c-120">-Name</span></span>
<span data-ttu-id="1460c-121">Specifica il nome della macchina virtuale di ripristino che verrà creata in failover.</span><span class="sxs-lookup"><span data-stu-id="1460c-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="1460c-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="1460c-122">-NicSelectionType</span></span>
<span data-ttu-id="1460c-123">Specifica le proprietà della scheda di rete (NIC, Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1460c-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="1460c-124">Puoi specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="1460c-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1460c-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="1460c-125">-PrimaryNic</span></span>
<span data-ttu-id="1460c-126">Specifica la scheda NIC della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1460c-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="1460c-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1460c-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="1460c-128">Set di disponibilità per l'elemento protetto da replica dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="1460c-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="1460c-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1460c-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="1460c-130">Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="1460c-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="1460c-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="1460c-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="1460c-132">ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1460c-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="1460c-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="1460c-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="1460c-134">Specifica l'ID della rete virtuale di Azure a cui deve essere fallito l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="1460c-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="1460c-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1460c-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1460c-136">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda NIC primaria al ripristino.</span><span class="sxs-lookup"><span data-stu-id="1460c-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="1460c-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="1460c-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="1460c-138">Specifica il nome della subnet nella rete virtuale di Azure di ripristino a cui deve essere connessa questa NIC dell'elemento protetto per il failover.</span><span class="sxs-lookup"><span data-stu-id="1460c-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="1460c-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="1460c-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="1460c-140">ID del gruppo di risorse Azure nell'area di ripristino in cui verrà recuperato l'elemento protetto in failover.</span><span class="sxs-lookup"><span data-stu-id="1460c-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="1460c-141">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="1460c-141">-Size</span></span>
<span data-ttu-id="1460c-142">Specifica la dimensione della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1460c-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="1460c-143">Il valore deve essere del set di dimensioni supportate da macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="1460c-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="1460c-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1460c-144">-UseManagedDisk</span></span>
<span data-ttu-id="1460c-145">Specifica se la macchina virtuale di Azure creata in failover deve usare i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="1460c-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1460c-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1460c-146">-Confirm</span></span>
<span data-ttu-id="1460c-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1460c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1460c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1460c-148">-WhatIf</span></span>
<span data-ttu-id="1460c-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1460c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1460c-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1460c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1460c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1460c-151">CommonParameters</span></span>
<span data-ttu-id="1460c-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1460c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1460c-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1460c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1460c-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1460c-154">INPUTS</span></span>

### <span data-ttu-id="1460c-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1460c-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1460c-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1460c-156">OUTPUTS</span></span>

### <span data-ttu-id="1460c-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1460c-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1460c-158">Note</span><span class="sxs-lookup"><span data-stu-id="1460c-158">NOTES</span></span>

## <span data-ttu-id="1460c-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1460c-159">RELATED LINKS</span></span>

[<span data-ttu-id="1460c-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1460c-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1460c-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1460c-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1460c-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1460c-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)