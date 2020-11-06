---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519669"
---
# <span data-ttu-id="26b1e-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="26b1e-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="26b1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="26b1e-103">Modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="26b1e-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26b1e-104">SYNTAX</span></span>

### <span data-ttu-id="26b1e-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26b1e-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b1e-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="26b1e-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26b1e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="26b1e-108">Il cmdlet **set-AzureRmSqlServerAuditing** modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="26b1e-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="26b1e-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="26b1e-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="26b1e-110">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26b1e-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="26b1e-111">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="26b1e-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="26b1e-112">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="26b1e-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="26b1e-113">Dopo l'esecuzione del cmdlet, è abilitato il controllo dei database SQL di Azure definiti nell'Azure SQL Server specificato.</span><span class="sxs-lookup"><span data-stu-id="26b1e-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="26b1e-114">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del server.</span><span class="sxs-lookup"><span data-stu-id="26b1e-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="26b1e-115">Gli identificatori del server includono, ma non sono limitati a, **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="26b1e-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="26b1e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26b1e-116">EXAMPLES</span></span>

### <span data-ttu-id="26b1e-117">Esempio 1: abilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="26b1e-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="26b1e-118">Esempio 2: disabilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="26b1e-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="26b1e-119">Esempio 3: abilitare i criteri di controllo di un server SQL di Azure usando un account di archiviazione da un abbonamento diverso</span><span class="sxs-lookup"><span data-stu-id="26b1e-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="26b1e-120">Esempio 4: abilitare i criteri di controllo esteso di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="26b1e-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="26b1e-121">Esempio 5: rimuovere i criteri di controllo esteso di un database SQL di Azure e impostare un criterio di controllo anziché.</span><span class="sxs-lookup"><span data-stu-id="26b1e-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="26b1e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26b1e-122">PARAMETERS</span></span>

### <span data-ttu-id="26b1e-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="26b1e-123">-AuditActionGroup</span></span>
<span data-ttu-id="26b1e-124">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti, ovvero "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26b1e-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="26b1e-125">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="26b1e-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="26b1e-126">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="26b1e-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="26b1e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b1e-127">-DefaultProfile</span></span>
<span data-ttu-id="26b1e-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26b1e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b1e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26b1e-129">-PassThru</span></span>
<span data-ttu-id="26b1e-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26b1e-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="26b1e-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="26b1e-131">-PredicateExpression</span></span>
<span data-ttu-id="26b1e-132">L'istruzione della clausola WHERE usata per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="26b1e-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="26b1e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b1e-133">-ResourceGroupName</span></span>
<span data-ttu-id="26b1e-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26b1e-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="26b1e-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="26b1e-135">-RetentionInDays</span></span>
<span data-ttu-id="26b1e-136">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="26b1e-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="26b1e-137">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="26b1e-137">-ServerName</span></span>
<span data-ttu-id="26b1e-138">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="26b1e-138">SQL server name.</span></span>

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

### <span data-ttu-id="26b1e-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="26b1e-139">-State</span></span>
<span data-ttu-id="26b1e-140">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="26b1e-140">The state of the policy.</span></span>

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

### <span data-ttu-id="26b1e-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="26b1e-141">-StorageAccountName</span></span>
<span data-ttu-id="26b1e-142">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="26b1e-142">The name of the storage account.</span></span> <span data-ttu-id="26b1e-143">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="26b1e-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="26b1e-144">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26b1e-144">This parameter is not required.</span></span>
<span data-ttu-id="26b1e-145">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="26b1e-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="26b1e-146">Se è la prima volta che si definisce un criterio di controllo e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="26b1e-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="26b1e-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26b1e-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="26b1e-148">Specifica l'ID abbonamento dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="26b1e-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="26b1e-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="26b1e-149">-StorageKeyType</span></span>
<span data-ttu-id="26b1e-150">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="26b1e-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="26b1e-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26b1e-151">-Confirm</span></span>
<span data-ttu-id="26b1e-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b1e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b1e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b1e-153">-WhatIf</span></span>
<span data-ttu-id="26b1e-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26b1e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26b1e-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26b1e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b1e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b1e-156">CommonParameters</span></span>
<span data-ttu-id="26b1e-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b1e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b1e-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b1e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b1e-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26b1e-159">INPUTS</span></span>

## <span data-ttu-id="26b1e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26b1e-160">OUTPUTS</span></span>

## <span data-ttu-id="26b1e-161">Note</span><span class="sxs-lookup"><span data-stu-id="26b1e-161">NOTES</span></span>

## <span data-ttu-id="26b1e-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26b1e-162">RELATED LINKS</span></span>
