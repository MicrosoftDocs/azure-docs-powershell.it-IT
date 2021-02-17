---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187942"
---
# <span data-ttu-id="422e8-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="422e8-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="422e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="422e8-102">SYNOPSIS</span></span>
<span data-ttu-id="422e8-103">Aggiorna un membro di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="422e8-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="422e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="422e8-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="422e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="422e8-105">DESCRIPTION</span></span>
<span data-ttu-id="422e8-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un membro di sincronizzazione del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="422e8-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="422e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="422e8-107">EXAMPLES</span></span>

### <span data-ttu-id="422e8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="422e8-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="422e8-109">Questo comando reimposta la password dell'amministratore per il database dei membri.</span><span class="sxs-lookup"><span data-stu-id="422e8-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="422e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="422e8-110">PARAMETERS</span></span>

### <span data-ttu-id="422e8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="422e8-111">-DatabaseName</span></span>
<span data-ttu-id="422e8-112">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="422e8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="422e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422e8-113">-DefaultProfile</span></span>
<span data-ttu-id="422e8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="422e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="422e8-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="422e8-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="422e8-116">Le credenziali (nome utente e password) del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="422e8-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="422e8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="422e8-117">-Name</span></span>
<span data-ttu-id="422e8-118">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="422e8-118">The sync member name.</span></span>

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

### <span data-ttu-id="422e8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="422e8-119">-ResourceGroupName</span></span>
<span data-ttu-id="422e8-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="422e8-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="422e8-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="422e8-121">-ServerName</span></span>
<span data-ttu-id="422e8-122">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="422e8-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="422e8-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="422e8-123">-SyncGroupName</span></span>
<span data-ttu-id="422e8-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="422e8-124">The sync group name.</span></span>

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

### <span data-ttu-id="422e8-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="422e8-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="422e8-126">ID della risorsa per il database dei membri di sincronizzazione, usato se UsePrivateLinkConnection è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="422e8-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="422e8-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="422e8-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="422e8-128">Se usare un collegamento privato quando ci si connette a questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="422e8-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="422e8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="422e8-129">-Confirm</span></span>
<span data-ttu-id="422e8-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="422e8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="422e8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="422e8-131">-WhatIf</span></span>
<span data-ttu-id="422e8-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="422e8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="422e8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="422e8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="422e8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422e8-134">CommonParameters</span></span>
<span data-ttu-id="422e8-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="422e8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422e8-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="422e8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422e8-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="422e8-137">INPUTS</span></span>

### <span data-ttu-id="422e8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="422e8-138">System.String</span></span>

## <span data-ttu-id="422e8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="422e8-139">OUTPUTS</span></span>

### <span data-ttu-id="422e8-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="422e8-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="422e8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="422e8-141">NOTES</span></span>

## <span data-ttu-id="422e8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="422e8-142">RELATED LINKS</span></span>

[<span data-ttu-id="422e8-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="422e8-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="422e8-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="422e8-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="422e8-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="422e8-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

