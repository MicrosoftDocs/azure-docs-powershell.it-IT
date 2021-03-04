---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 8261a4ee59d7a29911e7cfde3b28b5d28e3e1ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969246"
---
# <span data-ttu-id="db427-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="db427-101">Get-AzImage</span></span>

## <span data-ttu-id="db427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db427-102">SYNOPSIS</span></span>
<span data-ttu-id="db427-103">Ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="db427-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="db427-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db427-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db427-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db427-105">DESCRIPTION</span></span>
<span data-ttu-id="db427-106">Il **cmdlet Get-AzImage** ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="db427-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="db427-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db427-107">EXAMPLES</span></span>

### <span data-ttu-id="db427-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db427-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="db427-109">Questo comando ottiene le proprietà dell'immagine denominata 'Image01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="db427-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="db427-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="db427-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="db427-111">Questo comando ottiene le proprietà di tutte le immagini nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="db427-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="db427-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="db427-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="db427-113">Questo comando recupera le proprietà di tutte le immagini nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db427-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="db427-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="db427-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="db427-115">Questo comando recupera le proprietà di tutte le immagini nell'abbonamento che iniziano con "Immagine".</span><span class="sxs-lookup"><span data-stu-id="db427-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="db427-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db427-116">PARAMETERS</span></span>

### <span data-ttu-id="db427-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db427-117">-DefaultProfile</span></span>
<span data-ttu-id="db427-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db427-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db427-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="db427-119">-Expand</span></span>
<span data-ttu-id="db427-120">Specifica la query di espansione delle espressioni.</span><span class="sxs-lookup"><span data-stu-id="db427-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db427-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="db427-121">-ImageName</span></span>
<span data-ttu-id="db427-122">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="db427-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="db427-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db427-123">-ResourceGroupName</span></span>
<span data-ttu-id="db427-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db427-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="db427-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db427-125">CommonParameters</span></span>
<span data-ttu-id="db427-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db427-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db427-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db427-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db427-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="db427-128">INPUTS</span></span>

### <span data-ttu-id="db427-129">System.String</span><span class="sxs-lookup"><span data-stu-id="db427-129">System.String</span></span>

## <span data-ttu-id="db427-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db427-130">OUTPUTS</span></span>

### <span data-ttu-id="db427-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="db427-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="db427-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="db427-132">NOTES</span></span>

## <span data-ttu-id="db427-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db427-133">RELATED LINKS</span></span>
