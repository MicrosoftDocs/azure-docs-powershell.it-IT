---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 8879f013983888ff0400c0f43ec4e570c495760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862493"
---
# <span data-ttu-id="db9d2-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db9d2-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="db9d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="db9d2-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-103">Creates a policy definition.</span></span>

## <span data-ttu-id="db9d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db9d2-104">SYNTAX</span></span>

### <span data-ttu-id="db9d2-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db9d2-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="db9d2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9d2-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="db9d2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9d2-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="db9d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db9d2-108">DESCRIPTION</span></span>
<span data-ttu-id="db9d2-109">Il cmdlet **New-AzPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="db9d2-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="db9d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db9d2-110">EXAMPLES</span></span>

### <span data-ttu-id="db9d2-111">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="db9d2-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="db9d2-112">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="db9d2-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="db9d2-113">Il contenuto di esempio per il LocationPolicy.jsnel file è specificato sopra.</span><span class="sxs-lookup"><span data-stu-id="db9d2-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="db9d2-114">Esempio 2: creare una definizione di criteri con parametri usando i valori inline</span><span class="sxs-lookup"><span data-stu-id="db9d2-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="db9d2-115">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="db9d2-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="db9d2-116">La definizione di parametro per la regola dei criteri viene fornita in linea.</span><span class="sxs-lookup"><span data-stu-id="db9d2-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="db9d2-117">Esempio 3: creare una definizione di criteri in linea in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="db9d2-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="db9d2-118">Questo comando crea una definizione di criteri denominata VMPolicyDefinition nel gruppo di gestione Dept42.</span><span class="sxs-lookup"><span data-stu-id="db9d2-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="db9d2-119">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="db9d2-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="db9d2-120">Esempio 4: creare una definizione di criteri in linea con i metadati</span><span class="sxs-lookup"><span data-stu-id="db9d2-120">Example 4: Create a policy definition inline with metadata</span></span>
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

<span data-ttu-id="db9d2-121">Questo comando crea una definizione di criteri denominata VMPolicyDefinition con i metadati che indicano che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="db9d2-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="db9d2-122">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="db9d2-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="db9d2-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db9d2-123">PARAMETERS</span></span>

### <span data-ttu-id="db9d2-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="db9d2-124">-ApiVersion</span></span>
<span data-ttu-id="db9d2-125">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="db9d2-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="db9d2-126">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="db9d2-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="db9d2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9d2-127">-DefaultProfile</span></span>
<span data-ttu-id="db9d2-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db9d2-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db9d2-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="db9d2-129">-Description</span></span>
<span data-ttu-id="db9d2-130">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="db9d2-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db9d2-131">-DisplayName</span></span>
<span data-ttu-id="db9d2-132">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="db9d2-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="db9d2-133">-InformationAction</span></span>
<span data-ttu-id="db9d2-134">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="db9d2-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="db9d2-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="db9d2-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db9d2-136">Continuare</span><span class="sxs-lookup"><span data-stu-id="db9d2-136">Continue</span></span>
- <span data-ttu-id="db9d2-137">Ignora</span><span class="sxs-lookup"><span data-stu-id="db9d2-137">Ignore</span></span>
- <span data-ttu-id="db9d2-138">Informarsi</span><span class="sxs-lookup"><span data-stu-id="db9d2-138">Inquire</span></span>
- <span data-ttu-id="db9d2-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="db9d2-139">SilentlyContinue</span></span>
- <span data-ttu-id="db9d2-140">Stop</span><span class="sxs-lookup"><span data-stu-id="db9d2-140">Stop</span></span>
- <span data-ttu-id="db9d2-141">Sospensione</span><span class="sxs-lookup"><span data-stu-id="db9d2-141">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9d2-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="db9d2-142">-InformationVariable</span></span>
<span data-ttu-id="db9d2-143">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="db9d2-143">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9d2-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="db9d2-144">-ManagementGroupName</span></span>
<span data-ttu-id="db9d2-145">Nome del gruppo di gestione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="db9d2-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="db9d2-146">-Metadata</span></span>
<span data-ttu-id="db9d2-147">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-147">The metadata for policy definition.</span></span> <span data-ttu-id="db9d2-148">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="db9d2-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="db9d2-149">-Modalità</span><span class="sxs-lookup"><span data-stu-id="db9d2-149">-Mode</span></span>
<span data-ttu-id="db9d2-150">Modalità della definizione del criterio</span><span class="sxs-lookup"><span data-stu-id="db9d2-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9d2-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="db9d2-151">-Name</span></span>
<span data-ttu-id="db9d2-152">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="db9d2-153">Parametro-</span><span class="sxs-lookup"><span data-stu-id="db9d2-153">-Parameter</span></span>
<span data-ttu-id="db9d2-154">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="db9d2-155">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="db9d2-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="db9d2-156">-Policy</span><span class="sxs-lookup"><span data-stu-id="db9d2-156">-Policy</span></span>
<span data-ttu-id="db9d2-157">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="db9d2-158">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="db9d2-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="db9d2-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="db9d2-159">-Pre</span></span>
<span data-ttu-id="db9d2-160">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="db9d2-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db9d2-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db9d2-161">-SubscriptionId</span></span>
<span data-ttu-id="db9d2-162">ID sottoscrizione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="db9d2-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="db9d2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9d2-163">CommonParameters</span></span>
<span data-ttu-id="db9d2-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9d2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9d2-165">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9d2-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9d2-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db9d2-166">INPUTS</span></span>

## <span data-ttu-id="db9d2-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db9d2-167">OUTPUTS</span></span>

## <span data-ttu-id="db9d2-168">Note</span><span class="sxs-lookup"><span data-stu-id="db9d2-168">NOTES</span></span>

## <span data-ttu-id="db9d2-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db9d2-169">RELATED LINKS</span></span>

[<span data-ttu-id="db9d2-170">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db9d2-170">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="db9d2-171">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db9d2-171">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="db9d2-172">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db9d2-172">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


