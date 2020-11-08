---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: c15a7fca43568e63b8e7407b5c2048d03b9b6bc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191963"
---
# <span data-ttu-id="52b8d-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="52b8d-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="52b8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="52b8d-103">Creare una distribuzione in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="52b8d-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="52b8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b8d-104">SYNTAX</span></span>

### <span data-ttu-id="52b8d-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52b8d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52b8d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="52b8d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="52b8d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="52b8d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="52b8d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="52b8d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="52b8d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="52b8d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="52b8d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="52b8d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b8d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="52b8d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52b8d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="52b8d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52b8d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b8d-117">DESCRIPTION</span></span>
<span data-ttu-id="52b8d-118">Il cmdlet **New-AzManagementGroupDeployment** aggiunge una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="52b8d-119">Per aggiungere una distribuzione in un gruppo di gestione, specificare il gruppo di gestione, la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="52b8d-120">La posizione indica a Azure Resource Manager dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="52b8d-121">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="52b8d-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="52b8d-122">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="52b8d-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="52b8d-123">Per usare un modello personalizzato per la distribuzione, specifica il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="52b8d-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="52b8d-124">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="52b8d-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="52b8d-125">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="52b8d-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="52b8d-126">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="52b8d-127">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="52b8d-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="52b8d-128">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="52b8d-129">Per aggiungere risorse a un gruppo di risorse, usare il **nuovo AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52b8d-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="52b8d-130">Per aggiungere risorse a un abbonamento, usa il **nuovo-AzSubscriptionDeployment** che crea una distribuzione in ambito abbonamento, che distribuisce le risorse a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="52b8d-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="52b8d-131">Per aggiungere risorse nell'ambito del tenant, usare il **nuovo AzTenantDeployment** che crea una distribuzione in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="52b8d-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="52b8d-132">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b8d-132">EXAMPLES</span></span>

### <span data-ttu-id="52b8d-133">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="52b8d-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="52b8d-134">Questo comando crea una nuova distribuzione nel gruppo di gestione "myMG" usando un modello personalizzato e un file modello su disco, con il parametro di tag definito.</span><span class="sxs-lookup"><span data-stu-id="52b8d-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="52b8d-135">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="52b8d-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="52b8d-136">Esempio 2: usare un oggetto modello personalizzato e un file di parametro per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="52b8d-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="52b8d-137">Questo comando crea una nuova distribuzione nel gruppo di gestione "myMG" usando un modello personalizzato e un file modello su disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="52b8d-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="52b8d-138">I primi due comandi leggono il testo per il file del modello su disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="52b8d-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="52b8d-139">L'ultimo comando usa il parametro *TemplateObject* per specificare questo Hashtable e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="52b8d-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="52b8d-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52b8d-140">PARAMETERS</span></span>

### <span data-ttu-id="52b8d-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52b8d-141">-ApiVersion</span></span>
<span data-ttu-id="52b8d-142">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="52b8d-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="52b8d-143">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="52b8d-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="52b8d-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52b8d-144">-AsJob</span></span>
<span data-ttu-id="52b8d-145">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="52b8d-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52b8d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b8d-146">-DefaultProfile</span></span>
<span data-ttu-id="52b8d-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52b8d-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b8d-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="52b8d-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="52b8d-149">Livello del log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="52b8d-150">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52b8d-150">-Location</span></span>
<span data-ttu-id="52b8d-151">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="52b8d-152">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="52b8d-152">-ManagementGroupId</span></span>
<span data-ttu-id="52b8d-153">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-153">The management group ID.</span></span>

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

### <span data-ttu-id="52b8d-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b8d-154">-Name</span></span>
<span data-ttu-id="52b8d-155">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="52b8d-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="52b8d-156">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="52b8d-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="52b8d-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="52b8d-157">-Pre</span></span>
<span data-ttu-id="52b8d-158">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="52b8d-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="52b8d-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="52b8d-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="52b8d-160">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="52b8d-161">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="52b8d-162">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="52b8d-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="52b8d-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="52b8d-163">-Tag</span></span>
<span data-ttu-id="52b8d-164">Tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="52b8d-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="52b8d-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="52b8d-165">-TemplateFile</span></span>
<span data-ttu-id="52b8d-166">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="52b8d-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="52b8d-167">-TemplateObject</span></span>
<span data-ttu-id="52b8d-168">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="52b8d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="52b8d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="52b8d-170">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="52b8d-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="52b8d-171">-TemplateParameterObject</span></span>
<span data-ttu-id="52b8d-172">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="52b8d-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="52b8d-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="52b8d-173">-TemplateParameterUri</span></span>
<span data-ttu-id="52b8d-174">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="52b8d-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="52b8d-175">-TemplateUri</span></span>
<span data-ttu-id="52b8d-176">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="52b8d-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="52b8d-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="52b8d-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="52b8d-178">Tipi di modifica delle risorse delimitati da virgole da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="52b8d-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="52b8d-179">Applicabile quando è impostato l'opzione-WhatIf o-Confirm.</span><span class="sxs-lookup"><span data-stu-id="52b8d-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="52b8d-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="52b8d-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="52b8d-181">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="52b8d-181">The What-If result format.</span></span> <span data-ttu-id="52b8d-182">Applicabile quando è impostato l'opzione-WhatIf o-Confirm.</span><span class="sxs-lookup"><span data-stu-id="52b8d-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="52b8d-183">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52b8d-183">-Confirm</span></span>
<span data-ttu-id="52b8d-184">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b8d-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b8d-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b8d-185">-WhatIf</span></span>
<span data-ttu-id="52b8d-186">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52b8d-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b8d-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52b8d-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b8d-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b8d-188">CommonParameters</span></span>
<span data-ttu-id="52b8d-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b8d-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b8d-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52b8d-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b8d-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52b8d-191">INPUTS</span></span>

### <span data-ttu-id="52b8d-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="52b8d-192">System.Collections.Hashtable</span></span>

### <span data-ttu-id="52b8d-193">System. String</span><span class="sxs-lookup"><span data-stu-id="52b8d-193">System.String</span></span>

## <span data-ttu-id="52b8d-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b8d-194">OUTPUTS</span></span>

### <span data-ttu-id="52b8d-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="52b8d-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="52b8d-196">Note</span><span class="sxs-lookup"><span data-stu-id="52b8d-196">NOTES</span></span>

## <span data-ttu-id="52b8d-197">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b8d-197">RELATED LINKS</span></span>
