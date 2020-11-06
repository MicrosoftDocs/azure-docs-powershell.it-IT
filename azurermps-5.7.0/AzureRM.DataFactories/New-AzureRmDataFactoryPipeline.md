---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dbdefb2e6fa419898447c17053f58631b35a906d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516784"
---
# <span data-ttu-id="2127f-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="2127f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2127f-102">SYNOPSIS</span></span>
<span data-ttu-id="2127f-103">Crea una pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="2127f-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2127f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2127f-104">SYNTAX</span></span>

### <span data-ttu-id="2127f-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2127f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2127f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2127f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2127f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2127f-107">DESCRIPTION</span></span>
<span data-ttu-id="2127f-108">Il cmdlet **New-AzureRmDataFactoryPipeline** crea una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2127f-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="2127f-109">Se specifichi un nome per una pipeline già esistente, il cmdlet richiede conferma prima di sostituire la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="2127f-110">Se specifichi il parametro *Force* , il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="2127f-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="2127f-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="2127f-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="2127f-112">Creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="2127f-112">Create a data factory.</span></span> 
- <span data-ttu-id="2127f-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="2127f-113">Create linked services.</span></span> 
- <span data-ttu-id="2127f-114">Creare set di DataSet.</span><span class="sxs-lookup"><span data-stu-id="2127f-114">Create datasets.</span></span> 
- <span data-ttu-id="2127f-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-115">Create a pipeline.</span></span>

<span data-ttu-id="2127f-116">Se nella data factory esiste già una pipeline con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="2127f-117">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="2127f-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2127f-118">EXAMPLES</span></span>

### <span data-ttu-id="2127f-119">Esempio 1: creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="2127f-120">Questo comando crea una pipeline denominata DPWikisample nella Factory di dati denominata ADF.</span><span class="sxs-lookup"><span data-stu-id="2127f-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="2127f-121">Il comando basa la pipeline sulle informazioni nella DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="2127f-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="2127f-122">Questo file include informazioni sulle attività, ad esempio attività di copia e attività di HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="2127f-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2127f-123">PARAMETERS</span></span>

### <span data-ttu-id="2127f-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2127f-124">-DataFactory</span></span>
<span data-ttu-id="2127f-125">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="2127f-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2127f-126">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2127f-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2127f-127">-DataFactoryName</span></span>
<span data-ttu-id="2127f-128">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="2127f-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2127f-129">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2127f-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2127f-130">-DefaultProfile</span></span>
<span data-ttu-id="2127f-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2127f-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2127f-132">-File</span><span class="sxs-lookup"><span data-stu-id="2127f-132">-File</span></span>
<span data-ttu-id="2127f-133">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127f-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-134">-Force</span><span class="sxs-lookup"><span data-stu-id="2127f-134">-Force</span></span>
<span data-ttu-id="2127f-135">Indica che questo cmdlet sostituisce una pipeline esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2127f-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2127f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="2127f-136">-Name</span></span>
<span data-ttu-id="2127f-137">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="2127f-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2127f-138">-ResourceGroupName</span></span>
<span data-ttu-id="2127f-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="2127f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2127f-140">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2127f-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2127f-141">-Confirm</span></span>
<span data-ttu-id="2127f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2127f-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2127f-143">-WhatIf</span></span>
<span data-ttu-id="2127f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2127f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2127f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2127f-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2127f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2127f-146">CommonParameters</span></span>
<span data-ttu-id="2127f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2127f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2127f-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2127f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2127f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2127f-149">INPUTS</span></span>

### <span data-ttu-id="2127f-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2127f-150">None</span></span>
<span data-ttu-id="2127f-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2127f-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2127f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2127f-152">OUTPUTS</span></span>

### <span data-ttu-id="2127f-153">Microsoft. WindowsAzure. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-153">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="2127f-154">Note</span><span class="sxs-lookup"><span data-stu-id="2127f-154">NOTES</span></span>
* <span data-ttu-id="2127f-155">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="2127f-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2127f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2127f-156">RELATED LINKS</span></span>

[<span data-ttu-id="2127f-157">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2127f-158">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2127f-159">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2127f-160">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="2127f-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="2127f-161">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2127f-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


