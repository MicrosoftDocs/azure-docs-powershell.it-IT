---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 259b0abd120fb27eee1ca80da61266f4c890423f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972590"
---
# <span data-ttu-id="5bc42-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5bc42-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="5bc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc42-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc42-103">Crea una definizione di criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-103">Creates a policy definition.</span></span>

## <span data-ttu-id="5bc42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bc42-104">SYNTAX</span></span>

### <span data-ttu-id="5bc42-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="5bc42-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bc42-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc42-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bc42-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc42-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bc42-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5bc42-108">DESCRIPTION</span></span>
<span data-ttu-id="5bc42-109">Il cmdlet **New-AzPolicyDefinition** crea una definizione di criterio che include una regola del criterio in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="5bc42-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="5bc42-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bc42-110">EXAMPLES</span></span>

### <span data-ttu-id="5bc42-111">Esempio 1: Creare una definizione dei criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="5bc42-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="5bc42-112">Questo comando crea una definizione di criterio denominata LocationDefinition che contiene la regola del criterio specificata C:\LocationPolicy.jsattivo.</span><span class="sxs-lookup"><span data-stu-id="5bc42-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="5bc42-113">Il contenuto di esempio per LocationPolicy.jsfile è fornito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5bc42-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="5bc42-114">Esempio 2: Creare una definizione di criterio con parametri usando parametri inline</span><span class="sxs-lookup"><span data-stu-id="5bc42-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="5bc42-115">Questo comando crea una definizione di criterio denominata LocationDefinition che contiene la regola del criterio specificata C:\LocationPolicy.jsattivo.</span><span class="sxs-lookup"><span data-stu-id="5bc42-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="5bc42-116">La definizione del parametro per la regola dei criteri è fornita in linea.</span><span class="sxs-lookup"><span data-stu-id="5bc42-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="5bc42-117">Esempio 3: Creare una definizione dei criteri in linea in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5bc42-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="5bc42-118">Questo comando crea una definizione di criterio denominata VMPolicyDefinition nel gruppo di gestione Dept42.</span><span class="sxs-lookup"><span data-stu-id="5bc42-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="5bc42-119">Il comando specifica il criterio come stringa in formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="5bc42-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="5bc42-120">Esempio 4: Creare una definizione di criterio in linea con i metadati</span><span class="sxs-lookup"><span data-stu-id="5bc42-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="5bc42-121">Questo comando crea una definizione di criterio denominata VMPolicyDefinition con metadati che indicano che la categoria è "Macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="5bc42-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="5bc42-122">Il comando specifica il criterio come stringa in formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="5bc42-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="5bc42-123">Esempio 5: Creare una definizione di criterio in linea con la modalità</span><span class="sxs-lookup"><span data-stu-id="5bc42-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="5bc42-124">Questo comando crea una definizione di criterio denominata TagPolicyDefinition con modalità "Indicizzato" che indica che il criterio deve essere valutato solo per i tipi di risorse che supportano tag e posizione.</span><span class="sxs-lookup"><span data-stu-id="5bc42-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="5bc42-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc42-125">PARAMETERS</span></span>

### <span data-ttu-id="5bc42-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5bc42-126">-ApiVersion</span></span>
<span data-ttu-id="5bc42-127">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="5bc42-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5bc42-128">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="5bc42-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5bc42-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc42-129">-DefaultProfile</span></span>
<span data-ttu-id="5bc42-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5bc42-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bc42-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bc42-131">-Description</span></span>
<span data-ttu-id="5bc42-132">Specifica una descrizione per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="5bc42-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5bc42-133">-DisplayName</span></span>
<span data-ttu-id="5bc42-134">Specifica un nome visualizzato per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="5bc42-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc42-135">-ManagementGroupName</span></span>
<span data-ttu-id="5bc42-136">Nome del gruppo di gestione della definizione del nuovo criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="5bc42-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5bc42-137">-Metadata</span></span>
<span data-ttu-id="5bc42-138">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="5bc42-138">The metadata for policy definition.</span></span> <span data-ttu-id="5bc42-139">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="5bc42-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="5bc42-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="5bc42-140">-Mode</span></span>
<span data-ttu-id="5bc42-141">Modalità della definizione dei criteri</span><span class="sxs-lookup"><span data-stu-id="5bc42-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc42-142">-Name</span><span class="sxs-lookup"><span data-stu-id="5bc42-142">-Name</span></span>
<span data-ttu-id="5bc42-143">Specifica un nome per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="5bc42-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5bc42-144">-Parameter</span></span>
<span data-ttu-id="5bc42-145">Dichiarazione dei parametri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="5bc42-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="5bc42-146">Può trattarsi del percorso di un nome file contenente la dichiarazione dei parametri o della dichiarazione dei parametri come stringa.</span><span class="sxs-lookup"><span data-stu-id="5bc42-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="5bc42-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="5bc42-147">-Policy</span></span>
<span data-ttu-id="5bc42-148">Specifica una regola dei criteri per la definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="5bc42-149">È possibile specificare il percorso di un file JSON o di una stringa che contiene i criteri in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="5bc42-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="5bc42-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bc42-150">-Pre</span></span>
<span data-ttu-id="5bc42-151">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5bc42-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5bc42-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5bc42-152">-SubscriptionId</span></span>
<span data-ttu-id="5bc42-153">ID sottoscrizione della definizione del nuovo criterio.</span><span class="sxs-lookup"><span data-stu-id="5bc42-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="5bc42-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc42-154">CommonParameters</span></span>
<span data-ttu-id="5bc42-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc42-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc42-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bc42-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc42-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="5bc42-157">INPUTS</span></span>

### <span data-ttu-id="5bc42-158">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc42-158">System.String</span></span>

### <span data-ttu-id="5bc42-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5bc42-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5bc42-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bc42-160">OUTPUTS</span></span>

### <span data-ttu-id="5bc42-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5bc42-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5bc42-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="5bc42-162">NOTES</span></span>

## <span data-ttu-id="5bc42-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bc42-163">RELATED LINKS</span></span>

[<span data-ttu-id="5bc42-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5bc42-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="5bc42-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5bc42-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="5bc42-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5bc42-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


