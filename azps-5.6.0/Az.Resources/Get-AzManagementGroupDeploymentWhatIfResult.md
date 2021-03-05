---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971853"
---
# <span data-ttu-id="9b5cf-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="9b5cf-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="9b5cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5cf-103">Ottiene un modello che What-If risultato per una distribuzione nell'ambito del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="9b5cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b5cf-104">SYNTAX</span></span>

### <span data-ttu-id="9b5cf-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="9b5cf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9b5cf-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9b5cf-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9b5cf-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9b5cf-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9b5cf-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9b5cf-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9b5cf-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b5cf-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9b5cf-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b5cf-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b5cf-117">DESCRIPTION</span></span>
<span data-ttu-id="9b5cf-118">Il cmdlet **Get-AzManagementGroupDeploymentWhatIfResult** ottiene il risultato ARM modello What-If per la distribuzione di modelli nell'ambito del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="9b5cf-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="9b5cf-120">Per specificare il formato per il risultato restituito, usare il *parametro ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="9b5cf-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="9b5cf-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b5cf-121">EXAMPLES</span></span>

### <span data-ttu-id="9b5cf-122">Esempio 1: Ottenere un risultato What-If'ambito del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9b5cf-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="9b5cf-123">Questo comando ottiene un risultato What-If'ambito del gruppo di gestione usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="9b5cf-124">Il comando usa il *parametro Location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="9b5cf-125">Il comando usa il *parametro ManagementGroupId* per specificare il gruppo di gestione in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="9b5cf-126">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="9b5cf-127">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="9b5cf-128">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo da includere payload delle risorse completi.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="9b5cf-129">Esempio 2: Ottenere un risultato What-If'ambito del gruppo di gestione con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="9b5cf-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="9b5cf-130">Questo comando ottiene un risultato What-If'ambito del gruppo di gestione usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="9b5cf-131">Il comando usa il *parametro Location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="9b5cf-132">Il comando usa il *parametro ManagementGroupId* per specificare il gruppo di gestione in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="9b5cf-133">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="9b5cf-134">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="9b5cf-135">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo che contenga solo ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="9b5cf-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b5cf-136">PARAMETERS</span></span>

### <span data-ttu-id="9b5cf-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-137">-DefaultProfile</span></span>
<span data-ttu-id="9b5cf-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5cf-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="9b5cf-139">-ExcludeChangeType</span></span>
<span data-ttu-id="9b5cf-140">Elenco separato da virgole dei tipi di modifica delle risorse da escludere What-If risorse.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="9b5cf-141">-Location</span><span class="sxs-lookup"><span data-stu-id="9b5cf-141">-Location</span></span>
<span data-ttu-id="9b5cf-142">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9b5cf-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9b5cf-143">-ManagementGroupId</span></span>
<span data-ttu-id="9b5cf-144">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-144">The management group ID.</span></span>

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

### <span data-ttu-id="9b5cf-145">-Name</span><span class="sxs-lookup"><span data-stu-id="9b5cf-145">-Name</span></span>
<span data-ttu-id="9b5cf-146">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="9b5cf-147">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="9b5cf-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="9b5cf-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="9b5cf-148">-Pre</span></span>
<span data-ttu-id="9b5cf-149">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9b5cf-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="9b5cf-150">-ResultFormat</span></span>
<span data-ttu-id="9b5cf-151">Formato What-If risultato.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-151">The What-If result format.</span></span>

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

### <span data-ttu-id="9b5cf-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9b5cf-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9b5cf-153">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="9b5cf-154">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro da associazione nel modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="9b5cf-155">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9b5cf-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-156">-TemplateFile</span></span>
<span data-ttu-id="9b5cf-157">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-157">Local path to the template file.</span></span> <span data-ttu-id="9b5cf-158">Tipo di file di modello supportati: json e bicipite.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-158">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="9b5cf-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9b5cf-159">-TemplateObject</span></span>
<span data-ttu-id="9b5cf-160">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="9b5cf-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9b5cf-161">-TemplateParameterFile</span></span>
<span data-ttu-id="9b5cf-162">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9b5cf-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9b5cf-163">-TemplateParameterObject</span></span>
<span data-ttu-id="9b5cf-164">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9b5cf-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9b5cf-165">-TemplateParameterUri</span></span>
<span data-ttu-id="9b5cf-166">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9b5cf-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9b5cf-167">-TemplateUri</span></span>
<span data-ttu-id="9b5cf-168">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="9b5cf-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5cf-169">CommonParameters</span></span>
<span data-ttu-id="9b5cf-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5cf-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b5cf-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5cf-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b5cf-172">INPUTS</span></span>

### <span data-ttu-id="9b5cf-173">System.String</span><span class="sxs-lookup"><span data-stu-id="9b5cf-173">System.String</span></span>

### <span data-ttu-id="9b5cf-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b5cf-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b5cf-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b5cf-175">OUTPUTS</span></span>

### <span data-ttu-id="9b5cf-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="9b5cf-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="9b5cf-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b5cf-177">NOTES</span></span>

## <span data-ttu-id="9b5cf-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b5cf-178">RELATED LINKS</span></span>
