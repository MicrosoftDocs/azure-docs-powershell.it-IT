---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475650"
---
# <span data-ttu-id="eee9f-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eee9f-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="eee9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eee9f-102">SYNOPSIS</span></span>
<span data-ttu-id="eee9f-103">Ottiene i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="eee9f-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="eee9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eee9f-104">SYNTAX</span></span>

### <span data-ttu-id="eee9f-105">Posizione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eee9f-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="eee9f-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eee9f-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-108">NomeBackup</span><span class="sxs-lookup"><span data-stu-id="eee9f-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="eee9f-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="eee9f-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee9f-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="eee9f-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee9f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee9f-112">DESCRIPTION</span></span>
<span data-ttu-id="eee9f-113">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="eee9f-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="eee9f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eee9f-114">EXAMPLES</span></span>

### <span data-ttu-id="eee9f-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eee9f-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="eee9f-116">Ottiene tutti i backup di conservazione a lungo termine per un determinato database.</span><span class="sxs-lookup"><span data-stu-id="eee9f-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="eee9f-117">Il gruppo di risorse è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="eee9f-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="eee9f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eee9f-118">PARAMETERS</span></span>

### <span data-ttu-id="eee9f-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="eee9f-119">-BackupName</span></span>
<span data-ttu-id="eee9f-120">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eee9f-121">-DatabaseName</span></span>
<span data-ttu-id="eee9f-122">Nome del database gestito in cui si trovano i backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="eee9f-123">-DatabaseState</span></span>
<span data-ttu-id="eee9f-124">Lo stato del database di cui si vogliono trovare i backup, attivo, eliminato o tutti.</span><span class="sxs-lookup"><span data-stu-id="eee9f-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="eee9f-125">Impostazione predefinita per tutti</span><span class="sxs-lookup"><span data-stu-id="eee9f-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee9f-126">-DefaultProfile</span></span>
<span data-ttu-id="eee9f-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eee9f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eee9f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eee9f-128">-InputObject</span></span>
<span data-ttu-id="eee9f-129">Oggetto database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="eee9f-130">-InstanceName</span></span>
<span data-ttu-id="eee9f-131">Nome dell'istanza gestita in cui si trovano i backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eee9f-132">-Location</span></span>
<span data-ttu-id="eee9f-133">Posizione dell'istanza gestita di origine dei backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="eee9f-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="eee9f-135">Se ottenere o meno solo il backup più recente per ogni database.</span><span class="sxs-lookup"><span data-stu-id="eee9f-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="eee9f-136">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="eee9f-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee9f-137">-ResourceGroupName</span></span>
<span data-ttu-id="eee9f-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eee9f-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eee9f-139">-ResourceId</span></span>
<span data-ttu-id="eee9f-140">ID risorsa database per cui ottenere i backup.</span><span class="sxs-lookup"><span data-stu-id="eee9f-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee9f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eee9f-141">-Confirm</span></span>
<span data-ttu-id="eee9f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee9f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee9f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee9f-143">-WhatIf</span></span>
<span data-ttu-id="eee9f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee9f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee9f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee9f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee9f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee9f-146">CommonParameters</span></span>
<span data-ttu-id="eee9f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee9f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee9f-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eee9f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee9f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eee9f-149">INPUTS</span></span>

### <span data-ttu-id="eee9f-150">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eee9f-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="eee9f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="eee9f-151">System.String</span></span>

## <span data-ttu-id="eee9f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eee9f-152">OUTPUTS</span></span>

### <span data-ttu-id="eee9f-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="eee9f-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="eee9f-154">Note</span><span class="sxs-lookup"><span data-stu-id="eee9f-154">NOTES</span></span>

## <span data-ttu-id="eee9f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eee9f-155">RELATED LINKS</span></span>

[<span data-ttu-id="eee9f-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="eee9f-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="eee9f-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eee9f-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="eee9f-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eee9f-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="eee9f-159">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="eee9f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)