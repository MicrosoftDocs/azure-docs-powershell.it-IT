---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982014"
---
# <span data-ttu-id="fd56e-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="fd56e-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="fd56e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd56e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd56e-103">Crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="fd56e-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="fd56e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd56e-104">SYNTAX</span></span>

### <span data-ttu-id="fd56e-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd56e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd56e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd56e-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd56e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd56e-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd56e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd56e-108">DESCRIPTION</span></span>
<span data-ttu-id="fd56e-109">Il cmdlet New-AzSqlElasticJobAgent crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="fd56e-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="fd56e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd56e-110">EXAMPLES</span></span>

### <span data-ttu-id="fd56e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd56e-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="fd56e-112">Crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="fd56e-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="fd56e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd56e-113">PARAMETERS</span></span>

### <span data-ttu-id="fd56e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd56e-114">-DatabaseName</span></span>
<span data-ttu-id="fd56e-115">Il nome del database</span><span class="sxs-lookup"><span data-stu-id="fd56e-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd56e-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fd56e-116">-DatabaseObject</span></span>
<span data-ttu-id="fd56e-117">Oggetto di database controllo agente</span><span class="sxs-lookup"><span data-stu-id="fd56e-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd56e-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fd56e-118">-DatabaseResourceId</span></span>
<span data-ttu-id="fd56e-119">ID risorsa database controllo agente</span><span class="sxs-lookup"><span data-stu-id="fd56e-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="fd56e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd56e-120">-DefaultProfile</span></span>
<span data-ttu-id="fd56e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd56e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd56e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd56e-122">-Name</span></span>
<span data-ttu-id="fd56e-123">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="fd56e-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd56e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd56e-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd56e-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fd56e-125">The resource group name</span></span>

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

### <span data-ttu-id="fd56e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd56e-126">-ServerName</span></span>
<span data-ttu-id="fd56e-127">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="fd56e-127">The server name</span></span>

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

### <span data-ttu-id="fd56e-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd56e-128">-Tag</span></span>
<span data-ttu-id="fd56e-129">Tag agente</span><span class="sxs-lookup"><span data-stu-id="fd56e-129">The Agent Tags</span></span>

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

### <span data-ttu-id="fd56e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd56e-130">-Confirm</span></span>
<span data-ttu-id="fd56e-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd56e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd56e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd56e-132">-WhatIf</span></span>
<span data-ttu-id="fd56e-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd56e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd56e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd56e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd56e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd56e-135">CommonParameters</span></span>
<span data-ttu-id="fd56e-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd56e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd56e-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd56e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd56e-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd56e-138">INPUTS</span></span>

### <span data-ttu-id="fd56e-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fd56e-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fd56e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd56e-140">OUTPUTS</span></span>

### <span data-ttu-id="fd56e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="fd56e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fd56e-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd56e-142">NOTES</span></span>

## <span data-ttu-id="fd56e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd56e-143">RELATED LINKS</span></span>
