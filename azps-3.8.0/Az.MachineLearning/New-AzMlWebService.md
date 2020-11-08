---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022190"
---
# <span data-ttu-id="d15b1-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="d15b1-101">New-AzMlWebService</span></span>

## <span data-ttu-id="d15b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d15b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d15b1-103">Crea un nuovo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d15b1-103">Creates a new web service.</span></span>

## <span data-ttu-id="d15b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d15b1-104">SYNTAX</span></span>

### <span data-ttu-id="d15b1-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="d15b1-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d15b1-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="d15b1-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d15b1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d15b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d15b1-108">Crea un servizio Web di apprendimento di Azure Machine in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="d15b1-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="d15b1-109">Se nel gruppo risorse esiste un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="d15b1-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="d15b1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d15b1-110">EXAMPLES</span></span>

### <span data-ttu-id="d15b1-111">Esempio 1: creare un nuovo servizio da una definizione basata su file JSON</span><span class="sxs-lookup"><span data-stu-id="d15b1-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="d15b1-112">Crea un nuovo servizio Web di apprendimento di Azure Machine denominato "WebServiceName" nel gruppo "myresourcegroup" e nell'area sud centrale degli Stati Uniti, in base alla definizione presente nel file JSON a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="d15b1-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="d15b1-113">Esempio 2: creare un nuovo servizio da un'istanza di un oggetto</span><span class="sxs-lookup"><span data-stu-id="d15b1-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="d15b1-114">Puoi ottenere un'istanza di un oggetto servizio Web per personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="d15b1-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="d15b1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d15b1-115">PARAMETERS</span></span>

### <span data-ttu-id="d15b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15b1-116">-DefaultProfile</span></span>
<span data-ttu-id="d15b1-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d15b1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d15b1-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d15b1-118">-DefinitionFile</span></span>
<span data-ttu-id="d15b1-119">Specifica il percorso del file che contiene la definizione del formato JSON del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d15b1-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="d15b1-120">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="d15b1-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="d15b1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d15b1-121">-Force</span></span>
<span data-ttu-id="d15b1-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d15b1-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d15b1-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d15b1-123">-Location</span></span>
<span data-ttu-id="d15b1-124">Area geografica del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d15b1-124">The region of the web service.</span></span>
<span data-ttu-id="d15b1-125">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="d15b1-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="d15b1-126">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="d15b1-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="d15b1-127">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d15b1-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="d15b1-128">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="d15b1-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="d15b1-129">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="d15b1-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="d15b1-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="d15b1-130">-Name</span></span>
<span data-ttu-id="d15b1-131">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d15b1-131">The name for the web service.</span></span>
<span data-ttu-id="d15b1-132">Il nome deve essere univoco nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="d15b1-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="d15b1-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="d15b1-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="d15b1-134">La definizione per il nuovo servizio Web, contenente tutte le proprietà che costituiscono il servizio.</span><span class="sxs-lookup"><span data-stu-id="d15b1-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="d15b1-135">Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="d15b1-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="d15b1-136">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="d15b1-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="d15b1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d15b1-137">-ResourceGroupName</span></span>
<span data-ttu-id="d15b1-138">Gruppo di risorse in cui inserire il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d15b1-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="d15b1-139">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="d15b1-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="d15b1-140">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="d15b1-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="d15b1-141">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d15b1-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="d15b1-142">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="d15b1-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="d15b1-143">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="d15b1-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="d15b1-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d15b1-144">-Confirm</span></span>
<span data-ttu-id="d15b1-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15b1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15b1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15b1-146">-WhatIf</span></span>
<span data-ttu-id="d15b1-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15b1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d15b1-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15b1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15b1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15b1-149">CommonParameters</span></span>
<span data-ttu-id="d15b1-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15b1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15b1-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15b1-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15b1-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d15b1-152">INPUTS</span></span>

### <span data-ttu-id="d15b1-153">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="d15b1-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d15b1-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d15b1-154">OUTPUTS</span></span>

### <span data-ttu-id="d15b1-155">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="d15b1-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d15b1-156">Note</span><span class="sxs-lookup"><span data-stu-id="d15b1-156">NOTES</span></span>
<span data-ttu-id="d15b1-157">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d15b1-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d15b1-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d15b1-158">RELATED LINKS</span></span>
