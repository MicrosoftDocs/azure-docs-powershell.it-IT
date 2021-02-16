---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177775"
---
# <span data-ttu-id="9b849-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="9b849-101">Get-AzGallery</span></span>

## <span data-ttu-id="9b849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b849-102">SYNOPSIS</span></span>
<span data-ttu-id="9b849-103">Recuperare o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="9b849-103">Get or list galleries.</span></span>

## <span data-ttu-id="9b849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b849-104">SYNTAX</span></span>

### <span data-ttu-id="9b849-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="9b849-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b849-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9b849-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b849-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b849-107">DESCRIPTION</span></span>
<span data-ttu-id="9b849-108">Recuperare o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="9b849-108">Get or list galleries.</span></span>

## <span data-ttu-id="9b849-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b849-109">EXAMPLES</span></span>

### <span data-ttu-id="9b849-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b849-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9b849-111">Ottenere la raccolta "raccolta1"</span><span class="sxs-lookup"><span data-stu-id="9b849-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="9b849-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9b849-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9b849-113">Ottenere tutte le raccolte in rg1.</span><span class="sxs-lookup"><span data-stu-id="9b849-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="9b849-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9b849-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9b849-115">Ottieni tutte le raccolte nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9b849-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="9b849-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9b849-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="9b849-117">Ottenere tutte le raccolte nell'abbonamento che iniziano con "raccolta".</span><span class="sxs-lookup"><span data-stu-id="9b849-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="9b849-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b849-118">PARAMETERS</span></span>

### <span data-ttu-id="9b849-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b849-119">-DefaultProfile</span></span>
<span data-ttu-id="9b849-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b849-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b849-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b849-121">-Name</span></span>
<span data-ttu-id="9b849-122">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9b849-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9b849-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b849-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b849-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b849-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9b849-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b849-125">-ResourceId</span></span>
<span data-ttu-id="9b849-126">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="9b849-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="9b849-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b849-127">CommonParameters</span></span>
<span data-ttu-id="9b849-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b849-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b849-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b849-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b849-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b849-130">INPUTS</span></span>

### <span data-ttu-id="9b849-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9b849-131">System.String</span></span>

## <span data-ttu-id="9b849-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b849-132">OUTPUTS</span></span>

### <span data-ttu-id="9b849-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="9b849-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="9b849-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b849-134">NOTES</span></span>

## <span data-ttu-id="9b849-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b849-135">RELATED LINKS</span></span>
