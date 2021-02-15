---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200671"
---
# <span data-ttu-id="01464-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="01464-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="01464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01464-102">SYNOPSIS</span></span>
<span data-ttu-id="01464-103">Ottiene l'utilizzo del numero di core per le macchine virtuali per una posizione.</span><span class="sxs-lookup"><span data-stu-id="01464-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="01464-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01464-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01464-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01464-105">DESCRIPTION</span></span>
<span data-ttu-id="01464-106">Il cmdlet **Get-AzVMUsage** ottiene l'utilizzo del numero di core per le macchine virtuali per una posizione.</span><span class="sxs-lookup"><span data-stu-id="01464-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="01464-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01464-107">EXAMPLES</span></span>

### <span data-ttu-id="01464-108">Esempio 1: Ottenere l'utilizzo del numero principale per una posizione</span><span class="sxs-lookup"><span data-stu-id="01464-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="01464-109">Questo comando recupera l'utilizzo del numero di core della macchina virtuale per la posizione Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="01464-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="01464-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01464-110">PARAMETERS</span></span>

### <span data-ttu-id="01464-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01464-111">-DefaultProfile</span></span>
<span data-ttu-id="01464-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01464-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01464-113">-Location</span><span class="sxs-lookup"><span data-stu-id="01464-113">-Location</span></span>
<span data-ttu-id="01464-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="01464-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="01464-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01464-115">CommonParameters</span></span>
<span data-ttu-id="01464-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01464-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01464-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01464-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01464-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="01464-118">INPUTS</span></span>

### <span data-ttu-id="01464-119">System.String</span><span class="sxs-lookup"><span data-stu-id="01464-119">System.String</span></span>

## <span data-ttu-id="01464-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01464-120">OUTPUTS</span></span>

### <span data-ttu-id="01464-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="01464-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="01464-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="01464-122">NOTES</span></span>

## <span data-ttu-id="01464-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01464-123">RELATED LINKS</span></span>

[<span data-ttu-id="01464-124">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="01464-124">Get-AzVM</span></span>](./Get-AzVM.md)


