---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512819"
---
# <span data-ttu-id="0026e-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0026e-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="0026e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0026e-102">SYNOPSIS</span></span>
<span data-ttu-id="0026e-103">Imposta un criterio di rilevamento delle minacce in un database.</span><span class="sxs-lookup"><span data-stu-id="0026e-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0026e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0026e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0026e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0026e-105">DESCRIPTION</span></span>
<span data-ttu-id="0026e-106">Il cmdlet **set-AzureRmSqlDatabaseThreatDetectionPolicy** imposta un criterio di rilevamento delle minacce in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0026e-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="0026e-107">Per abilitare il rilevamento delle minacce in un database, è necessario che sia abilitato un criterio di controllo nel database.</span><span class="sxs-lookup"><span data-stu-id="0026e-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="0026e-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="0026e-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="0026e-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="0026e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0026e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0026e-110">EXAMPLES</span></span>

### <span data-ttu-id="0026e-111">Esempio 1: impostare i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="0026e-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="0026e-112">Questo comando imposta i criteri di rilevamento delle minacce per un database denominato Database01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="0026e-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0026e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0026e-113">PARAMETERS</span></span>

### <span data-ttu-id="0026e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0026e-114">-DatabaseName</span></span>
<span data-ttu-id="0026e-115">Specifica il nome del database in cui è impostato il criterio.</span><span class="sxs-lookup"><span data-stu-id="0026e-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="0026e-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0026e-116">-EmailAdmins</span></span>
<span data-ttu-id="0026e-117">Specifica se i criteri di rilevamento delle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="0026e-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="0026e-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="0026e-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="0026e-119">Specifica una matrice di tipi di rilevamento da escludere dal criterio.</span><span class="sxs-lookup"><span data-stu-id="0026e-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="0026e-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0026e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0026e-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="0026e-121">Sql_Injection</span></span> 
- <span data-ttu-id="0026e-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="0026e-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="0026e-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="0026e-123">Access_Anomaly</span></span> 
- <span data-ttu-id="0026e-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0026e-124">None</span></span>

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

### <span data-ttu-id="0026e-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="0026e-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="0026e-126">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui il criterio invia gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="0026e-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="0026e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0026e-127">-PassThru</span></span>
<span data-ttu-id="0026e-128">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0026e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0026e-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0026e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0026e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0026e-130">-ResourceGroupName</span></span>
<span data-ttu-id="0026e-131">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="0026e-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0026e-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0026e-132">-RetentionInDays</span></span>
<span data-ttu-id="0026e-133">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="0026e-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="0026e-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0026e-134">-ServerName</span></span>
<span data-ttu-id="0026e-135">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="0026e-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0026e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0026e-136">-StorageAccountName</span></span>
<span data-ttu-id="0026e-137">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="0026e-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="0026e-138">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="0026e-138">Wildcards are not permitted.</span></span> <span data-ttu-id="0026e-139">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0026e-139">This parameter is not required.</span></span> <span data-ttu-id="0026e-140">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte dei criteri di rilevamento delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="0026e-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="0026e-141">Se è la prima volta che viene definito un criterio di rilevamento delle minacce per il database e questo parametro non viene specificato, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0026e-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="0026e-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0026e-142">-Confirm</span></span>
<span data-ttu-id="0026e-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0026e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0026e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0026e-144">-WhatIf</span></span>
<span data-ttu-id="0026e-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0026e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0026e-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0026e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0026e-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0026e-147">-DefaultProfile</span></span>
<span data-ttu-id="0026e-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0026e-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0026e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0026e-149">CommonParameters</span></span>
<span data-ttu-id="0026e-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0026e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0026e-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0026e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0026e-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0026e-152">INPUTS</span></span>

###  
<span data-ttu-id="0026e-153">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0026e-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="0026e-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0026e-154">OUTPUTS</span></span>

### <span data-ttu-id="0026e-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0026e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="0026e-156">Questo cmdlet restituisce un oggetto **Model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="0026e-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="0026e-157">Note</span><span class="sxs-lookup"><span data-stu-id="0026e-157">NOTES</span></span>

## <span data-ttu-id="0026e-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0026e-158">RELATED LINKS</span></span>

[<span data-ttu-id="0026e-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0026e-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="0026e-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0026e-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="0026e-161">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0026e-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


