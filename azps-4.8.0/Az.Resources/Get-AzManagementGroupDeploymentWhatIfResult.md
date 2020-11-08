---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 39b652f1e6096f74da8d23baee10cd5b2ce54b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192182"
---
# <span data-ttu-id="50e13-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="50e13-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="50e13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50e13-102">SYNOPSIS</span></span>
<span data-ttu-id="50e13-103">Ottiene un modello ARM What-If risultato per una distribuzione nell'ambito di un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50e13-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="50e13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50e13-104">SYNTAX</span></span>

### <span data-ttu-id="50e13-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50e13-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50e13-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="50e13-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="50e13-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="50e13-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="50e13-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="50e13-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="50e13-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="50e13-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="50e13-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="50e13-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e13-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="50e13-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50e13-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="50e13-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50e13-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50e13-117">DESCRIPTION</span></span>
<span data-ttu-id="50e13-118">Il cmdlet **Get-AzManagementGroupDeploymentWhatIfResult** restituisce il modello ARM What-If risultato per una distribuzione di modelli nell'ambito del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="50e13-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="50e13-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="50e13-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="50e13-120">Per specificare il formato per il risultato restituito, usa il parametro *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="50e13-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="50e13-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50e13-121">EXAMPLES</span></span>

### <span data-ttu-id="50e13-122">Esempio 1: ottenere un risultato What-If all'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="50e13-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="50e13-123">Questo comando ottiene un risultato What-If nell'ambito del gruppo di gestione usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="50e13-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="50e13-124">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="50e13-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="50e13-125">Il comando usa il parametro *ManagementGroupId* per specificare il gruppo di gestione in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="50e13-126">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="50e13-127">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="50e13-128">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If per includere payload di risorse completo.</span><span class="sxs-lookup"><span data-stu-id="50e13-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="50e13-129">Esempio 2: ottenere un risultato What-If all'ambito del gruppo di gestione con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="50e13-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="50e13-130">Questo comando ottiene un risultato What-If nell'ambito del gruppo di gestione usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="50e13-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="50e13-131">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="50e13-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="50e13-132">Il comando usa il parametro *ManagementGroupId* per specificare il gruppo di gestione in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="50e13-133">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="50e13-134">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="50e13-135">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If solo per contenere gli ID delle risorse.</span><span class="sxs-lookup"><span data-stu-id="50e13-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="50e13-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50e13-136">PARAMETERS</span></span>

### <span data-ttu-id="50e13-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50e13-137">-ApiVersion</span></span>
<span data-ttu-id="50e13-138">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="50e13-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="50e13-139">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="50e13-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="50e13-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e13-140">-DefaultProfile</span></span>
<span data-ttu-id="50e13-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50e13-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50e13-142">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="50e13-142">-ExcludeChangeType</span></span>
<span data-ttu-id="50e13-143">Elenco delimitato da virgole dei tipi di modifica delle risorse da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="50e13-143">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="50e13-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50e13-144">-Location</span></span>
<span data-ttu-id="50e13-145">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="50e13-145">The location to store deployment data.</span></span>

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

### <span data-ttu-id="50e13-146">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="50e13-146">-ManagementGroupId</span></span>
<span data-ttu-id="50e13-147">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="50e13-147">The management group ID.</span></span>

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

### <span data-ttu-id="50e13-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="50e13-148">-Name</span></span>
<span data-ttu-id="50e13-149">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="50e13-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="50e13-150">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="50e13-150">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="50e13-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="50e13-151">-Pre</span></span>
<span data-ttu-id="50e13-152">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="50e13-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="50e13-153">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="50e13-153">-ResultFormat</span></span>
<span data-ttu-id="50e13-154">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="50e13-154">The What-If result format.</span></span>

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

### <span data-ttu-id="50e13-155">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="50e13-155">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="50e13-156">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-156">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="50e13-157">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-157">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="50e13-158">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="50e13-158">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="50e13-159">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="50e13-159">-TemplateFile</span></span>
<span data-ttu-id="50e13-160">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-160">Local path to the template file.</span></span>

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

### <span data-ttu-id="50e13-161">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="50e13-161">-TemplateObject</span></span>
<span data-ttu-id="50e13-162">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-162">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="50e13-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="50e13-163">-TemplateParameterFile</span></span>
<span data-ttu-id="50e13-164">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-164">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="50e13-165">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="50e13-165">-TemplateParameterObject</span></span>
<span data-ttu-id="50e13-166">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="50e13-166">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="50e13-167">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="50e13-167">-TemplateParameterUri</span></span>
<span data-ttu-id="50e13-168">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-168">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="50e13-169">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="50e13-169">-TemplateUri</span></span>
<span data-ttu-id="50e13-170">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="50e13-170">Uri to the template file.</span></span>

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

### <span data-ttu-id="50e13-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e13-171">CommonParameters</span></span>
<span data-ttu-id="50e13-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e13-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e13-173">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50e13-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e13-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50e13-174">INPUTS</span></span>

### <span data-ttu-id="50e13-175">System. String</span><span class="sxs-lookup"><span data-stu-id="50e13-175">System.String</span></span>

### <span data-ttu-id="50e13-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50e13-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="50e13-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50e13-177">OUTPUTS</span></span>

### <span data-ttu-id="50e13-178">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="50e13-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="50e13-179">Note</span><span class="sxs-lookup"><span data-stu-id="50e13-179">NOTES</span></span>

## <span data-ttu-id="50e13-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50e13-180">RELATED LINKS</span></span>
