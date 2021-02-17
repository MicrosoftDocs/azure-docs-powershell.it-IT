---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192743"
---
# <span data-ttu-id="8dc8a-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8dc8a-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="8dc8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc8a-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc8a-103">Crea una definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="8dc8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dc8a-104">SYNTAX</span></span>

### <span data-ttu-id="8dc8a-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8dc8a-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc8a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc8a-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dc8a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc8a-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dc8a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8dc8a-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc8a-109">Il cmdlet **New-AzPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="8dc8a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dc8a-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc8a-111">Esempio 1: Creare una definizione del set di criteri con metadati usando un file del set di criteri</span><span class="sxs-lookup"><span data-stu-id="8dc8a-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="8dc8a-112">Questo comando crea una definizione di set di criteri denominata VMPolicySetDefinition con metadati che indicano che la categoria è "Macchina virtuale" che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivo.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8dc8a-113">Il contenuto dell'VMPolicy.jsesempio è fornito sopra.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="8dc8a-114">Esempio 2: Creare una definizione di set di criteri con parametri</span><span class="sxs-lookup"><span data-stu-id="8dc8a-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="8dc8a-115">Questo comando crea una definizione di set di criteri con parametri denominata VMPolicySetDefinition che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivo.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8dc8a-116">Il contenuto dell'VMPolicy.jsesempio è fornito sopra.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="8dc8a-117">Esempio 3: Creare una definizione del set di criteri con gruppi di definizioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="8dc8a-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="8dc8a-118">Questo comando crea una definizione di set di criteri denominata VMPolicySetDefinition con il raggruppamento delle definizioni dei criteri specificate C:\VMPolicy.jsattivo.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8dc8a-119">Il contenuto dell'VMPolicy.jsesempio è fornito sopra.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="8dc8a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc8a-120">PARAMETERS</span></span>

### <span data-ttu-id="8dc8a-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8dc8a-121">-ApiVersion</span></span>
<span data-ttu-id="8dc8a-122">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8dc8a-123">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8dc8a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc8a-124">-DefaultProfile</span></span>
<span data-ttu-id="8dc8a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8dc8a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dc8a-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dc8a-126">-Description</span></span>
<span data-ttu-id="8dc8a-127">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="8dc8a-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8dc8a-128">-DisplayName</span></span>
<span data-ttu-id="8dc8a-129">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="8dc8a-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="8dc8a-130">-GroupDefinition</span></span>
<span data-ttu-id="8dc8a-131">Gruppi di definizione dei criteri per la definizione del nuovo set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="8dc8a-132">Può trattarsi del percorso di un file contenente i gruppi o dei gruppi come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="8dc8a-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc8a-133">-ManagementGroupName</span></span>
<span data-ttu-id="8dc8a-134">Nome del gruppo di gestione della definizione del nuovo set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="8dc8a-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8dc8a-135">-Metadata</span></span>
<span data-ttu-id="8dc8a-136">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-136">The metadata for policy set definition.</span></span> <span data-ttu-id="8dc8a-137">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="8dc8a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc8a-138">-Name</span></span>
<span data-ttu-id="8dc8a-139">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc8a-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8dc8a-140">-Parameter</span></span>
<span data-ttu-id="8dc8a-141">Dichiarazione dei parametri per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="8dc8a-142">Può trattarsi del percorso di un nome file contenente la dichiarazione dei parametri o della dichiarazione dei parametri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="8dc8a-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8dc8a-143">-PolicyDefinition</span></span>
<span data-ttu-id="8dc8a-144">Definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-144">The policy definitions.</span></span> <span data-ttu-id="8dc8a-145">Può trattarsi del percorso di un nome file contenente le definizioni dei criteri oppure delle definizioni dei criteri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc8a-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="8dc8a-146">-Pre</span></span>
<span data-ttu-id="8dc8a-147">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8dc8a-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dc8a-148">-SubscriptionId</span></span>
<span data-ttu-id="8dc8a-149">ID sottoscrizione della definizione del nuovo set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="8dc8a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc8a-150">-Confirm</span></span>
<span data-ttu-id="8dc8a-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc8a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc8a-152">-WhatIf</span></span>
<span data-ttu-id="8dc8a-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc8a-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc8a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc8a-155">CommonParameters</span></span>
<span data-ttu-id="8dc8a-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc8a-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8dc8a-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc8a-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="8dc8a-158">INPUTS</span></span>

### <span data-ttu-id="8dc8a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc8a-159">System.String</span></span>

### <span data-ttu-id="8dc8a-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8dc8a-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8dc8a-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dc8a-161">OUTPUTS</span></span>

### <span data-ttu-id="8dc8a-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8dc8a-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8dc8a-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="8dc8a-163">NOTES</span></span>

## <span data-ttu-id="8dc8a-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dc8a-164">RELATED LINKS</span></span>
