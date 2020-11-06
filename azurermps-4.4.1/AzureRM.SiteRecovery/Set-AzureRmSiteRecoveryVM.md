---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519500"
---
# <span data-ttu-id="a610d-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a610d-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="a610d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a610d-102">SYNOPSIS</span></span>
<span data-ttu-id="a610d-103">Imposta le opzioni sul lato ripristino per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="a610d-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a610d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a610d-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a610d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a610d-105">DESCRIPTION</span></span>
<span data-ttu-id="a610d-106">Il cmdlet **set-AzureRmSiteRecoveryVM** imposta le opzioni di protezione sul lato del ripristino, ad esempio la dimensione della macchina virtuale di ripristino e la rete Virtual Machine di ripristino, per le entità di protezione del ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="a610d-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="a610d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a610d-107">EXAMPLES</span></span>

## <span data-ttu-id="a610d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a610d-108">PARAMETERS</span></span>

### <span data-ttu-id="a610d-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="a610d-109">-Name</span></span>
<span data-ttu-id="a610d-110">Specifica il nome della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a610d-110">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="a610d-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="a610d-111">-NicSelectionType</span></span>
<span data-ttu-id="a610d-112">Specifica le proprietà di selezione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="a610d-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="a610d-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a610d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a610d-114">NotSelected</span><span class="sxs-lookup"><span data-stu-id="a610d-114">NotSelected</span></span>
- <span data-ttu-id="a610d-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="a610d-115">SelectedByUser</span></span>

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

### <span data-ttu-id="a610d-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="a610d-116">-PrimaryNic</span></span>
<span data-ttu-id="a610d-117">Specifica la scheda di rete principale.</span><span class="sxs-lookup"><span data-stu-id="a610d-117">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="a610d-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="a610d-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="a610d-119">Specifica l'ID della rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a610d-119">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="a610d-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a610d-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a610d-121">Specifica l'indirizzo IP statico assegnato al controller della scheda di rete principale durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="a610d-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="a610d-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="a610d-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="a610d-123">Specifica il nome della subnet di Azure Virtual Network con cui allegare il controller della scheda di rete principale al ripristino.</span><span class="sxs-lookup"><span data-stu-id="a610d-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="a610d-124">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="a610d-124">-Size</span></span>
<span data-ttu-id="a610d-125">Specifica la dimensione della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a610d-125">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="a610d-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a610d-126">-VirtualMachine</span></span>
<span data-ttu-id="a610d-127">Specifica l'oggetto macchina virtuale ripristino sito.</span><span class="sxs-lookup"><span data-stu-id="a610d-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a610d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a610d-128">-DefaultProfile</span></span>
<span data-ttu-id="a610d-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a610d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a610d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a610d-130">CommonParameters</span></span>
<span data-ttu-id="a610d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a610d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a610d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a610d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a610d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a610d-133">INPUTS</span></span>

### <span data-ttu-id="a610d-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a610d-134">ASRVirtualMachine</span></span>
<span data-ttu-id="a610d-135">Il parametro ' VirtualMachine ' accetta il valore di tipo ' ASRVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a610d-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="a610d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a610d-136">OUTPUTS</span></span>

### <span data-ttu-id="a610d-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a610d-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a610d-138">Note</span><span class="sxs-lookup"><span data-stu-id="a610d-138">NOTES</span></span>

## <span data-ttu-id="a610d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a610d-139">RELATED LINKS</span></span>

[<span data-ttu-id="a610d-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="a610d-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
