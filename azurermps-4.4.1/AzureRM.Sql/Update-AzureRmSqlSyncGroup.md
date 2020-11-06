---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: a530a9e99c698ca6b827df94b1966e4df065790d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519088"
---
# <span data-ttu-id="ca7e5-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ca7e5-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="ca7e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7e5-103">Aggiorna un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca7e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca7e5-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca7e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca7e5-105">DESCRIPTION</span></span>
<span data-ttu-id="ca7e5-106">Il cmdlet **Update-AzureRmSqlSyncGroup** modifica le proprietà di un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="ca7e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca7e5-107">EXAMPLES</span></span>

### <span data-ttu-id="ca7e5-108">Esempio 1: aggiornare un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="ca7e5-109">Questo comando aggiorna un gruppo di sincronizzazione per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="ca7e5-110">"schema.json" è un file nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="ca7e5-111">Contiene il payload Shema in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="ca7e5-112">Un esempio di JSON dello schema è il seguente: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f"-7614-4644-ad07-afa832620b4bManualTestsm4column1 "}, {" QuotedName ":" b3ee3a7f "-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null}</span><span class="sxs-lookup"><span data-stu-id="ca7e5-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="ca7e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca7e5-113">PARAMETERS</span></span>

### <span data-ttu-id="ca7e5-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca7e5-114">-Confirm</span></span>
<span data-ttu-id="ca7e5-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca7e5-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ca7e5-116">-DatabaseCredential</span></span>
<span data-ttu-id="ca7e5-117">Credenziali di autenticazione SQL del database hub.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="ca7e5-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca7e5-118">-DatabaseName</span></span>
<span data-ttu-id="ca7e5-119">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-119">SQL Database name.</span></span>

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

### <span data-ttu-id="ca7e5-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ca7e5-120">-IntervalInSeconds</span></span>
<span data-ttu-id="ca7e5-121">Frequenza (in secondi) della sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="ca7e5-122">Il valore predefinito è-1, che indica che la sincronizzazione automatica non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="ca7e5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca7e5-123">-Name</span></span>
<span data-ttu-id="ca7e5-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-124">The sync group name.</span></span>

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

### <span data-ttu-id="ca7e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca7e5-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca7e5-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="ca7e5-127">-SchemaFile</span></span>
<span data-ttu-id="ca7e5-128">Percorso del file di schema.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="ca7e5-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ca7e5-129">-ServerName</span></span>
<span data-ttu-id="ca7e5-130">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ca7e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca7e5-131">-WhatIf</span></span>
<span data-ttu-id="ca7e5-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca7e5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca7e5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7e5-134">-DefaultProfile</span></span>
<span data-ttu-id="ca7e5-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca7e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7e5-136">CommonParameters</span></span>
<span data-ttu-id="ca7e5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca7e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7e5-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca7e5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7e5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca7e5-139">INPUTS</span></span>

## <span data-ttu-id="ca7e5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca7e5-140">OUTPUTS</span></span>

### <span data-ttu-id="ca7e5-141">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ca7e5-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ca7e5-142">Note</span><span class="sxs-lookup"><span data-stu-id="ca7e5-142">NOTES</span></span>

## <span data-ttu-id="ca7e5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca7e5-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca7e5-144">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ca7e5-144">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="ca7e5-145">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ca7e5-145">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="ca7e5-146">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ca7e5-146">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

