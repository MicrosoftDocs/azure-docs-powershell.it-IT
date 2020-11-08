---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: d6222c0e1ecd6eee39b65ac65e74707d1d64ef17
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019664"
---
# <span data-ttu-id="2fe16-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2fe16-101">Test-AzDeployment</span></span>

## <span data-ttu-id="2fe16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fe16-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe16-103">Convalida una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2fe16-103">Validates a deployment.</span></span>

## <span data-ttu-id="2fe16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fe16-104">SYNTAX</span></span>

### <span data-ttu-id="2fe16-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fe16-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe16-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fe16-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fe16-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fe16-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fe16-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fe16-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fe16-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fe16-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fe16-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fe16-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe16-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2fe16-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe16-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2fe16-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe16-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fe16-117">DESCRIPTION</span></span>
<span data-ttu-id="2fe16-118">Il cmdlet **test-AzDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="2fe16-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="2fe16-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fe16-119">EXAMPLES</span></span>

### <span data-ttu-id="2fe16-120">Esempio 1: testare la distribuzione con un modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="2fe16-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="2fe16-121">Questo comando verifica una distribuzione nell'ambito dell'abbonamento corrente usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="2fe16-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="2fe16-122">Esempio 2: testare la distribuzione con un oggetto modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="2fe16-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2fe16-123">Questo comando verifica una distribuzione nell'ambito dell'abbonamento corrente usando la tabella hash in memoria creata dal file di modello dato e un file di parametro.</span><span class="sxs-lookup"><span data-stu-id="2fe16-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="2fe16-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fe16-124">PARAMETERS</span></span>

### <span data-ttu-id="2fe16-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fe16-125">-ApiVersion</span></span>
<span data-ttu-id="2fe16-126">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="2fe16-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2fe16-127">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="2fe16-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2fe16-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe16-128">-DefaultProfile</span></span>
<span data-ttu-id="2fe16-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fe16-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fe16-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2fe16-130">-Location</span></span>
<span data-ttu-id="2fe16-131">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2fe16-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2fe16-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="2fe16-132">-Pre</span></span>
<span data-ttu-id="2fe16-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2fe16-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2fe16-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2fe16-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2fe16-135">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="2fe16-136">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="2fe16-137">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="2fe16-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2fe16-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2fe16-138">-TemplateFile</span></span>
<span data-ttu-id="2fe16-139">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="2fe16-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2fe16-140">-TemplateObject</span></span>
<span data-ttu-id="2fe16-141">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2fe16-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2fe16-142">-TemplateParameterFile</span></span>
<span data-ttu-id="2fe16-143">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2fe16-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2fe16-144">-TemplateParameterObject</span></span>
<span data-ttu-id="2fe16-145">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="2fe16-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2fe16-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2fe16-146">-TemplateParameterUri</span></span>
<span data-ttu-id="2fe16-147">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2fe16-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2fe16-148">-TemplateUri</span></span>
<span data-ttu-id="2fe16-149">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="2fe16-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="2fe16-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe16-150">CommonParameters</span></span>
<span data-ttu-id="2fe16-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe16-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe16-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fe16-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe16-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fe16-153">INPUTS</span></span>

### <span data-ttu-id="2fe16-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2fe16-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2fe16-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2fe16-155">System.String</span></span>

## <span data-ttu-id="2fe16-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fe16-156">OUTPUTS</span></span>

### <span data-ttu-id="2fe16-157">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="2fe16-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="2fe16-158">Note</span><span class="sxs-lookup"><span data-stu-id="2fe16-158">NOTES</span></span>

## <span data-ttu-id="2fe16-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fe16-159">RELATED LINKS</span></span>
