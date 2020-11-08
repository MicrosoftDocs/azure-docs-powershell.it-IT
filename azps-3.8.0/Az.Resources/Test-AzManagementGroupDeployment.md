---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019662"
---
# <span data-ttu-id="67ebc-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67ebc-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="67ebc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="67ebc-103">Convalida una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="67ebc-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="67ebc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67ebc-104">SYNTAX</span></span>

### <span data-ttu-id="67ebc-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67ebc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ebc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67ebc-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67ebc-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67ebc-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67ebc-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67ebc-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67ebc-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67ebc-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67ebc-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67ebc-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ebc-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="67ebc-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ebc-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="67ebc-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67ebc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67ebc-117">DESCRIPTION</span></span>
<span data-ttu-id="67ebc-118">Il cmdlet **test-AzManagementGroupDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="67ebc-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="67ebc-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67ebc-119">EXAMPLES</span></span>

### <span data-ttu-id="67ebc-120">Esempio 1: testare la distribuzione con un modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="67ebc-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="67ebc-121">Questo comando verifica una distribuzione presso il gruppo di gestione "myMG" usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="67ebc-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="67ebc-122">Esempio 2: testare la distribuzione con un oggetto modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="67ebc-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="67ebc-123">Questo comando verifica una distribuzione presso il gruppo di gestione "myMG" usando la tabella hash in memoria creata dal file di modello e un file di parametro.</span><span class="sxs-lookup"><span data-stu-id="67ebc-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="67ebc-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67ebc-124">PARAMETERS</span></span>

### <span data-ttu-id="67ebc-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67ebc-125">-ApiVersion</span></span>
<span data-ttu-id="67ebc-126">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="67ebc-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="67ebc-127">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="67ebc-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ebc-128">-DefaultProfile</span></span>
<span data-ttu-id="67ebc-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67ebc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="67ebc-130">-Location</span></span>
<span data-ttu-id="67ebc-131">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="67ebc-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="67ebc-132">-ManagementGroupId</span></span>
<span data-ttu-id="67ebc-133">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="67ebc-133">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="67ebc-134">-Pre</span></span>
<span data-ttu-id="67ebc-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="67ebc-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="67ebc-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="67ebc-137">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="67ebc-138">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="67ebc-139">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="67ebc-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="67ebc-140">-TemplateFile</span></span>
<span data-ttu-id="67ebc-141">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-141">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-142">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="67ebc-142">-TemplateObject</span></span>
<span data-ttu-id="67ebc-143">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-143">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="67ebc-144">-TemplateParameterFile</span></span>
<span data-ttu-id="67ebc-145">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-145">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="67ebc-146">-TemplateParameterObject</span></span>
<span data-ttu-id="67ebc-147">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="67ebc-147">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="67ebc-148">-TemplateParameterUri</span></span>
<span data-ttu-id="67ebc-149">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-149">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="67ebc-150">-TemplateUri</span></span>
<span data-ttu-id="67ebc-151">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="67ebc-151">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ebc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ebc-152">CommonParameters</span></span>
<span data-ttu-id="67ebc-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ebc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ebc-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67ebc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ebc-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67ebc-155">INPUTS</span></span>

### <span data-ttu-id="67ebc-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="67ebc-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="67ebc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="67ebc-157">System.String</span></span>

## <span data-ttu-id="67ebc-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67ebc-158">OUTPUTS</span></span>

### <span data-ttu-id="67ebc-159">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="67ebc-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="67ebc-160">Note</span><span class="sxs-lookup"><span data-stu-id="67ebc-160">NOTES</span></span>

## <span data-ttu-id="67ebc-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67ebc-161">RELATED LINKS</span></span>
