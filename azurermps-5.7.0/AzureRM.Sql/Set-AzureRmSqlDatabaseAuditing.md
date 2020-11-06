---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512180"
---
# <span data-ttu-id="30585-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="30585-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="30585-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30585-102">SYNOPSIS</span></span>
<span data-ttu-id="30585-103">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="30585-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30585-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30585-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30585-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30585-105">DESCRIPTION</span></span>
<span data-ttu-id="30585-106">Il cmdlet **set-AzureRmSqlDatabaseAuditing** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="30585-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="30585-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="30585-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="30585-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="30585-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="30585-109">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="30585-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="30585-110">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="30585-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="30585-111">Una volta eseguito correttamente il cmdlet, il controllo del database è abilitato.</span><span class="sxs-lookup"><span data-stu-id="30585-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="30585-112">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="30585-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="30585-113">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="30585-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="30585-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30585-114">EXAMPLES</span></span>

### <span data-ttu-id="30585-115">Esempio 1: abilitare i criteri di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="30585-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="30585-116">Esempio 2: disabilitare i criteri di controllo BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="30585-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="30585-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30585-117">PARAMETERS</span></span>

### <span data-ttu-id="30585-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="30585-118">-AuditAction</span></span>
<span data-ttu-id="30585-119">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="30585-119">The set of audit actions.</span></span>  
<span data-ttu-id="30585-120">Le azioni supportate per il controllo sono:</span><span class="sxs-lookup"><span data-stu-id="30585-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="30585-121">Selezionare</span><span class="sxs-lookup"><span data-stu-id="30585-121">SELECT</span></span>  
<span data-ttu-id="30585-122">AGGIORNAMENTO</span><span class="sxs-lookup"><span data-stu-id="30585-122">UPDATE</span></span>  
<span data-ttu-id="30585-123">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="30585-123">INSERT</span></span>  
<span data-ttu-id="30585-124">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="30585-124">DELETE</span></span>  
<span data-ttu-id="30585-125">ESEGUIRE</span><span class="sxs-lookup"><span data-stu-id="30585-125">EXECUTE</span></span>  
<span data-ttu-id="30585-126">RICEVERE</span><span class="sxs-lookup"><span data-stu-id="30585-126">RECEIVE</span></span>  
<span data-ttu-id="30585-127">RIFERIMENTI</span><span class="sxs-lookup"><span data-stu-id="30585-127">REFERENCES</span></span>  

<span data-ttu-id="30585-128">Il modulo generale per la definizione di un'azione da controllare è:</span><span class="sxs-lookup"><span data-stu-id="30585-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="30585-129">azione IN [oggetto] per [Principal]</span><span class="sxs-lookup"><span data-stu-id="30585-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="30585-130">Tieni presente che [Object] nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="30585-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="30585-131">Per questi ultimi casi, vengono usati rispettivamente il DATABASE delle maschere:: [dbname] e lo SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="30585-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="30585-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="30585-132">For example:</span></span>  
<span data-ttu-id="30585-133">Selezionare su dbo. MyTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="30585-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="30585-134">Selezionare nel DATABASE:: database per pubblico</span><span class="sxs-lookup"><span data-stu-id="30585-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="30585-135">Selezionare su SCHEMA:: schema per pubblico</span><span class="sxs-lookup"><span data-stu-id="30585-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="30585-136">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="30585-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="30585-137">-AuditActionGroup</span></span>
<span data-ttu-id="30585-138">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="30585-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="30585-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="30585-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="30585-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="30585-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="30585-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="30585-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="30585-142">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="30585-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="30585-143">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="30585-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="30585-144">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="30585-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30585-145">-DatabaseName</span></span>
<span data-ttu-id="30585-146">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="30585-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30585-147">-DefaultProfile</span></span>
<span data-ttu-id="30585-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30585-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30585-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30585-149">-PassThru</span></span>
<span data-ttu-id="30585-150">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="30585-150">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="30585-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30585-151">-ResourceGroupName</span></span>
<span data-ttu-id="30585-152">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30585-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="30585-153">-RetentionInDays</span></span>
<span data-ttu-id="30585-154">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="30585-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-155">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="30585-155">-ServerName</span></span>
<span data-ttu-id="30585-156">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="30585-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-157">-Stato</span><span class="sxs-lookup"><span data-stu-id="30585-157">-State</span></span>
<span data-ttu-id="30585-158">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="30585-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="30585-159">-StorageAccountName</span></span>
<span data-ttu-id="30585-160">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="30585-160">The name of the storage account.</span></span> <span data-ttu-id="30585-161">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="30585-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="30585-162">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="30585-162">This parameter is not required.</span></span>  
<span data-ttu-id="30585-163">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="30585-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="30585-164">Se è la prima volta che si definisce un criterio di controllo e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="30585-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="30585-165">-StorageKeyType</span></span>
<span data-ttu-id="30585-166">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="30585-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30585-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30585-167">-Confirm</span></span>
<span data-ttu-id="30585-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30585-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30585-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30585-169">-WhatIf</span></span>
<span data-ttu-id="30585-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30585-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30585-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30585-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30585-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30585-172">CommonParameters</span></span>
<span data-ttu-id="30585-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30585-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30585-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30585-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30585-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30585-175">INPUTS</span></span>

### <span data-ttu-id="30585-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30585-176">None</span></span>
<span data-ttu-id="30585-177">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="30585-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30585-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30585-178">OUTPUTS</span></span>

### <span data-ttu-id="30585-179">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="30585-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="30585-180">Note</span><span class="sxs-lookup"><span data-stu-id="30585-180">NOTES</span></span>

## <span data-ttu-id="30585-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30585-181">RELATED LINKS</span></span>