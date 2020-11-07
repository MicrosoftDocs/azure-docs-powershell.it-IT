---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: c53cc7b410f0898af7a643babef1781433cbd120
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677581"
---
# <span data-ttu-id="3ea71-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="3ea71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ea71-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea71-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea71-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="3ea71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ea71-104">SYNTAX</span></span>

### <span data-ttu-id="3ea71-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ea71-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea71-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3ea71-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ea71-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea71-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea71-108">Il cmdlet **Restart-AzRecoveryServicesAsrJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea71-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="3ea71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ea71-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea71-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ea71-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="3ea71-111">Riavvia il processo ASR specificato e restituisce l'oggetto processo ASR aggiornato del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="3ea71-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="3ea71-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ea71-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea71-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea71-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3ea71-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ea71-115">-InputObject</span></span>
<span data-ttu-id="3ea71-116">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo ASR da riavviare</span><span class="sxs-lookup"><span data-stu-id="3ea71-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="3ea71-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ea71-117">-Name</span></span>
<span data-ttu-id="3ea71-118">Specificare il processo per nome.</span><span class="sxs-lookup"><span data-stu-id="3ea71-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="3ea71-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ea71-119">-Confirm</span></span>
<span data-ttu-id="3ea71-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea71-121">-WhatIf</span></span>
<span data-ttu-id="3ea71-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea71-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ea71-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea71-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea71-124">CommonParameters</span></span>
<span data-ttu-id="3ea71-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea71-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea71-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea71-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ea71-127">INPUTS</span></span>

### <span data-ttu-id="3ea71-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3ea71-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ea71-129">OUTPUTS</span></span>

### <span data-ttu-id="3ea71-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3ea71-131">Note</span><span class="sxs-lookup"><span data-stu-id="3ea71-131">NOTES</span></span>

## <span data-ttu-id="3ea71-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ea71-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ea71-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="3ea71-134">Curriculum vitae-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="3ea71-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3ea71-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)