---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ce726675946b2b8dc40feb82a529ccf27ccef443
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013822"
---
# <span data-ttu-id="b7b06-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b7b06-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="b7b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b06-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b06-103">Recupera tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b06-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="b7b06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7b06-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7b06-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b06-106">Il cmdlet **Get-AzVMExtensionImage** ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b06-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="b7b06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7b06-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b06-108">Esempio 1: Ottenere le versioni di un'immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="b7b06-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="b7b06-109">Questo comando recupera tutte le versioni dell'immagine dell'estensione per la posizione, l'autore e il tipo specificati.</span><span class="sxs-lookup"><span data-stu-id="b7b06-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="b7b06-110">Esempio 2: Ottenere le versioni di un'immagine dell'estensione con il filtro sulla versione</span><span class="sxs-lookup"><span data-stu-id="b7b06-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="b7b06-111">Questo comando recupera tutte le versioni dell'immagine dell'estensione per la posizione, l'autore, il tipo e la versione specificati a partire da 12.</span><span class="sxs-lookup"><span data-stu-id="b7b06-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="b7b06-112">Esempio 3: Ottenere le versioni di un'immagine dell'estensione con il filtro sulla versione</span><span class="sxs-lookup"><span data-stu-id="b7b06-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="b7b06-113">Questo comando recupera tutte le versioni dell'immagine dell'estensione per la posizione, l'autore, il tipo e la versione specificati.</span><span class="sxs-lookup"><span data-stu-id="b7b06-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="b7b06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7b06-114">PARAMETERS</span></span>

### <span data-ttu-id="b7b06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b06-115">-DefaultProfile</span></span>
<span data-ttu-id="b7b06-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b06-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b7b06-117">-FilterExpression</span></span>
<span data-ttu-id="b7b06-118">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="b7b06-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b06-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b7b06-119">-Location</span></span>
<span data-ttu-id="b7b06-120">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="b7b06-120">Specifies the location of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b06-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b7b06-121">-PublisherName</span></span>
<span data-ttu-id="b7b06-122">Specifica il nome di un autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b7b06-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="b7b06-123">Per ottenere un autore dell'estensione, usare il cmdlet Get-AzVMImagePublisher estensione.</span><span class="sxs-lookup"><span data-stu-id="b7b06-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b06-124">-Type</span><span class="sxs-lookup"><span data-stu-id="b7b06-124">-Type</span></span>
<span data-ttu-id="b7b06-125">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="b7b06-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="b7b06-126">Per ottenere un tipo di estensione, usare il cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="b7b06-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b06-127">-Version</span><span class="sxs-lookup"><span data-stu-id="b7b06-127">-Version</span></span>
<span data-ttu-id="b7b06-128">Specifica la versione dell'estensione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b06-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7b06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b06-129">CommonParameters</span></span>
<span data-ttu-id="b7b06-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b06-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7b06-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b06-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7b06-132">INPUTS</span></span>

### <span data-ttu-id="b7b06-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b7b06-133">System.String</span></span>

## <span data-ttu-id="b7b06-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7b06-134">OUTPUTS</span></span>

### <span data-ttu-id="b7b06-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b7b06-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="b7b06-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="b7b06-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="b7b06-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7b06-137">NOTES</span></span>

## <span data-ttu-id="b7b06-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7b06-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7b06-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b7b06-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="b7b06-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b7b06-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="b7b06-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b7b06-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


