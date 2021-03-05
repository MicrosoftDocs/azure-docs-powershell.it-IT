---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: db398fe5870a1ff304637c9aa33bf168c49a7759
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005678"
---
# <span data-ttu-id="b0959-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="b0959-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="b0959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0959-102">SYNOPSIS</span></span>
<span data-ttu-id="b0959-103">Ottenere un modello di regola analitica.</span><span class="sxs-lookup"><span data-stu-id="b0959-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="b0959-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0959-104">SYNTAX</span></span>

### <span data-ttu-id="b0959-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0959-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0959-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="b0959-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0959-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0959-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0959-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0959-108">DESCRIPTION</span></span>
<span data-ttu-id="b0959-109">Il **cmdlet Get-AzSentinelAlertRuleTemplate** ottiene un modello di regola di avviso dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="b0959-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="b0959-110">Se si specifica il *parametro AlertRuleTemplateId,* viene restituito un singolo **oggetto AlertRuleTemplate.**</span><span class="sxs-lookup"><span data-stu-id="b0959-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="b0959-111">Se non si specifica il parametro *AlertRuleTemplateId,* verrà restituita una matrice contenente tutti i modelli di regola di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="b0959-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="b0959-112">È possibile usare **l'oggetto AlertRuleTemplate** per creare una nuova regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="b0959-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="b0959-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0959-113">EXAMPLES</span></span>

### <span data-ttu-id="b0959-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0959-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="b0959-115">Questo esempio recupera tutti i **criteri AlertRuleTemplates nell'area** di lavoro specificata e quindi li archivia nella $AlertRuleTemplates variabile.</span><span class="sxs-lookup"><span data-stu-id="b0959-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="b0959-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0959-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="b0959-117">Questo esempio recupera un **valore AlertRuleTemplate** nell'area di lavoro specificata e quindi lo archivia nella $AlertRuleTemplate variabile.</span><span class="sxs-lookup"><span data-stu-id="b0959-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="b0959-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0959-118">PARAMETERS</span></span>

### <span data-ttu-id="b0959-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="b0959-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="b0959-120">ID regola di avviso modello.</span><span class="sxs-lookup"><span data-stu-id="b0959-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0959-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0959-121">-DefaultProfile</span></span>
<span data-ttu-id="b0959-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0959-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0959-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0959-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0959-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0959-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0959-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0959-125">-ResourceId</span></span>
<span data-ttu-id="b0959-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0959-126">Resource Id.</span></span>

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

### <span data-ttu-id="b0959-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0959-127">-WorkspaceName</span></span>
<span data-ttu-id="b0959-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b0959-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0959-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0959-129">CommonParameters</span></span>
<span data-ttu-id="b0959-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0959-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0959-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0959-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0959-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0959-132">INPUTS</span></span>

### <span data-ttu-id="b0959-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b0959-133">System.String</span></span>
## <span data-ttu-id="b0959-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0959-134">OUTPUTS</span></span>

### <span data-ttu-id="b0959-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="b0959-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="b0959-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0959-136">NOTES</span></span>

## <span data-ttu-id="b0959-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0959-137">RELATED LINKS</span></span>
