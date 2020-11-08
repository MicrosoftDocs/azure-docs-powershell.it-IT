---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020577"
---
# <span data-ttu-id="4a1c9-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4a1c9-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="4a1c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1c9-103">Ottiene le definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="4a1c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a1c9-104">SYNTAX</span></span>

### <span data-ttu-id="4a1c9-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a1c9-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1c9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1c9-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1c9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1c9-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1c9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1c9-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a1c9-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1c9-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a1c9-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a1c9-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a1c9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a1c9-111">DESCRIPTION</span></span>
<span data-ttu-id="4a1c9-112">Il cmdlet **Get-AzPolicySetDefinition** ottiene una raccolta di definizioni di set di criteri o una definizione specifica del set di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="4a1c9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a1c9-113">EXAMPLES</span></span>

### <span data-ttu-id="4a1c9-114">Esempio 1: ottenere tutte le definizioni di set di criteri</span><span class="sxs-lookup"><span data-stu-id="4a1c9-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="4a1c9-115">Questo comando ottiene tutte le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="4a1c9-116">Esempio 2: ottenere la definizione del set di criteri dall'abbonamento corrente per nome</span><span class="sxs-lookup"><span data-stu-id="4a1c9-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="4a1c9-117">Questo comando consente di ottenere la definizione del set di criteri denominata VMPolicySetDefinition dall'abbonamento predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="4a1c9-118">Esempio 3: ottenere la definizione del set di criteri dall'abbonamento per nome</span><span class="sxs-lookup"><span data-stu-id="4a1c9-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="4a1c9-119">Questo comando ottiene la definizione dei criteri denominata VMPolicySetDefinition dall'abbonamento con ID 3bf44b72-C631-427a-B8C8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="4a1c9-120">Esempio 4: ottenere tutte le definizioni di set di criteri personalizzati dal gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="4a1c9-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="4a1c9-121">Questo comando consente di ottenere tutte le definizioni di set di criteri personalizzati dal gruppo di gestione denominato Dept42.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="4a1c9-122">Esempio 5: ottenere le definizioni del set di criteri da una determinata categoria</span><span class="sxs-lookup"><span data-stu-id="4a1c9-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="4a1c9-123">Questo comando consente di ottenere tutte le definizioni di set di criteri nella categoria "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="4a1c9-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="4a1c9-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a1c9-124">PARAMETERS</span></span>

### <span data-ttu-id="4a1c9-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4a1c9-125">-ApiVersion</span></span>
<span data-ttu-id="4a1c9-126">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4a1c9-127">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4a1c9-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="4a1c9-128">-Builtin</span></span>
<span data-ttu-id="4a1c9-129">Limita l'elenco dei risultati solo alle definizioni predefinite del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="4a1c9-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="4a1c9-130">-Custom</span></span>
<span data-ttu-id="4a1c9-131">Limita l'elenco dei risultati solo alle definizioni di set di criteri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="4a1c9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1c9-132">-DefaultProfile</span></span>
<span data-ttu-id="4a1c9-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a1c9-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a1c9-134">-ID</span><span class="sxs-lookup"><span data-stu-id="4a1c9-134">-Id</span></span>
<span data-ttu-id="4a1c9-135">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="4a1c9-136">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4a1c9-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="4a1c9-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4a1c9-137">-ManagementGroupName</span></span>
<span data-ttu-id="4a1c9-138">Nome del gruppo di gestione delle definizioni dei set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="4a1c9-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a1c9-139">-Name</span></span>
<span data-ttu-id="4a1c9-140">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="4a1c9-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="4a1c9-141">-Pre</span></span>
<span data-ttu-id="4a1c9-142">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4a1c9-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a1c9-143">-SubscriptionId</span></span>
<span data-ttu-id="4a1c9-144">ID della sottoscrizione delle definizioni del set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="4a1c9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1c9-145">CommonParameters</span></span>
<span data-ttu-id="4a1c9-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1c9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1c9-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a1c9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1c9-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a1c9-148">INPUTS</span></span>

### <span data-ttu-id="4a1c9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1c9-149">System.String</span></span>

### <span data-ttu-id="4a1c9-150">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a1c9-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4a1c9-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a1c9-151">OUTPUTS</span></span>

### <span data-ttu-id="4a1c9-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4a1c9-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4a1c9-153">Note</span><span class="sxs-lookup"><span data-stu-id="4a1c9-153">NOTES</span></span>

## <span data-ttu-id="4a1c9-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a1c9-154">RELATED LINKS</span></span>
