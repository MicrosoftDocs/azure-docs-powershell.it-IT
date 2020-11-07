---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 66e03a171e0140dc9f84ad0a9161bf0af5af9b4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676669"
---
# <span data-ttu-id="7e0f3-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7e0f3-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="7e0f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0f3-103">Aggiorna un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7e0f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e0f3-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e0f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e0f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0f3-106">Il cmdlet **Update-AzSqlSyncGroup** modifica le proprietà di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7e0f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e0f3-107">EXAMPLES</span></span>

### <span data-ttu-id="7e0f3-108">Esempio 1: aggiornare un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="7e0f3-109">Questo comando aggiorna un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="7e0f3-110">"schema.json" è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="7e0f3-111">Contiene il payload Shema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="7e0f3-112">Un esempio di JSON dello schema è il seguente: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f"-7614-4644-ad07-afa832620b4bManualTestsm4column1 "}, {" QuotedName ":" b3ee3a7f "-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="7e0f3-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="7e0f3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e0f3-113">PARAMETERS</span></span>

### <span data-ttu-id="7e0f3-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7e0f3-114">-DatabaseCredential</span></span>
<span data-ttu-id="7e0f3-115">Credenziali di autenticazione SQL del database hub.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="7e0f3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e0f3-116">-DatabaseName</span></span>
<span data-ttu-id="7e0f3-117">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-117">SQL Database name.</span></span>

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

### <span data-ttu-id="7e0f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0f3-118">-DefaultProfile</span></span>
<span data-ttu-id="7e0f3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7e0f3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e0f3-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7e0f3-120">-IntervalInSeconds</span></span>
<span data-ttu-id="7e0f3-121">Frequenza (in secondi) della sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="7e0f3-122">Il valore predefinito è-1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="7e0f3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e0f3-123">-Name</span></span>
<span data-ttu-id="7e0f3-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-124">The sync group name.</span></span>

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

### <span data-ttu-id="7e0f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e0f3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e0f3-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="7e0f3-127">-SchemaFile</span></span>
<span data-ttu-id="7e0f3-128">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="7e0f3-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7e0f3-129">-ServerName</span></span>
<span data-ttu-id="7e0f3-130">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7e0f3-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e0f3-131">-Confirm</span></span>
<span data-ttu-id="7e0f3-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e0f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0f3-133">-WhatIf</span></span>
<span data-ttu-id="7e0f3-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0f3-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e0f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0f3-136">CommonParameters</span></span>
<span data-ttu-id="7e0f3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0f3-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e0f3-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0f3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e0f3-139">INPUTS</span></span>

### <span data-ttu-id="7e0f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7e0f3-140">System.String</span></span>

## <span data-ttu-id="7e0f3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e0f3-141">OUTPUTS</span></span>

### <span data-ttu-id="7e0f3-142">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="7e0f3-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="7e0f3-143">Note</span><span class="sxs-lookup"><span data-stu-id="7e0f3-143">NOTES</span></span>

## <span data-ttu-id="7e0f3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e0f3-144">RELATED LINKS</span></span>

[<span data-ttu-id="7e0f3-145">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7e0f3-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="7e0f3-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7e0f3-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="7e0f3-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7e0f3-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
