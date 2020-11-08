---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032118"
---
# <span data-ttu-id="1f996-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1f996-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="1f996-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f996-102">SYNOPSIS</span></span>
<span data-ttu-id="1f996-103">Questo comando crea un nuovo gruppo di failover di istanza di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f996-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="1f996-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f996-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f996-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f996-105">DESCRIPTION</span></span>
<span data-ttu-id="1f996-106">Crea un nuovo gruppo di failover di istanza di database SQL di Azure tra le aree geografiche specificate con la coppia di istanze gestite nota.</span><span class="sxs-lookup"><span data-stu-id="1f996-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="1f996-107">Due endpoint TDS di database SQL di Azure vengono creati in nome. SqlDatabaseDnsSuffix (ad esempio, Name.database.windows.net) e Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="1f996-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="1f996-108">Questi endpoint possono essere usati per connettersi rispettivamente alle aree primarie e secondarie del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="1f996-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="1f996-109">Se l'area principale è interessata da un'interruzione, il failover automatico degli endpoint e dei database viene attivato come dettato dai criteri di failover e dal periodo di tolleranza del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="1f996-110">Durante l'anteprima della caratteristica gruppi di failover delle istanze, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="1f996-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1f996-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f996-111">EXAMPLES</span></span>

### <span data-ttu-id="1f996-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f996-112">Example 1</span></span>
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

<span data-ttu-id="1f996-113">Questo comando crea un nuovo gruppo di failover delle istanze con il criterio di failover "automatico" per la coppia di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="1f996-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="1f996-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1f996-114">Example 2</span></span>
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

<span data-ttu-id="1f996-115">Questo comando crea un nuovo gruppo di failover delle istanze con i criteri di failover "manuale" per la coppia di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="1f996-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="1f996-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1f996-116">Example 3</span></span>

<span data-ttu-id="1f996-117">Questo comando crea un nuovo gruppo di failover di istanza di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f996-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="1f996-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="1f996-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="1f996-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f996-119">PARAMETERS</span></span>

### <span data-ttu-id="1f996-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1f996-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1f996-121">Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1f996-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="1f996-122">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="1f996-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="1f996-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f996-123">-DefaultProfile</span></span>
<span data-ttu-id="1f996-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f996-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f996-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1f996-125">-FailoverPolicy</span></span>
<span data-ttu-id="1f996-126">Criteri di failover del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1f996-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1f996-128">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="1f996-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="1f996-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1f996-129">-Location</span></span>
<span data-ttu-id="1f996-130">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f996-131">-Name</span></span>
<span data-ttu-id="1f996-132">Il nome del gruppo di failover di database SQL di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="1f996-132">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="1f996-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1f996-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="1f996-134">Nome dell'istanza gestita nell'area partner da aggiungere al gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="1f996-135">-PartnerRegion</span></span>
<span data-ttu-id="1f996-136">Nome dell'area partner del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-136">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f996-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1f996-138">Nome del gruppo di risorse secondarie del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f996-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="1f996-140">ID della sottoscrizione dell'istanza gestita secondaria del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="1f996-141">Questo parametro è necessario solo per la configurazione cross-Subscription</span><span class="sxs-lookup"><span data-stu-id="1f996-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="1f996-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1f996-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="1f996-143">Nome dell'istanza gestita nell'area locale da aggiungere al gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1f996-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1f996-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f996-144">-ResourceGroupName</span></span>
<span data-ttu-id="1f996-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f996-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f996-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f996-146">-Confirm</span></span>
<span data-ttu-id="1f996-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f996-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f996-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f996-148">-WhatIf</span></span>
<span data-ttu-id="1f996-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f996-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f996-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f996-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f996-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f996-151">CommonParameters</span></span>
<span data-ttu-id="1f996-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f996-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f996-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f996-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f996-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f996-154">INPUTS</span></span>

### <span data-ttu-id="1f996-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1f996-155">System.String</span></span>

## <span data-ttu-id="1f996-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f996-156">OUTPUTS</span></span>

### <span data-ttu-id="1f996-157">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1f996-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="1f996-158">Note</span><span class="sxs-lookup"><span data-stu-id="1f996-158">NOTES</span></span>

## <span data-ttu-id="1f996-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f996-159">RELATED LINKS</span></span>
