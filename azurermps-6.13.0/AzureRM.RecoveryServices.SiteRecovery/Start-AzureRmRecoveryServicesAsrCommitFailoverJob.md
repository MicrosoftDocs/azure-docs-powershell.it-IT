---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509167"
---
# <span data-ttu-id="b491c-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b491c-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="b491c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b491c-102">SYNOPSIS</span></span>
<span data-ttu-id="b491c-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="b491c-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b491c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b491c-104">SYNTAX</span></span>

### <span data-ttu-id="b491c-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b491c-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b491c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b491c-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b491c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b491c-107">DESCRIPTION</span></span>
<span data-ttu-id="b491c-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="b491c-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="b491c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b491c-109">EXAMPLES</span></span>

### <span data-ttu-id="b491c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b491c-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="b491c-111">Avvia il failover di commit per il piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b491c-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b491c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b491c-112">PARAMETERS</span></span>

### <span data-ttu-id="b491c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b491c-113">-DefaultProfile</span></span>
<span data-ttu-id="b491c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b491c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b491c-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b491c-115">-RecoveryPlan</span></span>
<span data-ttu-id="b491c-116">Specifica un oggetto piano di ripristino ASR che corrisponde al piano di ripristino per il failover.</span><span class="sxs-lookup"><span data-stu-id="b491c-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b491c-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b491c-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b491c-118">Specifica un oggetto elemento protetto da replica ASR che corrisponde all'elemento protetto da replica per il failover.</span><span class="sxs-lookup"><span data-stu-id="b491c-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b491c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b491c-119">-Confirm</span></span>
<span data-ttu-id="b491c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b491c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b491c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b491c-121">-WhatIf</span></span>
<span data-ttu-id="b491c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b491c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b491c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b491c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b491c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b491c-124">CommonParameters</span></span>
<span data-ttu-id="b491c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b491c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b491c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b491c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b491c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b491c-127">INPUTS</span></span>

### <span data-ttu-id="b491c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b491c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="b491c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b491c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b491c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b491c-130">OUTPUTS</span></span>

### <span data-ttu-id="b491c-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b491c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b491c-132">Note</span><span class="sxs-lookup"><span data-stu-id="b491c-132">NOTES</span></span>

## <span data-ttu-id="b491c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b491c-133">RELATED LINKS</span></span>
