---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514060"
---
# <span data-ttu-id="647f0-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="647f0-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="647f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="647f0-102">SYNOPSIS</span></span>
<span data-ttu-id="647f0-103">Modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647f0-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="647f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="647f0-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="647f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="647f0-105">DESCRIPTION</span></span>
<span data-ttu-id="647f0-106">Il cmdlet **set-AzureRmSqlServerAuditing** modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="647f0-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="647f0-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="647f0-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="647f0-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="647f0-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="647f0-109">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="647f0-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="647f0-110">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="647f0-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="647f0-111">Dopo l'esecuzione del cmdlet, è abilitato il controllo dei database SQL di Azure definiti nell'Azure SQL Server specificato.</span><span class="sxs-lookup"><span data-stu-id="647f0-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="647f0-112">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del server.</span><span class="sxs-lookup"><span data-stu-id="647f0-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="647f0-113">Gli identificatori del server includono, ma non sono limitati a, **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="647f0-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="647f0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="647f0-114">EXAMPLES</span></span>

### <span data-ttu-id="647f0-115">Esempio 1: abilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="647f0-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="647f0-116">Esempio 2: disabilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="647f0-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="647f0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="647f0-117">PARAMETERS</span></span>

### <span data-ttu-id="647f0-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="647f0-118">-AuditActionGroup</span></span>
<span data-ttu-id="647f0-119">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="647f0-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="647f0-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="647f0-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="647f0-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="647f0-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="647f0-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="647f0-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="647f0-123">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="647f0-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="647f0-124">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="647f0-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="647f0-125">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="647f0-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="647f0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647f0-126">-DefaultProfile</span></span>
<span data-ttu-id="647f0-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="647f0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="647f0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="647f0-128">-PassThru</span></span>
<span data-ttu-id="647f0-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="647f0-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="647f0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647f0-130">-ResourceGroupName</span></span>
<span data-ttu-id="647f0-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="647f0-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="647f0-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="647f0-132">-RetentionInDays</span></span>
<span data-ttu-id="647f0-133">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="647f0-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="647f0-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="647f0-134">-ServerName</span></span>
<span data-ttu-id="647f0-135">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="647f0-135">SQL server name.</span></span>

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

### <span data-ttu-id="647f0-136">-Stato</span><span class="sxs-lookup"><span data-stu-id="647f0-136">-State</span></span>
<span data-ttu-id="647f0-137">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="647f0-137">The state of the policy.</span></span>

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

### <span data-ttu-id="647f0-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="647f0-138">-StorageAccountName</span></span>
<span data-ttu-id="647f0-139">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="647f0-139">The name of the storage account.</span></span> <span data-ttu-id="647f0-140">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="647f0-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="647f0-141">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="647f0-141">This parameter is not required.</span></span>  
<span data-ttu-id="647f0-142">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="647f0-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="647f0-143">Se è la prima volta che si definisce un criterio di controllo e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="647f0-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="647f0-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="647f0-144">-StorageKeyType</span></span>
<span data-ttu-id="647f0-145">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="647f0-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="647f0-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="647f0-146">-Confirm</span></span>
<span data-ttu-id="647f0-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="647f0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="647f0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647f0-148">-WhatIf</span></span>
<span data-ttu-id="647f0-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647f0-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="647f0-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647f0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="647f0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647f0-151">CommonParameters</span></span>
<span data-ttu-id="647f0-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647f0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647f0-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647f0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647f0-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="647f0-154">INPUTS</span></span>

### <span data-ttu-id="647f0-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="647f0-155">None</span></span>
<span data-ttu-id="647f0-156">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="647f0-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="647f0-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="647f0-157">OUTPUTS</span></span>

### <span data-ttu-id="647f0-158">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="647f0-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="647f0-159">Note</span><span class="sxs-lookup"><span data-stu-id="647f0-159">NOTES</span></span>

## <span data-ttu-id="647f0-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="647f0-160">RELATED LINKS</span></span>
