---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350347"
---
# <span data-ttu-id="0b514-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b514-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0b514-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b514-102">SYNOPSIS</span></span>
<span data-ttu-id="0b514-103">Riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="0b514-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0b514-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b514-104">SYNTAX</span></span>

### <span data-ttu-id="0b514-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b514-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b514-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0b514-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b514-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b514-107">DESCRIPTION</span></span>
<span data-ttu-id="0b514-108">Il cmdlet **Resume-AzRecoveryServicesAsrJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="0b514-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="0b514-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b514-109">EXAMPLES</span></span>

### <span data-ttu-id="0b514-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b514-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0b514-111">Riprendi il processo specificato se si trova in uno stato in attesa o sospesa e Restituisci l'oggetto processo ASR aggiornato corrispondente al processo ASR.</span><span class="sxs-lookup"><span data-stu-id="0b514-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="0b514-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b514-112">PARAMETERS</span></span>

### <span data-ttu-id="0b514-113">-Commento</span><span class="sxs-lookup"><span data-stu-id="0b514-113">-Comment</span></span>
<span data-ttu-id="0b514-114">Commenti per il registro processi.</span><span class="sxs-lookup"><span data-stu-id="0b514-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b514-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b514-115">-DefaultProfile</span></span>
<span data-ttu-id="0b514-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b514-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0b514-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b514-117">-InputObject</span></span>
<span data-ttu-id="0b514-118">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo da riprendere.</span><span class="sxs-lookup"><span data-stu-id="0b514-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="0b514-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b514-119">-Name</span></span>
<span data-ttu-id="0b514-120">Specificare il processo ASR per nome.</span><span class="sxs-lookup"><span data-stu-id="0b514-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="0b514-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b514-121">-Confirm</span></span>
<span data-ttu-id="0b514-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b514-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b514-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b514-123">-WhatIf</span></span>
<span data-ttu-id="0b514-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b514-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b514-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b514-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b514-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b514-126">CommonParameters</span></span>
<span data-ttu-id="0b514-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b514-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b514-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b514-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b514-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b514-129">INPUTS</span></span>

### <span data-ttu-id="0b514-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b514-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b514-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b514-131">OUTPUTS</span></span>

### <span data-ttu-id="0b514-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b514-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b514-133">Note</span><span class="sxs-lookup"><span data-stu-id="0b514-133">NOTES</span></span>

## <span data-ttu-id="0b514-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b514-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b514-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b514-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0b514-136">Riavviare-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b514-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0b514-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0b514-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
