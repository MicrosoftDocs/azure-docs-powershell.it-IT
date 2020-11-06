---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513064"
---
# <span data-ttu-id="5eb29-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5eb29-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5eb29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eb29-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb29-103">Elimina i criteri di replica ASR specificati dall'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5eb29-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eb29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eb29-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb29-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb29-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb29-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrPolicy** ha eliminato i criteri di replica specificati dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5eb29-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5eb29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eb29-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb29-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5eb29-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="5eb29-109">Avvia l'eliminazione dei criteri di replica specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5eb29-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5eb29-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eb29-110">PARAMETERS</span></span>

### <span data-ttu-id="5eb29-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb29-111">-InputObject</span></span>
<span data-ttu-id="5eb29-112">Oggetto di input per il cmdlet: l'oggetto Criteri di replica ASR che corrisponde ai criteri di replica da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5eb29-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb29-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5eb29-113">-Confirm</span></span>
<span data-ttu-id="5eb29-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb29-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb29-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb29-115">-WhatIf</span></span>
<span data-ttu-id="5eb29-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5eb29-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5eb29-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5eb29-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb29-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb29-118">CommonParameters</span></span>
<span data-ttu-id="5eb29-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb29-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb29-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb29-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb29-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eb29-121">INPUTS</span></span>

### <span data-ttu-id="5eb29-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5eb29-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5eb29-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eb29-123">OUTPUTS</span></span>

### <span data-ttu-id="5eb29-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="5eb29-124">System.Object</span></span>

## <span data-ttu-id="5eb29-125">Note</span><span class="sxs-lookup"><span data-stu-id="5eb29-125">NOTES</span></span>

## <span data-ttu-id="5eb29-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eb29-126">RELATED LINKS</span></span>

[<span data-ttu-id="5eb29-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5eb29-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="5eb29-128">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5eb29-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
