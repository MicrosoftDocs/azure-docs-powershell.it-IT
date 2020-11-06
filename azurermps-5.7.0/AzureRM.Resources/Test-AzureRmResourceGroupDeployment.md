---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520387"
---
# <span data-ttu-id="0cffc-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0cffc-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="0cffc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cffc-102">SYNOPSIS</span></span>
<span data-ttu-id="0cffc-103">Convalida una distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0cffc-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cffc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cffc-104">SYNTAX</span></span>

### <span data-ttu-id="0cffc-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0cffc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0cffc-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0cffc-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0cffc-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0cffc-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0cffc-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0cffc-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cffc-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0cffc-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cffc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cffc-113">DESCRIPTION</span></span>
<span data-ttu-id="0cffc-114">Il cmdlet **test-AzureRmResourceGroupDeployment** determina se un modello di distribuzione di Azure Resource Group e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="0cffc-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="0cffc-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cffc-115">EXAMPLES</span></span>

## <span data-ttu-id="0cffc-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cffc-116">PARAMETERS</span></span>

### <span data-ttu-id="0cffc-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0cffc-117">-ApiVersion</span></span>
<span data-ttu-id="0cffc-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="0cffc-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0cffc-119">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0cffc-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0cffc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cffc-120">-DefaultProfile</span></span>
<span data-ttu-id="0cffc-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0cffc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cffc-122">-Modalità</span><span class="sxs-lookup"><span data-stu-id="0cffc-122">-Mode</span></span>
<span data-ttu-id="0cffc-123">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0cffc-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="0cffc-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cffc-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cffc-125">Incrementale</span><span class="sxs-lookup"><span data-stu-id="0cffc-125">Incremental</span></span>
- <span data-ttu-id="0cffc-126">Completare</span><span class="sxs-lookup"><span data-stu-id="0cffc-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cffc-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="0cffc-127">-Pre</span></span>
<span data-ttu-id="0cffc-128">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0cffc-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0cffc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cffc-129">-ResourceGroupName</span></span>
<span data-ttu-id="0cffc-130">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="0cffc-130">Specifies the name of the resource group to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cffc-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0cffc-131">-TemplateFile</span></span>
<span data-ttu-id="0cffc-132">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="0cffc-132">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="0cffc-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0cffc-133">-TemplateParameterFile</span></span>
<span data-ttu-id="0cffc-134">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="0cffc-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="0cffc-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0cffc-135">-TemplateParameterObject</span></span>
<span data-ttu-id="0cffc-136">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="0cffc-136">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="0cffc-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0cffc-137">-TemplateParameterUri</span></span>
<span data-ttu-id="0cffc-138">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="0cffc-138">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0cffc-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0cffc-139">-TemplateUri</span></span>
<span data-ttu-id="0cffc-140">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="0cffc-140">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="0cffc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cffc-141">CommonParameters</span></span>
<span data-ttu-id="0cffc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cffc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cffc-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cffc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cffc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cffc-144">INPUTS</span></span>

### <span data-ttu-id="0cffc-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0cffc-145">None</span></span>
<span data-ttu-id="0cffc-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0cffc-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0cffc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cffc-147">OUTPUTS</span></span>

### <span data-ttu-id="0cffc-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="0cffc-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="0cffc-149">Note</span><span class="sxs-lookup"><span data-stu-id="0cffc-149">NOTES</span></span>

## <span data-ttu-id="0cffc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cffc-150">RELATED LINKS</span></span>

[<span data-ttu-id="0cffc-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0cffc-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0cffc-152">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0cffc-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0cffc-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0cffc-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0cffc-154">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0cffc-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


