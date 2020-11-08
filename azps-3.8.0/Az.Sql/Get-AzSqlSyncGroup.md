---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018724"
---
# <span data-ttu-id="4b4f1-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4b4f1-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="4b4f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4f1-103">Restituisce informazioni sui gruppi di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="4b4f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b4f1-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b4f1-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4f1-106">Il cmdlet **Get-AzSqlSyncGroup** restituisce informazioni su uno o più gruppi di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="4b4f1-107">Specificare il nome di un gruppo di sincronizzazione per visualizzare le informazioni solo per il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="4b4f1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b4f1-108">EXAMPLES</span></span>

### <span data-ttu-id="4b4f1-109">Esempio 1: ottenere tutte le istanze del gruppo di sincronizzazione SQL di Azure assegnate a un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4b4f1-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="4b4f1-110">Questo comando consente di ottenere informazioni su tutti i gruppi di sincronizzazione di database SQL di Azure assegnati a un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="4b4f1-111">Esempio 2: ottenere informazioni su un gruppo di sincronizzazione di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4b4f1-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="4b4f1-112">Questo comando ottiene le informazioni sul gruppo di sincronizzazione di database SQL di Azure con il nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="4b4f1-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="4b4f1-113">Esempio 3: ottenere tutte le istanze del gruppo di sincronizzazione SQL di Azure assegnate a un database SQL di Azure con il filtro</span><span class="sxs-lookup"><span data-stu-id="4b4f1-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="4b4f1-114">Questo comando consente di ottenere informazioni su tutti i gruppi di sincronizzazione di database SQL di Azure assegnati a un database SQL di Azure che inizia con "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="4b4f1-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="4b4f1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b4f1-115">PARAMETERS</span></span>

### <span data-ttu-id="4b4f1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b4f1-116">-DatabaseName</span></span>
<span data-ttu-id="4b4f1-117">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4b4f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4f1-118">-DefaultProfile</span></span>
<span data-ttu-id="4b4f1-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b4f1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b4f1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b4f1-120">-Name</span></span>
<span data-ttu-id="4b4f1-121">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-121">The sync group name.</span></span>

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

### <span data-ttu-id="4b4f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b4f1-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b4f1-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4b4f1-124">-ServerName</span></span>
<span data-ttu-id="4b4f1-125">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4b4f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4f1-126">CommonParameters</span></span>
<span data-ttu-id="4b4f1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4f1-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b4f1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4f1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b4f1-129">INPUTS</span></span>

### <span data-ttu-id="4b4f1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4f1-130">System.String</span></span>

## <span data-ttu-id="4b4f1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b4f1-131">OUTPUTS</span></span>

### <span data-ttu-id="4b4f1-132">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4b4f1-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4b4f1-133">Note</span><span class="sxs-lookup"><span data-stu-id="4b4f1-133">NOTES</span></span>

## <span data-ttu-id="4b4f1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b4f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b4f1-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4b4f1-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="4b4f1-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4b4f1-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="4b4f1-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4b4f1-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

