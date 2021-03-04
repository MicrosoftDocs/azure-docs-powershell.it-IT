---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: b3cd900760821765d135810acaaafdeac45c0eb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007582"
---
# <span data-ttu-id="1dbf0-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1dbf0-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="1dbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbf0-103">Crea un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1dbf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dbf0-104">SYNTAX</span></span>

### <span data-ttu-id="1dbf0-105">SyncDatabaseDatabaseDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dbf0-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbf0-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="1dbf0-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbf0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dbf0-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbf0-108">Il cmdlet **New-AzSqlSyncAgent** crea un agente di sincronizzazione SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1dbf0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dbf0-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbf0-110">Esempio 1: Creare un agente di sincronizzazione per un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="1dbf0-111">Questo comando crea un agente di sincronizzazione per un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="1dbf0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbf0-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbf0-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbf0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1dbf0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dbf0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1dbf0-115">-Name</span></span>
<span data-ttu-id="1dbf0-116">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="1dbf0-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dbf0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1dbf0-119">-ServerName</span></span>
<span data-ttu-id="1dbf0-120">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1dbf0-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dbf0-121">-SyncDatabaseName</span></span>
<span data-ttu-id="1dbf0-122">Database usato per archiviare metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbf0-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="1dbf0-124">Gruppo di risorse a cui appartiene il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="1dbf0-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="1dbf0-126">ID risorsa del database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="1dbf0-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="1dbf0-128">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dbf0-129">-Confirm</span></span>
<span data-ttu-id="1dbf0-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbf0-131">-WhatIf</span></span>
<span data-ttu-id="1dbf0-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbf0-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbf0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbf0-134">CommonParameters</span></span>
<span data-ttu-id="1dbf0-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbf0-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dbf0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbf0-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dbf0-137">INPUTS</span></span>

### <span data-ttu-id="1dbf0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbf0-138">System.String</span></span>

## <span data-ttu-id="1dbf0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dbf0-139">OUTPUTS</span></span>

### <span data-ttu-id="1dbf0-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="1dbf0-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="1dbf0-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dbf0-141">NOTES</span></span>

## <span data-ttu-id="1dbf0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dbf0-142">RELATED LINKS</span></span>

[<span data-ttu-id="1dbf0-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1dbf0-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="1dbf0-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1dbf0-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

