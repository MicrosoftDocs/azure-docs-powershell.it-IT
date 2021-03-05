---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: c26cb74f1d9f9c30e63bb39ec7668216a5f3a297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961422"
---
# <span data-ttu-id="6cce1-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cce1-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="6cce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cce1-102">SYNOPSIS</span></span>
<span data-ttu-id="6cce1-103">Crea un membro di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6cce1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cce1-104">SYNTAX</span></span>

### <span data-ttu-id="6cce1-105">AzureSqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cce1-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cce1-106">OnPremisesDatabaseSyncAgentAgent</span><span class="sxs-lookup"><span data-stu-id="6cce1-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cce1-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="6cce1-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cce1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6cce1-108">DESCRIPTION</span></span>
<span data-ttu-id="6cce1-109">Il cmdlet **New-AzSqlSyncMember** crea un membro di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6cce1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cce1-110">EXAMPLES</span></span>

### <span data-ttu-id="6cce1-111">Esempio 1: Creare un membro di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
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
SyncState                   : UnProvisioned
```

<span data-ttu-id="6cce1-112">Questo comando crea un membro di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="6cce1-113">Esempio 2: Creare un membro di sincronizzazione per un database SQL Server locale</span><span class="sxs-lookup"><span data-stu-id="6cce1-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="6cce1-114">Questo comando crea un membro di sincronizzazione per un database SQL locale.</span><span class="sxs-lookup"><span data-stu-id="6cce1-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="6cce1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cce1-115">PARAMETERS</span></span>

### <span data-ttu-id="6cce1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cce1-116">-DatabaseName</span></span>
<span data-ttu-id="6cce1-117">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6cce1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cce1-118">-DefaultProfile</span></span>
<span data-ttu-id="6cce1-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6cce1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cce1-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6cce1-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="6cce1-121">Credenziali (nome utente e password) del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6cce1-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cce1-122">-MemberDatabaseName</span></span>
<span data-ttu-id="6cce1-123">Nome del SQL database di Azure del membro.</span><span class="sxs-lookup"><span data-stu-id="6cce1-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="6cce1-124">-MemberDatabaseType</span></span>
<span data-ttu-id="6cce1-125">Il tipo di database del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="6cce1-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="6cce1-126">-MemberServerName</span></span>
<span data-ttu-id="6cce1-127">Nome SQL Server Azure del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="6cce1-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6cce1-128">-Name</span></span>
<span data-ttu-id="6cce1-129">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce1-130">-ResourceGroupName</span></span>
<span data-ttu-id="6cce1-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cce1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cce1-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6cce1-132">-ServerName</span></span>
<span data-ttu-id="6cce1-133">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cce1-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6cce1-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="6cce1-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="6cce1-135">ID del database SQL server connesso dall'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="6cce1-136">-SyncAgentName</span></span>
<span data-ttu-id="6cce1-137">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce1-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="6cce1-139">Nome del gruppo di risorse in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="6cce1-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="6cce1-141">ID risorsa dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="6cce1-142">-SyncAgentServerName</span></span>
<span data-ttu-id="6cce1-143">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="6cce1-144">-SyncDirection</span></span>
<span data-ttu-id="6cce1-145">Direzione di sincronizzazione di questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce1-146">-SyncGroupName</span></span>
<span data-ttu-id="6cce1-147">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-147">The sync group name.</span></span>

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

### <span data-ttu-id="6cce1-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="6cce1-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="6cce1-149">ID della risorsa per il database dei membri di sincronizzazione, usato se UsePrivateLinkConnection è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="6cce1-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6cce1-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="6cce1-151">Usare una connessione di collegamento privato quando ci si connette a questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cce1-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce1-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cce1-152">-Confirm</span></span>
<span data-ttu-id="6cce1-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cce1-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cce1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cce1-154">-WhatIf</span></span>
<span data-ttu-id="6cce1-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cce1-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cce1-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cce1-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cce1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cce1-157">CommonParameters</span></span>
<span data-ttu-id="6cce1-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cce1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cce1-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6cce1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cce1-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="6cce1-160">INPUTS</span></span>

### <span data-ttu-id="6cce1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="6cce1-161">System.String</span></span>

## <span data-ttu-id="6cce1-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cce1-162">OUTPUTS</span></span>

### <span data-ttu-id="6cce1-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="6cce1-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6cce1-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="6cce1-164">NOTES</span></span>

## <span data-ttu-id="6cce1-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cce1-165">RELATED LINKS</span></span>

[<span data-ttu-id="6cce1-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cce1-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="6cce1-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cce1-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="6cce1-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cce1-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

