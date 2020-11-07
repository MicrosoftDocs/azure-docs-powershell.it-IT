---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: 0343cddd12fdf1fe438ec2c4c9c3c5763719cd43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857425"
---
# <span data-ttu-id="5644a-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="5644a-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="5644a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5644a-102">SYNOPSIS</span></span>
<span data-ttu-id="5644a-103">Restituisce i log di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5644a-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5644a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5644a-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5644a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5644a-105">DESCRIPTION</span></span>
<span data-ttu-id="5644a-106">Il cmdlet **Get-AzSqlSyncGroupLog** restituisce i log di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5644a-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5644a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5644a-107">EXAMPLES</span></span>

### <span data-ttu-id="5644a-108">Esempio 1: recuperare i log di un gruppo di sincronizzazione SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="5644a-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="5644a-109">Questo comando consente di ottenere i log di un gruppo di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5644a-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="5644a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5644a-110">PARAMETERS</span></span>

### <span data-ttu-id="5644a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5644a-111">-DatabaseName</span></span>
<span data-ttu-id="5644a-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5644a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5644a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5644a-113">-DefaultProfile</span></span>
<span data-ttu-id="5644a-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5644a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5644a-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5644a-115">-EndTime</span></span>
<span data-ttu-id="5644a-116">L'ora di fine dei registri da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="5644a-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5644a-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="5644a-117">-LogLevel</span></span>
<span data-ttu-id="5644a-118">Tipo di log da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="5644a-118">The type of the logs to query.</span></span>
<span data-ttu-id="5644a-119">I valori validi sono: "Error", "Warning", "success" e "All".</span><span class="sxs-lookup"><span data-stu-id="5644a-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5644a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5644a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5644a-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5644a-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5644a-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5644a-122">-ServerName</span></span>
<span data-ttu-id="5644a-123">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5644a-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5644a-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5644a-124">-StartTime</span></span>
<span data-ttu-id="5644a-125">L'ora di inizio dei registri da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="5644a-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5644a-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5644a-126">-SyncGroupName</span></span>
<span data-ttu-id="5644a-127">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5644a-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5644a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5644a-128">CommonParameters</span></span>
<span data-ttu-id="5644a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5644a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5644a-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5644a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5644a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5644a-131">INPUTS</span></span>

### <span data-ttu-id="5644a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5644a-132">System.String</span></span>

## <span data-ttu-id="5644a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5644a-133">OUTPUTS</span></span>

### <span data-ttu-id="5644a-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="5644a-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="5644a-135">Note</span><span class="sxs-lookup"><span data-stu-id="5644a-135">NOTES</span></span>

## <span data-ttu-id="5644a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5644a-136">RELATED LINKS</span></span>
