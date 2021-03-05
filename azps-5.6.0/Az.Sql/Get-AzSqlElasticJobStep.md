---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: d70a0b6abd31d4104301e877fb21bf1d0589a24f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999661"
---
# <span data-ttu-id="b1519-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="b1519-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="b1519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1519-102">SYNOPSIS</span></span>
<span data-ttu-id="b1519-103">Ottiene uno o più passaggi di processo</span><span class="sxs-lookup"><span data-stu-id="b1519-103">Gets one or more job steps</span></span>

## <span data-ttu-id="b1519-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1519-104">SYNTAX</span></span>

### <span data-ttu-id="b1519-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1519-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1519-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="b1519-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1519-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1519-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1519-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="b1519-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1519-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b1519-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1519-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1519-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1519-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1519-111">DESCRIPTION</span></span>
<span data-ttu-id="b1519-112">Il cmdlet Get-AzSqlElasticJobStep cmdlet ottiene uno o più passaggi di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="b1519-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="b1519-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1519-113">EXAMPLES</span></span>

### <span data-ttu-id="b1519-114">Esempio 1: Ottiene un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="b1519-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="b1519-115">Ottiene un passaggio di processo da un processo</span><span class="sxs-lookup"><span data-stu-id="b1519-115">Gets a job step from a job</span></span>

## <span data-ttu-id="b1519-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1519-116">PARAMETERS</span></span>

### <span data-ttu-id="b1519-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b1519-117">-AgentName</span></span>
<span data-ttu-id="b1519-118">Il nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="b1519-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1519-119">-DefaultProfile</span></span>
<span data-ttu-id="b1519-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1519-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1519-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="b1519-121">-JobName</span></span>
<span data-ttu-id="b1519-122">Nome del processo</span><span class="sxs-lookup"><span data-stu-id="b1519-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b1519-123">-Name</span></span>
<span data-ttu-id="b1519-124">Nome della fase del processo</span><span class="sxs-lookup"><span data-stu-id="b1519-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b1519-125">-ParentObject</span></span>
<span data-ttu-id="b1519-126">Oggetto di input del processo</span><span class="sxs-lookup"><span data-stu-id="b1519-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1519-127">-ParentResourceId</span></span>
<span data-ttu-id="b1519-128">ID risorsa processo</span><span class="sxs-lookup"><span data-stu-id="b1519-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1519-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1519-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b1519-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1519-131">-ServerName</span></span>
<span data-ttu-id="b1519-132">Il nome del server</span><span class="sxs-lookup"><span data-stu-id="b1519-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-133">-Version</span><span class="sxs-lookup"><span data-stu-id="b1519-133">-Version</span></span>
<span data-ttu-id="b1519-134">Nome della fase del processo</span><span class="sxs-lookup"><span data-stu-id="b1519-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1519-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1519-135">CommonParameters</span></span>
<span data-ttu-id="b1519-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1519-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1519-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1519-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1519-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1519-138">INPUTS</span></span>

### <span data-ttu-id="b1519-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="b1519-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="b1519-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1519-140">OUTPUTS</span></span>

### <span data-ttu-id="b1519-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="b1519-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b1519-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1519-142">NOTES</span></span>

## <span data-ttu-id="b1519-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1519-143">RELATED LINKS</span></span>
