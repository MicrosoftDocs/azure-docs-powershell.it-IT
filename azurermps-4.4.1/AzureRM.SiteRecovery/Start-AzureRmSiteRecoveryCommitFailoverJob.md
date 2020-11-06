---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512887"
---
# <span data-ttu-id="5ceed-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5ceed-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="5ceed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ceed-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceed-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="5ceed-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ceed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ceed-104">SYNTAX</span></span>

### <span data-ttu-id="5ceed-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ceed-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ceed-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5ceed-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ceed-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="5ceed-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ceed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ceed-108">DESCRIPTION</span></span>
<span data-ttu-id="5ceed-109">Il cmdlet **Start-AzureRmSiteRecoveryCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="5ceed-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="5ceed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ceed-110">EXAMPLES</span></span>

## <span data-ttu-id="5ceed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ceed-111">PARAMETERS</span></span>

### <span data-ttu-id="5ceed-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5ceed-112">-ProtectionEntity</span></span>
<span data-ttu-id="5ceed-113">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="5ceed-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceed-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5ceed-114">-RecoveryPlan</span></span>
<span data-ttu-id="5ceed-115">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ceed-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceed-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ceed-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceed-117">-DefaultProfile</span></span>
<span data-ttu-id="5ceed-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ceed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceed-119">CommonParameters</span></span>
<span data-ttu-id="5ceed-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ceed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceed-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ceed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceed-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ceed-122">INPUTS</span></span>

### <span data-ttu-id="5ceed-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5ceed-123">ASRProtectionEntity</span></span>
<span data-ttu-id="5ceed-124">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ceed-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="5ceed-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5ceed-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="5ceed-126">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ceed-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="5ceed-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ceed-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="5ceed-128">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ceed-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="5ceed-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ceed-129">OUTPUTS</span></span>

### <span data-ttu-id="5ceed-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5ceed-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5ceed-131">Note</span><span class="sxs-lookup"><span data-stu-id="5ceed-131">NOTES</span></span>

## <span data-ttu-id="5ceed-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ceed-132">RELATED LINKS</span></span>

