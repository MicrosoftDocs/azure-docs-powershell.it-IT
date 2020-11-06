---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521155"
---
# <span data-ttu-id="3495c-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3495c-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="3495c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3495c-102">SYNOPSIS</span></span>
<span data-ttu-id="3495c-103">Ottiene i mapping del contenitore di protezione del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="3495c-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3495c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3495c-104">SYNTAX</span></span>

### <span data-ttu-id="3495c-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3495c-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="3495c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3495c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="3495c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3495c-107">DESCRIPTION</span></span>
<span data-ttu-id="3495c-108">Il cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** ottiene le informazioni sul contenitore di protezione per i mapping dei criteri di replica (Association) nel Vault per il contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="3495c-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="3495c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3495c-109">EXAMPLES</span></span>

### <span data-ttu-id="3495c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3495c-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="3495c-111">Ottiene tutti i mapping dei contenitori di protezione per il contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="3495c-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="3495c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3495c-112">PARAMETERS</span></span>

### <span data-ttu-id="3495c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3495c-113">-Name</span></span>
<span data-ttu-id="3495c-114">Specifica il nome del mapping del contenitore di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3495c-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="3495c-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3495c-115">-ProtectionContainer</span></span>
<span data-ttu-id="3495c-116">Ottenere mapping contenitore di protezione corrispondente all'oggetto contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="3495c-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3495c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3495c-117">CommonParameters</span></span>
<span data-ttu-id="3495c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3495c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3495c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3495c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3495c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3495c-120">INPUTS</span></span>

### <span data-ttu-id="3495c-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3495c-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="3495c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3495c-122">OUTPUTS</span></span>

### <span data-ttu-id="3495c-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3495c-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3495c-124">Note</span><span class="sxs-lookup"><span data-stu-id="3495c-124">NOTES</span></span>

## <span data-ttu-id="3495c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3495c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3495c-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3495c-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="3495c-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3495c-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
