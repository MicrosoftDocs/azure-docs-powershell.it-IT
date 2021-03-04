---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 08248056ec98d79e00f2c606870e21af495310f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959357"
---
# <span data-ttu-id="44f2d-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="44f2d-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="44f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="44f2d-103">Restituisce informazioni sugli agenti di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44f2d-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="44f2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44f2d-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44f2d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="44f2d-106">Il cmdlet **Get-AzSqlSyncAgent** restituisce informazioni su uno o più agenti di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44f2d-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="44f2d-107">Specificare il nome di un agente di sincronizzazione per visualizzare le informazioni solo per tale agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="44f2d-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="44f2d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44f2d-108">EXAMPLES</span></span>

### <span data-ttu-id="44f2d-109">Esempio 1: Ottenere tutte le istanze dell'SQL di sincronizzazione di Azure assegnate a un SQL Server</span><span class="sxs-lookup"><span data-stu-id="44f2d-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="44f2d-110">Questo comando ottiene informazioni su tutti gli agenti di SQL azure e di sincronizzazione assegnati a un SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="44f2d-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="44f2d-111">Esempio 2: Ottenere informazioni su un agente di sincronizzazione SQL Azure</span><span class="sxs-lookup"><span data-stu-id="44f2d-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="44f2d-112">Questo comando ottiene informazioni sull'agente di SQL database di Azure con nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="44f2d-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="44f2d-113">Esempio 3: Ottenere tutte le istanze dell'SQL di sincronizzazione di Azure assegnate a un SQL Server Azure usando il filtro</span><span class="sxs-lookup"><span data-stu-id="44f2d-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="44f2d-114">Questo comando ottiene informazioni su tutti gli agenti di SQL azure SQL Server che iniziano con "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="44f2d-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="44f2d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44f2d-115">PARAMETERS</span></span>

### <span data-ttu-id="44f2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f2d-116">-DefaultProfile</span></span>
<span data-ttu-id="44f2d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="44f2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44f2d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="44f2d-118">-Name</span></span>
<span data-ttu-id="44f2d-119">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="44f2d-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="44f2d-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44f2d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="44f2d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="44f2d-122">-ServerName</span></span>
<span data-ttu-id="44f2d-123">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="44f2d-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="44f2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f2d-124">CommonParameters</span></span>
<span data-ttu-id="44f2d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f2d-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44f2d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f2d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="44f2d-127">INPUTS</span></span>

### <span data-ttu-id="44f2d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="44f2d-128">System.String</span></span>

## <span data-ttu-id="44f2d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44f2d-129">OUTPUTS</span></span>

### <span data-ttu-id="44f2d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="44f2d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="44f2d-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="44f2d-131">NOTES</span></span>

## <span data-ttu-id="44f2d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44f2d-132">RELATED LINKS</span></span>

[<span data-ttu-id="44f2d-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="44f2d-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="44f2d-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="44f2d-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

