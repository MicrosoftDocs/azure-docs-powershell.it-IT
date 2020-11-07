---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687112"
---
# <span data-ttu-id="9b851-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b851-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9b851-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b851-102">SYNOPSIS</span></span>
<span data-ttu-id="9b851-103">Interrompe un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="9b851-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b851-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b851-104">SYNTAX</span></span>

### <span data-ttu-id="9b851-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b851-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b851-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9b851-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b851-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b851-107">DESCRIPTION</span></span>
<span data-ttu-id="9b851-108">Il cmdlet **Stop-AzureRmRecoveryServicesAsrJob** interrompe il processo di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9b851-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="9b851-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b851-109">EXAMPLES</span></span>

### <span data-ttu-id="9b851-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b851-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="9b851-111">Tenta di arrestare il processo specificato e restituisce un oggetto processo ASR aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9b851-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="9b851-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b851-112">PARAMETERS</span></span>

### <span data-ttu-id="9b851-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b851-113">-InputObject</span></span>
<span data-ttu-id="9b851-114">Oggetto di input: specificare l'oggetto processo ASR che corrisponde al processo ASR da arrestare</span><span class="sxs-lookup"><span data-stu-id="9b851-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="9b851-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b851-115">-Name</span></span>
<span data-ttu-id="9b851-116">Specificare il processo ASR da arrestare tramite il nome del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="9b851-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="9b851-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b851-117">-Confirm</span></span>
<span data-ttu-id="9b851-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b851-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b851-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b851-119">-WhatIf</span></span>
<span data-ttu-id="9b851-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b851-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b851-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b851-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b851-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b851-122">CommonParameters</span></span>
<span data-ttu-id="9b851-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b851-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b851-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b851-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b851-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b851-125">INPUTS</span></span>

### <span data-ttu-id="9b851-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9b851-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b851-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b851-127">OUTPUTS</span></span>

### <span data-ttu-id="9b851-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9b851-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b851-129">Note</span><span class="sxs-lookup"><span data-stu-id="9b851-129">NOTES</span></span>

## <span data-ttu-id="9b851-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b851-130">RELATED LINKS</span></span>

[<span data-ttu-id="9b851-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b851-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b851-132">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b851-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9b851-133">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9b851-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
