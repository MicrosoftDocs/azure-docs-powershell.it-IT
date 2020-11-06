---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518272"
---
# <span data-ttu-id="037ad-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="037ad-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="037ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="037ad-102">SYNOPSIS</span></span>
<span data-ttu-id="037ad-103">Modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="037ad-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="037ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="037ad-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="037ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="037ad-105">DESCRIPTION</span></span>
<span data-ttu-id="037ad-106">Il cmdlet **set-AzureRmSqlServerAuditing** modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="037ad-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="037ad-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="037ad-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="037ad-108">Specifica il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="037ad-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="037ad-109">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="037ad-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="037ad-110">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="037ad-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="037ad-111">Dopo l'esecuzione del cmdlet, è abilitato il controllo dei database SQL di Azure definiti nell'Azure SQL Server specificato.</span><span class="sxs-lookup"><span data-stu-id="037ad-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="037ad-112">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive i criteri di controllo BLOB correnti oltre agli identificatori del server.</span><span class="sxs-lookup"><span data-stu-id="037ad-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="037ad-113">Gli identificatori del server includono, ma non sono limitati a, **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="037ad-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="037ad-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="037ad-114">EXAMPLES</span></span>

### <span data-ttu-id="037ad-115">Esempio 1: abilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="037ad-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="037ad-116">Esempio 2: disabilitare i criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="037ad-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="037ad-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="037ad-117">PARAMETERS</span></span>

### <span data-ttu-id="037ad-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="037ad-118">-AuditActionGroup</span></span>
<span data-ttu-id="037ad-119">Set di gruppi di azioni di controllo</span><span class="sxs-lookup"><span data-stu-id="037ad-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="037ad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="037ad-120">-PassThru</span></span>
<span data-ttu-id="037ad-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="037ad-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="037ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="037ad-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="037ad-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="037ad-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="037ad-124">-RetentionInDays</span></span>
<span data-ttu-id="037ad-125">Numero di giorni di conservazione per i registri di controllo</span><span class="sxs-lookup"><span data-stu-id="037ad-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="037ad-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="037ad-126">-ServerName</span></span>
<span data-ttu-id="037ad-127">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="037ad-127">SQL server name.</span></span>

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

### <span data-ttu-id="037ad-128">-Stato</span><span class="sxs-lookup"><span data-stu-id="037ad-128">-State</span></span>
<span data-ttu-id="037ad-129">Stato del criterio di controllo</span><span class="sxs-lookup"><span data-stu-id="037ad-129">The state of the auditing policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037ad-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="037ad-130">-StorageAccountName</span></span>
<span data-ttu-id="037ad-131">Nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="037ad-131">The name of the storage account</span></span>

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

### <span data-ttu-id="037ad-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="037ad-132">-StorageKeyType</span></span>
<span data-ttu-id="037ad-133">Tipo di chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="037ad-133">The type of the storage key</span></span>

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

### <span data-ttu-id="037ad-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="037ad-134">-Confirm</span></span>
<span data-ttu-id="037ad-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="037ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037ad-136">-WhatIf</span></span>
<span data-ttu-id="037ad-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="037ad-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="037ad-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="037ad-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037ad-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037ad-139">-DefaultProfile</span></span>
<span data-ttu-id="037ad-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="037ad-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="037ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037ad-141">CommonParameters</span></span>
<span data-ttu-id="037ad-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037ad-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="037ad-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037ad-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="037ad-144">INPUTS</span></span>

## <span data-ttu-id="037ad-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="037ad-145">OUTPUTS</span></span>

### <span data-ttu-id="037ad-146">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="037ad-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="037ad-147">Note</span><span class="sxs-lookup"><span data-stu-id="037ad-147">NOTES</span></span>

## <span data-ttu-id="037ad-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="037ad-148">RELATED LINKS</span></span>

