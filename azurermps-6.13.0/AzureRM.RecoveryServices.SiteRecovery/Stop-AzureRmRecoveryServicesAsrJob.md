---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 14f24f9b9659b6668041b800462eca422fb67c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685560"
---
# <span data-ttu-id="2caaf-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2caaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2caaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2caaf-103">Interrompe un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="2caaf-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2caaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2caaf-104">SYNTAX</span></span>

### <span data-ttu-id="2caaf-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2caaf-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2caaf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2caaf-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2caaf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2caaf-107">DESCRIPTION</span></span>
<span data-ttu-id="2caaf-108">Il cmdlet **Stop-AzureRmRecoveryServicesAsrJob** interrompe il processo di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="2caaf-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="2caaf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2caaf-109">EXAMPLES</span></span>

### <span data-ttu-id="2caaf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2caaf-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="2caaf-111">Tenta di arrestare il processo specificato e restituisce un oggetto processo ASR aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2caaf-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="2caaf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2caaf-112">PARAMETERS</span></span>

### <span data-ttu-id="2caaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2caaf-113">-DefaultProfile</span></span>
<span data-ttu-id="2caaf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2caaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2caaf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2caaf-115">-InputObject</span></span>
<span data-ttu-id="2caaf-116">Oggetto di input: specificare l'oggetto processo ASR che corrisponde al processo ASR da arrestare</span><span class="sxs-lookup"><span data-stu-id="2caaf-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="2caaf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2caaf-117">-Name</span></span>
<span data-ttu-id="2caaf-118">Specificare il processo ASR da arrestare tramite il nome del processo ASR.</span><span class="sxs-lookup"><span data-stu-id="2caaf-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="2caaf-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2caaf-119">-Confirm</span></span>
<span data-ttu-id="2caaf-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2caaf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2caaf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2caaf-121">-WhatIf</span></span>
<span data-ttu-id="2caaf-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2caaf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2caaf-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2caaf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2caaf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2caaf-124">CommonParameters</span></span>
<span data-ttu-id="2caaf-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2caaf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2caaf-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2caaf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2caaf-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2caaf-127">INPUTS</span></span>

### <span data-ttu-id="2caaf-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2caaf-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2caaf-129">OUTPUTS</span></span>

### <span data-ttu-id="2caaf-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2caaf-131">Note</span><span class="sxs-lookup"><span data-stu-id="2caaf-131">NOTES</span></span>

## <span data-ttu-id="2caaf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2caaf-132">RELATED LINKS</span></span>

[<span data-ttu-id="2caaf-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="2caaf-134">Riavviare-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="2caaf-135">Curriculum vitae-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2caaf-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
