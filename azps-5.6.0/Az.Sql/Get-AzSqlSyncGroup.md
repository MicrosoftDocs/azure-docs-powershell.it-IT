---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: 3ce7abdb2feb053fe2731484fda0f301225c0b6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005294"
---
# <span data-ttu-id="f23f8-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f23f8-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="f23f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f23f8-103">Restituisce informazioni sui gruppi di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f23f8-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="f23f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f23f8-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f23f8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f23f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f23f8-106">Il **cmdlet Get-AzSqlSyncGroup** restituisce informazioni su uno o più gruppi di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f23f8-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="f23f8-107">Specificare il nome di un gruppo di sincronizzazione per visualizzare informazioni solo per quel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f23f8-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="f23f8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f23f8-108">EXAMPLES</span></span>

### <span data-ttu-id="f23f8-109">Esempio 1: Ottenere tutte le istanze del gruppo di SQL azure assegnato a un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f23f8-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="f23f8-110">Questo comando ottiene informazioni su tutti i gruppi di SQL database di Azure assegnati a un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f23f8-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="f23f8-111">Esempio 2: Ottenere informazioni su un gruppo di sincronizzazione SQL database di Azure</span><span class="sxs-lookup"><span data-stu-id="f23f8-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="f23f8-112">Questo comando ottiene informazioni sul gruppo di sincronizzazione SQL database di Azure con nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="f23f8-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="f23f8-113">Esempio 3: Assegnare tutte le istanze del gruppo di sincronizzazione SQL Azure a un database SQL Azure usando il filtro</span><span class="sxs-lookup"><span data-stu-id="f23f8-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="f23f8-114">Questo comando ottiene informazioni su tutti i gruppi di SQL di database di Azure assegnati a un database SQL azure che iniziano con "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="f23f8-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="f23f8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f23f8-115">PARAMETERS</span></span>

### <span data-ttu-id="f23f8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f23f8-116">-DatabaseName</span></span>
<span data-ttu-id="f23f8-117">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f23f8-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f23f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23f8-118">-DefaultProfile</span></span>
<span data-ttu-id="f23f8-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f23f8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f23f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f23f8-120">-Name</span></span>
<span data-ttu-id="f23f8-121">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f23f8-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="f23f8-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f23f8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f23f8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f23f8-124">-ServerName</span></span>
<span data-ttu-id="f23f8-125">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f23f8-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f23f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23f8-126">CommonParameters</span></span>
<span data-ttu-id="f23f8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23f8-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f23f8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23f8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="f23f8-129">INPUTS</span></span>

### <span data-ttu-id="f23f8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f23f8-130">System.String</span></span>

## <span data-ttu-id="f23f8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f23f8-131">OUTPUTS</span></span>

### <span data-ttu-id="f23f8-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="f23f8-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f23f8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="f23f8-133">NOTES</span></span>

## <span data-ttu-id="f23f8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f23f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="f23f8-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f23f8-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="f23f8-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f23f8-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="f23f8-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f23f8-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

