---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354223"
---
# <span data-ttu-id="27fdc-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="27fdc-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="27fdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="27fdc-103">Accantona un amministratore di Azure AD per il pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27fdc-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="27fdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27fdc-104">SYNTAX</span></span>

### <span data-ttu-id="27fdc-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27fdc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27fdc-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27fdc-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27fdc-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27fdc-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27fdc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27fdc-108">DESCRIPTION</span></span>
<span data-ttu-id="27fdc-109">Il cmdlet **set-AzSynapseSqlActiveDirectoryAdministrator** dispone di un amministratore di Azure Active Directory (Azure ad) per l'area di lavoro Azure sinapsi Analytics nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="27fdc-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="27fdc-110">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="27fdc-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="27fdc-111">I membri seguenti di Azure AD possono essere provisionati come amministratore dell'area di lavoro di sinapsi Analytics:</span><span class="sxs-lookup"><span data-stu-id="27fdc-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="27fdc-112">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="27fdc-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="27fdc-113">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="27fdc-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="27fdc-114">Membri importati da altri annunci di Azure che sono membri nativi o federati</span><span class="sxs-lookup"><span data-stu-id="27fdc-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="27fdc-115">I gruppi di Azure AD creati come gruppi di sicurezza gli account Microsoft, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="27fdc-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="27fdc-116">Gli altri account Guest, ad esempio quelli presenti nei domini Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="27fdc-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="27fdc-117">Ti consigliamo di eseguire il provisioning di un gruppo di annunci Azure dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="27fdc-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="27fdc-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27fdc-118">EXAMPLES</span></span>

### <span data-ttu-id="27fdc-119">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27fdc-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="27fdc-120">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="27fdc-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="27fdc-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="27fdc-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="27fdc-122">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="27fdc-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="27fdc-123">In questo modo si verifica che il comando abbia esito positivo anche se il nome visualizzato del gruppo non è univoco.</span><span class="sxs-lookup"><span data-stu-id="27fdc-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="27fdc-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27fdc-124">PARAMETERS</span></span>

### <span data-ttu-id="27fdc-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27fdc-125">-AsJob</span></span>
<span data-ttu-id="27fdc-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27fdc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27fdc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fdc-127">-DefaultProfile</span></span>
<span data-ttu-id="27fdc-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27fdc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27fdc-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27fdc-129">-DisplayName</span></span>
<span data-ttu-id="27fdc-130">Specifica il nome visualizzato dell'utente o del gruppo per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="27fdc-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="27fdc-131">Questo nome visualizzato deve esistere in Active Directory associato alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="27fdc-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="27fdc-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27fdc-132">-InputObject</span></span>
<span data-ttu-id="27fdc-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="27fdc-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="27fdc-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="27fdc-134">-ObjectId</span></span>
<span data-ttu-id="27fdc-135">Specifica l'ID oggetto dell'utente o del gruppo in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="27fdc-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="27fdc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27fdc-136">-ResourceGroupName</span></span>
<span data-ttu-id="27fdc-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27fdc-137">Resource group name.</span></span>

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

### <span data-ttu-id="27fdc-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27fdc-138">-ResourceId</span></span>
<span data-ttu-id="27fdc-139">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27fdc-139">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="27fdc-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27fdc-140">-WorkspaceName</span></span>
<span data-ttu-id="27fdc-141">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27fdc-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="27fdc-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27fdc-142">-Confirm</span></span>
<span data-ttu-id="27fdc-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27fdc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27fdc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27fdc-144">-WhatIf</span></span>
<span data-ttu-id="27fdc-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27fdc-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27fdc-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27fdc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27fdc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fdc-147">CommonParameters</span></span>
<span data-ttu-id="27fdc-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27fdc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fdc-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27fdc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fdc-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27fdc-150">INPUTS</span></span>

### <span data-ttu-id="27fdc-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27fdc-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="27fdc-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27fdc-152">OUTPUTS</span></span>

### <span data-ttu-id="27fdc-153">Microsoft. Azure. Commands. sinapsi. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="27fdc-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="27fdc-154">Note</span><span class="sxs-lookup"><span data-stu-id="27fdc-154">NOTES</span></span>

## <span data-ttu-id="27fdc-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27fdc-155">RELATED LINKS</span></span>
