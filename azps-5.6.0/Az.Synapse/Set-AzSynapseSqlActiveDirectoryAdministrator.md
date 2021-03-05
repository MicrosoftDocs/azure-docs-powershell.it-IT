---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992135"
---
# <span data-ttu-id="f7095-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f7095-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f7095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7095-102">SYNOPSIS</span></span>
<span data-ttu-id="f7095-103">Esegue il provisioning di un amministratore di Azure AD per il pool SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7095-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f7095-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7095-104">SYNTAX</span></span>

### <span data-ttu-id="f7095-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7095-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7095-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7095-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7095-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7095-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7095-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7095-108">DESCRIPTION</span></span>
<span data-ttu-id="f7095-109">Il cmdlet **Set-AzSynapseSqlActiveDirectoryAdministrator** esegue il provisioning di un amministratore di Azure Active Directory (Azure AD) per l'area di lavoro analisi di Azure Synapse nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f7095-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="f7095-110">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="f7095-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="f7095-111">È possibile eseguire il provisioning dei seguenti membri di Azure AD come amministratore dell'area di lavoro Synapse Analytics:</span><span class="sxs-lookup"><span data-stu-id="f7095-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="f7095-112">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="f7095-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="f7095-113">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="f7095-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="f7095-114">Membri importati da altri Azure ADs che sono membri nativi o federati</span><span class="sxs-lookup"><span data-stu-id="f7095-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="f7095-115">I gruppi di Azure AD creati come account Microsoft dei gruppi di sicurezza, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="f7095-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f7095-116">Gli altri account guest, ad esempio quelli nel dominio Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="f7095-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f7095-117">È consigliabile eseguire il provisioning di un gruppo di Azure AD dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="f7095-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="f7095-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7095-118">EXAMPLES</span></span>

### <span data-ttu-id="f7095-119">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7095-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="f7095-120">Questo comando esegue il provisioning di un gruppo di amministratori di Azure AD denominato DBA per l'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f7095-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f7095-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f7095-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="f7095-122">Questo comando esegue il provisioning di un gruppo di amministratori di Azure AD denominato DBA per l'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f7095-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="f7095-123">In questo modo il comando ha esito positivo anche se il nome visualizzato del gruppo non è univoco.</span><span class="sxs-lookup"><span data-stu-id="f7095-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="f7095-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7095-124">PARAMETERS</span></span>

### <span data-ttu-id="f7095-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7095-125">-AsJob</span></span>
<span data-ttu-id="f7095-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7095-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7095-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7095-127">-DefaultProfile</span></span>
<span data-ttu-id="f7095-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7095-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7095-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7095-129">-DisplayName</span></span>
<span data-ttu-id="f7095-130">Specifica il nome visualizzato dell'utente o del gruppo a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f7095-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="f7095-131">Questo nome visualizzato deve essere in Active Directory associato all'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f7095-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7095-132">-InputObject</span></span>
<span data-ttu-id="f7095-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7095-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7095-134">-ObjectId</span></span>
<span data-ttu-id="f7095-135">Specifica l'ID oggetto dell'utente o gruppo in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f7095-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7095-136">-ResourceGroupName</span></span>
<span data-ttu-id="f7095-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7095-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7095-138">-ResourceId</span></span>
<span data-ttu-id="f7095-139">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7095-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7095-140">-WorkspaceName</span></span>
<span data-ttu-id="f7095-141">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7095-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7095-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7095-142">-Confirm</span></span>
<span data-ttu-id="f7095-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7095-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7095-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7095-144">-WhatIf</span></span>
<span data-ttu-id="f7095-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7095-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7095-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7095-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7095-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7095-147">CommonParameters</span></span>
<span data-ttu-id="f7095-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7095-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7095-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7095-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7095-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7095-150">INPUTS</span></span>

### <span data-ttu-id="f7095-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7095-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f7095-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7095-152">OUTPUTS</span></span>

### <span data-ttu-id="f7095-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="f7095-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="f7095-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7095-154">NOTES</span></span>

## <span data-ttu-id="f7095-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7095-155">RELATED LINKS</span></span>
