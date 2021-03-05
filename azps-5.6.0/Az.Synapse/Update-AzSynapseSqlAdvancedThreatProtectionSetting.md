---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991912"
---
# <span data-ttu-id="f7e17-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f7e17-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f7e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7e17-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e17-103">Aggiorna le impostazioni di Protezione avanzata dalle minacce in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7e17-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="f7e17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7e17-104">SYNTAX</span></span>

### <span data-ttu-id="f7e17-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7e17-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e17-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7e17-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7e17-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7e17-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7e17-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7e17-108">DESCRIPTION</span></span>
<span data-ttu-id="f7e17-109">Il cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** aggiorna le impostazioni di Protezione avanzata dalle minacce in un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7e17-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="f7e17-110">Per abilitare la protezione avanzata dalle minacce in un'area di lavoro, è necessario che in tale area di lavoro siano abilitate le impostazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="f7e17-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="f7e17-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7e17-111">EXAMPLES</span></span>

### <span data-ttu-id="f7e17-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7e17-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="f7e17-113">Questo comando aggiorna le impostazioni di Protezione avanzata dalle minacce per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f7e17-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f7e17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7e17-114">PARAMETERS</span></span>

### <span data-ttu-id="f7e17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7e17-115">-AsJob</span></span>
<span data-ttu-id="f7e17-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7e17-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7e17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e17-117">-DefaultProfile</span></span>
<span data-ttu-id="f7e17-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e17-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="f7e17-119">-EmailAdmin</span></span>
<span data-ttu-id="f7e17-120">Definisce se agli amministratori di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f7e17-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="f7e17-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="f7e17-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="f7e17-122">Tipi di rilevamento da escludere.</span><span class="sxs-lookup"><span data-stu-id="f7e17-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="f7e17-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7e17-123">-InputObject</span></span>
<span data-ttu-id="f7e17-124">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7e17-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7e17-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="f7e17-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="f7e17-126">Elenco separato da punti e virgola degli indirizzi di posta elettronica a cui inviare gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="f7e17-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="f7e17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e17-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7e17-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7e17-128">Resource group name.</span></span>

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

### <span data-ttu-id="f7e17-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e17-129">-ResourceId</span></span>
<span data-ttu-id="f7e17-130">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7e17-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7e17-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f7e17-131">-RetentionInDays</span></span>
<span data-ttu-id="f7e17-132">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f7e17-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="f7e17-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7e17-133">-StorageAccountName</span></span>
<span data-ttu-id="f7e17-134">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7e17-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="f7e17-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7e17-135">-WorkspaceName</span></span>
<span data-ttu-id="f7e17-136">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7e17-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7e17-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7e17-137">-Confirm</span></span>
<span data-ttu-id="f7e17-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7e17-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e17-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e17-139">-WhatIf</span></span>
<span data-ttu-id="f7e17-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7e17-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e17-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7e17-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e17-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e17-142">CommonParameters</span></span>
<span data-ttu-id="f7e17-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e17-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e17-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7e17-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e17-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7e17-145">INPUTS</span></span>

### <span data-ttu-id="f7e17-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7e17-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f7e17-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7e17-147">OUTPUTS</span></span>

### <span data-ttu-id="f7e17-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="f7e17-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="f7e17-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7e17-149">NOTES</span></span>

## <span data-ttu-id="f7e17-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7e17-150">RELATED LINKS</span></span>
