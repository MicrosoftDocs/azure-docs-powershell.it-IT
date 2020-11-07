---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: fe8a76ed0851393462ba94937d2ab92914b503b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687249"
---
# <span data-ttu-id="06009-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06009-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="06009-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06009-102">SYNOPSIS</span></span>
<span data-ttu-id="06009-103">Imposta un criterio di rilevamento delle minacce in un database.</span><span class="sxs-lookup"><span data-stu-id="06009-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06009-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06009-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06009-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06009-105">DESCRIPTION</span></span>
<span data-ttu-id="06009-106">Il cmdlet **set-AzureRmSqlDatabaseThreatDetectionPolicy** imposta un criterio di rilevamento delle minacce in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="06009-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="06009-107">Per abilitare il rilevamento delle minacce in un database, è necessario che sia abilitato un criterio di controllo nel database.</span><span class="sxs-lookup"><span data-stu-id="06009-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="06009-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="06009-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="06009-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="06009-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="06009-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06009-110">EXAMPLES</span></span>

### <span data-ttu-id="06009-111">Esempio 1: impostare i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="06009-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="06009-112">Questo comando imposta i criteri di rilevamento delle minacce per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="06009-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="06009-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06009-113">PARAMETERS</span></span>

### <span data-ttu-id="06009-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06009-114">-DatabaseName</span></span>
<span data-ttu-id="06009-115">Specifica il nome del database in cui è impostato il criterio.</span><span class="sxs-lookup"><span data-stu-id="06009-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="06009-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06009-116">-DefaultProfile</span></span>
<span data-ttu-id="06009-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="06009-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06009-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="06009-118">-EmailAdmins</span></span>
<span data-ttu-id="06009-119">Specifica se i criteri di rilevamento delle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="06009-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="06009-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="06009-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="06009-121">Specifica una matrice di tipi di rilevamento da escludere dal criterio.</span><span class="sxs-lookup"><span data-stu-id="06009-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="06009-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06009-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06009-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="06009-123">Sql_Injection</span></span> 
- <span data-ttu-id="06009-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="06009-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="06009-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="06009-125">Access_Anomaly</span></span> 
- <span data-ttu-id="06009-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06009-126">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06009-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="06009-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="06009-128">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui il criterio invia gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="06009-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="06009-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06009-129">-PassThru</span></span>
<span data-ttu-id="06009-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="06009-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06009-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="06009-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06009-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06009-132">-ResourceGroupName</span></span>
<span data-ttu-id="06009-133">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="06009-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="06009-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="06009-134">-RetentionInDays</span></span>
<span data-ttu-id="06009-135">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="06009-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="06009-136">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06009-136">-ServerName</span></span>
<span data-ttu-id="06009-137">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="06009-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="06009-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06009-138">-StorageAccountName</span></span>
<span data-ttu-id="06009-139">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="06009-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="06009-140">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="06009-140">Wildcards are not permitted.</span></span> <span data-ttu-id="06009-141">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="06009-141">This parameter is not required.</span></span> <span data-ttu-id="06009-142">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte dei criteri di rilevamento delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="06009-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="06009-143">Se è la prima volta che viene definito un criterio di rilevamento delle minacce per il database e questo parametro non viene specificato, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="06009-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="06009-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06009-144">-Confirm</span></span>
<span data-ttu-id="06009-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06009-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06009-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06009-146">-WhatIf</span></span>
<span data-ttu-id="06009-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06009-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06009-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06009-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06009-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06009-149">CommonParameters</span></span>
<span data-ttu-id="06009-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06009-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06009-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06009-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06009-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06009-152">INPUTS</span></span>

### <span data-ttu-id="06009-153">System. String</span><span class="sxs-lookup"><span data-stu-id="06009-153">System.String</span></span>

### <span data-ttu-id="06009-154">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06009-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="06009-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="06009-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="06009-156">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06009-156">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="06009-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06009-157">OUTPUTS</span></span>

### <span data-ttu-id="06009-158">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="06009-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="06009-159">Note</span><span class="sxs-lookup"><span data-stu-id="06009-159">NOTES</span></span>

## <span data-ttu-id="06009-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06009-160">RELATED LINKS</span></span>

[<span data-ttu-id="06009-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06009-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="06009-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06009-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="06009-163">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="06009-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


