---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685403"
---
# <span data-ttu-id="87391-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="87391-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="87391-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87391-102">SYNOPSIS</span></span>
<span data-ttu-id="87391-103">Ottiene gli account che non sono associati a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="87391-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="87391-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87391-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87391-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87391-105">DESCRIPTION</span></span>
<span data-ttu-id="87391-106">Il cmdlet **Get-AzOperationalInsightsLinkTarget** elenca gli account esistenti che non sono associati a un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="87391-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="87391-107">Per collegare una nuova area di lavoro a un account esistente, utilizzare un ID cliente restituito da questa operazione nella proprietà ID cliente di una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="87391-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="87391-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87391-108">EXAMPLES</span></span>

### <span data-ttu-id="87391-109">Esempio 1: ottenere gli account non collegati</span><span class="sxs-lookup"><span data-stu-id="87391-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="87391-110">Questo comando ottiene gli account non collegati che appartengono all'ID del chiamante.</span><span class="sxs-lookup"><span data-stu-id="87391-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="87391-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87391-111">PARAMETERS</span></span>

### <span data-ttu-id="87391-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87391-112">-DefaultProfile</span></span>
<span data-ttu-id="87391-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="87391-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87391-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87391-114">CommonParameters</span></span>
<span data-ttu-id="87391-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87391-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87391-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87391-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87391-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87391-117">INPUTS</span></span>

### <span data-ttu-id="87391-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="87391-118">None</span></span>

## <span data-ttu-id="87391-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87391-119">OUTPUTS</span></span>

### <span data-ttu-id="87391-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="87391-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="87391-121">Note</span><span class="sxs-lookup"><span data-stu-id="87391-121">NOTES</span></span>

## <span data-ttu-id="87391-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87391-122">RELATED LINKS</span></span>

[<span data-ttu-id="87391-123">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="87391-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


