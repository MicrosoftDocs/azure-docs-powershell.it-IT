---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512892"
---
# <span data-ttu-id="26fb1-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="26fb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="26fb1-103">Imposta le proprietà di ripristino, ad esempio la rete di destinazione e la dimensione della macchina virtuale per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="26fb1-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26fb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26fb1-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26fb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="26fb1-106">Il cmdlet **set-AzureRmSiteRecoveryReplicationProtectedItem** imposta le proprietà di ripristino per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="26fb1-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="26fb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26fb1-107">EXAMPLES</span></span>

## <span data-ttu-id="26fb1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26fb1-108">PARAMETERS</span></span>

### <span data-ttu-id="26fb1-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="26fb1-109">-LicenseType</span></span>
<span data-ttu-id="26fb1-110">Specifica la selezione del tipo di licenza per le macchine virtuali di Windows Server migrate tramite vantaggi per l'uso ibrido.</span><span class="sxs-lookup"><span data-stu-id="26fb1-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

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

### <span data-ttu-id="26fb1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="26fb1-111">-Name</span></span>
<span data-ttu-id="26fb1-112">Specifica il nome della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26fb1-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="26fb1-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="26fb1-113">-NicSelectionType</span></span>
<span data-ttu-id="26fb1-114">Specifica le proprietà della scheda di rete (NIC, Network Interface Card) impostate dall'utente o impostate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26fb1-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="26fb1-115">Puoi specificare NotSelected per tornare ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="26fb1-115">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="26fb1-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="26fb1-116">-PrimaryNic</span></span>
<span data-ttu-id="26fb1-117">Specifica la scheda NIC della macchina virtuale per cui questo cmdlet imposta la proprietà di rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26fb1-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="26fb1-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="26fb1-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="26fb1-119">Specifica l'ID della rete virtuale di Azure per cui questo cmdlet ripristina l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="26fb1-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="26fb1-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="26fb1-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="26fb1-121">Specifica l'indirizzo IP statico che deve essere assegnato alla scheda NIC primaria al ripristino.</span><span class="sxs-lookup"><span data-stu-id="26fb1-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="26fb1-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="26fb1-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="26fb1-123">Specifica il nome della subnet nella rete virtuale di Azure di ripristino per cui questo cmdlet recupera l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="26fb1-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="26fb1-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26fb1-125">Specifica l'elemento protetto della replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="26fb1-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26fb1-126">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="26fb1-126">-Size</span></span>
<span data-ttu-id="26fb1-127">Specifica la dimensione della macchina virtuale di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26fb1-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="26fb1-128">Il valore deve essere del set di dimensioni supportate da macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="26fb1-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="26fb1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fb1-129">-DefaultProfile</span></span>
<span data-ttu-id="26fb1-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26fb1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26fb1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fb1-131">CommonParameters</span></span>
<span data-ttu-id="26fb1-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fb1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fb1-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26fb1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fb1-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26fb1-134">INPUTS</span></span>

### <span data-ttu-id="26fb1-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="26fb1-136">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="26fb1-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="26fb1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26fb1-137">OUTPUTS</span></span>

### <span data-ttu-id="26fb1-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="26fb1-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26fb1-139">Note</span><span class="sxs-lookup"><span data-stu-id="26fb1-139">NOTES</span></span>

## <span data-ttu-id="26fb1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26fb1-140">RELATED LINKS</span></span>

[<span data-ttu-id="26fb1-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="26fb1-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="26fb1-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26fb1-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
