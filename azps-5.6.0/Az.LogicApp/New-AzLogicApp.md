---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 98fb733f661d4d1c5a6c50ce472005763584a72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968957"
---
# <span data-ttu-id="ad9e5-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad9e5-101">New-AzLogicApp</span></span>

## <span data-ttu-id="ad9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9e5-103">Crea un'app per la logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="ad9e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad9e5-104">SYNTAX</span></span>

### <span data-ttu-id="ad9e5-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad9e5-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad9e5-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad9e5-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad9e5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad9e5-107">DESCRIPTION</span></span>
<span data-ttu-id="ad9e5-108">Il cmdlet **New-AzLogicApp** crea un'app per la logica usando la funzionalità App logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ad9e5-109">Un'app per la logica è una raccolta di azioni o trigger definiti nella definizione dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="ad9e5-110">Questo cmdlet restituisce un oggetto **flusso di** lavoro.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="ad9e5-111">È possibile creare un'app per la logica specificando un nome, un percorso, una definizione dell'app logica, un gruppo di risorse e un piano.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="ad9e5-112">La definizione e i parametri di un'app per logica sono formattati in JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="ad9e5-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="ad9e5-113">È possibile usare un'app per la logica come modello per la definizione e i parametri.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="ad9e5-114">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad9e5-115">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad9e5-116">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad9e5-117">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="ad9e5-118">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="ad9e5-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad9e5-119">EXAMPLES</span></span>

### <span data-ttu-id="ad9e5-120">Esempio 1: Creare un'app per la logica usando i percorsi dei file di definizione e dei parametri</span><span class="sxs-lookup"><span data-stu-id="ad9e5-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="ad9e5-121">Questo comando crea un'app per la logica nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="ad9e5-122">L'app per la logica include la definizione e i parametri specificati dai percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="ad9e5-123">Esempio 2: Creare un'app per la logica usando oggetti definizione e parametro</span><span class="sxs-lookup"><span data-stu-id="ad9e5-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="ad9e5-124">Questo comando crea un'app per la logica nel gruppo di risorse del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="ad9e5-125">Esempio 3: Creare un'app per la logica usando la pipeline per specificare il gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ad9e5-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="ad9e5-126">Questo comando recupera il gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ad9e5-127">Il comando passa il gruppo di risorse al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad9e5-128">Il cmdlet corrente crea un'app per la logica nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="ad9e5-129">L'app per la logica include la definizione e i parametri specificati dai percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="ad9e5-130">Esempio 4: Creare un'app per la logica basata su un'app logica esistente</span><span class="sxs-lookup"><span data-stu-id="ad9e5-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="ad9e5-131">Il primo comando ottiene l'app logica denominata LogicApp03 usando il cmdlet Get-AzLogicApp logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="ad9e5-132">Il comando archivia l'app per la logica nella $Workflow variabile.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="ad9e5-133">Il secondo comando crea una nuova app per la logica che usa la definizione e i parametri dell'app per la logica archiviati in $Workflow.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="ad9e5-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad9e5-134">PARAMETERS</span></span>

### <span data-ttu-id="ad9e5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9e5-135">-DefaultProfile</span></span>
<span data-ttu-id="ad9e5-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad9e5-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad9e5-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="ad9e5-137">-Definition</span></span>
<span data-ttu-id="ad9e5-138">Specifica la definizione per l'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="ad9e5-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="ad9e5-139">-DefinitionFilePath</span></span>
<span data-ttu-id="ad9e5-140">Specifica la definizione di un'app per la logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="ad9e5-141">-IntegrationAccountId</span></span>
<span data-ttu-id="ad9e5-142">Specifica un ID account di integrazione per l'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="ad9e5-143">-Location</span><span class="sxs-lookup"><span data-stu-id="ad9e5-143">-Location</span></span>
<span data-ttu-id="ad9e5-144">Specifica la posizione dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="ad9e5-145">Immettere la posizione di un data center di Azure, ad esempio Stati Uniti occidentali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="ad9e5-146">È possibile inserire un'app per la logica in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="ad9e5-147">-Name</span><span class="sxs-lookup"><span data-stu-id="ad9e5-147">-Name</span></span>
<span data-ttu-id="ad9e5-148">Specifica il nome per l'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="ad9e5-149">-ParameterFilePath</span></span>
<span data-ttu-id="ad9e5-150">Specifica il percorso di un file di parametri in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="ad9e5-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ad9e5-151">-Parameters</span></span>
<span data-ttu-id="ad9e5-152">Specifica un oggetto raccolta di parametri per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="ad9e5-153">Specificare una tabella hash, \<string\> un dizionario o un \<string, WorkflowParameter\> dizionario.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9e5-154">-ResourceGroupName</span></span>
<span data-ttu-id="ad9e5-155">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad9e5-156">-State</span><span class="sxs-lookup"><span data-stu-id="ad9e5-156">-State</span></span>
<span data-ttu-id="ad9e5-157">Specifica lo stato dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="ad9e5-158">I valori accettabili per questo parametro sono: Abilitato e Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad9e5-159">-Confirm</span></span>
<span data-ttu-id="ad9e5-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9e5-161">-WhatIf</span></span>
<span data-ttu-id="ad9e5-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad9e5-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9e5-164">CommonParameters</span></span>
<span data-ttu-id="ad9e5-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad9e5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9e5-166">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad9e5-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9e5-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad9e5-167">INPUTS</span></span>

### <span data-ttu-id="ad9e5-168">System.String</span><span class="sxs-lookup"><span data-stu-id="ad9e5-168">System.String</span></span>

## <span data-ttu-id="ad9e5-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad9e5-169">OUTPUTS</span></span>

### <span data-ttu-id="ad9e5-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad9e5-170">System.Object</span></span>

## <span data-ttu-id="ad9e5-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad9e5-171">NOTES</span></span>

## <span data-ttu-id="ad9e5-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad9e5-172">RELATED LINKS</span></span>

[<span data-ttu-id="ad9e5-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad9e5-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="ad9e5-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad9e5-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="ad9e5-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad9e5-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ad9e5-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad9e5-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


