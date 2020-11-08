---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: fd7aa7e892c4874ad0087956156e0ef28ab9f995
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188926"
---
# <span data-ttu-id="d9c44-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="d9c44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9c44-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c44-103">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9c44-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="d9c44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9c44-104">SYNTAX</span></span>

### <span data-ttu-id="d9c44-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9c44-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9c44-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9c44-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9c44-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9c44-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9c44-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9c44-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9c44-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9c44-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9c44-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9c44-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c44-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9c44-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9c44-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9c44-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c44-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9c44-117">DESCRIPTION</span></span>
<span data-ttu-id="d9c44-118">Il cmdlet **New-AzResourceGroupDeployment** aggiunge una distribuzione a un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="d9c44-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="d9c44-119">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d9c44-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="d9c44-120">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d9c44-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="d9c44-121">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità, ad esempio il sito Web, il server di database e i database necessari per un sito Web finanziario.</span><span class="sxs-lookup"><span data-stu-id="d9c44-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="d9c44-122">La distribuzione di un gruppo di risorse usa un modello per aggiungere risorse a un gruppo di risorse e pubblicarle in modo che siano disponibili in Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c44-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="d9c44-123">Per aggiungere risorse a un gruppo di risorse senza usare un modello, usare il cmdlet New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="d9c44-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="d9c44-124">Per aggiungere una distribuzione di un gruppo di risorse, specificare il nome di un gruppo di risorse esistente e un modello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9c44-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="d9c44-125">Un modello di gruppo di risorse è una stringa JSON che rappresenta un gruppo di risorse per un servizio complesso basato su cloud, ad esempio un portale Web.</span><span class="sxs-lookup"><span data-stu-id="d9c44-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="d9c44-126">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d9c44-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="d9c44-127">Puoi trovare molti modelli nella raccolta di modelli di Azure oppure puoi creare modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d9c44-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="d9c44-128">Per usare un modello personalizzato per creare un gruppo di risorse, specificare il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="d9c44-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d9c44-129">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="d9c44-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d9c44-130">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d9c44-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d9c44-131">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d9c44-132">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d9c44-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d9c44-133">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="d9c44-134">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9c44-134">EXAMPLES</span></span>

### <span data-ttu-id="d9c44-135">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d9c44-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="d9c44-136">Questo comando crea una nuova distribuzione usando un modello personalizzato e un file modello su disco, con il parametro di tag definito.</span><span class="sxs-lookup"><span data-stu-id="d9c44-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="d9c44-137">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="d9c44-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d9c44-138">Esempio 2: usare un oggetto modello personalizzato e un file di parametro per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d9c44-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="d9c44-139">Questo comando crea una nuova distribuzione usando un file personalizzato e un modello su disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d9c44-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d9c44-140">I primi due comandi leggono il testo per il file del modello su disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d9c44-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d9c44-141">L'ultimo comando usa il parametro *TemplateObject* per specificare la Hashtable e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="d9c44-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d9c44-142">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d9c44-142">Example 3</span></span>

<span data-ttu-id="d9c44-143">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9c44-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="d9c44-144">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d9c44-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="d9c44-145">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9c44-145">PARAMETERS</span></span>

