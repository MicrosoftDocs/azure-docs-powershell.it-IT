---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514647"
---
# <span data-ttu-id="8f186-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8f186-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="8f186-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f186-102">SYNOPSIS</span></span>
<span data-ttu-id="8f186-103">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f186-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f186-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f186-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f186-105">DESCRIPTION</span></span>
<span data-ttu-id="8f186-106">Il cmdlet **set-AzureRmSqlDatabaseAuditing** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f186-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="8f186-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="8f186-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="8f186-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8f186-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="8f186-109">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="8f186-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="8f186-110">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="8f186-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="8f186-111">Una volta eseguito correttamente il cmdlet, il controllo del database è abilitato.</span><span class="sxs-lookup"><span data-stu-id="8f186-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="8f186-112">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="8f186-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="8f186-113">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="8f186-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="8f186-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f186-114">EXAMPLES</span></span>

### <span data-ttu-id="8f186-115">Esempio 1: abilitare i criteri di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8f186-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="8f186-116">Esempio 2: disabilitare i criteri di controllo BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8f186-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="8f186-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f186-117">PARAMETERS</span></span>

### <span data-ttu-id="8f186-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="8f186-118">-AuditAction</span></span>
<span data-ttu-id="8f186-119">Il set di azioni di controllo</span><span class="sxs-lookup"><span data-stu-id="8f186-119">The set of the audit actions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8f186-120">-AuditActionGroup</span></span>
<span data-ttu-id="8f186-121">Set di gruppi di azioni di controllo</span><span class="sxs-lookup"><span data-stu-id="8f186-121">The set of the audit action groups</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f186-122">-DatabaseName</span></span>
<span data-ttu-id="8f186-123">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="8f186-123">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f186-124">-PassThru</span></span>
<span data-ttu-id="8f186-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8f186-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8f186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f186-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f186-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f186-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8f186-128">-RetentionInDays</span></span>
<span data-ttu-id="8f186-129">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="8f186-129">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8f186-130">-ServerName</span></span>
<span data-ttu-id="8f186-131">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="8f186-131">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="8f186-132">-State</span></span>
<span data-ttu-id="8f186-133">Stato del criterio di controllo</span><span class="sxs-lookup"><span data-stu-id="8f186-133">The state of the auditing policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f186-134">-StorageAccountName</span></span>
<span data-ttu-id="8f186-135">Nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8f186-135">The name of the storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8f186-136">-StorageKeyType</span></span>
<span data-ttu-id="8f186-137">Tipo di chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8f186-137">The type of the storage key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f186-138">-Confirm</span></span>
<span data-ttu-id="8f186-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f186-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f186-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f186-140">-WhatIf</span></span>
<span data-ttu-id="8f186-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f186-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f186-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f186-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f186-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f186-143">-DefaultProfile</span></span>
<span data-ttu-id="8f186-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f186-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f186-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f186-145">CommonParameters</span></span>
<span data-ttu-id="8f186-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f186-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f186-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f186-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f186-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f186-148">INPUTS</span></span>

## <span data-ttu-id="8f186-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f186-149">OUTPUTS</span></span>

### <span data-ttu-id="8f186-150">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="8f186-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8f186-151">Note</span><span class="sxs-lookup"><span data-stu-id="8f186-151">NOTES</span></span>

## <span data-ttu-id="8f186-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f186-152">RELATED LINKS</span></span>

