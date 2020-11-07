---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 5f8b237a6f7d08fc0339d3ba34d253bc457dd49f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857341"
---
# <span data-ttu-id="46d82-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="46d82-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="46d82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46d82-102">SYNOPSIS</span></span>
<span data-ttu-id="46d82-103">Rimuove l'agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="46d82-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="46d82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46d82-104">SYNTAX</span></span>

### <span data-ttu-id="46d82-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="46d82-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d82-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="46d82-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d82-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46d82-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d82-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46d82-108">DESCRIPTION</span></span>
<span data-ttu-id="46d82-109">Il cmdlet Remove-AzSqlElasticJobAgent rimuove un agente processo flessibile</span><span class="sxs-lookup"><span data-stu-id="46d82-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="46d82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46d82-110">EXAMPLES</span></span>

### <span data-ttu-id="46d82-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46d82-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="46d82-112">Rimuove un agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="46d82-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="46d82-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46d82-113">PARAMETERS</span></span>

### <span data-ttu-id="46d82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d82-114">-DefaultProfile</span></span>
<span data-ttu-id="46d82-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46d82-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d82-116">-Force</span><span class="sxs-lookup"><span data-stu-id="46d82-116">-Force</span></span>
<span data-ttu-id="46d82-117">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="46d82-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="46d82-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46d82-118">-InputObject</span></span>
<span data-ttu-id="46d82-119">Oggetto Agent</span><span class="sxs-lookup"><span data-stu-id="46d82-119">The agent object</span></span>

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

### <span data-ttu-id="46d82-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="46d82-120">-Name</span></span>
<span data-ttu-id="46d82-121">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="46d82-121">The agent name</span></span>

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

### <span data-ttu-id="46d82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d82-122">-ResourceGroupName</span></span>
<span data-ttu-id="46d82-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="46d82-123">The resource group name</span></span>

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

### <span data-ttu-id="46d82-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46d82-124">-ResourceId</span></span>
<span data-ttu-id="46d82-125">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="46d82-125">The agent resource id</span></span>

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

### <span data-ttu-id="46d82-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="46d82-126">-ServerName</span></span>
<span data-ttu-id="46d82-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="46d82-127">The server name</span></span>

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

### <span data-ttu-id="46d82-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46d82-128">-Confirm</span></span>
<span data-ttu-id="46d82-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d82-130">-WhatIf</span></span>
<span data-ttu-id="46d82-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46d82-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d82-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46d82-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d82-133">CommonParameters</span></span>
<span data-ttu-id="46d82-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d82-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d82-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d82-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46d82-136">INPUTS</span></span>

### <span data-ttu-id="46d82-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="46d82-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="46d82-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46d82-138">OUTPUTS</span></span>

### <span data-ttu-id="46d82-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="46d82-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="46d82-140">Note</span><span class="sxs-lookup"><span data-stu-id="46d82-140">NOTES</span></span>

## <span data-ttu-id="46d82-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46d82-141">RELATED LINKS</span></span>
