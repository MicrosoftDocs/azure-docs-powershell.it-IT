---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863746"
---
# <span data-ttu-id="72c47-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="72c47-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="72c47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72c47-102">SYNOPSIS</span></span>
<span data-ttu-id="72c47-103">Ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="72c47-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="72c47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72c47-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72c47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72c47-105">DESCRIPTION</span></span>
<span data-ttu-id="72c47-106">Il cmdlet **Get-AzVMExtensionImage** ottiene tutte le versioni per un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="72c47-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="72c47-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72c47-107">EXAMPLES</span></span>

### <span data-ttu-id="72c47-108">Esempio 1: ottenere le versioni di un'immagine di estensione</span><span class="sxs-lookup"><span data-stu-id="72c47-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="72c47-109">Questo comando consente di ottenere tutte le versioni dell'immagine dell'estensione per la posizione, l'editore e il tipo specificati.</span><span class="sxs-lookup"><span data-stu-id="72c47-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="72c47-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72c47-110">PARAMETERS</span></span>

### <span data-ttu-id="72c47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c47-111">-DefaultProfile</span></span>
<span data-ttu-id="72c47-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72c47-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="72c47-113">-FilterExpression</span></span>
<span data-ttu-id="72c47-114">Specifica un'espressione di filtro.</span><span class="sxs-lookup"><span data-stu-id="72c47-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="72c47-115">-Location</span></span>
<span data-ttu-id="72c47-116">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="72c47-116">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="72c47-117">-PublisherName</span></span>
<span data-ttu-id="72c47-118">Specifica il nome di un Publisher di estensione.</span><span class="sxs-lookup"><span data-stu-id="72c47-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="72c47-119">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="72c47-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="72c47-120">-Type</span></span>
<span data-ttu-id="72c47-121">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="72c47-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="72c47-122">Per ottenere un tipo di estensione, usare il cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="72c47-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="72c47-123">-Version</span></span>
<span data-ttu-id="72c47-124">Specifica la versione dell'estensione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="72c47-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c47-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c47-125">CommonParameters</span></span>
<span data-ttu-id="72c47-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c47-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c47-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c47-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c47-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72c47-128">INPUTS</span></span>

### <span data-ttu-id="72c47-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72c47-129">None</span></span>
<span data-ttu-id="72c47-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="72c47-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72c47-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72c47-131">OUTPUTS</span></span>

### <span data-ttu-id="72c47-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="72c47-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="72c47-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="72c47-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="72c47-134">Note</span><span class="sxs-lookup"><span data-stu-id="72c47-134">NOTES</span></span>

## <span data-ttu-id="72c47-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72c47-135">RELATED LINKS</span></span>

[<span data-ttu-id="72c47-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="72c47-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="72c47-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="72c47-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="72c47-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="72c47-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


