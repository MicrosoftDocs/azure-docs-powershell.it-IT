---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: fcf973b31312fc525d7a1ae0c2bef84072b0cf9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970189"
---
# <span data-ttu-id="0de0d-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0de0d-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="0de0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0de0d-103">Crea un gruppo di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="0de0d-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0de0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0de0d-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de0d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0de0d-105">DESCRIPTION</span></span>
<span data-ttu-id="0de0d-106">Il cmdlet **New-AzSqlSyncGroup** crea un gruppo di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="0de0d-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0de0d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0de0d-107">EXAMPLES</span></span>

### <span data-ttu-id="0de0d-108">Esempio 1: Creare un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0de0d-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="0de0d-109">Questo comando crea un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0de0d-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="0de0d-110">"schema.js"è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="0de0d-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="0de0d-111">Contiene il payload dello schema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="0de0d-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="0de0d-112">Un esempio del json dello schema è: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="0de0d-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="0de0d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0de0d-113">PARAMETERS</span></span>

### <span data-ttu-id="0de0d-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0de0d-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0de0d-115">Criterio per la risoluzione dei conflitti tra il database hub e quello membro nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de0d-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="0de0d-116">-DatabaseCredential</span></span>
<span data-ttu-id="0de0d-117">Le SQL di autenticazione del database hub.</span><span class="sxs-lookup"><span data-stu-id="0de0d-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="0de0d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0de0d-118">-DatabaseName</span></span>
<span data-ttu-id="0de0d-119">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0de0d-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0de0d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de0d-120">-DefaultProfile</span></span>
<span data-ttu-id="0de0d-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0de0d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0de0d-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0de0d-122">-IntervalInSeconds</span></span>
<span data-ttu-id="0de0d-123">Frequenza (in secondi) dell'operazione di sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0de0d-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="0de0d-124">Il valore predefinito è -1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0de0d-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="0de0d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0de0d-125">-Name</span></span>
<span data-ttu-id="0de0d-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-126">The sync group name.</span></span>

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

### <span data-ttu-id="0de0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0de0d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0de0d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0de0d-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="0de0d-129">-SchemaFile</span></span>
<span data-ttu-id="0de0d-130">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="0de0d-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="0de0d-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0de0d-131">-ServerName</span></span>
<span data-ttu-id="0de0d-132">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0de0d-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0de0d-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0de0d-133">-SyncDatabaseName</span></span>
<span data-ttu-id="0de0d-134">Database usato per archiviare metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de0d-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de0d-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="0de0d-136">Gruppo di risorse a cui appartiene il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de0d-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="0de0d-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="0de0d-138">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de0d-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0de0d-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="0de0d-140">Usare una connessione di collegamento privato quando ci si connette all'hub di questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0de0d-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="0de0d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0de0d-141">-Confirm</span></span>
<span data-ttu-id="0de0d-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de0d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de0d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de0d-143">-WhatIf</span></span>
<span data-ttu-id="0de0d-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0de0d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de0d-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0de0d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de0d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de0d-146">CommonParameters</span></span>
<span data-ttu-id="0de0d-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de0d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de0d-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0de0d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de0d-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="0de0d-149">INPUTS</span></span>

### <span data-ttu-id="0de0d-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0de0d-150">System.String</span></span>

## <span data-ttu-id="0de0d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0de0d-151">OUTPUTS</span></span>

### <span data-ttu-id="0de0d-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0de0d-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0de0d-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="0de0d-153">NOTES</span></span>

## <span data-ttu-id="0de0d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0de0d-154">RELATED LINKS</span></span>

[<span data-ttu-id="0de0d-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0de0d-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="0de0d-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0de0d-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="0de0d-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0de0d-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

