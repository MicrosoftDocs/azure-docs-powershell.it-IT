---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510680"
---
# <span data-ttu-id="590a6-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="590a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="590a6-102">SYNOPSIS</span></span>
<span data-ttu-id="590a6-103">Modifica un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="590a6-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="590a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="590a6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="590a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590a6-105">DESCRIPTION</span></span>
<span data-ttu-id="590a6-106">Il cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="590a6-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="590a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="590a6-107">EXAMPLES</span></span>

### <span data-ttu-id="590a6-108">Esempio 1: modificare l'origine dati di un account</span><span class="sxs-lookup"><span data-stu-id="590a6-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="590a6-109">Questo comando modifica l'origine dati predefinita e la proprietà Tags dell'account.</span><span class="sxs-lookup"><span data-stu-id="590a6-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="590a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="590a6-110">PARAMETERS</span></span>

### <span data-ttu-id="590a6-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="590a6-111">-AllowAzureIpState</span></span>
<span data-ttu-id="590a6-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="590a6-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="590a6-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="590a6-113">-FirewallState</span></span>
<span data-ttu-id="590a6-114">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="590a6-114">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="590a6-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="590a6-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="590a6-116">Il grado di parallelismo supportato massimo facoltativo per aggiornare l'account.</span><span class="sxs-lookup"><span data-stu-id="590a6-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="590a6-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="590a6-117">-MaxJobCount</span></span>
<span data-ttu-id="590a6-118">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente a set.</span><span class="sxs-lookup"><span data-stu-id="590a6-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="590a6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="590a6-119">-Name</span></span>
<span data-ttu-id="590a6-120">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="590a6-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="590a6-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="590a6-121">-QueryStoreRetention</span></span>
<span data-ttu-id="590a6-122">Numero facoltativo di giorni in cui i metadati del processo vengono conservati per l'impostazione nell'account.</span><span class="sxs-lookup"><span data-stu-id="590a6-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="590a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="590a6-124">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="590a6-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="590a6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="590a6-125">-Tags</span></span>
<span data-ttu-id="590a6-126">Specifica le coppie chiave-valore che possono essere usate per identificare l'account di analisi dei dati di Lake tra le altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="590a6-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="590a6-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="590a6-127">-Tier</span></span>
<span data-ttu-id="590a6-128">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="590a6-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="590a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590a6-129">-DefaultProfile</span></span>
<span data-ttu-id="590a6-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="590a6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="590a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590a6-131">CommonParameters</span></span>
<span data-ttu-id="590a6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590a6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="590a6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590a6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="590a6-134">INPUTS</span></span>

## <span data-ttu-id="590a6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="590a6-135">OUTPUTS</span></span>

### <span data-ttu-id="590a6-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="590a6-137">Dettagli dell'account aggiornato.</span><span class="sxs-lookup"><span data-stu-id="590a6-137">The updated account details.</span></span>

## <span data-ttu-id="590a6-138">Note</span><span class="sxs-lookup"><span data-stu-id="590a6-138">NOTES</span></span>

## <span data-ttu-id="590a6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="590a6-139">RELATED LINKS</span></span>

[<span data-ttu-id="590a6-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="590a6-141">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="590a6-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="590a6-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="590a6-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


