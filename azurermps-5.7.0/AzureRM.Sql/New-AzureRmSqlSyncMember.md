---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517863"
---
# <span data-ttu-id="4397f-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4397f-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="4397f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4397f-102">SYNOPSIS</span></span>
<span data-ttu-id="4397f-103">Crea un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4397f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4397f-104">SYNTAX</span></span>

### <span data-ttu-id="4397f-105">AzureSqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4397f-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4397f-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="4397f-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4397f-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="4397f-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4397f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4397f-108">DESCRIPTION</span></span>
<span data-ttu-id="4397f-109">Il cmdlet **New-AzureRmSqlSyncMember** crea un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="4397f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4397f-110">EXAMPLES</span></span>

### <span data-ttu-id="4397f-111">Esempio 1: creare un membro di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="4397f-112">Questo comando crea un membro di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="4397f-113">Esempio 2: creare un membro di sincronizzazione per un database di SQL Server locale</span><span class="sxs-lookup"><span data-stu-id="4397f-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="4397f-114">Questo comando crea un membro di sincronizzazione per un database SQL locale.</span><span class="sxs-lookup"><span data-stu-id="4397f-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="4397f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4397f-115">PARAMETERS</span></span>

### <span data-ttu-id="4397f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4397f-116">-DatabaseName</span></span>
<span data-ttu-id="4397f-117">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4397f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4397f-118">-DefaultProfile</span></span>
<span data-ttu-id="4397f-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4397f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4397f-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="4397f-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="4397f-121">Credenziali (nome utente e password) del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4397f-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4397f-122">-MemberDatabaseName</span></span>
<span data-ttu-id="4397f-123">Nome del database SQL di Azure del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="4397f-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="4397f-124">-MemberDatabaseType</span></span>
<span data-ttu-id="4397f-125">Tipo di database del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="4397f-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="4397f-126">-MemberServerName</span></span>
<span data-ttu-id="4397f-127">Nome di Azure SQL Server del database dei membri.</span><span class="sxs-lookup"><span data-stu-id="4397f-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4397f-128">-Name</span></span>
<span data-ttu-id="4397f-129">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4397f-130">-ResourceGroupName</span></span>
<span data-ttu-id="4397f-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4397f-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4397f-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4397f-132">-ServerName</span></span>
<span data-ttu-id="4397f-133">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4397f-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4397f-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="4397f-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="4397f-135">ID del database di SQL Server connesso dall'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="4397f-136">-SyncAgentName</span></span>
<span data-ttu-id="4397f-137">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4397f-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="4397f-139">Nome del gruppo di risorse in cui è in corso l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="4397f-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="4397f-141">ID risorsa dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="4397f-142">-SyncAgentServerName</span></span>
<span data-ttu-id="4397f-143">Nome di Azure SQL Server in cui è in corso l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="4397f-144">-SyncDirection</span></span>
<span data-ttu-id="4397f-145">Direzione di sincronizzazione di questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4397f-146">-SyncGroupName</span></span>
<span data-ttu-id="4397f-147">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4397f-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4397f-148">-Confirm</span></span>
<span data-ttu-id="4397f-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4397f-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4397f-150">-WhatIf</span></span>
<span data-ttu-id="4397f-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4397f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4397f-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4397f-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4397f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4397f-153">CommonParameters</span></span>
<span data-ttu-id="4397f-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4397f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4397f-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4397f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4397f-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4397f-156">INPUTS</span></span>

### <span data-ttu-id="4397f-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4397f-157">None</span></span>
<span data-ttu-id="4397f-158">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4397f-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4397f-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4397f-159">OUTPUTS</span></span>

### <span data-ttu-id="4397f-160">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="4397f-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="4397f-161">Note</span><span class="sxs-lookup"><span data-stu-id="4397f-161">NOTES</span></span>

## <span data-ttu-id="4397f-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4397f-162">RELATED LINKS</span></span>

[<span data-ttu-id="4397f-163">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4397f-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="4397f-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4397f-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="4397f-165">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4397f-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

