---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687108"
---
# <span data-ttu-id="7438d-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="7438d-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="7438d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7438d-102">SYNOPSIS</span></span>
<span data-ttu-id="7438d-103">Aggiorna la direzione di replica per l'elemento protetto di replica o il piano di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="7438d-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="7438d-104">Usato per ripetere la protezione/inversione della replica di un piano di ripristino o di elemento replicato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="7438d-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7438d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7438d-105">SYNTAX</span></span>

### <span data-ttu-id="7438d-106">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7438d-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7438d-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7438d-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7438d-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="7438d-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7438d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7438d-109">DESCRIPTION</span></span>
<span data-ttu-id="7438d-110">Il cmdlet **Update-AzureRmRecoveryServicesAsrProtectionDirection** aggiorna la direzione di replica per l'oggetto di recupero del sito di Azure specificato dopo il completamento di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="7438d-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="7438d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7438d-111">EXAMPLES</span></span>

### <span data-ttu-id="7438d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7438d-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="7438d-113">Avviare l'operazione di direzione dell'aggiornamento per il piano di recoveyr specificato e restituire l'oggetto processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7438d-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="7438d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7438d-114">PARAMETERS</span></span>

### <span data-ttu-id="7438d-115">-Direzione</span><span class="sxs-lookup"><span data-stu-id="7438d-115">-Direction</span></span>
<span data-ttu-id="7438d-116">Specifica la direzione da usare per l'operazione di aggiornamento dopo un failover.</span><span class="sxs-lookup"><span data-stu-id="7438d-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="7438d-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7438d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7438d-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7438d-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="7438d-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7438d-119">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7438d-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7438d-120">-RecoveryPlan</span></span>
<span data-ttu-id="7438d-121">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="7438d-121">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7438d-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7438d-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7438d-123">Specifica un elemento protetto da replica ASR</span><span class="sxs-lookup"><span data-stu-id="7438d-123">Specifies an ASR replication protected item</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7438d-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7438d-124">-Confirm</span></span>
<span data-ttu-id="7438d-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7438d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7438d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7438d-126">-WhatIf</span></span>
<span data-ttu-id="7438d-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7438d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7438d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7438d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7438d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7438d-129">CommonParameters</span></span>
<span data-ttu-id="7438d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7438d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7438d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7438d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7438d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7438d-132">INPUTS</span></span>

### <span data-ttu-id="7438d-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7438d-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="7438d-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7438d-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7438d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7438d-135">OUTPUTS</span></span>

### <span data-ttu-id="7438d-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7438d-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7438d-137">Note</span><span class="sxs-lookup"><span data-stu-id="7438d-137">NOTES</span></span>

## <span data-ttu-id="7438d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7438d-138">RELATED LINKS</span></span>

