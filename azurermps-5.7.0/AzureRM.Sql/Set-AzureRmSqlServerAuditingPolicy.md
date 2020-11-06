---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514059"
---
# <span data-ttu-id="5077d-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5077d-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="5077d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5077d-102">SYNOPSIS</span></span>
<span data-ttu-id="5077d-103">Modifica i criteri di controllo di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="5077d-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5077d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5077d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5077d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5077d-105">DESCRIPTION</span></span>
<span data-ttu-id="5077d-106">Il cmdlet **set-AzureRmSqlServerAuditingPolicy** modifica i criteri di controllo di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5077d-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="5077d-107">Specifica i parametri *ResourceGroupName* e *ServerName* per identificare il server, il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="5077d-108">È anche possibile definire la conservazione per la tabella log di controllo impostando il valore dei parametri *RetentionInDays* e *TableIdentifier* per definire il periodo e il seme per i nomi delle tabelle del log di controllo.</span><span class="sxs-lookup"><span data-stu-id="5077d-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="5077d-109">Specifica il parametro *eventType* per definire i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="5077d-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="5077d-110">Dopo aver eseguito questo cmdlet, è abilitato il controllo dei database che usano i criteri di questo server.</span><span class="sxs-lookup"><span data-stu-id="5077d-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="5077d-111">Se il cmdlet riesce e si specifica il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive il criterio di controllo corrente e gli identificatori del server.</span><span class="sxs-lookup"><span data-stu-id="5077d-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="5077d-112">Gli identificatori del server includono **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="5077d-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="5077d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5077d-113">EXAMPLES</span></span>

### <span data-ttu-id="5077d-114">Esempio 1: impostare i criteri di controllo di un server SQL di Azure usare il controllo della tabella</span><span class="sxs-lookup"><span data-stu-id="5077d-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="5077d-115">Questo comando imposta i criteri di controllo del server denominato Server01 per l'uso di un account di archiviazione denominato Storage22.</span><span class="sxs-lookup"><span data-stu-id="5077d-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="5077d-116">Esempio 2: impostare la chiave dell'account di archiviazione di un criterio di controllo esistente di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="5077d-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="5077d-117">Questo comando imposta i criteri di controllo del server denominato Server01 per usare la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="5077d-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="5077d-118">Il comando non modifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5077d-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="5077d-119">Esempio 3: impostare i criteri di controllo di un server SQL di Azure per l'uso di un tipo di evento specifico</span><span class="sxs-lookup"><span data-stu-id="5077d-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="5077d-120">Esempio 4: impostare i criteri di controllo di un database per l'uso del controllo BLOB</span><span class="sxs-lookup"><span data-stu-id="5077d-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="5077d-121">Questo comando imposta i criteri di controllo del server denominato Server01 per usare il tipo di evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="5077d-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="5077d-122">Questo comando non modifica altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="5077d-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="5077d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5077d-123">PARAMETERS</span></span>

