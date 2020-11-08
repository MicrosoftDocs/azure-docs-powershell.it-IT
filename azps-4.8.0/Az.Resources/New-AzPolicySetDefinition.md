---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189380"
---
# <span data-ttu-id="050dc-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="050dc-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="050dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="050dc-102">SYNOPSIS</span></span>
<span data-ttu-id="050dc-103">Crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="050dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="050dc-104">SYNTAX</span></span>

### <span data-ttu-id="050dc-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="050dc-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050dc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="050dc-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="050dc-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="050dc-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="050dc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="050dc-108">DESCRIPTION</span></span>
<span data-ttu-id="050dc-109">Il cmdlet **New-AzPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="050dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="050dc-110">EXAMPLES</span></span>

### <span data-ttu-id="050dc-111">Esempio 1: creare una definizione di set di criteri con i metadati tramite un file di set di criteri</span><span class="sxs-lookup"><span data-stu-id="050dc-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="050dc-112">Questo comando crea una definizione di set di criteri denominata VMPolicySetDefinition con metadati che indicano che la relativa categoria è "macchina virtuale" che contiene le definizioni di criteri specificate in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="050dc-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="050dc-113">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="050dc-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="050dc-114">Esempio 2: creare una definizione di set di criteri con parametri</span><span class="sxs-lookup"><span data-stu-id="050dc-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="050dc-115">Questo comando crea una definizione di set di criteri con parametri denominata VMPolicySetDefinition che contiene le definizioni di criteri specificate in C:\VMPolicy.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="050dc-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="050dc-116">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="050dc-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="050dc-117">Esempio 3: creare una definizione di set di criteri con i gruppi di definizione dei criteri</span><span class="sxs-lookup"><span data-stu-id="050dc-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="050dc-118">Questo comando crea una definizione di set di criteri denominata VMPolicySetDefinition con il raggruppamento di definizioni di criteri specificato in C:\VMPolicy.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="050dc-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="050dc-119">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="050dc-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="050dc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="050dc-120">PARAMETERS</span></span>

### <span data-ttu-id="050dc-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="050dc-121">-ApiVersion</span></span>
<span data-ttu-id="050dc-122">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="050dc-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="050dc-123">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="050dc-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="050dc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050dc-124">-DefaultProfile</span></span>
<span data-ttu-id="050dc-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="050dc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="050dc-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="050dc-126">-Description</span></span>
<span data-ttu-id="050dc-127">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="050dc-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="050dc-128">-DisplayName</span></span>
<span data-ttu-id="050dc-129">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="050dc-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="050dc-130">-GroupDefinition</span></span>
<span data-ttu-id="050dc-131">Gruppi di definizione dei criteri per la nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="050dc-132">Può essere un percorso di un file contenente i gruppi o i gruppi come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="050dc-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="050dc-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="050dc-133">-ManagementGroupName</span></span>
<span data-ttu-id="050dc-134">Nome del gruppo di gestione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="050dc-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="050dc-135">-Metadata</span></span>
<span data-ttu-id="050dc-136">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-136">The metadata for policy set definition.</span></span> <span data-ttu-id="050dc-137">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="050dc-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="050dc-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="050dc-138">-Name</span></span>
<span data-ttu-id="050dc-139">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="050dc-140">Parametro-</span><span class="sxs-lookup"><span data-stu-id="050dc-140">-Parameter</span></span>
<span data-ttu-id="050dc-141">Dichiarazione Parameters per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="050dc-142">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="050dc-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="050dc-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="050dc-143">-PolicyDefinition</span></span>
<span data-ttu-id="050dc-144">Definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-144">The policy definitions.</span></span> <span data-ttu-id="050dc-145">Può essere un percorso per un nome di file contenente le definizioni dei criteri o le definizioni dei criteri come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="050dc-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="050dc-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="050dc-146">-Pre</span></span>
<span data-ttu-id="050dc-147">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="050dc-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="050dc-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="050dc-148">-SubscriptionId</span></span>
<span data-ttu-id="050dc-149">ID sottoscrizione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="050dc-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="050dc-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="050dc-150">-Confirm</span></span>
<span data-ttu-id="050dc-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="050dc-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050dc-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050dc-152">-WhatIf</span></span>
<span data-ttu-id="050dc-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="050dc-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="050dc-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="050dc-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050dc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050dc-155">CommonParameters</span></span>
<span data-ttu-id="050dc-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050dc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050dc-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="050dc-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050dc-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="050dc-158">INPUTS</span></span>

### <span data-ttu-id="050dc-159">System. String</span><span class="sxs-lookup"><span data-stu-id="050dc-159">System.String</span></span>

### <span data-ttu-id="050dc-160">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="050dc-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="050dc-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="050dc-161">OUTPUTS</span></span>

### <span data-ttu-id="050dc-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="050dc-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="050dc-163">Note</span><span class="sxs-lookup"><span data-stu-id="050dc-163">NOTES</span></span>

## <span data-ttu-id="050dc-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="050dc-164">RELATED LINKS</span></span>
