---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349204"
---
# <span data-ttu-id="ca816-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ca816-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="ca816-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca816-102">SYNOPSIS</span></span>
<span data-ttu-id="ca816-103">Ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ca816-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="ca816-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca816-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca816-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca816-105">DESCRIPTION</span></span>
<span data-ttu-id="ca816-106">Il cmdlet **Get-AzVMImagePublisher** ottiene gli editori di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ca816-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="ca816-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca816-107">EXAMPLES</span></span>

### <span data-ttu-id="ca816-108">Esempio 1: ottenere gli editori di VMImage per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="ca816-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="ca816-109">Questo comando consente di ottenere gli editori delle istanze di VMImage per l'area centrale degli Stati Uniti all'interno del profilo di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca816-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="ca816-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca816-110">PARAMETERS</span></span>

### <span data-ttu-id="ca816-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca816-111">-DefaultProfile</span></span>
<span data-ttu-id="ca816-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca816-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca816-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ca816-113">-Location</span></span>
<span data-ttu-id="ca816-114">Specifica la posizione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ca816-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="ca816-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca816-115">CommonParameters</span></span>
<span data-ttu-id="ca816-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca816-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca816-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca816-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca816-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca816-118">INPUTS</span></span>

### <span data-ttu-id="ca816-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ca816-119">System.String</span></span>

## <span data-ttu-id="ca816-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca816-120">OUTPUTS</span></span>

### <span data-ttu-id="ca816-121">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ca816-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="ca816-122">Note</span><span class="sxs-lookup"><span data-stu-id="ca816-122">NOTES</span></span>

## <span data-ttu-id="ca816-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca816-123">RELATED LINKS</span></span>

[<span data-ttu-id="ca816-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ca816-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ca816-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ca816-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="ca816-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ca816-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ca816-127">Salva-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ca816-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


