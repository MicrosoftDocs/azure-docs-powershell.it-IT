---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191185"
---
# <span data-ttu-id="e5eb8-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="e5eb8-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="e5eb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5eb8-103">Restituisce i log di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e5eb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5eb8-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5eb8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="e5eb8-106">Il cmdlet **Get-AzSqlSyncGroupLog** restituisce i log di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e5eb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="e5eb8-108">Esempio 1: recuperare i log di un gruppo di sincronizzazione SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e5eb8-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="e5eb8-109">Questo comando consente di ottenere i log di un gruppo di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="e5eb8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5eb8-110">PARAMETERS</span></span>

### <span data-ttu-id="e5eb8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5eb8-111">-DatabaseName</span></span>
<span data-ttu-id="e5eb8-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e5eb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5eb8-113">-DefaultProfile</span></span>
<span data-ttu-id="e5eb8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5eb8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5eb8-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e5eb8-115">-EndTime</span></span>
<span data-ttu-id="e5eb8-116">L'ora di fine dei registri da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="e5eb8-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e5eb8-117">-LogLevel</span></span>
<span data-ttu-id="e5eb8-118">Tipo di log da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-118">The type of the logs to query.</span></span>
<span data-ttu-id="e5eb8-119">I valori validi sono: "Error", "Warning", "success" e "All".</span><span class="sxs-lookup"><span data-stu-id="e5eb8-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="e5eb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5eb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5eb8-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5eb8-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e5eb8-122">-ServerName</span></span>
<span data-ttu-id="e5eb8-123">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e5eb8-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e5eb8-124">-StartTime</span></span>
<span data-ttu-id="e5eb8-125">L'ora di inizio dei registri da eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="e5eb8-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e5eb8-126">-SyncGroupName</span></span>
<span data-ttu-id="e5eb8-127">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-127">The sync group name.</span></span>

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

### <span data-ttu-id="e5eb8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5eb8-128">CommonParameters</span></span>
<span data-ttu-id="e5eb8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5eb8-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5eb8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5eb8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5eb8-131">INPUTS</span></span>

### <span data-ttu-id="e5eb8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e5eb8-132">System.String</span></span>

## <span data-ttu-id="e5eb8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5eb8-133">OUTPUTS</span></span>

### <span data-ttu-id="e5eb8-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="e5eb8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="e5eb8-135">Note</span><span class="sxs-lookup"><span data-stu-id="e5eb8-135">NOTES</span></span>

## <span data-ttu-id="e5eb8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5eb8-136">RELATED LINKS</span></span>
