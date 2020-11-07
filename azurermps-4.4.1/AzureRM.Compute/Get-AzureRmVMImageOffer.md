---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688035"
---
# <span data-ttu-id="68631-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="68631-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="68631-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68631-102">SYNOPSIS</span></span>
<span data-ttu-id="68631-103">Ottiene i tipi di offerta di VMImage.</span><span class="sxs-lookup"><span data-stu-id="68631-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68631-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68631-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68631-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68631-105">DESCRIPTION</span></span>
<span data-ttu-id="68631-106">Il cmdlet **Get-AzureRmVMImageOffer** ottiene i tipi di offerta VMImage.</span><span class="sxs-lookup"><span data-stu-id="68631-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="68631-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68631-107">EXAMPLES</span></span>

### <span data-ttu-id="68631-108">Esempio 1: ottenere tipi di offerta per un autore</span><span class="sxs-lookup"><span data-stu-id="68631-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="68631-109">Questo comando consente di ottenere i tipi di offerta per l'autore specificato nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="68631-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="68631-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68631-110">PARAMETERS</span></span>

### <span data-ttu-id="68631-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68631-111">-DefaultProfile</span></span>
<span data-ttu-id="68631-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68631-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68631-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="68631-113">-Location</span></span>
<span data-ttu-id="68631-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="68631-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="68631-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="68631-115">-PublisherName</span></span>
<span data-ttu-id="68631-116">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="68631-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="68631-117">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="68631-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="68631-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68631-118">CommonParameters</span></span>
<span data-ttu-id="68631-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68631-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68631-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68631-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68631-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68631-121">INPUTS</span></span>

## <span data-ttu-id="68631-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68631-122">OUTPUTS</span></span>

## <span data-ttu-id="68631-123">Note</span><span class="sxs-lookup"><span data-stu-id="68631-123">NOTES</span></span>

## <span data-ttu-id="68631-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68631-124">RELATED LINKS</span></span>

[<span data-ttu-id="68631-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="68631-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="68631-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="68631-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="68631-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="68631-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="68631-128">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="68631-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


