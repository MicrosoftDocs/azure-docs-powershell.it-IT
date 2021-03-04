---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989153"
---
# <span data-ttu-id="2e773-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="2e773-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="2e773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e773-102">SYNOPSIS</span></span>
<span data-ttu-id="2e773-103">Ottiene risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2e773-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="2e773-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e773-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e773-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e773-105">DESCRIPTION</span></span>
<span data-ttu-id="2e773-106">Il cmdlet **Get-AzPolicyRemediation** ottiene tutte le risorse dei metadati dei criteri o una particolare risorsa metadati dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2e773-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="2e773-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e773-107">EXAMPLES</span></span>

### <span data-ttu-id="2e773-108">Esempio 1: Ottenere tutte le risorse sui metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2e773-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="2e773-109">Questo comando recupera tutte le risorse per i metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2e773-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="2e773-110">Esempio 2: Ottenere una raccolta di 10 risorse sui metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2e773-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="2e773-111">Questo comando ottiene una raccolta di 10 risorse sui metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2e773-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="2e773-112">Esempio 3: Ottenere una singola risorsa metadati criterio con il nome 'ACF1348'</span><span class="sxs-lookup"><span data-stu-id="2e773-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="2e773-113">Questo comando ottiene una singola risorsa metadati criterio con il nome 'ACF1348'</span><span class="sxs-lookup"><span data-stu-id="2e773-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="2e773-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e773-114">PARAMETERS</span></span>

### <span data-ttu-id="2e773-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e773-115">-DefaultProfile</span></span>
<span data-ttu-id="2e773-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e773-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e773-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e773-117">-Name</span></span>
<span data-ttu-id="2e773-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e773-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e773-119">-In alto</span><span class="sxs-lookup"><span data-stu-id="2e773-119">-Top</span></span>
<span data-ttu-id="2e773-120">Numero massimo di risorse metadati dei criteri da restituire.</span><span class="sxs-lookup"><span data-stu-id="2e773-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e773-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e773-121">CommonParameters</span></span>
<span data-ttu-id="2e773-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e773-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e773-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e773-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e773-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e773-124">INPUTS</span></span>

### <span data-ttu-id="2e773-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2e773-125">System.String</span></span>

## <span data-ttu-id="2e773-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e773-126">OUTPUTS</span></span>

### <span data-ttu-id="2e773-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="2e773-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="2e773-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e773-128">NOTES</span></span>

## <span data-ttu-id="2e773-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e773-129">RELATED LINKS</span></span>
