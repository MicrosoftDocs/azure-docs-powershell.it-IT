---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867150"
---
# <span data-ttu-id="b85a6-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="b85a6-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="b85a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b85a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b85a6-103">Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="b85a6-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b85a6-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b85a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b85a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b85a6-106">Il cmdlet **Get-AzureRmVMUsage** Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="b85a6-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="b85a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b85a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b85a6-108">Esempio 1: ottenere l'utilizzo del numero di base per una posizione</span><span class="sxs-lookup"><span data-stu-id="b85a6-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="b85a6-109">Questo comando ottiene l'utilizzo del numero di core della macchina virtuale per l'ubicazione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="b85a6-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="b85a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b85a6-110">PARAMETERS</span></span>

### <span data-ttu-id="b85a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85a6-111">-DefaultProfile</span></span>
<span data-ttu-id="b85a6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b85a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85a6-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b85a6-113">-Location</span></span>
<span data-ttu-id="b85a6-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b85a6-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="b85a6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85a6-115">CommonParameters</span></span>
<span data-ttu-id="b85a6-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85a6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85a6-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85a6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85a6-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b85a6-118">INPUTS</span></span>

### <span data-ttu-id="b85a6-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b85a6-119">None</span></span>
<span data-ttu-id="b85a6-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b85a6-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b85a6-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b85a6-121">OUTPUTS</span></span>

### <span data-ttu-id="b85a6-122">Microsoft. Azure. Commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="b85a6-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="b85a6-123">Note</span><span class="sxs-lookup"><span data-stu-id="b85a6-123">NOTES</span></span>

## <span data-ttu-id="b85a6-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b85a6-124">RELATED LINKS</span></span>

[<span data-ttu-id="b85a6-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b85a6-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


