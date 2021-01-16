---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375843"
---
# <span data-ttu-id="a5f5d-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a5f5d-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a5f5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f5d-103">Aggiorna le impostazioni avanzate di protezione dalle minacce in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="a5f5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5f5d-104">SYNTAX</span></span>

### <span data-ttu-id="a5f5d-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5f5d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f5d-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f5d-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f5d-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f5d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f5d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f5d-108">DESCRIPTION</span></span>
<span data-ttu-id="a5f5d-109">Il cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** aggiorna le impostazioni avanzate di protezione dalle minacce in un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="a5f5d-110">Per abilitare la protezione avanzata dalle minacce in un'area di lavoro, è necessario abilitare le impostazioni di controllo nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="a5f5d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5f5d-111">EXAMPLES</span></span>

### <span data-ttu-id="a5f5d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5f5d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="a5f5d-113">Questo comando Aggiorna le impostazioni avanzate di protezione dalle minacce per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a5f5d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="a5f5d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5f5d-115">-AsJob</span></span>
<span data-ttu-id="a5f5d-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a5f5d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5f5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f5d-117">-DefaultProfile</span></span>
<span data-ttu-id="a5f5d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5f5d-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="a5f5d-119">-EmailAdmin</span></span>
<span data-ttu-id="a5f5d-120">Definisce se gli amministratori di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="a5f5d-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="a5f5d-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="a5f5d-122">Tipi di rilevamento da escludere.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="a5f5d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5f5d-123">-InputObject</span></span>
<span data-ttu-id="a5f5d-124">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5f5d-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="a5f5d-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="a5f5d-126">Elenco separato da un punto e virgola di indirizzi di posta elettronica a cui inviare gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="a5f5d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f5d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5f5d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-128">Resource group name.</span></span>

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

### <span data-ttu-id="a5f5d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5f5d-129">-ResourceId</span></span>
<span data-ttu-id="a5f5d-130">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5f5d-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a5f5d-131">-RetentionInDays</span></span>
<span data-ttu-id="a5f5d-132">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a5f5d-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5f5d-133">-StorageAccountName</span></span>
<span data-ttu-id="a5f5d-134">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="a5f5d-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5f5d-135">-WorkspaceName</span></span>
<span data-ttu-id="a5f5d-136">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5f5d-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5f5d-137">-Confirm</span></span>
<span data-ttu-id="a5f5d-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f5d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f5d-139">-WhatIf</span></span>
<span data-ttu-id="a5f5d-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f5d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f5d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f5d-142">CommonParameters</span></span>
<span data-ttu-id="a5f5d-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f5d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f5d-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5f5d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f5d-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5f5d-145">INPUTS</span></span>

### <span data-ttu-id="a5f5d-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5f5d-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a5f5d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5f5d-147">OUTPUTS</span></span>

### <span data-ttu-id="a5f5d-148">Microsoft. Azure. Commands. sinapsi. Models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a5f5d-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="a5f5d-149">Note</span><span class="sxs-lookup"><span data-stu-id="a5f5d-149">NOTES</span></span>

## <span data-ttu-id="a5f5d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5f5d-150">RELATED LINKS</span></span>
