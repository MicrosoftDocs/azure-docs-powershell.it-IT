---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866383"
---
# <span data-ttu-id="1eb6d-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1eb6d-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="1eb6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1eb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb6d-103">Ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eb6d-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb6d-106">Il cmdlet **Get-AzureRmVMExtensionImageType** ottiene il tipo di un'estensione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="1eb6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eb6d-107">EXAMPLES</span></span>

### <span data-ttu-id="1eb6d-108">Esempio 1: ottenere un tipo di immagine dell'estensione</span><span class="sxs-lookup"><span data-stu-id="1eb6d-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="1eb6d-109">Questo comando ottiene il tipo di immagine dell'estensione per l'editore e la posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="1eb6d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1eb6d-110">PARAMETERS</span></span>

### <span data-ttu-id="1eb6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb6d-111">-DefaultProfile</span></span>
<span data-ttu-id="1eb6d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb6d-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1eb6d-113">-Location</span></span>
<span data-ttu-id="1eb6d-114">Specifica la posizione di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="1eb6d-115">Questo cmdlet ottiene il tipo per un'estensione nella posizione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="1eb6d-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1eb6d-116">-PublisherName</span></span>
<span data-ttu-id="1eb6d-117">Specifica il nome di un autore di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="1eb6d-118">Per ottenere un Publisher di estensione, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="1eb6d-119">Questo cmdlet ottiene il tipo per un'estensione dall'editore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="1eb6d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb6d-120">CommonParameters</span></span>
<span data-ttu-id="1eb6d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb6d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb6d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb6d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1eb6d-123">INPUTS</span></span>

### <span data-ttu-id="1eb6d-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1eb6d-124">None</span></span>
<span data-ttu-id="1eb6d-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1eb6d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1eb6d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eb6d-126">OUTPUTS</span></span>

### <span data-ttu-id="1eb6d-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1eb6d-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="1eb6d-128">Note</span><span class="sxs-lookup"><span data-stu-id="1eb6d-128">NOTES</span></span>

## <span data-ttu-id="1eb6d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eb6d-129">RELATED LINKS</span></span>

[<span data-ttu-id="1eb6d-130">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1eb6d-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="1eb6d-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1eb6d-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


