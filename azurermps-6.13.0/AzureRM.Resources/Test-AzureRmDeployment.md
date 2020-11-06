---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
ms.openlocfilehash: fdfef01f9ba8013b25db227c0833a7add408c490
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513479"
---
# <span data-ttu-id="19ba9-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="19ba9-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="19ba9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="19ba9-103">Convalida una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="19ba9-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19ba9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19ba9-104">SYNTAX</span></span>

### <span data-ttu-id="19ba9-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19ba9-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="19ba9-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="19ba9-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="19ba9-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="19ba9-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="19ba9-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="19ba9-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19ba9-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="19ba9-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19ba9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19ba9-113">DESCRIPTION</span></span>
<span data-ttu-id="19ba9-114">Il cmdlet **test-AzureRmDeployment** determina se un modello di distribuzione e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="19ba9-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="19ba9-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19ba9-115">EXAMPLES</span></span>

### <span data-ttu-id="19ba9-116">Esempio 1: testare la distribuzione con un modello e un file di parametro personalizzati</span><span class="sxs-lookup"><span data-stu-id="19ba9-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="19ba9-117">Questo comando verifica una distribuzione nell'ambito dell'abbonamento corrente usando il file di modello e il file di parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="19ba9-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="19ba9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19ba9-118">PARAMETERS</span></span>

### <span data-ttu-id="19ba9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19ba9-119">-ApiVersion</span></span>
<span data-ttu-id="19ba9-120">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="19ba9-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="19ba9-121">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="19ba9-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="19ba9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ba9-122">-DefaultProfile</span></span>
<span data-ttu-id="19ba9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19ba9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ba9-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="19ba9-124">-Location</span></span>
<span data-ttu-id="19ba9-125">Posizione in cui archiviare i dati di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="19ba9-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="19ba9-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="19ba9-126">-Pre</span></span>
<span data-ttu-id="19ba9-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="19ba9-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="19ba9-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="19ba9-128">-TemplateFile</span></span>
<span data-ttu-id="19ba9-129">Percorso locale del file di modello.</span><span class="sxs-lookup"><span data-stu-id="19ba9-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="19ba9-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="19ba9-130">-TemplateParameterFile</span></span>
<span data-ttu-id="19ba9-131">Un file con i parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="19ba9-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="19ba9-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="19ba9-132">-TemplateParameterObject</span></span>
<span data-ttu-id="19ba9-133">Tabella hash che rappresenta i parametri.</span><span class="sxs-lookup"><span data-stu-id="19ba9-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="19ba9-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="19ba9-134">-TemplateParameterUri</span></span>
<span data-ttu-id="19ba9-135">URI per il file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="19ba9-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="19ba9-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="19ba9-136">-TemplateUri</span></span>
<span data-ttu-id="19ba9-137">URI nel file del modello.</span><span class="sxs-lookup"><span data-stu-id="19ba9-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="19ba9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ba9-138">CommonParameters</span></span>
<span data-ttu-id="19ba9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ba9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ba9-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ba9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ba9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19ba9-141">INPUTS</span></span>

### <span data-ttu-id="19ba9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="19ba9-142">System.String</span></span>
<span data-ttu-id="19ba9-143">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19ba9-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="19ba9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19ba9-144">OUTPUTS</span></span>

### <span data-ttu-id="19ba9-145">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="19ba9-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="19ba9-146">Note</span><span class="sxs-lookup"><span data-stu-id="19ba9-146">NOTES</span></span>

## <span data-ttu-id="19ba9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19ba9-147">RELATED LINKS</span></span>
