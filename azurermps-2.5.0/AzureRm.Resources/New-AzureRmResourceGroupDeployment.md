---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 6c64c9defb3905e9851e79da5303b68e98514f44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866809"
---
# <span data-ttu-id="89436-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="89436-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89436-102">SYNOPSIS</span></span>
<span data-ttu-id="89436-103">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89436-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89436-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89436-104">SYNTAX</span></span>

### <span data-ttu-id="89436-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89436-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="89436-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="89436-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="89436-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="89436-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="89436-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="89436-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89436-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="89436-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89436-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89436-113">DESCRIPTION</span></span>
<span data-ttu-id="89436-114">Il cmdlet **New-AzureRmResourceGroupDeployment** aggiunge una distribuzione a un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="89436-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="89436-115">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="89436-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="89436-116">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="89436-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="89436-117">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità, ad esempio il sito Web, il server di database e i database necessari per un sito Web finanziario.</span><span class="sxs-lookup"><span data-stu-id="89436-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="89436-118">La distribuzione di un gruppo di risorse usa un modello per aggiungere risorse a un gruppo di risorse e pubblicarle in modo che siano disponibili in Azure.</span><span class="sxs-lookup"><span data-stu-id="89436-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="89436-119">Per aggiungere risorse a un gruppo di risorse senza usare un modello, usare il cmdlet New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="89436-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="89436-120">Per aggiungere una distribuzione di un gruppo di risorse, specificare il nome di un gruppo di risorse esistente e un modello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89436-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="89436-121">Un modello di gruppo di risorse è una stringa JSON che rappresenta un gruppo di risorse per un servizio complesso basato su cloud, ad esempio un portale Web.</span><span class="sxs-lookup"><span data-stu-id="89436-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="89436-122">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="89436-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="89436-123">Puoi trovare molti modelli nella raccolta di modelli di Azure oppure puoi creare modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="89436-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="89436-124">Puoi usare il cmdlet **Get-AzureRmResourceGroupGalleryTemplate** per trovare un modello nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="89436-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="89436-125">Per usare un modello personalizzato per creare un gruppo di risorse, specificare il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="89436-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="89436-126">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="89436-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="89436-127">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="89436-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="89436-128">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="89436-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="89436-129">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="89436-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="89436-130">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="89436-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="89436-131">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89436-131">EXAMPLES</span></span>

### <span data-ttu-id="89436-132">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="89436-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="89436-133">Questo comando crea una nuova distribuzione usando un modello personalizzato e un file modello su disco.</span><span class="sxs-lookup"><span data-stu-id="89436-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="89436-134">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="89436-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="89436-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89436-135">PARAMETERS</span></span>

### <span data-ttu-id="89436-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89436-136">-ApiVersion</span></span>
<span data-ttu-id="89436-137">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="89436-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="89436-138">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="89436-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="89436-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89436-139">-AsJob</span></span>
<span data-ttu-id="89436-140">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="89436-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89436-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89436-141">-DefaultProfile</span></span>
<span data-ttu-id="89436-142">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89436-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89436-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="89436-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="89436-144">Specifica un livello di log di debug.</span><span class="sxs-lookup"><span data-stu-id="89436-144">Specifies a debug log level.</span></span>
<span data-ttu-id="89436-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="89436-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89436-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="89436-146">RequestContent</span></span>
- <span data-ttu-id="89436-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="89436-147">ResponseContent</span></span>
- <span data-ttu-id="89436-148">Tutti</span><span class="sxs-lookup"><span data-stu-id="89436-148">All</span></span>
- <span data-ttu-id="89436-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="89436-149">None</span></span>

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

