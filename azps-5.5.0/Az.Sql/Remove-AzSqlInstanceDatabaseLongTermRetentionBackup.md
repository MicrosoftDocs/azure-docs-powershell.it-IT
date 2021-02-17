---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188023"
---
# <span data-ttu-id="afe75-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="afe75-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="afe75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe75-102">SYNOPSIS</span></span>
<span data-ttu-id="afe75-103">Elimina un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="afe75-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="afe75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afe75-104">SYNTAX</span></span>

### <span data-ttu-id="afe75-105">RemoveBackupDefault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afe75-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe75-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="afe75-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe75-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="afe75-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe75-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="afe75-108">DESCRIPTION</span></span>
<span data-ttu-id="afe75-109">Il cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** elimina il backup specificato.</span><span class="sxs-lookup"><span data-stu-id="afe75-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="afe75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afe75-110">EXAMPLES</span></span>

### <span data-ttu-id="afe75-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afe75-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="afe75-112">Elimina il backup con nome 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span><span class="sxs-lookup"><span data-stu-id="afe75-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="afe75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afe75-113">PARAMETERS</span></span>

### <span data-ttu-id="afe75-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="afe75-114">-BackupName</span></span>
<span data-ttu-id="afe75-115">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="afe75-115">The name of the backup.</span></span>

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

### <span data-ttu-id="afe75-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="afe75-116">-DatabaseName</span></span>
<span data-ttu-id="afe75-117">Il nome del database gestito da cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="afe75-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="afe75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe75-118">-DefaultProfile</span></span>
<span data-ttu-id="afe75-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afe75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe75-120">-Force</span><span class="sxs-lookup"><span data-stu-id="afe75-120">-Force</span></span>
<span data-ttu-id="afe75-121">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="afe75-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="afe75-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afe75-122">-InputObject</span></span>
<span data-ttu-id="afe75-123">Oggetto backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="afe75-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="afe75-124">-InstanceName</span></span>
<span data-ttu-id="afe75-125">Nome dell'istanza gestita in cui si trova il backup.</span><span class="sxs-lookup"><span data-stu-id="afe75-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="afe75-126">-Location</span><span class="sxs-lookup"><span data-stu-id="afe75-126">-Location</span></span>
<span data-ttu-id="afe75-127">Posizione dell'istanza gestita di origine dei backup.</span><span class="sxs-lookup"><span data-stu-id="afe75-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="afe75-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe75-128">-ResourceGroupName</span></span>
<span data-ttu-id="afe75-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="afe75-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="afe75-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afe75-130">-ResourceId</span></span>
<span data-ttu-id="afe75-131">ID risorsa del backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="afe75-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="afe75-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afe75-132">-Confirm</span></span>
<span data-ttu-id="afe75-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afe75-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe75-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe75-134">-WhatIf</span></span>
<span data-ttu-id="afe75-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afe75-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe75-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afe75-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe75-137">CommonParameters</span></span>
<span data-ttu-id="afe75-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe75-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="afe75-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe75-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="afe75-140">INPUTS</span></span>

### <span data-ttu-id="afe75-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="afe75-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="afe75-142">System.String</span><span class="sxs-lookup"><span data-stu-id="afe75-142">System.String</span></span>

## <span data-ttu-id="afe75-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afe75-143">OUTPUTS</span></span>

### <span data-ttu-id="afe75-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="afe75-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="afe75-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="afe75-145">NOTES</span></span>

## <span data-ttu-id="afe75-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afe75-146">RELATED LINKS</span></span>

[<span data-ttu-id="afe75-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="afe75-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="afe75-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="afe75-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="afe75-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="afe75-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="afe75-150">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="afe75-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)