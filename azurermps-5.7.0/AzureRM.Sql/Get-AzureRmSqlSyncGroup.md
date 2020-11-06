---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 71a4d20c6296c8a9d725cb9a16960d6c4a06646c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512224"
---
# <span data-ttu-id="e57e5-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e57e5-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e57e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e57e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e57e5-103">Restituisce informazioni sui gruppi di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e57e5-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e57e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57e5-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e57e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e57e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e57e5-106">Il cmdlet **Get-AzureRmSqlSyncGroup** restituisce informazioni su uno o più gruppi di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e57e5-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="e57e5-107">Specificare il nome di un gruppo di sincronizzazione per visualizzare le informazioni solo per il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e57e5-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="e57e5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57e5-108">EXAMPLES</span></span>

### <span data-ttu-id="e57e5-109">Esempio 1: ottenere tutte le istanze del gruppo di sincronizzazione SQL di Azure assegnate a un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e57e5-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="e57e5-110">Questo comando consente di ottenere informazioni su tutti i gruppi di sincronizzazione di database SQL di Azure assegnati a un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e57e5-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="e57e5-111">Esempio 2: ottenere informazioni su un gruppo di sincronizzazione di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e57e5-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="e57e5-112">Questo comando ottiene le informazioni sul gruppo di sincronizzazione di database SQL di Azure con il nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="e57e5-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="e57e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e57e5-113">PARAMETERS</span></span>

### <span data-ttu-id="e57e5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e57e5-114">-DatabaseName</span></span>
<span data-ttu-id="e57e5-115">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e57e5-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e57e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57e5-116">-DefaultProfile</span></span>
<span data-ttu-id="e57e5-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e57e5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e57e5-118">-Name</span></span>
<span data-ttu-id="e57e5-119">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e57e5-119">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="e57e5-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e57e5-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e57e5-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e57e5-122">-ServerName</span></span>
<span data-ttu-id="e57e5-123">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e57e5-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e57e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57e5-124">CommonParameters</span></span>
<span data-ttu-id="e57e5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57e5-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57e5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e57e5-127">INPUTS</span></span>

### <span data-ttu-id="e57e5-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e57e5-128">None</span></span>
<span data-ttu-id="e57e5-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e57e5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e57e5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57e5-130">OUTPUTS</span></span>

### <span data-ttu-id="e57e5-131">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e57e5-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e57e5-132">Note</span><span class="sxs-lookup"><span data-stu-id="e57e5-132">NOTES</span></span>

## <span data-ttu-id="e57e5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="e57e5-134">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e57e5-134">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e57e5-135">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e57e5-135">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e57e5-136">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e57e5-136">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

