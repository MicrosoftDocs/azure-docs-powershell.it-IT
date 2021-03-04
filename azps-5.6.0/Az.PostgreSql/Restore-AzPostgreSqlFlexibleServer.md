---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953598"
---
# <span data-ttu-id="97ef7-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="97ef7-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="97ef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="97ef7-103">Ripristinare un server flessibile PostgreSQL da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="97ef7-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="97ef7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97ef7-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97ef7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="97ef7-106">Ripristinare un server da un backup esistente</span><span class="sxs-lookup"><span data-stu-id="97ef7-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="97ef7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="97ef7-108">Esempio 1: Ripristinare un server PostgreSql usando PointInTime Restore</span><span class="sxs-lookup"><span data-stu-id="97ef7-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="97ef7-109">Questi cmdlet ripristinano il server PostgreSql tramite PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="97ef7-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="97ef7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97ef7-110">PARAMETERS</span></span>

### <span data-ttu-id="97ef7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97ef7-111">-AsJob</span></span>
<span data-ttu-id="97ef7-112">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="97ef7-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ef7-113">-DefaultProfile</span></span>
<span data-ttu-id="97ef7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97ef7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-115">-Location</span><span class="sxs-lookup"><span data-stu-id="97ef7-115">-Location</span></span>
<span data-ttu-id="97ef7-116">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="97ef7-116">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="97ef7-117">-Name</span></span>
<span data-ttu-id="97ef7-118">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="97ef7-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="97ef7-119">-NoWait</span></span>
<span data-ttu-id="97ef7-120">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="97ef7-120">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ef7-121">-ResourceGroupName</span></span>
<span data-ttu-id="97ef7-122">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="97ef7-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="97ef7-123">-RestorePointInTime</span></span>
<span data-ttu-id="97ef7-124">Il momento in cui eseguire il ripristino (formato ISO8601), ad esempio 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="97ef7-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="97ef7-125">-SourceServerName</span></span>
<span data-ttu-id="97ef7-126">Nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="97ef7-126">The name of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97ef7-127">-SubscriptionId</span></span>
<span data-ttu-id="97ef7-128">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97ef7-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-129">-Zone</span><span class="sxs-lookup"><span data-stu-id="97ef7-129">-Zone</span></span>
<span data-ttu-id="97ef7-130">Area di disponibilità in cui effettuare il provisioning della risorsa.</span><span class="sxs-lookup"><span data-stu-id="97ef7-130">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97ef7-131">-Confirm</span></span>
<span data-ttu-id="97ef7-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ef7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ef7-133">-WhatIf</span></span>
<span data-ttu-id="97ef7-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97ef7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97ef7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97ef7-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ef7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ef7-136">CommonParameters</span></span>
<span data-ttu-id="97ef7-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ef7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ef7-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97ef7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ef7-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="97ef7-139">INPUTS</span></span>

## <span data-ttu-id="97ef7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97ef7-140">OUTPUTS</span></span>

### <span data-ttu-id="97ef7-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="97ef7-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="97ef7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="97ef7-142">NOTES</span></span>

<span data-ttu-id="97ef7-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="97ef7-143">ALIASES</span></span>

## <span data-ttu-id="97ef7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97ef7-144">RELATED LINKS</span></span>

