---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178742"
---
# <span data-ttu-id="17bac-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="17bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17bac-102">SYNOPSIS</span></span>
<span data-ttu-id="17bac-103">Convalida la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17bac-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="17bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17bac-104">SYNTAX</span></span>

### <span data-ttu-id="17bac-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="17bac-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17bac-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17bac-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="17bac-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17bac-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17bac-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="17bac-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17bac-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17bac-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="17bac-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17bac-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bac-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="17bac-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bac-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17bac-117">DESCRIPTION</span></span>
<span data-ttu-id="17bac-118">Il **cmdlet Test-AzResourceGroupDeployment** determina se un modello di distribuzione del gruppo di risorse di Azure e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="17bac-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="17bac-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17bac-119">EXAMPLES</span></span>

### <span data-ttu-id="17bac-120">Esempio 1: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="17bac-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="17bac-121">Questo comando testa una distribuzione nel gruppo di risorse specificato usando una tabella hash in memoria creata dal file di modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="17bac-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="17bac-122">Esempio 2: Testare la distribuzione con il file di modello e il file di parametri</span><span class="sxs-lookup"><span data-stu-id="17bac-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="17bac-123">Questo comando testa una distribuzione nel gruppo di risorse e nella risorsa specificata usando il file di modello fornito e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="17bac-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="17bac-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17bac-124">PARAMETERS</span></span>

### <span data-ttu-id="17bac-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bac-125">-DefaultProfile</span></span>
<span data-ttu-id="17bac-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="17bac-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17bac-127">-Modalità</span><span class="sxs-lookup"><span data-stu-id="17bac-127">-Mode</span></span>
<span data-ttu-id="17bac-128">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="17bac-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="17bac-129">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="17bac-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17bac-130">Incrementale</span><span class="sxs-lookup"><span data-stu-id="17bac-130">Incremental</span></span>
- <span data-ttu-id="17bac-131">Completa</span><span class="sxs-lookup"><span data-stu-id="17bac-131">Complete</span></span>

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

### <span data-ttu-id="17bac-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="17bac-132">-Pre</span></span>
<span data-ttu-id="17bac-133">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="17bac-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="17bac-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bac-134">-ResourceGroupName</span></span>
<span data-ttu-id="17bac-135">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="17bac-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="17bac-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="17bac-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="17bac-137">Eseguire il rollback alla distribuzione riuscita con il nome specificato nel gruppo di risorse. Non deve essere usato se si usa -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="17bac-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="17bac-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="17bac-139">Eseguire il rollback all'ultima distribuzione riuscita nel gruppo di risorse, non deve essere presente se si usa -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="17bac-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="17bac-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="17bac-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="17bac-141">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="17bac-142">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="17bac-143">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="17bac-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="17bac-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="17bac-144">-TemplateFile</span></span>
<span data-ttu-id="17bac-145">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="17bac-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="17bac-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="17bac-146">-TemplateObject</span></span>
<span data-ttu-id="17bac-147">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="17bac-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="17bac-148">-TemplateParameterFile</span></span>
<span data-ttu-id="17bac-149">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="17bac-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="17bac-150">-TemplateParameterObject</span></span>
<span data-ttu-id="17bac-151">Specifica una tabella hash dei nomi e dei valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="17bac-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="17bac-152">-TemplateParameterUri</span></span>
<span data-ttu-id="17bac-153">Specifica l'URI di un file di parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="17bac-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="17bac-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="17bac-154">-TemplateUri</span></span>
<span data-ttu-id="17bac-155">Specifica l'URI di un file modello JSON.</span><span class="sxs-lookup"><span data-stu-id="17bac-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="17bac-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bac-156">CommonParameters</span></span>
<span data-ttu-id="17bac-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bac-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bac-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17bac-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bac-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="17bac-159">INPUTS</span></span>

### <span data-ttu-id="17bac-160">System.String</span><span class="sxs-lookup"><span data-stu-id="17bac-160">System.String</span></span>

### <span data-ttu-id="17bac-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="17bac-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="17bac-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17bac-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17bac-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17bac-163">OUTPUTS</span></span>

### <span data-ttu-id="17bac-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="17bac-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="17bac-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="17bac-165">NOTES</span></span>

## <span data-ttu-id="17bac-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17bac-166">RELATED LINKS</span></span>

[<span data-ttu-id="17bac-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="17bac-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="17bac-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="17bac-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="17bac-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


