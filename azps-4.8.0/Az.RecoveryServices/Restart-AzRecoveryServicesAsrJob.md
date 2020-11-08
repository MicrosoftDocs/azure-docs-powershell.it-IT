---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188966"
---
# <span data-ttu-id="9062e-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9062e-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9062e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9062e-102">SYNOPSIS</span></span>
<span data-ttu-id="9062e-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="9062e-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9062e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9062e-104">SYNTAX</span></span>

### <span data-ttu-id="9062e-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9062e-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9062e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9062e-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9062e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9062e-107">DESCRIPTION</span></span>
<span data-ttu-id="9062e-108">Il cmdlet **Restart-AzRecoveryServicesAsrJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="9062e-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9062e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9062e-109">EXAMPLES</span></span>

### <span data-ttu-id="9062e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9062e-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="9062e-111">Riavvia il processo ASR specificato e restituisce l'oggetto processo ASR aggiornato del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="9062e-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="9062e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9062e-112">PARAMETERS</span></span>

### <span data-ttu-id="9062e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9062e-113">-DefaultProfile</span></span>
<span data-ttu-id="9062e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9062e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9062e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9062e-115">-InputObject</span></span>
<span data-ttu-id="9062e-116">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo ASR da riavviare</span><span class="sxs-lookup"><span data-stu-id="9062e-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="9062e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9062e-117">-Name</span></span>
<span data-ttu-id="9062e-118">Specificare il processo per nome.</span><span class="sxs-lookup"><span data-stu-id="9062e-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="9062e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9062e-119">-Confirm</span></span>
<span data-ttu-id="9062e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9062e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9062e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9062e-121">-WhatIf</span></span>
<span data-ttu-id="9062e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9062e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9062e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9062e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9062e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9062e-124">CommonParameters</span></span>
<span data-ttu-id="9062e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9062e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9062e-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9062e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9062e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9062e-127">INPUTS</span></span>

### <span data-ttu-id="9062e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9062e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9062e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9062e-129">OUTPUTS</span></span>

### <span data-ttu-id="9062e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9062e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9062e-131">Note</span><span class="sxs-lookup"><span data-stu-id="9062e-131">NOTES</span></span>

## <span data-ttu-id="9062e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9062e-132">RELATED LINKS</span></span>

[<span data-ttu-id="9062e-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9062e-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="9062e-134">Curriculum vitae-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9062e-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="9062e-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9062e-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
