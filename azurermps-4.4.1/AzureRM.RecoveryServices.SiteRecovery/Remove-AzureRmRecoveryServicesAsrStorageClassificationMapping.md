---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520001"
---
# <span data-ttu-id="99465-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="99465-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="99465-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99465-102">SYNOPSIS</span></span>
<span data-ttu-id="99465-103">Elimina il mapping della classificazione dello spazio di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="99465-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99465-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99465-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99465-105">DESCRIPTION</span></span>
<span data-ttu-id="99465-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** Elimina il mapping di classificazione dello spazio di archiviazione del ripristino di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="99465-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="99465-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99465-107">EXAMPLES</span></span>

### <span data-ttu-id="99465-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99465-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="99465-109">Avvia l'eliminazione del mapping di classificazione dello spazio di archiviazione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="99465-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="99465-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99465-110">PARAMETERS</span></span>

### <span data-ttu-id="99465-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99465-111">-InputObject</span></span>
<span data-ttu-id="99465-112">L'oggetto di input per il cmdlet: l'oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping di classificazione dello spazio di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="99465-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99465-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99465-113">-Confirm</span></span>
<span data-ttu-id="99465-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99465-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99465-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99465-115">-WhatIf</span></span>
<span data-ttu-id="99465-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99465-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99465-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99465-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99465-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99465-118">CommonParameters</span></span>
<span data-ttu-id="99465-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99465-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99465-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99465-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99465-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99465-121">INPUTS</span></span>

### <span data-ttu-id="99465-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="99465-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="99465-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99465-123">OUTPUTS</span></span>

### <span data-ttu-id="99465-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="99465-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="99465-125">Note</span><span class="sxs-lookup"><span data-stu-id="99465-125">NOTES</span></span>

## <span data-ttu-id="99465-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99465-126">RELATED LINKS</span></span>

[<span data-ttu-id="99465-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="99465-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="99465-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="99465-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
