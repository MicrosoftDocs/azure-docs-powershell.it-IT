---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522047"
---
# <span data-ttu-id="57fc6-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="57fc6-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="57fc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="57fc6-103">Ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="57fc6-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57fc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57fc6-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57fc6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="57fc6-106">Il cmdlet **Get-AzureRmVMExtensionImage** ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="57fc6-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="57fc6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="57fc6-108">Esempio 1: ottenere le versioni di un'immagine di estensione</span><span class="sxs-lookup"><span data-stu-id="57fc6-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="57fc6-109">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore e il tipo specificati.</span><span class="sxs-lookup"><span data-stu-id="57fc6-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="57fc6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="57fc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fc6-111">-DefaultProfile</span></span>
<span data-ttu-id="57fc6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57fc6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57fc6-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="57fc6-113">-FilterExpression</span></span>
<span data-ttu-id="57fc6-114">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="57fc6-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="57fc6-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="57fc6-115">-Location</span></span>
<span data-ttu-id="57fc6-116">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="57fc6-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="57fc6-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="57fc6-117">-PublisherName</span></span>
<span data-ttu-id="57fc6-118">Specifica il nome di un Publisher di estensione.</span><span class="sxs-lookup"><span data-stu-id="57fc6-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="57fc6-119">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="57fc6-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="57fc6-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="57fc6-120">-Type</span></span>
<span data-ttu-id="57fc6-121">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="57fc6-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="57fc6-122">Per ottenere un tipo di estensione, usare il cmdlet Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="57fc6-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="57fc6-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="57fc6-123">-Version</span></span>
<span data-ttu-id="57fc6-124">Specifica la versione dell'estensione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="57fc6-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fc6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fc6-125">CommonParameters</span></span>
<span data-ttu-id="57fc6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fc6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fc6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fc6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fc6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57fc6-128">INPUTS</span></span>

### <span data-ttu-id="57fc6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="57fc6-129">System.String</span></span>

## <span data-ttu-id="57fc6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57fc6-130">OUTPUTS</span></span>

### <span data-ttu-id="57fc6-131">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="57fc6-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="57fc6-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="57fc6-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="57fc6-133">Note</span><span class="sxs-lookup"><span data-stu-id="57fc6-133">NOTES</span></span>

## <span data-ttu-id="57fc6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57fc6-134">RELATED LINKS</span></span>

[<span data-ttu-id="57fc6-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="57fc6-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="57fc6-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="57fc6-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="57fc6-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="57fc6-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


