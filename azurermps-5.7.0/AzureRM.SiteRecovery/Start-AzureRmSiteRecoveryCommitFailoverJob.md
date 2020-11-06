---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverycommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 839855b9b56e4ecc73552af310af7221c9b7b2d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520333"
---
# <span data-ttu-id="8cd92-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8cd92-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="8cd92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cd92-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd92-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8cd92-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cd92-104">SYNTAX</span></span>

### <span data-ttu-id="8cd92-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cd92-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cd92-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8cd92-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cd92-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="8cd92-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cd92-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cd92-108">DESCRIPTION</span></span>
<span data-ttu-id="8cd92-109">Il cmdlet **Start-AzureRmSiteRecoveryCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="8cd92-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="8cd92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cd92-110">EXAMPLES</span></span>

## <span data-ttu-id="8cd92-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cd92-111">PARAMETERS</span></span>

### <span data-ttu-id="8cd92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd92-112">-DefaultProfile</span></span>
<span data-ttu-id="8cd92-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd92-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cd92-114">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8cd92-114">-ProtectionEntity</span></span>
<span data-ttu-id="8cd92-115">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8cd92-115">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cd92-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cd92-116">-RecoveryPlan</span></span>
<span data-ttu-id="8cd92-117">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8cd92-117">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="8cd92-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8cd92-118">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="8cd92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd92-119">CommonParameters</span></span>
<span data-ttu-id="8cd92-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd92-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd92-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd92-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cd92-122">INPUTS</span></span>

### <span data-ttu-id="8cd92-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8cd92-123">ASRProtectionEntity</span></span>
<span data-ttu-id="8cd92-124">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8cd92-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="8cd92-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cd92-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="8cd92-126">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8cd92-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="8cd92-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8cd92-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="8cd92-128">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8cd92-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="8cd92-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cd92-129">OUTPUTS</span></span>

### <span data-ttu-id="8cd92-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8cd92-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8cd92-131">Note</span><span class="sxs-lookup"><span data-stu-id="8cd92-131">NOTES</span></span>

## <span data-ttu-id="8cd92-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cd92-132">RELATED LINKS</span></span>

