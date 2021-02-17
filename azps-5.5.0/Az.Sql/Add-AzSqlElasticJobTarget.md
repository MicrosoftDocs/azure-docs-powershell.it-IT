---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191134"
---
# <span data-ttu-id="80a86-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="80a86-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="80a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a86-102">SYNOPSIS</span></span>
<span data-ttu-id="80a86-103">Aggiunge una destinazione a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="80a86-103">Adds a target to a target group</span></span>

## <span data-ttu-id="80a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80a86-104">SYNTAX</span></span>

### <span data-ttu-id="80a86-105">SqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80a86-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="80a86-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80a86-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="80a86-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="80a86-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="80a86-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="80a86-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80a86-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80a86-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a86-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80a86-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a86-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80a86-114">DESCRIPTION</span></span>
<span data-ttu-id="80a86-115">Il cmdlet Add-AzSqlElasticJobTarget aggiunge una risorsa di destinazione a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="80a86-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="80a86-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80a86-116">EXAMPLES</span></span>

### <span data-ttu-id="80a86-117">Esempio 1: Aggiungere una destinazione del server</span><span class="sxs-lookup"><span data-stu-id="80a86-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="80a86-118">Esempio 2: Aggiungere una destinazione di database</span><span class="sxs-lookup"><span data-stu-id="80a86-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="80a86-119">Esempio 3: Aggiungere una destinazione del pool flessibile</span><span class="sxs-lookup"><span data-stu-id="80a86-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="80a86-120">Esempio 4: Aggiungere una destinazione di una mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="80a86-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="80a86-121">Aggiunge una destinazione (server, pool flessibile, database e mappa partizionata) a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="80a86-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="80a86-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80a86-122">PARAMETERS</span></span>

### <span data-ttu-id="80a86-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="80a86-123">-AgentName</span></span>
<span data-ttu-id="80a86-124">Il nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="80a86-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="80a86-125">-AgentServerName</span></span>
<span data-ttu-id="80a86-126">Il nome del server.</span><span class="sxs-lookup"><span data-stu-id="80a86-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80a86-127">-DatabaseName</span></span>
<span data-ttu-id="80a86-128">Nome destinazione database</span><span class="sxs-lookup"><span data-stu-id="80a86-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a86-129">-DefaultProfile</span></span>
<span data-ttu-id="80a86-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80a86-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a86-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="80a86-131">-ElasticPoolName</span></span>
<span data-ttu-id="80a86-132">Nome destinazione pool elastico</span><span class="sxs-lookup"><span data-stu-id="80a86-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="80a86-133">-Exclude</span></span>
<span data-ttu-id="80a86-134">Esclude una destinazione.</span><span class="sxs-lookup"><span data-stu-id="80a86-134">Excludes a target.</span></span>

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

### <span data-ttu-id="80a86-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80a86-135">-ParentObject</span></span>
<span data-ttu-id="80a86-136">Oggetto gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80a86-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80a86-137">-ParentResourceId</span></span>
<span data-ttu-id="80a86-138">ID risorsa del gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80a86-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="80a86-139">-RefreshCredentialName</span></span>
<span data-ttu-id="80a86-140">Aggiorna nome credenziali</span><span class="sxs-lookup"><span data-stu-id="80a86-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a86-141">-ResourceGroupName</span></span>
<span data-ttu-id="80a86-142">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="80a86-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80a86-143">-ServerName</span></span>
<span data-ttu-id="80a86-144">Nome di destinazione del server</span><span class="sxs-lookup"><span data-stu-id="80a86-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="80a86-145">-ShardMapName</span></span>
<span data-ttu-id="80a86-146">Nome destinazione mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="80a86-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="80a86-147">-TargetGroupName</span></span>
<span data-ttu-id="80a86-148">Nome del gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80a86-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a86-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80a86-149">-Confirm</span></span>
<span data-ttu-id="80a86-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a86-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a86-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a86-151">-WhatIf</span></span>
<span data-ttu-id="80a86-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80a86-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a86-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80a86-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a86-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a86-154">CommonParameters</span></span>
<span data-ttu-id="80a86-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a86-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a86-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80a86-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a86-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="80a86-157">INPUTS</span></span>

### <span data-ttu-id="80a86-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="80a86-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="80a86-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80a86-159">OUTPUTS</span></span>

### <span data-ttu-id="80a86-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="80a86-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="80a86-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="80a86-161">NOTES</span></span>

## <span data-ttu-id="80a86-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80a86-162">RELATED LINKS</span></span>
