---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 49da4b322a2782ad23079c07e7f6c5dce171adb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684556"
---
# <span data-ttu-id="8e343-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8e343-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e343-102">SYNOPSIS</span></span>
<span data-ttu-id="8e343-103">Crea un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="8e343-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8e343-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e343-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e343-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e343-105">DESCRIPTION</span></span>
<span data-ttu-id="8e343-106">Il cmdlet **New-AzDataLakeAnalyticsAccount** crea un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8e343-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8e343-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e343-107">EXAMPLES</span></span>

### <span data-ttu-id="8e343-108">Esempio 1: creare un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="8e343-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="8e343-109">Questo comando crea un account di analisi dei dati del lago denominato ContosoAdlAccount che usa l'archivio dati di ContosoAdlStore, nel gruppo risorse denominato ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="8e343-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="8e343-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e343-110">PARAMETERS</span></span>

### <span data-ttu-id="8e343-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e343-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="8e343-112">Specifica il nome dell'account del data Lake Store da impostare come origine dati predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e343-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="8e343-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e343-113">-DefaultProfile</span></span>
<span data-ttu-id="8e343-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e343-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e343-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8e343-115">-Location</span></span>
<span data-ttu-id="8e343-116">Specifica la posizione in cui creare l'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="8e343-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="8e343-117">Attualmente è supportata solo la parte est degli Stati Uniti 2.</span><span class="sxs-lookup"><span data-stu-id="8e343-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="8e343-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="8e343-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="8e343-119">Le unità di analisi massime supportate facoltative per questo account.</span><span class="sxs-lookup"><span data-stu-id="8e343-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="8e343-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8e343-120">-MaxJobCount</span></span>
<span data-ttu-id="8e343-121">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="8e343-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="8e343-122">Se non si specifica nessuno, il valore predefinito è 3</span><span class="sxs-lookup"><span data-stu-id="8e343-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="8e343-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e343-123">-Name</span></span>
<span data-ttu-id="8e343-124">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="8e343-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8e343-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="8e343-125">-QueryStoreRetention</span></span>
<span data-ttu-id="8e343-126">Numero facoltativo di giorni in cui vengono conservati i metadati del processo.</span><span class="sxs-lookup"><span data-stu-id="8e343-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="8e343-127">Se nessuno specificato, il valore predefinito è 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="8e343-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="8e343-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e343-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e343-129">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="8e343-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="8e343-130">Per creare un gruppo di risorse, usare il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8e343-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="8e343-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e343-131">-Tag</span></span>
<span data-ttu-id="8e343-132">Stringa, dizionario di stringhe di tag associati a questo account</span><span class="sxs-lookup"><span data-stu-id="8e343-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="8e343-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="8e343-133">-Tier</span></span>
<span data-ttu-id="8e343-134">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="8e343-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8e343-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e343-135">CommonParameters</span></span>
<span data-ttu-id="8e343-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e343-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e343-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e343-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e343-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e343-138">INPUTS</span></span>

### <span data-ttu-id="8e343-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e343-139">System.String</span></span>

### <span data-ttu-id="8e343-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e343-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8e343-141">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e343-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e343-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. TierType, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8e343-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8e343-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e343-143">OUTPUTS</span></span>

### <span data-ttu-id="8e343-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8e343-145">Note</span><span class="sxs-lookup"><span data-stu-id="8e343-145">NOTES</span></span>

## <span data-ttu-id="8e343-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e343-146">RELATED LINKS</span></span>

[<span data-ttu-id="8e343-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8e343-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8e343-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8e343-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8e343-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

