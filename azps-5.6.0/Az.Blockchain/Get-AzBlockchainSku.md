---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: 9f33eef5b9f0bd0b245c444cf869fa0ff7a0a064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971485"
---
# <span data-ttu-id="96738-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="96738-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="96738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96738-102">SYNOPSIS</span></span>
<span data-ttu-id="96738-103">Elenca le SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="96738-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="96738-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96738-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96738-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="96738-105">DESCRIPTION</span></span>
<span data-ttu-id="96738-106">Elenca le SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="96738-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="96738-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96738-107">EXAMPLES</span></span>

### <span data-ttu-id="96738-108">Esempio 1: Elencare SKU per una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="96738-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="96738-109">Questo comando elenca lo SKU per una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="96738-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="96738-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96738-110">PARAMETERS</span></span>

### <span data-ttu-id="96738-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96738-111">-DefaultProfile</span></span>
<span data-ttu-id="96738-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96738-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96738-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96738-113">-SubscriptionId</span></span>
<span data-ttu-id="96738-114">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="96738-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="96738-115">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="96738-115">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96738-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96738-116">CommonParameters</span></span>
<span data-ttu-id="96738-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96738-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96738-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96738-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96738-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="96738-119">INPUTS</span></span>

## <span data-ttu-id="96738-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96738-120">OUTPUTS</span></span>

### <span data-ttu-id="96738-121">Microsoft.Azure.PowerShell.Cmdlets.Uovo.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="96738-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="96738-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="96738-122">NOTES</span></span>

<span data-ttu-id="96738-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="96738-123">ALIASES</span></span>

## <span data-ttu-id="96738-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96738-124">RELATED LINKS</span></span>

