---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344008"
---
# <span data-ttu-id="806d3-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="806d3-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="806d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="806d3-102">SYNOPSIS</span></span>
<span data-ttu-id="806d3-103">Aggiorna un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="806d3-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="806d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="806d3-104">SYNTAX</span></span>

### <span data-ttu-id="806d3-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="806d3-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="806d3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="806d3-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="806d3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="806d3-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806d3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="806d3-108">DESCRIPTION</span></span>
<span data-ttu-id="806d3-109">Il cmdlet Set-AzSqlElasticJobAgent aggiorna gli agenti di processo elastici</span><span class="sxs-lookup"><span data-stu-id="806d3-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="806d3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="806d3-110">EXAMPLES</span></span>

### <span data-ttu-id="806d3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="806d3-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="806d3-112">Aggiorna un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="806d3-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="806d3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="806d3-113">PARAMETERS</span></span>

### <span data-ttu-id="806d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806d3-114">-DefaultProfile</span></span>
<span data-ttu-id="806d3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="806d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="806d3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="806d3-116">-InputObject</span></span>
<span data-ttu-id="806d3-117">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="806d3-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="806d3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="806d3-118">-Name</span></span>
<span data-ttu-id="806d3-119">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="806d3-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="806d3-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="806d3-121">The resource group name</span></span>

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

### <span data-ttu-id="806d3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="806d3-122">-ResourceId</span></span>
<span data-ttu-id="806d3-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="806d3-123">The agent resource id</span></span>

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

### <span data-ttu-id="806d3-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="806d3-124">-ServerName</span></span>
<span data-ttu-id="806d3-125">Nome del server</span><span class="sxs-lookup"><span data-stu-id="806d3-125">The server name</span></span>

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

### <span data-ttu-id="806d3-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="806d3-126">-Tag</span></span>
<span data-ttu-id="806d3-127">Tag da associare all'agente di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="806d3-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d3-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="806d3-128">-Confirm</span></span>
<span data-ttu-id="806d3-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="806d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806d3-130">-WhatIf</span></span>
<span data-ttu-id="806d3-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="806d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="806d3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="806d3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806d3-133">CommonParameters</span></span>
<span data-ttu-id="806d3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806d3-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="806d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806d3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="806d3-136">INPUTS</span></span>

### <span data-ttu-id="806d3-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="806d3-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="806d3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="806d3-138">OUTPUTS</span></span>

### <span data-ttu-id="806d3-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="806d3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="806d3-140">Note</span><span class="sxs-lookup"><span data-stu-id="806d3-140">NOTES</span></span>

## <span data-ttu-id="806d3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="806d3-141">RELATED LINKS</span></span>
