---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332875"
---
# <span data-ttu-id="82950-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="82950-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="82950-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82950-102">SYNOPSIS</span></span>
<span data-ttu-id="82950-103">Aggiorna un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="82950-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="82950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82950-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82950-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82950-105">DESCRIPTION</span></span>
<span data-ttu-id="82950-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="82950-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="82950-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82950-107">EXAMPLES</span></span>

### <span data-ttu-id="82950-108">Esempio 1: aggiornare un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="82950-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="82950-109">Questo comando aggiorna un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="82950-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="82950-110">"schema.json" è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="82950-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="82950-111">Contiene il payload dello schema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="82950-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="82950-112">Un esempio di JSON dello schema è il seguente: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f"-7614-4644-ad07-afa832620b4bManualTestsm4column1 "}, {" QuotedName ":" b3ee3a7f "-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="82950-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="82950-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82950-113">PARAMETERS</span></span>

### <span data-ttu-id="82950-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="82950-114">-DatabaseCredential</span></span>
<span data-ttu-id="82950-115">Credenziali di autenticazione SQL del database hub.</span><span class="sxs-lookup"><span data-stu-id="82950-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="82950-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82950-116">-DatabaseName</span></span>
<span data-ttu-id="82950-117">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="82950-117">SQL Database name.</span></span>

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

### <span data-ttu-id="82950-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82950-118">-DefaultProfile</span></span>
<span data-ttu-id="82950-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="82950-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82950-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="82950-120">-IntervalInSeconds</span></span>
<span data-ttu-id="82950-121">Frequenza (in secondi) della sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="82950-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="82950-122">Il valore predefinito è-1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="82950-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="82950-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="82950-123">-Name</span></span>
<span data-ttu-id="82950-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="82950-124">The sync group name.</span></span>

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

### <span data-ttu-id="82950-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82950-125">-ResourceGroupName</span></span>
<span data-ttu-id="82950-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82950-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="82950-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="82950-127">-SchemaFile</span></span>
<span data-ttu-id="82950-128">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="82950-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="82950-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="82950-129">-ServerName</span></span>
<span data-ttu-id="82950-130">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="82950-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="82950-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="82950-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="82950-132">Se usare una connessione di collegamento privato quando si esegue la connessione all'hub di questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="82950-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="82950-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82950-133">-Confirm</span></span>
<span data-ttu-id="82950-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82950-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82950-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82950-135">-WhatIf</span></span>
<span data-ttu-id="82950-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82950-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82950-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82950-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82950-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82950-138">CommonParameters</span></span>
<span data-ttu-id="82950-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82950-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82950-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82950-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82950-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82950-141">INPUTS</span></span>

### <span data-ttu-id="82950-142">System. String</span><span class="sxs-lookup"><span data-stu-id="82950-142">System.String</span></span>

## <span data-ttu-id="82950-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82950-143">OUTPUTS</span></span>

### <span data-ttu-id="82950-144">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="82950-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="82950-145">Note</span><span class="sxs-lookup"><span data-stu-id="82950-145">NOTES</span></span>

## <span data-ttu-id="82950-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82950-146">RELATED LINKS</span></span>

[<span data-ttu-id="82950-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="82950-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="82950-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="82950-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="82950-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="82950-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

