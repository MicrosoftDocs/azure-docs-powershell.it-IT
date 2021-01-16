---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475429"
---
# <span data-ttu-id="fb985-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="fb985-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="fb985-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb985-102">SYNOPSIS</span></span>
<span data-ttu-id="fb985-103">Modifica le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb985-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="fb985-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb985-104">SYNTAX</span></span>

### <span data-ttu-id="fb985-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb985-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb985-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb985-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb985-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb985-107">DESCRIPTION</span></span>
<span data-ttu-id="fb985-108">Il cmdlet **set-AzSqlServerMSSupportAudit** modifica le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb985-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="fb985-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="fb985-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="fb985-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="fb985-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="fb985-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb985-111">EXAMPLES</span></span>

### <span data-ttu-id="fb985-112">Esempio 1: abilitare il criterio di controllo delle operazioni di archiviazione BLOB Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="fb985-113">Esempio 2: disabilitare il criterio di controllo delle operazioni di archiviazione BLOB Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="fb985-114">Esempio 3: abilitare i criteri di controllo delle operazioni del supporto tecnico Microsoft per l'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="fb985-115">Esempio 4: disabilitare i criteri di controllo delle operazioni del supporto Microsoft dell'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="fb985-116">Esempio 5: abilitare i criteri di controllo delle operazioni del supporto tecnico del log analitico Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="fb985-117">Esempio 6: disabilitare i criteri per il controllo delle operazioni del supporto tecnico del registro Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="fb985-118">Esempio 7: disabilitare, tramite pipeline, il criterio di controllo delle operazioni di analisi dei dati del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fb985-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="fb985-119">Esempio 8: disabilitare l'invio dei record di controllo delle operazioni di supporto di Microsoft di un server SQL di Azure a archiviazione BLOB e consentire l'invio di analisi di log.</span><span class="sxs-lookup"><span data-stu-id="fb985-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="fb985-120">Esempio 9: abilitare l'invio dei record di controllo delle operazioni di supporto Microsoft di un server SQL di Azure a archiviazione BLOB, Hub eventi e analisi log.</span><span class="sxs-lookup"><span data-stu-id="fb985-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="fb985-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb985-121">PARAMETERS</span></span>

### <span data-ttu-id="fb985-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb985-122">-AsJob</span></span>
<span data-ttu-id="fb985-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fb985-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb985-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="fb985-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="fb985-125">Indica se l'archiviazione BLOB è una destinazione per i record di controllo delle operazioni del supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb985-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb985-126">-DefaultProfile</span></span>
<span data-ttu-id="fb985-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb985-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb985-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="fb985-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="fb985-129">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="fb985-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="fb985-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="fb985-130">-EventHubName</span></span>
<span data-ttu-id="fb985-131">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="fb985-131">The name of the event hub.</span></span> <span data-ttu-id="fb985-132">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="fb985-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="fb985-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="fb985-133">-EventHubTargetState</span></span>
<span data-ttu-id="fb985-134">Indica se Hub eventi è una destinazione per i record di controllo delle operazioni del supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb985-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="fb985-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="fb985-136">Indica se analisi log è una destinazione per i record di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb985-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb985-137">-PassThru</span></span>
<span data-ttu-id="fb985-138">Specifica se eseguire l'output dei criteri di controllo delle operazioni del supporto Microsoft alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb985-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="fb985-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb985-139">-ResourceGroupName</span></span>
<span data-ttu-id="fb985-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb985-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-141">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fb985-141">-ServerName</span></span>
<span data-ttu-id="fb985-142">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb985-142">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="fb985-143">-ServerObject</span></span>
<span data-ttu-id="fb985-144">L'oggetto server per gestire i criteri di controllo delle operazioni del supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb985-144">The server object to manage its Microsoft support operations audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fb985-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="fb985-146">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fb985-146">The storage account resource id</span></span>

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

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb985-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fb985-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="fb985-148">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i registri di controllo delle operazioni del supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb985-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="fb985-149">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="fb985-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="fb985-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb985-150">-Confirm</span></span>
<span data-ttu-id="fb985-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb985-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb985-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb985-152">-WhatIf</span></span>
<span data-ttu-id="fb985-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb985-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb985-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb985-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb985-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb985-155">CommonParameters</span></span>
<span data-ttu-id="fb985-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb985-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb985-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb985-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb985-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb985-158">INPUTS</span></span>

### <span data-ttu-id="fb985-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fb985-159">System.String</span></span>

### <span data-ttu-id="fb985-160">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fb985-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="fb985-161">System. Guid</span><span class="sxs-lookup"><span data-stu-id="fb985-161">System.Guid</span></span>

### <span data-ttu-id="fb985-162">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb985-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb985-163">Microsoft. Azure. Commands. SQL. auditing. Model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="fb985-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="fb985-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb985-164">OUTPUTS</span></span>

### <span data-ttu-id="fb985-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb985-165">System.Boolean</span></span>

## <span data-ttu-id="fb985-166">Note</span><span class="sxs-lookup"><span data-stu-id="fb985-166">NOTES</span></span>

## <span data-ttu-id="fb985-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb985-167">RELATED LINKS</span></span>
