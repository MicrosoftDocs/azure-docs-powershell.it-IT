---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957886"
---
# <span data-ttu-id="db1aa-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="db1aa-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="db1aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="db1aa-103">Rimuove l'agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="db1aa-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="db1aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db1aa-104">SYNTAX</span></span>

### <span data-ttu-id="db1aa-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db1aa-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1aa-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="db1aa-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db1aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="db1aa-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db1aa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db1aa-108">DESCRIPTION</span></span>
<span data-ttu-id="db1aa-109">Il cmdlet Remove-AzSqlElasticJobAgent rimuove un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="db1aa-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="db1aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db1aa-110">EXAMPLES</span></span>

### <span data-ttu-id="db1aa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db1aa-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="db1aa-112">Rimuove un agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="db1aa-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="db1aa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db1aa-113">PARAMETERS</span></span>

### <span data-ttu-id="db1aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1aa-114">-DefaultProfile</span></span>
<span data-ttu-id="db1aa-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db1aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db1aa-116">-Force</span><span class="sxs-lookup"><span data-stu-id="db1aa-116">-Force</span></span>
<span data-ttu-id="db1aa-117">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="db1aa-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db1aa-118">-InputObject</span></span>
<span data-ttu-id="db1aa-119">Oggetto agente</span><span class="sxs-lookup"><span data-stu-id="db1aa-119">The agent object</span></span>

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

### <span data-ttu-id="db1aa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="db1aa-120">-Name</span></span>
<span data-ttu-id="db1aa-121">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="db1aa-121">The agent name</span></span>

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

### <span data-ttu-id="db1aa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1aa-122">-ResourceGroupName</span></span>
<span data-ttu-id="db1aa-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="db1aa-123">The resource group name</span></span>

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

### <span data-ttu-id="db1aa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db1aa-124">-ResourceId</span></span>
<span data-ttu-id="db1aa-125">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="db1aa-125">The agent resource id</span></span>

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

### <span data-ttu-id="db1aa-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db1aa-126">-ServerName</span></span>
<span data-ttu-id="db1aa-127">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="db1aa-127">The server name</span></span>

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

### <span data-ttu-id="db1aa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db1aa-128">-Confirm</span></span>
<span data-ttu-id="db1aa-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db1aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db1aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1aa-130">-WhatIf</span></span>
<span data-ttu-id="db1aa-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db1aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db1aa-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db1aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db1aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1aa-133">CommonParameters</span></span>
<span data-ttu-id="db1aa-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1aa-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db1aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1aa-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="db1aa-136">INPUTS</span></span>

### <span data-ttu-id="db1aa-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="db1aa-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="db1aa-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db1aa-138">OUTPUTS</span></span>

### <span data-ttu-id="db1aa-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="db1aa-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="db1aa-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="db1aa-140">NOTES</span></span>

## <span data-ttu-id="db1aa-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db1aa-141">RELATED LINKS</span></span>
