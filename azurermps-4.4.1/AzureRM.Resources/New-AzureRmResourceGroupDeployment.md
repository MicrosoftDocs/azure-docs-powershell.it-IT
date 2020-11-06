---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519533"
---
# <span data-ttu-id="a2a50-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="a2a50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2a50-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a50-103">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2a50-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2a50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2a50-104">SYNTAX</span></span>

### <span data-ttu-id="a2a50-105">Distribuzione tramite file modello senza parametri (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2a50-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a50-106">Distribuzione tramite un oggetto modello di file e parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a2a50-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-107">Distribuzione tramite URI di modello e oggetto parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a2a50-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-108">Distribuzione tramite file modello e parametri del modello</span><span class="sxs-lookup"><span data-stu-id="a2a50-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-109">Distribuzione tramite URI modello e file di parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a2a50-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-110">Distribuzione tramite URI parametri modello file modello</span><span class="sxs-lookup"><span data-stu-id="a2a50-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-111">Distribuzione tramite URI di modello e parametri di modello URI</span><span class="sxs-lookup"><span data-stu-id="a2a50-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a50-112">Distribuzione tramite URI di modello senza parametri</span><span class="sxs-lookup"><span data-stu-id="a2a50-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a50-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2a50-113">DESCRIPTION</span></span>
<span data-ttu-id="a2a50-114">Il cmdlet **New-AzureRmResourceGroupDeployment** aggiunge una distribuzione a un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="a2a50-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="a2a50-115">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a2a50-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="a2a50-116">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a2a50-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="a2a50-117">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità, ad esempio il sito Web, il server di database e i database necessari per un sito Web finanziario.</span><span class="sxs-lookup"><span data-stu-id="a2a50-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="a2a50-118">La distribuzione di un gruppo di risorse usa un modello per aggiungere risorse a un gruppo di risorse e pubblicarle in modo che siano disponibili in Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a50-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="a2a50-119">Per aggiungere risorse a un gruppo di risorse senza usare un modello, usare il cmdlet New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a2a50-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="a2a50-120">Per aggiungere una distribuzione di un gruppo di risorse, specificare il nome di un gruppo di risorse esistente e un modello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2a50-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="a2a50-121">Un modello di gruppo di risorse è una stringa JSON che rappresenta un gruppo di risorse per un servizio complesso basato su cloud, ad esempio un portale Web.</span><span class="sxs-lookup"><span data-stu-id="a2a50-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="a2a50-122">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a2a50-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="a2a50-123">Puoi trovare molti modelli nella raccolta di modelli di Azure oppure puoi creare modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a2a50-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="a2a50-124">Puoi usare il cmdlet **Get-AzureRmResourceGroupGalleryTemplate** per trovare un modello nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a2a50-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="a2a50-125">Per usare un modello personalizzato per creare un gruppo di risorse, specificare il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="a2a50-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a2a50-126">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="a2a50-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a2a50-127">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a2a50-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a2a50-128">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a2a50-129">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a2a50-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a2a50-130">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="a2a50-131">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2a50-131">EXAMPLES</span></span>

### <span data-ttu-id="a2a50-132">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="a2a50-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="a2a50-133">Questo comando crea una nuova distribuzione usando un modello personalizzato e un file modello su disco.</span><span class="sxs-lookup"><span data-stu-id="a2a50-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="a2a50-134">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="a2a50-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="a2a50-135">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="a2a50-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2a50-136">PARAMETERS</span></span>

