---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: 8e25d83eda64bb9705829ff0a8b1dd40d6055953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474239"
---
# <span data-ttu-id="27dca-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="27dca-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="27dca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27dca-102">SYNOPSIS</span></span>
<span data-ttu-id="27dca-103">Ottiene un modello ARM What-If risultato per una distribuzione in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="27dca-103">Gets an ARM template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="27dca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27dca-104">SYNTAX</span></span>

### <span data-ttu-id="27dca-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27dca-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="27dca-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="27dca-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="27dca-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="27dca-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="27dca-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="27dca-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="27dca-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="27dca-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="27dca-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="27dca-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27dca-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="27dca-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27dca-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27dca-117">DESCRIPTION</span></span>
<span data-ttu-id="27dca-118">Il cmdlet **Get-AzTenantDeploymentWhatIfResult** restituisce il modello ARM What-If risultato per una distribuzione di modelli in corrispondenza dell'ambito tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="27dca-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="27dca-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="27dca-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="27dca-120">Per specificare il formato per il risultato restituito, usa il parametro *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="27dca-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="27dca-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27dca-121">EXAMPLES</span></span>

### <span data-ttu-id="27dca-122">Esempio 1: ottenere un risultato What-If all'ambito del tenant</span><span class="sxs-lookup"><span data-stu-id="27dca-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="27dca-123">Questo comando ottiene un risultato What-If nell'ambito del tenant usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="27dca-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="27dca-124">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="27dca-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="27dca-125">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="27dca-126">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="27dca-127">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If per includere payload di risorse completo.</span><span class="sxs-lookup"><span data-stu-id="27dca-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="27dca-128">Esempio 2: ottenere un risultato What-If all'ambito del tenant con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="27dca-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="27dca-129">Questo comando ottiene un risultato What-If nell'ambito del tenant usando un file di modello personalizzato e un file di parametro su disco.</span><span class="sxs-lookup"><span data-stu-id="27dca-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="27dca-130">Il comando usa il parametro *location* per specificare dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="27dca-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="27dca-131">Il comando usa il parametro *TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="27dca-132">Il comando usa il parametro *TemplateParameterFile* per specificare un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="27dca-133">Il comando usa il parametro *ResultFormat* per impostare il risultato What-If solo per contenere gli ID delle risorse.</span><span class="sxs-lookup"><span data-stu-id="27dca-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="27dca-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27dca-134">PARAMETERS</span></span>

### <span data-ttu-id="27dca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dca-135">-DefaultProfile</span></span>
<span data-ttu-id="27dca-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27dca-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27dca-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="27dca-137">-ExcludeChangeType</span></span>
<span data-ttu-id="27dca-138">Elenco delimitato da virgole dei tipi di modifica delle risorse da escludere dai risultati What-If.</span><span class="sxs-lookup"><span data-stu-id="27dca-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="27dca-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="27dca-139">-Location</span></span>
<span data-ttu-id="27dca-140">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="27dca-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="27dca-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="27dca-141">-Name</span></span>
<span data-ttu-id="27dca-142">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="27dca-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="27dca-143">Se non viene specificato, il nome del file del modello viene impostato automaticamente quando viene fornito un file di modello; il valore predefinito è l'ora corrente in cui viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="27dca-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="27dca-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="27dca-144">-Pre</span></span>
<span data-ttu-id="27dca-145">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="27dca-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="27dca-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="27dca-146">-ResultFormat</span></span>
<span data-ttu-id="27dca-147">Formato del risultato What-If.</span><span class="sxs-lookup"><span data-stu-id="27dca-147">The What-If result format.</span></span>

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

### <span data-ttu-id="27dca-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="27dca-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="27dca-149">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="27dca-150">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="27dca-151">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="27dca-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="27dca-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="27dca-152">-TemplateFile</span></span>
<span data-ttu-id="27dca-153">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="27dca-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="27dca-154">-TemplateObject</span></span>
<span data-ttu-id="27dca-155">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="27dca-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="27dca-156">-TemplateParameterFile</span></span>
<span data-ttu-id="27dca-157">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="27dca-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="27dca-158">-TemplateParameterObject</span></span>
<span data-ttu-id="27dca-159">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="27dca-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="27dca-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="27dca-160">-TemplateParameterUri</span></span>
<span data-ttu-id="27dca-161">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="27dca-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="27dca-162">-TemplateUri</span></span>
<span data-ttu-id="27dca-163">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="27dca-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="27dca-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dca-164">CommonParameters</span></span>
<span data-ttu-id="27dca-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27dca-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dca-166">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27dca-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dca-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27dca-167">INPUTS</span></span>

### <span data-ttu-id="27dca-168">System. String</span><span class="sxs-lookup"><span data-stu-id="27dca-168">System.String</span></span>

### <span data-ttu-id="27dca-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="27dca-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27dca-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27dca-170">OUTPUTS</span></span>

### <span data-ttu-id="27dca-171">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="27dca-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="27dca-172">Note</span><span class="sxs-lookup"><span data-stu-id="27dca-172">NOTES</span></span>

## <span data-ttu-id="27dca-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27dca-173">RELATED LINKS</span></span>
