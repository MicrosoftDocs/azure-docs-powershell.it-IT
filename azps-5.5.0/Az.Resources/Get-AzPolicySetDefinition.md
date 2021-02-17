---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192782"
---
# <span data-ttu-id="1956e-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1956e-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="1956e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1956e-102">SYNOPSIS</span></span>
<span data-ttu-id="1956e-103">Ottiene le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1956e-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="1956e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1956e-104">SYNTAX</span></span>

### <span data-ttu-id="1956e-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1956e-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1956e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1956e-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1956e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1956e-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1956e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1956e-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1956e-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="1956e-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1956e-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="1956e-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1956e-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1956e-111">DESCRIPTION</span></span>
<span data-ttu-id="1956e-112">Il cmdlet **Get-AzPolicySetDefinition** ottiene una raccolta di definizioni del set di criteri o una definizione di set di criteri specifica identificata da nome o ID.</span><span class="sxs-lookup"><span data-stu-id="1956e-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="1956e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1956e-113">EXAMPLES</span></span>

### <span data-ttu-id="1956e-114">Esempio 1: Ottenere tutte le definizioni del set di criteri</span><span class="sxs-lookup"><span data-stu-id="1956e-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="1956e-115">Questo comando ottiene tutte le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1956e-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="1956e-116">Esempio 2: Ottenere la definizione del set di criteri dall'abbonamento corrente in base al nome</span><span class="sxs-lookup"><span data-stu-id="1956e-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="1956e-117">Questo comando recupera la definizione del set di criteri denominata VMPolicySetDefinition dalla sottoscrizione predefinita corrente.</span><span class="sxs-lookup"><span data-stu-id="1956e-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="1956e-118">Esempio 3: Ottenere la definizione del set di criteri dall'abbonamento in base al nome</span><span class="sxs-lookup"><span data-stu-id="1956e-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="1956e-119">Questo comando recupera la definizione del criterio denominata VMPolicySetDefinition dalla sottoscrizione con ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="1956e-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="1956e-120">Esempio 4: Ottenere tutte le definizioni del set di criteri personalizzate dal gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="1956e-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="1956e-121">Questo comando recupera tutte le definizioni del set di criteri personalizzate dal gruppo di gestione denominato Dept42.</span><span class="sxs-lookup"><span data-stu-id="1956e-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="1956e-122">Esempio 5: Ottenere le definizioni del set di criteri da una determinata categoria</span><span class="sxs-lookup"><span data-stu-id="1956e-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="1956e-123">Questo comando recupera tutte le definizioni del set di criteri nella categoria "Macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="1956e-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="1956e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1956e-124">PARAMETERS</span></span>

### <span data-ttu-id="1956e-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1956e-125">-ApiVersion</span></span>
<span data-ttu-id="1956e-126">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1956e-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1956e-127">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="1956e-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="1956e-128">-Builtin</span></span>
<span data-ttu-id="1956e-129">Limita l'elenco dei risultati solo alle definizioni del set di criteri incorporate.</span><span class="sxs-lookup"><span data-stu-id="1956e-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-130">-Personalizzato</span><span class="sxs-lookup"><span data-stu-id="1956e-130">-Custom</span></span>
<span data-ttu-id="1956e-131">Limita l'elenco dei risultati solo alle definizioni del set di criteri personalizzate.</span><span class="sxs-lookup"><span data-stu-id="1956e-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1956e-132">-DefaultProfile</span></span>
<span data-ttu-id="1956e-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1956e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1956e-134">-Id</span><span class="sxs-lookup"><span data-stu-id="1956e-134">-Id</span></span>
<span data-ttu-id="1956e-135">ID di definizione del set di criteri completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1956e-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="1956e-136">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1956e-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1956e-137">-ManagementGroupName</span></span>
<span data-ttu-id="1956e-138">Nome del gruppo di gestione delle definizioni dei set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1956e-138">The name of the management group of the policy set definition(s) to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="1956e-139">-Name</span></span>
<span data-ttu-id="1956e-140">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="1956e-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="1956e-141">-Pre</span></span>
<span data-ttu-id="1956e-142">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1956e-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1956e-143">-SubscriptionId</span></span>
<span data-ttu-id="1956e-144">ID sottoscrizione delle definizioni di set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1956e-144">The subscription ID of the policy set definition(s) to get.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1956e-145">CommonParameters</span></span>
<span data-ttu-id="1956e-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1956e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1956e-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1956e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1956e-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="1956e-148">INPUTS</span></span>

### <span data-ttu-id="1956e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1956e-149">System.String</span></span>

### <span data-ttu-id="1956e-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1956e-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1956e-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1956e-151">OUTPUTS</span></span>

### <span data-ttu-id="1956e-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="1956e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1956e-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="1956e-153">NOTES</span></span>

## <span data-ttu-id="1956e-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1956e-154">RELATED LINKS</span></span>
