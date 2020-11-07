---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 33c833004269e26204d97b9993db93aac7389642
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852158"
---
# <span data-ttu-id="15d47-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="15d47-101">Get-AzGallery</span></span>

## <span data-ttu-id="15d47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15d47-102">SYNOPSIS</span></span>
<span data-ttu-id="15d47-103">Ottenere o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="15d47-103">Get or list galleries.</span></span>

## <span data-ttu-id="15d47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15d47-104">SYNTAX</span></span>

### <span data-ttu-id="15d47-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15d47-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15d47-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="15d47-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d47-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15d47-107">DESCRIPTION</span></span>
<span data-ttu-id="15d47-108">Ottenere o elencare le raccolte.</span><span class="sxs-lookup"><span data-stu-id="15d47-108">Get or list galleries.</span></span>

## <span data-ttu-id="15d47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15d47-109">EXAMPLES</span></span>

### <span data-ttu-id="15d47-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15d47-110">Example 1</span></span>
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

<span data-ttu-id="15d47-111">Ottenere la raccolta "Gallery1"</span><span class="sxs-lookup"><span data-stu-id="15d47-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="15d47-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="15d47-112">Example 2</span></span>
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

<span data-ttu-id="15d47-113">Ottenere tutte le raccolte in RG1.</span><span class="sxs-lookup"><span data-stu-id="15d47-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="15d47-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="15d47-114">Example 3</span></span>
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

<span data-ttu-id="15d47-115">Ottenere tutte le raccolte in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="15d47-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="15d47-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="15d47-116">Example 4</span></span>
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

<span data-ttu-id="15d47-117">Ottenere tutte le raccolte in abbonamento che iniziano con "raccolta".</span><span class="sxs-lookup"><span data-stu-id="15d47-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="15d47-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15d47-118">PARAMETERS</span></span>

### <span data-ttu-id="15d47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d47-119">-DefaultProfile</span></span>
<span data-ttu-id="15d47-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15d47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d47-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="15d47-121">-Name</span></span>
<span data-ttu-id="15d47-122">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="15d47-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="15d47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d47-123">-ResourceGroupName</span></span>
<span data-ttu-id="15d47-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15d47-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="15d47-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15d47-125">-ResourceId</span></span>
<span data-ttu-id="15d47-126">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="15d47-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="15d47-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d47-127">CommonParameters</span></span>
<span data-ttu-id="15d47-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d47-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d47-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15d47-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d47-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15d47-130">INPUTS</span></span>

### <span data-ttu-id="15d47-131">System. String</span><span class="sxs-lookup"><span data-stu-id="15d47-131">System.String</span></span>

## <span data-ttu-id="15d47-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15d47-132">OUTPUTS</span></span>

### <span data-ttu-id="15d47-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="15d47-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="15d47-134">Note</span><span class="sxs-lookup"><span data-stu-id="15d47-134">NOTES</span></span>

## <span data-ttu-id="15d47-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15d47-135">RELATED LINKS</span></span>
