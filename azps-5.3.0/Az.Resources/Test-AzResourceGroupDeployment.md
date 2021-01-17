---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474141"
---
# <span data-ttu-id="90d95-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="90d95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90d95-102">SYNOPSIS</span></span>
<span data-ttu-id="90d95-103">Convalida una distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90d95-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="90d95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90d95-104">SYNTAX</span></span>

### <span data-ttu-id="90d95-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90d95-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="90d95-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="90d95-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="90d95-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="90d95-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="90d95-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="90d95-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="90d95-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="90d95-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="90d95-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="90d95-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d95-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="90d95-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90d95-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90d95-117">DESCRIPTION</span></span>
<span data-ttu-id="90d95-118">Il cmdlet **test-AzResourceGroupDeployment** determina se un modello di distribuzione di Azure Resource Group e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="90d95-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="90d95-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90d95-119">EXAMPLES</span></span>

### <span data-ttu-id="90d95-120">Esempio 1: testare la distribuzione con un oggetto modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="90d95-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="90d95-121">Questo comando verifica una distribuzione nel gruppo di risorse specifico usando la tabella hash in memoria creata dal file di modello indicato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="90d95-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="90d95-122">Esempio 2: testare la distribuzione tramite il file di modello e il file di parametro</span><span class="sxs-lookup"><span data-stu-id="90d95-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="90d95-123">Questo comando verifica una distribuzione nel gruppo di risorse e nella risorsa specificati usando il file di modello e un file di parametro specificati.</span><span class="sxs-lookup"><span data-stu-id="90d95-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="90d95-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90d95-124">PARAMETERS</span></span>

### <span data-ttu-id="90d95-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d95-125">-DefaultProfile</span></span>
<span data-ttu-id="90d95-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90d95-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90d95-127">-Modalità</span><span class="sxs-lookup"><span data-stu-id="90d95-127">-Mode</span></span>
<span data-ttu-id="90d95-128">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="90d95-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="90d95-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="90d95-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90d95-130">Incrementale</span><span class="sxs-lookup"><span data-stu-id="90d95-130">Incremental</span></span>
- <span data-ttu-id="90d95-131">Completare</span><span class="sxs-lookup"><span data-stu-id="90d95-131">Complete</span></span>

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

### <span data-ttu-id="90d95-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="90d95-132">-Pre</span></span>
<span data-ttu-id="90d95-133">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="90d95-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="90d95-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d95-134">-ResourceGroupName</span></span>
<span data-ttu-id="90d95-135">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="90d95-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="90d95-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="90d95-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="90d95-137">Il rollback alla distribuzione corretta con il nome indicato nel gruppo di risorse non deve essere usato se viene usato-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="90d95-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="90d95-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="90d95-139">Il rollback all'ultima distribuzione corretta nel gruppo di risorse non dovrebbe essere presente se viene usato-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="90d95-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="90d95-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="90d95-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="90d95-141">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="90d95-142">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="90d95-143">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="90d95-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="90d95-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="90d95-144">-TemplateFile</span></span>
<span data-ttu-id="90d95-145">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="90d95-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="90d95-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="90d95-146">-TemplateObject</span></span>
<span data-ttu-id="90d95-147">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="90d95-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="90d95-148">-TemplateParameterFile</span></span>
<span data-ttu-id="90d95-149">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="90d95-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="90d95-150">-TemplateParameterObject</span></span>
<span data-ttu-id="90d95-151">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="90d95-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="90d95-152">-TemplateParameterUri</span></span>
<span data-ttu-id="90d95-153">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="90d95-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="90d95-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="90d95-154">-TemplateUri</span></span>
<span data-ttu-id="90d95-155">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="90d95-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="90d95-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d95-156">CommonParameters</span></span>
<span data-ttu-id="90d95-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d95-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d95-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90d95-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d95-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90d95-159">INPUTS</span></span>

### <span data-ttu-id="90d95-160">System. String</span><span class="sxs-lookup"><span data-stu-id="90d95-160">System.String</span></span>

### <span data-ttu-id="90d95-161">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="90d95-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="90d95-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90d95-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90d95-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90d95-163">OUTPUTS</span></span>

### <span data-ttu-id="90d95-164">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="90d95-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="90d95-165">Note</span><span class="sxs-lookup"><span data-stu-id="90d95-165">NOTES</span></span>

## <span data-ttu-id="90d95-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90d95-166">RELATED LINKS</span></span>

[<span data-ttu-id="90d95-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="90d95-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="90d95-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="90d95-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="90d95-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


