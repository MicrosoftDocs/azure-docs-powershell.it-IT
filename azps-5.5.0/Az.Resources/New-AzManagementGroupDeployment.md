---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 95aa46354fb0ea1f2a1883fe7d319acfda220526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208467"
---
# <span data-ttu-id="d5c0a-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d5c0a-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d5c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c0a-103">Creare una distribuzione in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="d5c0a-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="d5c0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5c0a-104">SYNTAX</span></span>

### <span data-ttu-id="d5c0a-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="d5c0a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d5c0a-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d5c0a-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d5c0a-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="d5c0a-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d5c0a-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d5c0a-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c0a-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c0a-119">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c0a-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5c0a-120">DESCRIPTION</span></span>
<span data-ttu-id="d5c0a-121">Il cmdlet **New-AzManagementGroupDeployment aggiunge** una distribuzione a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-121">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="d5c0a-122">Per aggiungere una distribuzione a un gruppo di gestione, specificare il gruppo di gestione, la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-122">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="d5c0a-123">La posizione indica a Gestione risorse di Azure dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="d5c0a-124">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="d5c0a-125">Il modello include segnaposto di parametro per le risorse necessarie e valori di proprietà configurabili, come nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="d5c0a-126">Per usare un modello personalizzato per la distribuzione, specificare il *parametro TemplateFile* o *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="d5c0a-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d5c0a-127">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d5c0a-128">Per specificare i valori per i parametri del modello, specificare il *parametro TemplateParameterFile* o *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="d5c0a-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d5c0a-129">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d5c0a-130">Per usare parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare TAB per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d5c0a-131">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un file o in un oggetto parametro del modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="d5c0a-132">Per aggiungere risorse a un gruppo di risorse, usare **New-AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="d5c0a-133">Per aggiungere risorse a una sottoscrizione, usare **New-AzSubscriptionDeployment** che crea una distribuzione nell'ambito della sottoscrizione, che distribuisce risorse a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="d5c0a-134">Per aggiungere risorse nell'ambito tenant, usare **New-AzTenantDeployment** che crea una distribuzione nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-134">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="d5c0a-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5c0a-135">EXAMPLES</span></span>

### <span data-ttu-id="d5c0a-136">Esempio 1: Usare un modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d5c0a-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="d5c0a-137">Questo comando crea una nuova distribuzione nel gruppo di gestione "myMG" usando un modello personalizzato e un file di modello sul disco, con un parametro tag definito.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="d5c0a-138">Il comando usa il *parametro TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file contenente parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d5c0a-139">Esempio 2: Distribuire un modello archiviato in un account di archiviazione non pubblico usando un URI e un token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="d5c0a-139">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="d5c0a-140">Questo comando crea una nuova distribuzione usando il modello in TemplateUri che non è pubblico e per accedere a un parametro token che verrebbe fornito con il parametro QueryString.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-140">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="d5c0a-141">L'esecuzione di questo comando accede in modo efficace al modello usando https://example.com/example.json?foo l'URL.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-141">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="d5c0a-142">Può essere usato se si vuole usare un modello in un account di archiviazione fornendo il token di firma di accesso condiviso come QueryString</span><span class="sxs-lookup"><span data-stu-id="d5c0a-142">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="d5c0a-143">Esempio 3: Usare un oggetto modello personalizzato e un file di parametri per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d5c0a-143">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="d5c0a-144">Questo comando crea una nuova distribuzione nel gruppo di gestione "myMG" usando un modello personalizzato e un file di modello sul disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-144">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d5c0a-145">I primi due comandi leggono il testo del file modello sul disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-145">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d5c0a-146">L'ultimo comando usa *il parametro TemplateObject* per specificare questa tabella hash e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-146">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="d5c0a-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5c0a-147">PARAMETERS</span></span>

### <span data-ttu-id="d5c0a-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5c0a-148">-AsJob</span></span>
<span data-ttu-id="d5c0a-149">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d5c0a-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5c0a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-150">-DefaultProfile</span></span>
<span data-ttu-id="d5c0a-151">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c0a-152">-DeploymentLogLogLevel</span><span class="sxs-lookup"><span data-stu-id="d5c0a-152">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d5c0a-153">Livello di log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-153">The deployment debug log level.</span></span>

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

