---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186399"
---
# <span data-ttu-id="b4f32-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b4f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4f32-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f32-103">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4f32-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="b4f32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4f32-104">SYNTAX</span></span>

### <span data-ttu-id="b4f32-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="b4f32-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f32-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4f32-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4f32-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4f32-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4f32-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4f32-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4f32-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="b4f32-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f32-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b4f32-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f32-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b4f32-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f32-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f32-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f32-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4f32-120">DESCRIPTION</span></span>
<span data-ttu-id="b4f32-121">Il cmdlet **New-AzResourceGroupDeployment** aggiunge una distribuzione a un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b4f32-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="b4f32-122">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4f32-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="b4f32-123">Una risorsa di Azure è un'entità di Azure gestita dall'utente, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4f32-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="b4f32-124">Un gruppo di risorse di Azure è una raccolta di risorse di Azure distribuite come unità, ad esempio il sito Web, il server di database e i database necessari per un sito Web finanziario.</span><span class="sxs-lookup"><span data-stu-id="b4f32-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="b4f32-125">La distribuzione di un gruppo di risorse usa un modello per aggiungere risorse a un gruppo di risorse e le pubblica in modo che siano disponibili in Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f32-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="b4f32-126">Per aggiungere risorse a un gruppo di risorse senza usare un modello, usare il cmdlet New-AzResource risorse.</span><span class="sxs-lookup"><span data-stu-id="b4f32-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="b4f32-127">Per aggiungere una distribuzione di un gruppo di risorse, specificare il nome di un gruppo di risorse esistente e un modello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4f32-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="b4f32-128">Un modello di gruppo di risorse è una stringa JSON che rappresenta un gruppo di risorse per un servizio complesso basato sul cloud, ad esempio un portale Web.</span><span class="sxs-lookup"><span data-stu-id="b4f32-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="b4f32-129">Il modello include segnaposto di parametro per le risorse necessarie e valori di proprietà configurabili, come nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b4f32-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="b4f32-130">Molti modelli sono disponibili nella raccolta di modelli di Azure oppure è possibile creare modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b4f32-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="b4f32-131">Per usare un modello personalizzato per creare un gruppo di risorse, specificare il *parametro TemplateFile* o *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="b4f32-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b4f32-132">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="b4f32-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b4f32-133">Per specificare i valori per i parametri del modello, specificare il *parametro TemplateParameterFile* o *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="b4f32-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b4f32-134">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b4f32-135">Per usare parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b4f32-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b4f32-136">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un file o in un oggetto parametro del modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="b4f32-137">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4f32-137">EXAMPLES</span></span>

### <span data-ttu-id="b4f32-138">Esempio 1: Usare un modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="b4f32-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="b4f32-139">Questo comando crea una nuova distribuzione usando un modello personalizzato e un file modello su disco, con un parametro tag definito.</span><span class="sxs-lookup"><span data-stu-id="b4f32-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="b4f32-140">Il comando usa il *parametro TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file contenente parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="b4f32-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b4f32-141">Esempio 2: Usare un oggetto modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="b4f32-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="b4f32-142">Questo comando crea una nuova distribuzione usando un file personalizzato e un file di modello sul disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="b4f32-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="b4f32-143">I primi due comandi leggono il testo del file modello sul disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="b4f32-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="b4f32-144">L'ultimo comando usa *il parametro TemplateObject* per specificare la tabella hash e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="b4f32-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b4f32-145">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b4f32-145">Example 3</span></span>

<span data-ttu-id="b4f32-146">Aggiunge una distribuzione di Azure a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4f32-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="b4f32-147">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b4f32-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="b4f32-148">Esempio 4: Distribuire un modello archiviato in un account di archiviazione non pubblico con un URI e un token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="b4f32-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="b4f32-149">Questo comando crea una nuova distribuzione usando il modello in TemplateUri che non è pubblico e per accedere a un parametro token che verrebbe fornito con il parametro QueryString.</span><span class="sxs-lookup"><span data-stu-id="b4f32-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="b4f32-150">L'esecuzione di questo comando accede in modo efficace al modello usando https://example.com/example.json?foo l'URL.</span><span class="sxs-lookup"><span data-stu-id="b4f32-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="b4f32-151">Può essere usato se si vuole usare un modello in un account di archiviazione fornendo il token di firma di accesso condiviso come QueryString</span><span class="sxs-lookup"><span data-stu-id="b4f32-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="b4f32-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4f32-152">PARAMETERS</span></span>

### <span data-ttu-id="b4f32-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4f32-153">-AsJob</span></span>
<span data-ttu-id="b4f32-154">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b4f32-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4f32-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f32-155">-DefaultProfile</span></span>
<span data-ttu-id="b4f32-156">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b4f32-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4f32-157">-DeploymentLogLogLevel</span><span class="sxs-lookup"><span data-stu-id="b4f32-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b4f32-158">Specifica un livello di log di debug.</span><span class="sxs-lookup"><span data-stu-id="b4f32-158">Specifies a debug log level.</span></span>
<span data-ttu-id="b4f32-159">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b4f32-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4f32-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="b4f32-160">RequestContent</span></span>
- <span data-ttu-id="b4f32-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="b4f32-161">ResponseContent</span></span>
- <span data-ttu-id="b4f32-162">Tutti</span><span class="sxs-lookup"><span data-stu-id="b4f32-162">All</span></span>
- <span data-ttu-id="b4f32-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b4f32-163">None</span></span>

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

