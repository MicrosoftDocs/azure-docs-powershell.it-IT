---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 37cc56714712d71ab34adee14a8b758cd9dd1113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986465"
---
# <span data-ttu-id="0bd32-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="0bd32-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="0bd32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd32-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd32-103">Ottenere una risposta automatica (azione regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="0bd32-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="0bd32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bd32-104">SYNTAX</span></span>

### <span data-ttu-id="0bd32-105">AlertRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bd32-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd32-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="0bd32-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd32-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0bd32-107">DESCRIPTION</span></span>
<span data-ttu-id="0bd32-108">Il cmdlet **Get-AzSentinelAlertRuleAction** ottiene una risposta automatica (azione regola di avviso) dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="0bd32-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="0bd32-109">Se si specificano i *parametri ActionId* e *AlertRuleId,* viene restituito un singolo **oggetto AlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="0bd32-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="0bd32-110">Se non si specifica il parametro *ActionId,* verrà restituita una matrice contenente tutte le azioni per la specifica regola di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="0bd32-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="0bd32-111">È possibile usare **l'oggetto Azione** per aggiornare l'azione, ad esempio per modificare l'azione **di** una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="0bd32-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="0bd32-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bd32-112">EXAMPLES</span></span>

### <span data-ttu-id="0bd32-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0bd32-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="0bd32-114">Questo esempio recupera  tutte le azioni per la regola di avviso specificata nell'area di lavoro specificata e quindi la archivia nella variabile $AlertRuleActions specificata.</span><span class="sxs-lookup"><span data-stu-id="0bd32-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="0bd32-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0bd32-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="0bd32-116">Questo esempio ottiene **un'azione AlertRuleAction** per la regola di avviso specificata nell'area di lavoro specificata e la archivia nella variabile $AlertRuleAction specificata.</span><span class="sxs-lookup"><span data-stu-id="0bd32-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="0bd32-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bd32-117">PARAMETERS</span></span>

### <span data-ttu-id="0bd32-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="0bd32-118">-ActionId</span></span>
<span data-ttu-id="0bd32-119">ID azione.</span><span class="sxs-lookup"><span data-stu-id="0bd32-119">Action Id.</span></span>

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

### <span data-ttu-id="0bd32-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0bd32-120">-AlertRuleId</span></span>
<span data-ttu-id="0bd32-121">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="0bd32-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="0bd32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd32-122">-DefaultProfile</span></span>
<span data-ttu-id="0bd32-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bd32-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd32-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bd32-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0bd32-125">Resource group name.</span></span>

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

### <span data-ttu-id="0bd32-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0bd32-126">-WorkspaceName</span></span>
<span data-ttu-id="0bd32-127">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0bd32-127">Workspace Name.</span></span>

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

### <span data-ttu-id="0bd32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd32-128">CommonParameters</span></span>
<span data-ttu-id="0bd32-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd32-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0bd32-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd32-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="0bd32-131">INPUTS</span></span>

### <span data-ttu-id="0bd32-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0bd32-132">None</span></span>
## <span data-ttu-id="0bd32-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bd32-133">OUTPUTS</span></span>

### <span data-ttu-id="0bd32-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="0bd32-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="0bd32-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0bd32-135">NOTES</span></span>

## <span data-ttu-id="0bd32-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bd32-136">RELATED LINKS</span></span>
