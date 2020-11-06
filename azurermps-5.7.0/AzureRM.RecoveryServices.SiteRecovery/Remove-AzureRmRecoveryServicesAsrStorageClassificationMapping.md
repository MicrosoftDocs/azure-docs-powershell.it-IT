---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c944bb084ccbcba740dc05a4ff1782500ff60930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514227"
---
# <span data-ttu-id="8dc5c-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8dc5c-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8dc5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc5c-103">Elimina il mapping della classificazione dello spazio di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dc5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dc5c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dc5c-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc5c-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** Elimina il mapping di classificazione dello spazio di archiviazione del ripristino di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="8dc5c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dc5c-107">EXAMPLES</span></span>

### <span data-ttu-id="8dc5c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dc5c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="8dc5c-109">Avvia l'eliminazione del mapping di classificazione dello spazio di archiviazione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8dc5c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dc5c-110">PARAMETERS</span></span>

### <span data-ttu-id="8dc5c-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8dc5c-111">-Confirm</span></span>
<span data-ttu-id="8dc5c-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc5c-113">-DefaultProfile</span></span>
<span data-ttu-id="8dc5c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8dc5c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc5c-115">-InputObject</span></span>
<span data-ttu-id="8dc5c-116">L'oggetto di input per il cmdlet: l'oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping di classificazione dello spazio di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-116">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="8dc5c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc5c-117">-WhatIf</span></span>
<span data-ttu-id="8dc5c-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc5c-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc5c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc5c-120">CommonParameters</span></span>
<span data-ttu-id="8dc5c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc5c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc5c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc5c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc5c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dc5c-123">INPUTS</span></span>

### <span data-ttu-id="8dc5c-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8dc5c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="8dc5c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dc5c-125">OUTPUTS</span></span>

### <span data-ttu-id="8dc5c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8dc5c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8dc5c-127">Note</span><span class="sxs-lookup"><span data-stu-id="8dc5c-127">NOTES</span></span>

## <span data-ttu-id="8dc5c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dc5c-128">RELATED LINKS</span></span>

[<span data-ttu-id="8dc5c-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8dc5c-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8dc5c-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8dc5c-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
