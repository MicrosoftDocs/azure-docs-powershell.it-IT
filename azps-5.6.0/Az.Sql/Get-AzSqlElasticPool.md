---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: 5d66ac468cbb11ce31d23e5954edbfba360a00ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999566"
---
# <span data-ttu-id="bc53b-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc53b-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="bc53b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc53b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc53b-103">Recupera i pool elastici e i relativi valori di proprietà in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bc53b-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="bc53b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc53b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc53b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc53b-105">DESCRIPTION</span></span>
<span data-ttu-id="bc53b-106">Il cmdlet **Get-AzSqlElasticPool** ottiene pool di elastici e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc53b-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="bc53b-107">Specificare il nome di un pool elastico esistente per visualizzare i valori delle proprietà solo per tale pool.</span><span class="sxs-lookup"><span data-stu-id="bc53b-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="bc53b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc53b-108">EXAMPLES</span></span>

### <span data-ttu-id="bc53b-109">Esempio 1: Ottenere tutti i pool di elastici</span><span class="sxs-lookup"><span data-stu-id="bc53b-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="bc53b-110">Questo comando recupera tutti i pool elastici nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="bc53b-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="bc53b-111">Esempio 2: Ottenere uno specifico pool elastico</span><span class="sxs-lookup"><span data-stu-id="bc53b-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="bc53b-112">Questo comando recupera il pool elastico denominato ElasticPool0127 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="bc53b-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="bc53b-113">Esempio 3: Ottenere metriche per un pool di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="bc53b-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
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

<span data-ttu-id="bc53b-114">Questo comando restituisce le metriche per un pool di database SQL Azure denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="bc53b-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="bc53b-115">Esempio 4: Ottenere tutti i pool di elastici usando il filtro -ElasticPoolName "ElasticPool\*"</span><span class="sxs-lookup"><span data-stu-id="bc53b-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="bc53b-116">Questo comando recupera tutti i pool elastici nel server denominato Server01 che iniziano con "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="bc53b-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="bc53b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc53b-117">PARAMETERS</span></span>

### <span data-ttu-id="bc53b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc53b-118">-DefaultProfile</span></span>
<span data-ttu-id="bc53b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="bc53b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc53b-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bc53b-120">-ElasticPoolName</span></span>
<span data-ttu-id="bc53b-121">Specifica il nome del pool flessibile che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc53b-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc53b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc53b-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc53b-123">Specifica il nome del gruppo di risorse che contiene il pool flessibile che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc53b-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc53b-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc53b-124">-ServerName</span></span>
<span data-ttu-id="bc53b-125">Specifica il nome del server che contiene il pool flessibile che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc53b-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc53b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc53b-126">CommonParameters</span></span>
<span data-ttu-id="bc53b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc53b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc53b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc53b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc53b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc53b-129">INPUTS</span></span>

### <span data-ttu-id="bc53b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bc53b-130">System.String</span></span>

## <span data-ttu-id="bc53b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc53b-131">OUTPUTS</span></span>

### <span data-ttu-id="bc53b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="bc53b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="bc53b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc53b-133">NOTES</span></span>

## <span data-ttu-id="bc53b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc53b-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc53b-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc53b-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="bc53b-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc53b-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="bc53b-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc53b-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


