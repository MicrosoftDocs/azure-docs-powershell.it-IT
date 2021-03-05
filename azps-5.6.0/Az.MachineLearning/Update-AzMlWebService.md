---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: 510e33655fd2e76383fa89a972c477e65d67f070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976782"
---
# <span data-ttu-id="49620-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="49620-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="49620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49620-102">SYNOPSIS</span></span>
<span data-ttu-id="49620-103">Aggiorna le proprietà di una risorsa del servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="49620-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="49620-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49620-104">SYNTAX</span></span>

### <span data-ttu-id="49620-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="49620-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49620-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="49620-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49620-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49620-107">DESCRIPTION</span></span>
<span data-ttu-id="49620-108">Il Update-AzMlWebService cmdlet consente di aggiornare le proprietà non statiche di un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="49620-109">Il cmdlet funziona come operazione di patch.</span><span class="sxs-lookup"><span data-stu-id="49620-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="49620-110">Passare solo le proprietà da modificare.</span><span class="sxs-lookup"><span data-stu-id="49620-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="49620-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49620-111">EXAMPLES</span></span>

### <span data-ttu-id="49620-112">Esempio 1: Argomenti per l'aggiornamento selettivo</span><span class="sxs-lookup"><span data-stu-id="49620-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="49620-113">Qui viene cambiata la descrizione e la chiave di accesso primario e viene abilitata la raccolta di diagnostica per tutte le tracce durante il runtime per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="49620-114">Esempio 2: Aggiornamento basato su un'istanza di un servizio Web</span><span class="sxs-lookup"><span data-stu-id="49620-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="49620-115">Nell'esempio viene prima creata una definizione di servizio Web che contiene solo i campi da aggiornare, quindi viene chiamato il Update-AzMlWebService per applicarli usando il parametro ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="49620-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="49620-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49620-116">PARAMETERS</span></span>

### <span data-ttu-id="49620-117">-Beni</span><span class="sxs-lookup"><span data-stu-id="49620-117">-Assets</span></span>
<span data-ttu-id="49620-118">Insieme di risorse (ad esempio moduli, set di dati) che costituiscono il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

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

### <span data-ttu-id="49620-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49620-119">-DefaultProfile</span></span>
<span data-ttu-id="49620-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="49620-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49620-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="49620-121">-Description</span></span>
<span data-ttu-id="49620-122">Nuovo valore per la descrizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-122">The new value for the web service's description.</span></span>
<span data-ttu-id="49620-123">Questo è visibile nello schema API Swagger del servizio.</span><span class="sxs-lookup"><span data-stu-id="49620-123">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="49620-124">-Diagnostics</span><span class="sxs-lookup"><span data-stu-id="49620-124">-Diagnostics</span></span>
<span data-ttu-id="49620-125">Impostazioni che controllano la raccolta di tracce di diagnostica per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-125">The settings that control the diagnostics traces collection for the web service.</span></span>

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

### <span data-ttu-id="49620-126">-Force</span><span class="sxs-lookup"><span data-stu-id="49620-126">-Force</span></span>
<span data-ttu-id="49620-127">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="49620-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="49620-128">-Input</span><span class="sxs-lookup"><span data-stu-id="49620-128">-Input</span></span>
<span data-ttu-id="49620-129">Definizione degli input del servizio Web, fornita come costrutto di schema Swagger.</span><span class="sxs-lookup"><span data-stu-id="49620-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="49620-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="49620-130">-IsReadOnly</span></span>
<span data-ttu-id="49620-131">Specifica che il servizio Web è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="49620-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="49620-132">Dopo l'impostazione, il servizio Web può essere più aggiornato, inclusa la modifica del valore di questa proprietà, ed è possibile solo eliminare.</span><span class="sxs-lookup"><span data-stu-id="49620-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

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

### <span data-ttu-id="49620-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="49620-133">-Keys</span></span>
<span data-ttu-id="49620-134">Aggiorna una o entrambe le chiavi di accesso usate per autenticare le chiamate alle API di runtime del servizio.</span><span class="sxs-lookup"><span data-stu-id="49620-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

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

### <span data-ttu-id="49620-135">-Name</span><span class="sxs-lookup"><span data-stu-id="49620-135">-Name</span></span>
<span data-ttu-id="49620-136">Nome della risorsa del servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49620-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="49620-137">-Output</span><span class="sxs-lookup"><span data-stu-id="49620-137">-Output</span></span>
<span data-ttu-id="49620-138">Definizione degli output del servizio Web, forniti come costrutto di schema Swagger.</span><span class="sxs-lookup"><span data-stu-id="49620-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

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

### <span data-ttu-id="49620-139">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="49620-139">-Package</span></span>
<span data-ttu-id="49620-140">Definizione del pacchetto grafico che definisce questo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-140">The definition of the graph package that defines this web service.</span></span>

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

### <span data-ttu-id="49620-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="49620-141">-Parameters</span></span>
<span data-ttu-id="49620-142">Insieme dei valori dei parametri globali definiti per il servizio Web, dati come nome di parametro globale, raccolta \> di valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="49620-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="49620-143">Se non viene specificato alcun valore predefinito, il parametro viene considerato obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="49620-143">If no default value is specified, the parameter is considered to be required.</span></span>

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

### <span data-ttu-id="49620-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="49620-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="49620-145">Aggiornamenti per la configurazione dell'endpoint in tempo reale del servizio.</span><span class="sxs-lookup"><span data-stu-id="49620-145">Updates for the configuration of the service's realtime endpoint.</span></span>

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

### <span data-ttu-id="49620-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49620-146">-ResourceGroupName</span></span>
<span data-ttu-id="49620-147">Gruppo di risorse che contiene il servizio Web da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49620-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="49620-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="49620-148">-ServiceUpdates</span></span>
<span data-ttu-id="49620-149">Insieme di aggiornamenti da applicare al servizio Web fornito come istanza della definizione di servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="49620-150">Vengono modificati solo i campi non statici.</span><span class="sxs-lookup"><span data-stu-id="49620-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="49620-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="49620-151">-StorageAccountKey</span></span>
<span data-ttu-id="49620-152">Ruota la chiave di accesso per l'account di archiviazione associato al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-152">Rotates the access key for the storage account associated with the web service.</span></span>

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

### <span data-ttu-id="49620-153">-Title</span><span class="sxs-lookup"><span data-stu-id="49620-153">-Title</span></span>
<span data-ttu-id="49620-154">Nuovo valore per il titolo del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="49620-154">The new value for the web service's title.</span></span>
<span data-ttu-id="49620-155">Questo è visibile nello schema API Swagger del servizio.</span><span class="sxs-lookup"><span data-stu-id="49620-155">This is visible in the service's Swagger API schema.</span></span>

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

### <span data-ttu-id="49620-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49620-156">-Confirm</span></span>
<span data-ttu-id="49620-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49620-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49620-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49620-158">-WhatIf</span></span>
<span data-ttu-id="49620-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49620-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49620-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49620-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49620-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49620-161">CommonParameters</span></span>
<span data-ttu-id="49620-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49620-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49620-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49620-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49620-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="49620-164">INPUTS</span></span>

### <span data-ttu-id="49620-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="49620-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="49620-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49620-166">OUTPUTS</span></span>

### <span data-ttu-id="49620-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="49620-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="49620-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="49620-168">NOTES</span></span>
<span data-ttu-id="49620-169">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="49620-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="49620-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49620-170">RELATED LINKS</span></span>
