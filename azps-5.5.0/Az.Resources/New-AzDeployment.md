---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: d3b9fce538512fdb55328d6c2e846c955bcfbb5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186423"
---
# <span data-ttu-id="9aee0-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9aee0-101">New-AzDeployment</span></span>

## <span data-ttu-id="9aee0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aee0-102">SYNOPSIS</span></span>
<span data-ttu-id="9aee0-103">Creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="9aee0-103">Create a deployment</span></span>

## <span data-ttu-id="9aee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aee0-104">SYNTAX</span></span>

### <span data-ttu-id="9aee0-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="9aee0-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9aee0-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9aee0-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9aee0-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9aee0-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9aee0-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9aee0-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="9aee0-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9aee0-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9aee0-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee0-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="9aee0-119">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aee0-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9aee0-120">DESCRIPTION</span></span>
<span data-ttu-id="9aee0-121">Il cmdlet **New-AzDeployment** aggiunge una distribuzione all'ambito di sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9aee0-121">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="9aee0-122">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-122">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="9aee0-123">Una risorsa di Azure è un'entità di Azure gestita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9aee0-123">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="9aee0-124">Una risorsa può essere presente in un gruppo di risorse, ad esempio un server di database, un database, un sito Web, una macchina virtuale o un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-124">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="9aee0-125">Oppure può essere una risorsa a livello di abbonamento, come la definizione del ruolo, la definizione dei criteri e così via.</span><span class="sxs-lookup"><span data-stu-id="9aee0-125">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="9aee0-126">Per aggiungere risorse a un gruppo di risorse, usare **New-AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9aee0-126">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="9aee0-127">Il cmdlet **New-AzDeployment crea** una distribuzione nell'ambito di sottoscrizione corrente, che distribuisce risorse a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-127">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="9aee0-128">Per aggiungere una distribuzione in abbonamento, specificare il percorso e un modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-128">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="9aee0-129">La posizione indica a Gestione risorse di Azure dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-129">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="9aee0-130">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="9aee0-130">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="9aee0-131">Il modello include segnaposto di parametro per le risorse necessarie e valori di proprietà configurabili, come nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="9aee0-131">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="9aee0-132">Per usare un modello personalizzato per la distribuzione, specificare il *parametro TemplateFile* o *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="9aee0-132">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="9aee0-133">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="9aee0-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="9aee0-134">Per specificare i valori per i parametri del modello, specificare il *parametro TemplateParameterFile* o *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="9aee0-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="9aee0-135">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="9aee0-136">Per usare parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="9aee0-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="9aee0-137">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un file o in un oggetto parametro del modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="9aee0-138">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aee0-138">EXAMPLES</span></span>

### <span data-ttu-id="9aee0-139">Esempio 1: Usare un modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="9aee0-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="9aee0-140">Questo comando crea una nuova distribuzione nell'ambito di sottoscrizione corrente usando un modello personalizzato e un file di modello su disco, con un parametro di tag definito.</span><span class="sxs-lookup"><span data-stu-id="9aee0-140">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="9aee0-141">Il comando usa il *parametro TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file contenente parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9aee0-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="9aee0-142">Usa il *parametro TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-142">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="9aee0-143">Esempio 2: Distribuire un modello archiviato in un account di archiviazione non pubblico usando un URI e un token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="9aee0-143">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="9aee0-144">Questo comando crea una nuova distribuzione usando il modello in TemplateUri che non è pubblico e per accedere a un parametro token che verrebbe fornito con il parametro QueryString.</span><span class="sxs-lookup"><span data-stu-id="9aee0-144">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="9aee0-145">L'esecuzione di questo comando accede in modo efficace al modello usando https://example.com/example.json?foo l'URL.</span><span class="sxs-lookup"><span data-stu-id="9aee0-145">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="9aee0-146">Può essere usato se si vuole usare un modello in un account di archiviazione fornendo il token di firma di accesso condiviso come QueryString</span><span class="sxs-lookup"><span data-stu-id="9aee0-146">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="9aee0-147">Esempio 3: Usare un oggetto modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="9aee0-147">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="9aee0-148">Questo comando crea una nuova distribuzione nell'ambito della sottoscrizione corrente usando un modello personalizzato e un file di modello su disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="9aee0-148">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="9aee0-149">I primi due comandi leggono il testo del file modello sul disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="9aee0-149">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="9aee0-150">L'ultimo comando usa *il parametro TemplateObject* per specificare questa tabella hash e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="9aee0-150">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="9aee0-151">Usa il *parametro TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-151">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="9aee0-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9aee0-152">PARAMETERS</span></span>

