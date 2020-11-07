---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 5e0ee389a5d2d126cfbccc2a91b1644d81a5fedf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688336"
---
# <span data-ttu-id="ddcf4-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ddcf4-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ddcf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcf4-103">Collega un archivio dati o un servizio cloud a data factory.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddcf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddcf4-104">SYNTAX</span></span>

### <span data-ttu-id="ddcf4-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddcf4-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddcf4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddcf4-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcf4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddcf4-107">DESCRIPTION</span></span>
<span data-ttu-id="ddcf4-108">Il cmdlet Set-AzureRmDataFactoryV2LinkedService collega un archivio dati o un servizio cloud a Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="ddcf4-109">Se si specifica un nome per un servizio collegato già esistente, questo cmdlet richiede conferma prima di sostituire il servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="ddcf4-110">Se specifichi il parametro Force, il cmdlet sostituisce il servizio collegato esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="ddcf4-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="ddcf4-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="ddcf4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddcf4-112">EXAMPLES</span></span>

### <span data-ttu-id="ddcf4-113">Esempio 1: creare un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="ddcf4-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ddcf4-114">Questo comando crea un servizio collegato denominato LinkedServiceCuratedWikiData nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ddcf4-115">Questo servizio collegato collega un archivio BLOB di Azure specificato nel file alla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="ddcf4-116">Il comando passa il risultato al cmdlet Format-List usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ddcf4-117">Il cmdlet di Windows PowerShell formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ddcf4-118">Per altre informazioni, digitare Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="ddcf4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddcf4-119">PARAMETERS</span></span>

### <span data-ttu-id="ddcf4-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddcf4-120">-Confirm</span></span>
<span data-ttu-id="ddcf4-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcf4-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ddcf4-122">-DataFactoryName</span></span>
<span data-ttu-id="ddcf4-123">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ddcf4-124">Questo cmdlet crea un servizio collegato per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddcf4-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ddcf4-125">-DefinitionFile</span></span>
<span data-ttu-id="ddcf4-126">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-126">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcf4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ddcf4-127">-Force</span></span>
<span data-ttu-id="ddcf4-128">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ddcf4-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddcf4-129">-Name</span></span>
<span data-ttu-id="ddcf4-130">Specifica il nome del servizio collegato da creare.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcf4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddcf4-131">-ResourceGroupName</span></span>
<span data-ttu-id="ddcf4-132">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ddcf4-133">Questo cmdlet crea un servizio collegato per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddcf4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddcf4-134">-ResourceId</span></span>
<span data-ttu-id="ddcf4-135">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-135">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcf4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcf4-136">-WhatIf</span></span>
<span data-ttu-id="ddcf4-137">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcf4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcf4-138">-DefaultProfile</span></span>
<span data-ttu-id="ddcf4-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddcf4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcf4-140">CommonParameters</span></span>
<span data-ttu-id="ddcf4-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcf4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcf4-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcf4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcf4-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddcf4-143">INPUTS</span></span>

### <span data-ttu-id="ddcf4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcf4-144">System.String</span></span>

## <span data-ttu-id="ddcf4-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddcf4-145">OUTPUTS</span></span>

### <span data-ttu-id="ddcf4-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ddcf4-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ddcf4-147">Note</span><span class="sxs-lookup"><span data-stu-id="ddcf4-147">NOTES</span></span>
<span data-ttu-id="ddcf4-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="ddcf4-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ddcf4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddcf4-149">RELATED LINKS</span></span>

[<span data-ttu-id="ddcf4-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ddcf4-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ddcf4-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ddcf4-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()