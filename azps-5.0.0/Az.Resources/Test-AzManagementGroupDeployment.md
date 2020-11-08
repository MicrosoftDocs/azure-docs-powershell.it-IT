---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202619"
---
# <span data-ttu-id="57830-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="57830-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="57830-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57830-102">SYNOPSIS</span></span>
<span data-ttu-id="57830-103">Convalida una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="57830-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="57830-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57830-104">SYNTAX</span></span>

### <span data-ttu-id="57830-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57830-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57830-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="57830-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57830-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="57830-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57830-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="57830-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57830-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="57830-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="57830-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="57830-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="57830-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="57830-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="57830-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57830-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="57830-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57830-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="57830-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57830-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57830-117">DESCRIPTION</span></span>
<span data-ttu-id="57830-118">Il cmdlet **test-AzManagementGroupDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="57830-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="57830-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57830-119">EXAMPLES</span></span>

### <span data-ttu-id="57830-120">Esempio 1: testare la distribuzione con un modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="57830-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="57830-121">Questo comando verifica una distribuzione presso il gruppo di gestione "myMG" usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="57830-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="57830-122">Esempio 2: testare la distribuzione con un oggetto modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="57830-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="57830-123">Questo comando verifica una distribuzione presso il gruppo di gestione "myMG" usando la tabella hash in memoria creata dal file di modello e un file di parametro.</span><span class="sxs-lookup"><span data-stu-id="57830-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="57830-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57830-124">PARAMETERS</span></span>

### <span data-ttu-id="57830-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57830-125">-DefaultProfile</span></span>
<span data-ttu-id="57830-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57830-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57830-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="57830-127">-Location</span></span>
<span data-ttu-id="57830-128">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="57830-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="57830-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="57830-129">-ManagementGroupId</span></span>
<span data-ttu-id="57830-130">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="57830-130">The management group id.</span></span>

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

### <span data-ttu-id="57830-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="57830-131">-Pre</span></span>
<span data-ttu-id="57830-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="57830-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="57830-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="57830-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="57830-134">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="57830-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="57830-135">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="57830-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="57830-136">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="57830-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="57830-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="57830-137">-TemplateFile</span></span>
<span data-ttu-id="57830-138">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="57830-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="57830-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="57830-139">-TemplateObject</span></span>
<span data-ttu-id="57830-140">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="57830-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="57830-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="57830-141">-TemplateParameterFile</span></span>
<span data-ttu-id="57830-142">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="57830-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="57830-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="57830-143">-TemplateParameterObject</span></span>
<span data-ttu-id="57830-144">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="57830-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="57830-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="57830-145">-TemplateParameterUri</span></span>
<span data-ttu-id="57830-146">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="57830-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="57830-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="57830-147">-TemplateUri</span></span>
<span data-ttu-id="57830-148">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="57830-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="57830-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57830-149">CommonParameters</span></span>
<span data-ttu-id="57830-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57830-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57830-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57830-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57830-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57830-152">INPUTS</span></span>

### <span data-ttu-id="57830-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57830-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="57830-154">System. String</span><span class="sxs-lookup"><span data-stu-id="57830-154">System.String</span></span>

## <span data-ttu-id="57830-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57830-155">OUTPUTS</span></span>

### <span data-ttu-id="57830-156">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="57830-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="57830-157">Note</span><span class="sxs-lookup"><span data-stu-id="57830-157">NOTES</span></span>

## <span data-ttu-id="57830-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57830-158">RELATED LINKS</span></span>
