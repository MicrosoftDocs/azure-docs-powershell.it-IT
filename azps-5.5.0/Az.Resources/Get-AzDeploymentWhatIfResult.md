---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206026"
---
# <span data-ttu-id="4511e-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4511e-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="4511e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4511e-102">SYNOPSIS</span></span>
<span data-ttu-id="4511e-103">Ottiene un modello ARM un What-If risultato per una distribuzione con ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4511e-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="4511e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4511e-104">SYNTAX</span></span>

### <span data-ttu-id="4511e-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="4511e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4511e-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4511e-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4511e-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4511e-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4511e-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4511e-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4511e-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4511e-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4511e-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4511e-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4511e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4511e-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4511e-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4511e-117">DESCRIPTION</span></span>
<span data-ttu-id="4511e-118">Il cmdlet **Get-AzDeploymentWhatIfResult** ottiene il risultato ARM modello What-If distribuzione di modelli nell'ambito della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4511e-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="4511e-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="4511e-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="4511e-120">Per specificare il formato per il risultato restituito, usare il *parametro ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="4511e-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="4511e-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4511e-121">EXAMPLES</span></span>

### <span data-ttu-id="4511e-122">Esempio 1: Ottenere un risultato What-If'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4511e-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="4511e-123">Questo comando ottiene un risultato What-If'ambito di sottoscrizione corrente usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="4511e-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4511e-124">Il comando usa il *parametro Location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4511e-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4511e-125">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4511e-126">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4511e-127">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo da includere payload delle risorse completi.</span><span class="sxs-lookup"><span data-stu-id="4511e-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="4511e-128">Esempio 2: Ottenere un risultato What-If'ambito della sottoscrizione con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="4511e-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="4511e-129">Questo comando ottiene un risultato What-If'ambito di sottoscrizione corrente usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="4511e-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4511e-130">Il comando usa il *parametro Location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4511e-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4511e-131">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4511e-132">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4511e-133">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo che contenga solo ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4511e-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="4511e-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4511e-134">PARAMETERS</span></span>

### <span data-ttu-id="4511e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4511e-135">-DefaultProfile</span></span>
<span data-ttu-id="4511e-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4511e-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4511e-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4511e-137">-ExcludeChangeType</span></span>
<span data-ttu-id="4511e-138">Elenco separato da virgola dei tipi di modifica delle risorse da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="4511e-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="4511e-139">-Location</span><span class="sxs-lookup"><span data-stu-id="4511e-139">-Location</span></span>
<span data-ttu-id="4511e-140">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4511e-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4511e-141">-Name</span><span class="sxs-lookup"><span data-stu-id="4511e-141">-Name</span></span>
<span data-ttu-id="4511e-142">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="4511e-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4511e-143">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4511e-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="4511e-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="4511e-144">-Pre</span></span>
<span data-ttu-id="4511e-145">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4511e-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4511e-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="4511e-146">-ResultFormat</span></span>
<span data-ttu-id="4511e-147">Il What-If del risultato.</span><span class="sxs-lookup"><span data-stu-id="4511e-147">The What-If result format.</span></span>

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

### <span data-ttu-id="4511e-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4511e-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4511e-149">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="4511e-150">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="4511e-151">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="4511e-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4511e-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4511e-152">-TemplateFile</span></span>
<span data-ttu-id="4511e-153">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="4511e-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4511e-154">-TemplateObject</span></span>
<span data-ttu-id="4511e-155">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4511e-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4511e-156">-TemplateParameterFile</span></span>
<span data-ttu-id="4511e-157">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4511e-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4511e-158">-TemplateParameterObject</span></span>
<span data-ttu-id="4511e-159">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="4511e-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4511e-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4511e-160">-TemplateParameterUri</span></span>
<span data-ttu-id="4511e-161">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4511e-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4511e-162">-TemplateUri</span></span>
<span data-ttu-id="4511e-163">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="4511e-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="4511e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4511e-164">CommonParameters</span></span>
<span data-ttu-id="4511e-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4511e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4511e-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4511e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4511e-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="4511e-167">INPUTS</span></span>

### <span data-ttu-id="4511e-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4511e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4511e-169">System.String</span><span class="sxs-lookup"><span data-stu-id="4511e-169">System.String</span></span>

## <span data-ttu-id="4511e-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4511e-170">OUTPUTS</span></span>

### <span data-ttu-id="4511e-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="4511e-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="4511e-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="4511e-172">NOTES</span></span>

## <span data-ttu-id="4511e-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4511e-173">RELATED LINKS</span></span>
