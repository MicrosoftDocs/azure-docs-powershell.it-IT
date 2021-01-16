---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375829"
---
# <span data-ttu-id="3253a-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3253a-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3253a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3253a-102">SYNOPSIS</span></span>
<span data-ttu-id="3253a-103">Imposta impostazioni avanzate per la protezione delle minacce in un pool SQL.</span><span class="sxs-lookup"><span data-stu-id="3253a-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="3253a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3253a-104">SYNTAX</span></span>

### <span data-ttu-id="3253a-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3253a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3253a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3253a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3253a-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3253a-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3253a-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3253a-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3253a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3253a-109">DESCRIPTION</span></span>
<span data-ttu-id="3253a-110">Il cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** imposta le impostazioni avanzate per la protezione delle minacce in un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="3253a-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="3253a-111">Per abilitare la protezione avanzata dalle minacce in un pool SQL, è necessario abilitare le impostazioni di controllo nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="3253a-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="3253a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3253a-112">EXAMPLES</span></span>

### <span data-ttu-id="3253a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3253a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="3253a-114">Questo comando imposta le impostazioni avanzate di protezione dalle minacce per un pool SQL denominato ContosoSqlPool sotto l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3253a-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3253a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3253a-115">PARAMETERS</span></span>

### <span data-ttu-id="3253a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3253a-116">-AsJob</span></span>
<span data-ttu-id="3253a-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3253a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3253a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3253a-118">-DefaultProfile</span></span>
<span data-ttu-id="3253a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3253a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3253a-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="3253a-120">-EmailAdmin</span></span>
<span data-ttu-id="3253a-121">Definisce se gli amministratori di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="3253a-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="3253a-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="3253a-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="3253a-123">Tipi di rilevamento da escludere.</span><span class="sxs-lookup"><span data-stu-id="3253a-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="3253a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3253a-124">-InputObject</span></span>
<span data-ttu-id="3253a-125">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3253a-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3253a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3253a-126">-Name</span></span>
<span data-ttu-id="3253a-127">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="3253a-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="3253a-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="3253a-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="3253a-129">Elenco separato da un punto e virgola di indirizzi di posta elettronica a cui inviare gli avvisi.</span><span class="sxs-lookup"><span data-stu-id="3253a-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="3253a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3253a-130">-ResourceGroupName</span></span>
<span data-ttu-id="3253a-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3253a-131">Resource group name.</span></span>

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

### <span data-ttu-id="3253a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3253a-132">-ResourceId</span></span>
<span data-ttu-id="3253a-133">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="3253a-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="3253a-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3253a-134">-RetentionInDays</span></span>
<span data-ttu-id="3253a-135">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="3253a-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="3253a-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3253a-136">-StorageAccountName</span></span>
<span data-ttu-id="3253a-137">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3253a-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="3253a-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3253a-138">-WorkspaceName</span></span>
<span data-ttu-id="3253a-139">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3253a-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3253a-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3253a-140">-WorkspaceObject</span></span>
<span data-ttu-id="3253a-141">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3253a-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3253a-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3253a-142">-Confirm</span></span>
<span data-ttu-id="3253a-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3253a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3253a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3253a-144">-WhatIf</span></span>
<span data-ttu-id="3253a-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3253a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3253a-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3253a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3253a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3253a-147">CommonParameters</span></span>
<span data-ttu-id="3253a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3253a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3253a-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3253a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3253a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3253a-150">INPUTS</span></span>

### <span data-ttu-id="3253a-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3253a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3253a-152">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3253a-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3253a-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3253a-153">OUTPUTS</span></span>

### <span data-ttu-id="3253a-154">Microsoft. Azure. Commands. sinapsi. Models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="3253a-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="3253a-155">Note</span><span class="sxs-lookup"><span data-stu-id="3253a-155">NOTES</span></span>

## <span data-ttu-id="3253a-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3253a-156">RELATED LINKS</span></span>
