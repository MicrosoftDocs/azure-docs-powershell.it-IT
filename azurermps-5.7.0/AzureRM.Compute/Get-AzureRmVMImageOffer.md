---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521089"
---
# <span data-ttu-id="0ac6d-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0ac6d-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="0ac6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ac6d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac6d-103">Ottiene i tipi di offerta di VMImage.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ac6d-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## <span data-ttu-id="0ac6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ac6d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac6d-106">Il cmdlet **Get-AzureRmVMImageOffer** ottiene i tipi di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="0ac6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ac6d-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac6d-108">Esempio 1: ottenere tipi di offerta per un autore</span><span class="sxs-lookup"><span data-stu-id="0ac6d-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="0ac6d-109">Questo comando consente di ottenere i tipi di offerta per l'autore specificato nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="0ac6d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ac6d-110">PARAMETERS</span></span>

### <span data-ttu-id="0ac6d-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0ac6d-111">-Location</span></span>
<span data-ttu-id="0ac6d-112">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="0ac6d-113">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="0ac6d-113">-PublisherName</span></span>
<span data-ttu-id="0ac6d-114">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-114">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="0ac6d-115">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-115">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="0ac6d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac6d-116">CommonParameters</span></span>
<span data-ttu-id="0ac6d-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac6d-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac6d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac6d-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ac6d-119">INPUTS</span></span>

### <span data-ttu-id="0ac6d-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ac6d-120">None</span></span>
<span data-ttu-id="0ac6d-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ac6d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ac6d-122">OUTPUTS</span></span>

## <span data-ttu-id="0ac6d-123">Note</span><span class="sxs-lookup"><span data-stu-id="0ac6d-123">NOTES</span></span>

## <span data-ttu-id="0ac6d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ac6d-124">RELATED LINKS</span></span>

[<span data-ttu-id="0ac6d-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0ac6d-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="0ac6d-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0ac6d-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0ac6d-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0ac6d-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="0ac6d-128">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0ac6d-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


