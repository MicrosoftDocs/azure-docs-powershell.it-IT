---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521945"
---
# <span data-ttu-id="7c667-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c667-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="7c667-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c667-102">SYNOPSIS</span></span>
<span data-ttu-id="7c667-103">Imposta un criterio di rilevamento delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="7c667-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c667-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c667-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c667-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c667-105">DESCRIPTION</span></span>
<span data-ttu-id="7c667-106">Il cmdlet **set-AzureRmSqlServerThreatDetectionPolicy** imposta un criterio di rilevamento delle minacce in un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c667-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="7c667-107">Per abilitare il rilevamento delle minacce in un server, è necessario che un criterio di controllo sia abilitato nel server.</span><span class="sxs-lookup"><span data-stu-id="7c667-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="7c667-108">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e ServerName per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="7c667-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="7c667-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c667-109">EXAMPLES</span></span>

### <span data-ttu-id="7c667-110">Esempio 1: impostare i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="7c667-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="7c667-111">Questo comando imposta i criteri di rilevamento delle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="7c667-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="7c667-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c667-112">PARAMETERS</span></span>

### <span data-ttu-id="7c667-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7c667-113">-EmailAdmins</span></span>
<span data-ttu-id="7c667-114">Specifica se i criteri di rilevamento delle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="7c667-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="7c667-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="7c667-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="7c667-116">Specifica una matrice di tipi di rilevamento da escludere dal criterio.</span><span class="sxs-lookup"><span data-stu-id="7c667-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="7c667-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c667-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c667-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="7c667-118">Sql_Injection</span></span>
- <span data-ttu-id="7c667-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="7c667-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="7c667-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="7c667-120">Access_Anomaly</span></span>
- <span data-ttu-id="7c667-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c667-121">None</span></span>

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

### <span data-ttu-id="7c667-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="7c667-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="7c667-123">Specifica un elenco di indirizzi di posta elettronica separati da punti e virgola a cui il criterio invia gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="7c667-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="7c667-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c667-124">-PassThru</span></span>
<span data-ttu-id="7c667-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7c667-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c667-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7c667-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c667-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c667-127">-ResourceGroupName</span></span>
<span data-ttu-id="7c667-128">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="7c667-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="7c667-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7c667-129">-RetentionInDays</span></span>
<span data-ttu-id="7c667-130">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="7c667-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="7c667-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7c667-131">-ServerName</span></span>
<span data-ttu-id="7c667-132">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="7c667-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7c667-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c667-133">-StorageAccountName</span></span>
<span data-ttu-id="7c667-134">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="7c667-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="7c667-135">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="7c667-135">Wildcards are not permitted.</span></span> <span data-ttu-id="7c667-136">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c667-136">This parameter is not required.</span></span> <span data-ttu-id="7c667-137">Quando questo parametro non viene specificato, il cmdlet utilizzerà l'account di archiviazione definito in precedenza come parte dei criteri di rilevamento delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="7c667-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="7c667-138">Se è la prima volta che viene definito un criterio di rilevamento Theat per il database e questo parametro non è disponibile, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7c667-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="7c667-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c667-139">-Confirm</span></span>
<span data-ttu-id="7c667-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c667-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c667-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c667-141">-WhatIf</span></span>
<span data-ttu-id="7c667-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c667-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c667-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c667-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c667-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c667-144">-DefaultProfile</span></span>
<span data-ttu-id="7c667-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c667-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c667-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c667-146">CommonParameters</span></span>
<span data-ttu-id="7c667-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c667-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c667-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c667-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c667-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c667-149">INPUTS</span></span>

###  
<span data-ttu-id="7c667-150">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c667-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="7c667-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c667-151">OUTPUTS</span></span>

### <span data-ttu-id="7c667-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7c667-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="7c667-153">Questo cmdlet restituisce un oggetto **ServerThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="7c667-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="7c667-154">Note</span><span class="sxs-lookup"><span data-stu-id="7c667-154">NOTES</span></span>

## <span data-ttu-id="7c667-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c667-155">RELATED LINKS</span></span>

[<span data-ttu-id="7c667-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c667-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="7c667-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c667-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="7c667-158">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="7c667-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
