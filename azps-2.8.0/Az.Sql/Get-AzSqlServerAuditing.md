---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857469"
---
# <span data-ttu-id="36efb-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="36efb-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="36efb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36efb-102">SYNOPSIS</span></span>
<span data-ttu-id="36efb-103">**Importante: questo cmdlet è deprecato, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) la sostituisce.**</span><span class="sxs-lookup"><span data-stu-id="36efb-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="36efb-104">Ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="36efb-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="36efb-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36efb-105">SYNTAX</span></span>

### <span data-ttu-id="36efb-106">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36efb-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36efb-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="36efb-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36efb-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="36efb-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36efb-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="36efb-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36efb-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="36efb-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36efb-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="36efb-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36efb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36efb-112">DESCRIPTION</span></span>
<span data-ttu-id="36efb-113">Il cmdlet **Get-AzSqlServerAuditing** ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="36efb-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="36efb-114">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="36efb-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="36efb-115">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="36efb-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="36efb-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36efb-116">EXAMPLES</span></span>

### <span data-ttu-id="36efb-117">Esempio 1: ottenere le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="36efb-118">Esempio 2: ottenere le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="36efb-119">Esempio 3: ottenere, tramite pipeline, le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="36efb-120">Esempio 4: ottenere le impostazioni di controllo dell'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="36efb-121">Esempio 5: ottenere, tramite pipeline, le impostazioni di controllo dell'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="36efb-122">Esempio 6: ottenere le impostazioni di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="36efb-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="36efb-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36efb-123">PARAMETERS</span></span>

### <span data-ttu-id="36efb-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="36efb-124">-BlobStorage</span></span>
<span data-ttu-id="36efb-125">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="36efb-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36efb-126">-DefaultProfile</span></span>
<span data-ttu-id="36efb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36efb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36efb-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="36efb-128">-EventHub</span></span>
<span data-ttu-id="36efb-129">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="36efb-129">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36efb-130">-InputObject</span></span>
<span data-ttu-id="36efb-131">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="36efb-131">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="36efb-132">-LogAnalytics</span></span>
<span data-ttu-id="36efb-133">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="36efb-133">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36efb-134">-ResourceGroupName</span></span>
<span data-ttu-id="36efb-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36efb-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-136">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="36efb-136">-ServerName</span></span>
<span data-ttu-id="36efb-137">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36efb-137">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36efb-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36efb-138">-Confirm</span></span>
<span data-ttu-id="36efb-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36efb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36efb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36efb-140">-WhatIf</span></span>
<span data-ttu-id="36efb-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36efb-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36efb-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36efb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36efb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36efb-143">CommonParameters</span></span>
<span data-ttu-id="36efb-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36efb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36efb-145">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36efb-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36efb-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36efb-146">INPUTS</span></span>

### <span data-ttu-id="36efb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="36efb-147">System.String</span></span>

### <span data-ttu-id="36efb-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="36efb-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="36efb-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36efb-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36efb-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36efb-150">OUTPUTS</span></span>

### <span data-ttu-id="36efb-151">Microsoft. Azure. Commands. SQL. auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="36efb-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="36efb-152">Note</span><span class="sxs-lookup"><span data-stu-id="36efb-152">NOTES</span></span>

## <span data-ttu-id="36efb-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36efb-153">RELATED LINKS</span></span>
