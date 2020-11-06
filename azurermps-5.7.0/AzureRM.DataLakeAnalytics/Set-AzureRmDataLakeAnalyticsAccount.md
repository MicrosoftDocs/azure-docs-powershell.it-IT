---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514403"
---
# <span data-ttu-id="31a1b-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="31a1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="31a1b-103">Modifica un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="31a1b-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31a1b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31a1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="31a1b-106">Il cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="31a1b-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="31a1b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="31a1b-108">Esempio 1: modificare l'origine dati di un account</span><span class="sxs-lookup"><span data-stu-id="31a1b-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="31a1b-109">Questo comando modifica l'origine dati predefinita e la proprietà Tags dell'account.</span><span class="sxs-lookup"><span data-stu-id="31a1b-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="31a1b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31a1b-110">PARAMETERS</span></span>

### <span data-ttu-id="31a1b-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="31a1b-111">-AllowAzureIpState</span></span>
<span data-ttu-id="31a1b-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="31a1b-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a1b-113">-DefaultProfile</span></span>
<span data-ttu-id="31a1b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="31a1b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31a1b-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="31a1b-115">-FirewallState</span></span>
<span data-ttu-id="31a1b-116">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="31a1b-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a1b-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="31a1b-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="31a1b-118">Le unità di analisi massime supportate facoltative per aggiornare l'account.</span><span class="sxs-lookup"><span data-stu-id="31a1b-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="31a1b-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="31a1b-119">-MaxJobCount</span></span>
<span data-ttu-id="31a1b-120">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente a set.</span><span class="sxs-lookup"><span data-stu-id="31a1b-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="31a1b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="31a1b-121">-Name</span></span>
<span data-ttu-id="31a1b-122">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="31a1b-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="31a1b-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="31a1b-123">-QueryStoreRetention</span></span>
<span data-ttu-id="31a1b-124">Numero facoltativo di giorni in cui i metadati del processo vengono conservati per l'impostazione nell'account.</span><span class="sxs-lookup"><span data-stu-id="31a1b-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="31a1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="31a1b-126">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="31a1b-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a1b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="31a1b-127">-Tag</span></span>
<span data-ttu-id="31a1b-128">Una stringa, un dizionario di stringhe di tag associato a questo account che deve sostituire il set corrente di tag</span><span class="sxs-lookup"><span data-stu-id="31a1b-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a1b-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="31a1b-129">-Tier</span></span>
<span data-ttu-id="31a1b-130">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="31a1b-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="31a1b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a1b-131">CommonParameters</span></span>
<span data-ttu-id="31a1b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a1b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a1b-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a1b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a1b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31a1b-134">INPUTS</span></span>

### <span data-ttu-id="31a1b-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31a1b-135">None</span></span>
<span data-ttu-id="31a1b-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="31a1b-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31a1b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31a1b-137">OUTPUTS</span></span>

### <span data-ttu-id="31a1b-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="31a1b-139">Dettagli dell'account aggiornato.</span><span class="sxs-lookup"><span data-stu-id="31a1b-139">The updated account details.</span></span>

## <span data-ttu-id="31a1b-140">Note</span><span class="sxs-lookup"><span data-stu-id="31a1b-140">NOTES</span></span>

## <span data-ttu-id="31a1b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31a1b-141">RELATED LINKS</span></span>

[<span data-ttu-id="31a1b-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="31a1b-143">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="31a1b-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="31a1b-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31a1b-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


