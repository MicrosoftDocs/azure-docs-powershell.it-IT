---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: ebed943bfea17bf348c48c6d1378822eb8f9c675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519959"
---
# <span data-ttu-id="4fd67-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fd67-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="4fd67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fd67-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd67-103">Ottiene i pool elastici e i relativi valori di proprietà in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd67-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fd67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fd67-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd67-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd67-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd67-106">Il cmdlet **Get-AzureRmSqlElasticPool** ottiene i pool elastici e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="4fd67-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="4fd67-107">Specificare il nome di un pool elastico esistente per visualizzare i valori delle proprietà solo per il pool.</span><span class="sxs-lookup"><span data-stu-id="4fd67-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="4fd67-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fd67-108">EXAMPLES</span></span>

### <span data-ttu-id="4fd67-109">Esempio 1: ottenere tutti i pool elastici</span><span class="sxs-lookup"><span data-stu-id="4fd67-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4fd67-110">Questo comando recupera tutti i pool elastici nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4fd67-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="4fd67-111">Esempio 2: ottenere uno specifico pool elastico</span><span class="sxs-lookup"><span data-stu-id="4fd67-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4fd67-112">Questo comando ottiene il pool elastico denominato ElasticPool0127 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4fd67-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="4fd67-113">Esempio 3: ottenere le metriche per un pool di database elastico di Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4fd67-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="4fd67-114">Questo comando restituisce le metriche per un pool di database elastico di Azure SQL denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4fd67-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="4fd67-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fd67-115">PARAMETERS</span></span>

### <span data-ttu-id="4fd67-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4fd67-116">-ElasticPoolName</span></span>
<span data-ttu-id="4fd67-117">Specifica il nome del pool elastico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd67-117">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd67-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fd67-119">Specifica il nome del gruppo di risorse che contiene il pool elastico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd67-119">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4fd67-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4fd67-120">-ServerName</span></span>
<span data-ttu-id="4fd67-121">Specifica il nome del server che contiene il pool elastico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd67-121">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4fd67-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd67-122">-DefaultProfile</span></span>
<span data-ttu-id="4fd67-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd67-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fd67-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd67-124">CommonParameters</span></span>
<span data-ttu-id="4fd67-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd67-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd67-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd67-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd67-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fd67-127">INPUTS</span></span>

## <span data-ttu-id="4fd67-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fd67-128">OUTPUTS</span></span>

### <span data-ttu-id="4fd67-129">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4fd67-129">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4fd67-130">Note</span><span class="sxs-lookup"><span data-stu-id="4fd67-130">NOTES</span></span>

## <span data-ttu-id="4fd67-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fd67-131">RELATED LINKS</span></span>

[<span data-ttu-id="4fd67-132">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fd67-132">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4fd67-133">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fd67-133">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4fd67-134">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fd67-134">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


