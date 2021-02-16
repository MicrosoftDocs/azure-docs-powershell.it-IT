---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209178"
---
# <span data-ttu-id="20f5a-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="20f5a-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="20f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="20f5a-103">Modifica le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="20f5a-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="20f5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20f5a-104">SYNTAX</span></span>

### <span data-ttu-id="20f5a-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20f5a-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20f5a-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f5a-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f5a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="20f5a-108">Il cmdlet **Set-AzSqlServerMSSupportAudit** modifica le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="20f5a-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="20f5a-109">Per usare il cmdlet, usare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="20f5a-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="20f5a-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare *il parametro StorageAccountResourceId* per determinare l'account di archiviazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="20f5a-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="20f5a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="20f5a-112">Esempio 1: Abilitare i criteri di controllo delle operazioni di supporto Microsoft per l'archiviazione BLOB di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="20f5a-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="20f5a-113">Esempio 2: Disabilitare i criteri di controllo delle operazioni di supporto Microsoft per l'archiviazione BLOB di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="20f5a-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="20f5a-114">Esempio 3: Abilitare i criteri di controllo delle operazioni di supporto microsoft dell'hub eventi di azure SQL</span><span class="sxs-lookup"><span data-stu-id="20f5a-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="20f5a-115">Esempio 4: Disabilitare i criteri di controllo delle operazioni di supporto per l'hub eventi Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="20f5a-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="20f5a-116">Esempio 5: Abilitare i criteri di controllo delle operazioni di supporto Microsoft per i log di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="20f5a-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="20f5a-117">Esempio 6: Disabilitare i criteri di controllo delle operazioni di supporto Microsoft per i log di un server azure SQL</span><span class="sxs-lookup"><span data-stu-id="20f5a-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="20f5a-118">Esempio 7: Disabilitare, tramite pipeline, i criteri di controllo delle operazioni di supporto microsoft del log di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="20f5a-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="20f5a-119">Esempio 8: Disabilitare l'invio dei record di controllo delle operazioni di supporto Microsoft di un server di SQL azure all'archiviazione BLOB e abilitarli all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="20f5a-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="20f5a-120">Esempio 9: Abilitare l'invio dei record di controllo delle operazioni di supporto Microsoft di un server SQL Azure all'archiviazione BLOB, all'hub eventi e all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="20f5a-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="20f5a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f5a-121">PARAMETERS</span></span>

### <span data-ttu-id="20f5a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20f5a-122">-AsJob</span></span>
<span data-ttu-id="20f5a-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="20f5a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20f5a-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="20f5a-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="20f5a-125">Indica se l'archiviazione BLOB è una destinazione per i record di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f5a-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="20f5a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f5a-126">-DefaultProfile</span></span>
<span data-ttu-id="20f5a-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20f5a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f5a-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="20f5a-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="20f5a-129">ID risorsa per la regola di autorizzazione dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="20f5a-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="20f5a-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="20f5a-130">-EventHubName</span></span>
<span data-ttu-id="20f5a-131">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="20f5a-131">The name of the event hub.</span></span> <span data-ttu-id="20f5a-132">Se non ne viene specificato nessuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="20f5a-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="20f5a-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="20f5a-133">-EventHubTargetState</span></span>
<span data-ttu-id="20f5a-134">Indica se l'hub eventi è una destinazione per i record di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f5a-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="20f5a-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="20f5a-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="20f5a-136">Indica se l'analisi del log è una destinazione per i record di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f5a-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="20f5a-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20f5a-137">-PassThru</span></span>
<span data-ttu-id="20f5a-138">Specifica se eseguire l'output del criterio di controllo delle operazioni di supporto Microsoft alla fine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="20f5a-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="20f5a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f5a-139">-ResourceGroupName</span></span>
<span data-ttu-id="20f5a-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20f5a-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="20f5a-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20f5a-141">-ServerName</span></span>
<span data-ttu-id="20f5a-142">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="20f5a-142">SQL server name.</span></span>

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

### <span data-ttu-id="20f5a-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="20f5a-143">-ServerObject</span></span>
<span data-ttu-id="20f5a-144">Oggetto server per la gestione dei criteri di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f5a-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="20f5a-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="20f5a-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="20f5a-146">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="20f5a-146">The storage account resource id</span></span>

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

### <span data-ttu-id="20f5a-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="20f5a-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="20f5a-148">ID area di lavoro (ID risorsa di un'area di lavoro Analisi log) per un'area di lavoro Analisi log a cui inviare i log di controllo delle operazioni di supporto Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f5a-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="20f5a-149">Esempio: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/rba2</span><span class="sxs-lookup"><span data-stu-id="20f5a-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="20f5a-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20f5a-150">-Confirm</span></span>
<span data-ttu-id="20f5a-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20f5a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f5a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f5a-152">-WhatIf</span></span>
<span data-ttu-id="20f5a-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20f5a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20f5a-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20f5a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f5a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f5a-155">CommonParameters</span></span>
<span data-ttu-id="20f5a-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f5a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f5a-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20f5a-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f5a-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="20f5a-158">INPUTS</span></span>

### <span data-ttu-id="20f5a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="20f5a-159">System.String</span></span>

### <span data-ttu-id="20f5a-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="20f5a-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="20f5a-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="20f5a-161">System.Guid</span></span>

### <span data-ttu-id="20f5a-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20f5a-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="20f5a-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="20f5a-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="20f5a-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20f5a-164">OUTPUTS</span></span>

### <span data-ttu-id="20f5a-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20f5a-165">System.Boolean</span></span>

## <span data-ttu-id="20f5a-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="20f5a-166">NOTES</span></span>

## <span data-ttu-id="20f5a-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20f5a-167">RELATED LINKS</span></span>
