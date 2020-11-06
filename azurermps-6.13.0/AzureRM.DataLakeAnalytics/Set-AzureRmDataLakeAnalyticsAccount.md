---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518767"
---
# <span data-ttu-id="63130-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="63130-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63130-102">SYNOPSIS</span></span>
<span data-ttu-id="63130-103">Modifica un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="63130-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63130-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63130-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63130-105">DESCRIPTION</span></span>
<span data-ttu-id="63130-106">Il cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="63130-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="63130-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63130-107">EXAMPLES</span></span>

### <span data-ttu-id="63130-108">Esempio 1: modificare l'origine dati di un account</span><span class="sxs-lookup"><span data-stu-id="63130-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="63130-109">Questo comando modifica l'origine dati predefinita e la proprietà Tags dell'account.</span><span class="sxs-lookup"><span data-stu-id="63130-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="63130-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63130-110">PARAMETERS</span></span>

### <span data-ttu-id="63130-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="63130-111">-AllowAzureIpState</span></span>
<span data-ttu-id="63130-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="63130-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="63130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63130-113">-DefaultProfile</span></span>
<span data-ttu-id="63130-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63130-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63130-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="63130-115">-FirewallState</span></span>
<span data-ttu-id="63130-116">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="63130-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="63130-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="63130-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="63130-118">Le unità di analisi massime supportate facoltative per aggiornare l'account.</span><span class="sxs-lookup"><span data-stu-id="63130-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="63130-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="63130-119">-MaxJobCount</span></span>
<span data-ttu-id="63130-120">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente a set.</span><span class="sxs-lookup"><span data-stu-id="63130-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="63130-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="63130-121">-Name</span></span>
<span data-ttu-id="63130-122">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="63130-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="63130-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="63130-123">-QueryStoreRetention</span></span>
<span data-ttu-id="63130-124">Numero facoltativo di giorni in cui i metadati del processo vengono conservati per l'impostazione nell'account.</span><span class="sxs-lookup"><span data-stu-id="63130-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="63130-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63130-125">-ResourceGroupName</span></span>
<span data-ttu-id="63130-126">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="63130-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="63130-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="63130-127">-Tag</span></span>
<span data-ttu-id="63130-128">Una stringa, un dizionario di stringhe di tag associato a questo account che deve sostituire il set corrente di tag</span><span class="sxs-lookup"><span data-stu-id="63130-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="63130-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="63130-129">-Tier</span></span>
<span data-ttu-id="63130-130">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="63130-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="63130-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63130-131">CommonParameters</span></span>
<span data-ttu-id="63130-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63130-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63130-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63130-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63130-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63130-134">INPUTS</span></span>

### <span data-ttu-id="63130-135">System. String</span><span class="sxs-lookup"><span data-stu-id="63130-135">System.String</span></span>

### <span data-ttu-id="63130-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63130-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63130-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="63130-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="63130-138">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. TierType, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="63130-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="63130-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="63130-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="63130-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="63130-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="63130-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63130-141">OUTPUTS</span></span>

### <span data-ttu-id="63130-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="63130-143">Note</span><span class="sxs-lookup"><span data-stu-id="63130-143">NOTES</span></span>

## <span data-ttu-id="63130-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63130-144">RELATED LINKS</span></span>

[<span data-ttu-id="63130-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63130-146">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63130-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63130-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63130-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