### <span data-ttu-id="d5c0a-154">-Location</span><span class="sxs-lookup"><span data-stu-id="d5c0a-154">-Location</span></span>
<span data-ttu-id="d5c0a-155">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-155">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d5c0a-156">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d5c0a-156">-ManagementGroupId</span></span>
<span data-ttu-id="d5c0a-157">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-157">The management group ID.</span></span>

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

### <span data-ttu-id="d5c0a-158">-Name</span><span class="sxs-lookup"><span data-stu-id="d5c0a-158">-Name</span></span>
<span data-ttu-id="d5c0a-159">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-159">The name of the deployment it's going to create.</span></span> <span data-ttu-id="d5c0a-160">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d5c0a-160">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="d5c0a-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="d5c0a-161">-Pre</span></span>
<span data-ttu-id="d5c0a-162">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d5c0a-163">-QueryString</span><span class="sxs-lookup"><span data-stu-id="d5c0a-163">-QueryString</span></span>
<span data-ttu-id="d5c0a-164">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-164">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="d5c0a-165">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="d5c0a-165">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="d5c0a-166">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d5c0a-166">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d5c0a-167">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-167">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="d5c0a-168">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-168">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="d5c0a-169">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-169">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d5c0a-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5c0a-170">-Tag</span></span>
<span data-ttu-id="d5c0a-171">I tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-171">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="d5c0a-172">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-172">-TemplateFile</span></span>
<span data-ttu-id="d5c0a-173">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-173">Local path to the template file.</span></span>

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

### <span data-ttu-id="d5c0a-174">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="d5c0a-174">-TemplateObject</span></span>
<span data-ttu-id="d5c0a-175">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-175">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d5c0a-176">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d5c0a-176">-TemplateParameterFile</span></span>
<span data-ttu-id="d5c0a-177">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-177">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d5c0a-178">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d5c0a-178">-TemplateParameterObject</span></span>
<span data-ttu-id="d5c0a-179">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-179">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d5c0a-180">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-180">-TemplateParameterUri</span></span>
<span data-ttu-id="d5c0a-181">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-181">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d5c0a-182">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="d5c0a-182">-TemplateSpecId</span></span>
<span data-ttu-id="d5c0a-183">ID risorsa del valore templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-183">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="d5c0a-184">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d5c0a-184">-TemplateUri</span></span>
<span data-ttu-id="d5c0a-185">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-185">Uri to the template file.</span></span>

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

### <span data-ttu-id="d5c0a-186">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="d5c0a-186">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="d5c0a-187">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-187">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="d5c0a-188">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-188">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="d5c0a-189">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="d5c0a-189">-WhatIfResultFormat</span></span>
<span data-ttu-id="d5c0a-190">Il What-If del risultato.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-190">The What-If result format.</span></span> <span data-ttu-id="d5c0a-191">Applicabile quando è impostata l'opzione -WhatIf o -Confirm.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="d5c0a-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5c0a-192">-Confirm</span></span>
<span data-ttu-id="d5c0a-193">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c0a-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c0a-194">-WhatIf</span></span>
<span data-ttu-id="d5c0a-195">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c0a-196">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c0a-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c0a-197">CommonParameters</span></span>
<span data-ttu-id="d5c0a-198">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c0a-199">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5c0a-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c0a-200">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5c0a-200">INPUTS</span></span>

### <span data-ttu-id="d5c0a-201">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d5c0a-201">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d5c0a-202">System.String</span><span class="sxs-lookup"><span data-stu-id="d5c0a-202">System.String</span></span>

## <span data-ttu-id="d5c0a-203">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5c0a-203">OUTPUTS</span></span>

### <span data-ttu-id="d5c0a-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d5c0a-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d5c0a-205">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5c0a-205">NOTES</span></span>

## <span data-ttu-id="d5c0a-206">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5c0a-206">RELATED LINKS</span></span>
