---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474220"
---
# <span data-ttu-id="41ece-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="41ece-101">New-AzDeployment</span></span>

## <span data-ttu-id="41ece-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41ece-102">SYNOPSIS</span></span>
<span data-ttu-id="41ece-103">Creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="41ece-103">Create a deployment</span></span>

## <span data-ttu-id="41ece-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41ece-104">SYNTAX</span></span>

### <span data-ttu-id="41ece-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41ece-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="41ece-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="41ece-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="41ece-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="41ece-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="41ece-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="41ece-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="41ece-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="41ece-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="41ece-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="41ece-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ece-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="41ece-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ece-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41ece-117">DESCRIPTION</span></span>
<span data-ttu-id="41ece-118">Il cmdlet **New-AzDeployment** aggiunge una distribuzione nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="41ece-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="41ece-119">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="41ece-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="41ece-120">Una risorsa Azure è un'entità Azure gestita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="41ece-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="41ece-121">Una risorsa può essere attiva in un gruppo di risorse, ad esempio database server, database, sito Web, macchina virtuale o account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="41ece-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="41ece-122">In alternativa, può essere una risorsa a livello di abbonamento, come la definizione dei ruoli, la definizione dei criteri e così via.</span><span class="sxs-lookup"><span data-stu-id="41ece-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="41ece-123">Per aggiungere risorse a un gruppo di risorse, usare il **nuovo AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41ece-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="41ece-124">Il cmdlet **New-AzDeployment** crea una distribuzione nell'ambito dell'abbonamento corrente, che distribuisce le risorse a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="41ece-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="41ece-125">Per aggiungere una distribuzione in abbonamento, specificare la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="41ece-126">La posizione indica a Azure Resource Manager dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="41ece-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="41ece-127">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="41ece-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="41ece-128">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="41ece-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="41ece-129">Per usare un modello personalizzato per la distribuzione, specifica il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="41ece-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="41ece-130">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="41ece-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="41ece-131">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="41ece-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="41ece-132">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="41ece-133">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="41ece-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="41ece-134">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="41ece-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41ece-135">EXAMPLES</span></span>

### <span data-ttu-id="41ece-136">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="41ece-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="41ece-137">Questo comando crea una nuova distribuzione nell'ambito dell'abbonamento corrente usando un modello personalizzato e un file modello su disco, con il parametro di tag definito.</span><span class="sxs-lookup"><span data-stu-id="41ece-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="41ece-138">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="41ece-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="41ece-139">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="41ece-140">Esempio 2: usare un oggetto modello personalizzato e un file di parametro per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="41ece-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="41ece-141">Questo comando crea una nuova distribuzione nell'ambito dell'abbonamento corrente usando un modello personalizzato e un file modello su disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="41ece-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="41ece-142">I primi due comandi leggono il testo per il file del modello su disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="41ece-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="41ece-143">L'ultimo comando usa il parametro *TemplateObject* per specificare questo Hashtable e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="41ece-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="41ece-144">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="41ece-145">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41ece-145">PARAMETERS</span></span>

### <span data-ttu-id="41ece-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41ece-146">-AsJob</span></span>
<span data-ttu-id="41ece-147">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41ece-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41ece-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ece-148">-DefaultProfile</span></span>
<span data-ttu-id="41ece-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41ece-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41ece-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="41ece-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="41ece-151">Livello del log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="41ece-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="41ece-152">-Posizione</span><span class="sxs-lookup"><span data-stu-id="41ece-152">-Location</span></span>
<span data-ttu-id="41ece-153">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="41ece-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="41ece-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="41ece-154">-Name</span></span>
<span data-ttu-id="41ece-155">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="41ece-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="41ece-156">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="41ece-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="41ece-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="41ece-157">-Pre</span></span>
<span data-ttu-id="41ece-158">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="41ece-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="41ece-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="41ece-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="41ece-160">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="41ece-161">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="41ece-162">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="41ece-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="41ece-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="41ece-163">-Tag</span></span>
<span data-ttu-id="41ece-164">Tag da inserire nella distribuzione.</span><span class="sxs-lookup"><span data-stu-id="41ece-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="41ece-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="41ece-165">-TemplateFile</span></span>
<span data-ttu-id="41ece-166">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="41ece-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="41ece-167">-TemplateObject</span></span>
<span data-ttu-id="41ece-168">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="41ece-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="41ece-169">-TemplateParameterFile</span></span>
<span data-ttu-id="41ece-170">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="41ece-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="41ece-171">-TemplateParameterObject</span></span>
<span data-ttu-id="41ece-172">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="41ece-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="41ece-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="41ece-173">-TemplateParameterUri</span></span>
<span data-ttu-id="41ece-174">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="41ece-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="41ece-175">-TemplateUri</span></span>
<span data-ttu-id="41ece-176">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="41ece-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="41ece-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="41ece-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="41ece-178">Tipi di modifica delle risorse delimitati da virgole da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="41ece-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="41ece-179">Applicabile quando è impostato l'opzione-WhatIf o-Confirm.</span><span class="sxs-lookup"><span data-stu-id="41ece-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="41ece-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="41ece-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="41ece-181">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="41ece-181">The What-If result format.</span></span>

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

### <span data-ttu-id="41ece-182">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41ece-182">-Confirm</span></span>
<span data-ttu-id="41ece-183">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41ece-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ece-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ece-184">-WhatIf</span></span>
<span data-ttu-id="41ece-185">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41ece-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41ece-186">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41ece-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ece-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ece-187">CommonParameters</span></span>
<span data-ttu-id="41ece-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ece-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ece-189">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41ece-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ece-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41ece-190">INPUTS</span></span>

### <span data-ttu-id="41ece-191">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41ece-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41ece-192">System. String</span><span class="sxs-lookup"><span data-stu-id="41ece-192">System.String</span></span>

## <span data-ttu-id="41ece-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41ece-193">OUTPUTS</span></span>

### <span data-ttu-id="41ece-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="41ece-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="41ece-195">Note</span><span class="sxs-lookup"><span data-stu-id="41ece-195">NOTES</span></span>

## <span data-ttu-id="41ece-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41ece-196">RELATED LINKS</span></span>
