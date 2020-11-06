---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 3041d7a25ad87e6e2b9242043645a66219ac7e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517899"
---
# <span data-ttu-id="d61b9-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d61b9-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="d61b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d61b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d61b9-103">Restituisce informazioni sugli agenti di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d61b9-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d61b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d61b9-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d61b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d61b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d61b9-106">Il cmdlet **Get-AzureRmSqlSyncAgent** restituisce informazioni su uno o più agenti di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d61b9-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="d61b9-107">Specificare il nome di un agente di sincronizzazione per visualizzare le informazioni solo per l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d61b9-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="d61b9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d61b9-108">EXAMPLES</span></span>

### <span data-ttu-id="d61b9-109">Esempio 1: ottenere tutte le istanze dell'agente di sincronizzazione di Azure SQL assegnato a un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d61b9-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="d61b9-110">Questo comando consente di ottenere informazioni su tutti gli agenti di sincronizzazione SQL di Azure assegnati a un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d61b9-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="d61b9-111">Esempio 2: ottenere informazioni su un agente di sincronizzazione SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d61b9-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="d61b9-112">Questo comando ottiene informazioni sull'agente di sincronizzazione di database SQL di Azure con il nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="d61b9-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="d61b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d61b9-113">PARAMETERS</span></span>

### <span data-ttu-id="d61b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61b9-114">-DefaultProfile</span></span>
<span data-ttu-id="d61b9-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d61b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d61b9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d61b9-116">-Name</span></span>
<span data-ttu-id="d61b9-117">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d61b9-117">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="d61b9-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d61b9-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d61b9-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d61b9-120">-ServerName</span></span>
<span data-ttu-id="d61b9-121">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d61b9-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="d61b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61b9-122">CommonParameters</span></span>
<span data-ttu-id="d61b9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61b9-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61b9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61b9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d61b9-125">INPUTS</span></span>

### <span data-ttu-id="d61b9-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d61b9-126">None</span></span>
<span data-ttu-id="d61b9-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d61b9-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d61b9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d61b9-128">OUTPUTS</span></span>

### <span data-ttu-id="d61b9-129">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="d61b9-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="d61b9-130">Note</span><span class="sxs-lookup"><span data-stu-id="d61b9-130">NOTES</span></span>

## <span data-ttu-id="d61b9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d61b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="d61b9-132">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d61b9-132">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="d61b9-133">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="d61b9-133">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

