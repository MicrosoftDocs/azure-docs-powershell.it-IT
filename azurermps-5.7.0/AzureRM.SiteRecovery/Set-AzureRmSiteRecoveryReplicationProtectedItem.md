---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e09cc216b7ba3ef383467ea53478cfe8819e0a4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520339"
---
# <span data-ttu-id="d3eb3-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="d3eb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eb3-103">Imposta le proprietà di ripristino, ad esempio la rete di destinazione e la dimensione della macchina virtuale per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3eb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3eb3-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3eb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="d3eb3-106">Il cmdlet **set-AzureRmSiteRecoveryReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="d3eb3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3eb3-107">EXAMPLES</span></span>

## <span data-ttu-id="d3eb3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3eb3-108">PARAMETERS</span></span>

### <span data-ttu-id="d3eb3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eb3-109">-DefaultProfile</span></span>
<span data-ttu-id="d3eb3-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3eb3-111">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d3eb3-111">-LicenseType</span></span>
<span data-ttu-id="d3eb3-112">Specifica la selezione del tipo di licenza per le macchine virtuali di Windows Server migrate tramite vantaggi per l'uso ibrido.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-112">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

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

### <span data-ttu-id="d3eb3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3eb3-113">-Name</span></span>
<span data-ttu-id="d3eb3-114">Specifica il nome della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-114">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="d3eb3-115">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="d3eb3-115">-NicSelectionType</span></span>
<span data-ttu-id="d3eb3-116">Specifica le proprietà della scheda di rete (NIC, Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-116">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="d3eb3-117">Puoi specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-117">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="d3eb3-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="d3eb3-118">-PrimaryNic</span></span>
<span data-ttu-id="d3eb3-119">Specifica la scheda NIC della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-119">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="d3eb3-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="d3eb3-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="d3eb3-121">Specifica l'ID della rete virtuale di Azure per cui questo cmdlet ripristina l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-121">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="d3eb3-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3eb3-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="d3eb3-123">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda NIC primaria al ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-123">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="d3eb3-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="d3eb3-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="d3eb3-125">Specifica il nome della subnet nella rete virtuale di Azure di ripristino per cui questo cmdlet recupera l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-125">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="d3eb3-126">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-126">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d3eb3-127">Specifica l'elemento protetto della replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-127">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3eb3-128">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="d3eb3-128">-Size</span></span>
<span data-ttu-id="d3eb3-129">Specifica la dimensione della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-129">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="d3eb3-130">Il valore deve essere del set di dimensioni supportate da macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-130">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="d3eb3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eb3-131">CommonParameters</span></span>
<span data-ttu-id="d3eb3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3eb3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eb3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3eb3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eb3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3eb3-134">INPUTS</span></span>

### <span data-ttu-id="d3eb3-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="d3eb3-136">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d3eb3-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="d3eb3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3eb3-137">OUTPUTS</span></span>

### <span data-ttu-id="d3eb3-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d3eb3-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d3eb3-139">Note</span><span class="sxs-lookup"><span data-stu-id="d3eb3-139">NOTES</span></span>

## <span data-ttu-id="d3eb3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3eb3-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3eb3-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d3eb3-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d3eb3-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d3eb3-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
