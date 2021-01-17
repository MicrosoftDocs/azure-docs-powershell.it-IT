---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474291"
---
# <span data-ttu-id="2eb88-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="2eb88-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="2eb88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2eb88-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb88-103">Ottiene un modello ARM What-If risultato per una distribuzione nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2eb88-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="2eb88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eb88-104">SYNTAX</span></span>

### <span data-ttu-id="2eb88-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2eb88-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2eb88-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2eb88-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2eb88-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2eb88-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2eb88-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2eb88-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2eb88-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2eb88-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2eb88-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2eb88-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb88-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2eb88-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb88-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2eb88-117">DESCRIPTION</span></span>
<span data-ttu-id="2eb88-118">Il cmdlet **Get-AzDeploymentWhatIfResult** restituisce il modello ARM What-If risultato per una distribuzione di modelli nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="2eb88-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="2eb88-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="2eb88-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="2eb88-120">Per specificare il formato per il risultato restituito, usa il parametro *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="2eb88-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="2eb88-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eb88-121">EXAMPLES</span></span>

### <span data-ttu-id="2eb88-122">Esempio 1: ottenere un risultato What-If all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="2eb88-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="2eb88-123">Questo comando ottiene un risultato What-If nell'ambito dell'abbonamento corrente usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="2eb88-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2eb88-124">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2eb88-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="2eb88-125">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2eb88-126">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2eb88-127">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If per includere payload di risorse completo.</span><span class="sxs-lookup"><span data-stu-id="2eb88-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="2eb88-128">Esempio 2: ottenere un risultato What-If all'ambito dell'abbonamento con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="2eb88-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="2eb88-129">Questo comando ottiene un risultato What-If nell'ambito dell'abbonamento corrente usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="2eb88-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2eb88-130">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2eb88-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="2eb88-131">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2eb88-132">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2eb88-133">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If solo per contenere gli ID delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2eb88-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="2eb88-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2eb88-134">PARAMETERS</span></span>

### <span data-ttu-id="2eb88-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb88-135">-DefaultProfile</span></span>
<span data-ttu-id="2eb88-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb88-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb88-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2eb88-137">-ExcludeChangeType</span></span>
<span data-ttu-id="2eb88-138">Elenco delimitato da virgole dei tipi di modifica delle risorse da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="2eb88-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="2eb88-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2eb88-139">-Location</span></span>
<span data-ttu-id="2eb88-140">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2eb88-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2eb88-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="2eb88-141">-Name</span></span>
<span data-ttu-id="2eb88-142">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="2eb88-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="2eb88-143">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="2eb88-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2eb88-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="2eb88-144">-Pre</span></span>
<span data-ttu-id="2eb88-145">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2eb88-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2eb88-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="2eb88-146">-ResultFormat</span></span>
<span data-ttu-id="2eb88-147">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="2eb88-147">The What-If result format.</span></span>

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

### <span data-ttu-id="2eb88-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2eb88-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2eb88-149">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2eb88-150">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2eb88-151">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="2eb88-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2eb88-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2eb88-152">-TemplateFile</span></span>
<span data-ttu-id="2eb88-153">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="2eb88-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2eb88-154">-TemplateObject</span></span>
<span data-ttu-id="2eb88-155">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2eb88-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2eb88-156">-TemplateParameterFile</span></span>
<span data-ttu-id="2eb88-157">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2eb88-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2eb88-158">-TemplateParameterObject</span></span>
<span data-ttu-id="2eb88-159">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="2eb88-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2eb88-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2eb88-160">-TemplateParameterUri</span></span>
<span data-ttu-id="2eb88-161">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2eb88-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2eb88-162">-TemplateUri</span></span>
<span data-ttu-id="2eb88-163">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="2eb88-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="2eb88-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb88-164">CommonParameters</span></span>
<span data-ttu-id="2eb88-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb88-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb88-166">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eb88-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb88-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2eb88-167">INPUTS</span></span>

### <span data-ttu-id="2eb88-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2eb88-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2eb88-169">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb88-169">System.String</span></span>

## <span data-ttu-id="2eb88-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eb88-170">OUTPUTS</span></span>

### <span data-ttu-id="2eb88-171">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="2eb88-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="2eb88-172">Note</span><span class="sxs-lookup"><span data-stu-id="2eb88-172">NOTES</span></span>

## <span data-ttu-id="2eb88-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eb88-173">RELATED LINKS</span></span>
