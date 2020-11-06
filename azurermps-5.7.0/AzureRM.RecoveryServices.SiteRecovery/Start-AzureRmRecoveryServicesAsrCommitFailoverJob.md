---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: b491ede16973704f873e018a06ae6147df5cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508044"
---
# <span data-ttu-id="99f4d-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="99f4d-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="99f4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="99f4d-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="99f4d-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99f4d-104">SYNTAX</span></span>

### <span data-ttu-id="99f4d-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99f4d-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f4d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="99f4d-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99f4d-107">DESCRIPTION</span></span>
<span data-ttu-id="99f4d-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="99f4d-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="99f4d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99f4d-109">EXAMPLES</span></span>

### <span data-ttu-id="99f4d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99f4d-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="99f4d-111">Avvia il failover di commit per il piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="99f4d-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="99f4d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99f4d-112">PARAMETERS</span></span>

### <span data-ttu-id="99f4d-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99f4d-113">-Confirm</span></span>
<span data-ttu-id="99f4d-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f4d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f4d-115">-DefaultProfile</span></span>
<span data-ttu-id="99f4d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99f4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="99f4d-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99f4d-117">-RecoveryPlan</span></span>
<span data-ttu-id="99f4d-118">Specifica un oggetto piano di ripristino ASR che corrisponde al piano di ripristino per il failover.</span><span class="sxs-lookup"><span data-stu-id="99f4d-118">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="99f4d-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="99f4d-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="99f4d-120">Specifica un oggetto elemento protetto da replica ASR che corrisponde all'elemento protetto da replica per il failover.</span><span class="sxs-lookup"><span data-stu-id="99f4d-120">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="99f4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f4d-121">-WhatIf</span></span>
<span data-ttu-id="99f4d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99f4d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99f4d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99f4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f4d-124">CommonParameters</span></span>
<span data-ttu-id="99f4d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f4d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f4d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f4d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99f4d-127">INPUTS</span></span>

### <span data-ttu-id="99f4d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99f4d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="99f4d-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="99f4d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="99f4d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99f4d-130">OUTPUTS</span></span>

### <span data-ttu-id="99f4d-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="99f4d-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="99f4d-132">Note</span><span class="sxs-lookup"><span data-stu-id="99f4d-132">NOTES</span></span>

## <span data-ttu-id="99f4d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99f4d-133">RELATED LINKS</span></span>
