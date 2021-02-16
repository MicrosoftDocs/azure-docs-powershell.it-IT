---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208946"
---
# <span data-ttu-id="be66c-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="be66c-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="be66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be66c-102">SYNOPSIS</span></span>
<span data-ttu-id="be66c-103">Aggiorna le impostazioni di Protezione avanzata dalle minacce in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="be66c-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="be66c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be66c-104">SYNTAX</span></span>

### <span data-ttu-id="be66c-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be66c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be66c-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be66c-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be66c-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be66c-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be66c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be66c-108">DESCRIPTION</span></span>
<span data-ttu-id="be66c-109">Il cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** aggiorna le impostazioni di Protezione avanzata dalle minacce in un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="be66c-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="be66c-110">Per abilitare la protezione avanzata dalle minacce in un'area di lavoro, è necessario che in tale area di lavoro siano abilitate le impostazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="be66c-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="be66c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be66c-111">EXAMPLES</span></span>

### <span data-ttu-id="be66c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be66c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="be66c-113">Questo comando aggiorna le impostazioni di Protezione avanzata dalle minacce per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="be66c-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="be66c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be66c-114">PARAMETERS</span></span>

### <span data-ttu-id="be66c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be66c-115">-AsJob</span></span>
<span data-ttu-id="be66c-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="be66c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be66c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be66c-117">-DefaultProfile</span></span>
<span data-ttu-id="be66c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be66c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be66c-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="be66c-119">-EmailAdmin</span></span>
<span data-ttu-id="be66c-120">Definisce se agli amministratori di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="be66c-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="be66c-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="be66c-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="be66c-122">Tipi di rilevamento da escludere.</span><span class="sxs-lookup"><span data-stu-id="be66c-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="be66c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be66c-123">-InputObject</span></span>
<span data-ttu-id="be66c-124">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="be66c-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be66c-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="be66c-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="be66c-126">Elenco separato da punti e virgola degli indirizzi di posta elettronica a cui inviare gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="be66c-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="be66c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be66c-127">-ResourceGroupName</span></span>
<span data-ttu-id="be66c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be66c-128">Resource group name.</span></span>

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

### <span data-ttu-id="be66c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be66c-129">-ResourceId</span></span>
<span data-ttu-id="be66c-130">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="be66c-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="be66c-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="be66c-131">-RetentionInDays</span></span>
<span data-ttu-id="be66c-132">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="be66c-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="be66c-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="be66c-133">-StorageAccountName</span></span>
<span data-ttu-id="be66c-134">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="be66c-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="be66c-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be66c-135">-WorkspaceName</span></span>
<span data-ttu-id="be66c-136">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="be66c-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="be66c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be66c-137">-Confirm</span></span>
<span data-ttu-id="be66c-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be66c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be66c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be66c-139">-WhatIf</span></span>
<span data-ttu-id="be66c-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be66c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be66c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be66c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be66c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be66c-142">CommonParameters</span></span>
<span data-ttu-id="be66c-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be66c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be66c-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be66c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be66c-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="be66c-145">INPUTS</span></span>

### <span data-ttu-id="be66c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="be66c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="be66c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be66c-147">OUTPUTS</span></span>

### <span data-ttu-id="be66c-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="be66c-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="be66c-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="be66c-149">NOTES</span></span>

## <span data-ttu-id="be66c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be66c-150">RELATED LINKS</span></span>
