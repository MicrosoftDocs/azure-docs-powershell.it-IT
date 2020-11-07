---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 6a342143c8117bca1da5165ecb5a285ee6c0b686
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863741"
---
# <span data-ttu-id="9bbd5-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9bbd5-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="9bbd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbd5-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="9bbd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bbd5-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bbd5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="9bbd5-106">Il cmdlet **Get-AzVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="9bbd5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="9bbd5-108">Esempio 1: ottenere un tipo di immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="9bbd5-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9bbd5-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="9bbd5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bbd5-110">PARAMETERS</span></span>

### <span data-ttu-id="9bbd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbd5-111">-DefaultProfile</span></span>
<span data-ttu-id="9bbd5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bbd5-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9bbd5-113">-Location</span></span>
<span data-ttu-id="9bbd5-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="9bbd5-115">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bbd5-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9bbd5-116">-PublisherName</span></span>
<span data-ttu-id="9bbd5-117">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="9bbd5-118">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="9bbd5-119">Questo cmdlet ottiene il tipo per un'estensione dall'editore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bbd5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbd5-120">CommonParameters</span></span>
<span data-ttu-id="9bbd5-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbd5-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bbd5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbd5-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bbd5-123">INPUTS</span></span>

### <span data-ttu-id="9bbd5-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9bbd5-124">None</span></span>
<span data-ttu-id="9bbd5-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9bbd5-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bbd5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bbd5-126">OUTPUTS</span></span>

### <span data-ttu-id="9bbd5-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9bbd5-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="9bbd5-128">Note</span><span class="sxs-lookup"><span data-stu-id="9bbd5-128">NOTES</span></span>

## <span data-ttu-id="9bbd5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bbd5-129">RELATED LINKS</span></span>

[<span data-ttu-id="9bbd5-130">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9bbd5-130">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="9bbd5-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9bbd5-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


