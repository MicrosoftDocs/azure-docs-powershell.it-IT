---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190974"
---
# <span data-ttu-id="aff40-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aff40-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="aff40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff40-102">SYNOPSIS</span></span>
<span data-ttu-id="aff40-103">Esegue il failover di un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="aff40-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="aff40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aff40-104">SYNTAX</span></span>

### <span data-ttu-id="aff40-105">SwitchInstanceFailoverGroupDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aff40-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aff40-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aff40-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aff40-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aff40-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aff40-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aff40-108">DESCRIPTION</span></span>
<span data-ttu-id="aff40-109">Questo comando scambia i ruoli delle istanze gestite in un gruppo di failover di istanza effettuando il failover sull'area secondaria specificata, rendendola la nuova area principale.</span><span class="sxs-lookup"><span data-stu-id="aff40-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="aff40-110">Tutte le nuove sessioni TDS che si connettono all'endpoint principale vengono automaticamente ri instradati alla nuova area primaria.</span><span class="sxs-lookup"><span data-stu-id="aff40-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="aff40-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aff40-111">EXAMPLES</span></span>

### <span data-ttu-id="aff40-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aff40-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="aff40-113">Eseguire un'operazione di failover che consente la perdita di dati tramite piping nel gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="aff40-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="aff40-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aff40-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="aff40-115">Eseguire un'operazione di failover che ha esito positivo senza perdere i dati oppure eseguire il rollback.</span><span class="sxs-lookup"><span data-stu-id="aff40-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="aff40-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aff40-116">PARAMETERS</span></span>

### <span data-ttu-id="aff40-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="aff40-117">-AllowDataLoss</span></span>
<span data-ttu-id="aff40-118">Completare il failover anche in questo caso può causare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="aff40-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="aff40-119">In questo modo il failover può proseguire anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="aff40-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="aff40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff40-120">-DefaultProfile</span></span>
<span data-ttu-id="aff40-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aff40-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff40-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aff40-122">-InputObject</span></span>
<span data-ttu-id="aff40-123">L'oggetto gruppo di failover dell'istanza da cambiare</span><span class="sxs-lookup"><span data-stu-id="aff40-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff40-124">-Location</span><span class="sxs-lookup"><span data-stu-id="aff40-124">-Location</span></span>
<span data-ttu-id="aff40-125">Nome dell'area locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="aff40-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff40-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aff40-126">-Name</span></span>
<span data-ttu-id="aff40-127">Nome del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="aff40-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff40-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff40-128">-ResourceGroupName</span></span>
<span data-ttu-id="aff40-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aff40-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff40-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aff40-130">-ResourceId</span></span>
<span data-ttu-id="aff40-131">ID risorsa del gruppo di failover dell'istanza da cambiare.</span><span class="sxs-lookup"><span data-stu-id="aff40-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff40-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aff40-132">-Confirm</span></span>
<span data-ttu-id="aff40-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aff40-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff40-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff40-134">-WhatIf</span></span>
<span data-ttu-id="aff40-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aff40-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff40-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aff40-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff40-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff40-137">CommonParameters</span></span>
<span data-ttu-id="aff40-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff40-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff40-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aff40-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff40-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="aff40-140">INPUTS</span></span>

### <span data-ttu-id="aff40-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="aff40-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="aff40-142">System.String</span><span class="sxs-lookup"><span data-stu-id="aff40-142">System.String</span></span>

## <span data-ttu-id="aff40-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aff40-143">OUTPUTS</span></span>

### <span data-ttu-id="aff40-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="aff40-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="aff40-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="aff40-145">NOTES</span></span>

## <span data-ttu-id="aff40-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aff40-146">RELATED LINKS</span></span>
