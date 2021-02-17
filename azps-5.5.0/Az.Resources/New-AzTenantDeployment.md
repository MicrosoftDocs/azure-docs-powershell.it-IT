---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: d2a54022768bd3751ed18713fdc123ef2ef9cbf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208443"
---
# <span data-ttu-id="4d978-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4d978-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="4d978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d978-102">SYNOPSIS</span></span>
<span data-ttu-id="4d978-103">Creare una distribuzione con ambito tenant</span><span class="sxs-lookup"><span data-stu-id="4d978-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="4d978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d978-104">SYNTAX</span></span>

### <span data-ttu-id="4d978-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="4d978-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4d978-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4d978-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4d978-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4d978-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4d978-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4d978-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="4d978-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4d978-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d978-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4d978-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4d978-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="4d978-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4d978-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4d978-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d978-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="4d978-119">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d978-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d978-120">DESCRIPTION</span></span>
<span data-ttu-id="4d978-121">Il cmdlet **New-AzTenantDeployment** aggiunge una distribuzione all'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="4d978-121">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="4d978-122">Per aggiungere una distribuzione nell'ambito tenant, specificare la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-122">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="4d978-123">La posizione indica a Gestione risorse di Azure dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d978-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="4d978-124">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="4d978-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="4d978-125">Il modello include segnaposto di parametro per le risorse necessarie e valori di proprietà configurabili, come nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="4d978-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="4d978-126">Per usare un modello personalizzato per la distribuzione, specificare il *parametro TemplateFile* o *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="4d978-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="4d978-127">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="4d978-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="4d978-128">Per specificare i valori per i parametri del modello, specificare il *parametro TemplateParameterFile* o *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="4d978-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4d978-129">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4d978-130">Per usare parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="4d978-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="4d978-131">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un file o in un oggetto parametro del modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="4d978-132">Per aggiungere risorse a un gruppo di risorse, usare **New-AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d978-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="4d978-133">Per aggiungere risorse a una sottoscrizione, usare **New-AzSubscriptionDeployment** che crea una distribuzione nell'ambito della sottoscrizione, che distribuisce risorse a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4d978-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="4d978-134">Per aggiungere risorse a un gruppo di gestione, usare **New-AzManagementGroupDeployment,** che crea una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="4d978-134">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="4d978-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d978-135">EXAMPLES</span></span>

### <span data-ttu-id="4d978-136">Esempio 1: Usare un modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="4d978-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="4d978-137">Questo comando crea una nuova distribuzione nell'ambito tenant corrente usando un modello personalizzato e un file di modello su disco, con un parametro tag definito.</span><span class="sxs-lookup"><span data-stu-id="4d978-137">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="4d978-138">Il comando usa il *parametro TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file contenente parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="4d978-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="4d978-139">Esempio 2: Usare un oggetto modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="4d978-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="4d978-140">Questo comando crea una nuova distribuzione nel tenant corrente usando un modello personalizzato e un file di modello sul disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="4d978-140">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="4d978-141">I primi due comandi leggono il testo del file modello sul disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="4d978-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="4d978-142">L'ultimo comando usa *il parametro TemplateObject* per specificare questa tabella hash e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="4d978-142">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="4d978-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d978-143">PARAMETERS</span></span>

### <span data-ttu-id="4d978-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d978-144">-AsJob</span></span>
<span data-ttu-id="4d978-145">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4d978-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d978-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d978-146">-DefaultProfile</span></span>
<span data-ttu-id="4d978-147">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d978-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d978-148">-DeploymentLogLogLevel</span><span class="sxs-lookup"><span data-stu-id="4d978-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="4d978-149">Livello di log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d978-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="4d978-150">-Location</span><span class="sxs-lookup"><span data-stu-id="4d978-150">-Location</span></span>
<span data-ttu-id="4d978-151">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d978-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4d978-152">-Name</span><span class="sxs-lookup"><span data-stu-id="4d978-152">-Name</span></span>
<span data-ttu-id="4d978-153">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="4d978-153">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4d978-154">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4d978-154">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="4d978-155">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d978-155">-Pre</span></span>
<span data-ttu-id="4d978-156">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4d978-156">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4d978-157">-QueryString</span><span class="sxs-lookup"><span data-stu-id="4d978-157">-QueryString</span></span>
<span data-ttu-id="4d978-158">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="4d978-158">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="4d978-159">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="4d978-159">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="4d978-160">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4d978-160">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4d978-161">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-161">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="4d978-162">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-162">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="4d978-163">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="4d978-163">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4d978-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d978-164">-Tag</span></span>
<span data-ttu-id="4d978-165">I tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d978-165">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="4d978-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4d978-166">-TemplateFile</span></span>
<span data-ttu-id="4d978-167">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-167">Local path to the template file.</span></span>

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

### <span data-ttu-id="4d978-168">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4d978-168">-TemplateObject</span></span>
<span data-ttu-id="4d978-169">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-169">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4d978-170">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4d978-170">-TemplateParameterFile</span></span>
<span data-ttu-id="4d978-171">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-171">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4d978-172">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4d978-172">-TemplateParameterObject</span></span>
<span data-ttu-id="4d978-173">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="4d978-173">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4d978-174">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4d978-174">-TemplateParameterUri</span></span>
<span data-ttu-id="4d978-175">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-175">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4d978-176">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="4d978-176">-TemplateSpecId</span></span>
<span data-ttu-id="4d978-177">ID risorsa del valore templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="4d978-177">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="4d978-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4d978-178">-TemplateUri</span></span>
<span data-ttu-id="4d978-179">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="4d978-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="4d978-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4d978-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="4d978-181">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="4d978-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="4d978-182">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="4d978-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="4d978-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="4d978-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="4d978-184">Il What-If del risultato.</span><span class="sxs-lookup"><span data-stu-id="4d978-184">The What-If result format.</span></span> <span data-ttu-id="4d978-185">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="4d978-185">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="4d978-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d978-186">-Confirm</span></span>
<span data-ttu-id="4d978-187">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d978-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d978-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d978-188">-WhatIf</span></span>
<span data-ttu-id="4d978-189">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d978-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d978-190">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d978-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d978-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d978-191">CommonParameters</span></span>
<span data-ttu-id="4d978-192">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d978-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d978-193">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d978-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d978-194">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d978-194">INPUTS</span></span>

### <span data-ttu-id="4d978-195">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d978-195">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4d978-196">System.String</span><span class="sxs-lookup"><span data-stu-id="4d978-196">System.String</span></span>

## <span data-ttu-id="4d978-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d978-197">OUTPUTS</span></span>

### <span data-ttu-id="4d978-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4d978-198">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4d978-199">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d978-199">NOTES</span></span>

## <span data-ttu-id="4d978-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d978-200">RELATED LINKS</span></span>
