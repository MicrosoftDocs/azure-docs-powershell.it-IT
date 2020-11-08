---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200136"
---
# <span data-ttu-id="65b5e-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="65b5e-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="65b5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="65b5e-103">Crea un nuovo gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="65b5e-103">Creates a new target group</span></span>

## <span data-ttu-id="65b5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b5e-104">SYNTAX</span></span>

### <span data-ttu-id="65b5e-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65b5e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b5e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="65b5e-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="65b5e-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b5e-108">DESCRIPTION</span></span>
<span data-ttu-id="65b5e-109">Il cmdlet New-AzSqlElasticJobTargetGroup crea un nuovo gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="65b5e-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="65b5e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b5e-110">EXAMPLES</span></span>

### <span data-ttu-id="65b5e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65b5e-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="65b5e-112">Crea un gruppo di destinazione vuoto</span><span class="sxs-lookup"><span data-stu-id="65b5e-112">Creates an empty target group</span></span>

## <span data-ttu-id="65b5e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65b5e-113">PARAMETERS</span></span>

### <span data-ttu-id="65b5e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="65b5e-114">-AgentName</span></span>
<span data-ttu-id="65b5e-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="65b5e-115">The agent name</span></span>

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

### <span data-ttu-id="65b5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b5e-116">-DefaultProfile</span></span>
<span data-ttu-id="65b5e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65b5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b5e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="65b5e-118">-Name</span></span>
<span data-ttu-id="65b5e-119">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="65b5e-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b5e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="65b5e-120">-ParentObject</span></span>
<span data-ttu-id="65b5e-121">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="65b5e-121">The agent input object</span></span>

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

### <span data-ttu-id="65b5e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="65b5e-122">-ParentResourceId</span></span>
<span data-ttu-id="65b5e-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="65b5e-123">The agent resource id</span></span>

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

### <span data-ttu-id="65b5e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b5e-124">-ResourceGroupName</span></span>
<span data-ttu-id="65b5e-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="65b5e-125">The resource group name</span></span>

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

### <span data-ttu-id="65b5e-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="65b5e-126">-ServerName</span></span>
<span data-ttu-id="65b5e-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="65b5e-127">The server name</span></span>

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

### <span data-ttu-id="65b5e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65b5e-128">-Confirm</span></span>
<span data-ttu-id="65b5e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b5e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b5e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b5e-130">-WhatIf</span></span>
<span data-ttu-id="65b5e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b5e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b5e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65b5e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b5e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b5e-133">CommonParameters</span></span>
<span data-ttu-id="65b5e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b5e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b5e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b5e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b5e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65b5e-136">INPUTS</span></span>

### <span data-ttu-id="65b5e-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="65b5e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="65b5e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b5e-138">OUTPUTS</span></span>

### <span data-ttu-id="65b5e-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="65b5e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="65b5e-140">Note</span><span class="sxs-lookup"><span data-stu-id="65b5e-140">NOTES</span></span>

## <span data-ttu-id="65b5e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b5e-141">RELATED LINKS</span></span>