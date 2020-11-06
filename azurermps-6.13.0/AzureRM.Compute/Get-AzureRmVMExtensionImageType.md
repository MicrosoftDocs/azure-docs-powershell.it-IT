---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516676"
---
# <span data-ttu-id="371be-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="371be-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="371be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="371be-102">SYNOPSIS</span></span>
<span data-ttu-id="371be-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="371be-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="371be-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="371be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="371be-105">DESCRIPTION</span></span>
<span data-ttu-id="371be-106">Il cmdlet **Get-AzureRmVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="371be-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="371be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="371be-107">EXAMPLES</span></span>

### <span data-ttu-id="371be-108">Esempio 1: ottenere un tipo di immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="371be-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="371be-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="371be-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="371be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="371be-110">PARAMETERS</span></span>

### <span data-ttu-id="371be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371be-111">-DefaultProfile</span></span>
<span data-ttu-id="371be-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="371be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="371be-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="371be-113">-Location</span></span>
<span data-ttu-id="371be-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="371be-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="371be-115">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="371be-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="371be-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="371be-116">-PublisherName</span></span>
<span data-ttu-id="371be-117">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="371be-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="371be-118">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="371be-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="371be-119">Questo cmdlet ottiene il tipo per un'estensione dall'editore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="371be-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="371be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371be-120">CommonParameters</span></span>
<span data-ttu-id="371be-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371be-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371be-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="371be-123">INPUTS</span></span>

### <span data-ttu-id="371be-124">System. String</span><span class="sxs-lookup"><span data-stu-id="371be-124">System.String</span></span>

## <span data-ttu-id="371be-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="371be-125">OUTPUTS</span></span>

### <span data-ttu-id="371be-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="371be-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="371be-127">Note</span><span class="sxs-lookup"><span data-stu-id="371be-127">NOTES</span></span>

## <span data-ttu-id="371be-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="371be-128">RELATED LINKS</span></span>

[<span data-ttu-id="371be-129">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="371be-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="371be-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="371be-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


