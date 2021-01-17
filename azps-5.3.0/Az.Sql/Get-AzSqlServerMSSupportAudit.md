---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473677"
---
# <span data-ttu-id="cccbd-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="cccbd-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="cccbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cccbd-102">SYNOPSIS</span></span>
<span data-ttu-id="cccbd-103">Ottiene le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cccbd-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="cccbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cccbd-104">SYNTAX</span></span>

### <span data-ttu-id="cccbd-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cccbd-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cccbd-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cccbd-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cccbd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cccbd-107">DESCRIPTION</span></span>
<span data-ttu-id="cccbd-108">Il cmdlet **Get-AzSqlServerMSSupportAudit** ottiene le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cccbd-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="cccbd-109">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="cccbd-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="cccbd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cccbd-110">EXAMPLES</span></span>

### <span data-ttu-id="cccbd-111">Esempio 1: ottenere le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="cccbd-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="cccbd-112">Esempio 2: ottenere, tramite pipeline, le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="cccbd-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="cccbd-113">Esempio 3: ottenere le impostazioni di controllo delle operazioni del supporto Microsoft di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="cccbd-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="cccbd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cccbd-114">PARAMETERS</span></span>

### <span data-ttu-id="cccbd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cccbd-115">-AsJob</span></span>
<span data-ttu-id="cccbd-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cccbd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cccbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccbd-117">-DefaultProfile</span></span>
<span data-ttu-id="cccbd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cccbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccbd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccbd-119">-ResourceGroupName</span></span>
<span data-ttu-id="cccbd-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cccbd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cccbd-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cccbd-121">-ServerName</span></span>
<span data-ttu-id="cccbd-122">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cccbd-122">SQL server name.</span></span>

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

### <span data-ttu-id="cccbd-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="cccbd-123">-ServerObject</span></span>
<span data-ttu-id="cccbd-124">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="cccbd-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="cccbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccbd-125">CommonParameters</span></span>
<span data-ttu-id="cccbd-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccbd-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cccbd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccbd-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cccbd-128">INPUTS</span></span>

### <span data-ttu-id="cccbd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cccbd-129">System.String</span></span>

### <span data-ttu-id="cccbd-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cccbd-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="cccbd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cccbd-131">OUTPUTS</span></span>

### <span data-ttu-id="cccbd-132">Microsoft. Azure. Commands. SQL. auditing. Model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="cccbd-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="cccbd-133">Note</span><span class="sxs-lookup"><span data-stu-id="cccbd-133">NOTES</span></span>

## <span data-ttu-id="cccbd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cccbd-134">RELATED LINKS</span></span>
