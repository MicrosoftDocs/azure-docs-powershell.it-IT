---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193625"
---
# <span data-ttu-id="80dc3-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="80dc3-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="80dc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="80dc3-103">Restituisce informazioni sui membri della sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc3-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="80dc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80dc3-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80dc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="80dc3-106">Il cmdlet **Get-AzSqlSyncMember** restituisce informazioni su uno o più membri della sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc3-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="80dc3-107">Specificare il nome di un membro di sincronizzazione per visualizzare le informazioni solo per il membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="80dc3-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="80dc3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80dc3-108">EXAMPLES</span></span>

### <span data-ttu-id="80dc3-109">Esempio 1: ottenere tutte le istanze del membro di sincronizzazione di Azure SQL assegnato a un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="80dc3-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="80dc3-110">Questo comando consente di ottenere informazioni su tutto il membro di sincronizzazione del database SQL di Azure assegnato al gruppo di sincronizzazione SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="80dc3-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="80dc3-111">Esempio 2: ottenere informazioni su un membro di sincronizzazione di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="80dc3-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="80dc3-112">Questo comando ottiene le informazioni sul membro di sincronizzazione di database SQL di Azure con il nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="80dc3-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="80dc3-113">Esempio 3: ottenere tutte le istanze del membro di sincronizzazione di Azure SQL assegnate a un gruppo di sincronizzazione tramite filtro</span><span class="sxs-lookup"><span data-stu-id="80dc3-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="80dc3-114">Questo comando consente di ottenere informazioni su tutto il membro di sincronizzazione di database SQL di Azure assegnato al gruppo di sincronizzazione SyncGroup01 che inizia con "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="80dc3-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="80dc3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80dc3-115">PARAMETERS</span></span>

### <span data-ttu-id="80dc3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80dc3-116">-DatabaseName</span></span>
<span data-ttu-id="80dc3-117">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="80dc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dc3-118">-DefaultProfile</span></span>
<span data-ttu-id="80dc3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="80dc3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80dc3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="80dc3-120">-Name</span></span>
<span data-ttu-id="80dc3-121">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="80dc3-121">The sync member name.</span></span>

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

### <span data-ttu-id="80dc3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80dc3-122">-ResourceGroupName</span></span>
<span data-ttu-id="80dc3-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80dc3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="80dc3-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="80dc3-124">-ServerName</span></span>
<span data-ttu-id="80dc3-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80dc3-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="80dc3-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="80dc3-126">-SyncGroupName</span></span>
<span data-ttu-id="80dc3-127">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="80dc3-127">The sync group name.</span></span>

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

### <span data-ttu-id="80dc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dc3-128">CommonParameters</span></span>
<span data-ttu-id="80dc3-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80dc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dc3-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80dc3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dc3-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80dc3-131">INPUTS</span></span>

### <span data-ttu-id="80dc3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80dc3-132">System.String</span></span>

## <span data-ttu-id="80dc3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80dc3-133">OUTPUTS</span></span>

### <span data-ttu-id="80dc3-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="80dc3-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="80dc3-135">Note</span><span class="sxs-lookup"><span data-stu-id="80dc3-135">NOTES</span></span>

## <span data-ttu-id="80dc3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80dc3-136">RELATED LINKS</span></span>

[<span data-ttu-id="80dc3-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="80dc3-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="80dc3-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="80dc3-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="80dc3-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="80dc3-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)
