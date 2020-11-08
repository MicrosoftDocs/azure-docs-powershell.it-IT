---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189247"
---
# <span data-ttu-id="9fa14-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9fa14-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="9fa14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fa14-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa14-103">Esegue un failover di un gruppo di failover di istanze.</span><span class="sxs-lookup"><span data-stu-id="9fa14-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="9fa14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fa14-104">SYNTAX</span></span>

### <span data-ttu-id="9fa14-105">SwitchInstanceFailoverGroupDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fa14-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa14-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9fa14-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa14-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9fa14-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa14-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fa14-108">DESCRIPTION</span></span>
<span data-ttu-id="9fa14-109">Questo comando scambia i ruoli delle istanze gestite in un gruppo di failover dell'istanza omettendo l'area secondaria specificata, rendendola la nuova area principale.</span><span class="sxs-lookup"><span data-stu-id="9fa14-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="9fa14-110">Tutte le nuove sessioni TDS che si connettono all'endpoint principale vengono automaticamente reindirizzate alla nuova area principale.</span><span class="sxs-lookup"><span data-stu-id="9fa14-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="9fa14-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fa14-111">EXAMPLES</span></span>

### <span data-ttu-id="9fa14-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fa14-112">Example 1</span></span>
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

<span data-ttu-id="9fa14-113">Eseguire un'operazione di failover per consentire la perdita dei dati tramite piping nel gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9fa14-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="9fa14-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9fa14-114">Example 2</span></span>
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

<span data-ttu-id="9fa14-115">Eseguire un'operazione di failover ottimale dello sforzo che avrà esito positivo senza perdere dati o non riesce e ripristinare il rollback.</span><span class="sxs-lookup"><span data-stu-id="9fa14-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="9fa14-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fa14-116">PARAMETERS</span></span>

### <span data-ttu-id="9fa14-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="9fa14-117">-AllowDataLoss</span></span>
<span data-ttu-id="9fa14-118">Completare il failover anche se tale operazione può causare una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="9fa14-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="9fa14-119">In questo modo il failover verrà continuato anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="9fa14-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="9fa14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa14-120">-DefaultProfile</span></span>
<span data-ttu-id="9fa14-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa14-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fa14-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa14-122">-InputObject</span></span>
<span data-ttu-id="9fa14-123">Oggetto gruppo di failover dell'istanza per passare</span><span class="sxs-lookup"><span data-stu-id="9fa14-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="9fa14-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9fa14-124">-Location</span></span>
<span data-ttu-id="9fa14-125">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9fa14-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9fa14-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fa14-126">-Name</span></span>
<span data-ttu-id="9fa14-127">Nome del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9fa14-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9fa14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa14-128">-ResourceGroupName</span></span>
<span data-ttu-id="9fa14-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fa14-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9fa14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa14-130">-ResourceId</span></span>
<span data-ttu-id="9fa14-131">ID risorsa del gruppo di failover delle istanze da cambiare.</span><span class="sxs-lookup"><span data-stu-id="9fa14-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="9fa14-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fa14-132">-Confirm</span></span>
<span data-ttu-id="9fa14-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa14-134">-WhatIf</span></span>
<span data-ttu-id="9fa14-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fa14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa14-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fa14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa14-137">CommonParameters</span></span>
<span data-ttu-id="9fa14-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa14-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fa14-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa14-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fa14-140">INPUTS</span></span>

### <span data-ttu-id="9fa14-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9fa14-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="9fa14-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9fa14-142">System.String</span></span>

## <span data-ttu-id="9fa14-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fa14-143">OUTPUTS</span></span>

### <span data-ttu-id="9fa14-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9fa14-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="9fa14-145">Note</span><span class="sxs-lookup"><span data-stu-id="9fa14-145">NOTES</span></span>

## <span data-ttu-id="9fa14-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fa14-146">RELATED LINKS</span></span>
