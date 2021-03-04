---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969230"
---
# <span data-ttu-id="91453-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="91453-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="91453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91453-102">SYNOPSIS</span></span>
<span data-ttu-id="91453-103">Aggiunge i set di dati alla condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="91453-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="91453-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91453-104">SYNTAX</span></span>

### <span data-ttu-id="91453-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91453-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91453-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="91453-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91453-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="91453-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91453-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="91453-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91453-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91453-109">DESCRIPTION</span></span>
<span data-ttu-id="91453-110">Il cmdlet **New-AzDataShareDataSet aggiunge** set di dati nella condivisione dati di Azure dell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="91453-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="91453-111">È possibile aggiungere set di dati di tipo BLOB, ADLS Gen2 e ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="91453-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="91453-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91453-112">EXAMPLES</span></span>

### <span data-ttu-id="91453-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91453-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="91453-114">Questo comando aggiunge un set di dati denominato AdsDataSet del contenitore BLOB di tipo alla condivisione di dati di Azure AdsShare.</span><span class="sxs-lookup"><span data-stu-id="91453-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="91453-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91453-115">PARAMETERS</span></span>

### <span data-ttu-id="91453-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91453-116">-AccountName</span></span>
<span data-ttu-id="91453-117">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-117">Azure data share account name</span></span>

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

### <span data-ttu-id="91453-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="91453-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="91453-119">Percorso cartella gen1 di Azure Storage ADLS</span><span class="sxs-lookup"><span data-stu-id="91453-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="91453-120">-Container</span><span class="sxs-lookup"><span data-stu-id="91453-120">-Container</span></span>
<span data-ttu-id="91453-121">Nome contenitore account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="91453-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91453-122">-DefaultProfile</span></span>
<span data-ttu-id="91453-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91453-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91453-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="91453-124">-FileName</span></span>
<span data-ttu-id="91453-125">Nome file gen1 di Azure Storage ADLS</span><span class="sxs-lookup"><span data-stu-id="91453-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="91453-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="91453-126">-FilePath</span></span>
<span data-ttu-id="91453-127">Percorso file di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-127">Azure storage file path</span></span>

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

### <span data-ttu-id="91453-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="91453-128">-FileSystem</span></span>
<span data-ttu-id="91453-129">Nome file system di Azure ADLS gen2</span><span class="sxs-lookup"><span data-stu-id="91453-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="91453-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="91453-130">-FolderPath</span></span>
<span data-ttu-id="91453-131">Percorso cartella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="91453-132">-Name</span><span class="sxs-lookup"><span data-stu-id="91453-132">-Name</span></span>
<span data-ttu-id="91453-133">Nome del set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-133">Azure data set name</span></span>

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

### <span data-ttu-id="91453-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91453-134">-ResourceGroupName</span></span>
<span data-ttu-id="91453-135">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="91453-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="91453-136">-ShareName</span></span>
<span data-ttu-id="91453-137">Nome condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-137">Azure data share name</span></span>

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

### <span data-ttu-id="91453-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="91453-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="91453-139">ResourceId dell'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="91453-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="91453-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91453-140">-Confirm</span></span>
<span data-ttu-id="91453-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91453-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91453-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91453-142">-WhatIf</span></span>
<span data-ttu-id="91453-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91453-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91453-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91453-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91453-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91453-145">CommonParameters</span></span>
<span data-ttu-id="91453-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91453-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91453-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91453-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91453-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="91453-148">INPUTS</span></span>

### <span data-ttu-id="91453-149">System.String</span><span class="sxs-lookup"><span data-stu-id="91453-149">System.String</span></span>

## <span data-ttu-id="91453-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91453-150">OUTPUTS</span></span>

### <span data-ttu-id="91453-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="91453-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="91453-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="91453-152">NOTES</span></span>

## <span data-ttu-id="91453-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91453-153">RELATED LINKS</span></span>
