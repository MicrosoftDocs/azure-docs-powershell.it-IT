---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486239"
---
# <span data-ttu-id="6fec4-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="6fec4-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="6fec4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fec4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fec4-103">Ottiene un oggetto analitico (regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="6fec4-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="6fec4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fec4-104">SYNTAX</span></span>

### <span data-ttu-id="6fec4-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6fec4-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fec4-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6fec4-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fec4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fec4-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fec4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fec4-108">DESCRIPTION</span></span>
<span data-ttu-id="6fec4-109">Il cmdlet **Get-AzSentinelAlertRule** ottiene una regola analitica (Alert Rule) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="6fec4-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="6fec4-110">Se specifichi il parametro *AlertRuleId* , viene restituito un singolo oggetto **AlertRule** .</span><span class="sxs-lookup"><span data-stu-id="6fec4-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="6fec4-111">Se non specifichi il parametro *AlertRuleId* , viene restituita una matrice contenente tutte le regole di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="6fec4-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="6fec4-112">Puoi usare l'oggetto **AlertRule** per aggiornare AlertRule, ad esempio puoi disabilitare **AlertRule**.</span><span class="sxs-lookup"><span data-stu-id="6fec4-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="6fec4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fec4-113">EXAMPLES</span></span>

### <span data-ttu-id="6fec4-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fec4-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="6fec4-115">Questo esempio recupera tutti i **AlertRules** nell'area di lavoro specificata e lo archivia nella variabile $AlertRules.</span><span class="sxs-lookup"><span data-stu-id="6fec4-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="6fec4-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6fec4-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="6fec4-117">Questo esempio ottiene un **AlertRule** nell'area di lavoro specificata e lo archivia nella variabile $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="6fec4-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="6fec4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fec4-118">PARAMETERS</span></span>

### <span data-ttu-id="6fec4-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6fec4-119">-AlertRuleId</span></span>
<span data-ttu-id="6fec4-120">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="6fec4-120">Alert Rule Id.</span></span>

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

### <span data-ttu-id="6fec4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fec4-121">-DefaultProfile</span></span>
<span data-ttu-id="6fec4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fec4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fec4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fec4-123">-ResourceGroupName</span></span>
<span data-ttu-id="6fec4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6fec4-124">Resource group name.</span></span>

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

### <span data-ttu-id="6fec4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fec4-125">-ResourceId</span></span>
<span data-ttu-id="6fec4-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fec4-126">Resource Id.</span></span>

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

### <span data-ttu-id="6fec4-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fec4-127">-WorkspaceName</span></span>
<span data-ttu-id="6fec4-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6fec4-128">Workspace Name.</span></span>

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

### <span data-ttu-id="6fec4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fec4-129">CommonParameters</span></span>
<span data-ttu-id="6fec4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fec4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fec4-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fec4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fec4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fec4-132">INPUTS</span></span>

### <span data-ttu-id="6fec4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6fec4-133">System.String</span></span>
## <span data-ttu-id="6fec4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fec4-134">OUTPUTS</span></span>

### <span data-ttu-id="6fec4-135">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="6fec4-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="6fec4-136">Note</span><span class="sxs-lookup"><span data-stu-id="6fec4-136">NOTES</span></span>

## <span data-ttu-id="6fec4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fec4-137">RELATED LINKS</span></span>
