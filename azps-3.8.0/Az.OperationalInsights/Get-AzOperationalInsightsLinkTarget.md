---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: 72841dc8ecc90c14bb41ae8f0f207d990afec9a8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030733"
---
# <span data-ttu-id="a83ab-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="a83ab-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="a83ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a83ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a83ab-103">Ottiene gli account che non sono associati a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a83ab-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="a83ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a83ab-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83ab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a83ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a83ab-106">Il cmdlet **Get-AzOperationalInsightsLinkTarget** elenca gli account esistenti che non sono associati a un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="a83ab-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="a83ab-107">Per collegare una nuova area di lavoro a un account esistente, utilizzare un ID cliente restituito da questa operazione nella proprietà ID cliente di una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a83ab-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="a83ab-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a83ab-108">EXAMPLES</span></span>

### <span data-ttu-id="a83ab-109">Esempio 1: ottenere gli account non collegati</span><span class="sxs-lookup"><span data-stu-id="a83ab-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="a83ab-110">Questo comando ottiene gli account non collegati che appartengono all'ID del chiamante.</span><span class="sxs-lookup"><span data-stu-id="a83ab-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="a83ab-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a83ab-111">PARAMETERS</span></span>

### <span data-ttu-id="a83ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83ab-112">-DefaultProfile</span></span>
<span data-ttu-id="a83ab-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a83ab-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a83ab-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83ab-114">CommonParameters</span></span>
<span data-ttu-id="a83ab-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83ab-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83ab-116">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83ab-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83ab-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a83ab-117">INPUTS</span></span>

### <span data-ttu-id="a83ab-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a83ab-118">None</span></span>

## <span data-ttu-id="a83ab-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a83ab-119">OUTPUTS</span></span>

### <span data-ttu-id="a83ab-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="a83ab-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="a83ab-121">Note</span><span class="sxs-lookup"><span data-stu-id="a83ab-121">NOTES</span></span>

## <span data-ttu-id="a83ab-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a83ab-122">RELATED LINKS</span></span>

[<span data-ttu-id="a83ab-123">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="a83ab-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


