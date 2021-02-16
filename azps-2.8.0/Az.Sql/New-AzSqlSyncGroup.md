---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: f89054dad3fa4c66f845e3cdd9a309563efa9e44
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398173"
---
# <span data-ttu-id="31e31-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="31e31-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="31e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e31-102">SYNOPSIS</span></span>
<span data-ttu-id="31e31-103">Crea un gruppo di sincronizzazione SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="31e31-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="31e31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31e31-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31e31-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31e31-105">DESCRIPTION</span></span>
<span data-ttu-id="31e31-106">Il cmdlet **New-AzSqlSyncGroup** crea un gruppo di SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="31e31-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="31e31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31e31-107">EXAMPLES</span></span>

### <span data-ttu-id="31e31-108">Esempio 1: Creare un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31e31-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="31e31-109">Questo comando crea un gruppo di sincronizzazione per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31e31-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="31e31-110">"schema.js"è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="31e31-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="31e31-111">Contiene il payload dello schema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="31e31-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="31e31-112">Un esempio del json dello schema è: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="31e31-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="31e31-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e31-113">PARAMETERS</span></span>

### <span data-ttu-id="31e31-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="31e31-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="31e31-115">Criterio per la risoluzione dei conflitti tra il database hub e quello membro nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="31e31-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="31e31-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="31e31-116">-DatabaseCredential</span></span>
<span data-ttu-id="31e31-117">L SQL credenziali di autenticazione del database hub.</span><span class="sxs-lookup"><span data-stu-id="31e31-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="31e31-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31e31-118">-DatabaseName</span></span>
<span data-ttu-id="31e31-119">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31e31-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="31e31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e31-120">-DefaultProfile</span></span>
<span data-ttu-id="31e31-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="31e31-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31e31-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="31e31-122">-IntervalInSeconds</span></span>
<span data-ttu-id="31e31-123">Frequenza (in secondi) dell'operazione di sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="31e31-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="31e31-124">Il valore predefinito è -1, ovvero la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="31e31-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="31e31-125">-Name</span><span class="sxs-lookup"><span data-stu-id="31e31-125">-Name</span></span>
<span data-ttu-id="31e31-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="31e31-126">The sync group name.</span></span>

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

### <span data-ttu-id="31e31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e31-127">-ResourceGroupName</span></span>
<span data-ttu-id="31e31-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31e31-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="31e31-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="31e31-129">-SchemaFile</span></span>
<span data-ttu-id="31e31-130">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="31e31-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="31e31-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31e31-131">-ServerName</span></span>
<span data-ttu-id="31e31-132">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31e31-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="31e31-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="31e31-133">-SyncDatabaseName</span></span>
<span data-ttu-id="31e31-134">Database usato per archiviare metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="31e31-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="31e31-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e31-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="31e31-136">Gruppo di risorse a cui appartiene il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="31e31-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="31e31-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="31e31-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="31e31-138">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="31e31-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="31e31-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31e31-139">-Confirm</span></span>
<span data-ttu-id="31e31-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e31-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e31-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e31-141">-WhatIf</span></span>
<span data-ttu-id="31e31-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e31-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e31-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e31-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e31-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e31-144">CommonParameters</span></span>
<span data-ttu-id="31e31-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e31-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e31-146">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31e31-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e31-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="31e31-147">INPUTS</span></span>

### <span data-ttu-id="31e31-148">System.String</span><span class="sxs-lookup"><span data-stu-id="31e31-148">System.String</span></span>

## <span data-ttu-id="31e31-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31e31-149">OUTPUTS</span></span>

### <span data-ttu-id="31e31-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="31e31-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="31e31-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="31e31-151">NOTES</span></span>

## <span data-ttu-id="31e31-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31e31-152">RELATED LINKS</span></span>


[<span data-ttu-id="31e31-153">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="31e31-153">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="31e31-154">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="31e31-154">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

