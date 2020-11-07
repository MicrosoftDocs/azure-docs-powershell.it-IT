---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687121"
---
# <span data-ttu-id="c9b34-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b34-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c9b34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9b34-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b34-103">Ottiene i mapping di classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="c9b34-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9b34-104">SYNTAX</span></span>

### <span data-ttu-id="c9b34-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9b34-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="c9b34-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c9b34-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="c9b34-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9b34-107">DESCRIPTION</span></span>
<span data-ttu-id="c9b34-108">Il cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** ottiene i dettagli di un mapping della classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="c9b34-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="c9b34-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9b34-109">EXAMPLES</span></span>

### <span data-ttu-id="c9b34-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9b34-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="c9b34-111">Elenca tutti i mapping di classificazione dello spazio di archiviazione corrispondenti alla classificazione di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="c9b34-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="c9b34-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9b34-112">PARAMETERS</span></span>

### <span data-ttu-id="c9b34-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9b34-113">-Name</span></span>
<span data-ttu-id="c9b34-114">Specifica il nome del mapping di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c9b34-114">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b34-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="c9b34-115">-StorageClassification</span></span>
<span data-ttu-id="c9b34-116">Specifica un oggetto di classificazione dello spazio di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="c9b34-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="c9b34-117">Il cmdlet ottiene i mapping di classificazione di archiviazione ASR corrispondenti alla classificazione di archiviazione specificata</span><span class="sxs-lookup"><span data-stu-id="c9b34-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b34-118">CommonParameters</span></span>
<span data-ttu-id="c9b34-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b34-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b34-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b34-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9b34-121">INPUTS</span></span>

### <span data-ttu-id="c9b34-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9b34-122">None</span></span>

## <span data-ttu-id="c9b34-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9b34-123">OUTPUTS</span></span>

### <span data-ttu-id="c9b34-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c9b34-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c9b34-125">Note</span><span class="sxs-lookup"><span data-stu-id="c9b34-125">NOTES</span></span>

## <span data-ttu-id="c9b34-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9b34-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9b34-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b34-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c9b34-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c9b34-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
