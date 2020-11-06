---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516079"
---
# <span data-ttu-id="a52b3-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52b3-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="a52b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a52b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a52b3-103">Convalida una distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a52b3-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a52b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a52b3-104">SYNTAX</span></span>

### <span data-ttu-id="a52b3-105">Distribuzione tramite file modello senza parametri (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a52b3-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-106">Distribuzione tramite un oggetto modello di file e parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a52b3-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-107">Distribuzione tramite URI di modello e oggetto parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a52b3-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-108">Distribuzione tramite file modello e parametri del modello</span><span class="sxs-lookup"><span data-stu-id="a52b3-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-109">Distribuzione tramite URI modello e file di parametri di modello</span><span class="sxs-lookup"><span data-stu-id="a52b3-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-110">Distribuzione tramite URI parametri modello file modello</span><span class="sxs-lookup"><span data-stu-id="a52b3-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-111">Distribuzione tramite URI di modello e parametri di modello URI</span><span class="sxs-lookup"><span data-stu-id="a52b3-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52b3-112">Distribuzione tramite URI di modello senza parametri</span><span class="sxs-lookup"><span data-stu-id="a52b3-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52b3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a52b3-113">DESCRIPTION</span></span>
<span data-ttu-id="a52b3-114">Il cmdlet **test-AzureRmResourceGroupDeployment** determina se un modello di distribuzione di Azure Resource Group e i relativi valori di parametro sono validi.</span><span class="sxs-lookup"><span data-stu-id="a52b3-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="a52b3-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a52b3-115">EXAMPLES</span></span>

## <span data-ttu-id="a52b3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a52b3-116">PARAMETERS</span></span>

### <span data-ttu-id="a52b3-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a52b3-117">-ApiVersion</span></span>
<span data-ttu-id="a52b3-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a52b3-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a52b3-119">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a52b3-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a52b3-120">-Modalità</span><span class="sxs-lookup"><span data-stu-id="a52b3-120">-Mode</span></span>
<span data-ttu-id="a52b3-121">Specifica la modalità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a52b3-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="a52b3-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a52b3-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a52b3-123">Incrementale</span><span class="sxs-lookup"><span data-stu-id="a52b3-123">Incremental</span></span>
- <span data-ttu-id="a52b3-124">Completare</span><span class="sxs-lookup"><span data-stu-id="a52b3-124">Complete</span></span>

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

### <span data-ttu-id="a52b3-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="a52b3-125">-Pre</span></span>
<span data-ttu-id="a52b3-126">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a52b3-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a52b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a52b3-128">Specifica il nome del gruppo di risorse da testare.</span><span class="sxs-lookup"><span data-stu-id="a52b3-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="a52b3-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a52b3-129">-TemplateFile</span></span>
<span data-ttu-id="a52b3-130">Specifica il percorso completo di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="a52b3-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52b3-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a52b3-131">-TemplateParameterFile</span></span>
<span data-ttu-id="a52b3-132">Specifica il percorso completo di un file JSON che contiene i nomi e i valori dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="a52b3-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52b3-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a52b3-133">-TemplateParameterObject</span></span>
<span data-ttu-id="a52b3-134">Specifica una tabella hash di nomi e valori di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="a52b3-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52b3-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a52b3-135">-TemplateParameterUri</span></span>
<span data-ttu-id="a52b3-136">Specifica l'URI di un file di parametri di modello.</span><span class="sxs-lookup"><span data-stu-id="a52b3-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52b3-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a52b3-137">-TemplateUri</span></span>
<span data-ttu-id="a52b3-138">Specifica l'URI di un file di modello JSON.</span><span class="sxs-lookup"><span data-stu-id="a52b3-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a52b3-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52b3-139">-DefaultProfile</span></span>
<span data-ttu-id="a52b3-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a52b3-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52b3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52b3-141">CommonParameters</span></span>
<span data-ttu-id="a52b3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52b3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52b3-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52b3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52b3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a52b3-144">INPUTS</span></span>

## <span data-ttu-id="a52b3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a52b3-145">OUTPUTS</span></span>

### <span data-ttu-id="a52b3-146">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="a52b3-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="a52b3-147">Note</span><span class="sxs-lookup"><span data-stu-id="a52b3-147">NOTES</span></span>

## <span data-ttu-id="a52b3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a52b3-148">RELATED LINKS</span></span>

[<span data-ttu-id="a52b3-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52b3-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a52b3-150">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52b3-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a52b3-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52b3-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a52b3-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a52b3-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


