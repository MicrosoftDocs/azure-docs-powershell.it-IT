---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032827"
---
# <span data-ttu-id="285fe-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285fe-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="285fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="285fe-102">SYNOPSIS</span></span>
<span data-ttu-id="285fe-103">Interrompe un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="285fe-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="285fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="285fe-104">SYNTAX</span></span>

### <span data-ttu-id="285fe-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="285fe-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285fe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="285fe-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="285fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="285fe-107">DESCRIPTION</span></span>
<span data-ttu-id="285fe-108">Il cmdlet **Stop-AzRecoveryServicesAsrJob** interrompe il processo di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="285fe-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="285fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="285fe-109">EXAMPLES</span></span>

### <span data-ttu-id="285fe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="285fe-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="285fe-111">Tenta di arrestare il processo specificato e restituisce un oggetto processo ASR aggiornato.</span><span class="sxs-lookup"><span data-stu-id="285fe-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="285fe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="285fe-112">PARAMETERS</span></span>

### <span data-ttu-id="285fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285fe-113">-DefaultProfile</span></span>
<span data-ttu-id="285fe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="285fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="285fe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="285fe-115">-InputObject</span></span>
<span data-ttu-id="285fe-116">Oggetto di input: specificare l'oggetto processo ASR che corrisponde al processo ASR da arrestare</span><span class="sxs-lookup"><span data-stu-id="285fe-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="285fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="285fe-117">-Name</span></span>
<span data-ttu-id="285fe-118">Specificare il processo ASR da arrestare tramite il nome del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="285fe-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285fe-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="285fe-119">-Confirm</span></span>
<span data-ttu-id="285fe-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="285fe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285fe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="285fe-121">-WhatIf</span></span>
<span data-ttu-id="285fe-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="285fe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="285fe-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="285fe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285fe-124">CommonParameters</span></span>
<span data-ttu-id="285fe-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285fe-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="285fe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285fe-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="285fe-127">INPUTS</span></span>

### <span data-ttu-id="285fe-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="285fe-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="285fe-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="285fe-129">OUTPUTS</span></span>

### <span data-ttu-id="285fe-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="285fe-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="285fe-131">Note</span><span class="sxs-lookup"><span data-stu-id="285fe-131">NOTES</span></span>

## <span data-ttu-id="285fe-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="285fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="285fe-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285fe-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="285fe-134">Riavviare-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285fe-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="285fe-135">Curriculum vitae-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="285fe-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
