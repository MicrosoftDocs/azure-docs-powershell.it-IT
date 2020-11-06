---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521294"
---
# <span data-ttu-id="de30f-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="de30f-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="de30f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de30f-102">SYNOPSIS</span></span>
<span data-ttu-id="de30f-103">Ripristina un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="de30f-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de30f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de30f-104">SYNTAX</span></span>

### <span data-ttu-id="de30f-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de30f-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de30f-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="de30f-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de30f-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="de30f-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de30f-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="de30f-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de30f-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="de30f-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de30f-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="de30f-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de30f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de30f-111">DESCRIPTION</span></span>
<span data-ttu-id="de30f-112">Il cmdlet **Restore-AzureRmSqlInstanceDatabase** ripristina un database di istanza da un momento in un database dinamico.</span><span class="sxs-lookup"><span data-stu-id="de30f-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="de30f-113">Il database ripristinato viene creato come nuovo database di istanza.</span><span class="sxs-lookup"><span data-stu-id="de30f-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="de30f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de30f-114">EXAMPLES</span></span>

### <span data-ttu-id="de30f-115">Esempio 1: ripristinare un database di istanza da un momento</span><span class="sxs-lookup"><span data-stu-id="de30f-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="de30f-116">Il comando Ripristina il database dell'istanza Database01 dal backup temporizzatore specificato al database dell'istanza denominato Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="de30f-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="de30f-117">Esempio 2: ripristinare un database di istanza da un momento a un'altra istanza in un gruppo di risorse diverso</span><span class="sxs-lookup"><span data-stu-id="de30f-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="de30f-118">Il comando Ripristina il database dell'istanza Database01 nell'istanza managedInstance1 nel gruppo di risorse ResourceGroup01 dal backup temporizzatore specificato al database dell'istanza denominato Database01_restored nell'istanza managedInstance2 nel gruppo di risorse ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="de30f-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="de30f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de30f-119">PARAMETERS</span></span>

### <span data-ttu-id="de30f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de30f-120">-AsJob</span></span>
<span data-ttu-id="de30f-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="de30f-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de30f-122">-DefaultProfile</span></span>
<span data-ttu-id="de30f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de30f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de30f-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="de30f-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="de30f-125">Eseguire il ripristino da un backup puntuale.</span><span class="sxs-lookup"><span data-stu-id="de30f-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de30f-126">-InputObject</span></span>
<span data-ttu-id="de30f-127">Oggetto database dell'istanza da ripristinare</span><span class="sxs-lookup"><span data-stu-id="de30f-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="de30f-128">-InstanceName</span></span>
<span data-ttu-id="de30f-129">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="de30f-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="de30f-130">-Name</span></span>
<span data-ttu-id="de30f-131">Nome del database dell'istanza da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="de30f-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="de30f-132">-PointInTime</span></span>
<span data-ttu-id="de30f-133">Il momento in cui ripristinare il database.</span><span class="sxs-lookup"><span data-stu-id="de30f-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de30f-134">-ResourceGroupName</span></span>
<span data-ttu-id="de30f-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de30f-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de30f-136">-ResourceId</span></span>
<span data-ttu-id="de30f-137">ID risorsa dell'oggetto di database di istanza da ripristinare</span><span class="sxs-lookup"><span data-stu-id="de30f-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="de30f-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="de30f-139">Nome del database dell'istanza di destinazione a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="de30f-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="de30f-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="de30f-140">-TargetInstanceName</span></span>
<span data-ttu-id="de30f-141">Nome dell'istanza di destinazione in cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="de30f-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="de30f-142">Se non specificato, l'istanza di destinazione è uguale all'istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="de30f-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de30f-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="de30f-144">Il nome del gruppo di risorse di destinazione a cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="de30f-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="de30f-145">Se non viene specificato, il gruppo di risorse di destinazione è uguale al gruppo di risorse di origine.</span><span class="sxs-lookup"><span data-stu-id="de30f-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de30f-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de30f-146">-Confirm</span></span>
<span data-ttu-id="de30f-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de30f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de30f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de30f-148">-WhatIf</span></span>
<span data-ttu-id="de30f-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de30f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de30f-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de30f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de30f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de30f-151">CommonParameters</span></span>
<span data-ttu-id="de30f-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de30f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de30f-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de30f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de30f-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de30f-154">INPUTS</span></span>

### <span data-ttu-id="de30f-155">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="de30f-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="de30f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="de30f-156">System.String</span></span>

## <span data-ttu-id="de30f-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de30f-157">OUTPUTS</span></span>

### <span data-ttu-id="de30f-158">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="de30f-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="de30f-159">Note</span><span class="sxs-lookup"><span data-stu-id="de30f-159">NOTES</span></span>

## <span data-ttu-id="de30f-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de30f-160">RELATED LINKS</span></span>
