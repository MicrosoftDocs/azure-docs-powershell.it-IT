---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 7f177b94b851f1a3702a153032c715f81badbcc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008685"
---
# <span data-ttu-id="66172-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="66172-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="66172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66172-102">SYNOPSIS</span></span>
<span data-ttu-id="66172-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66172-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="66172-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66172-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66172-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66172-105">DESCRIPTION</span></span>
<span data-ttu-id="66172-106">Il cmdlet **Get-AzOperationalInsightsSchema** restituisce lo schema associato all'area di lavoro specificata all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66172-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="66172-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66172-107">EXAMPLES</span></span>

### <span data-ttu-id="66172-108">Esempio 1: Ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="66172-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="66172-109">Questo comando recupera gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66172-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="66172-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66172-110">PARAMETERS</span></span>

### <span data-ttu-id="66172-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66172-111">-DefaultProfile</span></span>
<span data-ttu-id="66172-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="66172-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66172-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66172-113">-ResourceGroupName</span></span>
<span data-ttu-id="66172-114">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66172-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66172-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66172-115">-WorkspaceName</span></span>
<span data-ttu-id="66172-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66172-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66172-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66172-117">CommonParameters</span></span>
<span data-ttu-id="66172-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66172-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66172-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66172-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66172-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="66172-120">INPUTS</span></span>

### <span data-ttu-id="66172-121">System.String</span><span class="sxs-lookup"><span data-stu-id="66172-121">System.String</span></span>

## <span data-ttu-id="66172-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66172-122">OUTPUTS</span></span>

### <span data-ttu-id="66172-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="66172-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="66172-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="66172-124">NOTES</span></span>

## <span data-ttu-id="66172-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66172-125">RELATED LINKS</span></span>

[<span data-ttu-id="66172-126">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="66172-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


