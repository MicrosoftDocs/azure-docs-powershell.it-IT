---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512660"
---
# <span data-ttu-id="bf335-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="bf335-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf335-102">SYNOPSIS</span></span>
<span data-ttu-id="bf335-103">Crea un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="bf335-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf335-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf335-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf335-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf335-105">DESCRIPTION</span></span>
<span data-ttu-id="bf335-106">Il cmdlet **New-AzureRmDataLakeAnalyticsAccount** crea un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="bf335-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bf335-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf335-107">EXAMPLES</span></span>

### <span data-ttu-id="bf335-108">Esempio 1: creare un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="bf335-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="bf335-109">Questo comando crea un account di analisi dei dati del lago denominato ContosoAdlAccount che usa l'archivio dati di ContosoAdlStore, nel gruppo risorse denominato ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="bf335-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="bf335-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf335-110">PARAMETERS</span></span>

### <span data-ttu-id="bf335-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf335-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="bf335-112">Specifica il nome dell'account del data Lake Store da impostare come origine dati predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf335-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf335-113">-DefaultProfile</span></span>
<span data-ttu-id="bf335-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bf335-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf335-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bf335-115">-Location</span></span>
<span data-ttu-id="bf335-116">Specifica la posizione in cui creare l'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="bf335-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="bf335-117">Attualmente è supportata solo la parte est degli Stati Uniti 2.</span><span class="sxs-lookup"><span data-stu-id="bf335-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="bf335-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="bf335-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="bf335-119">Le unità di analisi massime supportate facoltative per questo account.</span><span class="sxs-lookup"><span data-stu-id="bf335-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="bf335-120">-MaxJobCount</span></span>
<span data-ttu-id="bf335-121">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="bf335-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="bf335-122">Se non si specifica nessuno, il valore predefinito è 3</span><span class="sxs-lookup"><span data-stu-id="bf335-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf335-123">-Name</span></span>
<span data-ttu-id="bf335-124">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="bf335-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="bf335-125">-QueryStoreRetention</span></span>
<span data-ttu-id="bf335-126">Numero facoltativo di giorni in cui vengono conservati i metadati del processo.</span><span class="sxs-lookup"><span data-stu-id="bf335-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="bf335-127">Se nessuno specificato, il valore predefinito è 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="bf335-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf335-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf335-129">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="bf335-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="bf335-130">Per creare un gruppo di risorse, usare il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bf335-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf335-131">-Tag</span></span>
<span data-ttu-id="bf335-132">Stringa, dizionario di stringhe di tag associati a questo account</span><span class="sxs-lookup"><span data-stu-id="bf335-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="bf335-133">-Tier</span></span>
<span data-ttu-id="bf335-134">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="bf335-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf335-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf335-135">CommonParameters</span></span>
<span data-ttu-id="bf335-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf335-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf335-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf335-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf335-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf335-138">INPUTS</span></span>

### <span data-ttu-id="bf335-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bf335-139">None</span></span>
<span data-ttu-id="bf335-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bf335-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf335-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf335-141">OUTPUTS</span></span>

### <span data-ttu-id="bf335-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="bf335-143">Dettagli dell'account appena creato.</span><span class="sxs-lookup"><span data-stu-id="bf335-143">The details of the newly created account.</span></span>

## <span data-ttu-id="bf335-144">Note</span><span class="sxs-lookup"><span data-stu-id="bf335-144">NOTES</span></span>

## <span data-ttu-id="bf335-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf335-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf335-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf335-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf335-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf335-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf335-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


