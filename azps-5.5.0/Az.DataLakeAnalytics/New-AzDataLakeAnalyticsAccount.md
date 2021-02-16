---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204402"
---
# <span data-ttu-id="36911-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="36911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36911-102">SYNOPSIS</span></span>
<span data-ttu-id="36911-103">Crea un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="36911-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="36911-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36911-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36911-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36911-105">DESCRIPTION</span></span>
<span data-ttu-id="36911-106">Il cmdlet **New-AzDataLakeAnalyticsAccount** crea un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="36911-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="36911-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36911-107">EXAMPLES</span></span>

### <span data-ttu-id="36911-108">Esempio 1: Creare un account Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="36911-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="36911-109">Questo comando crea un account Data Lake Analytics denominato ContosoAdlAccount che usa l'archivio dati ContosoAdlStore nel gruppo di risorse denominato ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="36911-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="36911-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36911-110">PARAMETERS</span></span>

### <span data-ttu-id="36911-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="36911-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="36911-112">Specifica il nome dell'account Data Lake Store da impostare come origine dati predefinita.</span><span class="sxs-lookup"><span data-stu-id="36911-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36911-113">-DefaultProfile</span></span>
<span data-ttu-id="36911-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="36911-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36911-115">-Location</span><span class="sxs-lookup"><span data-stu-id="36911-115">-Location</span></span>
<span data-ttu-id="36911-116">Specifica la posizione in cui creare l'account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="36911-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="36911-117">Al momento sono supportati solo gli Stati Uniti orientali 2.</span><span class="sxs-lookup"><span data-stu-id="36911-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="36911-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="36911-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="36911-119">Il numero massimo facoltativo di unità di analisi supportate per questo account.</span><span class="sxs-lookup"><span data-stu-id="36911-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="36911-120">-MaxJobCount</span></span>
<span data-ttu-id="36911-121">Numero massimo facoltativo di processi supportati in esecuzione contemporaneamente nell'account.</span><span class="sxs-lookup"><span data-stu-id="36911-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="36911-122">Se non viene specificato, il valore predefinito è 3</span><span class="sxs-lookup"><span data-stu-id="36911-122">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-123">-Name</span><span class="sxs-lookup"><span data-stu-id="36911-123">-Name</span></span>
<span data-ttu-id="36911-124">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="36911-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="36911-125">-QueryStoreRetention</span></span>
<span data-ttu-id="36911-126">Numero facoltativo di giorni per cui vengono conservati i metadati del processo.</span><span class="sxs-lookup"><span data-stu-id="36911-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="36911-127">Se non è specificato, il valore predefinito è 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="36911-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36911-128">-ResourceGroupName</span></span>
<span data-ttu-id="36911-129">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="36911-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="36911-130">Per creare un gruppo di risorse, usare il cmdlet New-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="36911-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="36911-131">-Tag</span></span>
<span data-ttu-id="36911-132">Stringa, dizionario stringa di tag associati a questo account</span><span class="sxs-lookup"><span data-stu-id="36911-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-133">-Livello</span><span class="sxs-lookup"><span data-stu-id="36911-133">-Tier</span></span>
<span data-ttu-id="36911-134">Il livello di impegno desiderato per l'uso di questo account.</span><span class="sxs-lookup"><span data-stu-id="36911-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36911-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36911-135">CommonParameters</span></span>
<span data-ttu-id="36911-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36911-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36911-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36911-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36911-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="36911-138">INPUTS</span></span>

### <span data-ttu-id="36911-139">System.String</span><span class="sxs-lookup"><span data-stu-id="36911-139">System.String</span></span>

### <span data-ttu-id="36911-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="36911-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="36911-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36911-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36911-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="36911-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="36911-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36911-143">OUTPUTS</span></span>

### <span data-ttu-id="36911-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="36911-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="36911-145">NOTES</span></span>

## <span data-ttu-id="36911-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36911-146">RELATED LINKS</span></span>

[<span data-ttu-id="36911-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="36911-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="36911-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="36911-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="36911-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


