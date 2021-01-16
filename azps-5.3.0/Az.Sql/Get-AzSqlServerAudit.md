---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476675"
---
# <span data-ttu-id="f0319-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f0319-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="f0319-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0319-102">SYNOPSIS</span></span>
<span data-ttu-id="f0319-103">Ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0319-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="f0319-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0319-104">SYNTAX</span></span>

### <span data-ttu-id="f0319-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0319-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0319-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0319-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0319-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0319-107">DESCRIPTION</span></span>
<span data-ttu-id="f0319-108">Il cmdlet **Get-AzSqlServerAudit** ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0319-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="f0319-109">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="f0319-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="f0319-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0319-110">EXAMPLES</span></span>

### <span data-ttu-id="f0319-111">Esempio 1: recuperare le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f0319-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="f0319-112">Esempio 2: ottenere, tramite pipeline, le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f0319-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="f0319-113">Esempio 3: ottenere le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f0319-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="f0319-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0319-114">PARAMETERS</span></span>

### <span data-ttu-id="f0319-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0319-115">-AsJob</span></span>
<span data-ttu-id="f0319-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f0319-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0319-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0319-117">-DefaultProfile</span></span>
<span data-ttu-id="f0319-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0319-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0319-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0319-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0319-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0319-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0319-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f0319-121">-ServerName</span></span>
<span data-ttu-id="f0319-122">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f0319-122">SQL server name.</span></span>

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

### <span data-ttu-id="f0319-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="f0319-123">-ServerObject</span></span>
<span data-ttu-id="f0319-124">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="f0319-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f0319-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0319-125">CommonParameters</span></span>
<span data-ttu-id="f0319-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0319-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0319-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0319-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0319-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0319-128">INPUTS</span></span>

### <span data-ttu-id="f0319-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f0319-129">System.String</span></span>

### <span data-ttu-id="f0319-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f0319-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f0319-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0319-131">OUTPUTS</span></span>

### <span data-ttu-id="f0319-132">Microsoft. Azure. Commands. SQL. auditing. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="f0319-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="f0319-133">Note</span><span class="sxs-lookup"><span data-stu-id="f0319-133">NOTES</span></span>

## <span data-ttu-id="f0319-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0319-134">RELATED LINKS</span></span>
