---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986353"
---
# <span data-ttu-id="a7b5f-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="a7b5f-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="a7b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b5f-103">Aggiorna un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="a7b5f-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="a7b5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7b5f-104">SYNTAX</span></span>

### <span data-ttu-id="a7b5f-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7b5f-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b5f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7b5f-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b5f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a7b5f-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b5f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7b5f-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b5f-109">Il cmdlet Set-AzSqlElasticJobAgent aggiorna gli agenti di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="a7b5f-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="a7b5f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7b5f-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b5f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7b5f-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="a7b5f-112">Aggiorna un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="a7b5f-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="a7b5f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b5f-113">PARAMETERS</span></span>

### <span data-ttu-id="a7b5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b5f-114">-DefaultProfile</span></span>
<span data-ttu-id="a7b5f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b5f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7b5f-116">-InputObject</span></span>
<span data-ttu-id="a7b5f-117">Oggetto di input agente</span><span class="sxs-lookup"><span data-stu-id="a7b5f-117">The agent input object</span></span>

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

### <span data-ttu-id="a7b5f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7b5f-118">-Name</span></span>
<span data-ttu-id="a7b5f-119">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="a7b5f-119">The agent name</span></span>

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

### <span data-ttu-id="a7b5f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b5f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7b5f-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a7b5f-121">The resource group name</span></span>

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

### <span data-ttu-id="a7b5f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7b5f-122">-ResourceId</span></span>
<span data-ttu-id="a7b5f-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="a7b5f-123">The agent resource id</span></span>

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

### <span data-ttu-id="a7b5f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7b5f-124">-ServerName</span></span>
<span data-ttu-id="a7b5f-125">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="a7b5f-125">The server name</span></span>

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

### <span data-ttu-id="a7b5f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7b5f-126">-Tag</span></span>
<span data-ttu-id="a7b5f-127">I tag da associare all'agente di SQL azure</span><span class="sxs-lookup"><span data-stu-id="a7b5f-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="a7b5f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7b5f-128">-Confirm</span></span>
<span data-ttu-id="a7b5f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b5f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b5f-130">-WhatIf</span></span>
<span data-ttu-id="a7b5f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7b5f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b5f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b5f-133">CommonParameters</span></span>
<span data-ttu-id="a7b5f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b5f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7b5f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b5f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7b5f-136">INPUTS</span></span>

### <span data-ttu-id="a7b5f-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a7b5f-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a7b5f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7b5f-138">OUTPUTS</span></span>

### <span data-ttu-id="a7b5f-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a7b5f-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a7b5f-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7b5f-140">NOTES</span></span>

## <span data-ttu-id="a7b5f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7b5f-141">RELATED LINKS</span></span>
