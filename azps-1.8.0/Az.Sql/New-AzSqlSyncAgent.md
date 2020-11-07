---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: a8e890bfa9c839c97ddc3d0f002782fdc0b4f2e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676834"
---
# <span data-ttu-id="b7a90-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b7a90-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="b7a90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7a90-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a90-103">Crea un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a90-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b7a90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7a90-104">SYNTAX</span></span>

### <span data-ttu-id="b7a90-105">SyncDatabaseComponent (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7a90-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a90-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b7a90-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a90-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a90-107">DESCRIPTION</span></span>
<span data-ttu-id="b7a90-108">Il cmdlet **New-AzSqlSyncAgent** crea un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a90-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b7a90-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7a90-109">EXAMPLES</span></span>

### <span data-ttu-id="b7a90-110">Esempio 1: creare un agente di sincronizzazione per un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a90-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="b7a90-111">Questo comando crea un agente di sincronizzazione per un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a90-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="b7a90-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7a90-112">PARAMETERS</span></span>

### <span data-ttu-id="b7a90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a90-113">-DefaultProfile</span></span>
<span data-ttu-id="b7a90-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7a90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7a90-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7a90-115">-Name</span></span>
<span data-ttu-id="b7a90-116">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a90-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7a90-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7a90-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7a90-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b7a90-119">-ServerName</span></span>
<span data-ttu-id="b7a90-120">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b7a90-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7a90-121">-SyncDatabaseName</span></span>
<span data-ttu-id="b7a90-122">Database usato per archiviare i metadati correlati alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a90-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a90-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="b7a90-124">Il gruppo di risorse a cui appartiene il database di metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a90-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b7a90-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="b7a90-126">ID risorsa del database di metadati della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a90-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="b7a90-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="b7a90-128">Server in cui è ospitato il database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7a90-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a90-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7a90-129">-Confirm</span></span>
<span data-ttu-id="b7a90-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7a90-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a90-131">-WhatIf</span></span>
<span data-ttu-id="b7a90-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7a90-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a90-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7a90-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a90-134">CommonParameters</span></span>
<span data-ttu-id="b7a90-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a90-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a90-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a90-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7a90-137">INPUTS</span></span>

### <span data-ttu-id="b7a90-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b7a90-138">System.String</span></span>

## <span data-ttu-id="b7a90-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7a90-139">OUTPUTS</span></span>

### <span data-ttu-id="b7a90-140">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="b7a90-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="b7a90-141">Note</span><span class="sxs-lookup"><span data-stu-id="b7a90-141">NOTES</span></span>

## <span data-ttu-id="b7a90-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7a90-142">RELATED LINKS</span></span>

[<span data-ttu-id="b7a90-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b7a90-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="b7a90-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b7a90-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

