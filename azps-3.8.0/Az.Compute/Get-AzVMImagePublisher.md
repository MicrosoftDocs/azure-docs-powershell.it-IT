---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020841"
---
# <span data-ttu-id="2c2f6-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2c2f6-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="2c2f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2f6-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="2c2f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c2f6-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c2f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="2c2f6-106">Il cmdlet **Get-AzVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="2c2f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="2c2f6-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="2c2f6-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="2c2f6-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="2c2f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c2f6-110">PARAMETERS</span></span>

### <span data-ttu-id="2c2f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2f6-111">-DefaultProfile</span></span>
<span data-ttu-id="2c2f6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2f6-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2c2f6-113">-Location</span></span>
<span data-ttu-id="2c2f6-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="2c2f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2f6-115">CommonParameters</span></span>
<span data-ttu-id="2c2f6-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c2f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2f6-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c2f6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2f6-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c2f6-118">INPUTS</span></span>

### <span data-ttu-id="2c2f6-119">System. String</span><span class="sxs-lookup"><span data-stu-id="2c2f6-119">System.String</span></span>

## <span data-ttu-id="2c2f6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c2f6-120">OUTPUTS</span></span>

### <span data-ttu-id="2c2f6-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2c2f6-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="2c2f6-122">Note</span><span class="sxs-lookup"><span data-stu-id="2c2f6-122">NOTES</span></span>

## <span data-ttu-id="2c2f6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c2f6-123">RELATED LINKS</span></span>

[<span data-ttu-id="2c2f6-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2c2f6-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="2c2f6-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2c2f6-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2c2f6-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2c2f6-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2c2f6-127">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2c2f6-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


