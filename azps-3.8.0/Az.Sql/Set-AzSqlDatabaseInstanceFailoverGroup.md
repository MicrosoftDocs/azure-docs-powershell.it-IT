---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864996"
---
# <span data-ttu-id="56a3f-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="56a3f-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="56a3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="56a3f-103">Modifica la configurazione di un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="56a3f-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="56a3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56a3f-104">SYNTAX</span></span>

### <span data-ttu-id="56a3f-105">SetInstanceFailoverGroupDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56a3f-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56a3f-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56a3f-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56a3f-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="56a3f-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56a3f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="56a3f-109">Questo comando modifica la configurazione di un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="56a3f-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="56a3f-110">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="56a3f-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="56a3f-111">Durante l'anteprima della caratteristica gruppi di failover delle istanze, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="56a3f-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="56a3f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56a3f-112">EXAMPLES</span></span>

### <span data-ttu-id="56a3f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56a3f-113">Example 1</span></span>
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

<span data-ttu-id="56a3f-114">Imposta i criteri di failover di un gruppo di failover delle istanze su' manual ' tramite piping nel gruppo failover.</span><span class="sxs-lookup"><span data-stu-id="56a3f-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="56a3f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56a3f-115">PARAMETERS</span></span>

### <span data-ttu-id="56a3f-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="56a3f-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="56a3f-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="56a3f-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="56a3f-118">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="56a3f-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="56a3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a3f-119">-DefaultProfile</span></span>
<span data-ttu-id="56a3f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56a3f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a3f-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="56a3f-121">-FailoverPolicy</span></span>
<span data-ttu-id="56a3f-122">Criteri di failover del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="56a3f-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="56a3f-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="56a3f-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="56a3f-124">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="56a3f-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="56a3f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56a3f-125">-InputObject</span></span>
<span data-ttu-id="56a3f-126">Oggetto gruppo di failover dell'istanza da impostare</span><span class="sxs-lookup"><span data-stu-id="56a3f-126">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="56a3f-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="56a3f-127">-Location</span></span>
<span data-ttu-id="56a3f-128">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="56a3f-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="56a3f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="56a3f-129">-Name</span></span>
<span data-ttu-id="56a3f-130">Nome del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="56a3f-130">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="56a3f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a3f-131">-ResourceGroupName</span></span>
<span data-ttu-id="56a3f-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56a3f-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="56a3f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56a3f-133">-ResourceId</span></span>
<span data-ttu-id="56a3f-134">ID risorsa del gruppo di failover delle istanze da impostare.</span><span class="sxs-lookup"><span data-stu-id="56a3f-134">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="56a3f-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56a3f-135">-Confirm</span></span>
<span data-ttu-id="56a3f-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56a3f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56a3f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56a3f-137">-WhatIf</span></span>
<span data-ttu-id="56a3f-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56a3f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56a3f-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56a3f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56a3f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a3f-140">CommonParameters</span></span>
<span data-ttu-id="56a3f-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a3f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a3f-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56a3f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a3f-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56a3f-143">INPUTS</span></span>

### <span data-ttu-id="56a3f-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="56a3f-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="56a3f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="56a3f-145">System.String</span></span>

## <span data-ttu-id="56a3f-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56a3f-146">OUTPUTS</span></span>

### <span data-ttu-id="56a3f-147">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="56a3f-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="56a3f-148">Note</span><span class="sxs-lookup"><span data-stu-id="56a3f-148">NOTES</span></span>

## <span data-ttu-id="56a3f-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56a3f-149">RELATED LINKS</span></span>
