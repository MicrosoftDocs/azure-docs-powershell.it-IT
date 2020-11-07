---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857357"
---
# <span data-ttu-id="e3591-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3591-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="e3591-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3591-102">SYNOPSIS</span></span>
<span data-ttu-id="e3591-103">Crea un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e3591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3591-104">SYNTAX</span></span>

### <span data-ttu-id="e3591-105">AzureSqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3591-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3591-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="e3591-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3591-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="e3591-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3591-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3591-108">DESCRIPTION</span></span>
<span data-ttu-id="e3591-109">Il cmdlet **New-AzSqlSyncMember** crea un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e3591-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3591-110">EXAMPLES</span></span>

### <span data-ttu-id="e3591-111">Esempio 1: creare un membro di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="e3591-112">Questo comando crea un membro di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="e3591-113">Esempio 2: creare un membro di sincronizzazione per un database di SQL Server locale</span><span class="sxs-lookup"><span data-stu-id="e3591-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="e3591-114">Questo comando crea un membro di sincronizzazione per un database SQL locale.</span><span class="sxs-lookup"><span data-stu-id="e3591-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="e3591-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3591-115">PARAMETERS</span></span>

### <span data-ttu-id="e3591-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3591-116">-DatabaseName</span></span>
<span data-ttu-id="e3591-117">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e3591-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3591-118">-DefaultProfile</span></span>
<span data-ttu-id="e3591-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e3591-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3591-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e3591-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="e3591-121">Credenziali (nome utente e password) del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3591-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e3591-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3591-122">-MemberDatabaseName</span></span>
<span data-ttu-id="e3591-123">Nome del database SQL di Azure del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="e3591-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="e3591-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="e3591-124">-MemberDatabaseType</span></span>
<span data-ttu-id="e3591-125">Tipo di database del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="e3591-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="e3591-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="e3591-126">-MemberServerName</span></span>
<span data-ttu-id="e3591-127">Nome di Azure SQL Server del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="e3591-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="e3591-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3591-128">-Name</span></span>
<span data-ttu-id="e3591-129">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-129">The sync member name.</span></span>

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

### <span data-ttu-id="e3591-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3591-130">-ResourceGroupName</span></span>
<span data-ttu-id="e3591-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3591-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3591-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e3591-132">-ServerName</span></span>
<span data-ttu-id="e3591-133">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e3591-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e3591-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e3591-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="e3591-135">ID del database di SQL Server connesso dall'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="e3591-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="e3591-136">-SyncAgentName</span></span>
<span data-ttu-id="e3591-137">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="e3591-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3591-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="e3591-139">Nome del gruppo di risorse in cui è in corso l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="e3591-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="e3591-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="e3591-141">ID risorsa dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="e3591-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="e3591-142">-SyncAgentServerName</span></span>
<span data-ttu-id="e3591-143">Nome di Azure SQL Server in cui è in corso l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="e3591-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="e3591-144">-SyncDirection</span></span>
<span data-ttu-id="e3591-145">Direzione di sincronizzazione di questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="e3591-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e3591-146">-SyncGroupName</span></span>
<span data-ttu-id="e3591-147">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3591-147">The sync group name.</span></span>

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

### <span data-ttu-id="e3591-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3591-148">-Confirm</span></span>
<span data-ttu-id="e3591-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3591-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3591-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3591-150">-WhatIf</span></span>
<span data-ttu-id="e3591-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3591-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3591-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3591-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3591-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3591-153">CommonParameters</span></span>
<span data-ttu-id="e3591-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3591-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3591-155">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3591-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3591-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3591-156">INPUTS</span></span>

### <span data-ttu-id="e3591-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e3591-157">System.String</span></span>

## <span data-ttu-id="e3591-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3591-158">OUTPUTS</span></span>

### <span data-ttu-id="e3591-159">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e3591-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e3591-160">Note</span><span class="sxs-lookup"><span data-stu-id="e3591-160">NOTES</span></span>

## <span data-ttu-id="e3591-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3591-161">RELATED LINKS</span></span>

[<span data-ttu-id="e3591-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3591-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="e3591-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3591-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="e3591-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e3591-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

