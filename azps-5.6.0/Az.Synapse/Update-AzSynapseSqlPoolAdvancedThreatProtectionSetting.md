---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994726"
---
# <span data-ttu-id="bbdbd-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="bbdbd-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="bbdbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdbd-103">Configura le impostazioni di protezione dalle minacce avanzate in un pool SQL avanzata.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="bbdbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbdbd-104">SYNTAX</span></span>

### <span data-ttu-id="bbdbd-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbdbd-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdbd-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdbd-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdbd-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdbd-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdbd-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdbd-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdbd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbdbd-109">DESCRIPTION</span></span>
<span data-ttu-id="bbdbd-110">Il cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** configura le impostazioni di Protezione avanzata dalle minacce in un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="bbdbd-111">Per abilitare advanced threat protection in un pool SQL è necessario abilitare le impostazioni di controllo in tale pool SQL sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="bbdbd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbdbd-112">EXAMPLES</span></span>

### <span data-ttu-id="bbdbd-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbdbd-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="bbdbd-114">Questo comando imposta le impostazioni di Protezione avanzata dalle minacce per un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="bbdbd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbdbd-115">PARAMETERS</span></span>

### <span data-ttu-id="bbdbd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbdbd-116">-AsJob</span></span>
<span data-ttu-id="bbdbd-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bbdbd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbdbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdbd-118">-DefaultProfile</span></span>
<span data-ttu-id="bbdbd-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbdbd-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="bbdbd-120">-EmailAdmin</span></span>
<span data-ttu-id="bbdbd-121">Definisce se agli amministratori di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="bbdbd-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="bbdbd-123">Tipi di rilevamento da escludere.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-123">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbdbd-124">-InputObject</span></span>
<span data-ttu-id="bbdbd-125">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bbdbd-126">-Name</span></span>
<span data-ttu-id="bbdbd-127">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="bbdbd-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="bbdbd-129">Elenco separato da punti e virgola degli indirizzi di posta elettronica a cui inviare gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdbd-130">-ResourceGroupName</span></span>
<span data-ttu-id="bbdbd-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbdbd-132">-ResourceId</span></span>
<span data-ttu-id="bbdbd-133">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bbdbd-134">-RetentionInDays</span></span>
<span data-ttu-id="bbdbd-135">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bbdbd-136">-StorageAccountName</span></span>
<span data-ttu-id="bbdbd-137">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-137">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbdbd-138">-WorkspaceName</span></span>
<span data-ttu-id="bbdbd-139">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bbdbd-140">-WorkspaceObject</span></span>
<span data-ttu-id="bbdbd-141">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdbd-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdbd-142">-Confirm</span></span>
<span data-ttu-id="bbdbd-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdbd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdbd-144">-WhatIf</span></span>
<span data-ttu-id="bbdbd-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdbd-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdbd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdbd-147">CommonParameters</span></span>
<span data-ttu-id="bbdbd-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdbd-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbdbd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdbd-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbdbd-150">INPUTS</span></span>

### <span data-ttu-id="bbdbd-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbdbd-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bbdbd-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bbdbd-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bbdbd-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbdbd-153">OUTPUTS</span></span>

### <span data-ttu-id="bbdbd-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="bbdbd-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="bbdbd-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbdbd-155">NOTES</span></span>

## <span data-ttu-id="bbdbd-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbdbd-156">RELATED LINKS</span></span>
