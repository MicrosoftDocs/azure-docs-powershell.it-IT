---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 6b07ba5e31ab8e301d94b50170aca3869f9dea65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176910"
---
# <span data-ttu-id="13122-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="13122-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="13122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13122-102">SYNOPSIS</span></span>
<span data-ttu-id="13122-103">Ottiene le impostazioni di controllo di un server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="13122-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="13122-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13122-104">SYNTAX</span></span>

### <span data-ttu-id="13122-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13122-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13122-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13122-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13122-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13122-107">DESCRIPTION</span></span>
<span data-ttu-id="13122-108">Il cmdlet **Get-AzSqlServerAudit** ottiene le impostazioni di controllo di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="13122-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="13122-109">Specificare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="13122-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="13122-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13122-110">EXAMPLES</span></span>

### <span data-ttu-id="13122-111">Esempio 1: Ottenere le impostazioni di controllo di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="13122-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="13122-112">Esempio 2: Ottenere, tramite pipeline, le impostazioni di controllo di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="13122-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="13122-113">Esempio 3: Ottenere le impostazioni di controllo di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="13122-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="13122-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13122-114">PARAMETERS</span></span>

### <span data-ttu-id="13122-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13122-115">-AsJob</span></span>
<span data-ttu-id="13122-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="13122-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13122-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13122-117">-DefaultProfile</span></span>
<span data-ttu-id="13122-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13122-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13122-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13122-119">-ResourceGroupName</span></span>
<span data-ttu-id="13122-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13122-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="13122-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13122-121">-ServerName</span></span>
<span data-ttu-id="13122-122">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="13122-122">SQL server name.</span></span>

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

### <span data-ttu-id="13122-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="13122-123">-ServerObject</span></span>
<span data-ttu-id="13122-124">Oggetto server per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="13122-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="13122-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13122-125">CommonParameters</span></span>
<span data-ttu-id="13122-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13122-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13122-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13122-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13122-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="13122-128">INPUTS</span></span>

### <span data-ttu-id="13122-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13122-129">System.String</span></span>

### <span data-ttu-id="13122-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="13122-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="13122-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13122-131">OUTPUTS</span></span>

### <span data-ttu-id="13122-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="13122-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="13122-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="13122-133">NOTES</span></span>

## <span data-ttu-id="13122-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13122-134">RELATED LINKS</span></span>
