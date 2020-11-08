---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021634"
---
# <span data-ttu-id="0be31-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="0be31-101">Get-AzImage</span></span>

## <span data-ttu-id="0be31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0be31-102">SYNOPSIS</span></span>
<span data-ttu-id="0be31-103">Ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="0be31-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="0be31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0be31-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be31-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0be31-105">DESCRIPTION</span></span>
<span data-ttu-id="0be31-106">Il cmdlet **Get-aziming** ottiene le proprietà di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="0be31-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="0be31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0be31-107">EXAMPLES</span></span>

### <span data-ttu-id="0be31-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0be31-108">Example 1</span></span>
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

<span data-ttu-id="0be31-109">Questo comando consente di ottenere le proprietà dell'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0be31-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0be31-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0be31-110">Example 2</span></span>
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

<span data-ttu-id="0be31-111">Questo comando consente di ottenere le proprietà di tutte le immagini nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0be31-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0be31-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0be31-112">Example 3</span></span>
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

<span data-ttu-id="0be31-113">Questo comando consente di ottenere le proprietà di tutte le immagini sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0be31-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="0be31-114">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="0be31-114">Example 4</span></span>
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

<span data-ttu-id="0be31-115">Questo comando consente di ottenere le proprietà di tutte le immagini sotto l'abbonamento che iniziano con "immagine".</span><span class="sxs-lookup"><span data-stu-id="0be31-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="0be31-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0be31-116">PARAMETERS</span></span>

### <span data-ttu-id="0be31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be31-117">-DefaultProfile</span></span>
<span data-ttu-id="0be31-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0be31-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0be31-119">-Espandi</span><span class="sxs-lookup"><span data-stu-id="0be31-119">-Expand</span></span>
<span data-ttu-id="0be31-120">Specifica la query di espressione Expand.</span><span class="sxs-lookup"><span data-stu-id="0be31-120">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="0be31-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0be31-121">-ImageName</span></span>
<span data-ttu-id="0be31-122">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="0be31-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="0be31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be31-123">-ResourceGroupName</span></span>
<span data-ttu-id="0be31-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0be31-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0be31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be31-125">CommonParameters</span></span>
<span data-ttu-id="0be31-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be31-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0be31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be31-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0be31-128">INPUTS</span></span>

### <span data-ttu-id="0be31-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0be31-129">System.String</span></span>

## <span data-ttu-id="0be31-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0be31-130">OUTPUTS</span></span>

### <span data-ttu-id="0be31-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="0be31-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0be31-132">Note</span><span class="sxs-lookup"><span data-stu-id="0be31-132">NOTES</span></span>

## <span data-ttu-id="0be31-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0be31-133">RELATED LINKS</span></span>
