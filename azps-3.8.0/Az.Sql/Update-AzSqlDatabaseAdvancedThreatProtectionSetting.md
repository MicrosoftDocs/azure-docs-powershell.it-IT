---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: baa3e3d4b272bccab5fe33b9af05edc9ed254236
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402542"
---
# <span data-ttu-id="9d5ed-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9d5ed-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9d5ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5ed-103">Configura le impostazioni di Protezione avanzata dalle minacce in un database.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="9d5ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d5ed-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5ed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d5ed-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5ed-106">Il cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** configura le impostazioni di Protezione avanzata dalle minacce in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="9d5ed-107">Per abilitare Advanced Threat Protection in un database, è necessario abilitare le impostazioni di controllo in tale database.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="9d5ed-108">Per usare questo cmdlet, specificare i *parametri ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9d5ed-109">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9d5ed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d5ed-110">EXAMPLES</span></span>

### <span data-ttu-id="9d5ed-111">Esempio 1: Configurare le impostazioni di Protezione avanzata dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="9d5ed-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9d5ed-112">Questo comando configura le impostazioni di Protezione avanzata dalle minacce per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9d5ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d5ed-113">PARAMETERS</span></span>

### <span data-ttu-id="9d5ed-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d5ed-114">-DatabaseName</span></span>
<span data-ttu-id="9d5ed-115">Specifica il nome del database in cui sono impostate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="9d5ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5ed-116">-DefaultProfile</span></span>
<span data-ttu-id="9d5ed-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9d5ed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d5ed-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="9d5ed-118">-EmailAdmins</span></span>
<span data-ttu-id="9d5ed-119">Specifica se le impostazioni di Protezione avanzata dalle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="9d5ed-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9d5ed-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="9d5ed-121">Specifica una matrice di tipi di rilevamento da escludere dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="9d5ed-122">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="9d5ed-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d5ed-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="9d5ed-123">Sql_Injection</span></span>
- <span data-ttu-id="9d5ed-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="9d5ed-124">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="9d5ed-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="9d5ed-125">Access_Anomaly</span></span>
- <span data-ttu-id="9d5ed-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9d5ed-126">None</span></span>

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

### <span data-ttu-id="9d5ed-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="9d5ed-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="9d5ed-128">Specifica un elenco di indirizzi di posta elettronica separati da punto e virgola a cui le impostazioni inviano avvisi.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="9d5ed-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d5ed-129">-PassThru</span></span>
<span data-ttu-id="9d5ed-130">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9d5ed-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d5ed-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5ed-132">-ResourceGroupName</span></span>
<span data-ttu-id="9d5ed-133">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9d5ed-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9d5ed-134">-RetentionInDays</span></span>
<span data-ttu-id="9d5ed-135">Il numero di giorni di conservazione per i log di controllo</span><span class="sxs-lookup"><span data-stu-id="9d5ed-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9d5ed-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d5ed-136">-ServerName</span></span>
<span data-ttu-id="9d5ed-137">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9d5ed-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d5ed-138">-StorageAccountName</span></span>
<span data-ttu-id="9d5ed-139">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="9d5ed-140">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-140">Wildcards are not permitted.</span></span> <span data-ttu-id="9d5ed-141">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-141">This parameter is not required.</span></span> <span data-ttu-id="9d5ed-142">Se questo parametro non è disponibile, il cmdlet userà l'account di archiviazione definito in precedenza nelle impostazioni di Protezione avanzata dalle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="9d5ed-143">Se è la prima volta che vengono definite le impostazioni di Protezione avanzata dalle minacce del database e questo parametro non viene fornito, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="9d5ed-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d5ed-144">-Confirm</span></span>
<span data-ttu-id="9d5ed-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5ed-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5ed-146">-WhatIf</span></span>
<span data-ttu-id="9d5ed-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5ed-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5ed-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5ed-149">CommonParameters</span></span>
<span data-ttu-id="9d5ed-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5ed-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d5ed-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5ed-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d5ed-152">INPUTS</span></span>

### <span data-ttu-id="9d5ed-153">System.String</span><span class="sxs-lookup"><span data-stu-id="9d5ed-153">System.String</span></span>

### <span data-ttu-id="9d5ed-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9d5ed-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="9d5ed-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9d5ed-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9d5ed-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d5ed-157">OUTPUTS</span></span>

### <span data-ttu-id="9d5ed-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="9d5ed-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="9d5ed-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d5ed-159">NOTES</span></span>

## <span data-ttu-id="9d5ed-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d5ed-160">RELATED LINKS</span></span>

[<span data-ttu-id="9d5ed-161">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="9d5ed-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
