---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: c5de339929e44433efdee64de0257c62845c5b26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862490"
---
# <span data-ttu-id="78ec4-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="78ec4-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="78ec4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="78ec4-103">Crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="78ec4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78ec4-104">SYNTAX</span></span>

### <span data-ttu-id="78ec4-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78ec4-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78ec4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78ec4-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78ec4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78ec4-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78ec4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78ec4-108">DESCRIPTION</span></span>
<span data-ttu-id="78ec4-109">Il cmdlet **New-AzPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="78ec4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78ec4-110">EXAMPLES</span></span>

### <span data-ttu-id="78ec4-111">Esempio 1: creare una definizione di set di criteri usando un file di set di criteri</span><span class="sxs-lookup"><span data-stu-id="78ec4-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="78ec4-112">Questo comando crea una definizione di set di criteri denominata VMPolicyDefinition che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="78ec4-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="78ec4-113">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="78ec4-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="78ec4-114">Esempio 2: creare una definizione di set di criteri con parametri</span><span class="sxs-lookup"><span data-stu-id="78ec4-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="78ec4-115">Questo comando crea una definizione di set di criteri con parametri denominata VMPolicyDefinition che contiene le definizioni di criteri specificate in C:\VMPolicy.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="78ec4-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="78ec4-116">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="78ec4-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="78ec4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78ec4-117">PARAMETERS</span></span>

### <span data-ttu-id="78ec4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78ec4-118">-ApiVersion</span></span>
<span data-ttu-id="78ec4-119">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="78ec4-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="78ec4-120">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="78ec4-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="78ec4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ec4-121">-DefaultProfile</span></span>
<span data-ttu-id="78ec4-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78ec4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78ec4-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="78ec4-123">-Description</span></span>
<span data-ttu-id="78ec4-124">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="78ec4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78ec4-125">-DisplayName</span></span>
<span data-ttu-id="78ec4-126">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="78ec4-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="78ec4-127">-ManagementGroupName</span></span>
<span data-ttu-id="78ec4-128">Nome del gruppo di gestione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="78ec4-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="78ec4-129">-Metadata</span></span>
<span data-ttu-id="78ec4-130">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-130">The metadata for policy set definition.</span></span> <span data-ttu-id="78ec4-131">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="78ec4-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="78ec4-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="78ec4-132">-Name</span></span>
<span data-ttu-id="78ec4-133">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="78ec4-134">Parametro-</span><span class="sxs-lookup"><span data-stu-id="78ec4-134">-Parameter</span></span>
<span data-ttu-id="78ec4-135">Dichiarazione Parameters per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="78ec4-136">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="78ec4-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="78ec4-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="78ec4-137">-PolicyDefinition</span></span>
<span data-ttu-id="78ec4-138">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-138">The policy set definition.</span></span> <span data-ttu-id="78ec4-139">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="78ec4-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="78ec4-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="78ec4-140">-Pre</span></span>
<span data-ttu-id="78ec4-141">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="78ec4-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="78ec4-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78ec4-142">-SubscriptionId</span></span>
<span data-ttu-id="78ec4-143">ID sottoscrizione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="78ec4-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="78ec4-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78ec4-144">-Confirm</span></span>
<span data-ttu-id="78ec4-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ec4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ec4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ec4-146">-WhatIf</span></span>
<span data-ttu-id="78ec4-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78ec4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78ec4-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78ec4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ec4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ec4-149">CommonParameters</span></span>
<span data-ttu-id="78ec4-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ec4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ec4-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ec4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ec4-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78ec4-152">INPUTS</span></span>

### <span data-ttu-id="78ec4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="78ec4-153">System.String</span></span>

### <span data-ttu-id="78ec4-154">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="78ec4-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="78ec4-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78ec4-155">OUTPUTS</span></span>

### <span data-ttu-id="78ec4-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="78ec4-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="78ec4-157">Note</span><span class="sxs-lookup"><span data-stu-id="78ec4-157">NOTES</span></span>

## <span data-ttu-id="78ec4-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78ec4-158">RELATED LINKS</span></span>
