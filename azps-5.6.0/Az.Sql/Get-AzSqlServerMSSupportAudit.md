---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: ee6d57c2fe7bad97c8b119fdd68a07daf4603cdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959358"
---
# <span data-ttu-id="025c3-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="025c3-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="025c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025c3-102">SYNOPSIS</span></span>
<span data-ttu-id="025c3-103">Recupera le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="025c3-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="025c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="025c3-104">SYNTAX</span></span>

### <span data-ttu-id="025c3-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="025c3-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025c3-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="025c3-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="025c3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="025c3-107">DESCRIPTION</span></span>
<span data-ttu-id="025c3-108">Il cmdlet **Get-AzSqlServerMSSupportAudit** ottiene le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="025c3-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="025c3-109">Specificare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="025c3-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="025c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="025c3-110">EXAMPLES</span></span>

### <span data-ttu-id="025c3-111">Esempio 1: Ottenere le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="025c3-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="025c3-112">Esempio 2: Ottenere, tramite pipeline, le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="025c3-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="025c3-113">Esempio 3: Ottenere le impostazioni di controllo delle operazioni di supporto Microsoft di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="025c3-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="025c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025c3-114">PARAMETERS</span></span>

### <span data-ttu-id="025c3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="025c3-115">-AsJob</span></span>
<span data-ttu-id="025c3-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="025c3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="025c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025c3-117">-DefaultProfile</span></span>
<span data-ttu-id="025c3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="025c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="025c3-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="025c3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="025c3-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="025c3-121">-ServerName</span></span>
<span data-ttu-id="025c3-122">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="025c3-122">SQL server name.</span></span>

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

### <span data-ttu-id="025c3-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="025c3-123">-ServerObject</span></span>
<span data-ttu-id="025c3-124">Oggetto server per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="025c3-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="025c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025c3-125">CommonParameters</span></span>
<span data-ttu-id="025c3-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025c3-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="025c3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025c3-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="025c3-128">INPUTS</span></span>

### <span data-ttu-id="025c3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="025c3-129">System.String</span></span>

### <span data-ttu-id="025c3-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="025c3-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="025c3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="025c3-131">OUTPUTS</span></span>

### <span data-ttu-id="025c3-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="025c3-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="025c3-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="025c3-133">NOTES</span></span>

## <span data-ttu-id="025c3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="025c3-134">RELATED LINKS</span></span>
