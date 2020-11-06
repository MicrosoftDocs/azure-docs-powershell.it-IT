---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520619"
---
# <span data-ttu-id="5548c-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5548c-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="5548c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5548c-102">SYNOPSIS</span></span>
<span data-ttu-id="5548c-103">Riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="5548c-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5548c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5548c-104">SYNTAX</span></span>

### <span data-ttu-id="5548c-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5548c-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5548c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5548c-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5548c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5548c-107">DESCRIPTION</span></span>
<span data-ttu-id="5548c-108">Il cmdlet **Resume-AzureRmRecoveryServicesAsrJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="5548c-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="5548c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5548c-109">EXAMPLES</span></span>

### <span data-ttu-id="5548c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5548c-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="5548c-111">Riprendi il processo specificato se si trova in uno stato in attesa o sospesa e Restituisci l'oggetto processo ASR aggiornato corrispondente al processo ASR.</span><span class="sxs-lookup"><span data-stu-id="5548c-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="5548c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5548c-112">PARAMETERS</span></span>

### <span data-ttu-id="5548c-113">-Commento</span><span class="sxs-lookup"><span data-stu-id="5548c-113">-Comment</span></span>
<span data-ttu-id="5548c-114">Commenti per il registro processi.</span><span class="sxs-lookup"><span data-stu-id="5548c-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="5548c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5548c-115">-DefaultProfile</span></span>
<span data-ttu-id="5548c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5548c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5548c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5548c-117">-InputObject</span></span>
<span data-ttu-id="5548c-118">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo da riprendere.</span><span class="sxs-lookup"><span data-stu-id="5548c-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="5548c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5548c-119">-Name</span></span>
<span data-ttu-id="5548c-120">Specificare il processo ASR per nome.</span><span class="sxs-lookup"><span data-stu-id="5548c-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="5548c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5548c-121">-Confirm</span></span>
<span data-ttu-id="5548c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5548c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5548c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5548c-123">-WhatIf</span></span>
<span data-ttu-id="5548c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5548c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5548c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5548c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5548c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5548c-126">CommonParameters</span></span>
<span data-ttu-id="5548c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5548c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5548c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5548c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5548c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5548c-129">INPUTS</span></span>

### <span data-ttu-id="5548c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5548c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5548c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5548c-131">OUTPUTS</span></span>

### <span data-ttu-id="5548c-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5548c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5548c-133">Note</span><span class="sxs-lookup"><span data-stu-id="5548c-133">NOTES</span></span>

## <span data-ttu-id="5548c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5548c-134">RELATED LINKS</span></span>

[<span data-ttu-id="5548c-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5548c-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="5548c-136">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5548c-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="5548c-137">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5548c-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
