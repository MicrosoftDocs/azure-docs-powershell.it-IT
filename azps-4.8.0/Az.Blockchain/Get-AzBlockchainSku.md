---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033513"
---
# <span data-ttu-id="d76a8-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="d76a8-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="d76a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d76a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d76a8-103">Elenca gli SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d76a8-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="d76a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d76a8-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d76a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d76a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d76a8-106">Elenca gli SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d76a8-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="d76a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d76a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d76a8-108">Esempio 1: elenco SKU per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="d76a8-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="d76a8-109">Questo comando elenca SKU per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d76a8-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="d76a8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d76a8-110">PARAMETERS</span></span>

### <span data-ttu-id="d76a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76a8-111">-DefaultProfile</span></span>
<span data-ttu-id="d76a8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76a8-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d76a8-113">-SubscriptionId</span></span>
<span data-ttu-id="d76a8-114">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a8-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d76a8-115">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d76a8-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d76a8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76a8-116">CommonParameters</span></span>
<span data-ttu-id="d76a8-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76a8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76a8-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76a8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76a8-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d76a8-119">INPUTS</span></span>

## <span data-ttu-id="d76a8-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d76a8-120">OUTPUTS</span></span>

### <span data-ttu-id="d76a8-121">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="d76a8-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="d76a8-122">Note</span><span class="sxs-lookup"><span data-stu-id="d76a8-122">NOTES</span></span>

<span data-ttu-id="d76a8-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d76a8-123">ALIASES</span></span>

## <span data-ttu-id="d76a8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d76a8-124">RELATED LINKS</span></span>

