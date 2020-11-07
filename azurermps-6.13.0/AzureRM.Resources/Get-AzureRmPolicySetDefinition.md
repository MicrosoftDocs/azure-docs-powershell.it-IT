---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d0a1097407c9941b5be49b19ea7ba99e75b3fce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687585"
---
# <span data-ttu-id="e4126-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e4126-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e4126-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4126-102">SYNOPSIS</span></span>
<span data-ttu-id="e4126-103">Ottiene le definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e4126-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4126-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4126-104">SYNTAX</span></span>

### <span data-ttu-id="e4126-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4126-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4126-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4126-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4126-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4126-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4126-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4126-108">IdParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4126-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4126-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4126-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4126-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4126-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4126-111">DESCRIPTION</span></span>
<span data-ttu-id="e4126-112">Il cmdlet **Get-AzureRmPolicySetDefinition** ottiene una raccolta di definizioni di set di criteri o una definizione specifica del set di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="e4126-112">The **Get-AzureRmPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="e4126-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4126-113">EXAMPLES</span></span>

### <span data-ttu-id="e4126-114">Esempio 1: ottenere tutte le definizioni di set di criteri</span><span class="sxs-lookup"><span data-stu-id="e4126-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="e4126-115">Questo comando ottiene tutte le definizioni del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e4126-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="e4126-116">Esempio 2: ottenere la definizione del set di criteri dall'abbonamento corrente per nome</span><span class="sxs-lookup"><span data-stu-id="e4126-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="e4126-117">Questo comando consente di ottenere la definizione del set di criteri denominata VMPolicySetDefinition dall'abbonamento predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="e4126-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="e4126-118">Esempio 3: ottenere la definizione del set di criteri dall'abbonamento per nome</span><span class="sxs-lookup"><span data-stu-id="e4126-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="e4126-119">Questo comando ottiene la definizione dei criteri denominata VMPolicySetDefinition dall'abbonamento con ID 3bf44b72-C631-427a-B8C8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="e4126-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="e4126-120">Esempio 4: ottenere tutte le definizioni di set di criteri personalizzati dal gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="e4126-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzureRmPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="e4126-121">Questo comando consente di ottenere tutte le definizioni di set di criteri personalizzati dal gruppo di gestione denominato Dept42.</span><span class="sxs-lookup"><span data-stu-id="e4126-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="e4126-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4126-122">PARAMETERS</span></span>

### <span data-ttu-id="e4126-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4126-123">-ApiVersion</span></span>
<span data-ttu-id="e4126-124">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e4126-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e4126-125">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="e4126-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e4126-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="e4126-126">-Builtin</span></span>
<span data-ttu-id="e4126-127">Limita l'elenco dei risultati solo alle definizioni predefinite del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e4126-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="e4126-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="e4126-128">-Custom</span></span>
<span data-ttu-id="e4126-129">Limita l'elenco dei risultati solo alle definizioni di set di criteri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e4126-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="e4126-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4126-130">-DefaultProfile</span></span>
<span data-ttu-id="e4126-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e4126-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4126-132">-ID</span><span class="sxs-lookup"><span data-stu-id="e4126-132">-Id</span></span>
<span data-ttu-id="e4126-133">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e4126-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e4126-134">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e4126-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e4126-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e4126-135">-ManagementGroupName</span></span>
<span data-ttu-id="e4126-136">Nome del gruppo di gestione delle definizioni dei set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e4126-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e4126-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4126-137">-Name</span></span>
<span data-ttu-id="e4126-138">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e4126-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="e4126-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="e4126-139">-Pre</span></span>
<span data-ttu-id="e4126-140">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e4126-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e4126-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4126-141">-SubscriptionId</span></span>
<span data-ttu-id="e4126-142">ID della sottoscrizione delle definizioni del set di criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e4126-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="e4126-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4126-143">CommonParameters</span></span>
<span data-ttu-id="e4126-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4126-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4126-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4126-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4126-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4126-146">INPUTS</span></span>

### <span data-ttu-id="e4126-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e4126-147">System.String</span></span>

### <span data-ttu-id="e4126-148">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e4126-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e4126-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4126-149">OUTPUTS</span></span>

### <span data-ttu-id="e4126-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e4126-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e4126-151">Note</span><span class="sxs-lookup"><span data-stu-id="e4126-151">NOTES</span></span>

## <span data-ttu-id="e4126-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4126-152">RELATED LINKS</span></span>
