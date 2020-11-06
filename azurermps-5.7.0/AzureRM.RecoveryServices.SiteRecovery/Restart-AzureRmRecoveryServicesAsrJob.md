---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514212"
---
# <span data-ttu-id="685e7-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="685e7-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="685e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="685e7-102">SYNOPSIS</span></span>
<span data-ttu-id="685e7-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="685e7-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="685e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="685e7-104">SYNTAX</span></span>

### <span data-ttu-id="685e7-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="685e7-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="685e7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="685e7-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="685e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="685e7-107">DESCRIPTION</span></span>
<span data-ttu-id="685e7-108">Il cmdlet **Restart-AzureRmRecoveryServicesAsrJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="685e7-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="685e7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="685e7-109">EXAMPLES</span></span>

### <span data-ttu-id="685e7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="685e7-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="685e7-111">Riavvia il processo ASR specificato e restituisce l'oggetto processo ASR aggiornato del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="685e7-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="685e7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="685e7-112">PARAMETERS</span></span>

### <span data-ttu-id="685e7-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="685e7-113">-Confirm</span></span>
<span data-ttu-id="685e7-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="685e7-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="685e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="685e7-115">-DefaultProfile</span></span>
<span data-ttu-id="685e7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="685e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="685e7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="685e7-117">-InputObject</span></span>
<span data-ttu-id="685e7-118">L'oggetto di input per il cmdlet: l'oggetto processo ASR che corrisponde al processo ASR da riavviare</span><span class="sxs-lookup"><span data-stu-id="685e7-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="685e7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="685e7-119">-Name</span></span>
<span data-ttu-id="685e7-120">Specificare il processo per nome.</span><span class="sxs-lookup"><span data-stu-id="685e7-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="685e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="685e7-121">-WhatIf</span></span>
<span data-ttu-id="685e7-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="685e7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="685e7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="685e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="685e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="685e7-124">CommonParameters</span></span>
<span data-ttu-id="685e7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="685e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="685e7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="685e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="685e7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="685e7-127">INPUTS</span></span>

### <span data-ttu-id="685e7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="685e7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="685e7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="685e7-129">OUTPUTS</span></span>

### <span data-ttu-id="685e7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="685e7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="685e7-131">Note</span><span class="sxs-lookup"><span data-stu-id="685e7-131">NOTES</span></span>

## <span data-ttu-id="685e7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="685e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="685e7-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="685e7-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="685e7-134">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="685e7-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="685e7-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="685e7-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
