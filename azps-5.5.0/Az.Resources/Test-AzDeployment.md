---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 9a1a183ac6a0fb896f6b3d901e8f429fdf225e26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178751"
---
# <span data-ttu-id="95f82-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="95f82-101">Test-AzDeployment</span></span>

## <span data-ttu-id="95f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f82-102">SYNOPSIS</span></span>
<span data-ttu-id="95f82-103">Convalida una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95f82-103">Validates a deployment.</span></span>

## <span data-ttu-id="95f82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95f82-104">SYNTAX</span></span>

### <span data-ttu-id="95f82-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="95f82-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95f82-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95f82-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="95f82-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95f82-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95f82-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="95f82-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95f82-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95f82-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="95f82-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="95f82-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f82-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="95f82-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f82-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="95f82-117">DESCRIPTION</span></span>
<span data-ttu-id="95f82-118">Il **cmdlet Test-AzDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="95f82-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="95f82-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95f82-119">EXAMPLES</span></span>

### <span data-ttu-id="95f82-120">Esempio 1: Testare la distribuzione con un modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="95f82-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="95f82-121">Questo comando testa una distribuzione nell'ambito della sottoscrizione corrente usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="95f82-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="95f82-122">Esempio 2: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="95f82-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="95f82-123">Questo comando verifica una distribuzione nell'ambito della sottoscrizione corrente usando una tabella hash in memoria creata dal file di modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="95f82-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="95f82-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95f82-124">PARAMETERS</span></span>

### <span data-ttu-id="95f82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f82-125">-DefaultProfile</span></span>
<span data-ttu-id="95f82-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95f82-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f82-127">-Location</span><span class="sxs-lookup"><span data-stu-id="95f82-127">-Location</span></span>
<span data-ttu-id="95f82-128">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95f82-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="95f82-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="95f82-129">-Pre</span></span>
<span data-ttu-id="95f82-130">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="95f82-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="95f82-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="95f82-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="95f82-132">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="95f82-133">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="95f82-134">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="95f82-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="95f82-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="95f82-135">-TemplateFile</span></span>
<span data-ttu-id="95f82-136">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="95f82-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="95f82-137">-TemplateObject</span></span>
<span data-ttu-id="95f82-138">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="95f82-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="95f82-139">-TemplateParameterFile</span></span>
<span data-ttu-id="95f82-140">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="95f82-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="95f82-141">-TemplateParameterObject</span></span>
<span data-ttu-id="95f82-142">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="95f82-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="95f82-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="95f82-143">-TemplateParameterUri</span></span>
<span data-ttu-id="95f82-144">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="95f82-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="95f82-145">-TemplateUri</span></span>
<span data-ttu-id="95f82-146">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="95f82-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="95f82-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f82-147">CommonParameters</span></span>
<span data-ttu-id="95f82-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f82-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f82-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95f82-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f82-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="95f82-150">INPUTS</span></span>

### <span data-ttu-id="95f82-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95f82-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95f82-152">System.String</span><span class="sxs-lookup"><span data-stu-id="95f82-152">System.String</span></span>

## <span data-ttu-id="95f82-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95f82-153">OUTPUTS</span></span>

### <span data-ttu-id="95f82-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="95f82-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="95f82-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="95f82-155">NOTES</span></span>

## <span data-ttu-id="95f82-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95f82-156">RELATED LINKS</span></span>
