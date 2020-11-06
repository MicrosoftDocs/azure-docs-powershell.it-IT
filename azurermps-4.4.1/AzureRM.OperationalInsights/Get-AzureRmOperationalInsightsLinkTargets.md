---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520010"
---
# <span data-ttu-id="2332c-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="2332c-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="2332c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2332c-102">SYNOPSIS</span></span>
<span data-ttu-id="2332c-103">Ottiene gli account che non sono associati a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2332c-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2332c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2332c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2332c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2332c-105">DESCRIPTION</span></span>
<span data-ttu-id="2332c-106">Il cmdlet **Get-AzureRmOperationalInsightsLinkTargets** elenca gli account esistenti che non sono associati a un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="2332c-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="2332c-107">Per collegare una nuova area di lavoro a un account esistente, utilizzare un ID cliente restituito da questa operazione nella proprietà ID cliente di una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2332c-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="2332c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2332c-108">EXAMPLES</span></span>

### <span data-ttu-id="2332c-109">Esempio 1: ottenere gli account non collegati</span><span class="sxs-lookup"><span data-stu-id="2332c-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="2332c-110">Questo comando ottiene gli account non collegati che appartengono all'ID del chiamante.</span><span class="sxs-lookup"><span data-stu-id="2332c-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="2332c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2332c-111">PARAMETERS</span></span>

### <span data-ttu-id="2332c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2332c-112">-DefaultProfile</span></span>
<span data-ttu-id="2332c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2332c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2332c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2332c-114">CommonParameters</span></span>
<span data-ttu-id="2332c-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2332c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2332c-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2332c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2332c-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2332c-117">INPUTS</span></span>

## <span data-ttu-id="2332c-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2332c-118">OUTPUTS</span></span>

### <span data-ttu-id="2332c-119">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="2332c-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="2332c-120">Note</span><span class="sxs-lookup"><span data-stu-id="2332c-120">NOTES</span></span>

## <span data-ttu-id="2332c-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2332c-121">RELATED LINKS</span></span>

[<span data-ttu-id="2332c-122">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="2332c-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


