---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 3a5c9284da784324b6b0887b836189c58077faa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961533"
---
# <span data-ttu-id="f1c30-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="f1c30-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="f1c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c30-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c30-103">Aggiunge una destinazione a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="f1c30-103">Adds a target to a target group</span></span>

## <span data-ttu-id="f1c30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1c30-104">SYNTAX</span></span>

### <span data-ttu-id="f1c30-105">SqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1c30-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="f1c30-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1c30-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="f1c30-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f1c30-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f1c30-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f1c30-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c30-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c30-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c30-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c30-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c30-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1c30-114">DESCRIPTION</span></span>
<span data-ttu-id="f1c30-115">Il cmdlet Add-AzSqlElasticJobTarget aggiunge una risorsa di destinazione a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="f1c30-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="f1c30-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1c30-116">EXAMPLES</span></span>

### <span data-ttu-id="f1c30-117">Esempio 1: Aggiungere una destinazione del server</span><span class="sxs-lookup"><span data-stu-id="f1c30-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="f1c30-118">Esempio 2: Aggiungere una destinazione di database</span><span class="sxs-lookup"><span data-stu-id="f1c30-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="f1c30-119">Esempio 3: Aggiungere una destinazione del pool flessibile</span><span class="sxs-lookup"><span data-stu-id="f1c30-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="f1c30-120">Esempio 4: Aggiungere una destinazione di una mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="f1c30-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="f1c30-121">Aggiunge una destinazione (server, pool flessibile, database e mappa partizionata) a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="f1c30-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="f1c30-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c30-122">PARAMETERS</span></span>

### <span data-ttu-id="f1c30-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f1c30-123">-AgentName</span></span>
<span data-ttu-id="f1c30-124">Il nome dell'agente.</span><span class="sxs-lookup"><span data-stu-id="f1c30-124">The agent name.</span></span>

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

### <span data-ttu-id="f1c30-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="f1c30-125">-AgentServerName</span></span>
<span data-ttu-id="f1c30-126">Il nome del server.</span><span class="sxs-lookup"><span data-stu-id="f1c30-126">The server name.</span></span>

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

### <span data-ttu-id="f1c30-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1c30-127">-DatabaseName</span></span>
<span data-ttu-id="f1c30-128">Nome destinazione database</span><span class="sxs-lookup"><span data-stu-id="f1c30-128">Database Target Name</span></span>

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

### <span data-ttu-id="f1c30-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c30-129">-DefaultProfile</span></span>
<span data-ttu-id="f1c30-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c30-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c30-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f1c30-131">-ElasticPoolName</span></span>
<span data-ttu-id="f1c30-132">Nome destinazione pool elastico</span><span class="sxs-lookup"><span data-stu-id="f1c30-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="f1c30-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="f1c30-133">-Exclude</span></span>
<span data-ttu-id="f1c30-134">Esclude una destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1c30-134">Excludes a target.</span></span>

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

### <span data-ttu-id="f1c30-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f1c30-135">-ParentObject</span></span>
<span data-ttu-id="f1c30-136">Oggetto gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1c30-136">The target group object.</span></span>

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

### <span data-ttu-id="f1c30-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c30-137">-ParentResourceId</span></span>
<span data-ttu-id="f1c30-138">ID della risorsa del gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1c30-138">The target group resource id.</span></span>

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

### <span data-ttu-id="f1c30-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="f1c30-139">-RefreshCredentialName</span></span>
<span data-ttu-id="f1c30-140">Aggiorna nome credenziali</span><span class="sxs-lookup"><span data-stu-id="f1c30-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="f1c30-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c30-141">-ResourceGroupName</span></span>
<span data-ttu-id="f1c30-142">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f1c30-142">Resource Group Name</span></span>

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

### <span data-ttu-id="f1c30-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1c30-143">-ServerName</span></span>
<span data-ttu-id="f1c30-144">Nome di destinazione del server</span><span class="sxs-lookup"><span data-stu-id="f1c30-144">Server Target Name</span></span>

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

### <span data-ttu-id="f1c30-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="f1c30-145">-ShardMapName</span></span>
<span data-ttu-id="f1c30-146">Nome destinazione mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="f1c30-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="f1c30-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c30-147">-TargetGroupName</span></span>
<span data-ttu-id="f1c30-148">Nome del gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1c30-148">The target group name.</span></span>

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

### <span data-ttu-id="f1c30-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1c30-149">-Confirm</span></span>
<span data-ttu-id="f1c30-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c30-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c30-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c30-151">-WhatIf</span></span>
<span data-ttu-id="f1c30-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1c30-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c30-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1c30-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c30-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c30-154">CommonParameters</span></span>
<span data-ttu-id="f1c30-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c30-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c30-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1c30-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c30-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1c30-157">INPUTS</span></span>

### <span data-ttu-id="f1c30-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f1c30-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f1c30-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1c30-159">OUTPUTS</span></span>

### <span data-ttu-id="f1c30-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="f1c30-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="f1c30-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1c30-161">NOTES</span></span>

## <span data-ttu-id="f1c30-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1c30-162">RELATED LINKS</span></span>
