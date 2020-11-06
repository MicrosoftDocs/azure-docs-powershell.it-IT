---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521268"
---
# <span data-ttu-id="c569c-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c569c-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="c569c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c569c-102">SYNOPSIS</span></span>
<span data-ttu-id="c569c-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="c569c-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c569c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c569c-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c569c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c569c-105">DESCRIPTION</span></span>
<span data-ttu-id="c569c-106">Il cmdlet **Get-AzureRmVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="c569c-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="c569c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c569c-107">EXAMPLES</span></span>

### <span data-ttu-id="c569c-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="c569c-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="c569c-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="c569c-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="c569c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c569c-110">PARAMETERS</span></span>

### <span data-ttu-id="c569c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c569c-111">-DefaultProfile</span></span>
<span data-ttu-id="c569c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c569c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c569c-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c569c-113">-Location</span></span>
<span data-ttu-id="c569c-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="c569c-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c569c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c569c-115">CommonParameters</span></span>
<span data-ttu-id="c569c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c569c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c569c-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c569c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c569c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c569c-118">INPUTS</span></span>

## <span data-ttu-id="c569c-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c569c-119">OUTPUTS</span></span>

## <span data-ttu-id="c569c-120">Note</span><span class="sxs-lookup"><span data-stu-id="c569c-120">NOTES</span></span>

## <span data-ttu-id="c569c-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c569c-121">RELATED LINKS</span></span>

[<span data-ttu-id="c569c-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c569c-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c569c-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c569c-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="c569c-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c569c-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c569c-125">Salva-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c569c-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


