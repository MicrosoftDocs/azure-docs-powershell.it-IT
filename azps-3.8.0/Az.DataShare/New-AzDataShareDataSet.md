---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 567d1449bdf84770f4699c84618ccdad0ba43ac4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018784"
---
# <span data-ttu-id="32f60-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="32f60-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="32f60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32f60-102">SYNOPSIS</span></span>
<span data-ttu-id="32f60-103">Aggiunge set di dati a una condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="32f60-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="32f60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32f60-104">SYNTAX</span></span>

### <span data-ttu-id="32f60-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32f60-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f60-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="32f60-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f60-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f60-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f60-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="32f60-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f60-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32f60-109">DESCRIPTION</span></span>
<span data-ttu-id="32f60-110">Il cmdlet **New-AzDataShareDataSet** aggiunge set di dati in Azure Data Share of Data Share account.</span><span class="sxs-lookup"><span data-stu-id="32f60-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="32f60-111">È possibile aggiungere set di dati di tipo BLOB, ADL Gen2 e ADL Gen1.</span><span class="sxs-lookup"><span data-stu-id="32f60-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="32f60-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32f60-112">EXAMPLES</span></span>

### <span data-ttu-id="32f60-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32f60-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="32f60-114">Questo comando aggiunge un DataSet denominato AdsDataSet di tipo contenitore BLOB in Azure Data Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="32f60-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="32f60-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32f60-115">PARAMETERS</span></span>

### <span data-ttu-id="32f60-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="32f60-116">-AccountName</span></span>
<span data-ttu-id="32f60-117">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="32f60-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="32f60-119">Percorso cartella di ADL Gen1 di Azure Storage</span><span class="sxs-lookup"><span data-stu-id="32f60-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-120">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="32f60-120">-Container</span></span>
<span data-ttu-id="32f60-121">Nome del contenitore dell'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-121">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f60-122">-DefaultProfile</span></span>
<span data-ttu-id="32f60-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32f60-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32f60-124">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="32f60-124">-FileName</span></span>
<span data-ttu-id="32f60-125">Nome file di Azure Storage ADL Gen1</span><span class="sxs-lookup"><span data-stu-id="32f60-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="32f60-126">-FilePath</span></span>
<span data-ttu-id="32f60-127">Percorso file di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-127">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="32f60-128">-FileSystem</span></span>
<span data-ttu-id="32f60-129">Nome del file System di Azure ADL Gen2</span><span class="sxs-lookup"><span data-stu-id="32f60-129">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="32f60-130">-FolderPath</span></span>
<span data-ttu-id="32f60-131">Percorso della cartella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-131">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="32f60-132">-Name</span></span>
<span data-ttu-id="32f60-133">Nome del set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f60-134">-ResourceGroupName</span></span>
<span data-ttu-id="32f60-135">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="32f60-136">-ShareName</span></span>
<span data-ttu-id="32f60-137">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="32f60-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="32f60-139">ResourceId account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="32f60-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32f60-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32f60-140">-Confirm</span></span>
<span data-ttu-id="32f60-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32f60-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f60-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f60-142">-WhatIf</span></span>
<span data-ttu-id="32f60-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32f60-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f60-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32f60-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f60-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f60-145">CommonParameters</span></span>
<span data-ttu-id="32f60-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f60-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f60-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f60-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f60-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32f60-148">INPUTS</span></span>

### <span data-ttu-id="32f60-149">System. String</span><span class="sxs-lookup"><span data-stu-id="32f60-149">System.String</span></span>

## <span data-ttu-id="32f60-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32f60-150">OUTPUTS</span></span>

### <span data-ttu-id="32f60-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="32f60-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="32f60-152">Note</span><span class="sxs-lookup"><span data-stu-id="32f60-152">NOTES</span></span>

## <span data-ttu-id="32f60-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32f60-153">RELATED LINKS</span></span>
