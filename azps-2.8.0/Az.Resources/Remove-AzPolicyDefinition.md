---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: f932e566d9fe6639e19e4f906775282cd17315d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856334"
---
# <span data-ttu-id="ea1f3-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea1f3-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="ea1f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1f3-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-103">Removes a policy definition.</span></span>

## <span data-ttu-id="ea1f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea1f3-104">SYNTAX</span></span>

### <span data-ttu-id="ea1f3-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea1f3-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1f3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1f3-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1f3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1f3-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1f3-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1f3-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1f3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea1f3-109">DESCRIPTION</span></span>
<span data-ttu-id="ea1f3-110">Il cmdlet **Remove-AzPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="ea1f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea1f3-111">EXAMPLES</span></span>

### <span data-ttu-id="ea1f3-112">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="ea1f3-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="ea1f3-113">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="ea1f3-114">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="ea1f3-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="ea1f3-115">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="ea1f3-116">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="ea1f3-117">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="ea1f3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea1f3-118">PARAMETERS</span></span>

### <span data-ttu-id="ea1f3-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea1f3-119">-ApiVersion</span></span>
<span data-ttu-id="ea1f3-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ea1f3-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ea1f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1f3-122">-DefaultProfile</span></span>
<span data-ttu-id="ea1f3-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ea1f3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea1f3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1f3-124">-Force</span></span>
<span data-ttu-id="ea1f3-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea1f3-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ea1f3-126">-Id</span></span>
<span data-ttu-id="ea1f3-127">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea1f3-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1f3-128">-ManagementGroupName</span></span>
<span data-ttu-id="ea1f3-129">Nome del gruppo di gestione della definizione di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="ea1f3-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea1f3-130">-Name</span></span>
<span data-ttu-id="ea1f3-131">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea1f3-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea1f3-132">-Pre</span></span>
<span data-ttu-id="ea1f3-133">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ea1f3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea1f3-134">-SubscriptionId</span></span>
<span data-ttu-id="ea1f3-135">ID sottoscrizione della definizione di criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="ea1f3-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea1f3-136">-Confirm</span></span>
<span data-ttu-id="ea1f3-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1f3-138">-WhatIf</span></span>
<span data-ttu-id="ea1f3-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1f3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1f3-141">CommonParameters</span></span>
<span data-ttu-id="ea1f3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1f3-143">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1f3-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1f3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea1f3-144">INPUTS</span></span>

### <span data-ttu-id="ea1f3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ea1f3-145">System.String</span></span>

### <span data-ttu-id="ea1f3-146">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea1f3-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ea1f3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea1f3-147">OUTPUTS</span></span>

### <span data-ttu-id="ea1f3-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea1f3-148">System.Boolean</span></span>

## <span data-ttu-id="ea1f3-149">Note</span><span class="sxs-lookup"><span data-stu-id="ea1f3-149">NOTES</span></span>

## <span data-ttu-id="ea1f3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea1f3-150">RELATED LINKS</span></span>

[<span data-ttu-id="ea1f3-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea1f3-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="ea1f3-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea1f3-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="ea1f3-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea1f3-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


