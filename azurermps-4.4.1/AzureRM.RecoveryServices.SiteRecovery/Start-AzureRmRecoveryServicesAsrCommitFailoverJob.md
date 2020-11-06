---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519551"
---
# <span data-ttu-id="9494e-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9494e-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="9494e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9494e-102">SYNOPSIS</span></span>
<span data-ttu-id="9494e-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="9494e-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9494e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9494e-104">SYNTAX</span></span>

### <span data-ttu-id="9494e-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9494e-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9494e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9494e-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9494e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9494e-107">DESCRIPTION</span></span>
<span data-ttu-id="9494e-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="9494e-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="9494e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9494e-109">EXAMPLES</span></span>

### <span data-ttu-id="9494e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9494e-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="9494e-111">Avvia il failover di commit per il piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9494e-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9494e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9494e-112">PARAMETERS</span></span>

### <span data-ttu-id="9494e-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9494e-113">-RecoveryPlan</span></span>
<span data-ttu-id="9494e-114">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="9494e-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="9494e-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9494e-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9494e-116">Specifica un oggetto elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="9494e-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="9494e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9494e-117">-Confirm</span></span>
<span data-ttu-id="9494e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9494e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9494e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9494e-119">-WhatIf</span></span>
<span data-ttu-id="9494e-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9494e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9494e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9494e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9494e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9494e-122">CommonParameters</span></span>
<span data-ttu-id="9494e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9494e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9494e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9494e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9494e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9494e-125">INPUTS</span></span>

### <span data-ttu-id="9494e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9494e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="9494e-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9494e-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9494e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9494e-128">OUTPUTS</span></span>

### <span data-ttu-id="9494e-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9494e-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9494e-130">Note</span><span class="sxs-lookup"><span data-stu-id="9494e-130">NOTES</span></span>

## <span data-ttu-id="9494e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9494e-131">RELATED LINKS</span></span>

