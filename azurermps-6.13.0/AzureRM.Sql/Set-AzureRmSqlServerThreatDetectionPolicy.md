---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5e9a4e25d54be7282e4d2f0b5f83471140241c58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685902"
---
# <span data-ttu-id="967eb-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="967eb-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="967eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="967eb-102">SYNOPSIS</span></span>
<span data-ttu-id="967eb-103">Imposta un criterio di rilevamento delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="967eb-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="967eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="967eb-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="967eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="967eb-105">DESCRIPTION</span></span>
<span data-ttu-id="967eb-106">Il cmdlet **set-AzureRmSqlServerThreatDetectionPolicy** imposta un criterio di rilevamento delle minacce in un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="967eb-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="967eb-107">Per abilitare il rilevamento delle minacce in un server, è necessario che un criterio di controllo sia abilitato nel server.</span><span class="sxs-lookup"><span data-stu-id="967eb-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="967eb-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e ServerName per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="967eb-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="967eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="967eb-109">EXAMPLES</span></span>

### <span data-ttu-id="967eb-110">Esempio 1: impostare i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="967eb-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="967eb-111">Questo comando imposta i criteri di rilevamento delle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="967eb-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="967eb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="967eb-112">PARAMETERS</span></span>

### <span data-ttu-id="967eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967eb-113">-DefaultProfile</span></span>
<span data-ttu-id="967eb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="967eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="967eb-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="967eb-115">-EmailAdmins</span></span>
<span data-ttu-id="967eb-116">Specifica se i criteri di rilevamento delle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="967eb-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="967eb-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="967eb-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="967eb-118">Specifica una matrice di tipi di rilevamento da escludere dal criterio.</span><span class="sxs-lookup"><span data-stu-id="967eb-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="967eb-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="967eb-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="967eb-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="967eb-120">Sql_Injection</span></span>
- <span data-ttu-id="967eb-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="967eb-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="967eb-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="967eb-122">Access_Anomaly</span></span>
- <span data-ttu-id="967eb-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="967eb-123">None</span></span>

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

### <span data-ttu-id="967eb-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="967eb-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="967eb-125">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui il criterio invia gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="967eb-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="967eb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="967eb-126">-PassThru</span></span>
<span data-ttu-id="967eb-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="967eb-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="967eb-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="967eb-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="967eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="967eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="967eb-130">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="967eb-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="967eb-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="967eb-131">-RetentionInDays</span></span>
<span data-ttu-id="967eb-132">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="967eb-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="967eb-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="967eb-133">-ServerName</span></span>
<span data-ttu-id="967eb-134">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="967eb-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="967eb-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="967eb-135">-StorageAccountName</span></span>
<span data-ttu-id="967eb-136">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="967eb-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="967eb-137">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="967eb-137">Wildcards are not permitted.</span></span> <span data-ttu-id="967eb-138">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="967eb-138">This parameter is not required.</span></span> <span data-ttu-id="967eb-139">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte dei criteri di rilevamento delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="967eb-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="967eb-140">Se è la prima volta che viene definito un criterio di rilevamento Theat per il database e questo parametro non è disponibile, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="967eb-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="967eb-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="967eb-141">-Confirm</span></span>
<span data-ttu-id="967eb-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="967eb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967eb-143">-WhatIf</span></span>
<span data-ttu-id="967eb-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="967eb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="967eb-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="967eb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967eb-146">CommonParameters</span></span>
<span data-ttu-id="967eb-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967eb-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967eb-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967eb-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="967eb-149">INPUTS</span></span>

### <span data-ttu-id="967eb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="967eb-150">System.String</span></span>

### <span data-ttu-id="967eb-151">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="967eb-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="967eb-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="967eb-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="967eb-153">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="967eb-153">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="967eb-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="967eb-154">OUTPUTS</span></span>

### <span data-ttu-id="967eb-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="967eb-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="967eb-156">Note</span><span class="sxs-lookup"><span data-stu-id="967eb-156">NOTES</span></span>

## <span data-ttu-id="967eb-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="967eb-157">RELATED LINKS</span></span>

[<span data-ttu-id="967eb-158">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="967eb-158">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="967eb-159">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="967eb-159">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="967eb-160">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="967eb-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
