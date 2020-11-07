---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857329"
---
# <span data-ttu-id="cfe9b-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="cfe9b-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="cfe9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe9b-103">Rimuove il gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-103">Removes the target group</span></span>

## <span data-ttu-id="cfe9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfe9b-104">SYNTAX</span></span>

### <span data-ttu-id="cfe9b-105">DefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfe9b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe9b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cfe9b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe9b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cfe9b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe9b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-108">DESCRIPTION</span></span>
<span data-ttu-id="cfe9b-109">Il cmdlet Remove-AzSqlElasticJobTargetGroup rimuove un gruppo di destinazione e le destinazioni</span><span class="sxs-lookup"><span data-stu-id="cfe9b-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="cfe9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfe9b-110">EXAMPLES</span></span>

### <span data-ttu-id="cfe9b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cfe9b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="cfe9b-112">Rimuove un gruppo di destinazione e le destinazioni</span><span class="sxs-lookup"><span data-stu-id="cfe9b-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="cfe9b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfe9b-113">PARAMETERS</span></span>

### <span data-ttu-id="cfe9b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cfe9b-114">-AgentName</span></span>
<span data-ttu-id="cfe9b-115">Nome dell'agente</span><span class="sxs-lookup"><span data-stu-id="cfe9b-115">The agent name</span></span>

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

### <span data-ttu-id="cfe9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe9b-116">-DefaultProfile</span></span>
<span data-ttu-id="cfe9b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe9b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cfe9b-118">-Force</span></span>
<span data-ttu-id="cfe9b-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cfe9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfe9b-120">-InputObject</span></span>
<span data-ttu-id="cfe9b-121">Oggetto gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe9b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfe9b-122">-Name</span></span>
<span data-ttu-id="cfe9b-123">Nome del gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="cfe9b-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cfe9b-125">The resource group name</span></span>

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

### <span data-ttu-id="cfe9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfe9b-126">-ResourceId</span></span>
<span data-ttu-id="cfe9b-127">ID risorsa gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cfe9b-127">The target group resource id</span></span>

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

### <span data-ttu-id="cfe9b-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cfe9b-128">-ServerName</span></span>
<span data-ttu-id="cfe9b-129">Nome del server</span><span class="sxs-lookup"><span data-stu-id="cfe9b-129">The server name</span></span>

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

### <span data-ttu-id="cfe9b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cfe9b-130">-Confirm</span></span>
<span data-ttu-id="cfe9b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe9b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe9b-132">-WhatIf</span></span>
<span data-ttu-id="cfe9b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe9b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe9b-135">CommonParameters</span></span>
<span data-ttu-id="cfe9b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe9b-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfe9b-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe9b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfe9b-138">INPUTS</span></span>

### <span data-ttu-id="cfe9b-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="cfe9b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="cfe9b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfe9b-140">OUTPUTS</span></span>

### <span data-ttu-id="cfe9b-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="cfe9b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="cfe9b-142">Note</span><span class="sxs-lookup"><span data-stu-id="cfe9b-142">NOTES</span></span>

## <span data-ttu-id="cfe9b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfe9b-143">RELATED LINKS</span></span>
