---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474272"
---
# <span data-ttu-id="a2624-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a2624-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="a2624-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2624-102">SYNOPSIS</span></span>
<span data-ttu-id="a2624-103">Ottiene le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a2624-103">Gets policy definitions.</span></span>

## <span data-ttu-id="a2624-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2624-104">SYNTAX</span></span>

### <span data-ttu-id="a2624-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2624-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2624-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2624-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2624-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2624-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2624-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2624-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2624-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2624-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2624-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2624-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2624-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2624-111">DESCRIPTION</span></span>
<span data-ttu-id="a2624-112">Il cmdlet **Get-AzPolicyDefinition** ottiene una raccolta di definizioni di criteri o una definizione di criteri specifica identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="a2624-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="a2624-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2624-113">EXAMPLES</span></span>

### <span data-ttu-id="a2624-114">Esempio 1: ottenere tutte le definizioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="a2624-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="a2624-115">Questo comando ottiene tutte le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a2624-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="a2624-116">Esempio 2: ottenere la definizione dei criteri dall'abbonamento corrente per nome</span><span class="sxs-lookup"><span data-stu-id="a2624-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="a2624-117">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition dall'abbonamento predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="a2624-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="a2624-118">Esempio 3: ottenere la definizione dei criteri dal gruppo di gestione per nome</span><span class="sxs-lookup"><span data-stu-id="a2624-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="a2624-119">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition dal gruppo di gestione denominato Dept42.</span><span class="sxs-lookup"><span data-stu-id="a2624-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="a2624-120">Esempio 4: ottenere tutte le definizioni dei criteri predefinite dall'abbonamento</span><span class="sxs-lookup"><span data-stu-id="a2624-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="a2624-121">Questo comando consente di ottenere tutte le definizioni dei criteri predefinite dall'abbonamento con ID 3bf44b72-C631-427a-B8C8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="a2624-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="a2624-122">Esempio 5: ottenere definizioni di criteri da una determinata categoria</span><span class="sxs-lookup"><span data-stu-id="a2624-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="a2624-123">Questo comando ottiene tutte le definizioni dei criteri nella categoria "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="a2624-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="a2624-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2624-124">PARAMETERS</span></span>

### <span data-ttu-id="a2624-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a2624-125">-ApiVersion</span></span>
<span data-ttu-id="a2624-126">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a2624-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a2624-127">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="a2624-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a2624-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="a2624-128">-Builtin</span></span>
<span data-ttu-id="a2624-129">Limita l'elenco dei risultati per le definizioni di criteri predefinite.</span><span class="sxs-lookup"><span data-stu-id="a2624-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="a2624-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="a2624-130">-Custom</span></span>
<span data-ttu-id="a2624-131">Limita l'elenco dei risultati solo alle definizioni di criteri personalizzate.</span><span class="sxs-lookup"><span data-stu-id="a2624-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="a2624-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2624-132">-DefaultProfile</span></span>
<span data-ttu-id="a2624-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a2624-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2624-134">-ID</span><span class="sxs-lookup"><span data-stu-id="a2624-134">-Id</span></span>
<span data-ttu-id="a2624-135">Specifica l'ID risorsa completo per la definizione dei criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2624-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a2624-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a2624-136">-ManagementGroupName</span></span>
<span data-ttu-id="a2624-137">Nome del gruppo di gestione delle definizioni dei criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a2624-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="a2624-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2624-138">-Name</span></span>
<span data-ttu-id="a2624-139">Specifica il nome della definizione del criterio ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2624-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a2624-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="a2624-140">-Pre</span></span>
<span data-ttu-id="a2624-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a2624-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a2624-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2624-142">-SubscriptionId</span></span>
<span data-ttu-id="a2624-143">ID della sottoscrizione delle definizioni dei criteri da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a2624-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="a2624-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2624-144">CommonParameters</span></span>
<span data-ttu-id="a2624-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2624-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2624-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2624-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2624-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2624-147">INPUTS</span></span>

### <span data-ttu-id="a2624-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a2624-148">System.String</span></span>

### <span data-ttu-id="a2624-149">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a2624-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a2624-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2624-150">OUTPUTS</span></span>

### <span data-ttu-id="a2624-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a2624-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a2624-152">Note</span><span class="sxs-lookup"><span data-stu-id="a2624-152">NOTES</span></span>

## <span data-ttu-id="a2624-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2624-153">RELATED LINKS</span></span>

[<span data-ttu-id="a2624-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a2624-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a2624-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a2624-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="a2624-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a2624-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


