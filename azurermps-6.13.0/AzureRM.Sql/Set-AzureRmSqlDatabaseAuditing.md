---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510820"
---
# <span data-ttu-id="333b0-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="333b0-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="333b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="333b0-102">SYNOPSIS</span></span>
<span data-ttu-id="333b0-103">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="333b0-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="333b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="333b0-104">SYNTAX</span></span>

### <span data-ttu-id="333b0-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="333b0-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="333b0-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="333b0-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333b0-107">DESCRIPTION</span></span>
<span data-ttu-id="333b0-108">Il cmdlet **set-AzureRmSqlDatabaseAuditing** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="333b0-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="333b0-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="333b0-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="333b0-110">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="333b0-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="333b0-111">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="333b0-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="333b0-112">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="333b0-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="333b0-113">Una volta eseguito correttamente il cmdlet, il controllo del database è abilitato.</span><span class="sxs-lookup"><span data-stu-id="333b0-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="333b0-114">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="333b0-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="333b0-115">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="333b0-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="333b0-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="333b0-116">EXAMPLES</span></span>

### <span data-ttu-id="333b0-117">Esempio 1: abilitare i criteri di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="333b0-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="333b0-118">Esempio 2: disabilitare i criteri di controllo BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="333b0-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="333b0-119">Esempio 3: abilitare i criteri di controllo di un database SQL di Azure usando un account di archiviazione da un abbonamento diverso</span><span class="sxs-lookup"><span data-stu-id="333b0-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="333b0-120">Esempio 4: abilitare i criteri di controllo esteso di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="333b0-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="333b0-121">Esempio 5: rimuovere i criteri di controllo esteso di un database SQL di Azure e impostare un criterio di controllo anziché.</span><span class="sxs-lookup"><span data-stu-id="333b0-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="333b0-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="333b0-122">PARAMETERS</span></span>

### <span data-ttu-id="333b0-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="333b0-123">-AuditAction</span></span>
<span data-ttu-id="333b0-124">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="333b0-124">The set of audit actions.</span></span>
<span data-ttu-id="333b0-125">Le azioni supportate per il controllo sono: selezionare Aggiorna Inserisci Elimina eseguire i riferimenti il modulo generale per la definizione di un'azione da controllare è: [azione] [oggetto] per [Principal] Nota che [oggetto] nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="333b0-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="333b0-126">Per questi ultimi casi, vengono usati rispettivamente il DATABASE delle maschere:: [dbname] e lo SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="333b0-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="333b0-127">Ad esempio: selezionare su dbo. MyTable in base a selezione pubblica in DATABASE:: database per selezionare pubblica su SCHEMA:: schema per pubblico per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="333b0-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="333b0-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="333b0-128">-AuditActionGroup</span></span>
<span data-ttu-id="333b0-129">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti, ovvero "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="333b0-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="333b0-130">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="333b0-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="333b0-131">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="333b0-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333b0-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="333b0-132">-DatabaseName</span></span>
<span data-ttu-id="333b0-133">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="333b0-133">SQL Database name.</span></span>

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

### <span data-ttu-id="333b0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b0-134">-DefaultProfile</span></span>
<span data-ttu-id="333b0-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="333b0-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333b0-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="333b0-136">-PassThru</span></span>
<span data-ttu-id="333b0-137">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="333b0-137">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="333b0-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="333b0-138">-PredicateExpression</span></span>
<span data-ttu-id="333b0-139">L'istruzione della clausola WHERE usata per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="333b0-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="333b0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333b0-140">-ResourceGroupName</span></span>
<span data-ttu-id="333b0-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="333b0-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="333b0-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="333b0-142">-RetentionInDays</span></span>
<span data-ttu-id="333b0-143">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="333b0-143">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="333b0-144">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="333b0-144">-ServerName</span></span>
<span data-ttu-id="333b0-145">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="333b0-145">SQL Database server name.</span></span>

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

### <span data-ttu-id="333b0-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="333b0-146">-State</span></span>
<span data-ttu-id="333b0-147">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="333b0-147">The state of the policy.</span></span>

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

### <span data-ttu-id="333b0-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="333b0-148">-StorageAccountName</span></span>
<span data-ttu-id="333b0-149">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="333b0-149">The name of the storage account.</span></span> <span data-ttu-id="333b0-150">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="333b0-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="333b0-151">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="333b0-151">This parameter is not required.</span></span>
<span data-ttu-id="333b0-152">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="333b0-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="333b0-153">Se è la prima volta che si definisce un criterio di controllo e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="333b0-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333b0-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="333b0-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="333b0-155">Specifica l'ID abbonamento dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="333b0-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333b0-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="333b0-156">-StorageKeyType</span></span>
<span data-ttu-id="333b0-157">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="333b0-157">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="333b0-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="333b0-158">-Confirm</span></span>
<span data-ttu-id="333b0-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333b0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333b0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333b0-160">-WhatIf</span></span>
<span data-ttu-id="333b0-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="333b0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="333b0-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="333b0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333b0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b0-163">CommonParameters</span></span>
<span data-ttu-id="333b0-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333b0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b0-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333b0-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b0-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="333b0-166">INPUTS</span></span>

## <span data-ttu-id="333b0-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="333b0-167">OUTPUTS</span></span>

## <span data-ttu-id="333b0-168">Note</span><span class="sxs-lookup"><span data-stu-id="333b0-168">NOTES</span></span>

## <span data-ttu-id="333b0-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="333b0-169">RELATED LINKS</span></span>
