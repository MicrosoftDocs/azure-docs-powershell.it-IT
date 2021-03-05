---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960109"
---
# <span data-ttu-id="6793c-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6793c-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="6793c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6793c-102">SYNOPSIS</span></span>
<span data-ttu-id="6793c-103">Convalida una distribuzione nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="6793c-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="6793c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6793c-104">SYNTAX</span></span>

### <span data-ttu-id="6793c-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="6793c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6793c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6793c-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6793c-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6793c-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6793c-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6793c-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6793c-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="6793c-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6793c-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6793c-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6793c-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="6793c-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6793c-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6793c-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6793c-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6793c-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6793c-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="6793c-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6793c-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6793c-120">DESCRIPTION</span></span>
<span data-ttu-id="6793c-121">Il cmdlet **Test-AzTenantDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi in base all'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="6793c-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="6793c-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6793c-122">EXAMPLES</span></span>

### <span data-ttu-id="6793c-123">Esempio 1: Testare la distribuzione con un modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="6793c-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="6793c-124">Questo comando testa una distribuzione nell'ambito tenant corrente usando il file di modello specificato e il file di parametri.</span><span class="sxs-lookup"><span data-stu-id="6793c-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="6793c-125">Esempio 2: Testare la distribuzione con un oggetto modello personalizzato e un file di parametri</span><span class="sxs-lookup"><span data-stu-id="6793c-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="6793c-126">Questo comando testa una distribuzione nell'ambito tenant corrente usando una tabella hash in memoria creata dal file di modello specificato e un file di parametri.</span><span class="sxs-lookup"><span data-stu-id="6793c-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="6793c-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6793c-127">PARAMETERS</span></span>

### <span data-ttu-id="6793c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6793c-128">-DefaultProfile</span></span>
<span data-ttu-id="6793c-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6793c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6793c-130">-Location</span><span class="sxs-lookup"><span data-stu-id="6793c-130">-Location</span></span>
<span data-ttu-id="6793c-131">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6793c-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="6793c-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="6793c-132">-Pre</span></span>
<span data-ttu-id="6793c-133">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6793c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6793c-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="6793c-134">-QueryString</span></span>
<span data-ttu-id="6793c-135">Stringa di query, ad esempio un token di firma di accesso condiviso, da usare con il parametro TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="6793c-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="6793c-136">Da usare nel caso di modelli collegati</span><span class="sxs-lookup"><span data-stu-id="6793c-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="6793c-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="6793c-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="6793c-138">Ignora l'elaborazione dinamica dei parametri di PowerShell che controlla se il parametro del modello fornito contiene tutti i parametri necessari usati dal modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="6793c-139">Questo controllo richiedeva all'utente di fornire un valore per i parametri mancanti, ma fornendo -SkipTemplateParameterPrompt ignorerà questo prompt ed errore immediatamente se non è stato trovato un parametro da associazione nel modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="6793c-140">Per gli script non interattivi, è possibile fornire -SkipTemplateParameterPrompt per fornire un messaggio di errore migliore nel caso in cui non siano soddisfatti tutti i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="6793c-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="6793c-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6793c-141">-TemplateFile</span></span>
<span data-ttu-id="6793c-142">Percorso locale del file modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-142">Local path to the template file.</span></span> <span data-ttu-id="6793c-143">Tipo di file di modello supportati: json e bicipite.</span><span class="sxs-lookup"><span data-stu-id="6793c-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="6793c-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="6793c-144">-TemplateObject</span></span>
<span data-ttu-id="6793c-145">Tabella hash che rappresenta il modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="6793c-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6793c-146">-TemplateParameterFile</span></span>
<span data-ttu-id="6793c-147">File con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="6793c-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6793c-148">-TemplateParameterObject</span></span>
<span data-ttu-id="6793c-149">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="6793c-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="6793c-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6793c-150">-TemplateParameterUri</span></span>
<span data-ttu-id="6793c-151">URI nel file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="6793c-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="6793c-152">-TemplateSpecId</span></span>
<span data-ttu-id="6793c-153">ID risorsa del valore templateSpec da distribuire.</span><span class="sxs-lookup"><span data-stu-id="6793c-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="6793c-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6793c-154">-TemplateUri</span></span>
<span data-ttu-id="6793c-155">URI del file modello.</span><span class="sxs-lookup"><span data-stu-id="6793c-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="6793c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6793c-156">CommonParameters</span></span>
<span data-ttu-id="6793c-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6793c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6793c-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6793c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6793c-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="6793c-159">INPUTS</span></span>

### <span data-ttu-id="6793c-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6793c-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6793c-161">System.String</span><span class="sxs-lookup"><span data-stu-id="6793c-161">System.String</span></span>

## <span data-ttu-id="6793c-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6793c-162">OUTPUTS</span></span>

### <span data-ttu-id="6793c-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="6793c-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="6793c-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="6793c-164">NOTES</span></span>

## <span data-ttu-id="6793c-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6793c-165">RELATED LINKS</span></span>
