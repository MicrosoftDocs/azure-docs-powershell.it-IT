---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178743"
---
# <span data-ttu-id="8e25d-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e25d-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="8e25d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e25d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e25d-103">Convalida una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8e25d-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="8e25d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e25d-104">SYNTAX</span></span>

### <span data-ttu-id="8e25d-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="8e25d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8e25d-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8e25d-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8e25d-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8e25d-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8e25d-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8e25d-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8e25d-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8e25d-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8e25d-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e25d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8e25d-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8e25d-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e25d-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e25d-117">DESCRIPTION</span></span>
<span data-ttu-id="8e25d-118">Il cmdlet **Test-AzManagementGroupDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8e25d-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="8e25d-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e25d-119">EXAMPLES</span></span>

### <span data-ttu-id="8e25d-120">Esempio 1: Testare la distribuzione con un modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="8e25d-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="8e25d-121">Questo comando testa una distribuzione nel gruppo di gestione "myMG" usando il file di modello e i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="8e25d-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="8e25d-122">Esempio 2: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="8e25d-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="8e25d-123">Questo comando verifica una distribuzione nel gruppo di gestione "myMG" usando una tabella hash in memoria creata dal file modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="8e25d-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="8e25d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e25d-124">PARAMETERS</span></span>

### <span data-ttu-id="8e25d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e25d-125">-DefaultProfile</span></span>
<span data-ttu-id="8e25d-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e25d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e25d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="8e25d-127">-Location</span></span>
<span data-ttu-id="8e25d-128">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8e25d-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8e25d-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8e25d-129">-ManagementGroupId</span></span>
<span data-ttu-id="8e25d-130">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8e25d-130">The management group id.</span></span>

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

### <span data-ttu-id="8e25d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e25d-131">-Pre</span></span>
<span data-ttu-id="8e25d-132">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="8e25d-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8e25d-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8e25d-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8e25d-134">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="8e25d-135">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="8e25d-136">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="8e25d-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8e25d-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8e25d-137">-TemplateFile</span></span>
<span data-ttu-id="8e25d-138">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="8e25d-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="8e25d-139">-TemplateObject</span></span>
<span data-ttu-id="8e25d-140">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8e25d-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8e25d-141">-TemplateParameterFile</span></span>
<span data-ttu-id="8e25d-142">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8e25d-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8e25d-143">-TemplateParameterObject</span></span>
<span data-ttu-id="8e25d-144">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="8e25d-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8e25d-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8e25d-145">-TemplateParameterUri</span></span>
<span data-ttu-id="8e25d-146">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8e25d-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8e25d-147">-TemplateUri</span></span>
<span data-ttu-id="8e25d-148">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="8e25d-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="8e25d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e25d-149">CommonParameters</span></span>
<span data-ttu-id="8e25d-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e25d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e25d-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e25d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e25d-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e25d-152">INPUTS</span></span>

### <span data-ttu-id="8e25d-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e25d-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8e25d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8e25d-154">System.String</span></span>

## <span data-ttu-id="8e25d-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e25d-155">OUTPUTS</span></span>

### <span data-ttu-id="8e25d-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="8e25d-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="8e25d-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e25d-157">NOTES</span></span>

## <span data-ttu-id="8e25d-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e25d-158">RELATED LINKS</span></span>
