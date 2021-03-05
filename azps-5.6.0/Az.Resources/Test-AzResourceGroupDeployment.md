---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976461"
---
# <span data-ttu-id="a48bf-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a48bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a48bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a48bf-103">Convalida la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a48bf-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="a48bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a48bf-104">SYNTAX</span></span>

### <span data-ttu-id="a48bf-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="a48bf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48bf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a48bf-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a48bf-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a48bf-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a48bf-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a48bf-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a48bf-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="a48bf-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a48bf-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a48bf-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48bf-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a48bf-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48bf-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="a48bf-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a48bf-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a48bf-120">DESCRIPTION</span></span>
<span data-ttu-id="a48bf-121">Il **cmdlet Test-AzResourceGroupDeployment** determina se un modello di distribuzione del gruppo di risorse di Azure e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="a48bf-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="a48bf-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a48bf-122">EXAMPLES</span></span>

### <span data-ttu-id="a48bf-123">Esempio 1: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="a48bf-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a48bf-124">Questo comando verifica una distribuzione nel gruppo di risorse specificato usando una tabella hash in memoria creata dal file di modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="a48bf-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="a48bf-125">Esempio 2: Testare la distribuzione con il file di modello e il file di parametri</span><span class="sxs-lookup"><span data-stu-id="a48bf-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="a48bf-126">Questo comando testa una distribuzione nel gruppo di risorse e nella risorsa specificata usando il file di modello fornito e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="a48bf-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="a48bf-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a48bf-127">PARAMETERS</span></span>

### <span data-ttu-id="a48bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48bf-128">-DefaultProfile</span></span>
<span data-ttu-id="a48bf-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a48bf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a48bf-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="a48bf-130">-Mode</span></span>
<span data-ttu-id="a48bf-131">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a48bf-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="a48bf-132">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="a48bf-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a48bf-133">Incrementale</span><span class="sxs-lookup"><span data-stu-id="a48bf-133">Incremental</span></span>
- <span data-ttu-id="a48bf-134">Completa</span><span class="sxs-lookup"><span data-stu-id="a48bf-134">Complete</span></span>

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

### <span data-ttu-id="a48bf-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a48bf-135">-Pre</span></span>
<span data-ttu-id="a48bf-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a48bf-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a48bf-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="a48bf-137">-QueryString</span></span>
<span data-ttu-id="a48bf-138">Stringa di query (ad esempio un token di firma di accesso condiviso) da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="a48bf-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="a48bf-139">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="a48bf-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="a48bf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48bf-140">-ResourceGroupName</span></span>
<span data-ttu-id="a48bf-141">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="a48bf-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="a48bf-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a48bf-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="a48bf-143">Eseguire il rollback alla distribuzione riuscita con il nome specificato nel gruppo di risorse. Non deve essere usato se si usa -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="a48bf-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48bf-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a48bf-145">Eseguire il rollback all'ultima distribuzione riuscita nel gruppo di risorse, non deve essere presente se si usa -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="a48bf-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a48bf-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a48bf-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a48bf-147">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a48bf-148">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro da associazione nel modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a48bf-149">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="a48bf-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a48bf-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a48bf-150">-TemplateFile</span></span>
<span data-ttu-id="a48bf-151">Specifica il percorso completo di un file modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="a48bf-152">Tipo di file di modello supportati: json e bicipite.</span><span class="sxs-lookup"><span data-stu-id="a48bf-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="a48bf-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a48bf-153">-TemplateObject</span></span>
<span data-ttu-id="a48bf-154">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a48bf-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a48bf-155">-TemplateParameterFile</span></span>
<span data-ttu-id="a48bf-156">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="a48bf-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a48bf-157">-TemplateParameterObject</span></span>
<span data-ttu-id="a48bf-158">Specifica una tabella hash dei nomi e dei valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="a48bf-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-159">-TemplateParameterUri</span></span>
<span data-ttu-id="a48bf-160">Specifica l'URI di un file di parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a48bf-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="a48bf-161">-TemplateSpecId</span></span>
<span data-ttu-id="a48bf-162">ID risorsa del templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a48bf-162">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="a48bf-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a48bf-163">-TemplateUri</span></span>
<span data-ttu-id="a48bf-164">Specifica l'URI di un file modello.</span><span class="sxs-lookup"><span data-stu-id="a48bf-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="a48bf-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48bf-165">CommonParameters</span></span>
<span data-ttu-id="a48bf-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a48bf-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48bf-167">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a48bf-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48bf-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="a48bf-168">INPUTS</span></span>

### <span data-ttu-id="a48bf-169">System.String</span><span class="sxs-lookup"><span data-stu-id="a48bf-169">System.String</span></span>

### <span data-ttu-id="a48bf-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a48bf-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a48bf-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a48bf-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a48bf-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a48bf-172">OUTPUTS</span></span>

### <span data-ttu-id="a48bf-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="a48bf-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="a48bf-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="a48bf-174">NOTES</span></span>

## <span data-ttu-id="a48bf-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a48bf-175">RELATED LINKS</span></span>

[<span data-ttu-id="a48bf-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a48bf-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a48bf-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a48bf-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a48bf-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


