---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687937"
---
# <span data-ttu-id="9471b-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="9471b-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="9471b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9471b-102">SYNOPSIS</span></span>
<span data-ttu-id="9471b-103">Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="9471b-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9471b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9471b-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="9471b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9471b-105">DESCRIPTION</span></span>
<span data-ttu-id="9471b-106">Il cmdlet **Get-AzureRmVMUsage** Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="9471b-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="9471b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9471b-107">EXAMPLES</span></span>

### <span data-ttu-id="9471b-108">Esempio 1: ottenere l'utilizzo del numero di base per una posizione</span><span class="sxs-lookup"><span data-stu-id="9471b-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="9471b-109">Questo comando ottiene l'utilizzo del numero di core della macchina virtuale per l'ubicazione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="9471b-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="9471b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9471b-110">PARAMETERS</span></span>

### <span data-ttu-id="9471b-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9471b-111">-Location</span></span>
<span data-ttu-id="9471b-112">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9471b-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9471b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9471b-113">CommonParameters</span></span>
<span data-ttu-id="9471b-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9471b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9471b-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9471b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9471b-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9471b-116">INPUTS</span></span>

### <span data-ttu-id="9471b-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9471b-117">None</span></span>
<span data-ttu-id="9471b-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9471b-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9471b-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9471b-119">OUTPUTS</span></span>

## <span data-ttu-id="9471b-120">Note</span><span class="sxs-lookup"><span data-stu-id="9471b-120">NOTES</span></span>

## <span data-ttu-id="9471b-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9471b-121">RELATED LINKS</span></span>

[<span data-ttu-id="9471b-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9471b-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


