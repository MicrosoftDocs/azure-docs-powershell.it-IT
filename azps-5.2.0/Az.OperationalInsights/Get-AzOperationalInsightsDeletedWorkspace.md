---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338596"
---
# <span data-ttu-id="e776e-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="e776e-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="e776e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e776e-102">SYNOPSIS</span></span>
<span data-ttu-id="e776e-103">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e776e-103">List deleted workspaces.</span></span>

## <span data-ttu-id="e776e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e776e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e776e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e776e-105">DESCRIPTION</span></span>
<span data-ttu-id="e776e-106">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e776e-106">List deleted workspaces.</span></span>

## <span data-ttu-id="e776e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e776e-107">EXAMPLES</span></span>

### <span data-ttu-id="e776e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e776e-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="e776e-109">Elencare le aree di lavoro eliminate.</span><span class="sxs-lookup"><span data-stu-id="e776e-109">List deleted workspaces.</span></span>

## <span data-ttu-id="e776e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e776e-110">PARAMETERS</span></span>

### <span data-ttu-id="e776e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e776e-111">-DefaultProfile</span></span>
<span data-ttu-id="e776e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e776e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e776e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e776e-113">-ResourceGroupName</span></span>
<span data-ttu-id="e776e-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e776e-114">The resource group name.</span></span>

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

### <span data-ttu-id="e776e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e776e-115">CommonParameters</span></span>
<span data-ttu-id="e776e-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e776e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e776e-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e776e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e776e-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e776e-118">INPUTS</span></span>

### <span data-ttu-id="e776e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e776e-119">System.String</span></span>

## <span data-ttu-id="e776e-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e776e-120">OUTPUTS</span></span>

### <span data-ttu-id="e776e-121">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e776e-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e776e-122">Note</span><span class="sxs-lookup"><span data-stu-id="e776e-122">NOTES</span></span>

## <span data-ttu-id="e776e-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e776e-123">RELATED LINKS</span></span>