### <span data-ttu-id="a2a50-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a2a50-137">-ApiVersion</span></span>
<span data-ttu-id="a2a50-138">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2a50-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a2a50-139">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a2a50-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a2a50-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a2a50-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a2a50-141">Specifica un livello di log di debug.</span><span class="sxs-lookup"><span data-stu-id="a2a50-141">Specifies a debug log level.</span></span>
<span data-ttu-id="a2a50-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2a50-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2a50-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="a2a50-143">RequestContent</span></span> 
- <span data-ttu-id="a2a50-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="a2a50-144">ResponseContent</span></span> 
- <span data-ttu-id="a2a50-145">Tutti</span><span class="sxs-lookup"><span data-stu-id="a2a50-145">All</span></span> 
- <span data-ttu-id="a2a50-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2a50-146">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-147">-Force</span><span class="sxs-lookup"><span data-stu-id="a2a50-147">-Force</span></span>
<span data-ttu-id="a2a50-148">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a2a50-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2a50-149">-Modalità</span><span class="sxs-lookup"><span data-stu-id="a2a50-149">-Mode</span></span>
<span data-ttu-id="a2a50-150">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a2a50-150">Specifies the deployment mode.</span></span> <span data-ttu-id="a2a50-151">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2a50-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2a50-152">Completare</span><span class="sxs-lookup"><span data-stu-id="a2a50-152">Complete</span></span> 
- <span data-ttu-id="a2a50-153">Incrementale</span><span class="sxs-lookup"><span data-stu-id="a2a50-153">Incremental</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2a50-154">-Name</span></span>
<span data-ttu-id="a2a50-155">Specifica il nome della distribuzione del gruppo di risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="a2a50-155">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="a2a50-156">-Pre</span></span>
<span data-ttu-id="a2a50-157">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a2a50-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a2a50-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a50-158">-ResourceGroupName</span></span>
<span data-ttu-id="a2a50-159">Specifica il nome del gruppo di risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a2a50-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="a2a50-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a2a50-160">-TemplateFile</span></span>
<span data-ttu-id="a2a50-161">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="a2a50-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="a2a50-162">Può trattarsi di un modello personalizzato o di un modello di raccolta salvato come file JSON, ad esempio uno creato usando il cmdlet **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="a2a50-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a2a50-163">-TemplateParameterFile</span></span>
<span data-ttu-id="a2a50-164">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="a2a50-165">Se un modello include parametri, devi specificare i valori di parametro con il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="a2a50-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a2a50-166">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="a2a50-167">Per usare i parametri dinamici, digitare un segno meno (-) per indicare il nome di un parametro e quindi usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a2a50-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a2a50-168">-TemplateParameterObject</span></span>
<span data-ttu-id="a2a50-169">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="a2a50-170">Per informazioni sulle tabelle hash in Windows PowerShell, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="a2a50-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a2a50-171">Se un modello include parametri, è necessario specificare i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="a2a50-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="a2a50-172">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a2a50-173">-TemplateParameterUri</span></span>
<span data-ttu-id="a2a50-174">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="a2a50-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a2a50-175">-TemplateUri</span></span>
<span data-ttu-id="a2a50-176">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="a2a50-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="a2a50-177">Questo file può essere un modello personalizzato o un modello di raccolta salvato come file JSON, ad esempio tramite **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="a2a50-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a50-178">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2a50-178">-Confirm</span></span>
<span data-ttu-id="a2a50-179">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a50-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a50-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a50-180">-WhatIf</span></span>
<span data-ttu-id="a2a50-181">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a50-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a50-182">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a50-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a50-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a50-183">-DefaultProfile</span></span>
<span data-ttu-id="a2a50-184">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a50-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2a50-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a50-185">CommonParameters</span></span>
<span data-ttu-id="a2a50-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a50-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a50-187">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a50-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a50-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2a50-188">INPUTS</span></span>

### <span data-ttu-id="a2a50-189">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2a50-189">None</span></span>

## <span data-ttu-id="a2a50-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2a50-190">OUTPUTS</span></span>

### <span data-ttu-id="a2a50-191">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a2a50-192">Note</span><span class="sxs-lookup"><span data-stu-id="a2a50-192">NOTES</span></span>

## <span data-ttu-id="a2a50-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2a50-193">RELATED LINKS</span></span>

[<span data-ttu-id="a2a50-194">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a2a50-195">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a2a50-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a2a50-196">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a2a50-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="a2a50-197">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a2a50-198">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a2a50-199">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a2a50-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


