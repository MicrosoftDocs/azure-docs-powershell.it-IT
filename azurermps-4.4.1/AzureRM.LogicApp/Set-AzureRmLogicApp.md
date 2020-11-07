---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522119"
---
# <span data-ttu-id="81e81-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81e81-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="81e81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81e81-102">SYNOPSIS</span></span>
<span data-ttu-id="81e81-103">Modifica un'app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81e81-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81e81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81e81-104">SYNTAX</span></span>

### <span data-ttu-id="81e81-105">Consumo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81e81-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81e81-106">Piano hosting</span><span class="sxs-lookup"><span data-stu-id="81e81-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81e81-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81e81-107">DESCRIPTION</span></span>
<span data-ttu-id="81e81-108">Il cmdlet **set-AzureRmLogicApp** modifica un'app logica usando la caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="81e81-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="81e81-109">Un'app logica è una raccolta di azioni o trigger definiti nella definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="81e81-110">Questo cmdlet restituisce un oggetto **flusso di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="81e81-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="81e81-111">Puoi modificare un'app logica specificando un nome, una posizione, una definizione di app logica, un gruppo di risorse e un piano.</span><span class="sxs-lookup"><span data-stu-id="81e81-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="81e81-112">La definizione e i parametri delle app logiche sono formattati in JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="81e81-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="81e81-113">Puoi usare un'app logica come modello per la definizione e i parametri.</span><span class="sxs-lookup"><span data-stu-id="81e81-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="81e81-114">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="81e81-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="81e81-115">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="81e81-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="81e81-116">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="81e81-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="81e81-117">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="81e81-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="81e81-118">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="81e81-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="81e81-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81e81-119">EXAMPLES</span></span>

### <span data-ttu-id="81e81-120">Esempio 1: modificare un'app logica</span><span class="sxs-lookup"><span data-stu-id="81e81-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="81e81-121">Questo comando modifica un'app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="81e81-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81e81-122">PARAMETERS</span></span>

### <span data-ttu-id="81e81-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="81e81-123">-AppServicePlan</span></span>
<span data-ttu-id="81e81-124">Specifica il nome di un piano.</span><span class="sxs-lookup"><span data-stu-id="81e81-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="81e81-125">-Definizione</span><span class="sxs-lookup"><span data-stu-id="81e81-125">-Definition</span></span>
<span data-ttu-id="81e81-126">Specifica la definizione di un'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="81e81-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="81e81-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="81e81-127">-DefinitionFilePath</span></span>
<span data-ttu-id="81e81-128">Specifica la definizione di un'app logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="81e81-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="81e81-129">-Force</span><span class="sxs-lookup"><span data-stu-id="81e81-129">-Force</span></span>
<span data-ttu-id="81e81-130">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="81e81-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81e81-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="81e81-131">-IntegrationAccountId</span></span>
<span data-ttu-id="81e81-132">Specifica un ID account di integrazione per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="81e81-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="81e81-133">-Name</span></span>
<span data-ttu-id="81e81-134">Specifica il nome di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="81e81-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="81e81-135">-ParameterFilePath</span></span>
<span data-ttu-id="81e81-136">Specifica il percorso di un file di parametro formattato JSON.</span><span class="sxs-lookup"><span data-stu-id="81e81-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="81e81-137">-Parameters</span><span class="sxs-lookup"><span data-stu-id="81e81-137">-Parameters</span></span>
<span data-ttu-id="81e81-138">Specifica un oggetto raccolta Parameters per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="81e81-139">Specificare una tabella hash, un dizionario \<string\> o un dizionario \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="81e81-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="81e81-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e81-140">-ResourceGroupName</span></span>
<span data-ttu-id="81e81-141">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81e81-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81e81-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="81e81-142">-State</span></span>
<span data-ttu-id="81e81-143">Specifica lo stato dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="81e81-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="81e81-144">I valori accettabili per questo parametro sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="81e81-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="81e81-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="81e81-145">-UseConsumptionModel</span></span>
<span data-ttu-id="81e81-146">Indica che la fatturazione dell'app logica usa il modello basato sul consumo.</span><span class="sxs-lookup"><span data-stu-id="81e81-146">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="81e81-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81e81-147">-Confirm</span></span>
<span data-ttu-id="81e81-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e81-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e81-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e81-149">-WhatIf</span></span>
<span data-ttu-id="81e81-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81e81-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e81-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81e81-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e81-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e81-152">-DefaultProfile</span></span>
<span data-ttu-id="81e81-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81e81-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e81-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e81-154">CommonParameters</span></span>
<span data-ttu-id="81e81-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e81-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e81-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e81-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e81-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81e81-157">INPUTS</span></span>

## <span data-ttu-id="81e81-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81e81-158">OUTPUTS</span></span>

### <span data-ttu-id="81e81-159">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="81e81-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="81e81-160">Note</span><span class="sxs-lookup"><span data-stu-id="81e81-160">NOTES</span></span>

## <span data-ttu-id="81e81-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81e81-161">RELATED LINKS</span></span>

[<span data-ttu-id="81e81-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81e81-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="81e81-163">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81e81-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="81e81-164">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81e81-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="81e81-165">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81e81-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

