---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190295"
---
# <span data-ttu-id="cf140-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="cf140-101">New-AzMlWebService</span></span>

## <span data-ttu-id="cf140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf140-102">SYNOPSIS</span></span>
<span data-ttu-id="cf140-103">Crea un nuovo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-103">Creates a new web service.</span></span>

## <span data-ttu-id="cf140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf140-104">SYNTAX</span></span>

### <span data-ttu-id="cf140-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="cf140-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf140-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="cf140-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf140-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf140-107">DESCRIPTION</span></span>
<span data-ttu-id="cf140-108">Crea un servizio Web Azure Machine Learning in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="cf140-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="cf140-109">Se nel gruppo di risorse è presente un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="cf140-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="cf140-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf140-110">EXAMPLES</span></span>

### <span data-ttu-id="cf140-111">Esempio 1: Creare un nuovo servizio da una definizione basata su file Json</span><span class="sxs-lookup"><span data-stu-id="cf140-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="cf140-112">Crea un nuovo servizio Web Azure Machine Learning denominato "mywebservicename" nel gruppo "myresourcegroup" e nell'area Stati Uniti centro meridionale, in base alla definizione presente nel file JSON a cui viene fatto riferimento.</span><span class="sxs-lookup"><span data-stu-id="cf140-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="cf140-113">Esempio 2: Creare un nuovo servizio da un'istanza di un oggetto</span><span class="sxs-lookup"><span data-stu-id="cf140-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="cf140-114">È possibile ottenere un'istanza dell'oggetto servizio Web da personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzMlWebService Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="cf140-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf140-115">PARAMETERS</span></span>

### <span data-ttu-id="cf140-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf140-116">-DefaultProfile</span></span>
<span data-ttu-id="cf140-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cf140-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf140-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cf140-118">-DefinitionFile</span></span>
<span data-ttu-id="cf140-119">Specifica il percorso del file che contiene la definizione in formato JSON del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="cf140-120">La specifica più recente per la definizione del servizio Web è indicata nella specifica più recente in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="cf140-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf140-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cf140-121">-Force</span></span>
<span data-ttu-id="cf140-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cf140-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf140-123">-Location</span><span class="sxs-lookup"><span data-stu-id="cf140-123">-Location</span></span>
<span data-ttu-id="cf140-124">Area geografica del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-124">The region of the web service.</span></span>
<span data-ttu-id="cf140-125">Immettere un'area geografica per il data center di Azure, ad esempio "Stati Uniti occidentali" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="cf140-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="cf140-126">È possibile inserire un servizio Web in qualsiasi area geografica che supporti risorse di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="cf140-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="cf140-127">Il servizio Web non deve essere nella stessa area geografica della sottoscrizione di Azure o nella stessa area geografica del relativo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf140-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="cf140-128">I gruppi di risorse possono contenere servizi Web da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="cf140-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="cf140-129">Per determinare le aree geografiche che supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet del parametro ProviderNtassi.</span><span class="sxs-lookup"><span data-stu-id="cf140-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="cf140-130">-Name</span><span class="sxs-lookup"><span data-stu-id="cf140-130">-Name</span></span>
<span data-ttu-id="cf140-131">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-131">The name for the web service.</span></span>
<span data-ttu-id="cf140-132">Il nome deve essere univoco nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf140-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="cf140-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="cf140-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="cf140-134">Definizione del nuovo servizio Web che contiene tutte le proprietà che costituiscono il servizio.</span><span class="sxs-lookup"><span data-stu-id="cf140-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="cf140-135">Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="cf140-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="cf140-136">La specifica più recente per la definizione del servizio Web è indicata nella specifica più recente in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="cf140-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf140-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf140-137">-ResourceGroupName</span></span>
<span data-ttu-id="cf140-138">Gruppo di risorse in cui inserire il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="cf140-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="cf140-139">Immettere un'area geografica per il data center di Azure, ad esempio "Stati Uniti occidentali" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="cf140-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="cf140-140">È possibile inserire un servizio Web in qualsiasi area geografica che supporti risorse di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="cf140-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="cf140-141">Il servizio Web non deve essere nella stessa area geografica della sottoscrizione di Azure o nella stessa area geografica del relativo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf140-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="cf140-142">I gruppi di risorse possono contenere servizi Web da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="cf140-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="cf140-143">Per determinare le aree geografiche che supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet del parametro ProviderNtassi.</span><span class="sxs-lookup"><span data-stu-id="cf140-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="cf140-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf140-144">-Confirm</span></span>
<span data-ttu-id="cf140-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf140-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf140-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf140-146">-WhatIf</span></span>
<span data-ttu-id="cf140-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf140-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf140-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf140-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf140-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf140-149">CommonParameters</span></span>
<span data-ttu-id="cf140-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf140-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf140-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf140-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf140-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf140-152">INPUTS</span></span>

### <span data-ttu-id="cf140-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="cf140-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="cf140-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf140-154">OUTPUTS</span></span>

### <span data-ttu-id="cf140-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="cf140-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="cf140-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf140-156">NOTES</span></span>
<span data-ttu-id="cf140-157">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="cf140-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="cf140-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf140-158">RELATED LINKS</span></span>
