---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 80835d33f75517bea6a91e65f110f441d20ab59c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857185"
---
# <span data-ttu-id="5519d-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="5519d-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="5519d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5519d-102">SYNOPSIS</span></span>
<span data-ttu-id="5519d-103">Ottiene un agente di processo elastico di Azure SQL</span><span class="sxs-lookup"><span data-stu-id="5519d-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="5519d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5519d-104">SYNTAX</span></span>

### <span data-ttu-id="5519d-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5519d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5519d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5519d-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5519d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5519d-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5519d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5519d-108">DESCRIPTION</span></span>
<span data-ttu-id="5519d-109">Il cmdlet Get-AzSqlElasticJobAgent ottiene uno o più agenti di processo elastici</span><span class="sxs-lookup"><span data-stu-id="5519d-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="5519d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5519d-110">EXAMPLES</span></span>

### <span data-ttu-id="5519d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5519d-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="5519d-112">Ottiene un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="5519d-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="5519d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5519d-113">PARAMETERS</span></span>

### <span data-ttu-id="5519d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5519d-114">-DefaultProfile</span></span>
<span data-ttu-id="5519d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5519d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5519d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5519d-116">-Name</span></span>
<span data-ttu-id="5519d-117">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="5519d-117">The agent name</span></span>

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

### <span data-ttu-id="5519d-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5519d-118">-ParentObject</span></span>
<span data-ttu-id="5519d-119">Oggetto di input del server</span><span class="sxs-lookup"><span data-stu-id="5519d-119">The server input object</span></span>

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

### <span data-ttu-id="5519d-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5519d-120">-ParentResourceId</span></span>
<span data-ttu-id="5519d-121">ID risorsa server</span><span class="sxs-lookup"><span data-stu-id="5519d-121">The server resource id</span></span>

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

### <span data-ttu-id="5519d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5519d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5519d-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5519d-123">The resource group name</span></span>

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

### <span data-ttu-id="5519d-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5519d-124">-ServerName</span></span>
<span data-ttu-id="5519d-125">Nome del server</span><span class="sxs-lookup"><span data-stu-id="5519d-125">The server name</span></span>

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

### <span data-ttu-id="5519d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5519d-126">CommonParameters</span></span>
<span data-ttu-id="5519d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5519d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5519d-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5519d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5519d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5519d-129">INPUTS</span></span>

### <span data-ttu-id="5519d-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5519d-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="5519d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5519d-131">OUTPUTS</span></span>

### <span data-ttu-id="5519d-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5519d-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5519d-133">Note</span><span class="sxs-lookup"><span data-stu-id="5519d-133">NOTES</span></span>

## <span data-ttu-id="5519d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5519d-134">RELATED LINKS</span></span>
