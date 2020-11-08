---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d147ac47b2f53aa48f8989884b99c519e5ffb08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191312"
---
# <span data-ttu-id="22c8b-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="22c8b-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="22c8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="22c8b-103">Avvia l'operazione di pulizia del failover test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="22c8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22c8b-104">SYNTAX</span></span>

### <span data-ttu-id="22c8b-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22c8b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c8b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22c8b-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22c8b-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="22c8b-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c8b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22c8b-108">DESCRIPTION</span></span>
<span data-ttu-id="22c8b-109">Il cmdlet **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** avvia l'operazione di pulizia del failover del test su un elemento protetto da replica o un piano di ripristino in cui è stato eseguito un failover di test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="22c8b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22c8b-110">EXAMPLES</span></span>

### <span data-ttu-id="22c8b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22c8b-111">Example 1</span></span>

<span data-ttu-id="22c8b-112">Processo per tenere traccia della pulizia del failover dei test di un recoveryPlan di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="22c8b-112">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

```powershell
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

### <span data-ttu-id="22c8b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="22c8b-113">Example 2</span></span>

<span data-ttu-id="22c8b-114">Avvia l'operazione di pulizia del failover test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-114">Starts the test failover cleanup operation.</span></span> <span data-ttu-id="22c8b-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="22c8b-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -Comment 'testing done' -ReplicationProtectedItem $rpi
```

## <span data-ttu-id="22c8b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22c8b-116">PARAMETERS</span></span>

### <span data-ttu-id="22c8b-117">-Commento</span><span class="sxs-lookup"><span data-stu-id="22c8b-117">-Comment</span></span>
<span data-ttu-id="22c8b-118">Commento utente per il failover dei test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-118">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="22c8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c8b-119">-DefaultProfile</span></span>
<span data-ttu-id="22c8b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22c8b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c8b-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22c8b-121">-RecoveryPlan</span></span>
<span data-ttu-id="22c8b-122">Piano di ripristino per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-122">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="22c8b-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22c8b-123">-ReplicationProtectedItem</span></span>
<span data-ttu-id="22c8b-124">Elemento protetto da replica per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="22c8b-124">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="22c8b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22c8b-125">-ResourceId</span></span>
<span data-ttu-id="22c8b-126">ID risorsa del piano di elemento/ripristino protetto da replica per il failover del test CleaningUp.</span><span class="sxs-lookup"><span data-stu-id="22c8b-126">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c8b-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22c8b-127">-Confirm</span></span>
<span data-ttu-id="22c8b-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c8b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c8b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c8b-129">-WhatIf</span></span>
<span data-ttu-id="22c8b-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22c8b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c8b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22c8b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c8b-132">CommonParameters</span></span>
<span data-ttu-id="22c8b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c8b-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22c8b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c8b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22c8b-135">INPUTS</span></span>

### <span data-ttu-id="22c8b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22c8b-136">System.String</span></span>

### <span data-ttu-id="22c8b-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22c8b-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="22c8b-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22c8b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="22c8b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22c8b-139">OUTPUTS</span></span>

### <span data-ttu-id="22c8b-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="22c8b-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22c8b-141">Note</span><span class="sxs-lookup"><span data-stu-id="22c8b-141">NOTES</span></span>

## <span data-ttu-id="22c8b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22c8b-142">RELATED LINKS</span></span>