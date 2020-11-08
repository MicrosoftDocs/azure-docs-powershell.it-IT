---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019473"
---
# <span data-ttu-id="5ac10-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="5ac10-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="5ac10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ac10-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac10-103">Ottiene uno o più processi</span><span class="sxs-lookup"><span data-stu-id="5ac10-103">Gets one or more jobs</span></span>

## <span data-ttu-id="5ac10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ac10-104">SYNTAX</span></span>

### <span data-ttu-id="5ac10-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ac10-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac10-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ac10-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac10-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5ac10-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ac10-108">DESCRIPTION</span></span>
<span data-ttu-id="5ac10-109">Il cmdlet Get-AzSqlElasticJob ottiene uno o più processi</span><span class="sxs-lookup"><span data-stu-id="5ac10-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="5ac10-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ac10-110">EXAMPLES</span></span>

### <span data-ttu-id="5ac10-111">Esempio 1-Ottiene un processo</span><span class="sxs-lookup"><span data-stu-id="5ac10-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="5ac10-112">Ottiene un processo</span><span class="sxs-lookup"><span data-stu-id="5ac10-112">Gets a job</span></span>

## <span data-ttu-id="5ac10-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ac10-113">PARAMETERS</span></span>

### <span data-ttu-id="5ac10-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5ac10-114">-AgentName</span></span>
<span data-ttu-id="5ac10-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="5ac10-115">The agent name</span></span>

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

### <span data-ttu-id="5ac10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac10-116">-DefaultProfile</span></span>
<span data-ttu-id="5ac10-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac10-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ac10-118">-Name</span></span>
<span data-ttu-id="5ac10-119">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="5ac10-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac10-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ac10-120">-ParentObject</span></span>
<span data-ttu-id="5ac10-121">Oggetto di input dell'agente</span><span class="sxs-lookup"><span data-stu-id="5ac10-121">The agent input object</span></span>

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

### <span data-ttu-id="5ac10-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac10-122">-ParentResourceId</span></span>
<span data-ttu-id="5ac10-123">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="5ac10-123">The agent resource id</span></span>

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

### <span data-ttu-id="5ac10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac10-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ac10-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5ac10-125">The resource group name</span></span>

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

### <span data-ttu-id="5ac10-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5ac10-126">-ServerName</span></span>
<span data-ttu-id="5ac10-127">Nome del server</span><span class="sxs-lookup"><span data-stu-id="5ac10-127">The server name</span></span>

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

### <span data-ttu-id="5ac10-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac10-128">CommonParameters</span></span>
<span data-ttu-id="5ac10-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac10-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac10-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ac10-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac10-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ac10-131">INPUTS</span></span>

### <span data-ttu-id="5ac10-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5ac10-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5ac10-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ac10-133">OUTPUTS</span></span>

### <span data-ttu-id="5ac10-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="5ac10-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="5ac10-135">Note</span><span class="sxs-lookup"><span data-stu-id="5ac10-135">NOTES</span></span>

## <span data-ttu-id="5ac10-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ac10-136">RELATED LINKS</span></span>
