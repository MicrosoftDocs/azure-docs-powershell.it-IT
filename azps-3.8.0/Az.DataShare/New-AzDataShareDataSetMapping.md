---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3cf556bce81a2e77250e597b428aa23c6eabe496
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019794"
---
# <span data-ttu-id="7021a-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="7021a-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="7021a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7021a-102">SYNOPSIS</span></span>
<span data-ttu-id="7021a-103">Crea il mapping del set di dati per l'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="7021a-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="7021a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7021a-104">SYNTAX</span></span>

### <span data-ttu-id="7021a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7021a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7021a-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="7021a-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7021a-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="7021a-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7021a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7021a-108">DESCRIPTION</span></span>
<span data-ttu-id="7021a-109">Il cmdlet **New-AzDataShareDataSetMapping** crea un mapping del set di dati tra i set di dati di origine e l'account di archiviazione del sink in sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="7021a-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="7021a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7021a-110">EXAMPLES</span></span>

### <span data-ttu-id="7021a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7021a-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="7021a-112">Questo comando crea un mapping del set di dati AdsDataSetMapping all'account di archiviazione AdsStorage per la condivisione dell'abbonamento AdsShareSubscription in WikiAdsAccount account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="7021a-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="7021a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7021a-113">PARAMETERS</span></span>

### <span data-ttu-id="7021a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7021a-114">-AccountName</span></span>
<span data-ttu-id="7021a-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-116">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="7021a-116">-Container</span></span>
<span data-ttu-id="7021a-117">Nome del contenitore dell'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="7021a-118">-DatasetId</span><span class="sxs-lookup"><span data-stu-id="7021a-118">-DataSetId</span></span>
<span data-ttu-id="7021a-119">ID set di dati del consumer</span><span class="sxs-lookup"><span data-stu-id="7021a-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7021a-120">-DefaultProfile</span></span>
<span data-ttu-id="7021a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7021a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7021a-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7021a-122">-FilePath</span></span>
<span data-ttu-id="7021a-123">Percorso file di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-123">Azure storage file path</span></span>

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

### <span data-ttu-id="7021a-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7021a-124">-FileSystem</span></span>
<span data-ttu-id="7021a-125">Nome del file System di Azure ADL Gen2</span><span class="sxs-lookup"><span data-stu-id="7021a-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="7021a-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="7021a-126">-FolderPath</span></span>
<span data-ttu-id="7021a-127">Percorso della cartella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="7021a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7021a-128">-Name</span></span>
<span data-ttu-id="7021a-129">Nome del mapping set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7021a-130">-ResourceGroupName</span></span>
<span data-ttu-id="7021a-131">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7021a-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="7021a-133">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7021a-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="7021a-135">ResourceId account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7021a-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7021a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7021a-136">-Confirm</span></span>
<span data-ttu-id="7021a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7021a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7021a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7021a-138">-WhatIf</span></span>
<span data-ttu-id="7021a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7021a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7021a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7021a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7021a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7021a-141">CommonParameters</span></span>
<span data-ttu-id="7021a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7021a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7021a-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7021a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7021a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7021a-144">INPUTS</span></span>

### <span data-ttu-id="7021a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7021a-145">System.String</span></span>

## <span data-ttu-id="7021a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7021a-146">OUTPUTS</span></span>

### <span data-ttu-id="7021a-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="7021a-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="7021a-148">Note</span><span class="sxs-lookup"><span data-stu-id="7021a-148">NOTES</span></span>

## <span data-ttu-id="7021a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7021a-149">RELATED LINKS</span></span>
