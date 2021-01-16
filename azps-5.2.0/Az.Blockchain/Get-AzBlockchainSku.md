---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341899"
---
# <span data-ttu-id="dd8bd-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="dd8bd-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="dd8bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8bd-103">Elenca gli SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="dd8bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd8bd-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dd8bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8bd-106">Elenca gli SKU del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="dd8bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8bd-108">Esempio 1: elenco SKU per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="dd8bd-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="dd8bd-109">Questo comando elenca SKU per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="dd8bd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd8bd-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8bd-111">-DefaultProfile</span></span>
<span data-ttu-id="dd8bd-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8bd-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd8bd-113">-SubscriptionId</span></span>
<span data-ttu-id="dd8bd-114">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd8bd-115">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dd8bd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8bd-116">CommonParameters</span></span>
<span data-ttu-id="dd8bd-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8bd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8bd-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd8bd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8bd-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd8bd-119">INPUTS</span></span>

## <span data-ttu-id="dd8bd-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd8bd-120">OUTPUTS</span></span>

### <span data-ttu-id="dd8bd-121">Microsoft. Azure. PowerShell. Cmdlets. blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="dd8bd-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="dd8bd-122">Note</span><span class="sxs-lookup"><span data-stu-id="dd8bd-122">NOTES</span></span>

<span data-ttu-id="dd8bd-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dd8bd-123">ALIASES</span></span>

## <span data-ttu-id="dd8bd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd8bd-124">RELATED LINKS</span></span>

