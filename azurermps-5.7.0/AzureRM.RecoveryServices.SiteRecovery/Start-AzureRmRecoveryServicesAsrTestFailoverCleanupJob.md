---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508043"
---
# <span data-ttu-id="e8f9b-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="e8f9b-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="e8f9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f9b-103">Avvia l'operazione di pulizia del failover test.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8f9b-104">SYNTAX</span></span>

### <span data-ttu-id="e8f9b-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8f9b-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f9b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f9b-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f9b-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e8f9b-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f9b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8f9b-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f9b-109">Il cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** avvia l'operazione di pulizia del failover del test su un elemento protetto da replica o un piano di ripristino in cui è stato eseguito un failover di test.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="e8f9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8f9b-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f9b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8f9b-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="e8f9b-112">Processo per tenere traccia della pulizia del failover dei test di un elemento protetto della replica di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="e8f9b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e8f9b-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

<span data-ttu-id="e8f9b-114">Processo per tenere traccia della pulizia del failover dei test di un recoveryPlan di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="e8f9b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8f9b-115">PARAMETERS</span></span>

### <span data-ttu-id="e8f9b-116">-Commento</span><span class="sxs-lookup"><span data-stu-id="e8f9b-116">-Comment</span></span>
<span data-ttu-id="e8f9b-117">Commento utente per il failover dei test.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="e8f9b-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8f9b-118">-Confirm</span></span>
<span data-ttu-id="e8f9b-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f9b-120">-DefaultProfile</span></span>
<span data-ttu-id="e8f9b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f9b-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8f9b-122">-RecoveryPlan</span></span>
<span data-ttu-id="e8f9b-123">Piano di ripristino per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-123">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="e8f9b-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8f9b-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e8f9b-125">Elemento protetto da replica per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-125">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="e8f9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f9b-126">-ResourceId</span></span>
<span data-ttu-id="e8f9b-127">ID risorsa del piano di elemento/ripristino protetto da replica per il failover del test CleaningUp.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-127">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f9b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f9b-128">-WhatIf</span></span>
<span data-ttu-id="e8f9b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f9b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f9b-131">CommonParameters</span></span>
<span data-ttu-id="e8f9b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f9b-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f9b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f9b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8f9b-134">INPUTS</span></span>

### <span data-ttu-id="e8f9b-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8f9b-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e8f9b-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8f9b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e8f9b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8f9b-137">OUTPUTS</span></span>

### <span data-ttu-id="e8f9b-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e8f9b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e8f9b-139">Note</span><span class="sxs-lookup"><span data-stu-id="e8f9b-139">NOTES</span></span>

## <span data-ttu-id="e8f9b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8f9b-140">RELATED LINKS</span></span>
