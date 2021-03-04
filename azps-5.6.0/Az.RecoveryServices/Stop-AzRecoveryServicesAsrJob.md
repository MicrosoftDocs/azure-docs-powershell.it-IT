---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 77038e7e77060f8c83bfb67e70bc2a805f395ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990861"
---
# <span data-ttu-id="76f73-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="76f73-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="76f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f73-102">SYNOPSIS</span></span>
<span data-ttu-id="76f73-103">Interrompe un processo di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="76f73-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="76f73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76f73-104">SYNTAX</span></span>

### <span data-ttu-id="76f73-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76f73-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f73-106">ByName</span><span class="sxs-lookup"><span data-stu-id="76f73-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76f73-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76f73-107">DESCRIPTION</span></span>
<span data-ttu-id="76f73-108">Il cmdlet **Stop-AzRecoveryServicesAsrJob** interrompe il processo di Ripristino siti di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="76f73-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="76f73-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76f73-109">EXAMPLES</span></span>

### <span data-ttu-id="76f73-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76f73-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="76f73-111">Prova ad arrestare il processo specificato e restituisce un oggetto processo ASR aggiornato.</span><span class="sxs-lookup"><span data-stu-id="76f73-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="76f73-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f73-112">PARAMETERS</span></span>

### <span data-ttu-id="76f73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f73-113">-DefaultProfile</span></span>
<span data-ttu-id="76f73-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="76f73-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76f73-115">-InputObject</span></span>
<span data-ttu-id="76f73-116">Oggetto di input: specificare l'oggetto processo ASR corrispondente al processo ASR da arrestato</span><span class="sxs-lookup"><span data-stu-id="76f73-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="76f73-117">-Name</span><span class="sxs-lookup"><span data-stu-id="76f73-117">-Name</span></span>
<span data-ttu-id="76f73-118">Specificare il processo ASR da fermarsi in base al nome del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="76f73-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="76f73-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f73-119">-Confirm</span></span>
<span data-ttu-id="76f73-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f73-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f73-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f73-121">-WhatIf</span></span>
<span data-ttu-id="76f73-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f73-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76f73-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f73-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f73-124">CommonParameters</span></span>
<span data-ttu-id="76f73-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f73-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76f73-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f73-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="76f73-127">INPUTS</span></span>

### <span data-ttu-id="76f73-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="76f73-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="76f73-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76f73-129">OUTPUTS</span></span>

### <span data-ttu-id="76f73-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="76f73-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="76f73-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="76f73-131">NOTES</span></span>

## <span data-ttu-id="76f73-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76f73-132">RELATED LINKS</span></span>

[<span data-ttu-id="76f73-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="76f73-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="76f73-134">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="76f73-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="76f73-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="76f73-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
