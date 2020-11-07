---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687116"
---
# <span data-ttu-id="695b1-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="695b1-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="695b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="695b1-102">SYNOPSIS</span></span>
<span data-ttu-id="695b1-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="695b1-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="695b1-104">SYNTAX</span></span>

### <span data-ttu-id="695b1-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="695b1-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="695b1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="695b1-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="695b1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="695b1-107">DESCRIPTION</span></span>
<span data-ttu-id="695b1-108">Il cmdlet **Restart-AzureRmRecoveryServicesAsrJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="695b1-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="695b1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="695b1-109">EXAMPLES</span></span>

### <span data-ttu-id="695b1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="695b1-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="695b1-111">Riavvia il processo ASR specificato e restituisce l'oggetto processo ASR aggiornato del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="695b1-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="695b1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="695b1-112">PARAMETERS</span></span>

### <span data-ttu-id="695b1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="695b1-113">-InputObject</span></span>
<span data-ttu-id="695b1-114">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo ASR da riavviare</span><span class="sxs-lookup"><span data-stu-id="695b1-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="695b1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="695b1-115">-Name</span></span>
<span data-ttu-id="695b1-116">Specificare il processo per nome.</span><span class="sxs-lookup"><span data-stu-id="695b1-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="695b1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="695b1-117">-Confirm</span></span>
<span data-ttu-id="695b1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="695b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="695b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695b1-119">-WhatIf</span></span>
<span data-ttu-id="695b1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="695b1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="695b1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="695b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="695b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695b1-122">CommonParameters</span></span>
<span data-ttu-id="695b1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695b1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695b1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="695b1-125">INPUTS</span></span>

### <span data-ttu-id="695b1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="695b1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="695b1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="695b1-127">OUTPUTS</span></span>

### <span data-ttu-id="695b1-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="695b1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="695b1-129">Note</span><span class="sxs-lookup"><span data-stu-id="695b1-129">NOTES</span></span>

## <span data-ttu-id="695b1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="695b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="695b1-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="695b1-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="695b1-132">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="695b1-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="695b1-133">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="695b1-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
