---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: e695e2de2cf0512ecffc1c072f94cc577d523ddf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516524"
---
# <span data-ttu-id="928d0-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="928d0-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="928d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="928d0-102">SYNOPSIS</span></span>
<span data-ttu-id="928d0-103">Aggiorna le proprietà di una risorsa del servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="928d0-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="928d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="928d0-104">SYNTAX</span></span>

### <span data-ttu-id="928d0-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="928d0-105">UpdateFromParameters</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928d0-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="928d0-106">UpdateFromObject</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="928d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="928d0-107">DESCRIPTION</span></span>
<span data-ttu-id="928d0-108">Il cmdlet Update-AzureRmMlWebService consente di aggiornare le proprietà non statiche di un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="928d0-109">Il cmdlet funziona come operazione di patch.</span><span class="sxs-lookup"><span data-stu-id="928d0-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="928d0-110">Passare solo le proprietà che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="928d0-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="928d0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="928d0-111">EXAMPLES</span></span>

### <span data-ttu-id="928d0-112">Esempio 1: argomenti di aggiornamento selettivi</span><span class="sxs-lookup"><span data-stu-id="928d0-112">Example 1: Selective update arguments</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="928d0-113">In questo caso modifichiamo la descrizione, il tasto di scelta principale e attiviamo la raccolta di diagnostica per tutte le tracce durante il runtime per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="928d0-114">Esempio 2: aggiornamento basato su un'istanza di un servizio Web</span><span class="sxs-lookup"><span data-stu-id="928d0-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="928d0-115">L'esempio crea prima di tutto una definizione di servizio Web, che contiene solo i campi da aggiornare e quindi chiama il Update-AzureRmMlWebService per applicarli usando il parametro ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="928d0-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="928d0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="928d0-116">PARAMETERS</span></span>

### <span data-ttu-id="928d0-117">-Asset</span><span class="sxs-lookup"><span data-stu-id="928d0-117">-Assets</span></span>
<span data-ttu-id="928d0-118">Set di asset (ad esempio moduli, DataSet) che costituiscono il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="928d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928d0-119">-DefaultProfile</span></span>
<span data-ttu-id="928d0-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="928d0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="928d0-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="928d0-121">-Description</span></span>
<span data-ttu-id="928d0-122">Nuovo valore per la descrizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-122">The new value for the web service's description.</span></span>
<span data-ttu-id="928d0-123">Questo è visibile nello schema dell'API di spavalderia del servizio.</span><span class="sxs-lookup"><span data-stu-id="928d0-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="928d0-124">-Diagnostica</span><span class="sxs-lookup"><span data-stu-id="928d0-124">-Diagnostics</span></span>
<span data-ttu-id="928d0-125">Impostazioni che controllano la raccolta di tracce di diagnostica per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="928d0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="928d0-126">-Force</span></span>
<span data-ttu-id="928d0-127">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="928d0-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="928d0-128">-Input</span><span class="sxs-lookup"><span data-stu-id="928d0-128">-Input</span></span>
<span data-ttu-id="928d0-129">La definizione per l'input o i dati del servizio Web, forniti come costrutto di schema spavalderia.</span><span class="sxs-lookup"><span data-stu-id="928d0-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="928d0-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="928d0-130">-IsReadOnly</span></span>
<span data-ttu-id="928d0-131">Specifica che questo servizio Web è ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="928d0-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="928d0-132">Una volta impostato, il servizio Web può essere più aggiornato, inclusa la modifica del valore di questa proprietà e può essere eliminato solo.</span><span class="sxs-lookup"><span data-stu-id="928d0-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="928d0-133">-Tasti</span><span class="sxs-lookup"><span data-stu-id="928d0-133">-Keys</span></span>
<span data-ttu-id="928d0-134">Aggiorna uno o entrambi i tasti di scelta usati per l'autenticazione delle chiamate alle API di runtime del servizio.</span><span class="sxs-lookup"><span data-stu-id="928d0-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="928d0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="928d0-135">-Name</span></span>
<span data-ttu-id="928d0-136">Nome della risorsa del servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="928d0-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="928d0-137">-Output</span><span class="sxs-lookup"><span data-stu-id="928d0-137">-Output</span></span>
<span data-ttu-id="928d0-138">La definizione per l'output o i risultati del servizio Web, forniti come costrutto di schema spavalderia.</span><span class="sxs-lookup"><span data-stu-id="928d0-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="928d0-139">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="928d0-139">-Package</span></span>
<span data-ttu-id="928d0-140">La definizione del pacchetto grafico che definisce questo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="928d0-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="928d0-141">-Parameters</span></span>
<span data-ttu-id="928d0-142">Set di valori di parametri globali definiti per il servizio Web, dato come nome di parametro globale- \> raccolta valori predefinita.</span><span class="sxs-lookup"><span data-stu-id="928d0-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="928d0-143">Se non viene specificato alcun valore predefinito, il parametro viene considerato obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="928d0-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="928d0-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="928d0-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="928d0-145">Aggiornamenti per la configurazione dell'endpoint in tempo reale del servizio.</span><span class="sxs-lookup"><span data-stu-id="928d0-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="928d0-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928d0-146">-ResourceGroupName</span></span>
<span data-ttu-id="928d0-147">Gruppo di risorse che contiene il servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="928d0-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="928d0-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="928d0-148">-ServiceUpdates</span></span>
<span data-ttu-id="928d0-149">Set di aggiornamenti da applicare al servizio Web fornito come istanza di definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="928d0-150">Vengono modificati solo i campi non statici.</span><span class="sxs-lookup"><span data-stu-id="928d0-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="928d0-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="928d0-151">-StorageAccountKey</span></span>
<span data-ttu-id="928d0-152">Ruota il tasto di scelta per l'account di archiviazione associato al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="928d0-153">-Titolo</span><span class="sxs-lookup"><span data-stu-id="928d0-153">-Title</span></span>
<span data-ttu-id="928d0-154">Nuovo valore per il titolo del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="928d0-154">The new value for the web service's title.</span></span>
<span data-ttu-id="928d0-155">Questo è visibile nello schema dell'API di spavalderia del servizio.</span><span class="sxs-lookup"><span data-stu-id="928d0-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="928d0-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="928d0-156">-Confirm</span></span>
<span data-ttu-id="928d0-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="928d0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="928d0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="928d0-158">-WhatIf</span></span>
<span data-ttu-id="928d0-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="928d0-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="928d0-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="928d0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="928d0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928d0-161">CommonParameters</span></span>
<span data-ttu-id="928d0-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928d0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928d0-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928d0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928d0-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="928d0-164">INPUTS</span></span>

### <span data-ttu-id="928d0-165">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="928d0-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="928d0-166">Parametri: ServiceUpdates (ByValue)</span><span class="sxs-lookup"><span data-stu-id="928d0-166">Parameters: ServiceUpdates (ByValue)</span></span>

## <span data-ttu-id="928d0-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="928d0-167">OUTPUTS</span></span>

### <span data-ttu-id="928d0-168">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="928d0-168">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="928d0-169">Note</span><span class="sxs-lookup"><span data-stu-id="928d0-169">NOTES</span></span>
<span data-ttu-id="928d0-170">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="928d0-170">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="928d0-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="928d0-171">RELATED LINKS</span></span>
