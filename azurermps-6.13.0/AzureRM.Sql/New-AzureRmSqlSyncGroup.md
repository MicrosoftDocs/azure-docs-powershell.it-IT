---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 9df59edf3b73597e639e49a13265468b495fe4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517340"
---
# <span data-ttu-id="647b9-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="647b9-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="647b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="647b9-102">SYNOPSIS</span></span>
<span data-ttu-id="647b9-103">Crea un gruppo di sincronizzazione database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647b9-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="647b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="647b9-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="647b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="647b9-105">DESCRIPTION</span></span>
<span data-ttu-id="647b9-106">Il cmdlet **New-AzureRmSqlSyncGroup** crea un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647b9-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="647b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="647b9-107">EXAMPLES</span></span>

### <span data-ttu-id="647b9-108">Esempio 1: creare un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647b9-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="647b9-109">Questo comando crea un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647b9-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="647b9-110">"schema.json" è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="647b9-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="647b9-111">Contiene il payload Shema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="647b9-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="647b9-112">Un esempio di JSON dello schema è il seguente: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f"-7614-4644-ad07-afa832620b4bManualTestsm4column1 "}, {" QuotedName ":" b3ee3a7f "-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="647b9-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="647b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="647b9-113">PARAMETERS</span></span>

### <span data-ttu-id="647b9-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="647b9-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="647b9-115">Criteri per la risoluzione dei conflitti tra hub e database membro nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="647b9-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="647b9-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="647b9-116">-DatabaseCredential</span></span>
<span data-ttu-id="647b9-117">Credenziali di autenticazione SQL del database hub.</span><span class="sxs-lookup"><span data-stu-id="647b9-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="647b9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="647b9-118">-DatabaseName</span></span>
<span data-ttu-id="647b9-119">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647b9-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="647b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647b9-120">-DefaultProfile</span></span>
<span data-ttu-id="647b9-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="647b9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="647b9-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="647b9-122">-IntervalInSeconds</span></span>
<span data-ttu-id="647b9-123">Frequenza (in secondi) della sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="647b9-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="647b9-124">Il valore predefinito è-1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="647b9-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="647b9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="647b9-125">-Name</span></span>
<span data-ttu-id="647b9-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="647b9-126">The sync group name.</span></span>

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

### <span data-ttu-id="647b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="647b9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="647b9-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="647b9-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="647b9-129">-SchemaFile</span></span>
<span data-ttu-id="647b9-130">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="647b9-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="647b9-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="647b9-131">-ServerName</span></span>
<span data-ttu-id="647b9-132">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="647b9-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="647b9-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="647b9-133">-SyncDatabaseName</span></span>
<span data-ttu-id="647b9-134">Database usato per archiviare i metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="647b9-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="647b9-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647b9-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="647b9-136">Il gruppo di risorse a cui appartiene il database di metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="647b9-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="647b9-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="647b9-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="647b9-138">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="647b9-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="647b9-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="647b9-139">-Confirm</span></span>
<span data-ttu-id="647b9-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="647b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="647b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647b9-141">-WhatIf</span></span>
<span data-ttu-id="647b9-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647b9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="647b9-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="647b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647b9-144">CommonParameters</span></span>
<span data-ttu-id="647b9-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647b9-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647b9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647b9-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="647b9-147">INPUTS</span></span>

### <span data-ttu-id="647b9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="647b9-148">System.String</span></span>

## <span data-ttu-id="647b9-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="647b9-149">OUTPUTS</span></span>

### <span data-ttu-id="647b9-150">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="647b9-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="647b9-151">Note</span><span class="sxs-lookup"><span data-stu-id="647b9-151">NOTES</span></span>

## <span data-ttu-id="647b9-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="647b9-152">RELATED LINKS</span></span>

[<span data-ttu-id="647b9-153">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="647b9-153">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="647b9-154">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="647b9-154">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="647b9-155">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="647b9-155">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

