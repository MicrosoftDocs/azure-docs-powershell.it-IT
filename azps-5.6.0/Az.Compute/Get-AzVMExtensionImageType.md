---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 551774d61e7887dfe115f37f67ce66fe95147406
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958989"
---
# <span data-ttu-id="a8d65-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a8d65-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="a8d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d65-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d65-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d65-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="a8d65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8d65-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d65-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8d65-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d65-106">Il cmdlet **Get-AzVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d65-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="a8d65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8d65-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d65-108">Esempio 1: Ottenere un tipo di immagine estensione</span><span class="sxs-lookup"><span data-stu-id="a8d65-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="a8d65-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="a8d65-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="a8d65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8d65-110">PARAMETERS</span></span>

### <span data-ttu-id="a8d65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d65-111">-DefaultProfile</span></span>
<span data-ttu-id="a8d65-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8d65-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a8d65-113">-Location</span></span>
<span data-ttu-id="a8d65-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="a8d65-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="a8d65-115">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a8d65-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8d65-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a8d65-116">-PublisherName</span></span>
<span data-ttu-id="a8d65-117">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="a8d65-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="a8d65-118">Per ottenere un autore dell'estensione, usare il cmdlet Get-AzVMImagePublisher estensione.</span><span class="sxs-lookup"><span data-stu-id="a8d65-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="a8d65-119">Questo cmdlet ottiene dall'autore il tipo di un'estensione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a8d65-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8d65-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d65-120">CommonParameters</span></span>
<span data-ttu-id="a8d65-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d65-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d65-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8d65-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d65-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8d65-123">INPUTS</span></span>

### <span data-ttu-id="a8d65-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a8d65-124">System.String</span></span>

## <span data-ttu-id="a8d65-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8d65-125">OUTPUTS</span></span>

### <span data-ttu-id="a8d65-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="a8d65-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="a8d65-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8d65-127">NOTES</span></span>

## <span data-ttu-id="a8d65-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8d65-128">RELATED LINKS</span></span>

[<span data-ttu-id="a8d65-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="a8d65-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="a8d65-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a8d65-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


