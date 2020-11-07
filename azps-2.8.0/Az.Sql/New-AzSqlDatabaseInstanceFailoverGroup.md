---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857397"
---
# <span data-ttu-id="38582-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="38582-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="38582-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38582-102">SYNOPSIS</span></span>
<span data-ttu-id="38582-103">Questo comando crea un nuovo gruppo di failover di istanza di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="38582-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="38582-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38582-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38582-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38582-105">DESCRIPTION</span></span>
<span data-ttu-id="38582-106">Crea un nuovo gruppo di failover di istanza di database SQL di Azure tra le aree geografiche specificate con la coppia di istanze gestite nota.</span><span class="sxs-lookup"><span data-stu-id="38582-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="38582-107">Due endpoint TDS di database SQL di Azure vengono creati in nome. SqlDatabaseDnsSuffix (ad esempio, Name.database.windows.net) e Name. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="38582-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="38582-108">Questi endpoint possono essere usati per connettersi rispettivamente alle aree primarie e secondarie del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="38582-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="38582-109">Se l'area principale è interessata da un'interruzione, il failover automatico degli endpoint e dei database viene attivato come dettato dai criteri di failover e dal periodo di tolleranza del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="38582-110">Durante l'anteprima della caratteristica gruppi di failover delle istanze, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="38582-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="38582-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38582-111">EXAMPLES</span></span>

### <span data-ttu-id="38582-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38582-112">Example 1</span></span>
```
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

<span data-ttu-id="38582-113">Questo comando crea un nuovo gruppo di failover delle istanze con il criterio di failover "automatico" per la coppia di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="38582-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="38582-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38582-114">Example 2</span></span>
```
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

<span data-ttu-id="38582-115">Questo comando crea un nuovo gruppo di failover delle istanze con i criteri di failover "manuale" per la coppia di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="38582-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="38582-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38582-116">PARAMETERS</span></span>

### <span data-ttu-id="38582-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="38582-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="38582-118">Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="38582-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="38582-119">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="38582-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38582-120">-DefaultProfile</span></span>
<span data-ttu-id="38582-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38582-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="38582-122">-FailoverPolicy</span></span>
<span data-ttu-id="38582-123">Criteri di failover del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="38582-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="38582-125">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="38582-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="38582-126">-Location</span></span>
<span data-ttu-id="38582-127">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="38582-128">-Name</span></span>
<span data-ttu-id="38582-129">Il nome del gruppo di failover di database SQL di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="38582-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="38582-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="38582-131">Nome dell'istanza gestita nell'area partner da aggiungere al gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="38582-132">-PartnerRegion</span></span>
<span data-ttu-id="38582-133">Nome dell'area partner del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38582-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="38582-135">Nome del gruppo di risorse secondarie del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38582-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="38582-137">ID della sottoscrizione dell'istanza gestita secondaria del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="38582-138">Questo parametro è necessario solo per la configurazione cross-Subscription</span><span class="sxs-lookup"><span data-stu-id="38582-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="38582-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="38582-140">Nome dell'istanza gestita nell'area locale da aggiungere al gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="38582-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38582-141">-ResourceGroupName</span></span>
<span data-ttu-id="38582-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38582-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38582-143">-Confirm</span></span>
<span data-ttu-id="38582-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38582-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38582-145">-WhatIf</span></span>
<span data-ttu-id="38582-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38582-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38582-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38582-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38582-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38582-148">CommonParameters</span></span>
<span data-ttu-id="38582-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38582-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38582-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38582-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38582-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38582-151">INPUTS</span></span>

### <span data-ttu-id="38582-152">System. String</span><span class="sxs-lookup"><span data-stu-id="38582-152">System.String</span></span>

## <span data-ttu-id="38582-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38582-153">OUTPUTS</span></span>

### <span data-ttu-id="38582-154">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="38582-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="38582-155">Note</span><span class="sxs-lookup"><span data-stu-id="38582-155">NOTES</span></span>

## <span data-ttu-id="38582-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38582-156">RELATED LINKS</span></span>
