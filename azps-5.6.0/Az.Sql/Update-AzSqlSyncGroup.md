---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: c95b6a7a42327b7380e19ff333453f956797dcdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008350"
---
# <span data-ttu-id="4c9a8-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4c9a8-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="4c9a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9a8-103">Aggiorna un gruppo di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4c9a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c9a8-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c9a8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c9a8-105">DESCRIPTION</span></span>
<span data-ttu-id="4c9a8-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un gruppo di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4c9a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c9a8-107">EXAMPLES</span></span>

### <span data-ttu-id="4c9a8-108">Esempio 1: Aggiornare un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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
```

<span data-ttu-id="4c9a8-109">Questo comando aggiorna un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="4c9a8-110">"schema.js"è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="4c9a8-111">Contiene il payload dello schema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="4c9a8-112">Un esempio del json dello schema è: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="4c9a8-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="4c9a8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c9a8-113">PARAMETERS</span></span>

### <span data-ttu-id="4c9a8-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="4c9a8-114">-DatabaseCredential</span></span>
<span data-ttu-id="4c9a8-115">Le SQL di autenticazione del database hub.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="4c9a8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c9a8-116">-DatabaseName</span></span>
<span data-ttu-id="4c9a8-117">SQL nome del database.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-117">SQL Database name.</span></span>

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

### <span data-ttu-id="4c9a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9a8-118">-DefaultProfile</span></span>
<span data-ttu-id="4c9a8-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c9a8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c9a8-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4c9a8-120">-IntervalInSeconds</span></span>
<span data-ttu-id="4c9a8-121">Frequenza (in secondi) dell'operazione di sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="4c9a8-122">Il valore predefinito è -1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4c9a8-123">-Name</span></span>
<span data-ttu-id="4c9a8-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9a8-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c9a8-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c9a8-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="4c9a8-127">-SchemaFile</span></span>
<span data-ttu-id="4c9a8-128">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="4c9a8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c9a8-129">-ServerName</span></span>
<span data-ttu-id="4c9a8-130">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4c9a8-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4c9a8-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="4c9a8-132">Se usare una connessione di collegamento privato durante la connessione all'hub del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c9a8-133">-Confirm</span></span>
<span data-ttu-id="4c9a8-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c9a8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9a8-135">-WhatIf</span></span>
<span data-ttu-id="4c9a8-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9a8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c9a8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9a8-138">CommonParameters</span></span>
<span data-ttu-id="4c9a8-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9a8-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c9a8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9a8-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c9a8-141">INPUTS</span></span>

### <span data-ttu-id="4c9a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4c9a8-142">System.String</span></span>

## <span data-ttu-id="4c9a8-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c9a8-143">OUTPUTS</span></span>

### <span data-ttu-id="4c9a8-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4c9a8-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4c9a8-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c9a8-145">NOTES</span></span>

## <span data-ttu-id="4c9a8-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c9a8-146">RELATED LINKS</span></span>

[<span data-ttu-id="4c9a8-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4c9a8-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="4c9a8-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4c9a8-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="4c9a8-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4c9a8-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

