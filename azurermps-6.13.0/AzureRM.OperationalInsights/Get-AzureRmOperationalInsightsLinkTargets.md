---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511620"
---
# <span data-ttu-id="c3df0-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="c3df0-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="c3df0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3df0-102">SYNOPSIS</span></span>
<span data-ttu-id="c3df0-103">Ottiene gli account che non sono associati a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c3df0-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3df0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3df0-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3df0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3df0-105">DESCRIPTION</span></span>
<span data-ttu-id="c3df0-106">Il cmdlet **Get-AzureRmOperationalInsightsLinkTargets** elenca gli account esistenti che non sono associati a un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c3df0-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="c3df0-107">Per collegare una nuova area di lavoro a un account esistente, utilizzare un ID cliente restituito da questa operazione nella proprietà ID cliente di una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c3df0-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="c3df0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3df0-108">EXAMPLES</span></span>

### <span data-ttu-id="c3df0-109">Esempio 1: ottenere gli account non collegati</span><span class="sxs-lookup"><span data-stu-id="c3df0-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="c3df0-110">Questo comando ottiene gli account non collegati che appartengono all'ID del chiamante.</span><span class="sxs-lookup"><span data-stu-id="c3df0-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="c3df0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3df0-111">PARAMETERS</span></span>

### <span data-ttu-id="c3df0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3df0-112">-DefaultProfile</span></span>
<span data-ttu-id="c3df0-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3df0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3df0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3df0-114">CommonParameters</span></span>
<span data-ttu-id="c3df0-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3df0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3df0-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3df0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3df0-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3df0-117">INPUTS</span></span>

### <span data-ttu-id="c3df0-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3df0-118">None</span></span>

## <span data-ttu-id="c3df0-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3df0-119">OUTPUTS</span></span>

### <span data-ttu-id="c3df0-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="c3df0-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="c3df0-121">Note</span><span class="sxs-lookup"><span data-stu-id="c3df0-121">NOTES</span></span>

## <span data-ttu-id="c3df0-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3df0-122">RELATED LINKS</span></span>

[<span data-ttu-id="c3df0-123">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="c3df0-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


