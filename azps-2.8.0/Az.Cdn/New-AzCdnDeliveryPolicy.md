---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 9dcb9720c194fbad4e82607f50132c9bbc5415c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675548"
---
# <span data-ttu-id="eb66e-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="eb66e-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="eb66e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb66e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb66e-103">Crea un criterio di recapito.</span><span class="sxs-lookup"><span data-stu-id="eb66e-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="eb66e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb66e-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb66e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb66e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb66e-106">Il cmdlet **New-AzCdnDeliveryPolicy** crea un criterio di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="eb66e-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="eb66e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb66e-107">EXAMPLES</span></span>

### <span data-ttu-id="eb66e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb66e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="eb66e-109">Creare un criterio di recapito di esempio</span><span class="sxs-lookup"><span data-stu-id="eb66e-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="eb66e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb66e-110">PARAMETERS</span></span>

### <span data-ttu-id="eb66e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb66e-111">-DefaultProfile</span></span>
<span data-ttu-id="eb66e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb66e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb66e-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb66e-113">-Description</span></span>
<span data-ttu-id="eb66e-114">Descrizione del criterio</span><span class="sxs-lookup"><span data-stu-id="eb66e-114">Description of the policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb66e-115">-Regola</span><span class="sxs-lookup"><span data-stu-id="eb66e-115">-Rule</span></span>
<span data-ttu-id="eb66e-116">Un elenco di deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="eb66e-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb66e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb66e-117">CommonParameters</span></span>
<span data-ttu-id="eb66e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb66e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb66e-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb66e-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb66e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb66e-120">INPUTS</span></span>

### <span data-ttu-id="eb66e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eb66e-121">None</span></span>

## <span data-ttu-id="eb66e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb66e-122">OUTPUTS</span></span>

### <span data-ttu-id="eb66e-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="eb66e-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="eb66e-124">Note</span><span class="sxs-lookup"><span data-stu-id="eb66e-124">NOTES</span></span>

## <span data-ttu-id="eb66e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb66e-125">RELATED LINKS</span></span>
