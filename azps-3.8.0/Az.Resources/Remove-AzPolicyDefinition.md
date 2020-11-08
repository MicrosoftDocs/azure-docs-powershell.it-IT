---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019718"
---
# <span data-ttu-id="4cff6-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cff6-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="4cff6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cff6-102">SYNOPSIS</span></span>
<span data-ttu-id="4cff6-103">Rimuove una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="4cff6-103">Removes a policy definition.</span></span>

## <span data-ttu-id="4cff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cff6-104">SYNTAX</span></span>

### <span data-ttu-id="4cff6-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cff6-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cff6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cff6-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cff6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cff6-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cff6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cff6-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cff6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cff6-109">DESCRIPTION</span></span>
<span data-ttu-id="4cff6-110">Il cmdlet **Remove-AzPolicyDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="4cff6-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="4cff6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cff6-111">EXAMPLES</span></span>

### <span data-ttu-id="4cff6-112">Esempio 1: rimuovere la definizione dei criteri in base al nome</span><span class="sxs-lookup"><span data-stu-id="4cff6-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="4cff6-113">Questo comando rimuove la definizione di criterio specificata.</span><span class="sxs-lookup"><span data-stu-id="4cff6-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="4cff6-114">Esempio 2: rimuovere la definizione dei criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4cff6-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="4cff6-115">Il primo comando ottiene una definizione di criteri denominata VMPolicyDefinition tramite il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cff6-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4cff6-116">Il comando lo archivia nella variabile $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cff6-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4cff6-117">Il secondo comando rimuove la definizione dei criteri identificata dalla proprietà **resourceId** di $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4cff6-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4cff6-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cff6-118">PARAMETERS</span></span>

### <span data-ttu-id="4cff6-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cff6-119">-ApiVersion</span></span>
<span data-ttu-id="4cff6-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="4cff6-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4cff6-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="4cff6-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4cff6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cff6-122">-DefaultProfile</span></span>
<span data-ttu-id="4cff6-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4cff6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cff6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4cff6-124">-Force</span></span>
<span data-ttu-id="4cff6-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4cff6-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cff6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4cff6-126">-Id</span></span>
<span data-ttu-id="4cff6-127">Specifica l'ID di risorsa completo per la definizione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cff6-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4cff6-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4cff6-128">-ManagementGroupName</span></span>
<span data-ttu-id="4cff6-129">Nome del gruppo di gestione della definizione di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4cff6-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4cff6-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cff6-130">-Name</span></span>
<span data-ttu-id="4cff6-131">Specifica il nome della definizione di criterio rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cff6-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4cff6-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4cff6-132">-Pre</span></span>
<span data-ttu-id="4cff6-133">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4cff6-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4cff6-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cff6-134">-SubscriptionId</span></span>
<span data-ttu-id="4cff6-135">ID sottoscrizione della definizione di criterio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4cff6-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4cff6-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4cff6-136">-Confirm</span></span>
<span data-ttu-id="4cff6-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cff6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cff6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cff6-138">-WhatIf</span></span>
<span data-ttu-id="4cff6-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cff6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cff6-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cff6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cff6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cff6-141">CommonParameters</span></span>
<span data-ttu-id="4cff6-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cff6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cff6-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cff6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cff6-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cff6-144">INPUTS</span></span>

### <span data-ttu-id="4cff6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4cff6-145">System.String</span></span>

### <span data-ttu-id="4cff6-146">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4cff6-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4cff6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cff6-147">OUTPUTS</span></span>

### <span data-ttu-id="4cff6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cff6-148">System.Boolean</span></span>

## <span data-ttu-id="4cff6-149">Note</span><span class="sxs-lookup"><span data-stu-id="4cff6-149">NOTES</span></span>

## <span data-ttu-id="4cff6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cff6-150">RELATED LINKS</span></span>

[<span data-ttu-id="4cff6-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cff6-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="4cff6-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cff6-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="4cff6-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4cff6-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


