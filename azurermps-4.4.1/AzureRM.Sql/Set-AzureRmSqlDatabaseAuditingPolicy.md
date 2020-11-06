---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510235"
---
# <span data-ttu-id="f33c3-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f33c3-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="f33c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f33c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f33c3-103">Imposta i criteri di controllo per un database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f33c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f33c3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f33c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f33c3-106">Il cmdlet **set-AzureRmSqlDatabaseAuditingPolicy** modifica i criteri di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f33c3-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="f33c3-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f33c3-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f33c3-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="f33c3-109">È anche possibile definire la conservazione per la tabella log di controllo impostando il valore dei parametri *RetentionInDays* e *TableIdentifier* per definire il periodo e il seme per i nomi delle tabelle del log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f33c3-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="f33c3-110">Specifica il parametro *eventType* per definire i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="f33c3-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="f33c3-111">Una volta eseguito correttamente il cmdlet, il controllo del database è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f33c3-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="f33c3-112">Se il database ha usato i criteri del server per il controllo prima di aver eseguito questo cmdlet, il controllo smette di usare tale criterio.</span><span class="sxs-lookup"><span data-stu-id="f33c3-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="f33c3-113">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive il criterio di controllo corrente oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="f33c3-114">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="f33c3-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="f33c3-115">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="f33c3-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f33c3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f33c3-116">EXAMPLES</span></span>

### <span data-ttu-id="f33c3-117">Esempio 1: impostare i criteri di controllo di un database per l'uso del controllo della tabella</span><span class="sxs-lookup"><span data-stu-id="f33c3-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="f33c3-118">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01 per usare l'account di archiviazione denominato Storage31.</span><span class="sxs-lookup"><span data-stu-id="f33c3-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="f33c3-119">Esempio 2: impostare la chiave dell'account di archiviazione di un criterio di controllo esistente di un database</span><span class="sxs-lookup"><span data-stu-id="f33c3-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="f33c3-120">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01 per conservare l'uso dello stesso nome dell'account di archiviazione, ma ora usare la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="f33c3-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="f33c3-121">Esempio 3: impostare i criteri di controllo di un database per l'uso di un tipo di evento specifico</span><span class="sxs-lookup"><span data-stu-id="f33c3-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="f33c3-122">Esempio 4: impostare i criteri di controllo di un database per l'uso del controllo BLOB</span><span class="sxs-lookup"><span data-stu-id="f33c3-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="f33c3-123">Questo comando imposta il criterio di controllo del database denominato Database01 situato in Server01.</span><span class="sxs-lookup"><span data-stu-id="f33c3-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="f33c3-124">Il criterio registra il tipo di evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="f33c3-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="f33c3-125">Il comando non modifica le impostazioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f33c3-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="f33c3-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f33c3-126">PARAMETERS</span></span>

### <span data-ttu-id="f33c3-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="f33c3-127">-AuditAction</span></span>
<span data-ttu-id="f33c3-128">Specificare una o più azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="f33c3-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="f33c3-129">Questo parametro è applicabile solo al controllo BLOB.</span><span class="sxs-lookup"><span data-stu-id="f33c3-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="f33c3-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f33c3-130">-AuditActionGroup</span></span>
<span data-ttu-id="f33c3-131">Specificare uno o più gruppi di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="f33c3-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="f33c3-132">Questo parametro è applicabile solo al controllo BLOB.</span><span class="sxs-lookup"><span data-stu-id="f33c3-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="f33c3-133">-AuditType</span><span class="sxs-lookup"><span data-stu-id="f33c3-133">-AuditType</span></span>
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

### <span data-ttu-id="f33c3-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f33c3-134">-DatabaseName</span></span>
<span data-ttu-id="f33c3-135">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f33c3-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="f33c3-136">-EventType</span></span>
<span data-ttu-id="f33c3-137">Specifica i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="f33c3-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="f33c3-138">Questo parametro è applicabile solo al controllo della tabella.</span><span class="sxs-lookup"><span data-stu-id="f33c3-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="f33c3-139">Puoi specificare diversi tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="f33c3-139">You can specify several event types.</span></span>
<span data-ttu-id="f33c3-140">Puoi specificare tutti per controllare tutti i tipi di evento o nessuno per specificare che non verranno controllati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f33c3-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="f33c3-141">Se si specificano tutti o nessuno contemporaneamente, il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f33c3-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="f33c3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f33c3-142">-PassThru</span></span>
<span data-ttu-id="f33c3-143">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f33c3-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f33c3-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f33c3-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f33c3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f33c3-145">-ResourceGroupName</span></span>
<span data-ttu-id="f33c3-146">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f33c3-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f33c3-147">-RetentionInDays</span></span>
<span data-ttu-id="f33c3-148">Specifica il numero di giorni di conservazione per la tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f33c3-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="f33c3-149">Un valore pari a zero (0) indica che la tabella non viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="f33c3-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="f33c3-150">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="f33c3-150">The default value is zero.</span></span>
<span data-ttu-id="f33c3-151">Se specifichi un valore maggiore di zero, devi specificare un valore per il parametro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="f33c3-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="f33c3-152">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f33c3-152">-ServerName</span></span>
<span data-ttu-id="f33c3-153">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f33c3-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f33c3-154">-StorageAccountName</span></span>
<span data-ttu-id="f33c3-155">Specifica il nome dell'account di archiviazione per il controllo del database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="f33c3-156">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="f33c3-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="f33c3-157">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f33c3-157">This parameter is not required.</span></span>
<span data-ttu-id="f33c3-158">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo del database.</span><span class="sxs-lookup"><span data-stu-id="f33c3-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="f33c3-159">Se è la prima volta che si definisce un criterio di controllo del database e non si specifica questo parametro, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="f33c3-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="f33c3-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f33c3-160">-StorageKeyType</span></span>
<span data-ttu-id="f33c3-161">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="f33c3-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="f33c3-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f33c3-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f33c3-163">Principale</span><span class="sxs-lookup"><span data-stu-id="f33c3-163">Primary</span></span>
- <span data-ttu-id="f33c3-164">Secondario</span><span class="sxs-lookup"><span data-stu-id="f33c3-164">Secondary</span></span>

<span data-ttu-id="f33c3-165">Il valore predefinito è Primary.</span><span class="sxs-lookup"><span data-stu-id="f33c3-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="f33c3-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="f33c3-166">-TableIdentifier</span></span>
<span data-ttu-id="f33c3-167">Specifica il nome della tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f33c3-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="f33c3-168">Specificare questo valore se si specifica un valore maggiore di zero per il parametro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="f33c3-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="f33c3-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f33c3-169">-Confirm</span></span>
<span data-ttu-id="f33c3-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f33c3-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f33c3-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f33c3-171">-WhatIf</span></span>
<span data-ttu-id="f33c3-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f33c3-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f33c3-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f33c3-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f33c3-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f33c3-174">-DefaultProfile</span></span>
<span data-ttu-id="f33c3-175">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f33c3-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f33c3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33c3-176">CommonParameters</span></span>
<span data-ttu-id="f33c3-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f33c3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33c3-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33c3-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33c3-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f33c3-179">INPUTS</span></span>

## <span data-ttu-id="f33c3-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f33c3-180">OUTPUTS</span></span>

### <span data-ttu-id="f33c3-181">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f33c3-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="f33c3-182">Note</span><span class="sxs-lookup"><span data-stu-id="f33c3-182">NOTES</span></span>

## <span data-ttu-id="f33c3-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f33c3-183">RELATED LINKS</span></span>

[<span data-ttu-id="f33c3-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f33c3-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f33c3-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="f33c3-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="f33c3-186">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f33c3-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


