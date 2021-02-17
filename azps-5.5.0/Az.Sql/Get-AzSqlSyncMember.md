---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178438"
---
# <span data-ttu-id="0b591-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0b591-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="0b591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b591-102">SYNOPSIS</span></span>
<span data-ttu-id="0b591-103">Restituisce informazioni sui membri di Azure SQL di sincronizzazione del database.</span><span class="sxs-lookup"><span data-stu-id="0b591-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="0b591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b591-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b591-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b591-105">DESCRIPTION</span></span>
<span data-ttu-id="0b591-106">Il **cmdlet Get-AzSqlSyncMember** restituisce informazioni su uno o più membri di Azure SQL di sincronizzazione del database.</span><span class="sxs-lookup"><span data-stu-id="0b591-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="0b591-107">Specificare il nome di un membro di sincronizzazione per visualizzare le informazioni solo per tale membro.</span><span class="sxs-lookup"><span data-stu-id="0b591-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="0b591-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b591-108">EXAMPLES</span></span>

### <span data-ttu-id="0b591-109">Esempio 1: Ottenere tutte le istanze di Azure SQL membro di sincronizzazione assegnato a un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0b591-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="0b591-110">Questo comando ottiene informazioni su tutti i membri di SQL database di Azure assegnati al gruppo di sincronizzazione SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="0b591-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="0b591-111">Esempio 2: Ottenere informazioni su un membro di sincronizzazione del database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0b591-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="0b591-112">Questo comando ottiene informazioni sul membro di sincronizzazione SQL database di Azure con nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="0b591-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="0b591-113">Esempio 3: Ottenere tutte le istanze di Azure SQL membro di sincronizzazione assegnato a un gruppo di sincronizzazione usando i filtri</span><span class="sxs-lookup"><span data-stu-id="0b591-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="0b591-114">Questo comando ottiene informazioni su tutti i membri di SQL database di Azure assegnati al gruppo di sincronizzazione SyncGroup01 che iniziano con "MembroSincronizzazione".</span><span class="sxs-lookup"><span data-stu-id="0b591-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="0b591-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b591-115">PARAMETERS</span></span>

### <span data-ttu-id="0b591-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b591-116">-DatabaseName</span></span>
<span data-ttu-id="0b591-117">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0b591-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0b591-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b591-118">-DefaultProfile</span></span>
<span data-ttu-id="0b591-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0b591-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b591-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0b591-120">-Name</span></span>
<span data-ttu-id="0b591-121">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0b591-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b591-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b591-122">-ResourceGroupName</span></span>
<span data-ttu-id="0b591-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b591-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b591-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b591-124">-ServerName</span></span>
<span data-ttu-id="0b591-125">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b591-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0b591-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0b591-126">-SyncGroupName</span></span>
<span data-ttu-id="0b591-127">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0b591-127">The sync group name.</span></span>

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

### <span data-ttu-id="0b591-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b591-128">CommonParameters</span></span>
<span data-ttu-id="0b591-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b591-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b591-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b591-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b591-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b591-131">INPUTS</span></span>

### <span data-ttu-id="0b591-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0b591-132">System.String</span></span>

## <span data-ttu-id="0b591-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b591-133">OUTPUTS</span></span>

### <span data-ttu-id="0b591-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="0b591-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="0b591-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b591-135">NOTES</span></span>

## <span data-ttu-id="0b591-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b591-136">RELATED LINKS</span></span>

[<span data-ttu-id="0b591-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0b591-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="0b591-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0b591-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="0b591-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0b591-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

