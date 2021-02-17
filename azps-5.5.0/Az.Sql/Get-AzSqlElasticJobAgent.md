---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191087"
---
# <span data-ttu-id="50051-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="50051-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="50051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50051-102">SYNOPSIS</span></span>
<span data-ttu-id="50051-103">Recupera un agente di processo SQL lavoro flessibile di Azure</span><span class="sxs-lookup"><span data-stu-id="50051-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="50051-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50051-104">SYNTAX</span></span>

### <span data-ttu-id="50051-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50051-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50051-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="50051-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50051-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50051-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50051-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50051-108">DESCRIPTION</span></span>
<span data-ttu-id="50051-109">Il cmdlet Get-AzSqlElasticJobAgent ottiene uno o più agenti di lavoro flessibile</span><span class="sxs-lookup"><span data-stu-id="50051-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="50051-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50051-110">EXAMPLES</span></span>

### <span data-ttu-id="50051-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50051-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="50051-112">Ottiene un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="50051-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="50051-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50051-113">PARAMETERS</span></span>

### <span data-ttu-id="50051-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50051-114">-DefaultProfile</span></span>
<span data-ttu-id="50051-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50051-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50051-116">-Name</span><span class="sxs-lookup"><span data-stu-id="50051-116">-Name</span></span>
<span data-ttu-id="50051-117">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="50051-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50051-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="50051-118">-ParentObject</span></span>
<span data-ttu-id="50051-119">Oggetto di input del server</span><span class="sxs-lookup"><span data-stu-id="50051-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50051-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50051-120">-ParentResourceId</span></span>
<span data-ttu-id="50051-121">ID di risorsa del server</span><span class="sxs-lookup"><span data-stu-id="50051-121">The server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50051-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50051-122">-ResourceGroupName</span></span>
<span data-ttu-id="50051-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50051-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50051-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50051-124">-ServerName</span></span>
<span data-ttu-id="50051-125">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="50051-125">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50051-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50051-126">CommonParameters</span></span>
<span data-ttu-id="50051-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50051-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50051-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50051-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50051-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="50051-129">INPUTS</span></span>

### <span data-ttu-id="50051-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="50051-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="50051-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50051-131">OUTPUTS</span></span>

### <span data-ttu-id="50051-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="50051-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="50051-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="50051-133">NOTES</span></span>

## <span data-ttu-id="50051-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50051-134">RELATED LINKS</span></span>
