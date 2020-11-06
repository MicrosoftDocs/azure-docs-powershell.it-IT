---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 22f77bfc5802527103dd0e391a11e16833696abd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518859"
---
# <span data-ttu-id="68a74-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="68a74-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="68a74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68a74-102">SYNOPSIS</span></span>
<span data-ttu-id="68a74-103">Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="68a74-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68a74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68a74-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68a74-105">DESCRIPTION</span></span>
<span data-ttu-id="68a74-106">Il cmdlet **Get-AzureRmVMUsage** Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="68a74-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="68a74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68a74-107">EXAMPLES</span></span>

### <span data-ttu-id="68a74-108">Esempio 1: ottenere l'utilizzo del numero di base per una posizione</span><span class="sxs-lookup"><span data-stu-id="68a74-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="68a74-109">Questo comando ottiene l'utilizzo del numero di core della macchina virtuale per l'ubicazione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="68a74-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="68a74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68a74-110">PARAMETERS</span></span>

### <span data-ttu-id="68a74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a74-111">-DefaultProfile</span></span>
<span data-ttu-id="68a74-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68a74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68a74-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="68a74-113">-Location</span></span>
<span data-ttu-id="68a74-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="68a74-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68a74-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a74-115">CommonParameters</span></span>
<span data-ttu-id="68a74-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a74-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a74-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a74-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a74-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68a74-118">INPUTS</span></span>

### <span data-ttu-id="68a74-119">System. String</span><span class="sxs-lookup"><span data-stu-id="68a74-119">System.String</span></span>

## <span data-ttu-id="68a74-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68a74-120">OUTPUTS</span></span>

### <span data-ttu-id="68a74-121">Microsoft. Azure. Commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="68a74-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="68a74-122">Note</span><span class="sxs-lookup"><span data-stu-id="68a74-122">NOTES</span></span>

## <span data-ttu-id="68a74-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68a74-123">RELATED LINKS</span></span>

[<span data-ttu-id="68a74-124">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="68a74-124">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