### <span data-ttu-id="5077d-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="5077d-124">-AuditActionGroup</span></span>
<span data-ttu-id="5077d-125">Specificare uno o più gruppi di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="5077d-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="5077d-126">Questo parametro è applicabile solo al controllo BLOB.</span><span class="sxs-lookup"><span data-stu-id="5077d-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="5077d-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="5077d-127">-AuditType</span></span>
<span data-ttu-id="5077d-128">Specificare il tipo di controllo.</span><span class="sxs-lookup"><span data-stu-id="5077d-128">Specify the audit type.</span></span> <span data-ttu-id="5077d-129">I log di controllo possono essere scritti nell'archiviazione di tabella o nell'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="5077d-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="5077d-130">Il controllo BLOB offre prestazioni più elevate e supporta il controllo a livello di oggetto.</span><span class="sxs-lookup"><span data-stu-id="5077d-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5077d-131">-DefaultProfile</span></span>
<span data-ttu-id="5077d-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5077d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5077d-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="5077d-133">-EventType</span></span>
<span data-ttu-id="5077d-134">Specifica i tipi di evento da controllare.</span><span class="sxs-lookup"><span data-stu-id="5077d-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="5077d-135">Questo parametro è applicabile solo al controllo della tabella.</span><span class="sxs-lookup"><span data-stu-id="5077d-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="5077d-136">Puoi specificare diversi tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="5077d-136">You can specify several event types.</span></span>
<span data-ttu-id="5077d-137">Puoi specificare tutti per controllare tutti i tipi di evento o nessuno per specificare che non verranno controllati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="5077d-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="5077d-138">Se si specificano tutti o nessuno contemporaneamente, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="5077d-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5077d-139">-PassThru</span></span>
<span data-ttu-id="5077d-140">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5077d-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5077d-141">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5077d-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5077d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5077d-142">-ResourceGroupName</span></span>
<span data-ttu-id="5077d-143">Specifica il nome del gruppo di risorse che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="5077d-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="5077d-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5077d-144">-RetentionInDays</span></span>
<span data-ttu-id="5077d-145">Specifica il numero di giorni di conservazione per la tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="5077d-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="5077d-146">Un valore pari a zero (0) indica che la tabella non viene mantenuta.</span><span class="sxs-lookup"><span data-stu-id="5077d-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="5077d-147">Questa è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5077d-147">this is the default.</span></span>
<span data-ttu-id="5077d-148">Se specifichi un valore maggiore di zero, devi anche specificare un valore per il parametro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="5077d-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="5077d-149">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5077d-149">-ServerName</span></span>
<span data-ttu-id="5077d-150">Specifica il nome del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="5077d-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5077d-151">-StorageAccountName</span></span>
<span data-ttu-id="5077d-152">Specifica il nome dell'account di archiviazione per il controllo del database.</span><span class="sxs-lookup"><span data-stu-id="5077d-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="5077d-153">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="5077d-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="5077d-154">Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo del database.</span><span class="sxs-lookup"><span data-stu-id="5077d-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="5077d-155">Se è la prima volta che si definisce un criterio di controllo del database e non si specifica questo parametro, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="5077d-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="5077d-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="5077d-156">-StorageKeyType</span></span>
<span data-ttu-id="5077d-157">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="5077d-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5077d-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5077d-159">Principale</span><span class="sxs-lookup"><span data-stu-id="5077d-159">Primary</span></span>
- <span data-ttu-id="5077d-160">Secondario</span><span class="sxs-lookup"><span data-stu-id="5077d-160">Secondary</span></span>

<span data-ttu-id="5077d-161">Il valore predefinito è Primary.</span><span class="sxs-lookup"><span data-stu-id="5077d-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="5077d-162">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="5077d-162">-TableIdentifier</span></span>
<span data-ttu-id="5077d-163">Specifica il nome della tabella log di controllo.</span><span class="sxs-lookup"><span data-stu-id="5077d-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="5077d-164">Specificare questo valore se si specifica un valore maggiore di zero per il parametro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="5077d-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="5077d-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5077d-165">-Confirm</span></span>
<span data-ttu-id="5077d-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5077d-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5077d-167">-WhatIf</span></span>
<span data-ttu-id="5077d-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5077d-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5077d-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5077d-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5077d-170">CommonParameters</span></span>
<span data-ttu-id="5077d-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5077d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5077d-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5077d-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5077d-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5077d-173">INPUTS</span></span>

### <span data-ttu-id="5077d-174">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5077d-174">None</span></span>
<span data-ttu-id="5077d-175">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5077d-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5077d-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5077d-176">OUTPUTS</span></span>

### <span data-ttu-id="5077d-177">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5077d-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="5077d-178">Note</span><span class="sxs-lookup"><span data-stu-id="5077d-178">NOTES</span></span>

## <span data-ttu-id="5077d-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5077d-179">RELATED LINKS</span></span>

[<span data-ttu-id="5077d-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5077d-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="5077d-181">Usare-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5077d-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="5077d-182">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="5077d-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


