---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020844"
---
# <span data-ttu-id="518a3-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="518a3-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="518a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="518a3-102">SYNOPSIS</span></span>
<span data-ttu-id="518a3-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="518a3-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="518a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="518a3-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="518a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="518a3-105">DESCRIPTION</span></span>
<span data-ttu-id="518a3-106">Il cmdlet **Get-AzVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="518a3-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="518a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="518a3-107">EXAMPLES</span></span>

### <span data-ttu-id="518a3-108">Esempio 1: ottenere un tipo di immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="518a3-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="518a3-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="518a3-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="518a3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="518a3-110">PARAMETERS</span></span>

### <span data-ttu-id="518a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518a3-111">-DefaultProfile</span></span>
<span data-ttu-id="518a3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="518a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="518a3-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="518a3-113">-Location</span></span>
<span data-ttu-id="518a3-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="518a3-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="518a3-115">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="518a3-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="518a3-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="518a3-116">-PublisherName</span></span>
<span data-ttu-id="518a3-117">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="518a3-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="518a3-118">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="518a3-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="518a3-119">Questo cmdlet ottiene il tipo per un'estensione dall'editore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="518a3-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="518a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518a3-120">CommonParameters</span></span>
<span data-ttu-id="518a3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="518a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518a3-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="518a3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518a3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="518a3-123">INPUTS</span></span>

### <span data-ttu-id="518a3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="518a3-124">System.String</span></span>

## <span data-ttu-id="518a3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="518a3-125">OUTPUTS</span></span>

### <span data-ttu-id="518a3-126">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="518a3-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="518a3-127">Note</span><span class="sxs-lookup"><span data-stu-id="518a3-127">NOTES</span></span>

## <span data-ttu-id="518a3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="518a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="518a3-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="518a3-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="518a3-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="518a3-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


