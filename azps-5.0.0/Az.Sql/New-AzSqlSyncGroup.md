---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200113"
---
# <span data-ttu-id="4a92a-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4a92a-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="4a92a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a92a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a92a-103">Crea un gruppo di sincronizzazione database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a92a-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4a92a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a92a-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a92a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a92a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a92a-106">Il cmdlet **New-AzSqlSyncGroup** crea un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a92a-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="4a92a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a92a-107">EXAMPLES</span></span>

### <span data-ttu-id="4a92a-108">Esempio 1: creare un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a92a-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="4a92a-109">Questo comando crea un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a92a-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="4a92a-110">"schema.json" è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="4a92a-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="4a92a-111">Contiene il payload dello schema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="4a92a-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="4a92a-112">Un esempio di JSON dello schema è il seguente: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f"-7614-4644-ad07-afa832620b4bManualTestsm4column1 "}, {" QuotedName ":" b3ee3a7f "-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="4a92a-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="4a92a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a92a-113">PARAMETERS</span></span>

### <span data-ttu-id="4a92a-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a92a-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="4a92a-115">Criteri per la risoluzione dei conflitti tra hub e database membro nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="4a92a-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="4a92a-116">-DatabaseCredential</span></span>
<span data-ttu-id="4a92a-117">Credenziali di autenticazione SQL del database hub.</span><span class="sxs-lookup"><span data-stu-id="4a92a-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="4a92a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a92a-118">-DatabaseName</span></span>
<span data-ttu-id="4a92a-119">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a92a-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4a92a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a92a-120">-DefaultProfile</span></span>
<span data-ttu-id="4a92a-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a92a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a92a-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4a92a-122">-IntervalInSeconds</span></span>
<span data-ttu-id="4a92a-123">Frequenza (in secondi) della sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4a92a-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="4a92a-124">Il valore predefinito è-1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="4a92a-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="4a92a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a92a-125">-Name</span></span>
<span data-ttu-id="4a92a-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-126">The sync group name.</span></span>

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

### <span data-ttu-id="4a92a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a92a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a92a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a92a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a92a-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="4a92a-129">-SchemaFile</span></span>
<span data-ttu-id="4a92a-130">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="4a92a-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="4a92a-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4a92a-131">-ServerName</span></span>
<span data-ttu-id="4a92a-132">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a92a-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4a92a-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a92a-133">-SyncDatabaseName</span></span>
<span data-ttu-id="4a92a-134">Database usato per archiviare i metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="4a92a-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a92a-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="4a92a-136">Il gruppo di risorse a cui appartiene il database di metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="4a92a-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="4a92a-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="4a92a-138">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="4a92a-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4a92a-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="4a92a-140">Usare una connessione di collegamento privato quando si esegue la connessione all'hub di questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a92a-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="4a92a-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a92a-141">-Confirm</span></span>
<span data-ttu-id="4a92a-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a92a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a92a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a92a-143">-WhatIf</span></span>
<span data-ttu-id="4a92a-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a92a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a92a-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a92a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a92a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a92a-146">CommonParameters</span></span>
<span data-ttu-id="4a92a-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a92a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a92a-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a92a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a92a-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a92a-149">INPUTS</span></span>

### <span data-ttu-id="4a92a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4a92a-150">System.String</span></span>

## <span data-ttu-id="4a92a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a92a-151">OUTPUTS</span></span>

### <span data-ttu-id="4a92a-152">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4a92a-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4a92a-153">Note</span><span class="sxs-lookup"><span data-stu-id="4a92a-153">NOTES</span></span>

## <span data-ttu-id="4a92a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a92a-154">RELATED LINKS</span></span>

[<span data-ttu-id="4a92a-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4a92a-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="4a92a-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4a92a-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="4a92a-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4a92a-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

