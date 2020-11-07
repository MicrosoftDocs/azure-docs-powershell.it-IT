---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: f72091d142b57cc7ef3897eceda2219634376daf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686555"
---
# <span data-ttu-id="22324-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22324-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="22324-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22324-102">SYNOPSIS</span></span>
<span data-ttu-id="22324-103">Aggiorna un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="22324-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22324-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22324-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22324-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22324-105">DESCRIPTION</span></span>
<span data-ttu-id="22324-106">Il cmdlet **Update-AzureRmSqlSyncGroup** modifica le proprietà di un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="22324-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="22324-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22324-107">EXAMPLES</span></span>

### <span data-ttu-id="22324-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22324-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="22324-109">Questo comando Reimposta la password di amministratore per il database dei membri.</span><span class="sxs-lookup"><span data-stu-id="22324-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="22324-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22324-110">PARAMETERS</span></span>

### <span data-ttu-id="22324-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22324-111">-Confirm</span></span>
<span data-ttu-id="22324-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22324-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22324-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22324-113">-DatabaseName</span></span>
<span data-ttu-id="22324-114">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="22324-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="22324-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="22324-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="22324-116">Credenziali (nome utente e password) del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="22324-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="22324-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="22324-117">-Name</span></span>
<span data-ttu-id="22324-118">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="22324-118">The sync member name.</span></span>

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

### <span data-ttu-id="22324-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22324-119">-ResourceGroupName</span></span>
<span data-ttu-id="22324-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22324-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="22324-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="22324-121">-ServerName</span></span>
<span data-ttu-id="22324-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22324-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="22324-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="22324-123">-SyncGroupName</span></span>
<span data-ttu-id="22324-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="22324-124">The sync group name.</span></span>

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

### <span data-ttu-id="22324-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22324-125">-WhatIf</span></span>
<span data-ttu-id="22324-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22324-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22324-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22324-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22324-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22324-128">-DefaultProfile</span></span>
<span data-ttu-id="22324-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22324-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22324-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22324-130">CommonParameters</span></span>
<span data-ttu-id="22324-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22324-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22324-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22324-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22324-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22324-133">INPUTS</span></span>

## <span data-ttu-id="22324-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22324-134">OUTPUTS</span></span>

### <span data-ttu-id="22324-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="22324-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="22324-136">Note</span><span class="sxs-lookup"><span data-stu-id="22324-136">NOTES</span></span>

## <span data-ttu-id="22324-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22324-137">RELATED LINKS</span></span>

[<span data-ttu-id="22324-138">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22324-138">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="22324-139">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22324-139">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="22324-140">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22324-140">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