### <span data-ttu-id="b4f32-164">-Force</span><span class="sxs-lookup"><span data-stu-id="b4f32-164">-Force</span></span>
<span data-ttu-id="b4f32-165">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b4f32-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4f32-166">-Modalità</span><span class="sxs-lookup"><span data-stu-id="b4f32-166">-Mode</span></span>
<span data-ttu-id="b4f32-167">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4f32-167">Specifies the deployment mode.</span></span> <span data-ttu-id="b4f32-168">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b4f32-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4f32-169">Completato: in modalità completa, Il manager delle risorse elimina le risorse presenti nel gruppo di risorse ma non specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="b4f32-170">Incrementale: in modalità incrementale, Gestione risorse lascia invariate le risorse esistenti nel gruppo di risorse, ma non vengono specificate nel modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="b4f32-171">-Name</span><span class="sxs-lookup"><span data-stu-id="b4f32-171">-Name</span></span>
<span data-ttu-id="b4f32-172">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="b4f32-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="b4f32-173">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b4f32-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="b4f32-174">-Pre</span><span class="sxs-lookup"><span data-stu-id="b4f32-174">-Pre</span></span>
<span data-ttu-id="b4f32-175">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b4f32-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b4f32-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="b4f32-176">-QueryString</span></span>
<span data-ttu-id="b4f32-177">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="b4f32-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="b4f32-178">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="b4f32-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="b4f32-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f32-179">-ResourceGroupName</span></span>
<span data-ttu-id="b4f32-180">Specifica il nome del gruppo di risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="b4f32-180">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="b4f32-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b4f32-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="b4f32-182">Eseguire il rollback alla distribuzione riuscita con il nome specificato nel gruppo di risorse. Non deve essere usato se si usa -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="b4f32-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="b4f32-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="b4f32-184">Eseguire il rollback all'ultima distribuzione riuscita nel gruppo di risorse, non deve essere presente se si usa -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="b4f32-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="b4f32-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b4f32-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b4f32-186">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="b4f32-187">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="b4f32-188">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="b4f32-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b4f32-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4f32-189">-Tag</span></span>
<span data-ttu-id="b4f32-190">I tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b4f32-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="b4f32-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b4f32-191">-TemplateFile</span></span>
<span data-ttu-id="b4f32-192">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="b4f32-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="b4f32-193">Può trattarsi di un modello personalizzato o di una raccolta che viene salvato come file JSON, ad esempio un modello creato con il cmdlet **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="b4f32-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="b4f32-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b4f32-194">-TemplateObject</span></span>
<span data-ttu-id="b4f32-195">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b4f32-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4f32-196">-TemplateParameterFile</span></span>
<span data-ttu-id="b4f32-197">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="b4f32-198">Se un modello contiene parametri, è necessario specificare i valori dei parametri con il *parametro TemplateParameterFile* o *il parametro TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="b4f32-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b4f32-199">Quando si specifica un modello, i parametri del modello vengono aggiunti dinamicamente al comando.</span><span class="sxs-lookup"><span data-stu-id="b4f32-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b4f32-200">Per usare i parametri dinamici, digitare un segno meno (-) per indicare il nome di un parametro e quindi premere TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b4f32-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f32-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4f32-201">-TemplateParameterObject</span></span>
<span data-ttu-id="b4f32-202">Specifica una tabella hash dei nomi e dei valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="b4f32-203">Per assistenza con le tabelle hash in Windows PowerShell, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="b4f32-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="b4f32-204">Se un modello contiene parametri, è necessario specificare i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="b4f32-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="b4f32-205">Quando si specifica un modello, i parametri del modello vengono aggiunti dinamicamente al comando.</span><span class="sxs-lookup"><span data-stu-id="b4f32-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="b4f32-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-206">-TemplateParameterUri</span></span>
<span data-ttu-id="b4f32-207">Specifica l'URI di un file di parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="b4f32-207">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f32-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="b4f32-208">-TemplateSpecId</span></span>
<span data-ttu-id="b4f32-209">ID risorsa del valore templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="b4f32-209">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f32-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b4f32-210">-TemplateUri</span></span>
<span data-ttu-id="b4f32-211">Specifica l'URI di un file modello JSON.</span><span class="sxs-lookup"><span data-stu-id="b4f32-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="b4f32-212">Può trattarsi di un modello personalizzato o di una raccolta che viene salvato come file JSON, ad esempio usando **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="b4f32-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="b4f32-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b4f32-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="b4f32-214">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="b4f32-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="b4f32-215">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="b4f32-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="b4f32-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="b4f32-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="b4f32-217">Il What-If del risultato.</span><span class="sxs-lookup"><span data-stu-id="b4f32-217">The What-If result format.</span></span>

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

### <span data-ttu-id="b4f32-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4f32-218">-Confirm</span></span>
<span data-ttu-id="b4f32-219">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4f32-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f32-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f32-220">-WhatIf</span></span>
<span data-ttu-id="b4f32-221">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4f32-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f32-222">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4f32-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f32-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f32-223">CommonParameters</span></span>
<span data-ttu-id="b4f32-224">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f32-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f32-225">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4f32-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f32-226">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4f32-226">INPUTS</span></span>

### <span data-ttu-id="b4f32-227">System.String</span><span class="sxs-lookup"><span data-stu-id="b4f32-227">System.String</span></span>

### <span data-ttu-id="b4f32-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="b4f32-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="b4f32-229">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4f32-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4f32-230">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4f32-230">OUTPUTS</span></span>

### <span data-ttu-id="b4f32-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="b4f32-232">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4f32-232">NOTES</span></span>

## <span data-ttu-id="b4f32-233">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4f32-233">RELATED LINKS</span></span>

[<span data-ttu-id="b4f32-234">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4f32-235">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="b4f32-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="b4f32-236">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4f32-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b4f32-237">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4f32-238">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4f32-239">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4f32-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)