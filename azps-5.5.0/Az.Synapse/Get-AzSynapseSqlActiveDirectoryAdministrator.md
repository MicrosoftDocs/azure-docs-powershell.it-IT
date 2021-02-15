---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197374"
---
# <span data-ttu-id="47641-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47641-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="47641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47641-102">SYNOPSIS</span></span>
<span data-ttu-id="47641-103">Recupera informazioni su un amministratore di Azure AD per l'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="47641-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="47641-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47641-104">SYNTAX</span></span>

### <span data-ttu-id="47641-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47641-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47641-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47641-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47641-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47641-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47641-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47641-108">DESCRIPTION</span></span>
<span data-ttu-id="47641-109">Il cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** ottiene informazioni su un amministratore di Azure Active Directory (Azure AD) per un'area di lavoro Analisi synapse di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="47641-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="47641-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47641-110">EXAMPLES</span></span>

### <span data-ttu-id="47641-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47641-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="47641-112">Questo comando recupera informazioni su un amministratore di Azure AD per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="47641-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="47641-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47641-113">PARAMETERS</span></span>

### <span data-ttu-id="47641-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47641-114">-DefaultProfile</span></span>
<span data-ttu-id="47641-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47641-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47641-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47641-116">-InputObject</span></span>
<span data-ttu-id="47641-117">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="47641-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47641-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47641-118">-ResourceGroupName</span></span>
<span data-ttu-id="47641-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47641-119">Resource group name.</span></span>

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

### <span data-ttu-id="47641-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47641-120">-ResourceId</span></span>
<span data-ttu-id="47641-121">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="47641-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="47641-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47641-122">-WorkspaceName</span></span>
<span data-ttu-id="47641-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="47641-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="47641-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47641-124">CommonParameters</span></span>
<span data-ttu-id="47641-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47641-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47641-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47641-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47641-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="47641-127">INPUTS</span></span>

### <span data-ttu-id="47641-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="47641-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="47641-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47641-129">OUTPUTS</span></span>

### <span data-ttu-id="47641-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="47641-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="47641-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="47641-131">NOTES</span></span>

## <span data-ttu-id="47641-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47641-132">RELATED LINKS</span></span>
