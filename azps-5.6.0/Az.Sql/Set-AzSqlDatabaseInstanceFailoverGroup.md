---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967326"
---
# <span data-ttu-id="02aef-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02aef-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="02aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02aef-102">SYNOPSIS</span></span>
<span data-ttu-id="02aef-103">Modifica la configurazione di un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="02aef-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="02aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02aef-104">SYNTAX</span></span>

### <span data-ttu-id="02aef-105">SetInstanceFailoverGroupDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02aef-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02aef-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="02aef-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02aef-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="02aef-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02aef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02aef-108">DESCRIPTION</span></span>
<span data-ttu-id="02aef-109">Questo comando modifica la configurazione di un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="02aef-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="02aef-110">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="02aef-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="02aef-111">Durante l'anteprima della funzionalità Gruppi di failover delle istanze, per il parametro '-GracePeriodWithDataLossHours' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="02aef-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="02aef-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02aef-112">EXAMPLES</span></span>

### <span data-ttu-id="02aef-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02aef-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="02aef-114">Imposta il criterio di failover di un gruppo di failover dell'istanza su "Manuale" tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="02aef-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="02aef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02aef-115">PARAMETERS</span></span>

### <span data-ttu-id="02aef-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="02aef-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="02aef-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="02aef-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="02aef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02aef-118">-DefaultProfile</span></span>
<span data-ttu-id="02aef-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02aef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02aef-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="02aef-120">-FailoverPolicy</span></span>
<span data-ttu-id="02aef-121">Criteri di failover del gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="02aef-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="02aef-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="02aef-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="02aef-123">Intervallo prima dell'avvio del failover automatico se si verifica un'interruzione nel server principale e il failover non può essere completato senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="02aef-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="02aef-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02aef-124">-InputObject</span></span>
<span data-ttu-id="02aef-125">Oggetto Gruppo di failover dell'istanza da impostare</span><span class="sxs-lookup"><span data-stu-id="02aef-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02aef-126">-Location</span><span class="sxs-lookup"><span data-stu-id="02aef-126">-Location</span></span>
<span data-ttu-id="02aef-127">Nome dell'area locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="02aef-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02aef-128">-Name</span><span class="sxs-lookup"><span data-stu-id="02aef-128">-Name</span></span>
<span data-ttu-id="02aef-129">Nome del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="02aef-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02aef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02aef-130">-ResourceGroupName</span></span>
<span data-ttu-id="02aef-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02aef-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02aef-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02aef-132">-ResourceId</span></span>
<span data-ttu-id="02aef-133">ID risorsa del gruppo di failover dell'istanza da impostare.</span><span class="sxs-lookup"><span data-stu-id="02aef-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02aef-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02aef-134">-Confirm</span></span>
<span data-ttu-id="02aef-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02aef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02aef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02aef-136">-WhatIf</span></span>
<span data-ttu-id="02aef-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02aef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02aef-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02aef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02aef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02aef-139">CommonParameters</span></span>
<span data-ttu-id="02aef-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02aef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02aef-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02aef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02aef-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="02aef-142">INPUTS</span></span>

### <span data-ttu-id="02aef-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="02aef-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="02aef-144">System.String</span><span class="sxs-lookup"><span data-stu-id="02aef-144">System.String</span></span>

## <span data-ttu-id="02aef-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02aef-145">OUTPUTS</span></span>

### <span data-ttu-id="02aef-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="02aef-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="02aef-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="02aef-147">NOTES</span></span>

## <span data-ttu-id="02aef-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02aef-148">RELATED LINKS</span></span>
