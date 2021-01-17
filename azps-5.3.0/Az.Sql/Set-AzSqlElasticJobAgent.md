---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475464"
---
# <span data-ttu-id="2af55-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2af55-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2af55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2af55-102">SYNOPSIS</span></span>
<span data-ttu-id="2af55-103">Aggiorna un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="2af55-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="2af55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2af55-104">SYNTAX</span></span>

### <span data-ttu-id="2af55-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2af55-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2af55-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2af55-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2af55-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2af55-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af55-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2af55-108">DESCRIPTION</span></span>
<span data-ttu-id="2af55-109">Il cmdlet Set-AzSqlElasticJobAgent aggiorna gli agenti di processo elastici</span><span class="sxs-lookup"><span data-stu-id="2af55-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="2af55-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2af55-110">EXAMPLES</span></span>

### <span data-ttu-id="2af55-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2af55-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="2af55-112">Aggiorna un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="2af55-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="2af55-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2af55-113">PARAMETERS</span></span>

### <span data-ttu-id="2af55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af55-114">-DefaultProfile</span></span>
<span data-ttu-id="2af55-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2af55-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2af55-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2af55-116">-InputObject</span></span>
<span data-ttu-id="2af55-117">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="2af55-117">The agent input object</span></span>

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

### <span data-ttu-id="2af55-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2af55-118">-Name</span></span>
<span data-ttu-id="2af55-119">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="2af55-119">The agent name</span></span>

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

### <span data-ttu-id="2af55-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af55-120">-ResourceGroupName</span></span>
<span data-ttu-id="2af55-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2af55-121">The resource group name</span></span>

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

### <span data-ttu-id="2af55-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2af55-122">-ResourceId</span></span>
<span data-ttu-id="2af55-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="2af55-123">The agent resource id</span></span>

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

### <span data-ttu-id="2af55-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2af55-124">-ServerName</span></span>
<span data-ttu-id="2af55-125">Nome del server</span><span class="sxs-lookup"><span data-stu-id="2af55-125">The server name</span></span>

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

### <span data-ttu-id="2af55-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2af55-126">-Tag</span></span>
<span data-ttu-id="2af55-127">Tag da associare all'agente di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="2af55-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="2af55-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2af55-128">-Confirm</span></span>
<span data-ttu-id="2af55-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af55-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2af55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af55-130">-WhatIf</span></span>
<span data-ttu-id="2af55-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2af55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af55-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2af55-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2af55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af55-133">CommonParameters</span></span>
<span data-ttu-id="2af55-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2af55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af55-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2af55-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af55-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2af55-136">INPUTS</span></span>

### <span data-ttu-id="2af55-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2af55-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2af55-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2af55-138">OUTPUTS</span></span>

### <span data-ttu-id="2af55-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2af55-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2af55-140">Note</span><span class="sxs-lookup"><span data-stu-id="2af55-140">NOTES</span></span>

## <span data-ttu-id="2af55-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2af55-141">RELATED LINKS</span></span>
