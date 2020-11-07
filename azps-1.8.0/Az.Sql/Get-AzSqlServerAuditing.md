---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676909"
---
# <span data-ttu-id="4ab29-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="4ab29-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="4ab29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ab29-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab29-103">Ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab29-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="4ab29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ab29-104">SYNTAX</span></span>

### <span data-ttu-id="4ab29-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ab29-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab29-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="4ab29-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab29-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="4ab29-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab29-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="4ab29-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab29-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="4ab29-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab29-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="4ab29-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab29-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ab29-111">DESCRIPTION</span></span>
<span data-ttu-id="4ab29-112">Il cmdlet **Get-AzSqlServerAuditing** ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab29-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="4ab29-113">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="4ab29-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="4ab29-114">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="4ab29-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="4ab29-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ab29-115">EXAMPLES</span></span>

### <span data-ttu-id="4ab29-116">Esempio 1: ottenere le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="4ab29-117">Esempio 2: ottenere le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="4ab29-118">Esempio 3: ottenere, tramite pipeline, le impostazioni di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="4ab29-119">Esempio 4: ottenere le impostazioni di controllo dell'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="4ab29-120">Esempio 5: ottenere, tramite pipeline, le impostazioni di controllo dell'hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="4ab29-121">Esempio 6: ottenere le impostazioni di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab29-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="4ab29-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ab29-122">PARAMETERS</span></span>

### <span data-ttu-id="4ab29-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="4ab29-123">-BlobStorage</span></span>
<span data-ttu-id="4ab29-124">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="4ab29-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="4ab29-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab29-125">-DefaultProfile</span></span>
<span data-ttu-id="4ab29-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab29-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab29-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4ab29-127">-EventHub</span></span>
<span data-ttu-id="4ab29-128">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="4ab29-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="4ab29-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ab29-129">-InputObject</span></span>
<span data-ttu-id="4ab29-130">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="4ab29-130">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="4ab29-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="4ab29-131">-LogAnalytics</span></span>
<span data-ttu-id="4ab29-132">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="4ab29-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="4ab29-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab29-133">-ResourceGroupName</span></span>
<span data-ttu-id="4ab29-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ab29-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ab29-135">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4ab29-135">-ServerName</span></span>
<span data-ttu-id="4ab29-136">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4ab29-136">SQL server name.</span></span>

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

### <span data-ttu-id="4ab29-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ab29-137">-Confirm</span></span>
<span data-ttu-id="4ab29-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab29-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab29-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab29-139">-WhatIf</span></span>
<span data-ttu-id="4ab29-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab29-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ab29-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab29-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab29-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab29-142">CommonParameters</span></span>
<span data-ttu-id="4ab29-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab29-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab29-144">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ab29-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab29-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ab29-145">INPUTS</span></span>

### <span data-ttu-id="4ab29-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab29-146">System.String</span></span>

### <span data-ttu-id="4ab29-147">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="4ab29-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4ab29-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ab29-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ab29-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ab29-149">OUTPUTS</span></span>

### <span data-ttu-id="4ab29-150">Microsoft. Azure. Commands. SQL. auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="4ab29-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="4ab29-151">Note</span><span class="sxs-lookup"><span data-stu-id="4ab29-151">NOTES</span></span>

## <span data-ttu-id="4ab29-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ab29-152">RELATED LINKS</span></span>
