---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190276"
---
# <span data-ttu-id="edb67-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="edb67-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="edb67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edb67-102">SYNOPSIS</span></span>
<span data-ttu-id="edb67-103">Collega un archivio dati o un servizio cloud a una factory di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="edb67-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="edb67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edb67-104">SYNTAX</span></span>

### <span data-ttu-id="edb67-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="edb67-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb67-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="edb67-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb67-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edb67-107">DESCRIPTION</span></span>
<span data-ttu-id="edb67-108">Il cmdlet **New-AzDataFactoryLinkedService** collega un archivio dati o un servizio cloud a Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="edb67-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="edb67-109">Se si specifica un nome per un servizio collegato già esistente, questo cmdlet richiede conferma prima di sostituire il servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="edb67-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="edb67-110">Se specifichi il parametro *Force* , il cmdlet sostituisce il servizio collegato esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="edb67-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="edb67-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="edb67-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="edb67-112">Creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="edb67-112">Create a data factory.</span></span> 
- <span data-ttu-id="edb67-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="edb67-113">Create linked services.</span></span> 
- <span data-ttu-id="edb67-114">Creare set di DataSet.</span><span class="sxs-lookup"><span data-stu-id="edb67-114">Create datasets.</span></span> 
- <span data-ttu-id="edb67-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="edb67-115">Create a pipeline.</span></span>

## <span data-ttu-id="edb67-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edb67-116">EXAMPLES</span></span>

### <span data-ttu-id="edb67-117">Esempio 1: creare un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="edb67-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="edb67-118">Questo comando crea un servizio collegato denominato LinkedServiceCuratedWikiData nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="edb67-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="edb67-119">Questo servizio collegato collega un archivio BLOB di Azure specificato nel file alla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="edb67-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="edb67-120">Il comando passa il risultato al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="edb67-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="edb67-121">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="edb67-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="edb67-122">Per altre informazioni, digitare `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="edb67-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="edb67-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edb67-123">PARAMETERS</span></span>

### <span data-ttu-id="edb67-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="edb67-124">-DataFactory</span></span>
<span data-ttu-id="edb67-125">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="edb67-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="edb67-126">Questo cmdlet crea un servizio collegato per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="edb67-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="edb67-127">-DataFactoryName</span></span>
<span data-ttu-id="edb67-128">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="edb67-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="edb67-129">Questo cmdlet crea un servizio collegato per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="edb67-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb67-130">-DefaultProfile</span></span>
<span data-ttu-id="edb67-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="edb67-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edb67-132">-File</span><span class="sxs-lookup"><span data-stu-id="edb67-132">-File</span></span>
<span data-ttu-id="edb67-133">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="edb67-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-134">-Force</span><span class="sxs-lookup"><span data-stu-id="edb67-134">-Force</span></span>
<span data-ttu-id="edb67-135">Indica che questo cmdlet sostituisce un servizio collegato esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="edb67-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="edb67-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="edb67-136">-Name</span></span>
<span data-ttu-id="edb67-137">Specifica il nome del servizio collegato da creare.</span><span class="sxs-lookup"><span data-stu-id="edb67-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb67-138">-ResourceGroupName</span></span>
<span data-ttu-id="edb67-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="edb67-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="edb67-140">Questo cmdlet crea un servizio collegato per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="edb67-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="edb67-141">-Confirm</span></span>
<span data-ttu-id="edb67-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb67-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb67-143">-WhatIf</span></span>
<span data-ttu-id="edb67-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edb67-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb67-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edb67-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb67-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb67-146">CommonParameters</span></span>
<span data-ttu-id="edb67-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb67-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb67-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb67-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb67-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edb67-149">INPUTS</span></span>

### <span data-ttu-id="edb67-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="edb67-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="edb67-151">System. String</span><span class="sxs-lookup"><span data-stu-id="edb67-151">System.String</span></span>

## <span data-ttu-id="edb67-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edb67-152">OUTPUTS</span></span>

### <span data-ttu-id="edb67-153">Microsoft. Azure. Commands. datafactories. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="edb67-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="edb67-154">Note</span><span class="sxs-lookup"><span data-stu-id="edb67-154">NOTES</span></span>
* <span data-ttu-id="edb67-155">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="edb67-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="edb67-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edb67-156">RELATED LINKS</span></span>

[<span data-ttu-id="edb67-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="edb67-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="edb67-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="edb67-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


