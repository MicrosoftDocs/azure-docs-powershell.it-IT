---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 01f9d475e678cee5b2fc131108a18bc5abec280d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957933"
---
# <span data-ttu-id="3b2da-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3b2da-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="3b2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b2da-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2da-103">Elimina un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="3b2da-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="3b2da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b2da-104">SYNTAX</span></span>

### <span data-ttu-id="3b2da-105">RemoveBackupDefault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b2da-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b2da-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b2da-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b2da-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b2da-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b2da-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b2da-108">DESCRIPTION</span></span>
<span data-ttu-id="3b2da-109">Il cmdlet **Remove-AzSqlDatabaseLongTermRetentionBackup** elimina il backup specificato.</span><span class="sxs-lookup"><span data-stu-id="3b2da-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="3b2da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b2da-110">EXAMPLES</span></span>

### <span data-ttu-id="3b2da-111">Esempio 1: Eliminare un singolo backup con un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3b2da-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="3b2da-112">Elimina il backup con nome 601061b7-d10b-46e0-bf77-a2bfb16a6add;1316556665500000000</span><span class="sxs-lookup"><span data-stu-id="3b2da-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="3b2da-113">Esempio 2: Eliminare un singolo backup senza gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3b2da-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="3b2da-114">Elimina il backup con nome 601061b7-d10b-46e0-bf77-a2bfb16a6add;1316556665500000000</span><span class="sxs-lookup"><span data-stu-id="3b2da-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="3b2da-115">Esempio 3: Eliminare tutti i backup per una posizione</span><span class="sxs-lookup"><span data-stu-id="3b2da-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="3b2da-116">Questo comando elimina tutti i backup di conservazione a lungo termine per la località nordeuropea.</span><span class="sxs-lookup"><span data-stu-id="3b2da-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="3b2da-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b2da-117">PARAMETERS</span></span>

### <span data-ttu-id="3b2da-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3b2da-118">-BackupName</span></span>
<span data-ttu-id="3b2da-119">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="3b2da-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b2da-120">-DatabaseName</span></span>
<span data-ttu-id="3b2da-121">Il nome del database di SQL Azure da cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="3b2da-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2da-122">-DefaultProfile</span></span>
<span data-ttu-id="3b2da-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b2da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b2da-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3b2da-124">-Force</span></span>
<span data-ttu-id="3b2da-125">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="3b2da-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b2da-126">-InputObject</span></span>
<span data-ttu-id="3b2da-127">Oggetto backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3b2da-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-128">-Location</span><span class="sxs-lookup"><span data-stu-id="3b2da-128">-Location</span></span>
<span data-ttu-id="3b2da-129">Posizione del server di origine dei backup.</span><span class="sxs-lookup"><span data-stu-id="3b2da-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b2da-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b2da-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b2da-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b2da-132">-ResourceId</span></span>
<span data-ttu-id="3b2da-133">ID risorsa del backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3b2da-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b2da-134">-ServerName</span></span>
<span data-ttu-id="3b2da-135">Il nome della copia di SQL Server azure in cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="3b2da-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b2da-136">-Confirm</span></span>
<span data-ttu-id="3b2da-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b2da-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b2da-138">-WhatIf</span></span>
<span data-ttu-id="3b2da-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b2da-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b2da-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b2da-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b2da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2da-141">CommonParameters</span></span>
<span data-ttu-id="3b2da-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b2da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2da-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b2da-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2da-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b2da-144">INPUTS</span></span>

### <span data-ttu-id="3b2da-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3b2da-145">System.String</span></span>

## <span data-ttu-id="3b2da-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b2da-146">OUTPUTS</span></span>

### <span data-ttu-id="3b2da-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3b2da-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="3b2da-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b2da-148">NOTES</span></span>

## <span data-ttu-id="3b2da-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b2da-149">RELATED LINKS</span></span>

[<span data-ttu-id="3b2da-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3b2da-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3b2da-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b2da-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3b2da-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b2da-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3b2da-153">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="3b2da-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)