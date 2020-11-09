---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310332"
---
# <span data-ttu-id="4e18b-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4e18b-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="4e18b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e18b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e18b-103">Ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e18b-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="4e18b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e18b-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e18b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e18b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e18b-106">Il cmdlet **Get-AzVMExtensionImage** ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e18b-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="4e18b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e18b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e18b-108">Esempio 1: ottenere le versioni di un'immagine di estensione</span><span class="sxs-lookup"><span data-stu-id="4e18b-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="4e18b-109">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore e il tipo specificati.</span><span class="sxs-lookup"><span data-stu-id="4e18b-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="4e18b-110">Esempio 2: ottenere le versioni di un'immagine di estensione con il filtro sulla versione</span><span class="sxs-lookup"><span data-stu-id="4e18b-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="4e18b-111">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore, il tipo e la versione specificati a partire da 12.</span><span class="sxs-lookup"><span data-stu-id="4e18b-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="4e18b-112">Esempio 3: ottenere le versioni di un'immagine di estensione con il filtro sulla versione</span><span class="sxs-lookup"><span data-stu-id="4e18b-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="4e18b-113">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore, il tipo e la versione specificati.</span><span class="sxs-lookup"><span data-stu-id="4e18b-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="4e18b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e18b-114">PARAMETERS</span></span>

### <span data-ttu-id="4e18b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e18b-115">-DefaultProfile</span></span>
<span data-ttu-id="4e18b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e18b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e18b-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="4e18b-117">-FilterExpression</span></span>
<span data-ttu-id="4e18b-118">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="4e18b-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="4e18b-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4e18b-119">-Location</span></span>
<span data-ttu-id="4e18b-120">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="4e18b-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="4e18b-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4e18b-121">-PublisherName</span></span>
<span data-ttu-id="4e18b-122">Specifica il nome di un Publisher di estensione.</span><span class="sxs-lookup"><span data-stu-id="4e18b-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="4e18b-123">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="4e18b-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4e18b-124">-Digitare</span><span class="sxs-lookup"><span data-stu-id="4e18b-124">-Type</span></span>
<span data-ttu-id="4e18b-125">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="4e18b-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="4e18b-126">Per ottenere un tipo di estensione, usare il cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="4e18b-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="4e18b-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="4e18b-127">-Version</span></span>
<span data-ttu-id="4e18b-128">Specifica la versione dell'estensione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="4e18b-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e18b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e18b-129">CommonParameters</span></span>
<span data-ttu-id="4e18b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e18b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e18b-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e18b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e18b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e18b-132">INPUTS</span></span>

### <span data-ttu-id="4e18b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4e18b-133">System.String</span></span>

## <span data-ttu-id="4e18b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e18b-134">OUTPUTS</span></span>

### <span data-ttu-id="4e18b-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4e18b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="4e18b-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="4e18b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="4e18b-137">Note</span><span class="sxs-lookup"><span data-stu-id="4e18b-137">NOTES</span></span>

## <span data-ttu-id="4e18b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e18b-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e18b-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="4e18b-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="4e18b-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4e18b-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="4e18b-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4e18b-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


