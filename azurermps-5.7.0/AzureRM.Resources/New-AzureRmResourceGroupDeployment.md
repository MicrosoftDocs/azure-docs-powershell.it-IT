---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512343"
---
# <span data-ttu-id="5f0fe-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="5f0fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0fe-103">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f0fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f0fe-104">SYNTAX</span></span>

### <span data-ttu-id="5f0fe-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f0fe-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f0fe-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f0fe-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f0fe-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f0fe-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f0fe-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f0fe-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f0fe-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5f0fe-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f0fe-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f0fe-113">DESCRIPTION</span></span>
<span data-ttu-id="5f0fe-114">Il cmdlet **New-AzureRmResourceGroupDeployment** aggiunge una distribuzione a un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="5f0fe-115">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="5f0fe-116">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5f0fe-117">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità, ad esempio il sito Web, il server di database e i database necessari per un sito Web finanziario.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="5f0fe-118">La distribuzione di un gruppo di risorse usa un modello per aggiungere risorse a un gruppo di risorse e pubblicarle in modo che siano disponibili in Azure.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="5f0fe-119">Per aggiungere risorse a un gruppo di risorse senza usare un modello, usare il cmdlet New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="5f0fe-120">Per aggiungere una distribuzione di un gruppo di risorse, specificare il nome di un gruppo di risorse esistente e un modello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="5f0fe-121">Un modello di gruppo di risorse è una stringa JSON che rappresenta un gruppo di risorse per un servizio complesso basato su cloud, ad esempio un portale Web.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="5f0fe-122">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="5f0fe-123">Puoi trovare molti modelli nella raccolta di modelli di Azure oppure puoi creare modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="5f0fe-124">Puoi usare il cmdlet **Get-AzureRmResourceGroupGalleryTemplate** per trovare un modello nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="5f0fe-125">Per usare un modello personalizzato per creare un gruppo di risorse, specificare il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5f0fe-126">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5f0fe-127">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5f0fe-128">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5f0fe-129">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5f0fe-130">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5f0fe-131">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f0fe-131">EXAMPLES</span></span>

### <span data-ttu-id="5f0fe-132">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="5f0fe-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="5f0fe-133">Questo comando crea una nuova distribuzione usando un modello personalizzato e un file modello su disco.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="5f0fe-134">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5f0fe-135">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="5f0fe-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f0fe-136">PARAMETERS</span></span>

### <span data-ttu-id="5f0fe-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f0fe-137">-ApiVersion</span></span>
<span data-ttu-id="5f0fe-138">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5f0fe-139">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-139">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f0fe-140">-AsJob</span></span>
<span data-ttu-id="5f0fe-141">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5f0fe-141">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0fe-142">-DefaultProfile</span></span>
<span data-ttu-id="5f0fe-143">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5f0fe-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5f0fe-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5f0fe-145">Specifica un livello di log di debug.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-145">Specifies a debug log level.</span></span>
<span data-ttu-id="5f0fe-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f0fe-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f0fe-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="5f0fe-147">RequestContent</span></span>
- <span data-ttu-id="5f0fe-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="5f0fe-148">ResponseContent</span></span>
- <span data-ttu-id="5f0fe-149">Tutti</span><span class="sxs-lookup"><span data-stu-id="5f0fe-149">All</span></span>
- <span data-ttu-id="5f0fe-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f0fe-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-151">-Force</span><span class="sxs-lookup"><span data-stu-id="5f0fe-151">-Force</span></span>
<span data-ttu-id="5f0fe-152">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-152">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-153">-Modalità</span><span class="sxs-lookup"><span data-stu-id="5f0fe-153">-Mode</span></span>
<span data-ttu-id="5f0fe-154">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-154">Specifies the deployment mode.</span></span> <span data-ttu-id="5f0fe-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f0fe-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f0fe-156">Completare</span><span class="sxs-lookup"><span data-stu-id="5f0fe-156">Complete</span></span>
- <span data-ttu-id="5f0fe-157">Incrementale</span><span class="sxs-lookup"><span data-stu-id="5f0fe-157">Incremental</span></span>

<span data-ttu-id="5f0fe-158">In modalità completa, gestione risorse Elimina le risorse esistenti nel gruppo di risorse, ma non sono specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="5f0fe-159">In modalità incrementale, gestione risorse consente di lasciare invariate le risorse esistenti nel gruppo di risorse, ma non nel modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f0fe-160">-Name</span></span>
<span data-ttu-id="5f0fe-161">Specifica il nome della distribuzione del gruppo di risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f0fe-162">-Pre</span></span>
<span data-ttu-id="5f0fe-163">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f0fe-164">-ResourceGroupName</span></span>
<span data-ttu-id="5f0fe-165">Specifica il nome del gruppo di risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5f0fe-166">-TemplateFile</span></span>
<span data-ttu-id="5f0fe-167">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="5f0fe-168">Può trattarsi di un modello personalizzato o di un modello di raccolta salvato come file JSON, ad esempio uno creato usando il cmdlet **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f0fe-169">-TemplateParameterFile</span></span>
<span data-ttu-id="5f0fe-170">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="5f0fe-171">Se un modello include parametri, devi specificare i valori di parametro con il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5f0fe-172">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="5f0fe-173">Per usare i parametri dinamici, digitare un segno meno (-) per indicare il nome di un parametro e quindi usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f0fe-174">-TemplateParameterObject</span></span>
<span data-ttu-id="5f0fe-175">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="5f0fe-176">Per informazioni sulle tabelle hash in Windows PowerShell, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="5f0fe-177">Se un modello include parametri, è necessario specificare i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="5f0fe-178">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f0fe-179">-TemplateParameterUri</span></span>
<span data-ttu-id="5f0fe-180">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5f0fe-181">-TemplateUri</span></span>
<span data-ttu-id="5f0fe-182">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="5f0fe-183">Questo file può essere un modello personalizzato o un modello di raccolta salvato come file JSON, ad esempio tramite **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f0fe-184">-Confirm</span></span>
<span data-ttu-id="5f0fe-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f0fe-186">-WhatIf</span></span>
<span data-ttu-id="5f0fe-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f0fe-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0fe-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0fe-189">CommonParameters</span></span>
<span data-ttu-id="5f0fe-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0fe-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0fe-191">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f0fe-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0fe-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f0fe-192">INPUTS</span></span>

### <span data-ttu-id="5f0fe-193">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f0fe-193">None</span></span>

## <span data-ttu-id="5f0fe-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f0fe-194">OUTPUTS</span></span>

### <span data-ttu-id="5f0fe-195">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="5f0fe-196">Note</span><span class="sxs-lookup"><span data-stu-id="5f0fe-196">NOTES</span></span>

## <span data-ttu-id="5f0fe-197">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f0fe-197">RELATED LINKS</span></span>

[<span data-ttu-id="5f0fe-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5f0fe-199">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5f0fe-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="5f0fe-200">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f0fe-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="5f0fe-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5f0fe-202">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5f0fe-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5f0fe-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