### <span data-ttu-id="d9c44-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9c44-146">-ApiVersion</span></span>
<span data-ttu-id="d9c44-147">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9c44-147">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d9c44-148">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d9c44-148">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d9c44-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9c44-149">-AsJob</span></span>
<span data-ttu-id="d9c44-150">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9c44-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9c44-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c44-151">-DefaultProfile</span></span>
<span data-ttu-id="d9c44-152">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d9c44-152">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9c44-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d9c44-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d9c44-154">Specifica un livello di log di debug.</span><span class="sxs-lookup"><span data-stu-id="d9c44-154">Specifies a debug log level.</span></span>
<span data-ttu-id="d9c44-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9c44-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9c44-156">RequestContent</span><span class="sxs-lookup"><span data-stu-id="d9c44-156">RequestContent</span></span>
- <span data-ttu-id="d9c44-157">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="d9c44-157">ResponseContent</span></span>
- <span data-ttu-id="d9c44-158">Tutti</span><span class="sxs-lookup"><span data-stu-id="d9c44-158">All</span></span>
- <span data-ttu-id="d9c44-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9c44-159">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-160">-Force</span><span class="sxs-lookup"><span data-stu-id="d9c44-160">-Force</span></span>
<span data-ttu-id="d9c44-161">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9c44-161">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9c44-162">-Modalità</span><span class="sxs-lookup"><span data-stu-id="d9c44-162">-Mode</span></span>
<span data-ttu-id="d9c44-163">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d9c44-163">Specifies the deployment mode.</span></span> <span data-ttu-id="d9c44-164">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9c44-164">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9c44-165">Completamento: in modalità completa, gestione risorse Elimina le risorse esistenti nel gruppo risorse, ma non sono specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-165">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="d9c44-166">Incrementale: in modalità incrementale, gestione risorse consente di lasciare invariate le risorse esistenti nel gruppo di risorse, ma non nel modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-166">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9c44-167">-Name</span></span>
<span data-ttu-id="d9c44-168">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="d9c44-168">The name of the deployment it's going to create.</span></span> <span data-ttu-id="d9c44-169">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d9c44-169">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="d9c44-170">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9c44-170">-Pre</span></span>
<span data-ttu-id="d9c44-171">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d9c44-171">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d9c44-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c44-172">-ResourceGroupName</span></span>
<span data-ttu-id="d9c44-173">Specifica il nome del gruppo di risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d9c44-173">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="d9c44-174">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="d9c44-174">-RollBackDeploymentName</span></span>
<span data-ttu-id="d9c44-175">Il rollback alla distribuzione corretta con il nome indicato nel gruppo di risorse non deve essere usato se viene usato-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="d9c44-175">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="d9c44-176">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-176">-RollbackToLastDeployment</span></span>
<span data-ttu-id="d9c44-177">Il rollback all'ultima distribuzione corretta nel gruppo di risorse non dovrebbe essere presente se viene usato-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="d9c44-177">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="d9c44-178">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d9c44-178">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d9c44-179">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-179">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="d9c44-180">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-180">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="d9c44-181">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="d9c44-181">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d9c44-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9c44-182">-Tag</span></span>
<span data-ttu-id="d9c44-183">Tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d9c44-183">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-184">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d9c44-184">-TemplateFile</span></span>
<span data-ttu-id="d9c44-185">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="d9c44-185">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="d9c44-186">Può trattarsi di un modello personalizzato o di un modello di raccolta salvato come file JSON, ad esempio uno creato usando il cmdlet **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="d9c44-186">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="d9c44-187">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="d9c44-187">-TemplateObject</span></span>
<span data-ttu-id="d9c44-188">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-188">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-189">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9c44-189">-TemplateParameterFile</span></span>
<span data-ttu-id="d9c44-190">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-190">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="d9c44-191">Se un modello include parametri, devi specificare i valori di parametro con il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d9c44-191">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d9c44-192">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-192">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d9c44-193">Per usare i parametri dinamici, digitare un segno meno (-) per indicare il nome di un parametro e quindi usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d9c44-193">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-194">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9c44-194">-TemplateParameterObject</span></span>
<span data-ttu-id="d9c44-195">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-195">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="d9c44-196">Per informazioni sulle tabelle hash in Windows PowerShell, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="d9c44-196">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="d9c44-197">Se un modello include parametri, è necessario specificare i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="d9c44-197">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="d9c44-198">I parametri di modello vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-198">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-199">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9c44-199">-TemplateParameterUri</span></span>
<span data-ttu-id="d9c44-200">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="d9c44-200">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-201">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d9c44-201">-TemplateUri</span></span>
<span data-ttu-id="d9c44-202">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="d9c44-202">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="d9c44-203">Questo file può essere un modello personalizzato o un modello di raccolta salvato come file JSON, ad esempio tramite **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="d9c44-203">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="d9c44-204">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="d9c44-204">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="d9c44-205">Tipi di modifica delle risorse delimitati da virgole da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="d9c44-205">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="d9c44-206">Applicabile quando è impostato l'opzione-WhatIf o-Confirm.</span><span class="sxs-lookup"><span data-stu-id="d9c44-206">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-207">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="d9c44-207">-WhatIfResultFormat</span></span>
<span data-ttu-id="d9c44-208">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="d9c44-208">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c44-209">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9c44-209">-Confirm</span></span>
<span data-ttu-id="d9c44-210">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c44-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c44-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c44-211">-WhatIf</span></span>
<span data-ttu-id="d9c44-212">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c44-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c44-213">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9c44-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c44-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c44-214">CommonParameters</span></span>
<span data-ttu-id="d9c44-215">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c44-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c44-216">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9c44-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c44-217">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9c44-217">INPUTS</span></span>

### <span data-ttu-id="d9c44-218">System. String</span><span class="sxs-lookup"><span data-stu-id="d9c44-218">System.String</span></span>

### <span data-ttu-id="d9c44-219">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="d9c44-219">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="d9c44-220">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9c44-220">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9c44-221">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9c44-221">OUTPUTS</span></span>

### <span data-ttu-id="d9c44-222">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-222">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="d9c44-223">Note</span><span class="sxs-lookup"><span data-stu-id="d9c44-223">NOTES</span></span>

## <span data-ttu-id="d9c44-224">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9c44-224">RELATED LINKS</span></span>

[<span data-ttu-id="d9c44-225">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-225">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9c44-226">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="d9c44-226">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="d9c44-227">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9c44-227">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="d9c44-228">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-228">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9c44-229">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-229">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9c44-230">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9c44-230">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)