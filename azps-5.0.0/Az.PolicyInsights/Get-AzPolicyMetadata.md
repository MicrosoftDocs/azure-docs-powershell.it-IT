---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199494"
---
# <span data-ttu-id="e8429-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="e8429-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="e8429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8429-102">SYNOPSIS</span></span>
<span data-ttu-id="e8429-103">Ottiene risorse per i metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="e8429-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="e8429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8429-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8429-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8429-105">DESCRIPTION</span></span>
<span data-ttu-id="e8429-106">Il cmdlet **Get-AzPolicyRemediation** consente di ottenere tutte le risorse di metadati dei criteri o una particolare risorsa di metadati dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e8429-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="e8429-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8429-107">EXAMPLES</span></span>

### <span data-ttu-id="e8429-108">Esempio 1: ottenere tutte le risorse per i metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="e8429-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="e8429-109">Questo comando consente di ottenere tutte le risorse dei criteri</span><span class="sxs-lookup"><span data-stu-id="e8429-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="e8429-110">Esempio 2: ottenere una raccolta di 10 risorse per i metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="e8429-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="e8429-111">Questo comando ottiene una raccolta di 10 risorse per i metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="e8429-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="e8429-112">Esempio 3: ottenere una singola risorsa di metadati dei criteri con il nome "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="e8429-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="e8429-113">Questo comando consente di ottenere una singola risorsa di metadati dei criteri con il nome "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="e8429-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="e8429-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8429-114">PARAMETERS</span></span>

### <span data-ttu-id="e8429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8429-115">-DefaultProfile</span></span>
<span data-ttu-id="e8429-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8429-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8429-117">-Name</span></span>
<span data-ttu-id="e8429-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="e8429-118">Resource name.</span></span>

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

### <span data-ttu-id="e8429-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="e8429-119">-Top</span></span>
<span data-ttu-id="e8429-120">Numero massimo di risorse di metadati dei criteri da restituire.</span><span class="sxs-lookup"><span data-stu-id="e8429-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="e8429-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8429-121">CommonParameters</span></span>
<span data-ttu-id="e8429-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8429-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8429-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8429-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8429-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8429-124">INPUTS</span></span>

### <span data-ttu-id="e8429-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e8429-125">System.String</span></span>

## <span data-ttu-id="e8429-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8429-126">OUTPUTS</span></span>

### <span data-ttu-id="e8429-127">Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="e8429-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="e8429-128">Note</span><span class="sxs-lookup"><span data-stu-id="e8429-128">NOTES</span></span>

## <span data-ttu-id="e8429-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8429-129">RELATED LINKS</span></span>
