---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207890"
---
# <span data-ttu-id="cd500-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="cd500-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="cd500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd500-102">SYNOPSIS</span></span>
<span data-ttu-id="cd500-103">Crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="cd500-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="cd500-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd500-104">SYNTAX</span></span>

### <span data-ttu-id="cd500-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd500-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd500-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd500-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd500-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd500-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd500-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd500-108">DESCRIPTION</span></span>
<span data-ttu-id="cd500-109">Il cmdlet New-AzSqlElasticJobAgent crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="cd500-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="cd500-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd500-110">EXAMPLES</span></span>

### <span data-ttu-id="cd500-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd500-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="cd500-112">Crea un nuovo agente di processo flessibile</span><span class="sxs-lookup"><span data-stu-id="cd500-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="cd500-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd500-113">PARAMETERS</span></span>

### <span data-ttu-id="cd500-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd500-114">-DatabaseName</span></span>
<span data-ttu-id="cd500-115">Nome del database</span><span class="sxs-lookup"><span data-stu-id="cd500-115">The database name</span></span>

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

### <span data-ttu-id="cd500-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cd500-116">-DatabaseObject</span></span>
<span data-ttu-id="cd500-117">Oggetto di database controllo agente</span><span class="sxs-lookup"><span data-stu-id="cd500-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="cd500-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="cd500-118">-DatabaseResourceId</span></span>
<span data-ttu-id="cd500-119">ID risorsa database controllo agente</span><span class="sxs-lookup"><span data-stu-id="cd500-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="cd500-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd500-120">-DefaultProfile</span></span>
<span data-ttu-id="cd500-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd500-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd500-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cd500-122">-Name</span></span>
<span data-ttu-id="cd500-123">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="cd500-123">The Agent Name</span></span>

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

### <span data-ttu-id="cd500-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd500-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd500-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cd500-125">The resource group name</span></span>

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

### <span data-ttu-id="cd500-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd500-126">-ServerName</span></span>
<span data-ttu-id="cd500-127">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="cd500-127">The server name</span></span>

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

### <span data-ttu-id="cd500-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd500-128">-Tag</span></span>
<span data-ttu-id="cd500-129">Tag agente</span><span class="sxs-lookup"><span data-stu-id="cd500-129">The Agent Tags</span></span>

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

### <span data-ttu-id="cd500-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd500-130">-Confirm</span></span>
<span data-ttu-id="cd500-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd500-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd500-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd500-132">-WhatIf</span></span>
<span data-ttu-id="cd500-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd500-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd500-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd500-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd500-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd500-135">CommonParameters</span></span>
<span data-ttu-id="cd500-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd500-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd500-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd500-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd500-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd500-138">INPUTS</span></span>

### <span data-ttu-id="cd500-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cd500-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cd500-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd500-140">OUTPUTS</span></span>

### <span data-ttu-id="cd500-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="cd500-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="cd500-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd500-142">NOTES</span></span>

## <span data-ttu-id="cd500-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd500-143">RELATED LINKS</span></span>
