---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193137"
---
# <span data-ttu-id="b2e9d-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2e9d-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="b2e9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e9d-103">Aggiorna un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b2e9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2e9d-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e9d-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b2e9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2e9d-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e9d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2e9d-108">Example 1</span></span>
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

<span data-ttu-id="b2e9d-109">Questo comando Reimposta la password di amministratore per il database dei membri.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="b2e9d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2e9d-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e9d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2e9d-111">-DatabaseName</span></span>
<span data-ttu-id="b2e9d-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b2e9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e9d-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e9d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2e9d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2e9d-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="b2e9d-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="b2e9d-116">Credenziali (nome utente e password) del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b2e9d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2e9d-117">-Name</span></span>
<span data-ttu-id="b2e9d-118">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-118">The sync member name.</span></span>

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

### <span data-ttu-id="b2e9d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e9d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2e9d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2e9d-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b2e9d-121">-ServerName</span></span>
<span data-ttu-id="b2e9d-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b2e9d-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e9d-123">-SyncGroupName</span></span>
<span data-ttu-id="b2e9d-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-124">The sync group name.</span></span>

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

### <span data-ttu-id="b2e9d-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="b2e9d-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="b2e9d-126">ID risorsa per il database del membro di sincronizzazione, usato se UsePrivateLinkConnection è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="b2e9d-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="b2e9d-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="b2e9d-128">Se usare il collegamento privato quando si esegue la connessione a questo membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-128">Whether to use private link when connecting to this sync member.</span></span>

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

### <span data-ttu-id="b2e9d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2e9d-129">-Confirm</span></span>
<span data-ttu-id="b2e9d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e9d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e9d-131">-WhatIf</span></span>
<span data-ttu-id="b2e9d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e9d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e9d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e9d-134">CommonParameters</span></span>
<span data-ttu-id="b2e9d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e9d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e9d-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2e9d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e9d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2e9d-137">INPUTS</span></span>

### <span data-ttu-id="b2e9d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e9d-138">System.String</span></span>

## <span data-ttu-id="b2e9d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2e9d-139">OUTPUTS</span></span>

### <span data-ttu-id="b2e9d-140">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="b2e9d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="b2e9d-141">Note</span><span class="sxs-lookup"><span data-stu-id="b2e9d-141">NOTES</span></span>

## <span data-ttu-id="b2e9d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2e9d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2e9d-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2e9d-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="b2e9d-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2e9d-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="b2e9d-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2e9d-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)
