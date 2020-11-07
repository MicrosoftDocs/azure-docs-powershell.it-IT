---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856586"
---
# <span data-ttu-id="7ffa5-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="7ffa5-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="7ffa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ffa5-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffa5-103">Avvia l'operazione di pulizia del failover test.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="7ffa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ffa5-104">SYNTAX</span></span>

### <span data-ttu-id="7ffa5-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ffa5-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ffa5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffa5-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ffa5-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7ffa5-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ffa5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ffa5-108">DESCRIPTION</span></span>
<span data-ttu-id="7ffa5-109">Il cmdlet **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** avvia l'operazione di pulizia del failover del test su un elemento protetto da replica o un piano di ripristino in cui è stato eseguito un failover di test.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="7ffa5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ffa5-110">EXAMPLES</span></span>

### <span data-ttu-id="7ffa5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ffa5-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="7ffa5-112">Processo per tenere traccia della pulizia del failover dei test di un elemento protetto della replica di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="7ffa5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7ffa5-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="7ffa5-114">Processo per tenere traccia della pulizia del failover dei test di un recoveryPlan di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="7ffa5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ffa5-115">PARAMETERS</span></span>

### <span data-ttu-id="7ffa5-116">-Commento</span><span class="sxs-lookup"><span data-stu-id="7ffa5-116">-Comment</span></span>
<span data-ttu-id="7ffa5-117">Commento utente per il failover dei test.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="7ffa5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffa5-118">-DefaultProfile</span></span>
<span data-ttu-id="7ffa5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ffa5-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ffa5-120">-RecoveryPlan</span></span>
<span data-ttu-id="7ffa5-121">Piano di ripristino per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="7ffa5-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ffa5-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7ffa5-123">Elemento protetto da replica per eseguire la pulizia del failover del test.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="7ffa5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ffa5-124">-ResourceId</span></span>
<span data-ttu-id="7ffa5-125">ID risorsa del piano di elemento/ripristino protetto da replica per il failover del test CleaningUp.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

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

### <span data-ttu-id="7ffa5-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ffa5-126">-Confirm</span></span>
<span data-ttu-id="7ffa5-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ffa5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffa5-128">-WhatIf</span></span>
<span data-ttu-id="7ffa5-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffa5-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ffa5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffa5-131">CommonParameters</span></span>
<span data-ttu-id="7ffa5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ffa5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffa5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffa5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffa5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ffa5-134">INPUTS</span></span>

### <span data-ttu-id="7ffa5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7ffa5-135">System.String</span></span>

### <span data-ttu-id="7ffa5-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7ffa5-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="7ffa5-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ffa5-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7ffa5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ffa5-138">OUTPUTS</span></span>

### <span data-ttu-id="7ffa5-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ffa5-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ffa5-140">Note</span><span class="sxs-lookup"><span data-stu-id="7ffa5-140">NOTES</span></span>

## <span data-ttu-id="7ffa5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ffa5-141">RELATED LINKS</span></span>
