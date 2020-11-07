---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865410"
---
# <span data-ttu-id="67021-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="67021-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="67021-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67021-102">SYNOPSIS</span></span>
<span data-ttu-id="67021-103">Ottiene un agente di processo elastico di Azure SQL</span><span class="sxs-lookup"><span data-stu-id="67021-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="67021-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67021-104">SYNTAX</span></span>

### <span data-ttu-id="67021-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67021-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67021-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="67021-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67021-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67021-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67021-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67021-108">DESCRIPTION</span></span>
<span data-ttu-id="67021-109">Il cmdlet Get-AzSqlElasticJobAgent ottiene uno o più agenti di processo elastici</span><span class="sxs-lookup"><span data-stu-id="67021-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="67021-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67021-110">EXAMPLES</span></span>

### <span data-ttu-id="67021-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67021-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="67021-112">Ottiene un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="67021-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="67021-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67021-113">PARAMETERS</span></span>

### <span data-ttu-id="67021-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67021-114">-DefaultProfile</span></span>
<span data-ttu-id="67021-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67021-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67021-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="67021-116">-Name</span></span>
<span data-ttu-id="67021-117">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="67021-117">The agent name</span></span>

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

### <span data-ttu-id="67021-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="67021-118">-ParentObject</span></span>
<span data-ttu-id="67021-119">Oggetto di input del server</span><span class="sxs-lookup"><span data-stu-id="67021-119">The server input object</span></span>

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

### <span data-ttu-id="67021-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="67021-120">-ParentResourceId</span></span>
<span data-ttu-id="67021-121">ID risorsa server</span><span class="sxs-lookup"><span data-stu-id="67021-121">The server resource id</span></span>

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

### <span data-ttu-id="67021-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67021-122">-ResourceGroupName</span></span>
<span data-ttu-id="67021-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67021-123">The resource group name</span></span>

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

### <span data-ttu-id="67021-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="67021-124">-ServerName</span></span>
<span data-ttu-id="67021-125">Nome del server</span><span class="sxs-lookup"><span data-stu-id="67021-125">The server name</span></span>

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

### <span data-ttu-id="67021-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67021-126">CommonParameters</span></span>
<span data-ttu-id="67021-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67021-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67021-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67021-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67021-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67021-129">INPUTS</span></span>

### <span data-ttu-id="67021-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="67021-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="67021-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67021-131">OUTPUTS</span></span>

### <span data-ttu-id="67021-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="67021-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="67021-133">Note</span><span class="sxs-lookup"><span data-stu-id="67021-133">NOTES</span></span>

## <span data-ttu-id="67021-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67021-134">RELATED LINKS</span></span>