### <span data-ttu-id="9aee0-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aee0-153">-AsJob</span></span>
<span data-ttu-id="9aee0-154">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9aee0-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9aee0-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aee0-155">-DefaultProfile</span></span>
<span data-ttu-id="9aee0-156">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9aee0-156">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aee0-157">-DeploymentLogLogLevel</span><span class="sxs-lookup"><span data-stu-id="9aee0-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="9aee0-158">Livello di log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-158">The deployment debug log level.</span></span>

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

### <span data-ttu-id="9aee0-159">-Location</span><span class="sxs-lookup"><span data-stu-id="9aee0-159">-Location</span></span>
<span data-ttu-id="9aee0-160">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-160">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9aee0-161">-Name</span><span class="sxs-lookup"><span data-stu-id="9aee0-161">-Name</span></span>
<span data-ttu-id="9aee0-162">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="9aee0-162">The name of the deployment it's going to create.</span></span> <span data-ttu-id="9aee0-163">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="9aee0-163">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aee0-164">-Pre</span><span class="sxs-lookup"><span data-stu-id="9aee0-164">-Pre</span></span>
<span data-ttu-id="9aee0-165">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9aee0-165">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9aee0-166">-QueryString</span><span class="sxs-lookup"><span data-stu-id="9aee0-166">-QueryString</span></span>
<span data-ttu-id="9aee0-167">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="9aee0-167">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="9aee0-168">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="9aee0-168">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="9aee0-169">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9aee0-169">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9aee0-170">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-170">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="9aee0-171">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-171">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="9aee0-172">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="9aee0-172">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9aee0-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="9aee0-173">-Tag</span></span>
<span data-ttu-id="9aee0-174">I tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9aee0-174">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="9aee0-175">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9aee0-175">-TemplateFile</span></span>
<span data-ttu-id="9aee0-176">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-176">Local path to the template file.</span></span>

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

### <span data-ttu-id="9aee0-177">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9aee0-177">-TemplateObject</span></span>
<span data-ttu-id="9aee0-178">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-178">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="9aee0-179">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9aee0-179">-TemplateParameterFile</span></span>
<span data-ttu-id="9aee0-180">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-180">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9aee0-181">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9aee0-181">-TemplateParameterObject</span></span>
<span data-ttu-id="9aee0-182">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="9aee0-182">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9aee0-183">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-183">-TemplateParameterUri</span></span>
<span data-ttu-id="9aee0-184">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-184">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9aee0-185">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="9aee0-185">-TemplateSpecId</span></span>
<span data-ttu-id="9aee0-186">ID risorsa del valore templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="9aee0-186">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="9aee0-187">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9aee0-187">-TemplateUri</span></span>
<span data-ttu-id="9aee0-188">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="9aee0-188">Uri to the template file.</span></span>

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

### <span data-ttu-id="9aee0-189">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="9aee0-189">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="9aee0-190">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="9aee0-190">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="9aee0-191">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="9aee0-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="9aee0-192">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="9aee0-192">-WhatIfResultFormat</span></span>
<span data-ttu-id="9aee0-193">Il What-If del risultato.</span><span class="sxs-lookup"><span data-stu-id="9aee0-193">The What-If result format.</span></span>

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

### <span data-ttu-id="9aee0-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9aee0-194">-Confirm</span></span>
<span data-ttu-id="9aee0-195">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9aee0-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aee0-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aee0-196">-WhatIf</span></span>
<span data-ttu-id="9aee0-197">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aee0-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aee0-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aee0-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aee0-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aee0-199">CommonParameters</span></span>
<span data-ttu-id="9aee0-200">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aee0-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aee0-201">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9aee0-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aee0-202">INPUT</span><span class="sxs-lookup"><span data-stu-id="9aee0-202">INPUTS</span></span>

### <span data-ttu-id="9aee0-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9aee0-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9aee0-204">System.String</span><span class="sxs-lookup"><span data-stu-id="9aee0-204">System.String</span></span>

## <span data-ttu-id="9aee0-205">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aee0-205">OUTPUTS</span></span>

### <span data-ttu-id="9aee0-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9aee0-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9aee0-207">NOTE</span><span class="sxs-lookup"><span data-stu-id="9aee0-207">NOTES</span></span>

## <span data-ttu-id="9aee0-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aee0-208">RELATED LINKS</span></span>
