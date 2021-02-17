---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178735"
---
# <span data-ttu-id="9af8e-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="9af8e-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="9af8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9af8e-103">Convalida una distribuzione nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="9af8e-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="9af8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9af8e-104">SYNTAX</span></span>

### <span data-ttu-id="9af8e-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="9af8e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9af8e-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9af8e-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9af8e-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9af8e-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9af8e-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9af8e-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9af8e-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9af8e-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9af8e-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9af8e-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9af8e-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af8e-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9af8e-117">DESCRIPTION</span></span>
<span data-ttu-id="9af8e-118">Il cmdlet **Test-AzTenantDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi in base all'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="9af8e-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="9af8e-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9af8e-119">EXAMPLES</span></span>

### <span data-ttu-id="9af8e-120">Esempio 1: Testare la distribuzione con un modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="9af8e-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="9af8e-121">Questo comando testa una distribuzione nell'ambito tenant corrente usando il file di modello specificato e il file di parametri.</span><span class="sxs-lookup"><span data-stu-id="9af8e-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="9af8e-122">Esempio 2: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="9af8e-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="9af8e-123">Questo comando testa una distribuzione nell'ambito tenant corrente usando una tabella hash in memoria creata dal file di modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="9af8e-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="9af8e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9af8e-124">PARAMETERS</span></span>

### <span data-ttu-id="9af8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af8e-125">-DefaultProfile</span></span>
<span data-ttu-id="9af8e-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9af8e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af8e-127">-Location</span><span class="sxs-lookup"><span data-stu-id="9af8e-127">-Location</span></span>
<span data-ttu-id="9af8e-128">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9af8e-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9af8e-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="9af8e-129">-Pre</span></span>
<span data-ttu-id="9af8e-130">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9af8e-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9af8e-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9af8e-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9af8e-132">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="9af8e-133">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro per essere associato nel modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="9af8e-134">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="9af8e-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9af8e-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9af8e-135">-TemplateFile</span></span>
<span data-ttu-id="9af8e-136">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="9af8e-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9af8e-137">-TemplateObject</span></span>
<span data-ttu-id="9af8e-138">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="9af8e-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9af8e-139">-TemplateParameterFile</span></span>
<span data-ttu-id="9af8e-140">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9af8e-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9af8e-141">-TemplateParameterObject</span></span>
<span data-ttu-id="9af8e-142">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="9af8e-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9af8e-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9af8e-143">-TemplateParameterUri</span></span>
<span data-ttu-id="9af8e-144">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9af8e-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9af8e-145">-TemplateUri</span></span>
<span data-ttu-id="9af8e-146">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="9af8e-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="9af8e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af8e-147">CommonParameters</span></span>
<span data-ttu-id="9af8e-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af8e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af8e-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9af8e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af8e-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="9af8e-150">INPUTS</span></span>

### <span data-ttu-id="9af8e-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9af8e-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9af8e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9af8e-152">System.String</span></span>

## <span data-ttu-id="9af8e-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9af8e-153">OUTPUTS</span></span>

### <span data-ttu-id="9af8e-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="9af8e-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="9af8e-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="9af8e-155">NOTES</span></span>

## <span data-ttu-id="9af8e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9af8e-156">RELATED LINKS</span></span>
