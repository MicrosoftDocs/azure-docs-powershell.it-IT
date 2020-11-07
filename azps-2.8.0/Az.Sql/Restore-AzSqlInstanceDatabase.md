---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857286"
---
# <span data-ttu-id="8068d-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8068d-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="8068d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8068d-102">SYNOPSIS</span></span>
<span data-ttu-id="8068d-103">Ripristina un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8068d-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="8068d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8068d-104">SYNTAX</span></span>

### <span data-ttu-id="8068d-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8068d-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8068d-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8068d-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8068d-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="8068d-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8068d-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8068d-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8068d-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8068d-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8068d-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8068d-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="8068d-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8068d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8068d-114">DESCRIPTION</span></span>
<span data-ttu-id="8068d-115">Il cmdlet **Restore-AzSqlInstanceDatabase** ripristina un database di istanza da un backup Geo-ridondante o un momento in un database dinamico.</span><span class="sxs-lookup"><span data-stu-id="8068d-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="8068d-116">Il database ripristinato viene creato come nuovo database di istanza.</span><span class="sxs-lookup"><span data-stu-id="8068d-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="8068d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8068d-117">EXAMPLES</span></span>

### <span data-ttu-id="8068d-118">Esempio 1: ripristinare un database di istanza da un momento</span><span class="sxs-lookup"><span data-stu-id="8068d-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="8068d-119">Il comando Ripristina il database dell'istanza Database01 dal backup temporizzatore specificato al database dell'istanza denominato Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="8068d-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="8068d-120">Esempio 2: ripristinare un database di istanza da un momento a un'altra istanza in un gruppo di risorse diverso</span><span class="sxs-lookup"><span data-stu-id="8068d-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="8068d-121">Il comando Ripristina il database dell'istanza Database01 nell'istanza managedInstance1 nel gruppo di risorse ResourceGroup01 dal backup temporizzatore specificato al database dell'istanza denominato Database01_restored nell'istanza managedInstance2 nel gruppo di risorse ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="8068d-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="8068d-122">Esempio 3: Geo-Restore un database di istanza</span><span class="sxs-lookup"><span data-stu-id="8068d-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="8068d-123">Il primo comando ottiene il backup Geo-ridondante per il database denominato Database01 e lo archivia nella variabile $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="8068d-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="8068d-124">Il secondo comando Ripristina il backup in $GeoBackup al database dell'istanza denominato Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="8068d-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="8068d-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8068d-125">PARAMETERS</span></span>

### <span data-ttu-id="8068d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8068d-126">-AsJob</span></span>
<span data-ttu-id="8068d-127">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8068d-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8068d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8068d-128">-DefaultProfile</span></span>
<span data-ttu-id="8068d-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8068d-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="8068d-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8068d-130">-FromGeoBackup</span></span>
<span data-ttu-id="8068d-131">Ripristinare da un backup Geo.</span><span class="sxs-lookup"><span data-stu-id="8068d-131">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="8068d-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="8068d-133">Eseguire il ripristino da un backup puntuale.</span><span class="sxs-lookup"><span data-stu-id="8068d-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="8068d-134">-GeoBackupObject</span></span>
<span data-ttu-id="8068d-135">L'oggetto di database dell'istanza ripristinabile da ripristinare</span><span class="sxs-lookup"><span data-stu-id="8068d-135">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8068d-136">-InputObject</span></span>
<span data-ttu-id="8068d-137">Oggetto database dell'istanza da ripristinare</span><span class="sxs-lookup"><span data-stu-id="8068d-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8068d-138">-InstanceName</span></span>
<span data-ttu-id="8068d-139">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8068d-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="8068d-140">-Name</span></span>
<span data-ttu-id="8068d-141">Nome del database dell'istanza da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="8068d-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="8068d-142">-PointInTime</span></span>
<span data-ttu-id="8068d-143">Il momento in cui ripristinare il database.</span><span class="sxs-lookup"><span data-stu-id="8068d-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8068d-144">-ResourceGroupName</span></span>
<span data-ttu-id="8068d-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8068d-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8068d-146">-ResourceId</span></span>
<span data-ttu-id="8068d-147">ID risorsa dell'oggetto di database di istanza da ripristinare</span><span class="sxs-lookup"><span data-stu-id="8068d-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8068d-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="8068d-149">Nome del database dell'istanza di destinazione a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8068d-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="8068d-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="8068d-150">-TargetInstanceName</span></span>
<span data-ttu-id="8068d-151">Nome dell'istanza di destinazione in cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8068d-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="8068d-152">Se non specificato, l'istanza di destinazione è uguale all'istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="8068d-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8068d-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="8068d-154">Il nome del gruppo di risorse di destinazione a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8068d-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="8068d-155">Se non viene specificato, il gruppo di risorse di destinazione è uguale al gruppo di risorse di origine.</span><span class="sxs-lookup"><span data-stu-id="8068d-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8068d-156">-Confirm</span></span>
<span data-ttu-id="8068d-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8068d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8068d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8068d-158">-WhatIf</span></span>
<span data-ttu-id="8068d-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8068d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8068d-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8068d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8068d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8068d-161">CommonParameters</span></span>
<span data-ttu-id="8068d-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8068d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8068d-163">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8068d-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8068d-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8068d-164">INPUTS</span></span>

### <span data-ttu-id="8068d-165">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8068d-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="8068d-166">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8068d-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="8068d-167">System. String</span><span class="sxs-lookup"><span data-stu-id="8068d-167">System.String</span></span>

## <span data-ttu-id="8068d-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8068d-168">OUTPUTS</span></span>

### <span data-ttu-id="8068d-169">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8068d-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="8068d-170">Note</span><span class="sxs-lookup"><span data-stu-id="8068d-170">NOTES</span></span>

## <span data-ttu-id="8068d-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8068d-171">RELATED LINKS</span></span>
