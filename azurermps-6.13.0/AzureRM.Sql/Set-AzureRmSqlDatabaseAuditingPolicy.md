---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510816"
---
# <span data-ttu-id="a9091-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a9091-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="a9091-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9091-102">SYNOPSIS</span></span>
<span data-ttu-id="a9091-103">Imposta i criteri di controllo per un database.</span><span class="sxs-lookup"><span data-stu-id="a9091-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9091-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9091-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9091-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9091-105">DESCRIPTION</span></span>
<span data-ttu-id="a9091-106">Il cmdlet **set-AzureRmSqlDatabaseAuditingPolicy** modifica i criteri di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9091-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="a9091-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="a9091-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a9091-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9091-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="a9091-109">È anche possibile definire la conservazione per la tabella log di controllo impostando il valore dei parametri *RetentionInDays* e *TableIdentifier* per definire il periodo e il seme per i nomi delle tabelle del log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9091-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="a9091-110">Specifica il parametro *eventType* per definire i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="a9091-110">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="a9091-111">Una volta eseguito correttamente il cmdlet, il controllo del database è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a9091-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="a9091-112">Per il controllo della tabella, se il database usa i criteri del server per il controllo prima di usare questo cmdlet, il controllo smette di utilizzare tale criterio.</span><span class="sxs-lookup"><span data-stu-id="a9091-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="a9091-113">Per il controllo BLOB, se il database usa i criteri del server per il controllo prima di eseguirlo, entrambi i criteri di controllo saranno affiancati.</span><span class="sxs-lookup"><span data-stu-id="a9091-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="a9091-114">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive il criterio di controllo corrente oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="a9091-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="a9091-115">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="a9091-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="a9091-116">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="a9091-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a9091-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9091-117">EXAMPLES</span></span>

### <span data-ttu-id="a9091-118">Esempio 1: impostare i criteri di controllo di un database per l'uso del controllo della tabella</span><span class="sxs-lookup"><span data-stu-id="a9091-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="a9091-119">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01 per usare l'account di archiviazione denominato Storage31.</span><span class="sxs-lookup"><span data-stu-id="a9091-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="a9091-120">Esempio 2: impostare la chiave dell'account di archiviazione di un criterio di controllo esistente di un database</span><span class="sxs-lookup"><span data-stu-id="a9091-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="a9091-121">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01 per conservare l'uso dello stesso nome dell'account di archiviazione, ma ora usare la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="a9091-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="a9091-122">Esempio 3: impostare i criteri di controllo di un database per l'uso di un tipo di evento specifico</span><span class="sxs-lookup"><span data-stu-id="a9091-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="a9091-123">Esempio 4: impostare i criteri di controllo di un database per l'uso del controllo BLOB</span><span class="sxs-lookup"><span data-stu-id="a9091-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="a9091-124">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01.</span><span class="sxs-lookup"><span data-stu-id="a9091-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="a9091-125">Il criterio registra il tipo di evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="a9091-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="a9091-126">Il comando non modifica le impostazioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9091-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="a9091-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9091-127">PARAMETERS</span></span>

