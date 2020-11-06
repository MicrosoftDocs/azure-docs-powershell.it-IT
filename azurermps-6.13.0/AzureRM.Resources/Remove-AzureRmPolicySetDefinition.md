---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9fcae03dba32aff18d2863c557c5827cf3e9d95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511487"
---
# <span data-ttu-id="a8458-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a8458-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="a8458-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8458-102">SYNOPSIS</span></span>
<span data-ttu-id="a8458-103">Rimuove una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="a8458-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8458-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8458-104">SYNTAX</span></span>

### <span data-ttu-id="a8458-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8458-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8458-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8458-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8458-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8458-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8458-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8458-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8458-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8458-109">DESCRIPTION</span></span>
<span data-ttu-id="a8458-110">Il cmdlet **Remove-AzureRmPolicySetDefinition** rimuove una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="a8458-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="a8458-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8458-111">EXAMPLES</span></span>

### <span data-ttu-id="a8458-112">Esempio 1: rimuovere la definizione del set di criteri in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a8458-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="a8458-113">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a8458-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="a8458-114">Il comando lo archivia nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a8458-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="a8458-115">Il secondo comando rimuove la definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="a8458-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="a8458-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8458-116">PARAMETERS</span></span>

### <span data-ttu-id="a8458-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a8458-117">-ApiVersion</span></span>
<span data-ttu-id="a8458-118">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a8458-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a8458-119">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="a8458-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a8458-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8458-120">-DefaultProfile</span></span>
<span data-ttu-id="a8458-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a8458-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8458-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a8458-122">-Force</span></span>
<span data-ttu-id="a8458-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a8458-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a8458-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a8458-124">-Id</span></span>
<span data-ttu-id="a8458-125">ID di definizione del set di criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a8458-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="a8458-126">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a8458-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a8458-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a8458-127">-ManagementGroupName</span></span>
<span data-ttu-id="a8458-128">Nome del gruppo di gestione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a8458-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="a8458-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8458-129">-Name</span></span>
<span data-ttu-id="a8458-130">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="a8458-130">The policy set definition name.</span></span>

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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8458-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="a8458-131">-Pre</span></span>
<span data-ttu-id="a8458-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a8458-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a8458-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8458-133">-SubscriptionId</span></span>
<span data-ttu-id="a8458-134">ID sottoscrizione della definizione del set di criteri da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a8458-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="a8458-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8458-135">-Confirm</span></span>
<span data-ttu-id="a8458-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8458-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8458-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8458-137">-WhatIf</span></span>
<span data-ttu-id="a8458-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8458-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8458-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8458-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8458-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8458-140">CommonParameters</span></span>
<span data-ttu-id="a8458-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8458-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8458-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8458-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8458-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8458-143">INPUTS</span></span>

### <span data-ttu-id="a8458-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a8458-144">System.String</span></span>

### <span data-ttu-id="a8458-145">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a8458-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a8458-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8458-146">OUTPUTS</span></span>

### <span data-ttu-id="a8458-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8458-147">System.Boolean</span></span>

## <span data-ttu-id="a8458-148">Note</span><span class="sxs-lookup"><span data-stu-id="a8458-148">NOTES</span></span>

## <span data-ttu-id="a8458-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8458-149">RELATED LINKS</span></span>
