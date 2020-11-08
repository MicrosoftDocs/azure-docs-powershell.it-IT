---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 9a1a183ac6a0fb896f6b3d901e8f429fdf225e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200015"
---
# <span data-ttu-id="3a1b4-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3a1b4-101">Test-AzDeployment</span></span>

## <span data-ttu-id="3a1b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a1b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1b4-103">Convalida una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-103">Validates a deployment.</span></span>

## <span data-ttu-id="3a1b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a1b4-104">SYNTAX</span></span>

### <span data-ttu-id="3a1b4-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a1b4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3a1b4-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3a1b4-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3a1b4-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3a1b4-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3a1b4-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3a1b4-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b4-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1b4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b4-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1b4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a1b4-117">DESCRIPTION</span></span>
<span data-ttu-id="3a1b4-118">Il cmdlet **test-AzDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="3a1b4-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a1b4-119">EXAMPLES</span></span>

### <span data-ttu-id="3a1b4-120">Esempio 1: testare la distribuzione con un modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="3a1b4-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="3a1b4-121">Questo comando verifica una distribuzione nell'ambito dell'abbonamento corrente usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="3a1b4-122">Esempio 2: testare la distribuzione con un oggetto modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="3a1b4-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="3a1b4-123">Questo comando verifica una distribuzione nell'ambito dell'abbonamento corrente usando la tabella hash in memoria creata dal file di modello dato e un file di parametro.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="3a1b4-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a1b4-124">PARAMETERS</span></span>

### <span data-ttu-id="3a1b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-125">-DefaultProfile</span></span>
<span data-ttu-id="3a1b4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1b4-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3a1b4-127">-Location</span></span>
<span data-ttu-id="3a1b4-128">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3a1b4-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="3a1b4-129">-Pre</span></span>
<span data-ttu-id="3a1b4-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3a1b4-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3a1b4-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3a1b4-132">Ignora l'elaborazione dei parametri dinamici di PowerShell che verifica se il parametro di modello specificato contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="3a1b4-133">Questo controllo consentirà all'utente di fornire un valore per i parametri mancanti, ma specificando che-SkipTemplateParameterPrompt ignorerà questo prompt e si verificherà un errore immediatamente se non è stato trovato un parametro associato al modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="3a1b4-134">Per gli script non interattivi,-SkipTemplateParameterPrompt può essere fornito per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3a1b4-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-135">-TemplateFile</span></span>
<span data-ttu-id="3a1b4-136">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="3a1b4-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3a1b4-137">-TemplateObject</span></span>
<span data-ttu-id="3a1b4-138">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3a1b4-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3a1b4-139">-TemplateParameterFile</span></span>
<span data-ttu-id="3a1b4-140">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3a1b4-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3a1b4-141">-TemplateParameterObject</span></span>
<span data-ttu-id="3a1b4-142">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3a1b4-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3a1b4-143">-TemplateParameterUri</span></span>
<span data-ttu-id="3a1b4-144">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3a1b4-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3a1b4-145">-TemplateUri</span></span>
<span data-ttu-id="3a1b4-146">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="3a1b4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b4-147">CommonParameters</span></span>
<span data-ttu-id="3a1b4-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1b4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1b4-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a1b4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1b4-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a1b4-150">INPUTS</span></span>

### <span data-ttu-id="3a1b4-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a1b4-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3a1b4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1b4-152">System.String</span></span>

## <span data-ttu-id="3a1b4-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a1b4-153">OUTPUTS</span></span>

### <span data-ttu-id="3a1b4-154">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="3a1b4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="3a1b4-155">Note</span><span class="sxs-lookup"><span data-stu-id="3a1b4-155">NOTES</span></span>

## <span data-ttu-id="3a1b4-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a1b4-156">RELATED LINKS</span></span>