### <span data-ttu-id="a9091-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="a9091-128">-AuditAction</span></span>
<span data-ttu-id="a9091-129">Specificare una o più azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9091-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="a9091-130">Questo parametro è applicabile solo al controllo BLOB.</span><span class="sxs-lookup"><span data-stu-id="a9091-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="a9091-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a9091-131">-AuditActionGroup</span></span>
<span data-ttu-id="a9091-132">Specificare uno o più gruppi di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9091-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="a9091-133">Questo parametro è applicabile solo al controllo BLOB.</span><span class="sxs-lookup"><span data-stu-id="a9091-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="a9091-134">-AuditType</span><span class="sxs-lookup"><span data-stu-id="a9091-134">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9091-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9091-135">-DatabaseName</span></span>
<span data-ttu-id="a9091-136">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="a9091-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a9091-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9091-137">-DefaultProfile</span></span>
<span data-ttu-id="a9091-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a9091-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9091-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="a9091-139">-EventType</span></span>
<span data-ttu-id="a9091-140">Specifica i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="a9091-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="a9091-141">Questo parametro è applicabile solo al controllo della tabella.</span><span class="sxs-lookup"><span data-stu-id="a9091-141">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="a9091-142">Puoi specificare diversi tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="a9091-142">You can specify several event types.</span></span>
<span data-ttu-id="a9091-143">Puoi specificare tutti per controllare tutti i tipi di evento o nessuno per specificare che non verranno controllati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="a9091-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="a9091-144">Se si specificano tutti o nessuno contemporaneamente, il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9091-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9091-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9091-145">-PassThru</span></span>
<span data-ttu-id="a9091-146">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a9091-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a9091-147">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a9091-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9091-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9091-148">-ResourceGroupName</span></span>
<span data-ttu-id="a9091-149">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="a9091-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a9091-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a9091-150">-RetentionInDays</span></span>
<span data-ttu-id="a9091-151">Specifica il numero di giorni di conservazione per la tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9091-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="a9091-152">Un valore pari a zero (0) indica che la tabella non viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="a9091-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="a9091-153">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="a9091-153">The default value is zero.</span></span>
<span data-ttu-id="a9091-154">Se specifichi un valore maggiore di zero, devi specificare un valore per il parametro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="a9091-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="a9091-155">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a9091-155">-ServerName</span></span>
<span data-ttu-id="a9091-156">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="a9091-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a9091-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9091-157">-StorageAccountName</span></span>
<span data-ttu-id="a9091-158">Specifica il nome dell'account di archiviazione per il controllo del database.</span><span class="sxs-lookup"><span data-stu-id="a9091-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="a9091-159">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="a9091-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="a9091-160">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a9091-160">This parameter is not required.</span></span>
<span data-ttu-id="a9091-161">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo del database.</span><span class="sxs-lookup"><span data-stu-id="a9091-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="a9091-162">Se è la prima volta che si definisce un criterio di controllo del database e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="a9091-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="a9091-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a9091-163">-StorageKeyType</span></span>
<span data-ttu-id="a9091-164">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="a9091-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="a9091-165">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9091-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9091-166">Principale</span><span class="sxs-lookup"><span data-stu-id="a9091-166">Primary</span></span>
- <span data-ttu-id="a9091-167">Secondario il valore predefinito è Primary.</span><span class="sxs-lookup"><span data-stu-id="a9091-167">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="a9091-168">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="a9091-168">-TableIdentifier</span></span>
<span data-ttu-id="a9091-169">Specifica il nome della tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a9091-169">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="a9091-170">Specificare questo valore se si specifica un valore maggiore di zero per il parametro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="a9091-170">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="a9091-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9091-171">-Confirm</span></span>
<span data-ttu-id="a9091-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9091-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9091-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9091-173">-WhatIf</span></span>
<span data-ttu-id="a9091-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9091-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9091-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9091-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9091-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9091-176">CommonParameters</span></span>
<span data-ttu-id="a9091-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9091-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9091-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9091-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9091-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9091-179">INPUTS</span></span>

### <span data-ttu-id="a9091-180">Microsoft. Azure. Commands. SQL. auditing. Model. AuditType</span><span class="sxs-lookup"><span data-stu-id="a9091-180">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="a9091-181">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="a9091-181">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="a9091-182">System. String []</span><span class="sxs-lookup"><span data-stu-id="a9091-182">System.String[]</span></span>

### <span data-ttu-id="a9091-183">System. String</span><span class="sxs-lookup"><span data-stu-id="a9091-183">System.String</span></span>

### <span data-ttu-id="a9091-184">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9091-184">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a9091-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9091-185">OUTPUTS</span></span>

### <span data-ttu-id="a9091-186">Microsoft. Azure. Commands. SQL. auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a9091-186">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="a9091-187">Note</span><span class="sxs-lookup"><span data-stu-id="a9091-187">NOTES</span></span>

## <span data-ttu-id="a9091-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9091-188">RELATED LINKS</span></span>

[<span data-ttu-id="a9091-189">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="a9091-189">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="a9091-190">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a9091-190">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="a9091-191">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a9091-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


