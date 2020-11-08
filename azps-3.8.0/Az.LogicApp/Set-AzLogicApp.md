---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018376"
---
# <span data-ttu-id="10a18-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="10a18-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="10a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10a18-102">SYNOPSIS</span></span>
<span data-ttu-id="10a18-103">Modifica un'app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10a18-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="10a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10a18-104">SYNTAX</span></span>

### <span data-ttu-id="10a18-105">Consumo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10a18-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10a18-106">Piano hosting</span><span class="sxs-lookup"><span data-stu-id="10a18-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10a18-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10a18-107">DESCRIPTION</span></span>
<span data-ttu-id="10a18-108">Il cmdlet **set-AzLogicApp** modifica un'app logica usando la caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="10a18-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="10a18-109">Un'app logica è una raccolta di azioni o trigger definiti nella definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="10a18-110">Questo cmdlet restituisce un oggetto **flusso di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="10a18-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="10a18-111">Puoi modificare un'app logica specificando un nome, una posizione, una definizione di app logica, un gruppo di risorse e un piano.</span><span class="sxs-lookup"><span data-stu-id="10a18-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="10a18-112">La definizione e i parametri delle app logiche sono formattati in JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="10a18-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="10a18-113">Puoi usare un'app logica come modello per la definizione e i parametri.</span><span class="sxs-lookup"><span data-stu-id="10a18-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="10a18-114">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="10a18-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="10a18-115">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="10a18-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="10a18-116">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="10a18-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10a18-117">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="10a18-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="10a18-118">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="10a18-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="10a18-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10a18-119">EXAMPLES</span></span>

### <span data-ttu-id="10a18-120">Esempio 1: modificare un'app logica</span><span class="sxs-lookup"><span data-stu-id="10a18-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="10a18-121">Questo comando modifica un'app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="10a18-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10a18-122">PARAMETERS</span></span>

### <span data-ttu-id="10a18-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10a18-123">-AppServicePlan</span></span>
<span data-ttu-id="10a18-124">Specifica il nome di un piano.</span><span class="sxs-lookup"><span data-stu-id="10a18-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a18-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a18-125">-DefaultProfile</span></span>
<span data-ttu-id="10a18-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="10a18-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10a18-127">-Definizione</span><span class="sxs-lookup"><span data-stu-id="10a18-127">-Definition</span></span>
<span data-ttu-id="10a18-128">Specifica la definizione di un'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="10a18-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="10a18-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="10a18-129">-DefinitionFilePath</span></span>
<span data-ttu-id="10a18-130">Specifica la definizione di un'app logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="10a18-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="10a18-131">-Force</span><span class="sxs-lookup"><span data-stu-id="10a18-131">-Force</span></span>
<span data-ttu-id="10a18-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10a18-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10a18-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="10a18-133">-IntegrationAccountId</span></span>
<span data-ttu-id="10a18-134">Specifica un ID account di integrazione per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="10a18-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="10a18-135">-Name</span></span>
<span data-ttu-id="10a18-136">Specifica il nome di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="10a18-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="10a18-137">-ParameterFilePath</span></span>
<span data-ttu-id="10a18-138">Specifica il percorso di un file di parametro formattato JSON.</span><span class="sxs-lookup"><span data-stu-id="10a18-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="10a18-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="10a18-139">-Parameters</span></span>
<span data-ttu-id="10a18-140">Specifica un oggetto raccolta Parameters per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="10a18-141">Specificare una tabella hash, una \< stringa di dizionario \> o una stringa di dizionario \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="10a18-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="10a18-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a18-142">-ResourceGroupName</span></span>
<span data-ttu-id="10a18-143">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10a18-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10a18-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="10a18-144">-State</span></span>
<span data-ttu-id="10a18-145">Specifica lo stato dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="10a18-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="10a18-146">I valori accettabili per questo parametro sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="10a18-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="10a18-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="10a18-147">-UseConsumptionModel</span></span>
<span data-ttu-id="10a18-148">Indica che la fatturazione dell'app logica usa il modello basato sul consumo.</span><span class="sxs-lookup"><span data-stu-id="10a18-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a18-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10a18-149">-Confirm</span></span>
<span data-ttu-id="10a18-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a18-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a18-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a18-151">-WhatIf</span></span>
<span data-ttu-id="10a18-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a18-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a18-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a18-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a18-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a18-154">CommonParameters</span></span>
<span data-ttu-id="10a18-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a18-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a18-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a18-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a18-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10a18-157">INPUTS</span></span>

### <span data-ttu-id="10a18-158">System. String</span><span class="sxs-lookup"><span data-stu-id="10a18-158">System.String</span></span>

## <span data-ttu-id="10a18-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10a18-159">OUTPUTS</span></span>

### <span data-ttu-id="10a18-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="10a18-160">System.Object</span></span>

## <span data-ttu-id="10a18-161">Note</span><span class="sxs-lookup"><span data-stu-id="10a18-161">NOTES</span></span>

## <span data-ttu-id="10a18-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10a18-162">RELATED LINKS</span></span>

[<span data-ttu-id="10a18-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="10a18-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="10a18-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="10a18-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="10a18-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="10a18-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="10a18-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="10a18-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


