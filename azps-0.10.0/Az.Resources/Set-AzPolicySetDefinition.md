---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 21ea2a78ed14cc7fbcc343bd7905a33ef4bd126a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862350"
---
# <span data-ttu-id="e8ac8-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e8ac8-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="e8ac8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ac8-103">Modifica di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="e8ac8-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="e8ac8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8ac8-104">SYNTAX</span></span>

### <span data-ttu-id="e8ac8-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8ac8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ac8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ac8-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8ac8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ac8-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8ac8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ac8-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ac8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8ac8-109">DESCRIPTION</span></span>
<span data-ttu-id="e8ac8-110">Il cmdlet **set-AzPolicySetDefinition** modifica una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e8ac8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8ac8-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ac8-112">Esempio 1: aggiornare la descrizione di una definizione di set di criteri</span><span class="sxs-lookup"><span data-stu-id="e8ac8-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e8ac8-113">Il primo comando ottiene una definizione di set di criteri usando il cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="e8ac8-114">Il comando Archivia l'oggetto nella variabile $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="e8ac8-115">Il secondo comando Aggiorna la descrizione della definizione del set di criteri identificata dalla proprietà **resourceId** di $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="e8ac8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8ac8-116">PARAMETERS</span></span>

### <span data-ttu-id="e8ac8-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e8ac8-117">-ApiVersion</span></span>
<span data-ttu-id="e8ac8-118">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e8ac8-119">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e8ac8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ac8-120">-DefaultProfile</span></span>
<span data-ttu-id="e8ac8-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8ac8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8ac8-122">-Description</span></span>
<span data-ttu-id="e8ac8-123">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-123">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8ac8-124">-DisplayName</span></span>
<span data-ttu-id="e8ac8-125">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-125">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-126">-ID</span><span class="sxs-lookup"><span data-stu-id="e8ac8-126">-Id</span></span>
<span data-ttu-id="e8ac8-127">ID di definizione dei criteri completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="e8ac8-128">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e8ac8-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e8ac8-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ac8-129">-ManagementGroupName</span></span>
<span data-ttu-id="e8ac8-130">Nome del gruppo di gestione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e8ac8-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e8ac8-131">-Metadata</span></span>
<span data-ttu-id="e8ac8-132">Metadati della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="e8ac8-133">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8ac8-134">-Name</span></span>
<span data-ttu-id="e8ac8-135">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-136">Parametro-</span><span class="sxs-lookup"><span data-stu-id="e8ac8-136">-Parameter</span></span>
<span data-ttu-id="e8ac8-137">Dichiarazione Parameters della definizione del set di criteri aggiornata.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="e8ac8-138">Può trattarsi di un percorso di un nome file o di un URI che contiene la dichiarazione parameters o della dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e8ac8-139">-PolicyDefinition</span></span>
<span data-ttu-id="e8ac8-140">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-140">The policy set definition.</span></span> <span data-ttu-id="e8ac8-141">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac8-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="e8ac8-142">-Pre</span></span>
<span data-ttu-id="e8ac8-143">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e8ac8-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8ac8-144">-SubscriptionId</span></span>
<span data-ttu-id="e8ac8-145">ID sottoscrizione della definizione del set di criteri da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="e8ac8-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8ac8-146">-Confirm</span></span>
<span data-ttu-id="e8ac8-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ac8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ac8-148">-WhatIf</span></span>
<span data-ttu-id="e8ac8-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ac8-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ac8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ac8-151">CommonParameters</span></span>
<span data-ttu-id="e8ac8-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ac8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ac8-153">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ac8-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ac8-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8ac8-154">INPUTS</span></span>

### <span data-ttu-id="e8ac8-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ac8-155">System.String</span></span>

### <span data-ttu-id="e8ac8-156">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e8ac8-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e8ac8-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8ac8-157">OUTPUTS</span></span>

### <span data-ttu-id="e8ac8-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e8ac8-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e8ac8-159">Note</span><span class="sxs-lookup"><span data-stu-id="e8ac8-159">NOTES</span></span>

## <span data-ttu-id="e8ac8-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8ac8-160">RELATED LINKS</span></span>
