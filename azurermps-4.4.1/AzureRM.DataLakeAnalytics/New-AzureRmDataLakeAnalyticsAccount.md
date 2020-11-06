---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521253"
---
# <span data-ttu-id="50277-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="50277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50277-102">SYNOPSIS</span></span>
<span data-ttu-id="50277-103">Crea un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="50277-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50277-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50277-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50277-105">DESCRIPTION</span></span>
<span data-ttu-id="50277-106">Il cmdlet **New-AzureRmDataLakeAnalyticsAccount** crea un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="50277-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="50277-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50277-107">EXAMPLES</span></span>

### <span data-ttu-id="50277-108">Esempio 1: creare un account di analisi dei dati sul lago</span><span class="sxs-lookup"><span data-stu-id="50277-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="50277-109">Questo comando crea un account di analisi dei dati del lago denominato ContosoAdlAccount che usa l'archivio dati di ContosoAdlStore, nel gruppo risorse denominato ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="50277-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="50277-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50277-110">PARAMETERS</span></span>

### <span data-ttu-id="50277-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50277-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="50277-112">Specifica il nome dell'account del data Lake Store da impostare come origine dati predefinita.</span><span class="sxs-lookup"><span data-stu-id="50277-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="50277-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50277-113">-Location</span></span>
<span data-ttu-id="50277-114">Specifica la posizione in cui creare l'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="50277-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="50277-115">Attualmente è supportata solo la parte est degli Stati Uniti 2.</span><span class="sxs-lookup"><span data-stu-id="50277-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="50277-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="50277-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="50277-117">Il grado di parallelismo supportato massimo facoltativo per questo account.</span><span class="sxs-lookup"><span data-stu-id="50277-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="50277-118">Se non si specifica nessuno, il valore predefinito è 30</span><span class="sxs-lookup"><span data-stu-id="50277-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="50277-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="50277-119">-MaxJobCount</span></span>
<span data-ttu-id="50277-120">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="50277-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="50277-121">Se non si specifica nessuno, il valore predefinito è 3</span><span class="sxs-lookup"><span data-stu-id="50277-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="50277-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="50277-122">-Name</span></span>
<span data-ttu-id="50277-123">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="50277-123">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="50277-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="50277-124">-QueryStoreRetention</span></span>
<span data-ttu-id="50277-125">Numero facoltativo di giorni in cui vengono conservati i metadati del processo.</span><span class="sxs-lookup"><span data-stu-id="50277-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="50277-126">Se nessuno specificato, il valore predefinito è 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="50277-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="50277-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50277-127">-ResourceGroupName</span></span>
<span data-ttu-id="50277-128">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="50277-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="50277-129">Per creare un gruppo di risorse, usare il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="50277-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="50277-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="50277-130">-Tags</span></span>
<span data-ttu-id="50277-131">Specifica le coppie chiave-valore che possono essere usate per identificare l'account di analisi dei dati di Lake tra le altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="50277-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="50277-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="50277-132">-Tier</span></span>
<span data-ttu-id="50277-133">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="50277-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="50277-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50277-134">-DefaultProfile</span></span>
<span data-ttu-id="50277-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50277-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50277-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50277-136">CommonParameters</span></span>
<span data-ttu-id="50277-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50277-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50277-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50277-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50277-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50277-139">INPUTS</span></span>

## <span data-ttu-id="50277-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50277-140">OUTPUTS</span></span>

### <span data-ttu-id="50277-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="50277-142">Dettagli dell'account appena creato.</span><span class="sxs-lookup"><span data-stu-id="50277-142">The details of the newly created account.</span></span>

## <span data-ttu-id="50277-143">Note</span><span class="sxs-lookup"><span data-stu-id="50277-143">NOTES</span></span>

## <span data-ttu-id="50277-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50277-144">RELATED LINKS</span></span>

[<span data-ttu-id="50277-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50277-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50277-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50277-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50277-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


