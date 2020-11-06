---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521607"
---
# <span data-ttu-id="5e8e8-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5e8e8-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="5e8e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8e8-103">Crea un nuovo servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e8e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e8e8-104">SYNTAX</span></span>

### <span data-ttu-id="5e8e8-105">Creare un nuovo servizio di Azure ML WebService da un file Definitore JSON.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e8e8-106">Creare un nuovo servizio di Azure ML WebService da una definizione di istanza di WebService.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e8e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e8e8-107">DESCRIPTION</span></span>
<span data-ttu-id="5e8e8-108">Crea un servizio Web di apprendimento di Azure Machine in un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="5e8e8-109">Se nel gruppo risorse esiste un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="5e8e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e8e8-110">EXAMPLES</span></span>

### <span data-ttu-id="5e8e8-111">--------------------------Esempio 1: creare un nuovo servizio da una definizione basata su file JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e8e8-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="5e8e8-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5e8e8-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="5e8e8-113">Crea un nuovo servizio Web di apprendimento di Azure Machine denominato "WebServiceName" nel gruppo "myresourcegroup" e nell'area sud centrale degli Stati Uniti, in base alla definizione presente nel file JSON a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="5e8e8-114">--------------------------Esempio 2: creare un nuovo servizio da un'istanza di oggetto--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e8e8-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="5e8e8-115">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5e8e8-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="5e8e8-116">Puoi ottenere un'istanza di un oggetto servizio Web per personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="5e8e8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e8e8-117">PARAMETERS</span></span>

### <span data-ttu-id="5e8e8-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5e8e8-118">-DefinitionFile</span></span>
<span data-ttu-id="5e8e8-119">Specifica il percorso del file che contiene la definizione del formato JSON del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="5e8e8-120">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="5e8e8-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5e8e8-121">-Force</span></span>
<span data-ttu-id="5e8e8-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5e8e8-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5e8e8-123">-Location</span></span>
<span data-ttu-id="5e8e8-124">Area geografica del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-124">The region of the web service.</span></span>
<span data-ttu-id="5e8e8-125">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="5e8e8-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5e8e8-126">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5e8e8-127">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5e8e8-128">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5e8e8-129">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzureRmResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5e8e8-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e8e8-130">-Name</span></span>
<span data-ttu-id="5e8e8-131">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-131">The name for the web service.</span></span>
<span data-ttu-id="5e8e8-132">Il nome deve essere univoco nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="5e8e8-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="5e8e8-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="5e8e8-134">La definizione per il nuovo servizio Web, contenente tutte le proprietà che costituiscono il servizio.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="5e8e8-135">Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="5e8e8-136">Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="5e8e8-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e8e8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8e8-137">-ResourceGroupName</span></span>
<span data-ttu-id="5e8e8-138">Gruppo di risorse in cui inserire il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="5e8e8-139">Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".</span><span class="sxs-lookup"><span data-stu-id="5e8e8-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5e8e8-140">Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5e8e8-141">Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5e8e8-142">I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5e8e8-143">Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzureRmResourceProvider con il cmdlet parametro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5e8e8-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e8e8-144">-Confirm</span></span>
<span data-ttu-id="5e8e8-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e8e8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e8e8-146">-WhatIf</span></span>
<span data-ttu-id="5e8e8-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e8e8-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e8e8-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8e8-149">-DefaultProfile</span></span>
<span data-ttu-id="5e8e8-150">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e8e8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8e8-151">CommonParameters</span></span>
<span data-ttu-id="5e8e8-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8e8-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e8e8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8e8-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e8e8-154">INPUTS</span></span>

### <span data-ttu-id="5e8e8-155">Servizio</span><span class="sxs-lookup"><span data-stu-id="5e8e8-155">WebService</span></span>
<span data-ttu-id="5e8e8-156">Il parametro ' NewWebServiceDefinition ' accetta il valore di tipo ' WebService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5e8e8-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="5e8e8-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e8e8-157">OUTPUTS</span></span>

### <span data-ttu-id="5e8e8-158">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="5e8e8-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="5e8e8-159">Descrizione di riepilogo del servizio Web di Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="5e8e8-160">In modo analogo alla descrizione restituita chiamando il cmdlet Get-AzureRmMlWebService in un servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="5e8e8-161">Questa descrizione non contiene proprietà riservate, ad esempio le credenziali dell'account di archiviazione e i tasti di scelta del servizio.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="5e8e8-162">Note</span><span class="sxs-lookup"><span data-stu-id="5e8e8-162">NOTES</span></span>
<span data-ttu-id="5e8e8-163">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5e8e8-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5e8e8-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e8e8-164">RELATED LINKS</span></span>

