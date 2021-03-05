---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: a65892efce36490d256c99935f6cbe8a96f5ff98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988916"
---
# <span data-ttu-id="a9842-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9842-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="a9842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9842-102">SYNOPSIS</span></span>
<span data-ttu-id="a9842-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="a9842-103">Removes a policy definition.</span></span>

## <span data-ttu-id="a9842-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9842-104">SYNTAX</span></span>

### <span data-ttu-id="a9842-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a9842-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9842-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9842-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9842-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9842-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9842-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9842-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9842-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9842-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9842-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9842-110">DESCRIPTION</span></span>
<span data-ttu-id="a9842-111">Il cmdlet **Remove-AzPolicyDefinition** rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="a9842-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="a9842-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9842-112">EXAMPLES</span></span>

### <span data-ttu-id="a9842-113">Esempio 1: Rimuovere la definizione del criterio in base al nome</span><span class="sxs-lookup"><span data-stu-id="a9842-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="a9842-114">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="a9842-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="a9842-115">Esempio 2: Rimuovere la definizione del criterio in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a9842-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="a9842-116">Il primo comando ottiene una definizione di criterio denominata VMPolicyDefinition usando Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9842-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a9842-117">Il comando lo archivia nella variabile $PolicyDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="a9842-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="a9842-118">Il secondo comando rimuove la definizione del criterio identificata dalla **proprietà ResourceId** dell'$PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a9842-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a9842-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9842-119">PARAMETERS</span></span>

### <span data-ttu-id="a9842-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9842-120">-ApiVersion</span></span>
<span data-ttu-id="a9842-121">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a9842-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a9842-122">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="a9842-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a9842-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9842-123">-DefaultProfile</span></span>
<span data-ttu-id="a9842-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a9842-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9842-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a9842-125">-Force</span></span>
<span data-ttu-id="a9842-126">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="a9842-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9842-127">-Id</span><span class="sxs-lookup"><span data-stu-id="a9842-127">-Id</span></span>
<span data-ttu-id="a9842-128">Specifica l'ID risorsa completo per la definizione del criterio che questo cmdlet rimuove.</span><span class="sxs-lookup"><span data-stu-id="a9842-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9842-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9842-129">-InputObject</span></span>
<span data-ttu-id="a9842-130">Oggetto definizione dei criteri per rimuovere l'output da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9842-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9842-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a9842-131">-ManagementGroupName</span></span>
<span data-ttu-id="a9842-132">Nome del gruppo di gestione della definizione dei criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a9842-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a9842-133">-Name</span><span class="sxs-lookup"><span data-stu-id="a9842-133">-Name</span></span>
<span data-ttu-id="a9842-134">Specifica il nome della definizione del criterio rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9842-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9842-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a9842-135">-Pre</span></span>
<span data-ttu-id="a9842-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a9842-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a9842-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9842-137">-SubscriptionId</span></span>
<span data-ttu-id="a9842-138">ID sottoscrizione della definizione dei criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a9842-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a9842-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9842-139">-Confirm</span></span>
<span data-ttu-id="a9842-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9842-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9842-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9842-141">-WhatIf</span></span>
<span data-ttu-id="a9842-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9842-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9842-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9842-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9842-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9842-144">CommonParameters</span></span>
<span data-ttu-id="a9842-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9842-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9842-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9842-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9842-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9842-147">INPUTS</span></span>

### <span data-ttu-id="a9842-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a9842-148">System.String</span></span>

### <span data-ttu-id="a9842-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9842-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9842-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9842-150">OUTPUTS</span></span>

### <span data-ttu-id="a9842-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9842-151">System.Boolean</span></span>

## <span data-ttu-id="a9842-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9842-152">NOTES</span></span>

## <span data-ttu-id="a9842-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9842-153">RELATED LINKS</span></span>

[<span data-ttu-id="a9842-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9842-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a9842-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9842-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a9842-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a9842-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


