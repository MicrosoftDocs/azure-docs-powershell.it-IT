---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 1b45c08f2906f3b1bec827a7f870d2c901bbb2b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963805"
---
# <span data-ttu-id="7a311-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a311-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="7a311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a311-102">SYNOPSIS</span></span>
<span data-ttu-id="7a311-103">Ottiene un modello che What-If risultato per una distribuzione nell'ambito del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a311-103">Gets a template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="7a311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a311-104">SYNTAX</span></span>

### <span data-ttu-id="7a311-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="7a311-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a311-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7a311-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7a311-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7a311-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7a311-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7a311-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7a311-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7a311-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7a311-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7a311-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a311-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7a311-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a311-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7a311-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a311-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a311-117">DESCRIPTION</span></span>
<span data-ttu-id="7a311-118">Il cmdlet **Get-AzResourceGroupDeploymentWhatIfResult** ottiene il risultato ARM modello What-If per la distribuzione di un modello nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7a311-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="7a311-119">Restituisce un elenco di modifiche che indicano quali risorse verranno aggiornate se la distribuzione viene applicata senza apportare modifiche alle risorse reali.</span><span class="sxs-lookup"><span data-stu-id="7a311-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="7a311-120">Per specificare il formato per il risultato restituito, usare il *parametro ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="7a311-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="7a311-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a311-121">EXAMPLES</span></span>

### <span data-ttu-id="7a311-122">Esempio 1: Ottenere un risultato What-If'ambito del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7a311-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="7a311-123">Questo comando ottiene un risultato What-If'ambito del gruppo di risorse specificato usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="7a311-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7a311-124">Il comando usa il *parametro ResourceGroupName* per specificare un gruppo di risorse in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7a311-125">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7a311-126">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7a311-127">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo da includere payload delle risorse completi.</span><span class="sxs-lookup"><span data-stu-id="7a311-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="7a311-128">Esempio 2: Ottenere un risultato What-If'ambito del gruppo di risorse con ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="7a311-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="7a311-129">Questo comando ottiene un risultato What-If'ambito del gruppo di risorse specificato usando un file di modello personalizzato e un file di parametri sul disco.</span><span class="sxs-lookup"><span data-stu-id="7a311-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7a311-130">Il comando usa il *parametro ResourceGroupName* per specificare un gruppo di risorse in cui verrà distribuito il modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7a311-131">Il comando usa il *parametro TemplateFile* per specificare un file modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7a311-132">Il comando usa il *parametro TemplateParameterFile* per specificare un file con parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7a311-133">Il comando usa il *parametro ResultFormat* per impostare What-If risultato in modo che contenga solo ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7a311-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="7a311-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a311-134">PARAMETERS</span></span>

### <span data-ttu-id="7a311-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a311-135">-DefaultProfile</span></span>
<span data-ttu-id="7a311-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a311-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a311-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7a311-137">-ExcludeChangeType</span></span>
<span data-ttu-id="7a311-138">Tipi di modifica delle risorse con valori delimitati da virgole da escludere What-If risultati.</span><span class="sxs-lookup"><span data-stu-id="7a311-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="7a311-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="7a311-139">-Mode</span></span>
<span data-ttu-id="7a311-140">Modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7a311-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a311-141">-Name</span><span class="sxs-lookup"><span data-stu-id="7a311-141">-Name</span></span>
<span data-ttu-id="7a311-142">Il nome della distribuzione che creerà.</span><span class="sxs-lookup"><span data-stu-id="7a311-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="7a311-143">Se non è specificato, quando viene fornito un file modello viene utilizzato il nome predefinito del file modello; per impostazione predefinita, quando viene fornito un oggetto modello, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="7a311-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a311-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="7a311-144">-Pre</span></span>
<span data-ttu-id="7a311-145">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7a311-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7a311-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a311-146">-ResourceGroupName</span></span>
<span data-ttu-id="7a311-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a311-147">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a311-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="7a311-148">-ResultFormat</span></span>
<span data-ttu-id="7a311-149">Formato What-If risultato.</span><span class="sxs-lookup"><span data-stu-id="7a311-149">The What-If result format.</span></span>

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

### <span data-ttu-id="7a311-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7a311-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7a311-151">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7a311-152">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7a311-153">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="7a311-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7a311-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7a311-154">-TemplateFile</span></span>
<span data-ttu-id="7a311-155">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-155">Local path to the template file.</span></span> <span data-ttu-id="7a311-156">Tipo di file di modello supportati: json e bicipite.</span><span class="sxs-lookup"><span data-stu-id="7a311-156">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="7a311-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="7a311-157">-TemplateObject</span></span>
<span data-ttu-id="7a311-158">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7a311-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7a311-159">-TemplateParameterFile</span></span>
<span data-ttu-id="7a311-160">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7a311-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7a311-161">-TemplateParameterObject</span></span>
<span data-ttu-id="7a311-162">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="7a311-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7a311-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7a311-163">-TemplateParameterUri</span></span>
<span data-ttu-id="7a311-164">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7a311-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7a311-165">-TemplateUri</span></span>
<span data-ttu-id="7a311-166">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="7a311-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="7a311-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a311-167">CommonParameters</span></span>
<span data-ttu-id="7a311-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a311-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a311-169">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a311-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a311-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a311-170">INPUTS</span></span>

### <span data-ttu-id="7a311-171">System.String</span><span class="sxs-lookup"><span data-stu-id="7a311-171">System.String</span></span>

### <span data-ttu-id="7a311-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="7a311-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="7a311-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a311-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7a311-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a311-174">OUTPUTS</span></span>

### <span data-ttu-id="7a311-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="7a311-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="7a311-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a311-176">NOTES</span></span>

## <span data-ttu-id="7a311-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a311-177">RELATED LINKS</span></span>
