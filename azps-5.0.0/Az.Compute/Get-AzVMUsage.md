---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193572"
---
# <span data-ttu-id="24647-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="24647-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="24647-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24647-102">SYNOPSIS</span></span>
<span data-ttu-id="24647-103">Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="24647-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="24647-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24647-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24647-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24647-105">DESCRIPTION</span></span>
<span data-ttu-id="24647-106">Il cmdlet **Get-AzVMUsage** Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="24647-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="24647-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24647-107">EXAMPLES</span></span>

### <span data-ttu-id="24647-108">Esempio 1: ottenere l'utilizzo del numero di base per una posizione</span><span class="sxs-lookup"><span data-stu-id="24647-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="24647-109">Questo comando ottiene l'utilizzo del numero di core della macchina virtuale per l'ubicazione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="24647-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="24647-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24647-110">PARAMETERS</span></span>

### <span data-ttu-id="24647-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24647-111">-DefaultProfile</span></span>
<span data-ttu-id="24647-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24647-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24647-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24647-113">-Location</span></span>
<span data-ttu-id="24647-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="24647-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="24647-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24647-115">CommonParameters</span></span>
<span data-ttu-id="24647-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24647-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24647-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24647-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24647-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24647-118">INPUTS</span></span>

### <span data-ttu-id="24647-119">System. String</span><span class="sxs-lookup"><span data-stu-id="24647-119">System.String</span></span>

## <span data-ttu-id="24647-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24647-120">OUTPUTS</span></span>

### <span data-ttu-id="24647-121">Microsoft. Azure. Commands. Compute. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="24647-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="24647-122">Note</span><span class="sxs-lookup"><span data-stu-id="24647-122">NOTES</span></span>

## <span data-ttu-id="24647-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24647-123">RELATED LINKS</span></span>

[<span data-ttu-id="24647-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="24647-124">Get-AzVM</span></span>](./Get-AzVM.md)


