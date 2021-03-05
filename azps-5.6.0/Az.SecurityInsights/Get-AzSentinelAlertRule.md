---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 836d566c9e75fdce825542ebb13520933c071cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986452"
---
# <span data-ttu-id="8b291-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8b291-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="8b291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b291-102">SYNOPSIS</span></span>
<span data-ttu-id="8b291-103">Ottiene un'analisi (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="8b291-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="8b291-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b291-104">SYNTAX</span></span>

### <span data-ttu-id="8b291-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b291-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b291-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8b291-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b291-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b291-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b291-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b291-108">DESCRIPTION</span></span>
<span data-ttu-id="8b291-109">Il cmdlet **Get-AzSentinelAlertRule** ottiene un'analisi (regola di avviso) dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="8b291-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="8b291-110">Se si specifica il *parametro AlertRuleId,* viene restituito un singolo **oggetto AlertRule.**</span><span class="sxs-lookup"><span data-stu-id="8b291-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="8b291-111">Se non si specifica il parametro *AlertRuleId,* verrà restituita una matrice contenente tutte le regole di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="8b291-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="8b291-112">È possibile usare **l'oggetto AlertRule** per aggiornare AlertRule, ad esempio disabilitare **AlertRule.**</span><span class="sxs-lookup"><span data-stu-id="8b291-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="8b291-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b291-113">EXAMPLES</span></span>

### <span data-ttu-id="8b291-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b291-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="8b291-115">Questo esempio recupera tutti i criteri di avviso **nell'area** di lavoro specificata e quindi li archivia nella $AlertRules variabile.</span><span class="sxs-lookup"><span data-stu-id="8b291-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="8b291-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b291-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="8b291-117">Questo esempio recupera un **valore AlertRule nell'area** di lavoro specificata e quindi lo archivia nella $AlertRule variabile.</span><span class="sxs-lookup"><span data-stu-id="8b291-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="8b291-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b291-118">PARAMETERS</span></span>

### <span data-ttu-id="8b291-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8b291-119">-AlertRuleId</span></span>
<span data-ttu-id="8b291-120">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="8b291-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b291-121">-DefaultProfile</span></span>
<span data-ttu-id="8b291-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b291-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b291-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b291-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b291-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b291-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b291-125">-ResourceId</span></span>
<span data-ttu-id="8b291-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b291-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b291-127">-WorkspaceName</span></span>
<span data-ttu-id="8b291-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8b291-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b291-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b291-129">CommonParameters</span></span>
<span data-ttu-id="8b291-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b291-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b291-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b291-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b291-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b291-132">INPUTS</span></span>

### <span data-ttu-id="8b291-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8b291-133">System.String</span></span>
## <span data-ttu-id="8b291-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b291-134">OUTPUTS</span></span>

### <span data-ttu-id="8b291-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="8b291-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="8b291-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b291-136">NOTES</span></span>

## <span data-ttu-id="8b291-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b291-137">RELATED LINKS</span></span>
