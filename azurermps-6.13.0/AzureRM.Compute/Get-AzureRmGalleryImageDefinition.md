---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511876"
---
# <span data-ttu-id="e82cb-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e82cb-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="e82cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e82cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e82cb-103">Ottenere o elencare le definizioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e82cb-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e82cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e82cb-104">SYNTAX</span></span>

### <span data-ttu-id="e82cb-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e82cb-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e82cb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e82cb-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e82cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e82cb-107">DESCRIPTION</span></span>
<span data-ttu-id="e82cb-108">Ottenere o elencare le definizioni delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e82cb-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="e82cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e82cb-109">EXAMPLES</span></span>

### <span data-ttu-id="e82cb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e82cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="e82cb-111">Ottenere la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e82cb-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="e82cb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e82cb-112">PARAMETERS</span></span>

### <span data-ttu-id="e82cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82cb-113">-DefaultProfile</span></span>
<span data-ttu-id="e82cb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e82cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e82cb-115">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="e82cb-115">-GalleryName</span></span>
<span data-ttu-id="e82cb-116">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e82cb-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82cb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e82cb-117">-Name</span></span>
<span data-ttu-id="e82cb-118">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e82cb-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="e82cb-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e82cb-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82cb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e82cb-121">-ResourceId</span></span>
<span data-ttu-id="e82cb-122">ID risorsa per la definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="e82cb-122">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82cb-123">CommonParameters</span></span>
<span data-ttu-id="e82cb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82cb-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82cb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e82cb-126">INPUTS</span></span>

### <span data-ttu-id="e82cb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e82cb-127">System.String</span></span>

## <span data-ttu-id="e82cb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e82cb-128">OUTPUTS</span></span>

### <span data-ttu-id="e82cb-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e82cb-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e82cb-130">Note</span><span class="sxs-lookup"><span data-stu-id="e82cb-130">NOTES</span></span>

## <span data-ttu-id="e82cb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e82cb-131">RELATED LINKS</span></span>
