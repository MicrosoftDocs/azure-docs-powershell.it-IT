---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 2e18ec6f920a1de2c890e29e34b4f15f58f0cfc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854849"
---
# <span data-ttu-id="d7fcc-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d7fcc-101">New-AzDeployment</span></span>

## <span data-ttu-id="d7fcc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fcc-103">Creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d7fcc-103">Create a deployment</span></span>

## <span data-ttu-id="d7fcc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7fcc-104">SYNTAX</span></span>

### <span data-ttu-id="d7fcc-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7fcc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d7fcc-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d7fcc-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d7fcc-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d7fcc-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d7fcc-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d7fcc-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d7fcc-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7fcc-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d7fcc-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7fcc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7fcc-117">DESCRIPTION</span></span>
<span data-ttu-id="d7fcc-118">Il cmdlet **New-AzDeployment** aggiunge una distribuzione nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="d7fcc-119">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="d7fcc-120">Una risorsa Azure è un'entità Azure gestita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="d7fcc-121">Una risorsa può essere attiva in un gruppo di risorse, ad esempio database server, database, sito Web, macchina virtuale o account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="d7fcc-122">In alternativa, può essere una risorsa a livello di abbonamento, come la definizione dei ruoli, la definizione dei criteri e così via.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="d7fcc-123">Per aggiungere risorse a un gruppo di risorse, usare il **nuovo AzResourceGroupDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="d7fcc-124">Il cmdlet **New-AzDeployment** crea una distribuzione nell'ambito dell'abbonamento corrente, che distribuisce le risorse a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="d7fcc-125">Per aggiungere una distribuzione in abbonamento, specificare la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="d7fcc-126">La posizione indica a Azure Resource Manager dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="d7fcc-127">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="d7fcc-128">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="d7fcc-129">Per usare un modello personalizzato per la distribuzione, specifica il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="d7fcc-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d7fcc-130">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d7fcc-131">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d7fcc-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d7fcc-132">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d7fcc-133">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d7fcc-134">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="d7fcc-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7fcc-135">EXAMPLES</span></span>

### <span data-ttu-id="d7fcc-136">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d7fcc-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="d7fcc-137">Questo comando crea una nuova distribuzione nell'ambito dell'abbonamento corrente usando un modello personalizzato e un file modello su disco.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="d7fcc-138">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="d7fcc-139">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="d7fcc-140">Esempio 2: usare un oggetto modello personalizzato e un file di parametro per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="d7fcc-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="d7fcc-141">Questo comando crea una nuova distribuzione nell'ambito dell'abbonamento corrente usando un modello personalizzato e un file modello su disco che è stato convertito in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d7fcc-142">I primi due comandi leggono il testo per il file del modello su disco e lo convertono in una tabella hash in memoria.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d7fcc-143">L'ultimo comando usa il parametro *TemplateObject* per specificare questo Hashtable e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="d7fcc-144">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="d7fcc-145">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7fcc-145">PARAMETERS</span></span>

### <span data-ttu-id="d7fcc-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d7fcc-146">-ApiVersion</span></span>
<span data-ttu-id="d7fcc-147">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d7fcc-148">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d7fcc-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7fcc-149">-AsJob</span></span>
<span data-ttu-id="d7fcc-150">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d7fcc-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7fcc-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-151">-DefaultProfile</span></span>
<span data-ttu-id="d7fcc-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7fcc-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d7fcc-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d7fcc-154">Livello del log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="d7fcc-155">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d7fcc-155">-Location</span></span>
<span data-ttu-id="d7fcc-156">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d7fcc-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7fcc-157">-Name</span></span>
<span data-ttu-id="d7fcc-158">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-158">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="d7fcc-159">Valido solo quando viene usato un modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-159">Only valid when a template is used.</span></span>
<span data-ttu-id="d7fcc-160">Quando viene usato un modello, se l'utente non specifica un nome di distribuzione, usa l'ora corrente, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d7fcc-160">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="d7fcc-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="d7fcc-161">-Pre</span></span>
<span data-ttu-id="d7fcc-162">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d7fcc-163">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d7fcc-163">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d7fcc-164">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-164">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="d7fcc-165">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-165">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="d7fcc-166">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-166">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d7fcc-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-167">-TemplateFile</span></span>
<span data-ttu-id="d7fcc-168">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-168">Local path to the template file.</span></span>

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

### <span data-ttu-id="d7fcc-169">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="d7fcc-169">-TemplateObject</span></span>
<span data-ttu-id="d7fcc-170">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-170">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d7fcc-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d7fcc-171">-TemplateParameterFile</span></span>
<span data-ttu-id="d7fcc-172">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-172">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d7fcc-173">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d7fcc-173">-TemplateParameterObject</span></span>
<span data-ttu-id="d7fcc-174">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-174">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d7fcc-175">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d7fcc-175">-TemplateParameterUri</span></span>
<span data-ttu-id="d7fcc-176">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-176">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d7fcc-177">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d7fcc-177">-TemplateUri</span></span>
<span data-ttu-id="d7fcc-178">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-178">Uri to the template file.</span></span>

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

### <span data-ttu-id="d7fcc-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7fcc-179">-Confirm</span></span>
<span data-ttu-id="d7fcc-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7fcc-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7fcc-181">-WhatIf</span></span>
<span data-ttu-id="d7fcc-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7fcc-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7fcc-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fcc-184">CommonParameters</span></span>
<span data-ttu-id="d7fcc-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fcc-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fcc-186">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fcc-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fcc-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7fcc-187">INPUTS</span></span>

### <span data-ttu-id="d7fcc-188">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7fcc-188">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d7fcc-189">System. String</span><span class="sxs-lookup"><span data-stu-id="d7fcc-189">System.String</span></span>

## <span data-ttu-id="d7fcc-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7fcc-190">OUTPUTS</span></span>

### <span data-ttu-id="d7fcc-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="d7fcc-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d7fcc-192">Note</span><span class="sxs-lookup"><span data-stu-id="d7fcc-192">NOTES</span></span>

## <span data-ttu-id="d7fcc-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7fcc-193">RELATED LINKS</span></span>
