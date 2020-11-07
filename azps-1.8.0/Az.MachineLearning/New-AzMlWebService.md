---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: e6ac8c2a47f7a8d11eb4f82d46be2047fd5ff47d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835288"
---
# <span data-ttu-id="11064-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="11064-101">New-AzMlWebService</span></span>

## <span data-ttu-id="11064-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11064-102">SYNOPSIS</span></span>
<span data-ttu-id="11064-103">Crea un nuovo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="11064-103">Creates a new web service.</span></span>

## <span data-ttu-id="11064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11064-104">SYNTAX</span></span>

### <span data-ttu-id="11064-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="11064-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11064-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="11064-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11064-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11064-107">DESCRIPTION</span></span>
<span data-ttu-id="11064-108">Crea un servizio Web di apprendimento di Azure Machine in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="11064-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="11064-109">Se nel gruppo risorse esiste un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="11064-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="11064-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11064-110">EXAMPLES</span></span>

### <span data-ttu-id="11064-111">Esempio 1: creare un nuovo servizio da una definizione basata su file JSON</span><span class="sxs-lookup"><span data-stu-id="11064-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="11064-112">Crea un nuovo servizio Web di apprendimento di Azure Machine denominato "WebServiceName" nel gruppo "myresourcegroup" e nell'area sud centrale degli Stati Uniti, in base alla definizione presente nel file JSON a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="11064-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="11064-113">Esempio 2: creare un nuovo servizio da un'istanza di un oggetto</span><span class="sxs-lookup"><span data-stu-id="11064-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="11064-114">Puoi ottenere un'istanza di un oggetto servizio Web per personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="11064-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="11064-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11064-115">PARAMETERS</span></span>

### <span data-ttu-id="11064-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11064-116">-DefaultProfile</span></span>
<span data-ttu-id="11064-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="11064-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11064-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="11064-118">-DefinitionFile</span></span>
<span data-ttu-id="11064-119">Specifica il percorso del file che contiene la definizione del formato JSON del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="11064-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="11064-120">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="11064-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="11064-121">-Force</span><span class="sxs-lookup"><span data-stu-id="11064-121">-Force</span></span>
<span data-ttu-id="11064-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="11064-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="11064-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="11064-123">-Location</span></span>
<span data-ttu-id="11064-124">Area geografica del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="11064-124">The region of the web service.</span></span>
<span data-ttu-id="11064-125">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="11064-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="11064-126">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="11064-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="11064-127">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11064-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="11064-128">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="11064-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="11064-129">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="11064-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="11064-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="11064-130">-Name</span></span>
<span data-ttu-id="11064-131">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="11064-131">The name for the web service.</span></span>
<span data-ttu-id="11064-132">Il nome deve essere univoco nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="11064-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="11064-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="11064-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="11064-134">La definizione per il nuovo servizio Web, contenente tutte le proprietà che costituiscono il servizio.</span><span class="sxs-lookup"><span data-stu-id="11064-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="11064-135">Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="11064-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="11064-136">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="11064-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="11064-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11064-137">-ResourceGroupName</span></span>
<span data-ttu-id="11064-138">Gruppo di risorse in cui inserire il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="11064-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="11064-139">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="11064-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="11064-140">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="11064-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="11064-141">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11064-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="11064-142">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="11064-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="11064-143">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="11064-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="11064-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11064-144">-Confirm</span></span>
<span data-ttu-id="11064-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11064-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11064-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11064-146">-WhatIf</span></span>
<span data-ttu-id="11064-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11064-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11064-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11064-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11064-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11064-149">CommonParameters</span></span>
<span data-ttu-id="11064-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11064-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11064-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11064-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11064-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11064-152">INPUTS</span></span>

### <span data-ttu-id="11064-153">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="11064-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="11064-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11064-154">OUTPUTS</span></span>

### <span data-ttu-id="11064-155">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="11064-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="11064-156">Note</span><span class="sxs-lookup"><span data-stu-id="11064-156">NOTES</span></span>
<span data-ttu-id="11064-157">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="11064-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="11064-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11064-158">RELATED LINKS</span></span>
