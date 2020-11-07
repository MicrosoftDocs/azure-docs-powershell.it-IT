---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857082"
---
# <span data-ttu-id="a6be7-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a6be7-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="a6be7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6be7-102">SYNOPSIS</span></span>
<span data-ttu-id="a6be7-103">**Importante: questo cmdlet è deprecato, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) la sostituisce.**</span><span class="sxs-lookup"><span data-stu-id="a6be7-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="a6be7-104">Ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6be7-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="a6be7-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6be7-105">SYNTAX</span></span>

### <span data-ttu-id="a6be7-106">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6be7-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6be7-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="a6be7-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6be7-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="a6be7-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6be7-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a6be7-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6be7-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a6be7-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6be7-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a6be7-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6be7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6be7-112">DESCRIPTION</span></span>
<span data-ttu-id="a6be7-113">Il cmdlet **Get-AzSqlDatabaseAuditing** ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6be7-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="a6be7-114">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="a6be7-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a6be7-115">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="a6be7-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="a6be7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6be7-116">EXAMPLES</span></span>

### <span data-ttu-id="a6be7-117">Esempio 1: recuperare le impostazioni di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
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

### <span data-ttu-id="a6be7-118">Esempio 2: ottenere le impostazioni di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
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

### <span data-ttu-id="a6be7-119">Esempio 3: ottenere, tramite pipeline, le impostazioni di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
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

### <span data-ttu-id="a6be7-120">Esempio 4: ottenere le impostazioni di controllo dell'hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="a6be7-121">Esempio 5: ottenere, tramite pipeline, le impostazioni di controllo dell'hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="a6be7-122">Esempio 6: ottenere le impostazioni di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6be7-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="a6be7-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6be7-123">PARAMETERS</span></span>

### <span data-ttu-id="a6be7-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="a6be7-124">-BlobStorage</span></span>
<span data-ttu-id="a6be7-125">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="a6be7-125">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="a6be7-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6be7-126">-DatabaseName</span></span>
<span data-ttu-id="a6be7-127">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="a6be7-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6be7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6be7-128">-DefaultProfile</span></span>
<span data-ttu-id="a6be7-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6be7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6be7-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a6be7-130">-EventHub</span></span>
<span data-ttu-id="a6be7-131">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="a6be7-131">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="a6be7-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6be7-132">-InputObject</span></span>
<span data-ttu-id="a6be7-133">Oggetto database per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a6be7-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6be7-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="a6be7-134">-LogAnalytics</span></span>
<span data-ttu-id="a6be7-135">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="a6be7-135">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="a6be7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6be7-136">-ResourceGroupName</span></span>
<span data-ttu-id="a6be7-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6be7-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6be7-138">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a6be7-138">-ServerName</span></span>
<span data-ttu-id="a6be7-139">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a6be7-139">SQL server name.</span></span>

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

### <span data-ttu-id="a6be7-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6be7-140">-Confirm</span></span>
<span data-ttu-id="a6be7-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6be7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6be7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6be7-142">-WhatIf</span></span>
<span data-ttu-id="a6be7-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6be7-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6be7-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6be7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6be7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6be7-145">CommonParameters</span></span>
<span data-ttu-id="a6be7-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6be7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6be7-147">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6be7-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6be7-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6be7-148">INPUTS</span></span>

### <span data-ttu-id="a6be7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a6be7-149">System.String</span></span>

### <span data-ttu-id="a6be7-150">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a6be7-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="a6be7-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6be7-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a6be7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6be7-152">OUTPUTS</span></span>

### <span data-ttu-id="a6be7-153">Microsoft. Azure. Commands. SQL. auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a6be7-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="a6be7-154">Note</span><span class="sxs-lookup"><span data-stu-id="a6be7-154">NOTES</span></span>

## <span data-ttu-id="a6be7-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6be7-155">RELATED LINKS</span></span>
