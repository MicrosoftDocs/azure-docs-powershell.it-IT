---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998506"
---
# <span data-ttu-id="163dd-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="163dd-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="163dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="163dd-102">SYNOPSIS</span></span>
<span data-ttu-id="163dd-103">Imposta lo stato delle sezioni per un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="163dd-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="163dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="163dd-104">SYNTAX</span></span>

### <span data-ttu-id="163dd-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="163dd-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="163dd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="163dd-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="163dd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="163dd-107">DESCRIPTION</span></span>
<span data-ttu-id="163dd-108">Il cmdlet **Set-AzDataFactorySliceStatus** imposta lo stato delle sezioni per un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="163dd-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="163dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="163dd-109">EXAMPLES</span></span>

### <span data-ttu-id="163dd-110">Esempio 1: Impostare lo stato di tutte le sezioni</span><span class="sxs-lookup"><span data-stu-id="163dd-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="163dd-111">Questo comando imposta lo stato di tutte le sezioni per il set di dati denominato DAWikiAggregatedData su In attesa nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="163dd-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="163dd-112">Il *parametro UpdateType* ha il valore UpstreamInPipeline, quindi il comando imposta lo stato di ogni sezione per il set di dati e per tutti i set di dati dipendenti.</span><span class="sxs-lookup"><span data-stu-id="163dd-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="163dd-113">I set di dati dipendenti vengono usati come set di dati di input per le attività nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="163dd-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="163dd-114">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="163dd-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="163dd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="163dd-115">PARAMETERS</span></span>

### <span data-ttu-id="163dd-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="163dd-116">-DataFactory</span></span>
<span data-ttu-id="163dd-117">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="163dd-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="163dd-118">Questo cmdlet modifica lo stato delle sezioni che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="163dd-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="163dd-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="163dd-119">-DataFactoryName</span></span>
<span data-ttu-id="163dd-120">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="163dd-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="163dd-121">Questo cmdlet modifica lo stato delle sezioni che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="163dd-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="163dd-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="163dd-122">-DatasetName</span></span>
<span data-ttu-id="163dd-123">Specifica il nome del set di dati per cui il cmdlet modifica le sezioni.</span><span class="sxs-lookup"><span data-stu-id="163dd-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163dd-124">-DefaultProfile</span></span>
<span data-ttu-id="163dd-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="163dd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="163dd-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="163dd-126">-EndDateTime</span></span>
<span data-ttu-id="163dd-127">Specifica la fine di un periodo di tempo come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="163dd-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="163dd-128">Questa volta è la fine di una sezione di dati.</span><span class="sxs-lookup"><span data-stu-id="163dd-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="163dd-129">Per altre informazioni sugli **oggetti DateTime,** digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="163dd-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="163dd-130">*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (ora standard del Pacifico) Il fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="163dd-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="163dd-132">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="163dd-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="163dd-133">Questo cmdlet modifica lo stato delle sezioni appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="163dd-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="163dd-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="163dd-134">-StartDateTime</span></span>
<span data-ttu-id="163dd-135">Specifica l'inizio di un periodo di tempo come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="163dd-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="163dd-136">Questa volta è l'inizio di una sezione di dati.</span><span class="sxs-lookup"><span data-stu-id="163dd-136">This time is the beginning of a data slice.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163dd-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="163dd-137">-Status</span></span>
<span data-ttu-id="163dd-138">Specifica lo stato da assegnare alla sezione dati.</span><span class="sxs-lookup"><span data-stu-id="163dd-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="163dd-139">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="163dd-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="163dd-140">In attesa.</span><span class="sxs-lookup"><span data-stu-id="163dd-140">Waiting.</span></span>
<span data-ttu-id="163dd-141">La sezione dati è in attesa di convalida in base ai criteri di convalida prima dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="163dd-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="163dd-142">Pronto.</span><span class="sxs-lookup"><span data-stu-id="163dd-142">Ready.</span></span>
<span data-ttu-id="163dd-143">L'elaborazione dei dati è stata completata e la sezione dati è pronta.</span><span class="sxs-lookup"><span data-stu-id="163dd-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="163dd-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="163dd-144">InProgress.</span></span>
<span data-ttu-id="163dd-145">L'elaborazione dei dati è in corso.</span><span class="sxs-lookup"><span data-stu-id="163dd-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="163dd-146">Operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="163dd-146">Failed.</span></span>
<span data-ttu-id="163dd-147">Elaborazione dei dati non riuscita.</span><span class="sxs-lookup"><span data-stu-id="163dd-147">Data processing failed.</span></span>
- <span data-ttu-id="163dd-148">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="163dd-148">Skipped.</span></span>
<span data-ttu-id="163dd-149">L'elaborazione della sezione dati è stata ignorata.</span><span class="sxs-lookup"><span data-stu-id="163dd-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163dd-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="163dd-150">-UpdateType</span></span>
<span data-ttu-id="163dd-151">Specifica il tipo di aggiornamento della sezione.</span><span class="sxs-lookup"><span data-stu-id="163dd-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="163dd-152">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="163dd-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="163dd-153">Individuo.</span><span class="sxs-lookup"><span data-stu-id="163dd-153">Individual.</span></span>
<span data-ttu-id="163dd-154">Imposta lo stato di ogni sezione per il set di dati nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="163dd-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="163dd-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="163dd-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="163dd-156">Imposta lo stato di ogni sezione per il set di dati e per tutti i set di dati dipendenti, che vengono usati come set di dati di input per le attività nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="163dd-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163dd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163dd-157">CommonParameters</span></span>
<span data-ttu-id="163dd-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="163dd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163dd-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="163dd-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163dd-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="163dd-160">INPUTS</span></span>

### <span data-ttu-id="163dd-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="163dd-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="163dd-162">System.String</span><span class="sxs-lookup"><span data-stu-id="163dd-162">System.String</span></span>

## <span data-ttu-id="163dd-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="163dd-163">OUTPUTS</span></span>

### <span data-ttu-id="163dd-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="163dd-164">System.Boolean</span></span>

## <span data-ttu-id="163dd-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="163dd-165">NOTES</span></span>
* <span data-ttu-id="163dd-166">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="163dd-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="163dd-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="163dd-167">RELATED LINKS</span></span>

[<span data-ttu-id="163dd-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="163dd-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


