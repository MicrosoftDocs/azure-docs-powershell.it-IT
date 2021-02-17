---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399499"
---
# <span data-ttu-id="b04b3-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b04b3-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="b04b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b04b3-103">Imposta un criterio di rilevamento delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="b04b3-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="b04b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b04b3-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b04b3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b04b3-105">DESCRIPTION</span></span>
<span data-ttu-id="b04b3-106">Il cmdlet **Set-AzSqlServerThreatDetectionPolicy** imposta un criterio di rilevamento delle minacce in un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b04b3-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="b04b3-107">Per abilitare il rilevamento delle minacce in un server, è necessario che in tale server sia abilitato un criterio di controllo.</span><span class="sxs-lookup"><span data-stu-id="b04b3-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="b04b3-108">Per usare questo cmdlet, specificare i *parametri ResourceGroupName* e ServerName per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="b04b3-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="b04b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b04b3-109">EXAMPLES</span></span>

### <span data-ttu-id="b04b3-110">Esempio 1: Impostare i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="b04b3-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="b04b3-111">Questo comando imposta i criteri di rilevamento delle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b04b3-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="b04b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b04b3-112">PARAMETERS</span></span>

### <span data-ttu-id="b04b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04b3-113">-DefaultProfile</span></span>
<span data-ttu-id="b04b3-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b04b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b04b3-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="b04b3-115">-EmailAdmins</span></span>
<span data-ttu-id="b04b3-116">Specifica se i criteri di rilevamento delle minacce contattano gli amministratori tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b04b3-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="b04b3-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="b04b3-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="b04b3-118">Specifica una matrice di tipi di rilevamento da escludere dal criterio.</span><span class="sxs-lookup"><span data-stu-id="b04b3-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="b04b3-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b04b3-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b04b3-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="b04b3-120">Sql_Injection</span></span>
- <span data-ttu-id="b04b3-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="b04b3-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="b04b3-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="b04b3-122">Access_Anomaly</span></span>
- <span data-ttu-id="b04b3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b04b3-123">None</span></span>

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

### <span data-ttu-id="b04b3-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="b04b3-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="b04b3-125">Specifica un elenco di indirizzi di posta elettronica separati da punto e virgola a cui vengono inviati avvisi dal criterio.</span><span class="sxs-lookup"><span data-stu-id="b04b3-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="b04b3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b04b3-126">-PassThru</span></span>
<span data-ttu-id="b04b3-127">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b04b3-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b04b3-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b04b3-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b04b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="b04b3-130">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="b04b3-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="b04b3-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b04b3-131">-RetentionInDays</span></span>
<span data-ttu-id="b04b3-132">Il numero di giorni di conservazione per i log di controllo</span><span class="sxs-lookup"><span data-stu-id="b04b3-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="b04b3-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b04b3-133">-ServerName</span></span>
<span data-ttu-id="b04b3-134">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="b04b3-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b04b3-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b04b3-135">-StorageAccountName</span></span>
<span data-ttu-id="b04b3-136">Specifica il nome dell'account di archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="b04b3-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="b04b3-137">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="b04b3-137">Wildcards are not permitted.</span></span> <span data-ttu-id="b04b3-138">Questo parametro non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b04b3-138">This parameter is not required.</span></span> <span data-ttu-id="b04b3-139">Se questo parametro non è fornito, il cmdlet userà l'account di archiviazione definito in precedenza come parte dei criteri di rilevamento delle minacce del database.</span><span class="sxs-lookup"><span data-stu-id="b04b3-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="b04b3-140">Se è la prima volta che viene definito un criterio di rilevamento diat nel database e questo parametro non viene fornito, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="b04b3-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="b04b3-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b04b3-141">-Confirm</span></span>
<span data-ttu-id="b04b3-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b04b3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04b3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04b3-143">-WhatIf</span></span>
<span data-ttu-id="b04b3-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04b3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b04b3-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04b3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04b3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04b3-146">CommonParameters</span></span>
<span data-ttu-id="b04b3-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04b3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04b3-148">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b04b3-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04b3-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="b04b3-149">INPUTS</span></span>

### <span data-ttu-id="b04b3-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b04b3-150">System.String</span></span>

### <span data-ttu-id="b04b3-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b04b3-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b04b3-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="b04b3-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="b04b3-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b04b3-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b04b3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b04b3-154">OUTPUTS</span></span>

### <span data-ttu-id="b04b3-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b04b3-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="b04b3-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="b04b3-156">NOTES</span></span>

## <span data-ttu-id="b04b3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b04b3-157">RELATED LINKS</span></span>

[<span data-ttu-id="b04b3-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b04b3-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="b04b3-159">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="b04b3-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
