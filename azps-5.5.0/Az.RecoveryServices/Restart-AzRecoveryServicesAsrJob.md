---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192846"
---
# <span data-ttu-id="554ff-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="554ff-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="554ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="554ff-102">SYNOPSIS</span></span>
<span data-ttu-id="554ff-103">Riavvia un processo di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="554ff-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="554ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="554ff-104">SYNTAX</span></span>

### <span data-ttu-id="554ff-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="554ff-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="554ff-106">ByName</span><span class="sxs-lookup"><span data-stu-id="554ff-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="554ff-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="554ff-107">DESCRIPTION</span></span>
<span data-ttu-id="554ff-108">Il cmdlet **Restart-AzRecoveryServicesAsrJob** riavvia un processo di Ripristino siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="554ff-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="554ff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="554ff-109">EXAMPLES</span></span>

### <span data-ttu-id="554ff-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="554ff-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="554ff-111">Riavvia il processo ASR specificato e restituisce l'oggetto processo ASR aggiornato del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="554ff-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="554ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="554ff-112">PARAMETERS</span></span>

### <span data-ttu-id="554ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554ff-113">-DefaultProfile</span></span>
<span data-ttu-id="554ff-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="554ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="554ff-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="554ff-115">-InputObject</span></span>
<span data-ttu-id="554ff-116">Oggetto di input per il cmdlet: oggetto processo ASR corrispondente al processo asr da riavviare</span><span class="sxs-lookup"><span data-stu-id="554ff-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="554ff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="554ff-117">-Name</span></span>
<span data-ttu-id="554ff-118">Specificare il processo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="554ff-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="554ff-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="554ff-119">-Confirm</span></span>
<span data-ttu-id="554ff-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="554ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="554ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="554ff-121">-WhatIf</span></span>
<span data-ttu-id="554ff-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="554ff-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="554ff-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="554ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="554ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554ff-124">CommonParameters</span></span>
<span data-ttu-id="554ff-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="554ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554ff-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="554ff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554ff-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="554ff-127">INPUTS</span></span>

### <span data-ttu-id="554ff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="554ff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="554ff-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="554ff-129">OUTPUTS</span></span>

### <span data-ttu-id="554ff-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="554ff-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="554ff-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="554ff-131">NOTES</span></span>

## <span data-ttu-id="554ff-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="554ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="554ff-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="554ff-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="554ff-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="554ff-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="554ff-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="554ff-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
