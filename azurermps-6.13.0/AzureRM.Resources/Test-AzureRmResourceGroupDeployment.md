---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f1109e61c2ea1f8c4d2f20aec7927cc550f95249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687755"
---
# <span data-ttu-id="f6863-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f6863-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6863-102">SYNOPSIS</span></span>
<span data-ttu-id="f6863-103">Convalida una distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6863-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6863-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6863-104">SYNTAX</span></span>

### <span data-ttu-id="f6863-105">ByTemplateFileWithNoParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6863-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6863-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6863-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6863-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6863-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6863-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6863-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6863-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6863-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f6863-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6863-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6863-113">DESCRIPTION</span></span>
<span data-ttu-id="f6863-114">Il cmdlet **test-AzureRmResourceGroupDeployment** determina se un modello di distribuzione di Azure Resource Group e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="f6863-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f6863-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6863-115">EXAMPLES</span></span>

## <span data-ttu-id="f6863-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6863-116">PARAMETERS</span></span>

### <span data-ttu-id="f6863-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6863-117">-ApiVersion</span></span>
<span data-ttu-id="f6863-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6863-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f6863-119">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f6863-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f6863-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6863-120">-DefaultProfile</span></span>
<span data-ttu-id="f6863-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f6863-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-122">-Modalità</span><span class="sxs-lookup"><span data-stu-id="f6863-122">-Mode</span></span>
<span data-ttu-id="f6863-123">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f6863-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="f6863-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f6863-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6863-125">Incrementale</span><span class="sxs-lookup"><span data-stu-id="f6863-125">Incremental</span></span>
- <span data-ttu-id="f6863-126">Completare</span><span class="sxs-lookup"><span data-stu-id="f6863-126">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6863-127">-Pre</span></span>
<span data-ttu-id="f6863-128">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f6863-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6863-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6863-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6863-130">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="f6863-130">Specifies the name of the resource group to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f6863-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="f6863-132">Il rollback alla distribuzione corretta con il nome indicato nel gruppo di risorse non deve essere usato se viene usato-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="f6863-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="f6863-134">Il rollback all'ultima distribuzione corretta nel gruppo di risorse non dovrebbe essere presente se viene usato-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="f6863-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="f6863-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f6863-135">-TemplateFile</span></span>
<span data-ttu-id="f6863-136">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="f6863-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f6863-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6863-137">-TemplateParameterFile</span></span>
<span data-ttu-id="f6863-138">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="f6863-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6863-139">-TemplateParameterObject</span></span>
<span data-ttu-id="f6863-140">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="f6863-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6863-141">-TemplateParameterUri</span></span>
<span data-ttu-id="f6863-142">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="f6863-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6863-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f6863-143">-TemplateUri</span></span>
<span data-ttu-id="f6863-144">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="f6863-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f6863-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6863-145">CommonParameters</span></span>
<span data-ttu-id="f6863-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6863-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6863-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6863-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6863-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6863-148">INPUTS</span></span>

### <span data-ttu-id="f6863-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f6863-149">None</span></span>

## <span data-ttu-id="f6863-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6863-150">OUTPUTS</span></span>

### <span data-ttu-id="f6863-151">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f6863-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="f6863-152">Note</span><span class="sxs-lookup"><span data-stu-id="f6863-152">NOTES</span></span>

## <span data-ttu-id="f6863-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6863-153">RELATED LINKS</span></span>

[<span data-ttu-id="f6863-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6863-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6863-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6863-157">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6863-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


