---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 1c3b18d5e098e19a8259f3b8faf06adcc25f7333
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854841"
---
# <span data-ttu-id="93acc-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="93acc-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="93acc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93acc-102">SYNOPSIS</span></span>
<span data-ttu-id="93acc-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-103">Creates a policy definition.</span></span>

## <span data-ttu-id="93acc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93acc-104">SYNTAX</span></span>

### <span data-ttu-id="93acc-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93acc-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93acc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93acc-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93acc-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93acc-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93acc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93acc-108">DESCRIPTION</span></span>
<span data-ttu-id="93acc-109">Il cmdlet **New-AzPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="93acc-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="93acc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93acc-110">EXAMPLES</span></span>

### <span data-ttu-id="93acc-111">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="93acc-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="93acc-112">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="93acc-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="93acc-113">Il contenuto di esempio per il LocationPolicy.jsnel file è specificato sopra.</span><span class="sxs-lookup"><span data-stu-id="93acc-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="93acc-114">Esempio 2: creare una definizione di criteri con parametri usando i valori inline</span><span class="sxs-lookup"><span data-stu-id="93acc-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="93acc-115">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="93acc-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="93acc-116">La definizione di parametro per la regola dei criteri viene fornita in linea.</span><span class="sxs-lookup"><span data-stu-id="93acc-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="93acc-117">Esempio 3: creare una definizione di criteri in linea in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="93acc-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="93acc-118">Questo comando crea una definizione di criteri denominata VMPolicyDefinition nel gruppo di gestione Dept42.</span><span class="sxs-lookup"><span data-stu-id="93acc-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="93acc-119">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="93acc-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="93acc-120">Esempio 4: creare una definizione di criteri in linea con i metadati</span><span class="sxs-lookup"><span data-stu-id="93acc-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="93acc-121">Questo comando crea una definizione di criteri denominata VMPolicyDefinition con i metadati che indicano che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="93acc-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="93acc-122">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="93acc-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="93acc-123">Esempio 5: creare una definizione di criteri in linea con la modalità</span><span class="sxs-lookup"><span data-stu-id="93acc-123">Example 5: Create a policy definition inline with mode</span></span>
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

<span data-ttu-id="93acc-124">Questo comando crea una definizione di criteri denominata TagsPolicyDefinition con la modalità "indicizzata" che indica che il criterio deve essere valutato solo per i tipi di risorsa che supportano i tag e la posizione.</span><span class="sxs-lookup"><span data-stu-id="93acc-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="93acc-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93acc-125">PARAMETERS</span></span>

### <span data-ttu-id="93acc-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93acc-126">-ApiVersion</span></span>
<span data-ttu-id="93acc-127">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="93acc-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="93acc-128">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="93acc-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="93acc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93acc-129">-DefaultProfile</span></span>
<span data-ttu-id="93acc-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93acc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93acc-131">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="93acc-131">-Description</span></span>
<span data-ttu-id="93acc-132">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="93acc-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="93acc-133">-DisplayName</span></span>
<span data-ttu-id="93acc-134">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="93acc-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="93acc-135">-ManagementGroupName</span></span>
<span data-ttu-id="93acc-136">Nome del gruppo di gestione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="93acc-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="93acc-137">-Metadata</span></span>
<span data-ttu-id="93acc-138">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-138">The metadata for policy definition.</span></span> <span data-ttu-id="93acc-139">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="93acc-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="93acc-140">-Modalità</span><span class="sxs-lookup"><span data-stu-id="93acc-140">-Mode</span></span>
<span data-ttu-id="93acc-141">Modalità della definizione del criterio</span><span class="sxs-lookup"><span data-stu-id="93acc-141">The mode of the policy definition</span></span>

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

### <span data-ttu-id="93acc-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="93acc-142">-Name</span></span>
<span data-ttu-id="93acc-143">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="93acc-144">Parametro-</span><span class="sxs-lookup"><span data-stu-id="93acc-144">-Parameter</span></span>
<span data-ttu-id="93acc-145">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="93acc-146">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="93acc-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="93acc-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="93acc-147">-Policy</span></span>
<span data-ttu-id="93acc-148">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="93acc-149">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="93acc-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="93acc-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="93acc-150">-Pre</span></span>
<span data-ttu-id="93acc-151">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="93acc-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="93acc-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93acc-152">-SubscriptionId</span></span>
<span data-ttu-id="93acc-153">ID sottoscrizione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="93acc-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="93acc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93acc-154">CommonParameters</span></span>
<span data-ttu-id="93acc-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93acc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93acc-156">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93acc-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93acc-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93acc-157">INPUTS</span></span>

### <span data-ttu-id="93acc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="93acc-158">System.String</span></span>

### <span data-ttu-id="93acc-159">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="93acc-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="93acc-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93acc-160">OUTPUTS</span></span>

### <span data-ttu-id="93acc-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="93acc-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="93acc-162">Note</span><span class="sxs-lookup"><span data-stu-id="93acc-162">NOTES</span></span>

## <span data-ttu-id="93acc-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93acc-163">RELATED LINKS</span></span>

[<span data-ttu-id="93acc-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="93acc-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="93acc-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="93acc-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="93acc-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="93acc-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


