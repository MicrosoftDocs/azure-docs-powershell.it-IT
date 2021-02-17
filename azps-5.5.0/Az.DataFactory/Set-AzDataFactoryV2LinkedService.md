---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198159"
---
# <span data-ttu-id="3ec89-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3ec89-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="3ec89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec89-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec89-103">Collega un archivio dati o un servizio cloud a Data factory.</span><span class="sxs-lookup"><span data-stu-id="3ec89-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="3ec89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ec89-104">SYNTAX</span></span>

### <span data-ttu-id="3ec89-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="3ec89-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ec89-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec89-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec89-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ec89-107">DESCRIPTION</span></span>
<span data-ttu-id="3ec89-108">Il cmdlet Set-AzDataFactoryV2LinkedService collega un archivio dati o un servizio cloud a Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec89-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="3ec89-109">Se si specifica un nome per un servizio collegato già esistente, questo cmdlet richiede conferma prima che sostituisca il servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="3ec89-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="3ec89-110">Se si specifica il parametro Force, il cmdlet sostituisce il servizio collegato esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="3ec89-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="3ec89-111">Eseguire queste operazioni nell'ordine seguente: -- Creare un data factory.</span><span class="sxs-lookup"><span data-stu-id="3ec89-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="3ec89-112">-- Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="3ec89-112">-- Create linked services.</span></span>
<span data-ttu-id="3ec89-113">-- Creare set di dati.</span><span class="sxs-lookup"><span data-stu-id="3ec89-113">-- Create datasets.</span></span>
<span data-ttu-id="3ec89-114">-- Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ec89-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="3ec89-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ec89-115">EXAMPLES</span></span>

### <span data-ttu-id="3ec89-116">Esempio 1: Creare un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="3ec89-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="3ec89-117">Questo comando crea un servizio collegato denominato LinkedServiceCuratedWikiData nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3ec89-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="3ec89-118">Questo servizio collegato collega un archivio BLOB di Azure specificato nel file al data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3ec89-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="3ec89-119">Il comando passa il risultato al cmdlet Format-List tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ec89-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ec89-120">Questo Windows PowerShell cmdlet formatta i risultati.</span><span class="sxs-lookup"><span data-stu-id="3ec89-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="3ec89-121">Per altre informazioni, digitare Get-Help-List.</span><span class="sxs-lookup"><span data-stu-id="3ec89-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="3ec89-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ec89-122">PARAMETERS</span></span>

### <span data-ttu-id="3ec89-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3ec89-123">-DataFactoryName</span></span>
<span data-ttu-id="3ec89-124">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="3ec89-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3ec89-125">Questo cmdlet crea un servizio collegato per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3ec89-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ec89-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec89-126">-DefaultProfile</span></span>
<span data-ttu-id="3ec89-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec89-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ec89-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3ec89-128">-DefinitionFile</span></span>
<span data-ttu-id="3ec89-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="3ec89-129">The JSON file path.</span></span>

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

### <span data-ttu-id="3ec89-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3ec89-130">-Force</span></span>
<span data-ttu-id="3ec89-131">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3ec89-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3ec89-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3ec89-132">-Name</span></span>
<span data-ttu-id="3ec89-133">Specifica il nome del servizio collegato da creare.</span><span class="sxs-lookup"><span data-stu-id="3ec89-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="3ec89-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec89-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ec89-135">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec89-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3ec89-136">Questo cmdlet crea un servizio collegato per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3ec89-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ec89-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec89-137">-ResourceId</span></span>
<span data-ttu-id="3ec89-138">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec89-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3ec89-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ec89-139">-Confirm</span></span>
<span data-ttu-id="3ec89-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec89-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec89-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec89-141">-WhatIf</span></span>
<span data-ttu-id="3ec89-142">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="3ec89-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3ec89-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec89-143">CommonParameters</span></span>
<span data-ttu-id="3ec89-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec89-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec89-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec89-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec89-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ec89-146">INPUTS</span></span>

### <span data-ttu-id="3ec89-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3ec89-147">System.String</span></span>

## <span data-ttu-id="3ec89-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ec89-148">OUTPUTS</span></span>

### <span data-ttu-id="3ec89-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="3ec89-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="3ec89-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ec89-150">NOTES</span></span>
<span data-ttu-id="3ec89-151">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="3ec89-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3ec89-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ec89-152">RELATED LINKS</span></span>

[<span data-ttu-id="3ec89-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3ec89-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="3ec89-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="3ec89-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
