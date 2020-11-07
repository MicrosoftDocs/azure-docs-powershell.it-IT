---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687105"
---
# <span data-ttu-id="7f179-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f179-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7f179-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f179-102">SYNOPSIS</span></span>
<span data-ttu-id="7f179-103">Aggiorna il contenuto di un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="7f179-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f179-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f179-104">SYNTAX</span></span>

### <span data-ttu-id="7f179-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f179-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f179-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="7f179-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f179-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f179-107">DESCRIPTION</span></span>
<span data-ttu-id="7f179-108">Il cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** aggiorna il contenuto di un piano di ripristino usando il contenuto dell'oggetto piano di ripristino ASR specificato o del file JSON di definizione del piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="7f179-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="7f179-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f179-109">EXAMPLES</span></span>

### <span data-ttu-id="7f179-110">Esempio 1: aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="7f179-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="7f179-111">Avviare l'operazione di aggiornamento di un piano di ripristino usando il contenuto dell'oggetto piano di ripristino ASR specificato e restituire il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f179-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7f179-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f179-112">PARAMETERS</span></span>

### <span data-ttu-id="7f179-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f179-113">-InputObject</span></span>
<span data-ttu-id="7f179-114">Oggetto di input per il cmdlet: specifica un oggetto piano di ripristino ASR, il cui contenuto viene usato per aggiornare il piano di ripristino a cui fa riferimento l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f179-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f179-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7f179-115">-Path</span></span>
<span data-ttu-id="7f179-116">Specifica il percorso del file JSON per la definizione del piano di ripristino usato per aggiornare il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f179-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f179-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f179-117">-Confirm</span></span>
<span data-ttu-id="7f179-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f179-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f179-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f179-119">-WhatIf</span></span>
<span data-ttu-id="7f179-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f179-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f179-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f179-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f179-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f179-122">CommonParameters</span></span>
<span data-ttu-id="7f179-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f179-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f179-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f179-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f179-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f179-125">INPUTS</span></span>

### <span data-ttu-id="7f179-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f179-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="7f179-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f179-127">OUTPUTS</span></span>

### <span data-ttu-id="7f179-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f179-128">System.Object</span></span>

## <span data-ttu-id="7f179-129">Note</span><span class="sxs-lookup"><span data-stu-id="7f179-129">NOTES</span></span>

## <span data-ttu-id="7f179-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f179-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f179-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f179-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7f179-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f179-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7f179-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7f179-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


