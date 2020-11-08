---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189271"
---
# <span data-ttu-id="d8f36-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d8f36-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="d8f36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8f36-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f36-103">Elimina un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="d8f36-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="d8f36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8f36-104">SYNTAX</span></span>

### <span data-ttu-id="d8f36-105">RemoveBackupDefault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8f36-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f36-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8f36-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f36-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f36-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f36-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8f36-108">DESCRIPTION</span></span>
<span data-ttu-id="d8f36-109">Il cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** Elimina il backup specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f36-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="d8f36-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8f36-110">EXAMPLES</span></span>

### <span data-ttu-id="d8f36-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8f36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="d8f36-112">Elimina il backup con il nome 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="d8f36-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="d8f36-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8f36-113">PARAMETERS</span></span>

### <span data-ttu-id="d8f36-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d8f36-114">-BackupName</span></span>
<span data-ttu-id="d8f36-115">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="d8f36-115">The name of the backup.</span></span>

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

### <span data-ttu-id="d8f36-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8f36-116">-DatabaseName</span></span>
<span data-ttu-id="d8f36-117">Nome del database gestito da cui è stato fatto il backup.</span><span class="sxs-lookup"><span data-stu-id="d8f36-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="d8f36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f36-118">-DefaultProfile</span></span>
<span data-ttu-id="d8f36-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f36-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d8f36-120">-Force</span></span>
<span data-ttu-id="d8f36-121">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="d8f36-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d8f36-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f36-122">-InputObject</span></span>
<span data-ttu-id="d8f36-123">Oggetto di backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d8f36-123">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="d8f36-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d8f36-124">-InstanceName</span></span>
<span data-ttu-id="d8f36-125">Nome dell'istanza gestita in cui è presente il backup.</span><span class="sxs-lookup"><span data-stu-id="d8f36-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="d8f36-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d8f36-126">-Location</span></span>
<span data-ttu-id="d8f36-127">Posizione dell'istanza gestita di origine dei backup.</span><span class="sxs-lookup"><span data-stu-id="d8f36-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="d8f36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f36-128">-ResourceGroupName</span></span>
<span data-ttu-id="d8f36-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8f36-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8f36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f36-130">-ResourceId</span></span>
<span data-ttu-id="d8f36-131">ID risorsa del backup del database di conservazione a lungo termine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d8f36-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="d8f36-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8f36-132">-Confirm</span></span>
<span data-ttu-id="d8f36-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f36-134">-WhatIf</span></span>
<span data-ttu-id="d8f36-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f36-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f36-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f36-137">CommonParameters</span></span>
<span data-ttu-id="d8f36-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f36-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8f36-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f36-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8f36-140">INPUTS</span></span>

### <span data-ttu-id="d8f36-141">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d8f36-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="d8f36-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d8f36-142">System.String</span></span>

## <span data-ttu-id="d8f36-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8f36-143">OUTPUTS</span></span>

### <span data-ttu-id="d8f36-144">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d8f36-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="d8f36-145">Note</span><span class="sxs-lookup"><span data-stu-id="d8f36-145">NOTES</span></span>

## <span data-ttu-id="d8f36-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8f36-146">RELATED LINKS</span></span>

[<span data-ttu-id="d8f36-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d8f36-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d8f36-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f36-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d8f36-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f36-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d8f36-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d8f36-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)