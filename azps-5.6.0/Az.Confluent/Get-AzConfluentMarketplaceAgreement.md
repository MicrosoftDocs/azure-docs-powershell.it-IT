---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012605"
---
# <span data-ttu-id="8117f-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="8117f-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="8117f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8117f-102">SYNOPSIS</span></span>
<span data-ttu-id="8117f-103">Elencare i contratti di Marketplace confluenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8117f-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="8117f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8117f-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8117f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8117f-105">DESCRIPTION</span></span>
<span data-ttu-id="8117f-106">Elencare i contratti di Marketplace confluenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8117f-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="8117f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8117f-107">EXAMPLES</span></span>

### <span data-ttu-id="8117f-108">Esempio 1: Elencare tutti i contratti di Marketplace confluenti in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="8117f-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="8117f-109">Questo comando elenca tutti i contratti di Marketplace confluenti in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8117f-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="8117f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8117f-110">PARAMETERS</span></span>

### <span data-ttu-id="8117f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8117f-111">-DefaultProfile</span></span>
<span data-ttu-id="8117f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8117f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8117f-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8117f-113">-SubscriptionId</span></span>
<span data-ttu-id="8117f-114">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8117f-114">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="8117f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8117f-115">CommonParameters</span></span>
<span data-ttu-id="8117f-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8117f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8117f-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8117f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8117f-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="8117f-118">INPUTS</span></span>

## <span data-ttu-id="8117f-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8117f-119">OUTPUTS</span></span>

### <span data-ttu-id="8117f-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="8117f-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="8117f-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="8117f-121">NOTES</span></span>

<span data-ttu-id="8117f-122">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8117f-122">ALIASES</span></span>

## <span data-ttu-id="8117f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8117f-123">RELATED LINKS</span></span>

