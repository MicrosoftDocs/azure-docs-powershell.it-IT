---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: e4517f99c44a734902f2d75ec7d432ad73ad8038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857389"
---
# <span data-ttu-id="88e04-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="88e04-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="88e04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88e04-102">SYNOPSIS</span></span>
<span data-ttu-id="88e04-103">Crea un nuovo agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="88e04-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="88e04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88e04-104">SYNTAX</span></span>

### <span data-ttu-id="88e04-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88e04-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88e04-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="88e04-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e04-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="88e04-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88e04-108">DESCRIPTION</span></span>
<span data-ttu-id="88e04-109">Il cmdlet New-AzSqlElasticJobAgent crea un nuovo agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="88e04-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="88e04-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88e04-110">EXAMPLES</span></span>

### <span data-ttu-id="88e04-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88e04-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="88e04-112">Crea un nuovo agente del processo elastico</span><span class="sxs-lookup"><span data-stu-id="88e04-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="88e04-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88e04-113">PARAMETERS</span></span>

### <span data-ttu-id="88e04-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88e04-114">-DatabaseName</span></span>
<span data-ttu-id="88e04-115">Nome del database</span><span class="sxs-lookup"><span data-stu-id="88e04-115">The database name</span></span>

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

### <span data-ttu-id="88e04-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="88e04-116">-DatabaseObject</span></span>
<span data-ttu-id="88e04-117">Oggetto database controllo agente</span><span class="sxs-lookup"><span data-stu-id="88e04-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="88e04-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="88e04-118">-DatabaseResourceId</span></span>
<span data-ttu-id="88e04-119">ID risorsa database controllo agente</span><span class="sxs-lookup"><span data-stu-id="88e04-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="88e04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e04-120">-DefaultProfile</span></span>
<span data-ttu-id="88e04-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88e04-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e04-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="88e04-122">-Name</span></span>
<span data-ttu-id="88e04-123">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="88e04-123">The Agent Name</span></span>

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

### <span data-ttu-id="88e04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e04-124">-ResourceGroupName</span></span>
<span data-ttu-id="88e04-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="88e04-125">The resource group name</span></span>

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

### <span data-ttu-id="88e04-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="88e04-126">-ServerName</span></span>
<span data-ttu-id="88e04-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="88e04-127">The server name</span></span>

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

### <span data-ttu-id="88e04-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="88e04-128">-Tag</span></span>
<span data-ttu-id="88e04-129">Tag Agent</span><span class="sxs-lookup"><span data-stu-id="88e04-129">The Agent Tags</span></span>

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

### <span data-ttu-id="88e04-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88e04-130">-Confirm</span></span>
<span data-ttu-id="88e04-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e04-132">-WhatIf</span></span>
<span data-ttu-id="88e04-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e04-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88e04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e04-135">CommonParameters</span></span>
<span data-ttu-id="88e04-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e04-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88e04-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e04-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88e04-138">INPUTS</span></span>

### <span data-ttu-id="88e04-139">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="88e04-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="88e04-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88e04-140">OUTPUTS</span></span>

### <span data-ttu-id="88e04-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="88e04-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="88e04-142">Note</span><span class="sxs-lookup"><span data-stu-id="88e04-142">NOTES</span></span>

## <span data-ttu-id="88e04-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88e04-143">RELATED LINKS</span></span>
