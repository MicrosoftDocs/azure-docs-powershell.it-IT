---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8ac386eba93f2d9083c086c1ff2b1ab3faca6be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970270"
---
# <span data-ttu-id="1d531-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1d531-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="1d531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d531-102">SYNOPSIS</span></span>
<span data-ttu-id="1d531-103">Questo comando crea un nuovo gruppo di failover dell SQL di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d531-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="1d531-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d531-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d531-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d531-105">DESCRIPTION</span></span>
<span data-ttu-id="1d531-106">Crea un nuovo gruppo di failover dell SQL di database di Azure tra le aree specificate con la coppia notata Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1d531-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="1d531-107">Vengono creati due endpoint TDS del database SQL Azure in Name.SqlDatabaseDnsSuffix, ad esempio Name.database.windows.net, e Name.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="1d531-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="1d531-108">Questi endpoint possono essere usati, rispettivamente, per connettersi alle aree primaria e secondaria del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="1d531-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="1d531-109">Se l'area principale è interessata da un'interruzione, il failover automatico degli endpoint e dei database verrà attivato in base ai criteri di failover e al periodo di tolleranza del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="1d531-110">Durante l'anteprima della funzionalità Gruppi di failover delle istanze, per il parametro '-GracePeriodWithDataLossHours' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="1d531-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1d531-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d531-111">EXAMPLES</span></span>

### <span data-ttu-id="1d531-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d531-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
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

<span data-ttu-id="1d531-113">Questo comando crea un nuovo gruppo di failover delle istanze con il criterio di failover "Automatico" per la coppia Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1d531-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="1d531-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1d531-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="1d531-115">Questo comando crea un nuovo gruppo di failover delle istanze con criterio di failover "Manuale" per la coppia Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1d531-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="1d531-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1d531-116">Example 3</span></span>

<span data-ttu-id="1d531-117">Questo comando crea un nuovo gruppo di failover dell SQL di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d531-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="1d531-118">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="1d531-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="1d531-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d531-119">PARAMETERS</span></span>

### <span data-ttu-id="1d531-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1d531-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1d531-121">Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1d531-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="1d531-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d531-122">-DefaultProfile</span></span>
<span data-ttu-id="1d531-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d531-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d531-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1d531-124">-FailoverPolicy</span></span>
<span data-ttu-id="1d531-125">Criteri di failover del gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="1d531-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1d531-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1d531-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1d531-127">Intervallo prima dell'avvio del failover automatico se si verifica un'interruzione nel server principale e il failover non può essere completato senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="1d531-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d531-128">-Location</span><span class="sxs-lookup"><span data-stu-id="1d531-128">-Location</span></span>
<span data-ttu-id="1d531-129">Nome dell'area locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d531-130">-Name</span><span class="sxs-lookup"><span data-stu-id="1d531-130">-Name</span></span>
<span data-ttu-id="1d531-131">Nome del gruppo di failover del database SQL Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="1d531-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d531-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1d531-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="1d531-133">Nome dell'istanza gestita nell'area del partner da aggiungere al gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1d531-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="1d531-134">-PartnerRegion</span></span>
<span data-ttu-id="1d531-135">Nome dell'area partner del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1d531-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d531-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1d531-137">Nome del gruppo di risorse secondario del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1d531-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d531-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="1d531-139">ID sottoscrizione dell'istanza gestita secondaria del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1d531-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="1d531-140">Questo parametro è necessario solo per la configurazione tra abbonamenti</span><span class="sxs-lookup"><span data-stu-id="1d531-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="1d531-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1d531-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="1d531-142">Nome dell'istanza gestita nell'area locale da aggiungere al gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="1d531-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1d531-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d531-143">-ResourceGroupName</span></span>
<span data-ttu-id="1d531-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d531-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d531-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d531-145">-Confirm</span></span>
<span data-ttu-id="1d531-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d531-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d531-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d531-147">-WhatIf</span></span>
<span data-ttu-id="1d531-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d531-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d531-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d531-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d531-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d531-150">CommonParameters</span></span>
<span data-ttu-id="1d531-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d531-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d531-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d531-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d531-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d531-153">INPUTS</span></span>

### <span data-ttu-id="1d531-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1d531-154">System.String</span></span>

## <span data-ttu-id="1d531-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d531-155">OUTPUTS</span></span>

### <span data-ttu-id="1d531-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1d531-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="1d531-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d531-157">NOTES</span></span>

## <span data-ttu-id="1d531-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d531-158">RELATED LINKS</span></span>
