---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 87b911f480e5bd3186b956f5d9529afbef1e4582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866629"
---
# <span data-ttu-id="257b5-101">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="257b5-101">New-AzureRmDeployment</span></span>

## <span data-ttu-id="257b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="257b5-102">SYNOPSIS</span></span>
<span data-ttu-id="257b5-103">Creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="257b5-103">Creat a deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="257b5-104">SYNTAX</span></span>

### <span data-ttu-id="257b5-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="257b5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="257b5-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="257b5-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="257b5-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="257b5-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="257b5-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="257b5-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257b5-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="257b5-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257b5-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="257b5-113">DESCRIPTION</span></span>
<span data-ttu-id="257b5-114">Il cmdlet **New-AzureRmDeployment** aggiunge una distribuzione nell'ambito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="257b5-114">The **New-AzureRmDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="257b5-115">Sono incluse le risorse necessarie per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="257b5-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="257b5-116">Una risorsa Azure è un'entità Azure gestita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="257b5-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="257b5-117">Una risorsa può essere attiva in un gruppo di risorse, ad esempio database server, database, sito Web, macchina virtuale o account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="257b5-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="257b5-118">In alternativa, può essere una risorsa a livello di abbonamento, come la definizione dei ruoli, la definizione dei criteri e così via.</span><span class="sxs-lookup"><span data-stu-id="257b5-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="257b5-119">Per aggiungere risorse a un gruppo di risorse, usare il **nuovo AzureRmDeployment** che crea una distribuzione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="257b5-119">To add resources to a resource group, use the **New-AzureRmDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="257b5-120">Il cmdlet **New-AzureRmDeployment** crea una distribuzione nell'ambito dell'abbonamento corrente, che distribuisce le risorse a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="257b5-120">The **New-AzureRmDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="257b5-121">Per aggiungere una distribuzione in abbonamento, specificare la posizione e un modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="257b5-122">La posizione indica a Azure Resource Manager dove archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="257b5-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="257b5-123">Il modello è una stringa JSON che contiene singole risorse da distribuire.</span><span class="sxs-lookup"><span data-stu-id="257b5-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="257b5-124">Il modello include i segnaposto dei parametri per le risorse necessarie e i valori delle proprietà configurabili, ad esempio nomi e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="257b5-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="257b5-125">Per usare un modello personalizzato per la distribuzione, specifica il parametro *TemplateFile* o il parametro *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="257b5-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="257b5-126">Ogni modello include parametri per le proprietà configurabili.</span><span class="sxs-lookup"><span data-stu-id="257b5-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="257b5-127">Per specificare i valori per i parametri del modello, specifica il parametro *TemplateParameterFile* o il parametro *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="257b5-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="257b5-128">In alternativa, è possibile usare i parametri del modello che vengono aggiunti dinamicamente al comando quando si specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="257b5-129">Per usare i parametri dinamici, digitarli al prompt dei comandi oppure digitare un segno meno (-) per indicare un parametro e usare il tasto TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="257b5-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="257b5-130">I valori dei parametri del modello immessi al prompt dei comandi hanno la precedenza sui valori in un oggetto o un file di parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="257b5-131">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="257b5-131">EXAMPLES</span></span>

### <span data-ttu-id="257b5-132">Esempio 1: usare un modello e un file di parametro personalizzati per creare una distribuzione</span><span class="sxs-lookup"><span data-stu-id="257b5-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="257b5-133">Questo comando crea una nuova distribuzione nell'ambito dell'abbonamento corrente usando un modello personalizzato e un file modello su disco.</span><span class="sxs-lookup"><span data-stu-id="257b5-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="257b5-134">Il comando usa il parametro *TemplateFile* per specificare il modello e il parametro *TemplateParameterFile* per specificare un file che contiene parametri e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="257b5-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="257b5-135">Usa il parametro *TemplateVersion* per specificare la versione del modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="257b5-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="257b5-136">PARAMETERS</span></span>

### <span data-ttu-id="257b5-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="257b5-137">-ApiVersion</span></span>
<span data-ttu-id="257b5-138">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="257b5-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="257b5-139">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="257b5-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="257b5-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="257b5-140">-AsJob</span></span>
<span data-ttu-id="257b5-141">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="257b5-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="257b5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257b5-142">-DefaultProfile</span></span>
<span data-ttu-id="257b5-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="257b5-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="257b5-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="257b5-145">Livello del log di debug della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="257b5-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="257b5-146">-Posizione</span><span class="sxs-lookup"><span data-stu-id="257b5-146">-Location</span></span>
<span data-ttu-id="257b5-147">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="257b5-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="257b5-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="257b5-148">-Name</span></span>
<span data-ttu-id="257b5-149">Nome della distribuzione che verrà creata.</span><span class="sxs-lookup"><span data-stu-id="257b5-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="257b5-150">Valido solo quando viene usato un modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-150">Only valid when a template is used.</span></span>
<span data-ttu-id="257b5-151">Quando viene usato un modello, se l'utente non specifica un nome di distribuzione, usa l'ora corrente, ad esempio "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="257b5-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="257b5-152">-Pre</span></span>
<span data-ttu-id="257b5-153">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="257b5-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="257b5-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="257b5-154">-TemplateFile</span></span>
<span data-ttu-id="257b5-155">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="257b5-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="257b5-156">-TemplateParameterFile</span></span>
<span data-ttu-id="257b5-157">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-157">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="257b5-158">-TemplateParameterObject</span></span>
<span data-ttu-id="257b5-159">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="257b5-159">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="257b5-160">-TemplateParameterUri</span></span>
<span data-ttu-id="257b5-161">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-161">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="257b5-162">-TemplateUri</span></span>
<span data-ttu-id="257b5-163">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="257b5-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="257b5-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="257b5-164">-Confirm</span></span>
<span data-ttu-id="257b5-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="257b5-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257b5-166">-WhatIf</span></span>
<span data-ttu-id="257b5-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="257b5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257b5-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="257b5-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257b5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257b5-169">CommonParameters</span></span>
<span data-ttu-id="257b5-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257b5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257b5-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257b5-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257b5-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="257b5-172">INPUTS</span></span>

### <span data-ttu-id="257b5-173">System. String</span><span class="sxs-lookup"><span data-stu-id="257b5-173">System.String</span></span>
<span data-ttu-id="257b5-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="257b5-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="257b5-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="257b5-175">OUTPUTS</span></span>

### <span data-ttu-id="257b5-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="257b5-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="257b5-177">Note</span><span class="sxs-lookup"><span data-stu-id="257b5-177">NOTES</span></span>

## <span data-ttu-id="257b5-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="257b5-178">RELATED LINKS</span></span>
