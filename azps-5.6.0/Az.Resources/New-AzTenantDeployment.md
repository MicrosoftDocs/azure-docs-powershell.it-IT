---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 029e1342caeac078d98418cfc508051b04dd816f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999821"
---
# <span data-ttu-id="0a45e-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a45e-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="0a45e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a45e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a45e-103">Creare una distribuzione con ambito tenant</span><span class="sxs-lookup"><span data-stu-id="0a45e-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="0a45e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a45e-104">SYNTAX</span></span>

### <span data-ttu-id="0a45e-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="0a45e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a45e-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a45e-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a45e-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="0a45e-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a45e-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0a45e-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0a45e-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a45e-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="0a45e-120">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a45e-121">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a45e-121">DESCRIPTION</span></span>
<span data-ttu-id="0a45e-122">Il cmdlet **New-AzTenantDeployment** aggiunge una distribuzione all'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="0a45e-122">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="0a45e-123">Per aggiungere una distribuzione nell'ambito tenant, specificare la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-123">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="0a45e-124">La posizione indica a Gestione risorse di Azure dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="0a45e-125">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="0a45e-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="0a45e-126">Il modello include segnaposto di parametro per le risorse necessarie e valori di proprietà configurabili, come nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="0a45e-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="0a45e-127">Per usare un modello personalizzato per la distribuzione, specificare il *parametro TemplateFile* o *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="0a45e-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0a45e-128">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="0a45e-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0a45e-129">Per specificare i valori per i parametri del modello, specificare il *parametro TemplateParameterFile* o *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="0a45e-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0a45e-130">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0a45e-131">Per usare parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="0a45e-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0a45e-132">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un file o in un oggetto parametro del modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="0a45e-133">Per aggiungere risorse a un gruppo di risorse, usare **New-AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a45e-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="0a45e-134">Per aggiungere risorse a una sottoscrizione, usare **New-AzSubscriptionDeployment** che crea una distribuzione nell'ambito della sottoscrizione, che distribuisce risorse a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="0a45e-135">Per aggiungere risorse a un gruppo di gestione, usare **New-AzManagementGroupDeployment,** che crea una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-135">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="0a45e-136">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a45e-136">EXAMPLES</span></span>

### <span data-ttu-id="0a45e-137">Esempio 1: Usare un modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="0a45e-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="0a45e-138">Questo comando crea una nuova distribuzione nell'ambito tenant corrente usando un modello personalizzato e un file di modello su disco, con un parametro tag definito.</span><span class="sxs-lookup"><span data-stu-id="0a45e-138">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="0a45e-139">Il comando usa il *parametro TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file contenente parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="0a45e-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0a45e-140">Esempio 2: Usare un oggetto modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="0a45e-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="0a45e-141">Questo comando crea una nuova distribuzione nel tenant corrente usando un modello personalizzato e un file di modello sul disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="0a45e-141">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0a45e-142">I primi due comandi leggono il testo del file modello sul disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="0a45e-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0a45e-143">L'ultimo comando usa *il parametro TemplateObject* per specificare questa tabella hash e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="0a45e-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="0a45e-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a45e-144">PARAMETERS</span></span>

### <span data-ttu-id="0a45e-145">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a45e-145">-AsJob</span></span>
<span data-ttu-id="0a45e-146">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0a45e-146">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a45e-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a45e-147">-DefaultProfile</span></span>
<span data-ttu-id="0a45e-148">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a45e-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a45e-149">-DeploymentLogLogLevel</span><span class="sxs-lookup"><span data-stu-id="0a45e-149">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0a45e-150">Livello di log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-150">The deployment debug log level.</span></span>

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

### <span data-ttu-id="0a45e-151">-Location</span><span class="sxs-lookup"><span data-stu-id="0a45e-151">-Location</span></span>
<span data-ttu-id="0a45e-152">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-152">The location to store deployment data.</span></span>

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

### <span data-ttu-id="0a45e-153">-Name</span><span class="sxs-lookup"><span data-stu-id="0a45e-153">-Name</span></span>
<span data-ttu-id="0a45e-154">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="0a45e-154">The name of the deployment it's going to create.</span></span> <span data-ttu-id="0a45e-155">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="0a45e-155">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="0a45e-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="0a45e-156">-Pre</span></span>
<span data-ttu-id="0a45e-157">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0a45e-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0a45e-158">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0a45e-158">-QueryString</span></span>
<span data-ttu-id="0a45e-159">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="0a45e-159">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="0a45e-160">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="0a45e-160">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="0a45e-161">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0a45e-161">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0a45e-162">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-162">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="0a45e-163">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro da associazione nel modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-163">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="0a45e-164">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="0a45e-164">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0a45e-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a45e-165">-Tag</span></span>
<span data-ttu-id="0a45e-166">I tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0a45e-166">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="0a45e-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0a45e-167">-TemplateFile</span></span>
<span data-ttu-id="0a45e-168">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-168">Local path to the template file.</span></span> <span data-ttu-id="0a45e-169">Tipo di file di modello supportati: json e bicipite.</span><span class="sxs-lookup"><span data-stu-id="0a45e-169">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="0a45e-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-170">-TemplateObject</span></span>
<span data-ttu-id="0a45e-171">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0a45e-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0a45e-172">-TemplateParameterFile</span></span>
<span data-ttu-id="0a45e-173">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-173">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0a45e-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0a45e-174">-TemplateParameterObject</span></span>
<span data-ttu-id="0a45e-175">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="0a45e-175">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45e-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-176">-TemplateParameterUri</span></span>
<span data-ttu-id="0a45e-177">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-177">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0a45e-178">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="0a45e-178">-TemplateSpecId</span></span>
<span data-ttu-id="0a45e-179">ID risorsa del templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="0a45e-179">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a45e-180">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0a45e-180">-TemplateUri</span></span>
<span data-ttu-id="0a45e-181">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="0a45e-181">Uri to the template file.</span></span>

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

### <span data-ttu-id="0a45e-182">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="0a45e-182">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="0a45e-183">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="0a45e-183">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="0a45e-184">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="0a45e-184">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="0a45e-185">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="0a45e-185">-WhatIfResultFormat</span></span>
<span data-ttu-id="0a45e-186">Formato What-If risultato.</span><span class="sxs-lookup"><span data-stu-id="0a45e-186">The What-If result format.</span></span> <span data-ttu-id="0a45e-187">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="0a45e-187">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="0a45e-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a45e-188">-Confirm</span></span>
<span data-ttu-id="0a45e-189">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a45e-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a45e-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a45e-190">-WhatIf</span></span>
<span data-ttu-id="0a45e-191">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a45e-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a45e-192">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a45e-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a45e-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a45e-193">CommonParameters</span></span>
<span data-ttu-id="0a45e-194">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a45e-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a45e-195">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a45e-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a45e-196">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a45e-196">INPUTS</span></span>

### <span data-ttu-id="0a45e-197">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a45e-197">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0a45e-198">System.String</span><span class="sxs-lookup"><span data-stu-id="0a45e-198">System.String</span></span>

## <span data-ttu-id="0a45e-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a45e-199">OUTPUTS</span></span>

### <span data-ttu-id="0a45e-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0a45e-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0a45e-201">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a45e-201">NOTES</span></span>

## <span data-ttu-id="0a45e-202">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a45e-202">RELATED LINKS</span></span>
