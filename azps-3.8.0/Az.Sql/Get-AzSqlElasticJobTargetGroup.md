---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865396"
---
# <span data-ttu-id="84047-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="84047-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="84047-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84047-102">SYNOPSIS</span></span>
<span data-ttu-id="84047-103">Ottiene uno o più gruppi di destinazione del processo</span><span class="sxs-lookup"><span data-stu-id="84047-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="84047-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84047-104">SYNTAX</span></span>

### <span data-ttu-id="84047-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84047-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84047-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="84047-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84047-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="84047-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84047-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84047-108">DESCRIPTION</span></span>
<span data-ttu-id="84047-109">Il cmdlet Get-AzSqlElasticJobTargetGroup ottiene un gruppo di destinazione e le destinazioni</span><span class="sxs-lookup"><span data-stu-id="84047-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="84047-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84047-110">EXAMPLES</span></span>

### <span data-ttu-id="84047-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84047-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="84047-112">Ottiene un gruppo di destinazione e le destinazioni</span><span class="sxs-lookup"><span data-stu-id="84047-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="84047-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84047-113">PARAMETERS</span></span>

### <span data-ttu-id="84047-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="84047-114">-AgentName</span></span>
<span data-ttu-id="84047-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="84047-115">The agent name</span></span>

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

### <span data-ttu-id="84047-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84047-116">-DefaultProfile</span></span>
<span data-ttu-id="84047-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84047-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84047-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="84047-118">-Name</span></span>
<span data-ttu-id="84047-119">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="84047-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84047-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="84047-120">-ParentObject</span></span>
<span data-ttu-id="84047-121">Oggetto Agent</span><span class="sxs-lookup"><span data-stu-id="84047-121">The agent object</span></span>

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

### <span data-ttu-id="84047-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="84047-122">-ParentResourceId</span></span>
<span data-ttu-id="84047-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="84047-123">The agent resource id</span></span>

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

### <span data-ttu-id="84047-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84047-124">-ResourceGroupName</span></span>
<span data-ttu-id="84047-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84047-125">The resource group name</span></span>

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

### <span data-ttu-id="84047-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="84047-126">-ServerName</span></span>
<span data-ttu-id="84047-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="84047-127">The server name</span></span>

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

### <span data-ttu-id="84047-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84047-128">CommonParameters</span></span>
<span data-ttu-id="84047-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84047-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84047-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84047-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84047-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84047-131">INPUTS</span></span>

### <span data-ttu-id="84047-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="84047-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="84047-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84047-133">OUTPUTS</span></span>

### <span data-ttu-id="84047-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="84047-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="84047-135">Note</span><span class="sxs-lookup"><span data-stu-id="84047-135">NOTES</span></span>

## <span data-ttu-id="84047-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84047-136">RELATED LINKS</span></span>