### <span data-ttu-id="89436-150">-Force</span><span class="sxs-lookup"><span data-stu-id="89436-150">-Force</span></span>
<span data-ttu-id="89436-151">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="89436-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89436-152">-Modalità</span><span class="sxs-lookup"><span data-stu-id="89436-152">-Mode</span></span>
<span data-ttu-id="89436-153">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="89436-153">Specifies the deployment mode.</span></span> <span data-ttu-id="89436-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="89436-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89436-155">Completare</span><span class="sxs-lookup"><span data-stu-id="89436-155">Complete</span></span>
- <span data-ttu-id="89436-156">Incrementale in modalità completa, gestione risorse Elimina le risorse esistenti nel gruppo risorse, ma non sono specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="89436-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="89436-157">In modalità incrementale, gestione risorse consente di lasciare invariate le risorse esistenti nel gruppo di risorse, ma non nel modello.</span><span class="sxs-lookup"><span data-stu-id="89436-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="89436-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="89436-158">-Name</span></span>
<span data-ttu-id="89436-159">Specifica il nome della distribuzione del gruppo di risorse da creare.</span><span class="sxs-lookup"><span data-stu-id="89436-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="89436-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="89436-160">-Pre</span></span>
<span data-ttu-id="89436-161">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="89436-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="89436-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89436-162">-ResourceGroupName</span></span>
<span data-ttu-id="89436-163">Specifica il nome del gruppo di risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="89436-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="89436-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="89436-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="89436-165">Il rollback alla distribuzione corretta con il nome indicato nel gruppo di risorse non deve essere usato se viene usato-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="89436-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="89436-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="89436-167">Il rollback all'ultima distribuzione corretta nel gruppo di risorse non dovrebbe essere presente se viene usato-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="89436-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="89436-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="89436-168">-TemplateFile</span></span>
<span data-ttu-id="89436-169">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="89436-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="89436-170">Può trattarsi di un modello personalizzato o di un modello di raccolta salvato come file JSON, ad esempio uno creato usando il cmdlet **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="89436-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89436-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="89436-171">-TemplateParameterFile</span></span>
<span data-ttu-id="89436-172">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="89436-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="89436-173">Se un modello include parametri, devi specificare i valori di parametro con il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="89436-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="89436-174">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="89436-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="89436-175">Per usare i parametri dinamici, digitare un segno meno (-) per indicare il nome di un parametro e quindi usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="89436-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89436-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="89436-176">-TemplateParameterObject</span></span>
<span data-ttu-id="89436-177">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="89436-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="89436-178">Per informazioni sulle tabelle hash in Windows PowerShell, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="89436-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="89436-179">Se un modello include parametri, è necessario specificare i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="89436-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="89436-180">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="89436-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89436-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="89436-181">-TemplateParameterUri</span></span>
<span data-ttu-id="89436-182">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="89436-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89436-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="89436-183">-TemplateUri</span></span>
<span data-ttu-id="89436-184">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="89436-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="89436-185">Questo file può essere un modello personalizzato o un modello di raccolta salvato come file JSON, ad esempio tramite **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="89436-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89436-186">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89436-186">-Confirm</span></span>
<span data-ttu-id="89436-187">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89436-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89436-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89436-188">-WhatIf</span></span>
<span data-ttu-id="89436-189">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89436-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89436-190">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89436-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89436-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89436-191">CommonParameters</span></span>
<span data-ttu-id="89436-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89436-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89436-193">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89436-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89436-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89436-194">INPUTS</span></span>

### <span data-ttu-id="89436-195">Nessuno</span><span class="sxs-lookup"><span data-stu-id="89436-195">None</span></span>

## <span data-ttu-id="89436-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89436-196">OUTPUTS</span></span>

### <span data-ttu-id="89436-197">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="89436-198">Note</span><span class="sxs-lookup"><span data-stu-id="89436-198">NOTES</span></span>

## <span data-ttu-id="89436-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89436-199">RELATED LINKS</span></span>

[<span data-ttu-id="89436-200">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="89436-201">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="89436-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="89436-202">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89436-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="89436-203">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="89436-204">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="89436-205">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89436-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


