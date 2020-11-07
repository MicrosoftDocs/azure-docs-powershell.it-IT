---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 9bb6475f0e9ea688c9339980c1a8955ea011fbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674856"
---
# <span data-ttu-id="d2a85-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d2a85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2a85-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a85-103">Modifica un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d2a85-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d2a85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2a85-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2a85-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a85-106">Il cmdlet **set-AzDataLakeAnalyticsAccount** modifica un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d2a85-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d2a85-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2a85-107">EXAMPLES</span></span>

### <span data-ttu-id="d2a85-108">Esempio 1: modificare l'origine dati di un account</span><span class="sxs-lookup"><span data-stu-id="d2a85-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="d2a85-109">Questo comando modifica l'origine dati predefinita e la proprietà Tags dell'account.</span><span class="sxs-lookup"><span data-stu-id="d2a85-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="d2a85-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2a85-110">PARAMETERS</span></span>

### <span data-ttu-id="d2a85-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="d2a85-111">-AllowAzureIpState</span></span>
<span data-ttu-id="d2a85-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="d2a85-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="d2a85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a85-113">-DefaultProfile</span></span>
<span data-ttu-id="d2a85-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d2a85-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2a85-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="d2a85-115">-FirewallState</span></span>
<span data-ttu-id="d2a85-116">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="d2a85-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="d2a85-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="d2a85-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="d2a85-118">Le unità di analisi massime supportate facoltative per aggiornare l'account.</span><span class="sxs-lookup"><span data-stu-id="d2a85-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="d2a85-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d2a85-119">-MaxJobCount</span></span>
<span data-ttu-id="d2a85-120">I processi facoltativi massimi supportati in esecuzione sotto l'account contemporaneamente a set.</span><span class="sxs-lookup"><span data-stu-id="d2a85-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="d2a85-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2a85-121">-Name</span></span>
<span data-ttu-id="d2a85-122">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="d2a85-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d2a85-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="d2a85-123">-QueryStoreRetention</span></span>
<span data-ttu-id="d2a85-124">Numero facoltativo di giorni in cui i metadati del processo vengono conservati per l'impostazione nell'account.</span><span class="sxs-lookup"><span data-stu-id="d2a85-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="d2a85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a85-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2a85-126">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="d2a85-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d2a85-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2a85-127">-Tag</span></span>
<span data-ttu-id="d2a85-128">Una stringa, un dizionario di stringhe di tag associato a questo account che deve sostituire il set corrente di tag</span><span class="sxs-lookup"><span data-stu-id="d2a85-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="d2a85-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="d2a85-129">-Tier</span></span>
<span data-ttu-id="d2a85-130">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="d2a85-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="d2a85-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a85-131">CommonParameters</span></span>
<span data-ttu-id="d2a85-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a85-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a85-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a85-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a85-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2a85-134">INPUTS</span></span>

### <span data-ttu-id="d2a85-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a85-135">System.String</span></span>

### <span data-ttu-id="d2a85-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2a85-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d2a85-137">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d2a85-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d2a85-138">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. TierType, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d2a85-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d2a85-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d2a85-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d2a85-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d2a85-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d2a85-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2a85-141">OUTPUTS</span></span>

### <span data-ttu-id="d2a85-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d2a85-143">Note</span><span class="sxs-lookup"><span data-stu-id="d2a85-143">NOTES</span></span>

## <span data-ttu-id="d2a85-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2a85-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2a85-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2a85-146">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2a85-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d2a85-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d2a85-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

