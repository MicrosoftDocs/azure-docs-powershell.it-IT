---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 16fa9df22141b62f8a5b7ff3b6cad3ca05b1d406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857682"
---
# <span data-ttu-id="ec5c8-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="ec5c8-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="ec5c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5c8-103">Imposta le impostazioni avanzate di protezione dalle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="ec5c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec5c8-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec5c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ec5c8-106">Il cmdlet **Update-AzSqlServerAdvancedThreatProtectionSettings** imposta le impostazioni avanzate per la protezione delle minacce in un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="ec5c8-107">Per abilitare la protezione avanzata dalle minacce in un server, è necessario abilitare le impostazioni di controllo nel server.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="ec5c8-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e ServerName per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="ec5c8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec5c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ec5c8-110">Esempio 1: impostare le impostazioni avanzate di protezione dalle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="ec5c8-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ec5c8-111">Questo comando imposta le impostazioni avanzate di protezione dalle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="ec5c8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec5c8-112">PARAMETERS</span></span>

### <span data-ttu-id="ec5c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5c8-113">-DefaultProfile</span></span>
<span data-ttu-id="ec5c8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec5c8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec5c8-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="ec5c8-115">-EmailAdmins</span></span>
<span data-ttu-id="ec5c8-116">Specifica se le impostazioni avanzate di protezione dalle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="ec5c8-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ec5c8-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="ec5c8-118">Specifica una matrice di tipi di rilevamento da escludere dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="ec5c8-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec5c8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec5c8-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="ec5c8-120">Sql_Injection</span></span>
- <span data-ttu-id="ec5c8-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="ec5c8-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="ec5c8-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="ec5c8-122">Access_Anomaly</span></span>
- <span data-ttu-id="ec5c8-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec5c8-123">None</span></span>

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

### <span data-ttu-id="ec5c8-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="ec5c8-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="ec5c8-125">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui le impostazioni inviano avvisi.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="ec5c8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec5c8-126">-PassThru</span></span>
<span data-ttu-id="ec5c8-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec5c8-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec5c8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec5c8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec5c8-130">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="ec5c8-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ec5c8-131">-RetentionInDays</span></span>
<span data-ttu-id="ec5c8-132">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="ec5c8-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="ec5c8-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ec5c8-133">-ServerName</span></span>
<span data-ttu-id="ec5c8-134">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5c8-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec5c8-135">-StorageAccountName</span></span>
<span data-ttu-id="ec5c8-136">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="ec5c8-137">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-137">Wildcards are not permitted.</span></span> <span data-ttu-id="ec5c8-138">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-138">This parameter is not required.</span></span> <span data-ttu-id="ec5c8-139">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte delle impostazioni avanzate per la protezione delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="ec5c8-140">Se è la prima volta che si definiscono le impostazioni per il rilevamento delle minacce di database e questo parametro non è disponibile, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="ec5c8-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec5c8-141">-Confirm</span></span>
<span data-ttu-id="ec5c8-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec5c8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec5c8-143">-WhatIf</span></span>
<span data-ttu-id="ec5c8-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec5c8-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec5c8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5c8-146">CommonParameters</span></span>
<span data-ttu-id="ec5c8-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5c8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5c8-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec5c8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5c8-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec5c8-149">INPUTS</span></span>

### <span data-ttu-id="ec5c8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ec5c8-150">System.String</span></span>

### <span data-ttu-id="ec5c8-151">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec5c8-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec5c8-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="ec5c8-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="ec5c8-153">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec5c8-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ec5c8-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec5c8-154">OUTPUTS</span></span>

### <span data-ttu-id="ec5c8-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ec5c8-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ec5c8-156">Note</span><span class="sxs-lookup"><span data-stu-id="ec5c8-156">NOTES</span></span>

## <span data-ttu-id="ec5c8-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec5c8-157">RELATED LINKS</span></span>

[<span data-ttu-id="ec5c8-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ec5c8-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="ec5c8-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="ec5c8-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="ec5c8-160">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ec5c8-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
