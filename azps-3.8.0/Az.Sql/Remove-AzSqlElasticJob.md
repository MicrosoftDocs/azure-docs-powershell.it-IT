---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021149"
---
# <span data-ttu-id="385bd-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="385bd-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="385bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="385bd-102">SYNOPSIS</span></span>
<span data-ttu-id="385bd-103">Rimuove un processo</span><span class="sxs-lookup"><span data-stu-id="385bd-103">Removes a job</span></span>

## <span data-ttu-id="385bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="385bd-104">SYNTAX</span></span>

### <span data-ttu-id="385bd-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="385bd-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385bd-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="385bd-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="385bd-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="385bd-108">DESCRIPTION</span></span>
<span data-ttu-id="385bd-109">Il cmdlet Remove-AzSqlElasticJob rimuove un processo</span><span class="sxs-lookup"><span data-stu-id="385bd-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="385bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="385bd-110">EXAMPLES</span></span>

### <span data-ttu-id="385bd-111">Esempio 1-rimozione di un processo</span><span class="sxs-lookup"><span data-stu-id="385bd-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="385bd-112">Rimuove un processo</span><span class="sxs-lookup"><span data-stu-id="385bd-112">Removes a job</span></span>

## <span data-ttu-id="385bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="385bd-113">PARAMETERS</span></span>

### <span data-ttu-id="385bd-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="385bd-114">-AgentName</span></span>
<span data-ttu-id="385bd-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="385bd-115">The agent name</span></span>

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

### <span data-ttu-id="385bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385bd-116">-DefaultProfile</span></span>
<span data-ttu-id="385bd-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="385bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385bd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="385bd-118">-Force</span></span>
<span data-ttu-id="385bd-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="385bd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="385bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="385bd-120">-InputObject</span></span>
<span data-ttu-id="385bd-121">Oggetto input processo</span><span class="sxs-lookup"><span data-stu-id="385bd-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="385bd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="385bd-122">-Name</span></span>
<span data-ttu-id="385bd-123">Il nome del processo</span><span class="sxs-lookup"><span data-stu-id="385bd-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="385bd-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="385bd-125">The resource group name</span></span>

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

### <span data-ttu-id="385bd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="385bd-126">-ResourceId</span></span>
<span data-ttu-id="385bd-127">ID risorsa agente</span><span class="sxs-lookup"><span data-stu-id="385bd-127">The agent resource id</span></span>

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

### <span data-ttu-id="385bd-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="385bd-128">-ServerName</span></span>
<span data-ttu-id="385bd-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="385bd-129">The server name</span></span>

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

### <span data-ttu-id="385bd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="385bd-130">-Confirm</span></span>
<span data-ttu-id="385bd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385bd-132">-WhatIf</span></span>
<span data-ttu-id="385bd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385bd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385bd-135">CommonParameters</span></span>
<span data-ttu-id="385bd-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385bd-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="385bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385bd-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="385bd-138">INPUTS</span></span>

### <span data-ttu-id="385bd-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="385bd-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="385bd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="385bd-140">OUTPUTS</span></span>

### <span data-ttu-id="385bd-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="385bd-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="385bd-142">Note</span><span class="sxs-lookup"><span data-stu-id="385bd-142">NOTES</span></span>

## <span data-ttu-id="385bd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="385bd-143">RELATED LINKS</span></span>
