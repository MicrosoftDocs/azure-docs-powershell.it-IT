---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 5846435df4921e425e12e908539849fda0bd2472
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405738"
---
# <span data-ttu-id="ecf56-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ecf56-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="ecf56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf56-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf56-103">Crea un membro di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ecf56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecf56-104">SYNTAX</span></span>

### <span data-ttu-id="ecf56-105">AzureSqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecf56-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf56-106">OnPremisesDatabaseSyncAgentAgent</span><span class="sxs-lookup"><span data-stu-id="ecf56-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf56-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ecf56-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf56-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecf56-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf56-109">Il cmdlet **New-AzSqlSyncMember** crea un membro di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ecf56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecf56-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf56-111">Esempio 1: Creare un membro di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="ecf56-112">Questo comando crea un membro di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="ecf56-113">Esempio 2: Creare un membro di sincronizzazione per un database SQL Server locale</span><span class="sxs-lookup"><span data-stu-id="ecf56-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="ecf56-114">Questo comando crea un membro di sincronizzazione per un database SQL locale.</span><span class="sxs-lookup"><span data-stu-id="ecf56-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="ecf56-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecf56-115">PARAMETERS</span></span>

### <span data-ttu-id="ecf56-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ecf56-116">-DatabaseName</span></span>
<span data-ttu-id="ecf56-117">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ecf56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf56-118">-DefaultProfile</span></span>
<span data-ttu-id="ecf56-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ecf56-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecf56-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ecf56-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ecf56-121">Le credenziali (nome utente e password) del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf56-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ecf56-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ecf56-122">-MemberDatabaseName</span></span>
<span data-ttu-id="ecf56-123">Nome del database SQL Azure del database membro.</span><span class="sxs-lookup"><span data-stu-id="ecf56-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="ecf56-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="ecf56-124">-MemberDatabaseType</span></span>
<span data-ttu-id="ecf56-125">Il tipo di database del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="ecf56-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="ecf56-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="ecf56-126">-MemberServerName</span></span>
<span data-ttu-id="ecf56-127">Nome SQL Server Azure del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="ecf56-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="ecf56-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ecf56-128">-Name</span></span>
<span data-ttu-id="ecf56-129">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-129">The sync member name.</span></span>

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

### <span data-ttu-id="ecf56-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf56-130">-ResourceGroupName</span></span>
<span data-ttu-id="ecf56-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ecf56-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecf56-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecf56-132">-ServerName</span></span>
<span data-ttu-id="ecf56-133">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ecf56-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ecf56-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ecf56-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="ecf56-135">ID del database SQL server connesso dall'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="ecf56-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="ecf56-136">-SyncAgentName</span></span>
<span data-ttu-id="ecf56-137">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="ecf56-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf56-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="ecf56-139">Nome del gruppo di risorse in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="ecf56-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ecf56-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="ecf56-141">ID risorsa dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="ecf56-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="ecf56-142">-SyncAgentServerName</span></span>
<span data-ttu-id="ecf56-143">Nome dell'agente di SQL Server Azure in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="ecf56-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="ecf56-144">-SyncDirection</span></span>
<span data-ttu-id="ecf56-145">Direzione di sincronizzazione di questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="ecf56-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf56-146">-SyncGroupName</span></span>
<span data-ttu-id="ecf56-147">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ecf56-147">The sync group name.</span></span>

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

### <span data-ttu-id="ecf56-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecf56-148">-Confirm</span></span>
<span data-ttu-id="ecf56-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf56-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf56-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf56-150">-WhatIf</span></span>
<span data-ttu-id="ecf56-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf56-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf56-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf56-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf56-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf56-153">CommonParameters</span></span>
<span data-ttu-id="ecf56-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf56-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf56-155">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecf56-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf56-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecf56-156">INPUTS</span></span>

### <span data-ttu-id="ecf56-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ecf56-157">System.String</span></span>

## <span data-ttu-id="ecf56-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecf56-158">OUTPUTS</span></span>

### <span data-ttu-id="ecf56-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ecf56-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ecf56-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecf56-160">NOTES</span></span>

## <span data-ttu-id="ecf56-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecf56-161">RELATED LINKS</span></span>

[<span data-ttu-id="ecf56-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ecf56-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="ecf56-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ecf56-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

