---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: c17daaf714154d24322111497841a1814dfb5773
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685467"
---
# <span data-ttu-id="d9513-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9513-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="d9513-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9513-102">SYNOPSIS</span></span>
<span data-ttu-id="d9513-103">Restituisce informazioni sui membri della sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9513-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9513-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9513-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9513-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9513-105">DESCRIPTION</span></span>
<span data-ttu-id="d9513-106">Il cmdlet **Get-AzureRmSqlSyncMember** restituisce informazioni su uno o più membri della sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9513-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="d9513-107">Specificare il nome di un membro di sincronizzazione per visualizzare le informazioni solo per il membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d9513-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="d9513-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9513-108">EXAMPLES</span></span>

### <span data-ttu-id="d9513-109">Esempio 1: ottenere tutte le istanze del membro di sincronizzazione di Azure SQL assegnato a un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="d9513-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="d9513-110">Questo comando consente di ottenere informazioni su tutto il membro di sincronizzazione del database SQL di Azure assegnato al gruppo di sincronizzazione SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="d9513-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="d9513-111">Esempio 2: ottenere informazioni su un membro di sincronizzazione di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d9513-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="d9513-112">Questo comando ottiene le informazioni sul membro di sincronizzazione di database SQL di Azure con il nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="d9513-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="d9513-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9513-113">PARAMETERS</span></span>

### <span data-ttu-id="d9513-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9513-114">-DatabaseName</span></span>
<span data-ttu-id="d9513-115">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9513-115">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9513-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9513-116">-DefaultProfile</span></span>
<span data-ttu-id="d9513-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d9513-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9513-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9513-118">-Name</span></span>
<span data-ttu-id="d9513-119">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d9513-119">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9513-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9513-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9513-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9513-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9513-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d9513-122">-ServerName</span></span>
<span data-ttu-id="d9513-123">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d9513-123">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9513-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d9513-124">-SyncGroupName</span></span>
<span data-ttu-id="d9513-125">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d9513-125">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9513-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9513-126">CommonParameters</span></span>
<span data-ttu-id="d9513-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9513-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9513-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9513-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9513-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9513-129">INPUTS</span></span>

### <span data-ttu-id="d9513-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9513-130">None</span></span>
<span data-ttu-id="d9513-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d9513-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9513-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9513-132">OUTPUTS</span></span>

### <span data-ttu-id="d9513-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d9513-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d9513-134">Note</span><span class="sxs-lookup"><span data-stu-id="d9513-134">NOTES</span></span>

## <span data-ttu-id="d9513-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9513-135">RELATED LINKS</span></span>

[<span data-ttu-id="d9513-136">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9513-136">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d9513-137">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9513-137">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d9513-138">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9513-138">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

