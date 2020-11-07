---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685417"
---
# <span data-ttu-id="d4a75-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4a75-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d4a75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4a75-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a75-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4a75-104">SYNTAX</span></span>

### <span data-ttu-id="d4a75-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4a75-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4a75-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a75-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4a75-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4a75-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4a75-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4a75-108">DESCRIPTION</span></span>
<span data-ttu-id="d4a75-109">Il cmdlet **New-AzureRmPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="d4a75-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="d4a75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4a75-110">EXAMPLES</span></span>

### <span data-ttu-id="d4a75-111">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="d4a75-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="d4a75-112">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="d4a75-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="d4a75-113">Il contenuto di esempio per il LocationPolicy.jsnel file è specificato sopra.</span><span class="sxs-lookup"><span data-stu-id="d4a75-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="d4a75-114">Esempio 2: creare una definizione di criteri con parametri usando i valori inline</span><span class="sxs-lookup"><span data-stu-id="d4a75-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="d4a75-115">Questo comando crea una definizione di criteri denominata LocationDefinition che contiene la regola di criteri specificata in C:\LocationPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="d4a75-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="d4a75-116">La definizione di parametro per la regola dei criteri viene fornita in linea.</span><span class="sxs-lookup"><span data-stu-id="d4a75-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="d4a75-117">Esempio 3: creare una definizione di criteri in linea in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="d4a75-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="d4a75-118">Questo comando crea una definizione di criteri denominata VMPolicyDefinition nel gruppo di gestione Dept42.</span><span class="sxs-lookup"><span data-stu-id="d4a75-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="d4a75-119">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="d4a75-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="d4a75-120">Esempio 4: creare una definizione di criteri in linea con i metadati</span><span class="sxs-lookup"><span data-stu-id="d4a75-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="d4a75-121">Questo comando crea una definizione di criteri denominata VMPolicyDefinition con i metadati che indicano che la relativa categoria è "macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="d4a75-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="d4a75-122">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="d4a75-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="d4a75-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4a75-123">PARAMETERS</span></span>

### <span data-ttu-id="d4a75-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4a75-124">-ApiVersion</span></span>
<span data-ttu-id="d4a75-125">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d4a75-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4a75-126">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d4a75-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d4a75-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a75-127">-DefaultProfile</span></span>
<span data-ttu-id="d4a75-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d4a75-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4a75-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4a75-129">-Description</span></span>
<span data-ttu-id="d4a75-130">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="d4a75-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d4a75-131">-DisplayName</span></span>
<span data-ttu-id="d4a75-132">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="d4a75-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d4a75-133">-InformationAction</span></span>
<span data-ttu-id="d4a75-134">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d4a75-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d4a75-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4a75-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4a75-136">Continuare</span><span class="sxs-lookup"><span data-stu-id="d4a75-136">Continue</span></span>
- <span data-ttu-id="d4a75-137">Ignora</span><span class="sxs-lookup"><span data-stu-id="d4a75-137">Ignore</span></span>
- <span data-ttu-id="d4a75-138">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d4a75-138">Inquire</span></span>
- <span data-ttu-id="d4a75-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4a75-139">SilentlyContinue</span></span>
- <span data-ttu-id="d4a75-140">Stop</span><span class="sxs-lookup"><span data-stu-id="d4a75-140">Stop</span></span>
- <span data-ttu-id="d4a75-141">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d4a75-141">Suspend</span></span>

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

### <span data-ttu-id="d4a75-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4a75-142">-InformationVariable</span></span>
<span data-ttu-id="d4a75-143">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d4a75-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d4a75-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a75-144">-ManagementGroupName</span></span>
<span data-ttu-id="d4a75-145">Nome del gruppo di gestione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="d4a75-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d4a75-146">-Metadata</span></span>
<span data-ttu-id="d4a75-147">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-147">The metadata for policy definition.</span></span> <span data-ttu-id="d4a75-148">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="d4a75-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="d4a75-149">-Modalità</span><span class="sxs-lookup"><span data-stu-id="d4a75-149">-Mode</span></span>
<span data-ttu-id="d4a75-150">Modalità della definizione del criterio</span><span class="sxs-lookup"><span data-stu-id="d4a75-150">The mode of the policy definition</span></span>

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

### <span data-ttu-id="d4a75-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4a75-151">-Name</span></span>
<span data-ttu-id="d4a75-152">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="d4a75-153">Parametro-</span><span class="sxs-lookup"><span data-stu-id="d4a75-153">-Parameter</span></span>
<span data-ttu-id="d4a75-154">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d4a75-155">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="d4a75-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d4a75-156">-Policy</span><span class="sxs-lookup"><span data-stu-id="d4a75-156">-Policy</span></span>
<span data-ttu-id="d4a75-157">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="d4a75-158">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="d4a75-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="d4a75-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4a75-159">-Pre</span></span>
<span data-ttu-id="d4a75-160">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d4a75-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d4a75-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4a75-161">-SubscriptionId</span></span>
<span data-ttu-id="d4a75-162">ID sottoscrizione della nuova definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d4a75-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="d4a75-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a75-163">CommonParameters</span></span>
<span data-ttu-id="d4a75-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a75-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a75-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a75-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a75-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4a75-166">INPUTS</span></span>

## <span data-ttu-id="d4a75-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4a75-167">OUTPUTS</span></span>

## <span data-ttu-id="d4a75-168">Note</span><span class="sxs-lookup"><span data-stu-id="d4a75-168">NOTES</span></span>

## <span data-ttu-id="d4a75-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4a75-169">RELATED LINKS</span></span>

[<span data-ttu-id="d4a75-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4a75-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d4a75-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4a75-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d4a75-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4a75-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


