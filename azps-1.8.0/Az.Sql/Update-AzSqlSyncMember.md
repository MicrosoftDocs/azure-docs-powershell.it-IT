---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 76b7366dabc648dc7f5812aedcc7fef18437b68e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676671"
---
# <span data-ttu-id="107b1-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="107b1-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="107b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="107b1-102">SYNOPSIS</span></span>
<span data-ttu-id="107b1-103">Aggiorna un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="107b1-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="107b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="107b1-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="107b1-105">DESCRIPTION</span></span>
<span data-ttu-id="107b1-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="107b1-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="107b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="107b1-107">EXAMPLES</span></span>

### <span data-ttu-id="107b1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="107b1-108">Example 1</span></span>
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

<span data-ttu-id="107b1-109">Questo comando Reimposta la password di amministratore per il database dei membri.</span><span class="sxs-lookup"><span data-stu-id="107b1-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="107b1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="107b1-110">PARAMETERS</span></span>

### <span data-ttu-id="107b1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="107b1-111">-DatabaseName</span></span>
<span data-ttu-id="107b1-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="107b1-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="107b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107b1-113">-DefaultProfile</span></span>
<span data-ttu-id="107b1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="107b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="107b1-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="107b1-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="107b1-116">Credenziali (nome utente e password) del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="107b1-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107b1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="107b1-117">-Name</span></span>
<span data-ttu-id="107b1-118">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="107b1-118">The sync member name.</span></span>

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

### <span data-ttu-id="107b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="107b1-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="107b1-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="107b1-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="107b1-121">-ServerName</span></span>
<span data-ttu-id="107b1-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="107b1-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="107b1-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="107b1-123">-SyncGroupName</span></span>
<span data-ttu-id="107b1-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="107b1-124">The sync group name.</span></span>

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

### <span data-ttu-id="107b1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="107b1-125">-Confirm</span></span>
<span data-ttu-id="107b1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107b1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107b1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107b1-127">-WhatIf</span></span>
<span data-ttu-id="107b1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="107b1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107b1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="107b1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107b1-130">CommonParameters</span></span>
<span data-ttu-id="107b1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107b1-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="107b1-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107b1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="107b1-133">INPUTS</span></span>

### <span data-ttu-id="107b1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="107b1-134">System.String</span></span>

## <span data-ttu-id="107b1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="107b1-135">OUTPUTS</span></span>

### <span data-ttu-id="107b1-136">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="107b1-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="107b1-137">Note</span><span class="sxs-lookup"><span data-stu-id="107b1-137">NOTES</span></span>

## <span data-ttu-id="107b1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="107b1-138">RELATED LINKS</span></span>

[<span data-ttu-id="107b1-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="107b1-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="107b1-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="107b1-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="107b1-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="107b1-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

