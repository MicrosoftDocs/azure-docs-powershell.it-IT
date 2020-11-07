---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688252"
---
# <span data-ttu-id="d4505-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4505-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d4505-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4505-102">SYNOPSIS</span></span>
<span data-ttu-id="d4505-103">Consente di recuperare il piano di ripristino ASR specificato da Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="d4505-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4505-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4505-104">SYNTAX</span></span>

### <span data-ttu-id="d4505-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4505-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4505-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d4505-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4505-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4505-107">DESCRIPTION</span></span>
<span data-ttu-id="d4505-108">Il cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** Elimina il piano di ripristino specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d4505-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="d4505-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4505-109">EXAMPLES</span></span>

### <span data-ttu-id="d4505-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4505-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="d4505-111">Avvia l'eliminazione del piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4505-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d4505-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4505-112">PARAMETERS</span></span>

### <span data-ttu-id="d4505-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4505-113">-InputObject</span></span>
<span data-ttu-id="d4505-114">Oggetto di input per il cmdlet: l'oggetto piano di ripristino ASR corrispondente al piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d4505-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4505-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4505-115">-Name</span></span>
<span data-ttu-id="d4505-116">Specifica il nome del piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d4505-116">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="d4505-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4505-117">-Confirm</span></span>
<span data-ttu-id="d4505-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4505-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4505-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4505-119">-WhatIf</span></span>
<span data-ttu-id="d4505-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4505-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4505-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4505-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4505-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4505-122">CommonParameters</span></span>
<span data-ttu-id="d4505-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4505-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4505-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4505-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4505-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4505-125">INPUTS</span></span>

### <span data-ttu-id="d4505-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4505-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d4505-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4505-127">OUTPUTS</span></span>

### <span data-ttu-id="d4505-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="d4505-128">System.Object</span></span>

## <span data-ttu-id="d4505-129">Note</span><span class="sxs-lookup"><span data-stu-id="d4505-129">NOTES</span></span>

## <span data-ttu-id="d4505-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4505-130">RELATED LINKS</span></span>

[<span data-ttu-id="d4505-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4505-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d4505-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4505-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d4505-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4505-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


