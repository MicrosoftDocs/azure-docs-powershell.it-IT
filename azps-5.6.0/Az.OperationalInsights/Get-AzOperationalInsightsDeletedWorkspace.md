---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: a4ac55c3c00ba35fa53f6e9a338712d02e507ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976510"
---
# <span data-ttu-id="e945d-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="e945d-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="e945d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e945d-102">SYNOPSIS</span></span>
<span data-ttu-id="e945d-103">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e945d-103">List deleted workspaces.</span></span>

## <span data-ttu-id="e945d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e945d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e945d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e945d-105">DESCRIPTION</span></span>
<span data-ttu-id="e945d-106">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e945d-106">List deleted workspaces.</span></span>

## <span data-ttu-id="e945d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e945d-107">EXAMPLES</span></span>

### <span data-ttu-id="e945d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e945d-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="e945d-109">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e945d-109">List deleted workspaces.</span></span>

## <span data-ttu-id="e945d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e945d-110">PARAMETERS</span></span>

### <span data-ttu-id="e945d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e945d-111">-DefaultProfile</span></span>
<span data-ttu-id="e945d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e945d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e945d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e945d-113">-ResourceGroupName</span></span>
<span data-ttu-id="e945d-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e945d-114">The resource group name.</span></span>

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

### <span data-ttu-id="e945d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e945d-115">CommonParameters</span></span>
<span data-ttu-id="e945d-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e945d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e945d-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e945d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e945d-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="e945d-118">INPUTS</span></span>

### <span data-ttu-id="e945d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="e945d-119">System.String</span></span>

## <span data-ttu-id="e945d-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e945d-120">OUTPUTS</span></span>

### <span data-ttu-id="e945d-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e945d-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e945d-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="e945d-122">NOTES</span></span>

## <span data-ttu-id="e945d-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e945d-123">RELATED LINKS</span></span>
