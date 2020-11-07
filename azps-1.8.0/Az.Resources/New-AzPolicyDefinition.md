---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 07882064fae3cfc4a24899b6106480551f3681a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677345"
---
# <span data-ttu-id="e7aba-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7aba-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="e7aba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7aba-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aba-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-103">Creates a policy definition.</span></span>

## <span data-ttu-id="e7aba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7aba-104">SYNTAX</span></span>

### <span data-ttu-id="e7aba-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7aba-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7aba-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7aba-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7aba-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7aba-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7aba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7aba-108">DESCRIPTION</span></span>
<span data-ttu-id="e7aba-109">Il cmdlet **New-AzPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e7aba-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="e7aba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7aba-110">EXAMPLES</span></span>

### <span data-ttu-id="e7aba-111">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="e7aba-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="e7aba-112">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="e7aba-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="e7aba-113">Il contenuto di esempio per il LocationPolicy.jsnel file è specificato sopra.</span><span class="sxs-lookup"><span data-stu-id="e7aba-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="e7aba-114">Esempio 2: creare una definizione di criteri con parametri usando i valori inline</span><span class="sxs-lookup"><span data-stu-id="e7aba-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="e7aba-115">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="e7aba-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="e7aba-116">La definizione di parametro per la regola dei criteri viene fornita in linea.</span><span class="sxs-lookup"><span data-stu-id="e7aba-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="e7aba-117">Esempio 3: creare una definizione di criteri in linea in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="e7aba-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="e7aba-118">Questo comando crea una definizione di criteri denominata VMPolicyDefinition nel gruppo di gestione Dept42.</span><span class="sxs-lookup"><span data-stu-id="e7aba-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="e7aba-119">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="e7aba-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="e7aba-120">Esempio 4: creare una definizione di criteri in linea con i metadati</span><span class="sxs-lookup"><span data-stu-id="e7aba-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="e7aba-121">Questo comando crea una definizione di criteri denominata VMPolicyDefinition con i metadati che indicano che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="e7aba-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="e7aba-122">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="e7aba-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="e7aba-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7aba-123">PARAMETERS</span></span>

### <span data-ttu-id="e7aba-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e7aba-124">-ApiVersion</span></span>
<span data-ttu-id="e7aba-125">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e7aba-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e7aba-126">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e7aba-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e7aba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aba-127">-DefaultProfile</span></span>
<span data-ttu-id="e7aba-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e7aba-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7aba-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7aba-129">-Description</span></span>
<span data-ttu-id="e7aba-130">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="e7aba-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e7aba-131">-DisplayName</span></span>
<span data-ttu-id="e7aba-132">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="e7aba-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aba-133">-ManagementGroupName</span></span>
<span data-ttu-id="e7aba-134">Nome del gruppo di gestione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-134">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="e7aba-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e7aba-135">-Metadata</span></span>
<span data-ttu-id="e7aba-136">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-136">The metadata for policy definition.</span></span> <span data-ttu-id="e7aba-137">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="e7aba-137">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="e7aba-138">-Modalità</span><span class="sxs-lookup"><span data-stu-id="e7aba-138">-Mode</span></span>
<span data-ttu-id="e7aba-139">Modalità della definizione del criterio</span><span class="sxs-lookup"><span data-stu-id="e7aba-139">The mode of the policy definition</span></span>

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

### <span data-ttu-id="e7aba-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7aba-140">-Name</span></span>
<span data-ttu-id="e7aba-141">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-141">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="e7aba-142">Parametro-</span><span class="sxs-lookup"><span data-stu-id="e7aba-142">-Parameter</span></span>
<span data-ttu-id="e7aba-143">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-143">The parameters declaration for policy definition.</span></span> <span data-ttu-id="e7aba-144">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="e7aba-144">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e7aba-145">-Policy</span><span class="sxs-lookup"><span data-stu-id="e7aba-145">-Policy</span></span>
<span data-ttu-id="e7aba-146">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-146">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="e7aba-147">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="e7aba-147">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="e7aba-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="e7aba-148">-Pre</span></span>
<span data-ttu-id="e7aba-149">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e7aba-149">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e7aba-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7aba-150">-SubscriptionId</span></span>
<span data-ttu-id="e7aba-151">ID sottoscrizione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e7aba-151">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="e7aba-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aba-152">CommonParameters</span></span>
<span data-ttu-id="e7aba-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7aba-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aba-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7aba-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aba-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7aba-155">INPUTS</span></span>

### <span data-ttu-id="e7aba-156">System. String</span><span class="sxs-lookup"><span data-stu-id="e7aba-156">System.String</span></span>

### <span data-ttu-id="e7aba-157">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7aba-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e7aba-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7aba-158">OUTPUTS</span></span>

### <span data-ttu-id="e7aba-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e7aba-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e7aba-160">Note</span><span class="sxs-lookup"><span data-stu-id="e7aba-160">NOTES</span></span>

## <span data-ttu-id="e7aba-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7aba-161">RELATED LINKS</span></span>

[<span data-ttu-id="e7aba-162">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7aba-162">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="e7aba-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7aba-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="e7aba-164">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7aba-164">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


