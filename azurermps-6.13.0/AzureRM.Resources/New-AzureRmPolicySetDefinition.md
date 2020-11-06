---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 44cf09bdbf3f7be5a30a1b48831e975b3f42e693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507315"
---
# <span data-ttu-id="488d1-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="488d1-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="488d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="488d1-102">SYNOPSIS</span></span>
<span data-ttu-id="488d1-103">Crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="488d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="488d1-104">SYNTAX</span></span>

### <span data-ttu-id="488d1-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="488d1-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="488d1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="488d1-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="488d1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="488d1-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="488d1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="488d1-108">DESCRIPTION</span></span>
<span data-ttu-id="488d1-109">Il cmdlet **New-AzureRmPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-109">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="488d1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="488d1-110">EXAMPLES</span></span>

### <span data-ttu-id="488d1-111">Esempio 1: creare una definizione di set di criteri usando un file di set di criteri</span><span class="sxs-lookup"><span data-stu-id="488d1-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="488d1-112">Questo comando crea una definizione di set di criteri denominata VMPolicyDefinition che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="488d1-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="488d1-113">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="488d1-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="488d1-114">Esempio 2: creare una definizione di set di criteri con parametri</span><span class="sxs-lookup"><span data-stu-id="488d1-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="488d1-115">Questo comando crea una definizione di set di criteri con parametri denominata VMPolicyDefinition che contiene le definizioni di criteri specificate in C:\VMPolicy.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="488d1-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="488d1-116">Il contenuto di esempio della VMPolicy.jsattivata è disponibile sopra.</span><span class="sxs-lookup"><span data-stu-id="488d1-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="488d1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="488d1-117">PARAMETERS</span></span>

### <span data-ttu-id="488d1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="488d1-118">-ApiVersion</span></span>
<span data-ttu-id="488d1-119">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="488d1-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="488d1-120">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="488d1-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="488d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488d1-121">-DefaultProfile</span></span>
<span data-ttu-id="488d1-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="488d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="488d1-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="488d1-123">-Description</span></span>
<span data-ttu-id="488d1-124">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="488d1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="488d1-125">-DisplayName</span></span>
<span data-ttu-id="488d1-126">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="488d1-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="488d1-127">-ManagementGroupName</span></span>
<span data-ttu-id="488d1-128">Nome del gruppo di gestione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="488d1-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="488d1-129">-Metadata</span></span>
<span data-ttu-id="488d1-130">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-130">The metadata for policy set definition.</span></span> <span data-ttu-id="488d1-131">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="488d1-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="488d1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="488d1-132">-Name</span></span>
<span data-ttu-id="488d1-133">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="488d1-134">Parametro-</span><span class="sxs-lookup"><span data-stu-id="488d1-134">-Parameter</span></span>
<span data-ttu-id="488d1-135">Dichiarazione Parameters per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="488d1-136">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="488d1-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="488d1-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="488d1-137">-PolicyDefinition</span></span>
<span data-ttu-id="488d1-138">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-138">The policy set definition.</span></span> <span data-ttu-id="488d1-139">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="488d1-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="488d1-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="488d1-140">-Pre</span></span>
<span data-ttu-id="488d1-141">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="488d1-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="488d1-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="488d1-142">-SubscriptionId</span></span>
<span data-ttu-id="488d1-143">ID sottoscrizione della nuova definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="488d1-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="488d1-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="488d1-144">-Confirm</span></span>
<span data-ttu-id="488d1-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="488d1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="488d1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="488d1-146">-WhatIf</span></span>
<span data-ttu-id="488d1-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488d1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="488d1-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488d1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="488d1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488d1-149">CommonParameters</span></span>
<span data-ttu-id="488d1-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="488d1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488d1-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488d1-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488d1-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="488d1-152">INPUTS</span></span>

### <span data-ttu-id="488d1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="488d1-153">System.String</span></span>

### <span data-ttu-id="488d1-154">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="488d1-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="488d1-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="488d1-155">OUTPUTS</span></span>

### <span data-ttu-id="488d1-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="488d1-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="488d1-157">Note</span><span class="sxs-lookup"><span data-stu-id="488d1-157">NOTES</span></span>

## <span data-ttu-id="488d1-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="488d1-158">RELATED LINKS</span></span>