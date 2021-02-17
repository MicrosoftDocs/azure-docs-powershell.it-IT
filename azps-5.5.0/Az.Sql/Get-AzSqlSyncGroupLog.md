---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178431"
---
# <span data-ttu-id="4d89d-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="4d89d-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="4d89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d89d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d89d-103">Restituisce i log di un gruppo di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d89d-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4d89d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d89d-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d89d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d89d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d89d-106">Il **cmdlet Get-AzSqlSyncGroupLog** restituisce i log di un gruppo di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d89d-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4d89d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d89d-107">EXAMPLES</span></span>

### <span data-ttu-id="4d89d-108">Esempio 1: Ottenere i log di un gruppo di sincronizzazione SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4d89d-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="4d89d-109">Questo comando recupera i log di un gruppo di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d89d-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="4d89d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d89d-110">PARAMETERS</span></span>

### <span data-ttu-id="4d89d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d89d-111">-DatabaseName</span></span>
<span data-ttu-id="4d89d-112">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d89d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4d89d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d89d-113">-DefaultProfile</span></span>
<span data-ttu-id="4d89d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4d89d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d89d-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4d89d-115">-EndTime</span></span>
<span data-ttu-id="4d89d-116">Ora di fine dei log per la query.</span><span class="sxs-lookup"><span data-stu-id="4d89d-116">The end time of the logs to query.</span></span>

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

### <span data-ttu-id="4d89d-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4d89d-117">-LogLevel</span></span>
<span data-ttu-id="4d89d-118">Tipo di log in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="4d89d-118">The type of the logs to query.</span></span>
<span data-ttu-id="4d89d-119">I valori validi sono"Error", "Warning", "Success" e "All".</span><span class="sxs-lookup"><span data-stu-id="4d89d-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

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

### <span data-ttu-id="4d89d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d89d-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d89d-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d89d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d89d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d89d-122">-ServerName</span></span>
<span data-ttu-id="4d89d-123">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4d89d-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4d89d-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4d89d-124">-StartTime</span></span>
<span data-ttu-id="4d89d-125">Ora di inizio dei log per la query.</span><span class="sxs-lookup"><span data-stu-id="4d89d-125">The start time of the logs to query.</span></span>

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

### <span data-ttu-id="4d89d-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4d89d-126">-SyncGroupName</span></span>
<span data-ttu-id="4d89d-127">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4d89d-127">The sync group name.</span></span>

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

### <span data-ttu-id="4d89d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d89d-128">CommonParameters</span></span>
<span data-ttu-id="4d89d-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d89d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d89d-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d89d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d89d-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d89d-131">INPUTS</span></span>

### <span data-ttu-id="4d89d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4d89d-132">System.String</span></span>

## <span data-ttu-id="4d89d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d89d-133">OUTPUTS</span></span>

### <span data-ttu-id="4d89d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="4d89d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="4d89d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d89d-135">NOTES</span></span>

## <span data-ttu-id="4d89d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d89d-136">RELATED LINKS</span></span>
