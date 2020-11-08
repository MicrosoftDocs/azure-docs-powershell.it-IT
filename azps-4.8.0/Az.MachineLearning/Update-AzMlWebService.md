---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189623"
---
# <span data-ttu-id="01da5-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="01da5-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="01da5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01da5-102">SYNOPSIS</span></span>
<span data-ttu-id="01da5-103">Aggiorna le proprietà di una risorsa del servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="01da5-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="01da5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01da5-104">SYNTAX</span></span>

### <span data-ttu-id="01da5-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="01da5-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01da5-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="01da5-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01da5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01da5-107">DESCRIPTION</span></span>
<span data-ttu-id="01da5-108">Il cmdlet Update-AzMlWebService consente di aggiornare le proprietà non statiche di un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="01da5-109">Il cmdlet funziona come operazione di patch.</span><span class="sxs-lookup"><span data-stu-id="01da5-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="01da5-110">Passare solo le proprietà che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="01da5-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="01da5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01da5-111">EXAMPLES</span></span>

### <span data-ttu-id="01da5-112">Esempio 1: argomenti di aggiornamento selettivi</span><span class="sxs-lookup"><span data-stu-id="01da5-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="01da5-113">In questo caso modifichiamo la descrizione, il tasto di scelta principale e attiviamo la raccolta di diagnostica per tutte le tracce durante il runtime per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="01da5-114">Esempio 2: aggiornamento basato su un'istanza di un servizio Web</span><span class="sxs-lookup"><span data-stu-id="01da5-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="01da5-115">L'esempio crea prima di tutto una definizione di servizio Web, che contiene solo i campi da aggiornare e quindi chiama il Update-AzMlWebService per applicarli usando il parametro ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="01da5-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="01da5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01da5-116">PARAMETERS</span></span>

### <span data-ttu-id="01da5-117">-Asset</span><span class="sxs-lookup"><span data-stu-id="01da5-117">-Assets</span></span>
<span data-ttu-id="01da5-118">Set di asset (ad esempio moduli, DataSet) che costituiscono il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01da5-119">-DefaultProfile</span></span>
<span data-ttu-id="01da5-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01da5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01da5-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="01da5-121">-Description</span></span>
<span data-ttu-id="01da5-122">Nuovo valore per la descrizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-122">The new value for the web service's description.</span></span>
<span data-ttu-id="01da5-123">Questo è visibile nello schema dell'API di spavalderia del servizio.</span><span class="sxs-lookup"><span data-stu-id="01da5-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-124">-Diagnostica</span><span class="sxs-lookup"><span data-stu-id="01da5-124">-Diagnostics</span></span>
<span data-ttu-id="01da5-125">Impostazioni che controllano la raccolta di tracce di diagnostica per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="01da5-126">-Force</span></span>
<span data-ttu-id="01da5-127">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="01da5-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="01da5-128">-Input</span><span class="sxs-lookup"><span data-stu-id="01da5-128">-Input</span></span>
<span data-ttu-id="01da5-129">La definizione per l'input o i dati del servizio Web, forniti come costrutto di schema spavalderia.</span><span class="sxs-lookup"><span data-stu-id="01da5-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="01da5-130">-IsReadOnly</span></span>
<span data-ttu-id="01da5-131">Specifica che il servizio Web è ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="01da5-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="01da5-132">Una volta impostato, il servizio Web può essere più aggiornato, inclusa la modifica del valore di questa proprietà e può essere eliminato solo.</span><span class="sxs-lookup"><span data-stu-id="01da5-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-133">-Tasti</span><span class="sxs-lookup"><span data-stu-id="01da5-133">-Keys</span></span>
<span data-ttu-id="01da5-134">Aggiorna uno o entrambi i tasti di scelta usati per l'autenticazione delle chiamate alle API di runtime del servizio.</span><span class="sxs-lookup"><span data-stu-id="01da5-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="01da5-135">-Name</span></span>
<span data-ttu-id="01da5-136">Nome della risorsa del servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="01da5-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-137">-Output</span><span class="sxs-lookup"><span data-stu-id="01da5-137">-Output</span></span>
<span data-ttu-id="01da5-138">La definizione per l'output o i risultati del servizio Web, forniti come costrutto di schema spavalderia.</span><span class="sxs-lookup"><span data-stu-id="01da5-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-139">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="01da5-139">-Package</span></span>
<span data-ttu-id="01da5-140">La definizione del pacchetto grafico che definisce questo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="01da5-141">-Parameters</span></span>
<span data-ttu-id="01da5-142">Set di valori di parametri globali definiti per il servizio Web, dato come nome di parametro globale- \> raccolta valori predefinita.</span><span class="sxs-lookup"><span data-stu-id="01da5-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="01da5-143">Se non viene specificato alcun valore predefinito, il parametro viene considerato obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01da5-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="01da5-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="01da5-145">Aggiornamenti per la configurazione dell'endpoint in tempo reale del servizio.</span><span class="sxs-lookup"><span data-stu-id="01da5-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01da5-146">-ResourceGroupName</span></span>
<span data-ttu-id="01da5-147">Gruppo di risorse che contiene il servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="01da5-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="01da5-148">-ServiceUpdates</span></span>
<span data-ttu-id="01da5-149">Set di aggiornamenti da applicare al servizio Web fornito come istanza di definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="01da5-150">Vengono modificati solo i campi non statici.</span><span class="sxs-lookup"><span data-stu-id="01da5-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="01da5-151">-StorageAccountKey</span></span>
<span data-ttu-id="01da5-152">Ruota il tasto di scelta per l'account di archiviazione associato al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-153">-Titolo</span><span class="sxs-lookup"><span data-stu-id="01da5-153">-Title</span></span>
<span data-ttu-id="01da5-154">Nuovo valore per il titolo del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="01da5-154">The new value for the web service's title.</span></span>
<span data-ttu-id="01da5-155">Questo è visibile nello schema dell'API di spavalderia del servizio.</span><span class="sxs-lookup"><span data-stu-id="01da5-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01da5-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01da5-156">-Confirm</span></span>
<span data-ttu-id="01da5-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01da5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01da5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01da5-158">-WhatIf</span></span>
<span data-ttu-id="01da5-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01da5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01da5-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01da5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01da5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01da5-161">CommonParameters</span></span>
<span data-ttu-id="01da5-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01da5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01da5-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01da5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01da5-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01da5-164">INPUTS</span></span>

### <span data-ttu-id="01da5-165">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="01da5-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="01da5-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01da5-166">OUTPUTS</span></span>

### <span data-ttu-id="01da5-167">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="01da5-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="01da5-168">Note</span><span class="sxs-lookup"><span data-stu-id="01da5-168">NOTES</span></span>
<span data-ttu-id="01da5-169">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="01da5-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="01da5-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01da5-170">RELATED LINKS</span></span>
