---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 1f5c9c619c037c243246f9dec26ae2504a162d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015725"
---
# <span data-ttu-id="78e9c-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="78e9c-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="78e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="78e9c-103">Recupera informazioni su un amministratore di Azure AD per l'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78e9c-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="78e9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78e9c-104">SYNTAX</span></span>

### <span data-ttu-id="78e9c-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78e9c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78e9c-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e9c-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78e9c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e9c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78e9c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78e9c-108">DESCRIPTION</span></span>
<span data-ttu-id="78e9c-109">Il cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** ottiene informazioni su un amministratore di Azure Active Directory (Azure AD) per un'area di lavoro Analisi synapse di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="78e9c-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="78e9c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78e9c-110">EXAMPLES</span></span>

### <span data-ttu-id="78e9c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78e9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="78e9c-112">Questo comando recupera informazioni su un amministratore di Azure AD per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="78e9c-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="78e9c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78e9c-113">PARAMETERS</span></span>

### <span data-ttu-id="78e9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e9c-114">-DefaultProfile</span></span>
<span data-ttu-id="78e9c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78e9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78e9c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78e9c-116">-InputObject</span></span>
<span data-ttu-id="78e9c-117">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="78e9c-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9c-118">-ResourceGroupName</span></span>
<span data-ttu-id="78e9c-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78e9c-119">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78e9c-120">-ResourceId</span></span>
<span data-ttu-id="78e9c-121">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="78e9c-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78e9c-122">-WorkspaceName</span></span>
<span data-ttu-id="78e9c-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="78e9c-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e9c-124">CommonParameters</span></span>
<span data-ttu-id="78e9c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e9c-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78e9c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e9c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="78e9c-127">INPUTS</span></span>

### <span data-ttu-id="78e9c-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78e9c-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="78e9c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78e9c-129">OUTPUTS</span></span>

### <span data-ttu-id="78e9c-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="78e9c-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="78e9c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="78e9c-131">NOTES</span></span>

## <span data-ttu-id="78e9c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78e9c-132">RELATED LINKS</span></span>
