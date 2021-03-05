---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013726"
---
# <span data-ttu-id="e57ad-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="e57ad-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="e57ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e57ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e57ad-103">Ottiene l'utilizzo del numero di core per le macchine virtuali per una posizione.</span><span class="sxs-lookup"><span data-stu-id="e57ad-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e57ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57ad-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e57ad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e57ad-105">DESCRIPTION</span></span>
<span data-ttu-id="e57ad-106">Il cmdlet **Get-AzVMUsage** ottiene l'utilizzo del numero di core per le macchine virtuali per una posizione.</span><span class="sxs-lookup"><span data-stu-id="e57ad-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e57ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57ad-107">EXAMPLES</span></span>

### <span data-ttu-id="e57ad-108">Esempio 1: Ottenere l'utilizzo del numero principale per una posizione</span><span class="sxs-lookup"><span data-stu-id="e57ad-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="e57ad-109">Questo comando recupera l'utilizzo del numero di core della macchina virtuale per la posizione Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="e57ad-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="e57ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e57ad-110">PARAMETERS</span></span>

### <span data-ttu-id="e57ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57ad-111">-DefaultProfile</span></span>
<span data-ttu-id="e57ad-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e57ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e57ad-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e57ad-113">-Location</span></span>
<span data-ttu-id="e57ad-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e57ad-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="e57ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57ad-115">CommonParameters</span></span>
<span data-ttu-id="e57ad-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57ad-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e57ad-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57ad-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="e57ad-118">INPUTS</span></span>

### <span data-ttu-id="e57ad-119">System.String</span><span class="sxs-lookup"><span data-stu-id="e57ad-119">System.String</span></span>

## <span data-ttu-id="e57ad-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57ad-120">OUTPUTS</span></span>

### <span data-ttu-id="e57ad-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="e57ad-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="e57ad-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="e57ad-122">NOTES</span></span>

## <span data-ttu-id="e57ad-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57ad-123">RELATED LINKS</span></span>

[<span data-ttu-id="e57ad-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e57ad-124">Get-AzVM</span></span>](./Get-AzVM.md)


