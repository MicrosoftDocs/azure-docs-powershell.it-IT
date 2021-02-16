---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179231"
---
# <span data-ttu-id="43a1c-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="43a1c-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="43a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="43a1c-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43a1c-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="43a1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43a1c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a1c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="43a1c-106">Il cmdlet **Get-AzOperationalInsightsSchema restituisce** lo schema associato all'area di lavoro specificata all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43a1c-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="43a1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="43a1c-108">Esempio 1: Ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="43a1c-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="43a1c-109">Questo comando recupera gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43a1c-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="43a1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="43a1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a1c-111">-DefaultProfile</span></span>
<span data-ttu-id="43a1c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="43a1c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43a1c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a1c-113">-ResourceGroupName</span></span>
<span data-ttu-id="43a1c-114">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43a1c-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="43a1c-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43a1c-115">-WorkspaceName</span></span>
<span data-ttu-id="43a1c-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43a1c-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="43a1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a1c-117">CommonParameters</span></span>
<span data-ttu-id="43a1c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a1c-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a1c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a1c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="43a1c-120">INPUTS</span></span>

### <span data-ttu-id="43a1c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="43a1c-121">System.String</span></span>

## <span data-ttu-id="43a1c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43a1c-122">OUTPUTS</span></span>

### <span data-ttu-id="43a1c-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="43a1c-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="43a1c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="43a1c-124">NOTES</span></span>

## <span data-ttu-id="43a1c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43a1c-125">RELATED LINKS</span></span>

[<span data-ttu-id="43a1c-126">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="43a1c-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


