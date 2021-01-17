---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374790"
---
# <span data-ttu-id="ff298-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ff298-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="ff298-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff298-102">SYNOPSIS</span></span>
<span data-ttu-id="ff298-103">Restituisce informazioni sugli agenti di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ff298-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="ff298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff298-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff298-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff298-105">DESCRIPTION</span></span>
<span data-ttu-id="ff298-106">Il cmdlet **Get-AzSqlSyncAgent** restituisce informazioni su uno o più agenti di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff298-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="ff298-107">Specificare il nome di un agente di sincronizzazione per visualizzare le informazioni solo per l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff298-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="ff298-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff298-108">EXAMPLES</span></span>

### <span data-ttu-id="ff298-109">Esempio 1: ottenere tutte le istanze dell'agente di sincronizzazione di Azure SQL assegnato a un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ff298-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="ff298-110">Questo comando consente di ottenere informazioni su tutti gli agenti di sincronizzazione SQL di Azure assegnati a un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff298-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="ff298-111">Esempio 2: ottenere informazioni su un agente di sincronizzazione SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ff298-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="ff298-112">Questo comando ottiene informazioni sull'agente di sincronizzazione di database SQL di Azure con il nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="ff298-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="ff298-113">Esempio 3: ottenere tutte le istanze dell'agente di sincronizzazione di Azure SQL assegnate a un server SQL di Azure usando il filtro</span><span class="sxs-lookup"><span data-stu-id="ff298-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="ff298-114">Questo comando consente di ottenere informazioni su tutti gli agenti di sincronizzazione SQL di Azure assegnati a un server SQL di Azure che inizia con "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="ff298-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="ff298-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff298-115">PARAMETERS</span></span>

### <span data-ttu-id="ff298-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff298-116">-DefaultProfile</span></span>
<span data-ttu-id="ff298-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ff298-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff298-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff298-118">-Name</span></span>
<span data-ttu-id="ff298-119">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff298-119">The sync agent name.</span></span>

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

### <span data-ttu-id="ff298-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff298-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff298-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff298-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff298-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ff298-122">-ServerName</span></span>
<span data-ttu-id="ff298-123">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff298-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="ff298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff298-124">CommonParameters</span></span>
<span data-ttu-id="ff298-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff298-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff298-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff298-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff298-127">INPUTS</span></span>

### <span data-ttu-id="ff298-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ff298-128">System.String</span></span>

## <span data-ttu-id="ff298-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff298-129">OUTPUTS</span></span>

### <span data-ttu-id="ff298-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="ff298-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="ff298-131">Note</span><span class="sxs-lookup"><span data-stu-id="ff298-131">NOTES</span></span>

## <span data-ttu-id="ff298-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff298-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff298-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ff298-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="ff298-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="ff298-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

