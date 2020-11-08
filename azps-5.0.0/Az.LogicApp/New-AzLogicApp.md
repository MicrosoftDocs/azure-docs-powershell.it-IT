---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203603"
---
# <span data-ttu-id="e5999-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e5999-101">New-AzLogicApp</span></span>

## <span data-ttu-id="e5999-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5999-102">SYNOPSIS</span></span>
<span data-ttu-id="e5999-103">Crea un'app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5999-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="e5999-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5999-104">SYNTAX</span></span>

### <span data-ttu-id="e5999-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5999-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5999-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5999-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5999-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5999-107">DESCRIPTION</span></span>
<span data-ttu-id="e5999-108">Il cmdlet **New-AzLogicApp** crea un'app logica usando la funzionalità delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="e5999-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="e5999-109">Un'app logica è una raccolta di azioni o trigger definiti nella definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="e5999-110">Questo cmdlet restituisce un oggetto **flusso di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="e5999-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="e5999-111">Puoi creare un'app logica specificando un nome, una posizione, una definizione di app logica, un gruppo di risorse e un piano.</span><span class="sxs-lookup"><span data-stu-id="e5999-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="e5999-112">La definizione e i parametri delle app logiche sono formattati in JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e5999-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="e5999-113">Puoi usare un'app logica come modello per la definizione e i parametri.</span><span class="sxs-lookup"><span data-stu-id="e5999-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="e5999-114">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="e5999-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e5999-115">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="e5999-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e5999-116">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="e5999-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e5999-117">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="e5999-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e5999-118">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="e5999-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="e5999-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5999-119">EXAMPLES</span></span>

### <span data-ttu-id="e5999-120">Esempio 1: creare un'app logica usando i percorsi di definizione e di file dei parametri</span><span class="sxs-lookup"><span data-stu-id="e5999-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
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

<span data-ttu-id="e5999-121">Questo comando crea un'app logica nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e5999-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="e5999-122">L'app logica include la definizione e i parametri specificati dai percorsi dei file.</span><span class="sxs-lookup"><span data-stu-id="e5999-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e5999-123">Esempio 2: creare un'app logica usando la definizione e gli oggetti Parameter</span><span class="sxs-lookup"><span data-stu-id="e5999-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
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

<span data-ttu-id="e5999-124">Questo comando crea un'app logica nel gruppo risorse del gruppo risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e5999-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="e5999-125">Esempio 3: creare un'app logica usando la pipeline per specificare il gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e5999-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
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

<span data-ttu-id="e5999-126">Questo comando consente di ottenere il gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e5999-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e5999-127">Il comando passa il gruppo di risorse al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5999-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5999-128">Il cmdlet corrente crea un'app logica nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5999-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="e5999-129">L'app logica include la definizione e i parametri specificati dai percorsi dei file.</span><span class="sxs-lookup"><span data-stu-id="e5999-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="e5999-130">Esempio 4: creare un'app logica in base a un'app logica esistente</span><span class="sxs-lookup"><span data-stu-id="e5999-130">Example 4: Create a logic app based on an existing logic app</span></span>
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

<span data-ttu-id="e5999-131">Il primo comando consente di ottenere l'app logica denominata LogicApp03 usando il cmdlet Get-AzLogicApp.</span><span class="sxs-lookup"><span data-stu-id="e5999-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="e5999-132">Il comando Archivia l'app logica nella variabile $Workflow.</span><span class="sxs-lookup"><span data-stu-id="e5999-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="e5999-133">Il secondo comando crea una nuova app logica che usa la definizione e i parametri dell'app logica archiviata in $Workflow.</span><span class="sxs-lookup"><span data-stu-id="e5999-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="e5999-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5999-134">PARAMETERS</span></span>

### <span data-ttu-id="e5999-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5999-135">-DefaultProfile</span></span>
<span data-ttu-id="e5999-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5999-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5999-137">-Definizione</span><span class="sxs-lookup"><span data-stu-id="e5999-137">-Definition</span></span>
<span data-ttu-id="e5999-138">Specifica la definizione per l'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e5999-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e5999-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="e5999-139">-DefinitionFilePath</span></span>
<span data-ttu-id="e5999-140">Specifica la definizione di un'app logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="e5999-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="e5999-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="e5999-141">-IntegrationAccountId</span></span>
<span data-ttu-id="e5999-142">Specifica un ID account di integrazione per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="e5999-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e5999-143">-Location</span></span>
<span data-ttu-id="e5999-144">Specifica la posizione dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="e5999-145">Immettere una posizione nel centro dati di Azure, ad esempio ovest degli Stati Uniti o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="e5999-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="e5999-146">Puoi inserire un'app logica in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="e5999-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="e5999-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5999-147">-Name</span></span>
<span data-ttu-id="e5999-148">Specifica il nome dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="e5999-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="e5999-149">-ParameterFilePath</span></span>
<span data-ttu-id="e5999-150">Specifica il percorso di un file di parametro formattato JSON.</span><span class="sxs-lookup"><span data-stu-id="e5999-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="e5999-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e5999-151">-Parameters</span></span>
<span data-ttu-id="e5999-152">Specifica un oggetto raccolta Parameters per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="e5999-153">Specificare una tabella hash, un dizionario \<string\> o un dizionario \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="e5999-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="e5999-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5999-154">-ResourceGroupName</span></span>
<span data-ttu-id="e5999-155">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5999-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5999-156">-Stato</span><span class="sxs-lookup"><span data-stu-id="e5999-156">-State</span></span>
<span data-ttu-id="e5999-157">Specifica lo stato dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="e5999-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="e5999-158">I valori accettabili per questo parametro sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="e5999-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="e5999-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5999-159">-Confirm</span></span>
<span data-ttu-id="e5999-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5999-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5999-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5999-161">-WhatIf</span></span>
<span data-ttu-id="e5999-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5999-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5999-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5999-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5999-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5999-164">CommonParameters</span></span>
<span data-ttu-id="e5999-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5999-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5999-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5999-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5999-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5999-167">INPUTS</span></span>

### <span data-ttu-id="e5999-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e5999-168">System.String</span></span>

## <span data-ttu-id="e5999-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5999-169">OUTPUTS</span></span>

### <span data-ttu-id="e5999-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="e5999-170">System.Object</span></span>

## <span data-ttu-id="e5999-171">Note</span><span class="sxs-lookup"><span data-stu-id="e5999-171">NOTES</span></span>

## <span data-ttu-id="e5999-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5999-172">RELATED LINKS</span></span>

[<span data-ttu-id="e5999-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e5999-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="e5999-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e5999-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="e5999-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e5999-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="e5999-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e5999-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


