---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509908"
---
# <span data-ttu-id="a2915-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a2915-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="a2915-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2915-102">SYNOPSIS</span></span>
<span data-ttu-id="a2915-103">Imposta lo stato delle sezioni per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a2915-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2915-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2915-104">SYNTAX</span></span>

### <span data-ttu-id="a2915-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2915-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2915-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a2915-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2915-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2915-107">DESCRIPTION</span></span>
<span data-ttu-id="a2915-108">Il cmdlet **set-AzureRmDataFactorySliceStatus** imposta lo stato delle sezioni per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a2915-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="a2915-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2915-109">EXAMPLES</span></span>

### <span data-ttu-id="a2915-110">Esempio 1: impostare lo stato di tutte le sezioni</span><span class="sxs-lookup"><span data-stu-id="a2915-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="a2915-111">Questo comando imposta lo stato di tutte le sezioni per il DataSet denominato DAWikiAggregatedData in attesa nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a2915-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="a2915-112">Il parametro *UpdateType* ha un valore di UpstreamInPipeline e quindi il comando imposta lo stato di ogni sezione per DataSet e tutti i set di dati dipendenti.</span><span class="sxs-lookup"><span data-stu-id="a2915-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="a2915-113">I DataSet dipendenti vengono usati come set di dati di input per le attività della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2915-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="a2915-114">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="a2915-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="a2915-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2915-115">PARAMETERS</span></span>

### <span data-ttu-id="a2915-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a2915-116">-DataFactory</span></span>
<span data-ttu-id="a2915-117">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a2915-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a2915-118">Questo cmdlet modifica lo stato delle sezioni che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a2915-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2915-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a2915-119">-DataFactoryName</span></span>
<span data-ttu-id="a2915-120">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="a2915-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a2915-121">Questo cmdlet modifica lo stato delle sezioni che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a2915-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2915-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="a2915-122">-DatasetName</span></span>
<span data-ttu-id="a2915-123">Specifica il nome del DataSet per cui questo cmdlet modifica le sezioni.</span><span class="sxs-lookup"><span data-stu-id="a2915-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2915-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2915-124">-DefaultProfile</span></span>
<span data-ttu-id="a2915-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a2915-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2915-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="a2915-126">-EndDateTime</span></span>
<span data-ttu-id="a2915-127">Specifica la fine di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a2915-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a2915-128">Questa volta è la fine di una sezione di dati.</span><span class="sxs-lookup"><span data-stu-id="a2915-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="a2915-129">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a2915-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="a2915-130">*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2915-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="a2915-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico)</span><span class="sxs-lookup"><span data-stu-id="a2915-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="a2915-132">L'indicatore di fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="a2915-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2915-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2915-133">-ResourceGroupName</span></span>
<span data-ttu-id="a2915-134">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a2915-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a2915-135">Questo cmdlet modifica lo stato delle sezioni che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a2915-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2915-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a2915-136">-StartDateTime</span></span>
<span data-ttu-id="a2915-137">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a2915-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a2915-138">Questa volta è l'inizio di una sezione di dati.</span><span class="sxs-lookup"><span data-stu-id="a2915-138">This time is the beginning of a data slice.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2915-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="a2915-139">-Status</span></span>
<span data-ttu-id="a2915-140">Specifica uno stato da assegnare alla sezione dati.</span><span class="sxs-lookup"><span data-stu-id="a2915-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="a2915-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2915-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2915-142">In attesa.</span><span class="sxs-lookup"><span data-stu-id="a2915-142">Waiting.</span></span>
<span data-ttu-id="a2915-143">La sezione dati attende la convalida per i criteri di convalida prima dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a2915-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="a2915-144">Pronto.</span><span class="sxs-lookup"><span data-stu-id="a2915-144">Ready.</span></span>
<span data-ttu-id="a2915-145">L'elaborazione dei dati è stata completata e la sezione dati è pronta.</span><span class="sxs-lookup"><span data-stu-id="a2915-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="a2915-146">InProgress.</span><span class="sxs-lookup"><span data-stu-id="a2915-146">InProgress.</span></span>
<span data-ttu-id="a2915-147">L'elaborazione dei dati è in corso.</span><span class="sxs-lookup"><span data-stu-id="a2915-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="a2915-148">Fallito.</span><span class="sxs-lookup"><span data-stu-id="a2915-148">Failed.</span></span>
<span data-ttu-id="a2915-149">L'elaborazione dei dati non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="a2915-149">Data processing failed.</span></span>
- <span data-ttu-id="a2915-150">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="a2915-150">Skipped.</span></span>
<span data-ttu-id="a2915-151">Ignorato l'elaborazione della sezione dati.</span><span class="sxs-lookup"><span data-stu-id="a2915-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2915-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="a2915-152">-UpdateType</span></span>
<span data-ttu-id="a2915-153">Specifica il tipo di aggiornamento alla sezione.</span><span class="sxs-lookup"><span data-stu-id="a2915-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="a2915-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2915-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2915-155">Singoli.</span><span class="sxs-lookup"><span data-stu-id="a2915-155">Individual.</span></span>
<span data-ttu-id="a2915-156">Imposta lo stato di ogni sezione per il DataSet nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="a2915-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="a2915-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="a2915-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="a2915-158">Imposta lo stato di ogni sezione per il DataSet e tutti i set di dati dipendenti, che vengono usati come set di dati di input per le attività della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2915-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2915-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2915-159">CommonParameters</span></span>
<span data-ttu-id="a2915-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2915-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2915-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2915-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2915-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2915-162">INPUTS</span></span>

### <span data-ttu-id="a2915-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2915-163">None</span></span>
<span data-ttu-id="a2915-164">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a2915-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2915-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2915-165">OUTPUTS</span></span>

### <span data-ttu-id="a2915-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2915-166">System.Boolean</span></span>

## <span data-ttu-id="a2915-167">Note</span><span class="sxs-lookup"><span data-stu-id="a2915-167">NOTES</span></span>
* <span data-ttu-id="a2915-168">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="a2915-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a2915-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2915-169">RELATED LINKS</span></span>

[<span data-ttu-id="a2915-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="a2915-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


