---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183359"
---
# <span data-ttu-id="dbc87-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dbc87-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="dbc87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc87-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc87-103">Ottiene le impostazioni di controllo di un database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc87-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="dbc87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbc87-104">SYNTAX</span></span>

### <span data-ttu-id="dbc87-105">DatabaseParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dbc87-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc87-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbc87-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbc87-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbc87-107">DESCRIPTION</span></span>
<span data-ttu-id="dbc87-108">Il cmdlet **Get-AzSqlDatabaseAudit** ottiene le impostazioni di controllo di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc87-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="dbc87-109">Per usare il cmdlet, usare i *parametri ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="dbc87-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="dbc87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbc87-110">EXAMPLES</span></span>

### <span data-ttu-id="dbc87-111">Esempio 1: Ottenere le impostazioni di controllo di un database di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="dbc87-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="dbc87-112">Esempio 2: Ottenere, tramite pipeline, le impostazioni di controllo di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="dbc87-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="dbc87-113">Esempio 3: Ottenere le impostazioni di controllo di un database di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="dbc87-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="dbc87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc87-114">PARAMETERS</span></span>

### <span data-ttu-id="dbc87-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbc87-115">-DatabaseName</span></span>
<span data-ttu-id="dbc87-116">SQL nome del database.</span><span class="sxs-lookup"><span data-stu-id="dbc87-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc87-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="dbc87-117">-DatabaseObject</span></span>
<span data-ttu-id="dbc87-118">Oggetto di database per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="dbc87-118">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc87-119">-DefaultProfile</span></span>
<span data-ttu-id="dbc87-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc87-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc87-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbc87-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbc87-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc87-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbc87-123">-ServerName</span></span>
<span data-ttu-id="dbc87-124">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="dbc87-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc87-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc87-125">CommonParameters</span></span>
<span data-ttu-id="dbc87-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc87-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc87-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbc87-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc87-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbc87-128">INPUTS</span></span>

### <span data-ttu-id="dbc87-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc87-129">System.String</span></span>

### <span data-ttu-id="dbc87-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dbc87-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="dbc87-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbc87-131">OUTPUTS</span></span>

### <span data-ttu-id="dbc87-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="dbc87-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="dbc87-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbc87-133">NOTES</span></span>

## <span data-ttu-id="dbc87-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbc87-134">RELATED LINKS</span></span>
