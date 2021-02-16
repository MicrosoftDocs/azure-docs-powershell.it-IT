---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195974"
---
# <span data-ttu-id="aa00e-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="aa00e-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="aa00e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa00e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa00e-103">Aggiorna un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="aa00e-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="aa00e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa00e-104">SYNTAX</span></span>

### <span data-ttu-id="aa00e-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa00e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa00e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa00e-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa00e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa00e-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa00e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa00e-108">DESCRIPTION</span></span>
<span data-ttu-id="aa00e-109">Il cmdlet Set-AzSqlElasticJobAgent aggiorna gli agenti di processo elastico</span><span class="sxs-lookup"><span data-stu-id="aa00e-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="aa00e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa00e-110">EXAMPLES</span></span>

### <span data-ttu-id="aa00e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa00e-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="aa00e-112">Aggiorna un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="aa00e-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="aa00e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa00e-113">PARAMETERS</span></span>

### <span data-ttu-id="aa00e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa00e-114">-DefaultProfile</span></span>
<span data-ttu-id="aa00e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa00e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa00e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa00e-116">-InputObject</span></span>
<span data-ttu-id="aa00e-117">Oggetto di input agente</span><span class="sxs-lookup"><span data-stu-id="aa00e-117">The agent input object</span></span>

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

### <span data-ttu-id="aa00e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="aa00e-118">-Name</span></span>
<span data-ttu-id="aa00e-119">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="aa00e-119">The agent name</span></span>

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

### <span data-ttu-id="aa00e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa00e-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa00e-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="aa00e-121">The resource group name</span></span>

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

### <span data-ttu-id="aa00e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa00e-122">-ResourceId</span></span>
<span data-ttu-id="aa00e-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="aa00e-123">The agent resource id</span></span>

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

### <span data-ttu-id="aa00e-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa00e-124">-ServerName</span></span>
<span data-ttu-id="aa00e-125">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="aa00e-125">The server name</span></span>

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

### <span data-ttu-id="aa00e-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa00e-126">-Tag</span></span>
<span data-ttu-id="aa00e-127">I tag da associare all'agente SQL database di Azure</span><span class="sxs-lookup"><span data-stu-id="aa00e-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="aa00e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa00e-128">-Confirm</span></span>
<span data-ttu-id="aa00e-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa00e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa00e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa00e-130">-WhatIf</span></span>
<span data-ttu-id="aa00e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa00e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa00e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa00e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa00e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa00e-133">CommonParameters</span></span>
<span data-ttu-id="aa00e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa00e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa00e-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa00e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa00e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa00e-136">INPUTS</span></span>

### <span data-ttu-id="aa00e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="aa00e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="aa00e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa00e-138">OUTPUTS</span></span>

### <span data-ttu-id="aa00e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="aa00e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="aa00e-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa00e-140">NOTES</span></span>

## <span data-ttu-id="aa00e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa00e-141">RELATED LINKS</span></span>
