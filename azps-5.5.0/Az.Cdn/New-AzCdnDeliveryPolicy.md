---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177879"
---
# <span data-ttu-id="81ecb-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="81ecb-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="81ecb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="81ecb-103">Crea criteri di recapito.</span><span class="sxs-lookup"><span data-stu-id="81ecb-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="81ecb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81ecb-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ecb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="81ecb-106">Il cmdlet **New-AzCdnDeliveryPolicy** crea un criterio di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="81ecb-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="81ecb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="81ecb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81ecb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="81ecb-109">Creare criteri di recapito di esempio</span><span class="sxs-lookup"><span data-stu-id="81ecb-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="81ecb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81ecb-110">PARAMETERS</span></span>

### <span data-ttu-id="81ecb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ecb-111">-DefaultProfile</span></span>
<span data-ttu-id="81ecb-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81ecb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81ecb-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="81ecb-113">-Description</span></span>
<span data-ttu-id="81ecb-114">Descrizione del criterio</span><span class="sxs-lookup"><span data-stu-id="81ecb-114">Description of the policy</span></span>

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

### <span data-ttu-id="81ecb-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="81ecb-115">-Rule</span></span>
<span data-ttu-id="81ecb-116">Elenco delle regole di recapito.</span><span class="sxs-lookup"><span data-stu-id="81ecb-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="81ecb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ecb-117">CommonParameters</span></span>
<span data-ttu-id="81ecb-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ecb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ecb-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81ecb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ecb-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="81ecb-120">INPUTS</span></span>

### <span data-ttu-id="81ecb-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="81ecb-121">None</span></span>

## <span data-ttu-id="81ecb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81ecb-122">OUTPUTS</span></span>

### <span data-ttu-id="81ecb-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="81ecb-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="81ecb-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="81ecb-124">NOTES</span></span>

## <span data-ttu-id="81ecb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81ecb-125">RELATED LINKS</span></span>
