---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191215"
---
# <span data-ttu-id="c1a9b-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="c1a9b-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="c1a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a9b-103">Ottenere una risposta automatica (azione regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="c1a9b-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="c1a9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1a9b-104">SYNTAX</span></span>

### <span data-ttu-id="c1a9b-105">AlertRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1a9b-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a9b-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="c1a9b-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a9b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1a9b-107">DESCRIPTION</span></span>
<span data-ttu-id="c1a9b-108">Il cmdlet **Get-AzSentinelAlertRuleAction** ottiene una risposta automatica (azione regola di avviso) dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="c1a9b-109">Se si specificano i *parametri ActionId* e *AlertRuleId,* viene restituito un singolo **oggetto AlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="c1a9b-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="c1a9b-110">Se non si specifica il parametro *ActionId,* verrà restituita una matrice contenente tutte le azioni per la regola di avviso specifica nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="c1a9b-111">È possibile usare **l'oggetto Azione** per aggiornare l'azione, ad esempio per modificare l'azione **di** una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="c1a9b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1a9b-112">EXAMPLES</span></span>

### <span data-ttu-id="c1a9b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1a9b-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="c1a9b-114">Questo esempio recupera  tutte le azioni per la regola di avviso specificata nell'area di lavoro specificata e quindi la archivia nella variabile $AlertRuleActions specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="c1a9b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1a9b-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="c1a9b-116">Questo esempio ottiene **un'azione AlertRuleAction** per la regola di avviso specificata nell'area di lavoro specificata e la archivia nella variabile $AlertRuleAction specificata.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="c1a9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1a9b-117">PARAMETERS</span></span>

### <span data-ttu-id="c1a9b-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="c1a9b-118">-ActionId</span></span>
<span data-ttu-id="c1a9b-119">ID azione.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9b-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c1a9b-120">-AlertRuleId</span></span>
<span data-ttu-id="c1a9b-121">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a9b-122">-DefaultProfile</span></span>
<span data-ttu-id="c1a9b-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1a9b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c1a9b-126">-WorkspaceName</span></span>
<span data-ttu-id="c1a9b-127">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a9b-128">CommonParameters</span></span>
<span data-ttu-id="c1a9b-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a9b-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1a9b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a9b-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1a9b-131">INPUTS</span></span>

### <span data-ttu-id="c1a9b-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1a9b-132">None</span></span>
## <span data-ttu-id="c1a9b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1a9b-133">OUTPUTS</span></span>

### <span data-ttu-id="c1a9b-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c1a9b-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="c1a9b-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1a9b-135">NOTES</span></span>

## <span data-ttu-id="c1a9b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1a9b-136">RELATED LINKS</span></span>
