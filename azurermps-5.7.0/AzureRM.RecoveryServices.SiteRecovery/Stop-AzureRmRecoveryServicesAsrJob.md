---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508036"
---
# <span data-ttu-id="68a2e-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="68a2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="68a2e-103">Interrompe un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="68a2e-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68a2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68a2e-104">SYNTAX</span></span>

### <span data-ttu-id="68a2e-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68a2e-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a2e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="68a2e-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a2e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68a2e-107">DESCRIPTION</span></span>
<span data-ttu-id="68a2e-108">Il cmdlet **Stop-AzureRmRecoveryServicesAsrJob** interrompe il processo di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="68a2e-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="68a2e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68a2e-109">EXAMPLES</span></span>

### <span data-ttu-id="68a2e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68a2e-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="68a2e-111">Tenta di arrestare il processo specificato e restituisce un oggetto processo ASR aggiornato.</span><span class="sxs-lookup"><span data-stu-id="68a2e-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="68a2e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68a2e-112">PARAMETERS</span></span>

### <span data-ttu-id="68a2e-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68a2e-113">-Confirm</span></span>
<span data-ttu-id="68a2e-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a2e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a2e-115">-DefaultProfile</span></span>
<span data-ttu-id="68a2e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68a2e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a2e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68a2e-117">-InputObject</span></span>
<span data-ttu-id="68a2e-118">Oggetto di input: specificare l'oggetto processo ASR che corrisponde al processo ASR da arrestare</span><span class="sxs-lookup"><span data-stu-id="68a2e-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="68a2e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="68a2e-119">-Name</span></span>
<span data-ttu-id="68a2e-120">Specificare il processo ASR da arrestare tramite il nome del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="68a2e-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="68a2e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a2e-121">-WhatIf</span></span>
<span data-ttu-id="68a2e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68a2e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68a2e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68a2e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a2e-124">CommonParameters</span></span>
<span data-ttu-id="68a2e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a2e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a2e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a2e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68a2e-127">INPUTS</span></span>

### <span data-ttu-id="68a2e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68a2e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68a2e-129">OUTPUTS</span></span>

### <span data-ttu-id="68a2e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68a2e-131">Note</span><span class="sxs-lookup"><span data-stu-id="68a2e-131">NOTES</span></span>

## <span data-ttu-id="68a2e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68a2e-132">RELATED LINKS</span></span>

[<span data-ttu-id="68a2e-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="68a2e-134">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="68a2e-135">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68a2e-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
