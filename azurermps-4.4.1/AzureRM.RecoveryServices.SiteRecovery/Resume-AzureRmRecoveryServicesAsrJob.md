---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519999"
---
# <span data-ttu-id="d4f11-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="d4f11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4f11-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f11-103">Riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="d4f11-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4f11-104">SYNTAX</span></span>

### <span data-ttu-id="d4f11-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4f11-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f11-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d4f11-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4f11-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4f11-107">DESCRIPTION</span></span>
<span data-ttu-id="d4f11-108">Il cmdlet **Resume-AzureRmRecoveryServicesAsrJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="d4f11-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="d4f11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4f11-109">EXAMPLES</span></span>

### <span data-ttu-id="d4f11-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4f11-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="d4f11-111">Riprendi il processo specificato se si trova in uno stato in attesa o sospesa e Restituisci l'oggetto processo ASR aggiornato corrispondente al processo ASR.</span><span class="sxs-lookup"><span data-stu-id="d4f11-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="d4f11-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4f11-112">PARAMETERS</span></span>

### <span data-ttu-id="d4f11-113">-Commento</span><span class="sxs-lookup"><span data-stu-id="d4f11-113">-Comment</span></span>
<span data-ttu-id="d4f11-114">Commenti per il registro processi.</span><span class="sxs-lookup"><span data-stu-id="d4f11-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f11-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4f11-115">-InputObject</span></span>
<span data-ttu-id="d4f11-116">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo da riprendere.</span><span class="sxs-lookup"><span data-stu-id="d4f11-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f11-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4f11-117">-Name</span></span>
<span data-ttu-id="d4f11-118">Specificare il processo ASR per nome.</span><span class="sxs-lookup"><span data-stu-id="d4f11-118">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4f11-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4f11-119">-Confirm</span></span>
<span data-ttu-id="d4f11-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4f11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f11-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f11-121">-WhatIf</span></span>
<span data-ttu-id="d4f11-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4f11-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4f11-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4f11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f11-124">CommonParameters</span></span>
<span data-ttu-id="d4f11-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f11-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f11-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4f11-127">INPUTS</span></span>

### <span data-ttu-id="d4f11-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4f11-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4f11-129">OUTPUTS</span></span>

### <span data-ttu-id="d4f11-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4f11-131">Note</span><span class="sxs-lookup"><span data-stu-id="d4f11-131">NOTES</span></span>

## <span data-ttu-id="d4f11-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4f11-132">RELATED LINKS</span></span>

[<span data-ttu-id="d4f11-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d4f11-134">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="d4f11-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d4f11-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
