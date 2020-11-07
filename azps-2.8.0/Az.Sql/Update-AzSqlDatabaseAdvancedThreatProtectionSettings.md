---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 2bbbe4e2b553055e4643cff973941095e0a468f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857689"
---
# <span data-ttu-id="0e470-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="0e470-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="0e470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e470-102">SYNOPSIS</span></span>
<span data-ttu-id="0e470-103">Imposta le impostazioni avanzate di protezione dalle minacce in un database.</span><span class="sxs-lookup"><span data-stu-id="0e470-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="0e470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e470-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e470-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e470-105">DESCRIPTION</span></span>
<span data-ttu-id="0e470-106">Il cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSettings** imposta le impostazioni avanzate per la protezione delle minacce in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e470-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="0e470-107">Per abilitare la protezione avanzata dalle minacce in un database, è necessario abilitare le impostazioni di controllo nel database.</span><span class="sxs-lookup"><span data-stu-id="0e470-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="0e470-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="0e470-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0e470-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e470-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0e470-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e470-110">EXAMPLES</span></span>

### <span data-ttu-id="0e470-111">Esempio 1: impostare le impostazioni avanzate di protezione dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="0e470-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="0e470-112">Questo comando imposta le impostazioni avanzate di protezione dalle minacce per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="0e470-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0e470-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e470-113">PARAMETERS</span></span>

### <span data-ttu-id="0e470-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e470-114">-DatabaseName</span></span>
<span data-ttu-id="0e470-115">Specifica il nome del database in cui sono impostate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0e470-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="0e470-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e470-116">-DefaultProfile</span></span>
<span data-ttu-id="0e470-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0e470-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e470-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0e470-118">-EmailAdmins</span></span>
<span data-ttu-id="0e470-119">Specifica se le impostazioni avanzate di protezione dalle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="0e470-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e470-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="0e470-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="0e470-121">Specifica una matrice di tipi di rilevamento da escludere dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0e470-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="0e470-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e470-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e470-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="0e470-123">Sql_Injection</span></span> 
- <span data-ttu-id="0e470-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="0e470-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="0e470-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="0e470-125">Access_Anomaly</span></span> 
- <span data-ttu-id="0e470-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0e470-126">None</span></span>

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

### <span data-ttu-id="0e470-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="0e470-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="0e470-128">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui le impostazioni inviano avvisi.</span><span class="sxs-lookup"><span data-stu-id="0e470-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="0e470-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e470-129">-PassThru</span></span>
<span data-ttu-id="0e470-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0e470-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e470-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0e470-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e470-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e470-132">-ResourceGroupName</span></span>
<span data-ttu-id="0e470-133">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="0e470-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0e470-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0e470-134">-RetentionInDays</span></span>
<span data-ttu-id="0e470-135">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="0e470-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="0e470-136">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0e470-136">-ServerName</span></span>
<span data-ttu-id="0e470-137">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="0e470-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0e470-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e470-138">-StorageAccountName</span></span>
<span data-ttu-id="0e470-139">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="0e470-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="0e470-140">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="0e470-140">Wildcards are not permitted.</span></span> <span data-ttu-id="0e470-141">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e470-141">This parameter is not required.</span></span> <span data-ttu-id="0e470-142">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte delle impostazioni avanzate per la protezione delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="0e470-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="0e470-143">Se è la prima volta che si definisce un database Advanced Threat Protection Settings e questo parametro non è disponibile, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0e470-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="0e470-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e470-144">-Confirm</span></span>
<span data-ttu-id="0e470-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e470-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e470-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e470-146">-WhatIf</span></span>
<span data-ttu-id="0e470-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e470-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e470-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e470-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e470-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e470-149">CommonParameters</span></span>
<span data-ttu-id="0e470-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e470-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e470-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e470-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e470-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e470-152">INPUTS</span></span>

### <span data-ttu-id="0e470-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0e470-153">System.String</span></span>

### <span data-ttu-id="0e470-154">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e470-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e470-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="0e470-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="0e470-156">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e470-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0e470-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e470-157">OUTPUTS</span></span>

### <span data-ttu-id="0e470-158">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="0e470-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="0e470-159">Note</span><span class="sxs-lookup"><span data-stu-id="0e470-159">NOTES</span></span>

## <span data-ttu-id="0e470-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e470-160">RELATED LINKS</span></span>

[<span data-ttu-id="0e470-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0e470-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="0e470-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0e470-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="0e470-163">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0e470-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


