---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6fe6e142184059d554922579e669db5815a18c94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955181"
---
# <span data-ttu-id="cdd11-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="cdd11-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="cdd11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd11-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd11-103">Rimuove la destinazione dal gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cdd11-103">Removes the target from the target group</span></span>

## <span data-ttu-id="cdd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdd11-104">SYNTAX</span></span>

### <span data-ttu-id="cdd11-105">SqlDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdd11-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="cdd11-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="cdd11-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdd11-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cdd11-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cdd11-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cdd11-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd11-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd11-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd11-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdd11-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd11-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd11-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdd11-114">DESCRIPTION</span></span>
<span data-ttu-id="cdd11-115">Il cmdlet Remove-AzSqlElasticJobTarget rimuove una risorsa di destinazione a un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cdd11-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="cdd11-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdd11-116">EXAMPLES</span></span>

### <span data-ttu-id="cdd11-117">Esempio 1: Rimuovere una destinazione del server</span><span class="sxs-lookup"><span data-stu-id="cdd11-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="cdd11-118">Esempio 2: Rimuovere una destinazione di database</span><span class="sxs-lookup"><span data-stu-id="cdd11-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="cdd11-119">Esempio 3: Rimuovere una destinazione del pool flessibile</span><span class="sxs-lookup"><span data-stu-id="cdd11-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="cdd11-120">Esempio 4: Rimuovere una destinazione della mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="cdd11-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="cdd11-121">Rimuove una destinazione (server, pool flessibile, database e mappa partizionata) da un gruppo di destinazione</span><span class="sxs-lookup"><span data-stu-id="cdd11-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="cdd11-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdd11-122">PARAMETERS</span></span>

### <span data-ttu-id="cdd11-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cdd11-123">-AgentName</span></span>
<span data-ttu-id="cdd11-124">SQL agente di database.</span><span class="sxs-lookup"><span data-stu-id="cdd11-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="cdd11-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="cdd11-125">-AgentServerName</span></span>
<span data-ttu-id="cdd11-126">SQL server Agente database.</span><span class="sxs-lookup"><span data-stu-id="cdd11-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="cdd11-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cdd11-127">-DatabaseName</span></span>
<span data-ttu-id="cdd11-128">Nome destinazione database</span><span class="sxs-lookup"><span data-stu-id="cdd11-128">Database Target Name</span></span>

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

### <span data-ttu-id="cdd11-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd11-129">-DefaultProfile</span></span>
<span data-ttu-id="cdd11-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd11-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd11-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cdd11-131">-ElasticPoolName</span></span>
<span data-ttu-id="cdd11-132">Nome di destinazione del pool flessibile</span><span class="sxs-lookup"><span data-stu-id="cdd11-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="cdd11-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cdd11-133">-ParentObject</span></span>
<span data-ttu-id="cdd11-134">Oggetto gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cdd11-134">The target group object.</span></span>

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

### <span data-ttu-id="cdd11-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd11-135">-ParentResourceId</span></span>
<span data-ttu-id="cdd11-136">ID della risorsa del gruppo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cdd11-136">The target group resource id.</span></span>

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

### <span data-ttu-id="cdd11-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="cdd11-137">-RefreshCredentialName</span></span>
<span data-ttu-id="cdd11-138">Aggiorna nome credenziali</span><span class="sxs-lookup"><span data-stu-id="cdd11-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="cdd11-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd11-139">-ResourceGroupName</span></span>
<span data-ttu-id="cdd11-140">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cdd11-140">Resource Group Name</span></span>

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

### <span data-ttu-id="cdd11-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cdd11-141">-ServerName</span></span>
<span data-ttu-id="cdd11-142">Nome di destinazione del server</span><span class="sxs-lookup"><span data-stu-id="cdd11-142">Server Target Name</span></span>

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

### <span data-ttu-id="cdd11-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="cdd11-143">-ShardMapName</span></span>
<span data-ttu-id="cdd11-144">Nome destinazione mappa partizionata</span><span class="sxs-lookup"><span data-stu-id="cdd11-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="cdd11-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd11-145">-TargetGroupName</span></span>
<span data-ttu-id="cdd11-146">SQL agente di database.</span><span class="sxs-lookup"><span data-stu-id="cdd11-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="cdd11-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdd11-147">-Confirm</span></span>
<span data-ttu-id="cdd11-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd11-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd11-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd11-149">-WhatIf</span></span>
<span data-ttu-id="cdd11-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd11-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd11-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd11-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd11-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd11-152">CommonParameters</span></span>
<span data-ttu-id="cdd11-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd11-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd11-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cdd11-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd11-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdd11-155">INPUTS</span></span>

### <span data-ttu-id="cdd11-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="cdd11-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="cdd11-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdd11-157">OUTPUTS</span></span>

### <span data-ttu-id="cdd11-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="cdd11-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="cdd11-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdd11-159">NOTES</span></span>

## <span data-ttu-id="cdd11-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdd11-160">RELATED LINKS</span></span>
